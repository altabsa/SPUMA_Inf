---
title: "Baza danych"
permalink: /docs/manual-dbhelp/
excerpt: "Dokumetacja SPUMA - podręcznik bazy danych"
---

# Tabele systemowe
> opis tabel systemowyxh

# Funkcje i procedury
Część zaawansowanych funkcjonalności systemu SPUMA konfiguruje się za pomocą procedur i funkcji SQL. 

> **Uwaga !!!**:
>  -  Modyfikacje procedur najlepiej zlecić osobom technicznym, znającym język SQL oraz strukturę bazy danych SPUMA
>  - Zabronione jest zmienianie danych w bazie bezpośrednio - za pomocą instrukcji `INSERT`, `UPDATE` i `DELETE`
>  - Przy edycji procedur i funkcji zalecane jest stosowanie komentarzy opisujących wprowadzone zmiany do standardowej funkcjonalności.

## APR_TRANSACTION - Obsługa transakcji  SQL
- **Działanie:** Reagowanie na zmiany w bazie danych - odpowiednik wyzwalaczy SQL
- **Obowiązkowa:** Nie
- **Opis:**
  Każdy wpis w bazie (zmiana, dodanie, usuwanie), wywołuje powyższą procedurę 2 razy. 
  
  Za pierwszym razem uruchamiana jest przed zapisaniem zmian do bazy (dane przed zmianą).  Za drugim razem, po zapisie do bazy (dane po zmianie) , ale przed zatwierdzeniem transakcji. Procedura  umożliwia anulowanie  zapisu  pod zadanymi warunkami, może więc działać, jako zaawansowana walidacja poprawności zapisanych danych. Stosowana jest również, do wykonania dodatkowych wpisów (np w bazie ERP), zaraz po zmianie w bazie SPUMA.
- **Parametry wejściowe:**
  - `@optype` - rodzaj operacji:

    | Rodzaj operacji | Opis |
    | ------- | ---- |
    | **A**| Po dodaniu |
    | **AB**| Przed dodaniem |
    | **U**| Po zmianie |
    | **UB**| Przed zmianą |
    | **D**| Przed skasowaniem |

  - `@users_id` -  id użytkownika dokonującego zmiany
  - `@objecttype` - Nazwa obiektu (patrz [Obiekty SPUMA](../manual-objects))
  - `@objectid` - id obiektu w którym odbywa się zmiana

- **Oczekiwane wyjście:**
  - Pusty tekst `''` - Transakcja jest zatwierdzana. Wszystkie dane zostaną zapisane
  - Dowolny tekst - Transakcja jest anulowana i dane nie będą zapisane. Aplikacja WWW wyświetla podany tekst w okienku dialogowym

- **Przykłady** 
  - Sprawdzenie czy suma planowana (atrybut nagłówka `sumap` nie jest większa niż 10 000.

    Wpis w procedurze:
    ```sql
    if @optype = 'U' and @objecttype = 'WFDocument' BEGIN
    	DECLARE 
     		@cls_id int,
     		@cls_name nvarchar(100),
     		@cmp_id int,
     		@attr_id int,
     		@attr_value float = 0;
         -- pobranie id i nazwy klasy oraz firmy oraz id atrybutu 	
     	SELECT 
     		@cls_id = a.classes_id, 
     		@cls_name = b.[name], 
     		@cmp_id = a.companies_id,
     		@attr_id = c.id 		
     	FROM DOCUMENTS a 
     	JOIN CLASSES b  on a.classes_id = b.id 
     	JOIN CLASSATTRIBS c ON 
            c.objtype=0 and 
            c.[objid] = b.id and 
            c.iscolumn=0 and 
            upper(c.[name]) like 'SUMAP'
     	WHERE a.id = @objectid;	
     
     	IF UPPER(@cls_name) like N'ZAMOWIENIA'
     	BEGIN
     		-- pobranie vartość atrybutu sumap
    		BEGIN TRY
     			SELECT 
     				@attr_value = cast([value] as float)
     			FROM DOCUMENTS_PROPERTIES 
     			WHERE documents_id=@objectid and attribs_id = @attr_id
    		END TRY 
    		BEGIN CATCH 
     			set @attr_value  = 0;
    		END CATCH
     		-- wyświetlenie informacji
     		IF @attr_value > 10000 
     		BEGIN
     			select N'Wartość zamówienia nie może przekraczać 10 000 !!!';
    			return;
     		END
         END
     END
    ```    

- **Uwagi** 
  - Można łatwo sprawdzić  jakie parametry są przekazywane do procedury. Wystarczy na początku wpisać atrybuty do technicznej tabeli przez polecenie:
    ```sql
    insert into APB_DEBUG(optype,users_id,objecttype,objectid)
    values(@optype,@users_id,@objecttype,@objectid);  
    ```

## APR_GETUSER_ALERTS - własne alarmy
- **Działanie:** Wyświetlanie własnych alarmów
- **Obowiązkowa:** Nie
- **Opis:**
  SPUMA ma wbudowany mechanizm wyświetlania alarmów. Standardowo wyświetlają się informacje o nieprzeczytanych wiadomościach, dokumentach do skomentowania, błędach OCR itp.  Procedura `APR_GETUSER_ALERTS` umożliwia utworzenie własnych alarmów. Procedura wywoływana jest przez SPUMA co określony interwał i wyświetla zwrócone dane w aplikacji WWW, w zakładce alarmy. Alarmy zawsze związane są z dokumentami
- **Parametry wejściowe:**
  - `@users_id` -  id zalogowanego użytkownika
  - `@auto` - Nieobsługiwane (zawsze 0)

- **Oczekiwane wyjście:**
  Tabela która w wierszach zawiera identyfikatory dokumentów oraz nazwy alarmów (po których wynik jest grupowany). Tabela musi zawierać kolumny:
  -  `folderpath` - nazwa alarmu w postaci ścieżki.
    >Przykład:  Jeśli  w kolumnie `folderpath`  zwrócony zostanie np tekst `Faktury\Przetreminowane` alarm wyświetlony zostanie w postaci drzewka:
    > ```ruby
    > ├── Faktury
    > │   ├── Przeterminowane (1)
    > ```
  - `document_id` - identyfikator dokumentu
  - `sumcount` - czy ilość dokumentów dzieci sumować w rodzicu (`1` tak, `0` nie)
  - `isalarm`- czy ilość dokumentów sumować w liczniku alarmu  (`1` tak, `0` nie)

- **Przykłady** 
  - Alarm pokazujący niezaksięgowane faktury w ERP.
  
    Założenia:    
    - Id klasy faktura: `6`
    - Nazwa atrybutu z numerem zapisu w ERP : `NRSAP`. Jesli jest pusta dokument nie został dodany do ERP
 
    Skrypt:
    
    ```sql
    DECLARE 
    		@class_id int =6,
    		@attr_id int;
    SELECT 
    		@attr_id = id 
    FROM CLASSATTRIBS 
    WHERE 
     	objtype=0 and [objid]=@class_id and iscolumn=0 and upper([name]) like 'NRSAP'
         
    	insert @ret
   		SELECT 
   		  'Faktury\Do zaksięgowania',a.id,0,0
   		FROM DOCUMENTS a
   		JOIN dbo.[AFN_USERDOCS](@users_id) b ON a.id = b.id
   		WHERE 
   			a.id not in (
   				select DISTINCT documents_id 
   				from DOCUMENTS_PROPERTIES a 
   				where 
   					isnull([value],'') < '' and 
   					attribs_id = @attr_id
   			) and
   			a.classes_id=@class_id and 
   			a.docstatus=3 
    	if exists(select 1 from @ret) select * from @ret
    
    ```
   
   

- **Uwagi**
  - Użycie w skrypcie funkcji `AFN_USERDOCS` zapewnia pokazywanie tylko dokumentów do których użytkownik ma dostęp


## APR_FORMATEMAIL - Wygląd maili
- **Działanie:** Formatowanie wiadomości wychodzących
- **Obowiązkowa:** Tak
- **Opis:**
  SPUMA przed wysłaniem mail'a uruchamia powyższą procedurę i na podstawie wyniku generuje wiadomość w postaci HTML. SPUMA jest instalowana z predefiniowaną procedurą `APR_FORMATEMAIL`. Zaleca wprowadzanie zmian tylko w obrębie kolumny `BODY`

- **Parametry wejściowe:**
  - `@messages_id` -  id wiadomości która jest wysyłana

- **Oczekiwane wyjście:**
  Wiersz który zawiera następujące kolumny:
  
  | Kolumna | Opis |
  | ------- | ---- |
  | **SUBJECT** | Temat wiadomości 
  | **TO** | Adresy email odbiorców (rozdzielane średnikami) 
  | **FROM** | Adres nadawcy
  | **CC** | Adresy email "do wiadomości" (rozdzielane średnikami) 
  | **CC** | Adresy email "ukryty" (rozdzielane średnikami) 
  | **BODY** | Treść maila

- **Uwagi**
  - W kolumnie `BODY` pod ciąg znaków `{DOCSIG}` podstawiany jest unikatowy numer sygnatury dokumentu który pozwala w mailu utworzyć link bezpośrednio do dokumentu związanego z wiadomością

## APR_EXOBJPREVIEW - Podgląd dokumentów połączonych
- **Działanie:** Formatowanie podglądu dla zakładki `Dokumenty połączone`
- **Obowiązkowa:** Tak
- **Opis:**
  SPUMA  w aplikacji WWW pokazuje na zakładce `Dokumenty połączone` pokazuje podgląd dokumentu z zewnętrznego systemu ERP (np SAP Business One). Aby określić format tego podglądu wywoływana jest w.w. procedura i jej wynik jest pokazywany. `APR_EXOBJPREVIEW` wywoływana jest 2 razy. Za pierwszym razem wywołanie jest dla danych nagłówka i parametr `@view_type = H`. Zwrócona tabela powinna zawierać jeden wiersz i pokazywana jest w formacie:
  
  | | |
  |---|---|
  | **Kolumna 1** | Wartość
  | **Kolumna 2** | Wartość 2
  | **Kolumna 3** | Wartość 3

  Drugie wywołanie (parametr ` @view_type = H`) pobiera dane która pokazuje linie dokumentu z ERP.  Tabela pokazywana jest standardowo
  
  | **Kolumna 1** | **Kolumna 2** | **Kolumna 3** |
  |---|---|---|
  | Wartość 1 wiersz 1 | Wartość 2 wiersz 1 | Wartość 3 wiersz 1 |
  | Wartość 1 wiersz 2 | Wartość 2 wiersz 2 | Wartość 3 wiersz 2 |


- **Parametry wejściowe:**
  - `@view_type` -  id wiadomości która jest wysyłana
  - `@documentrefs_id` -  id wpisu z tabeli połączeń z ERP `DOCUMENTREF`

- **Oczekiwane wyjście:**
  W przypadku `@view_type=H` wiersz który zawiera dowolne kolumny.
  W przypadku `@view_type=L` tabela która zawiera dowolne kolumny. 

- **Uwagi**
  - Nazwa kolumny w przypadku linii może decydować również o formacie kolumny. Można użyć nazwy w poniższym formacie
  
    ```batch
    nazwa_kolumny$$A;B;format
    ```
    
    gdzie: 
     
    `A` - wyrównanie kolumny (domyślnie do lewej)    
     
    |  Wyrównanie | Opis |
    | --- | --- |
    | **R** | Do prawej |
    | **C** | Wycentrowane |
   
    `B` - Rodzaj wartości (domyślnie tekst)
     
    |  Rodzaj | Opis |
    | --- | --- |
    | **I** | Numer |
    | **F** | Liczba |
    | **D** | Data |
    | **format** | Format wartości |

- **Przykłady:** 
  - Kolumna o nazwie `Wartość` z liczbami 2 miejsca po przecinku
    ```
    Ilość$$R;F;0.00
    ```
  - Kolumna o nazwie `Nr linii` wyrównana do prawej
    ```
    Nr Linii$$R;I
    ```
  - Kolumna o nazwie `Dostawa` wyśrodkowana (tylko data)
    ```   	
    Dostawa$$C;D;yyyyMMdd`
    ```
 
## APR_DICTIONARYVALUES - słowniki systemowe
- **Działanie:** Pobranie danych do słowników systemowych
- **Obowiązkowa:** Nie
- **Opis:**
  SPUMA podczas uruchamiania aplikacji WWW pobiera wypełnia słowniki systemowe. Dane pobierane są przez uruchomienie w.w procedury dla każdego ze słowników systemowych

- **Parametry wejściowe:**
  - `@companiesdicts_id` -  id słownika systemowego  (z tabeli `COMPANIESDICTS`)

- **Oczekiwane wyjście:**
  Tablica wartości słownikowych z dwoma kolumnami `value` i `description`

## APR_BEFOREOCRFILL - zarządzanie wynikami OCR
- **Działanie:** Procedura wywoływana jest przed przepisaniem pól rozpoznanych przez OCR do własności dokumentów.
- **Obowiązkowa:** Nie
- **Opis:**
  SPUMA po przetworzeniu dokumentu przez mechanizm OCR sprawdza pola które ten mechanizm rozpoznał. Na podstawie definicji atrybutów klasy ( patrz `Pole schematu` [Klasy / Atrybuty](../manual-reference#klasy_atrybuty) ) przepisuje rozpoznane wartości do określonych pól. Zanim przepisze uruchamia ww procedurę. Umożliwia to zmianę wartości rozpoznanych przez OCR przed przepisaniem ich do atrybutów.

- **Parametry wejściowe:**
  - `@documents_id` -  id dokumentu
  - `@classes_id` -  id klasy dokumentu

- **Oczekiwane wyjście:**
  Zmieniona tablica tymczasowa `#NVALUES`

- **Uwagi**
  Przed wywołanie procedury tworzona jest tabela tymczasowa o nazwie `#NVALUES`
  
  Przykład:
  
  | pcode | pvalue |
  | --- | --- |
  | SYS_DOCNUM | 31/1/2/061190|
  | SYS_DOCDATE | 02-01-2012 |
  | PH| D102<!>ACME S.A<!>ul. Polna 32<!>Warszawa<!>02672<!>Poland |
  | Termin | 30-01-2012 |

  - Pola `SYS_DOCNUM ` i `SYS_DOCDATE`  są przekazywane zawsze
  - Pole `PH` jest przekazywane tylko wtedy kiedy klasa ma atrybut własny
  - Reszta pól jest przekazywana tylko wtedy, gdy atrybut  ma określone pola OCR  we własności  `Pole schematu`.

- **Przykłady** 
  - Z numeru dokumentu należy usunąć wszystko, co nie jest cyfrą albo znakami `/-\`. Id klasy = `6`

    Wpis do procedury `APR_BEFOREOCRFILL`:
    ```sql
    IF (@classes_id = 6)
    BEGIN
	DECLARE @nr nvarchar(200)
	SELECT  @nr = pvalue FROM #NVALUES WHERE pcode='SYS_DOCNUM';
	WHILE PATINDEX('%[^0-9/-\]%', @nr) > 0
	    SET @nr = REPLACE(@nr, SUBSTRING(@nr, PATINDEX('%[^0-9/-\]%', @nr), 1), '' )
	update #NVALUES set pvalue=@nr where pcode='SYS_DOCNUM';
    END
    ```

## <a id='funkcje_sql_findlinevalues' hidden='true'></a> APR_FINDLINEVALUES - modyfikacja wyników OCR dla linii
- **Działanie:** Modyfikacja wartości atrybutów przy operacja `kopiuj do linii`
- **Obowiązkowa:** Nie
- **Opis:**
  Procedura opcjonalna. Wywoływana przy operacji `kopiuj do linii` gdy przynajmniej jedna z kolumn ma ustawioną operację mapowania `Zapamiętaj`. Służy do ewentualnej modyfikacji mechanizmu przepisywania wartości OCR
- **Parametry wejściowe:**
  - `@documents_id` -  id dokumentu
  - `@class_id` -  id klasy dokumentu
  - `@cardcode` -  kod klienta (jeśli klasa dokumentu ma atrybut własny)

- **Oczekiwane wyjście:**
  Zmieniona tablica tymczasowa `#LINEVALUES`

- **Uwagi** 
  Przed wywołanie procedury tworzona jest tabela tymczasowa o nazwie `#LINEVALUES` zawierająca wszystkie wartości wybranej kolumny
  
  Przykład:
  
  | AttribCode | OldValue | NewValue |
  | --- | --- | --- |
  | Indeks | Ksero Kolorowe | MAT_BIUR |
  | Indeks | DYPLOM NA PODKŁADZIE DREWNIANYM | MAT_BIUR |
  | Indeks | Kurier DHL| U_TRANSPORT |
   
  Gdzie
  - `Indeks` - nazwa kolumny (operację `Zapmiętaj` można wybrać dla więcej niż jednej kolumny)
  - `OldValue` - wartość z OCR
  - `NewValue` - nadpisana wartość

## AFN_FIND_DOCUMENTS - wyszukiwanie dokumentów
- **Działanie:** Funkcja wywoływana przy wyszukiwaniu dokumentów wg słów kluczowych z poziomu aplikacji WWW.
  > **Uwaga!!!:** Funkcja jest zakładana przy instalacji. Jej zmiana nie jest zalecana. Wymaga dużej znajomości mechanizmów SQL oraz struktury bazy SPUMA
 
- **Obowiązkowa:** Tak
- **Opis:**
  Funkcja wyszukuje w tabeli `resources`  w kolumnie `keywords` słów wpisanych w  polu `szukaj` w aplikacji WWW. Bierze dodatkowo pod uwagę  użycie specjalnych słów kluczowych w postaci:
  ```
   ?nazwa_atrybutu:tekst_szukany
  ```
 
- **Parametry wejściowe:**
  
  - `@keywords` -  Tekst wpisany w  polu `szukaj`.
  - `@indocname` - Szukaj w nazwie dokumentu (`Y` - tak, `N` - nie)
  - `@indocdesc` - Szukaj w opisie dokumentu (`Y` - tak, `N` - nie)
  - `@indocnum` - Szukaj w numerze  dokumentu (`Y` - tak, `N` - nie)
  - `@inkeywords` - Szukaj w tekście (`Y` - tak, `N` - nie)
  - `@incomments` - Szukaj w komentarzach (`Y` - tak, `N` - nie)

- **Oczekiwane wyjście:**
  Tablica identyfikatorów dokumentów. Kolumny:
  - `docid` - identyfikator dokumentu
  - `frac` -  trafność wyszukiwania (wartość od 0 do 1)


## AFN_SUGEST_PARTNERS - wyszukiwanie klienta
- **Działanie:** Funkcja zwraca tabele proponowanych dla dokumentu partnerów handlowych.
- **Obowiązkowa:** Tak
- **Opis:**
   Kiedy Partnerzy Handlowi rejestrowani są lokalnie (ustawienie `baza wewnętrzna` w   [konfiguracji firmy](../manual-reference#firmy1)) funkcja wywoływana jest z bazy `SPUMA`. W przypadku ustawienia `zewnętrzny SOAP` uruchamiany jest z bazy ERP (np SAP Business One) 

- **Parametry wejściowe:**
  - `@val` -  Tekst wyodrębniony przez mechanizm OCR
  - `@addkwords` - Pola rozpoznane  przez mechanizmu OCR. 

- **Oczekiwane wyjście:**
  Tekst - 250 znaków
- **Uwagi:**
  Parametr `addkwords` zwracany jest w postaci: 
  
  `pole:wartośc;pole2:wartosc` 

  Przykład: 
  ```
  INVOICENUMBER:1711080067982;
  NIP:527-10-37-727;
  INVOICEDATE:11-10-2017;
  DUEDATE:24.11.2017;
  TOTALAMOUNT:1 973,94;
  ACCOUNT:09 1240 6960 0601 0000 1407 6681
  ```

## <a id='funkcje_sql_suggestocrmap' hidden='true'></a>AFN_SUGGESTOCRMAP - mapowanie pól OCR
- **Działanie:** Funkcja zwracająca propozycje mapowania kolumn do atrybutów linii
- **Obowiązkowa:** Tak
- **Opis:** 
- **Parametry wejściowe:**
  - `@document_id` -  Identyfikator dokumentu
  - `@class_id` -  Identyfikator klasy
  - `@cardcode` -  kod klienta (jeśli klasa dokumentu ma atrybut własny)
  - `@schemacode` -  kod schematu OCR

- **Oczekiwane wyjście:**
  Tablica mapowania kolumn do atrybutów. Kolumny:
  - `OcrCode` - Nazwa kolumny 
  - `AttribCode` -  Nawa atrybutu
  - `MapType` -  Kod operacji:
    
    | MapType | Opis |
    | --- | --- |
    | `0` | Nie kopiuj |
    | `1` | Kopiuj |
    | `2` | Wyszukaj |
    | `3` | Zapamiętaj |


## AFN_USERDOCS - uprawnienia do dokumentów
- **Działanie:** Funkcja techniczna. Zwraca identyfikatory dokumentów do których użytkownik ma dostęp
- **Obowiązkowa:** Nie
- **Opis:**
  Funkcja powinna być używana w zapytaniach i procedurach własnych aby zapewnić dostęp do dokumentów tylko dla uprawnionych użytkowników
- **Parametry wejściowe:**
  - `@userid` -  Identyfikator użytkownika

- **Oczekiwane wyjście:**
  Tabela identyfikatorów dokumentów (kolumna `id`)

## AFN_SUGGEST_CARDCODE - kod klienta
- **Działanie:** Funkcja zwraca unikatowy kod używany podczas zakładania klienta przez atrybut własny z aplikacji WWW.
- **Uwaga!!!:** Funkcja jest używana tylko gdy Partnerzy Handlowi rejestrowani są w  bazie SPUMA (ustawienie `baza wewnętrzna` w   [konfiguracji firmy](../manual-reference#firmy1))
- **Obowiązkowa:** Tak
- **Opis:**
  Funkcja zwraca unikatowy kod (w ramach bazy SPUMA)  dla  nowego wpisu do tabeli `BUSINESSPARTNERDB`
- **Parametry wejściowe:**
  - `@dbname` -  Nazwa bazy zewnętrznej (z  [konfiguracji firmy](../manual-reference#firmy1) ).
  - `@cardtype` - Typ klienta 

    | cardtype | Opis |
    | --- | --- |
    | `S` | Dostawca |
    | `C` | Odbiorca |

- **Oczekiwane wyjście:**
  Tekst - 250 znaków
