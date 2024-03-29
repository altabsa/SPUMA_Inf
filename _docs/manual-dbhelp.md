---
title: "Baza danych"
permalink: /docs/manual-dbhelp/
excerpt: "Dokumetacja SPUMA - podręcznik bazy danych"
---

# Tabele systemowe
  > opis tabel systemowych

   | Nazwa Tabeli                 | Opis |
   | -------                      | ---- |
   | **ALLOWEDUSERS**             | Uprawnienia użytkowników do dokumentów |
   | **ATTRIBDICTS**              | Słownik atrybutów powiązanych z: klasami, dziennikiem korespondencji  |
   | **AUTHSCHEMA_INSPARAMETERS** | Proces autoryzacjia - parametry dla instrukcji (etapów) |
   | **AUTHSCHEMA_INSTRUCTIONS**  | Proces autoryzacji - instrukcje (etapy) |
   | **AUTHSCHEMA_PARVALUES**     | - |
   | **AUTHSCHEMA_PERMISSIONS**   | Proces autoryzacji - uprawnienia specjalne|
   | **AUTHSCHEMA_RECIPIENTS**    | Schemat autoryzacji - odbiorcy |
   | **AUTHSCHEMAS**              | Schematy autoryzacji  oraz procesy zatwierdzania |
   | **BUSINESSPARTNERDB**        | Wewnętrzna baza klientów SPUM'a - definicje PH|
   | **CLASS_SCHEMAS**            | Klasa - powiązane schematy autoryzacji dla klasy |
   | **CLASS_TRIGGERS**           | Klasa - powiązane wyzwalacze |
   | **CLASSATTRIBS**             | Klasa - powiązane atrybuty |
   | **CLASSES**                  | Klasa dokumentu |
   | **COLUMNSFORMATS**           | Ustawienia kolumn - format kolumny dla: raporty, dziennik korespondencji|
   | **COLUMNSMAPPING**           | Ustawienia kolumn - mapowanie parametrów dla podraportu|
   | **COMMENTENTRIES**           | Dokument - Komentarze |
   | **COMPANIES**                | Firmy - definicja podstawowa |
   | **COMPANIESDICTS**           | Firmy - słowniki |
   | **CONFIGURATION**            | Konfiguracja SPUMY |
   | **COUNTRIES**                | Wewnętrzna baza klientów SPUM'a - definicje krajów |
   | **CUSTOMPROCESS_DIALOGWND**  | Procesy UI - instrukcje typu komunikaty |
   | **CUSTOMPROCESS_EXCALLOP**   | Procesy UI - instrukcje typu wykonanie DLL|
   | **CUSTOMPROCESS_LINEOP**     | Procesy UI - instrukcje typu obsługa linii dokumentu |
   | **CUSTOMPROCESS_SCRIPTOP**   | Procesy UI - instrukcje typu skrypt SQL|
   | **CUSTOMPROCESSES**          | Procesy UI - definicja procesu |
   | **DAILYCORR_PROPERTIES**     | Dziennik korespondencji - własności dokumentu |
   | **DAILYCORR_REF**            | Dziennik korespondencji - referencje do dokumentów|
   | **DAILYCORRCLASS**           | Dziennik korespondencji - definicja klasy |
   | **DAILYCORRESPONDENCE**      | Dziennik korespondencji - wpisy dziennika |
   | **DEFINITIONS**              | Spis definicji wzorców OCR |
   | **DESIGNERCONNECTIONS**  | Opis |
   | **DESIGNERITEMS**| Opis |
   | **DICTIONARIES**             | Słowniki statyczne |
   | **DICTVALUES**               | Słowniki statyczne przypisane wartości |
   | **DIRECTORIES**		  | Katalogi dla dokumentów - definicja katalogów w firmie |
   | **DOCUMENTOCRRESULTS**	  | Dokument - wyniki rozpoznawania danych przez OCR wskazania zastosowanego szablonu OCR|
   | **DOCUMENTPAGES**		  | Dokument - powiązanie zasobów ze stronami dokumentu |
   | **DOCUMENTREF**		  | Dokument - powiązanie z dokumnentem w systemie ERP |
   | **DOCUMENTREFLINES**	  | Dokument - powiązanie z pozycjami dokumentu w systemie ERP|
   | **DOCUMENTS**		  | Dokument - podstawowe informacje dla dokumentu |
   | **DOCUMENTS_ATTACHMENTS**	  | Dokument - powiązane załączniki |
   | **DOCUMENTS_AUTHLOCKS**	  | Dokument - autoryzacje: blokada autoryzacji |
   | **DOCUMENTS_AUTHRECIPIENTS** | Dokument - autoryzacje: przypisane osoby do obiegu dokumentu |
   | **DOCUMENTS_AUTHSCHEMA**	  | Dokument - autoryzacje: przypisany schemat zatwierdzania  |
   | **DOCUMENTS_AUTHVAR_BASIC**  | Dokument - autoryzacje: zmienne podstawowe  |
   | **DOCUMENTS_AUTHVAR_SCHEMA** | Dokument - autoryzacje: zmienne schema  |
   | **DOCUMENTS_AUTHVAR_SCHEMARCP**| Dokument - autoryzacje: zmienne schema odbiorca  |
   | **DOCUMENTS_LINES**	  | Dokument linie: podstawowe informacje|
   | **DOCUMENTS_LINESOWNERS**	  | Dokument linie: uprawnienia do linii przypisanie właściciela linii |
   | **DOCUMENTS_LINESREFS**	  | Dokument linie: mapowanie wyników dla linii z OCR do linii dokumentu |
   | **DOCUMENTS_MODIFICATION**	  | Dokument - historia zmian |
   | **DOCUMENTS_OCRMAP**	  | Dokument - mapowanie wyników z OCR do dokumentu |
   | **DOCUMENTS_PROPERTIES**	  | Dokument - przypisane wartości do dodatkowych atrybutów klasy  |
   | **DOCUMENTUSAGE**		  | Dokument - historia przeglądania danego dokumentu|
   | **EXTERNALREFS**		  | Powiązanie dokumentuy SPUMA z dokumentem z zewnętrznych integracji np: IMAP, POP3, KSEF |
   | **INTERACTIVEDICTS**	  | Słowniki interaktywne |
   | **KSEF_DOCUMENTS**		  | KSEF - lista dokumentów pobranych z API |
   | **KSEF_SESSIONS**		  | KSEF - zapisane sesje logowania do API dla danego Tokena |
   | **MAILMONITORCFG**		  | Automatyzacje - Pobieranie automatyczne wiadomości z maila dla protokołu POP3 |
   | **MESSAGE_RECIPIENTS**	  | Wiadomości - powiązani odbiorcy dla danej wiadomości |
   | **MESSAGES**		  | Wiadomości - zapisane powiadomienia wewnętrzne oraz Email wysłane ze SPUMA |
   | **MODIFICATIONENTRY**	  | Historia zmian na dokumencie |
   | **MODULECONFIG**		  | Konfiguracja modułów wykorzystywanych w SPUMA |
   | **OCRFIELDS**		  | OCR - rozpoznane pola nagłówka |
   | **OCRLINES**		  | OCR - rozpoznane pola linii |
   | **OCRPROCESSLOG**		  | OCR - log błędów |
   | **OCRRESULTPAGES**		  | OCR - wyniki rozpoznawania dla strony dokumentu|
   | **OCRTEXTREGIONS**		  | OCR - rozpoznane regiony dla tekstu |
   | **ORGANIZATIONS**		  | Organizacje - definicja |
   | **PAGECOMMENTS**		  | Komentarze przypisane do strony |
   | **PERMISSIONS**		  | Uprawnienia do dokumentów |
   | **PROCESS_ACTIONS**	  | Proces UI - akcje |
   | **PROCESS_CNDFUNCTS**	  | Proces UI - warunki |
   | **PROCESS_VARCOLUMNS**	  | Proces UI - zmienne kolumnowe |
   | **PROCESS_VARIABLES**	  | Proces UI - zmienne |
   | **RECONSCHEMA**		  | Nie używane poprzednia generacja SPUMY |
   | **RECONSCHEMAREQUESTADDCLASS**| Nie używane poprzednia generacja SPUMY|
   | **RECONSCHEMAREQUESTPAGES**  | Nie używane poprzednia generacja SPUMY|
   | **RECONSCHEMAREQUESTS**      | Nie używane poprzednia generacja SPUMY |
   | **RESOURCES**		  | Źródła - zaimportowane pliki do SPUMY|
   | **SIGNATURES**		  | Sygnatury nadane użytkownikowi dla dokumentu na określony czas |
   | **STATES**			  | Wewnętrzna baza klientów SPUM'a - definicje  |
   | **USERGROUPS**		  | Grupy użytkowników - definicja|
   | **USERGROUPUSERS**		  | Grupy użytkowników - przypisanie osób |
   | **USERS**			  | Użytkownicy - definicja|
   | **USERS_DOCINTERFACECONFIGS**| Wymiana EDokumentów dodatkowe integracje |
   | **USERS_EVENTRESTRICTIONS**  | Użytkownik - wyłączenie powiadomień |
   | **USERS_FAVORITEDOCUMENTS**  | Użytkownik - dokumenty ulubione lub obserwowany |
   | **USERS_PERMISSIONS**	  | Użytkownik - uprawnienia do firm |

  > Opis kolumn:

### Tablica **ALLOWEDUSERS**

   | Kolumna | Typ danych  | Odwołanie| Opis |
   | ------- | ---- | ----- | ------|
   | **documents_id**| int | DOCUMENTS **id** | numer dokumentu |
   | **users_id**| int | USERS **id**| kod użytkownika |

### Tablica **ATTRIBDICTS**

   | Kolumna | Typ danych  | Odwołanie| Opis |
   | ------- | ---- | ----- | ------|
   |**classattribs_id**| 	int | CLASSESS **id**| numer atrybutu klasy |
   |**companies_id**| 	int | COMPANIES **id** | numer firmy |
   |**companiesdicts_id**| 	int | COMPANIESDICTS **id** | kod słownika powiązanego z firmą|

### Tablica **AUTHSCHEMA_INSPARAMETERS** 

   | Kolumna          | Typ danych | Odwołanie      | Opis |
   | -------          | ----- | --------------------| ------|   
   |**authschemas_id**| 	int | AUTHSCHEMAS **id**  | powiazanie ze schematem autoryzacji |
   |**insintid**      | 	int |                     | numer kolejny instancji parametru |
   |**intid**         | 	int |                     |             |
   |**name**          | 	varchar (100) | | nazwa parametru wejsciowego 
   |**description**   | 	ntext | | opis parametru wejsciowego
   |**type**          | 	int |                     | typ |
   |**allownull**     | 	bit |                     | czy wymagany |
   |**variable_id**   | 	int |                     | kod zmiennej |
   |**objtype**       | 	int |                     | typ obiektu (parametru): **0** - Wszyscy **1** - grupa zdefiniowana **2** Grupa własna |
   |**objid**         | 	int | USERGROUPS **id**   | kod obiektu powiązanego  |

### Tablica **AUTHSCHEMA_INSTRUCTIONS** 

   | Kolumna          | Typ danych  | Odwołanie| Opis |
   | -------          | ----        | ----- | ------|  
   |**authschemas_id**| 	int       | AUTHSCHEMAS **id**|powiazanie ze schematem autoryzacji |
   |**intid**         | 	int       |                   | numer kolejnej instrukcji w obrębie danego procesu autoryzacji |
   |**name**          | 	nvarchar (100) |                   | nazwa instrukcji
   |**description**   | 	ntext     |                   | opis instrukcji
   |**type**          | 	int       |                   | rodzaj instrukcji **0** - autoryzacja podstawowa  **1** - autoryzacja parametryzowana
   |**objid**         | 	int       | objtype=0: USERS **id** , objtype=1: AUTHSCHEMAS **id**   | kod powiązanego obiektu
   |**objtype**       | 	int       |                   | typ obiektu: **0** - Użytkownik zdefiniowany  **1** - Schemat zdefiniowany **2** - Użytkownik (przekazana zmienna)
   |**addinfo**       | 	nvarchar (max) |                   | dodatkowe informacje
   |**variable_id**   | 	int       |                   |

### Tablica **AUTHSCHEMA_PARVALUES** 

   | Kolumna          | Typ danych  | Odwołanie| Opis |
   | -------          | ----        | ----- | ------|  
   |**authschemas_id**| 	int       |AUTHSCHEMAS **id**| powiazanie ze schematem autoryzacji
   |**insintid**      | 	int       |                   |
   |**prmintid**      | 	int       |                   | 
   |**value**         | 	nvarchar (255) |                   | wartość
   |**description**   | 	nvarchar (512) |                   | opis

### Tablica **AUTHSCHEMA_PERMISSIONS** 

   | Kolumna          | Typ danych  | Odwołanie| Opis |
   | -------          | ----        | ----- | ------| 
   |**authschemas_id**| 	int |AUTHSCHEMAS **id**| powiazanie ze schematem autoryzacji
   |**documents_id**  | 	int | DOCUMENTS **id** | powiązanie z dokumentem
   |**attribs_id**    | 	int | ATTRIBDICTS **id** | powiązanie z atrybutem klasy lub systemowymi polami: **-1** [nazwa], **-2** [opis], **-3** [numer], **-4** [klasa] **-5** [schemat zatwierdzania] , **-6** [data dokumentu] **-7** [data wejscia]
   |**allow**         | 	bit |                    | **0** - zablokuj, **1** - zezwól 
   |**objid**         | 	int |USERS **id**, USERGROUPS **id**, AUTHSCHEMAS **id** | odwołanie do powiązanego obiektu
   |**objtype**       | 	int |                    |typ obiektu: **0** - użytkownik, **1** - grupa użytkowników, **2** - schemat autoryzacji **3** - numer etapu autoryzacji
   |**authmode**      | 	int |                    | **0** - nagłówek **1** linie
   |**authseq**       | 	int |                    | 
   |**proptype**      | 	int |                    |**0** - główne, **1** - przenaszalność **7** - edycja obcych linii, **10** - dodanie nowej strony
   |**order**         | 	int |                    | kolejność uprawnienia

### Tablica **AUTHSCHEMA_RECIPIENTS** 

   | Kolumna          | Typ danych  | Odwołanie| Opis |
   | -------          | ----        | ----- | ------| 
   |**authschemas_id**| 	int |AUTHSCHEMAS **id**  | powiazanie ze schematem autoryzacji
   |**objid**         | 	int |USERS **id**, USERGROUPS **id**, AUTHSCHEMAS **id** | odwołanie do powiązanego obiektu
   |**objtype**       | 	int |                    | Typ obiektu **0** - użytkownik, **1** - grupa użytkowników, **2** - schemat autoryzacji  
   |**order**         | 	int |                    | kolejność
   |**id**            | 	int |                    | numer kolejny
   |**marktodel**     | 	bit |                    |
   |**addinfo**       | 	nvarchar(max) |          | dodatkowe informacje

### Tablica **AUTHSCHEMAS** 

   | Kolumna            | Typ danych      |    Odwołanie       | Opis |
   | -------            | ----            | -----              | ------| 
   |**id**              | 	int           |                    |unikalny numer
   |**name**            | 	nvarchar(100) |                    | nazwa schematu
   |**description**     |  	ntext         |                    | opis schematu
   |**authmethodtype**  | 	int           |                    | rodzacj schematu: **0** - wszyscy z, **1** - jeden z, **2** - (n) z, **3** - proces autoryzacji
   |**CreatedAt**       | 	datetime      |                    | data utworzenia
   |**UpdatedAt**       | 	datetime      |                    | data aktualizacji
   |**authusrlimit**    | 	int           |                    | limit odbiorcow dla typu **2**
   |**headereditmode**  | 	int           |                    | tryb edycji nagłówka dokumentu
   |**lineseditmode**   | 	int           |                    | tryb edycji linii dokumentu
   |**headereditmode1** | 	int           |                    |
   |**lineseditmode1**  | 	int           |                    |
   |**headereditmode2** | 	int           |                    |
   |**lineseditmode2**  | 	int           |                    |
   |**addinfo**         | 	nvarchar(max) |                    | dodatkowe informacje
   |**organizations_id**| 	int           |ORGANIZATIONS **id**| powiązanie z organizacją
   |**globalid**        | 	varchar(36)   |                    | unikalny identyfikator
   |**usergroup_id**    | 	int           | USERGROUPS **id**  | powiązanie z grupą użytkowników (dla schematów utworzonych automatycznie na podstawie grupy)

### Tablica **BUSINESSPARTNERDB** 

   | Kolumna      | Typ danych      |    Odwołanie       | Opis |
   | -------      | ----            | -----              | ------| 
   |**DBName**    | 	varchar(128)  |                    | nazwa bazy danych
   |**CardCode**  | 	nvarchar(256) |                    | kod klienta
   |**CardType**  | 	varchar(1)    |                    | typ klienta
   |**CardName**  | 	nvarchar(1024)|                    | nazwa klienta
   |**CardFName** | 	nvarchar(1024)|                    | nazwa obca klienta
   |**FTaxID**    | 	varchar(32)   |                    | numer NIP
   |**FreeText**  | 	nvarchar(max) |                    |dodatkowe informacje o kliencie
   |**DStreet**   | 	nvarchar(128) |                    |adres dostawy: nr ulicy z numerem
   |**DCountry**  | 	varchar(32)   |                    |adres dostawy: państwo
   |**DState**    | 	varchar(32)   |                    |adres dostawy: województwo
   |**DZipCode**  | 	varchar(32)   |                    |adres dostawy: kod pocztowy
   |**DCity**     | 	nvarchar(128) |                    |adres dostawy: miasto
   |**BStreet**   | 	nvarchar(128) |                    |adres faktury: nr ulicy z numerem
   |**BCountry**  | 	varchar(32)   |                    |adres faktury: państwo
   |**BState**    | 	varchar(32)   |                    |adres faktury: województwo
   |**BZipCode**  | 	varchar(32)   |                    |adres faktury: kod pocztowy
   |**BCity**     | 	nvarchar(128) |                    |adres faktury: miasto
   |**SyncStatus**| 	int           |                    |status synchronizacji

### Tablica **CLASS_SCHEMAS** 

   | Kolumna    | Typ danych  |    Odwołanie      | Opis |
   | -------    | ----        | -----             | ------| 
   |**classes_id**     | 	int | CLASSES **id**    | powiązanie z klasą
   |**authschemas_id** | 	int |AUTHSCHEMAS **id** | powiązanie ze schematem autoryzacji

### Tablica **CLASS_TRIGGERS** 

   | Kolumna            | Typ danych     |    Odwołanie       | Opis |
   | -------            | ----           | -----              | ------| 
   |**classes_id**      | 	int          | CLASSES **id**     | powiązanie z klasą
   |**name**            | 	varchar(100) |                    | nazwa 
   |**description**     | 	ntext        |                    | opis
   |**label**           | 	nvarchar(max)|                    | etykieta wyświetlana na formatce
   |**order**           | 	int          |                    | kolejność
   |**classattribs_id** | 	int          | ATTRIBDICTS **id** | powiązanie z atrybutem lub systemowo **-2** - nagłówek, **-1** - linie

### Tablica **CLASSATTRIBS** 

   | Kolumna                | Typ danych      |    Odwołanie       | Opis |
   | -------                | ----            | -----              | ------| 
   |**id**                  | 	int           |                    |numer unikalny
   |**name**                | 	varchar(100)  |                    |nazwa atrybutu
   |**description**         | 	ntext         |                    |opis atrybutu
   |**regex**               | 	ntext         |                    |wzór dozwolonego wpisanego formatu tekstu w formie regex
   |**datatype**            | 	int           |                    |typy danych: **1** - float, **2** - tekst, **3** - DataCzas, **4** - własny, **5** - słownik systemowy, **6** - słownik użytkownika, **7** - słownik interaktywny, **8** - słownik statyczny, **9** - Długi tekst
   |**marktodel**           | 	bit           |                    |
   |**extensions_id**       | 	int           |                    | powiązane rozszerzenie
   |**order**               | 	int           |                    | kolejność
   |**mandatory**           | 	bit           |                    | czy obowiązkowy
   |**schemafcode**         | 	varchar(100)  |                    | pole schematu OCR
   |**erpfcode**            | 	varchar(100)  |                    | powiązanie z polem DI ERP
   |**iscolumn**            | 	bit           |                    | czy kolumna **0** - nie, **1** - tak
   |**evalctx**             | 	varchar(1024) |                    |formuła auto wyliczania
   |**allowcustomval**      | 	bit           |                    | dowolne wartości  **0** - nie, **1** - tak
   |**interactivedicts_id** | 	int           |INTERACTIVEDICTS **id**| powiązanie ze słownikiem interaktywnym
   |**label**               | 	nvarchar(max) |                    | etykieta
   |**visorder**            | 	int           |                    | kolejność wyświetlania na formatce
   |**defwidth**            | 	int           |                    | szerokość (atrybuty linii) 
   |**adder**               | 	bit           |                    |
   |**objtype**             | 	int           |                    | typ obiektu **0** - klasa dokumentu, **1** - dziennik korespondencji, **2** - raport
   |**objid**               | 	int           |CLASSES **id**, DAILYCORRCLASS **id**, INTERACTIVEDICTS **id** |kod powiązanego obiektu
   |**cmp_classattribs_id** | 	int           |                    | sumator powiazanie z atrybutem liczbowym z nagłówka
   |**allowgroup**          | 	bit           |                    | grupowanie

### Tablica **CLASSES** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**                | 	int           |                    |numer unikalny
   |**name**              | 	nvarchar(100) |                    | nazwa klasy
   |**description**       | 	ntext         |                    | opis klasy
   |**regex**             | 	ntext         |                    | dopasowanie
   |**allowcustomschema** | 	bit           |                    |czy dostępny schemat własny
   |**CreatedAt**         | 	datetime      |                    | data utworzenia
   |**UpdatedAt**         | 	datetime      |                    | data aktualizacji
   |**nameformat**        | 	nvarchar(255) |                    | format nazwy
   |**authschemas_id**    | 	int           |AUTHSCHEMAS **id**  | domyślny schemat autoryzacji
   |**prmcpmthtype**      | 	int           |                    | metoda kopiowania uprawnień: **0** - nigdy, **1** - zawsze, **2** - zapytaj
   |**authmandatory**     | 	bit           |                    | schemat jest wymagany
   |**visibility**        | 	int           |                    | widocznośc **0** - widoczna, **1** - ukryta
   |**classes_id**        | 	int           |CLASSES **id**      | powiązana klasa bazowa
   |**issys**             | 	bit           |                    | czy klasa systemowa
   |**uniqname**          | 	bit           |                    | kontrola unikalności nazwy
   |**checkformat**       | 	int           |                    |kontrola formatu nazwy: **0** - nie sprawdzaj, **1** - Pozwól edytować, **2** Automatycznie
   |**numrrequired**      | 	bit           |                    | czy numer dokumentu wymagany
   |**uniqnum**           | 	bit           |                    | kotrola unikalności numeru
   |**color**             | 	int           |                    |kolor
   |**organizations_id**  | 	int           |ORGANIZATIONS **id**| powiązana organizacją
   |**globalid**          | 	varchar(36)   |                    | unikalny kod
   |**autoaddrow**        | 	bit           |                    | automatycznie dodaj linie
   |**att_classes_id**    | 	int           |CLASSES **id**      |powiązana klasa załącznika
   |**attsendtocr**       | 	bit           |                    |wyślij załącznik do ocr
   |**newdocpath**        | 	varchar(1024) |                    |ścieżka zapisu noweg dokumentu w repozytorium

### Tablica **COLUMNSFORMATS** 

   | Kolumna        | Typ danych     |    Odwołanie       | Opis |
   | -------        | ----           | -----              | ------| 
   |**id**          | 	int          |                    |numer unikalny
   |**objtype**     | 	int          |                    |typ obiektu **1** - raport, **2** - dziennik korespondencji
   |**objid**       | 	int          |INTERACTIVEDICTS **id**, DAILYCORRCLASS **id** |odwołanie do powiązanego obiektu
   |**column**      | 	varchar(100) |                    |nazwa kolumny
   |**label**       | 	varchar(254) |                    |etykieta kolumny
   |**sortable**    | 	bit          |                    | czy sortowanie
   |**target**      | 	int          |                    |typ odnośnika: **0** - brak, **1** - podraport, **2** - dokument, **3** wpis dziennika korespondencji
   |**classes_id**  | 	int          |INTERACTIVEDICTS **id**| klasa odnośnika dla podraportu (inny raport)
   |**marktodel**   | 	bit          |                    |
   |**decscale**    | 	int          |                    |skala: **-1** - auto, **>0** tyle zer po przecinku (precyzja)
   |**width**       | 	int          |                    |szerokość
   |**group**       | 	int          |                    |grupowanie: **0** - brak, **>0** kolejność grupowania
   |**groupasc**    | 	bit          |                    |czy sortować grupowanie rosnąco
   |**alignright**  | 	bit          |                    |wyrównaj do prawej
   |**sumable**     | 	bit          |                    |czy sumator

### Tablica **COLUMNSMAPPING** 

   | Kolumna              | Typ danych     |    Odwołanie         | Opis |
   | -------              | ----           | -----                | ------| 
   |**columnsformats_id** | 	int          |COLUMNSFORMATS **id** |odwołanie do ustawienia formatu kolumny
   |**from**              | 	varchar(100) |                      |parametr z
   |**to**                | 	varchar(100) |                      |parametr do

### Tablica **COMMENTENTRIES** 

   | Kolumna            | Typ danych |    Odwołanie       | Opis |
   | -------            | ----       | -----              | ------| 
   |**id**              | 	int      |                    |numer unikalny
   |**pagecomments_id** | 	int      |PAGECOMMENTS **id** |odwołanie do powiązanej strony
   |**users_id**        | 	int      |USERS **id**        | kod powiązanego użytkownika
   |**entrynum**        | 	int      |                    | numer kolejny wpisu (komentarz do komentarza)
   |**content**         | 	ntext    |                    | zawartość komentarza
   |**createdat**       | 	datetime |                    |data utworzenia
   |**marktodel**       | 	bit      |                    |

### Tablica **COMPANIES** 

   | Kolumna            | Typ danych       |    Odwołanie       | Opis |
   | -------            | ----             | -----              | ------|  
   |**id**              | 	int            |                    |numer unikalny
   |**dbname**          | 	varchar(128)   |                    |nazwa bazy danych SAP (sql)
   |**company**         | 	nvarchar(1000) |                    |nazwa firmy
   |**CreatedAt**       | 	datetime       |                    |data utworzenia
   |**UpdatedAt**       | 	datetime       |                    |data ostatniej aktualizacji
   |**directories_id**  | 	int            |                    |katalog domyślny
   |**organizations_id**| 	int            |ORGANIZATIONS **id**| powiązana organizacją
   |**bpdbtype**        | 	int            |                    |rodzaj bazy PH: **0** - baza wewnętrzna SPUMA, **1** - zewnętrzny SOAP
   |**globalid**        | 	varchar(36)    |                    |unikalny kod firmy
   |**taxid**           | 	varchar(32)    |                    |NIP firmy dla KSEF

### Tablica **COMPANIESDICTS** 

   | Kolumna            | Typ danych        |    Odwołanie       | Opis |
   | -------            | ----              | -----              | ------|  
   |**id**              | 	int             |                    |numer unikalny
   |**companies_id**    | 	int             |COMPANIES **id**    | powiązana firma ze słownikiem
   |**name**            | 	nvarchar(100)   |                    |nazwa słownika
   |**description**     | 	ntext           |                    |opis słownika   
   |**regex**           | 	nvarchar(1024)  |                    |wzór do podpowiedzi w formacie regex
   |**marktodel**       | 	bit             |
   |**displtips**       | 	bit             |                    |pokaż podpowiedzi w polach tekstowych
   |**globalid**        | 	varchar(36)     |                    |unikalny kod firmy


### Tablica **CONFIGURATION** 

   | Kolumna            | Typ danych      |                    | Opis |
   | -------            | ----            | -----              | ------|  
   |**profile**         | 	varchar(100)  |                    |nazwa profilu
   |**active**          | 	bit           |                    |czy aktywny
   |**DefSMTPAddress**  | 	varchar(100)  |                    |Serwer SMTP - adres
   |**DefSMTPPort**     | 	int           |                    |Serwer SMTP - port
   |**DefSMTPUser**     | 	varchar(100)  |                    |Serwer SMTP - użytkownik
   |**DefSMTPPassword** | 	nvarchar(100) |                    |Serwer SMTP - hasło
   |**OCRInputPath**    | 	varchar(1024) |                    |OCR - ścieżka wejściowa
   |**OCROutputPath**   | 	varchar(1024) |                    |OCR - ścieżka wyjściowa
   |**SessionsFile**    | 	varchar(1024) |                    |ścieżka do pliku sessji
   |**SecurityKey**     | 	varchar(1024) |                    |klucz bezpieczeństwa
   |**SecurityIV**      | 	varchar(1024) |                    |klucz bezpieczeństwa IV
   |**CentralService**  | 	varchar(1024) |                    |OCR - adres serwera usługi OCR
   |**ClientID**        | 	nvarchar(100) |                    |OCR - nazwa klienta (CLient ID)
   |**ServicePort**     | 	int           |                    |OCR - port usługi
   |**OcrTaskMode**     | 	int           |                    |OCR - tryb - **0** - dysk, **1** - zewnętrzny web service
   |**initscale**       | 	int           |                    |skala inicjalna: **<=0** - dopasuj dokument do szerokości strony, **>0** - procent powiększenia dokumentu
   |**rescachelen**     | 	int           |                    |dłgugość cache - ilość dokumentów przechowywanych w historii
   |**defsighours**     | 	int           |                    |ważnośc sygnatury w godzinach
   |**jsfunct**         | 	ntext         |                    |funkcje JS
   |**checkrefdelay**   | 	int           |                    |Automatyzacja interwał odczytu danych ze skrzynki pocztowej (POP3)
   |**remoteaddress**   | 	nvarchar(max) |                    |Adres zdalny do SPUMY
   |**ksef_apiurl**     | 	nvarchar(128) |                    |KSEF adres do API
   |**ksef_pubkeyb64**  | 	nvarchar(max) |                    |KSEF klucz publiczny

### Tablica **COUNTRIES** 

   | Kolumna     | Typ danych     |    Opis|
   | -------     | ----           | -----              |  
   |**Code**     | 	varchar(32)   | kod kraju          |
   |**Name**     | 	nvarchar(128) | nazwa kraju        |


### Tablica **CUSTOMPROCESS_DIALOGWND** 

   | Kolumna              | Typ danych      |   Odwołanie           | Opis |
   | -------              | ----            | -----                 | -----|
   |**customprocesses_id**| 	int           | CUSTOMPROCESSES **id**|odwołanie do procesu UI |
   |**intid**             | 	int           |                       |numer kolejny instrukcji
   |**name**              | 	nvarchar(100) |                       |nazwa instrukcji komunikatu
   |**description**       | 	ntext         |                       |opis komunikatu
   |**message**           | 	nvarchar(max) |                       |komunikat
   |**btn1**              | 	nvarchar(100) |                       |tekst przycisku 1
   |**btn2**              | 	nvarchar(100) |                       |tekst przycisku 2
   |**btn3**              | 	nvarchar(100) |                       |tekst przycisku 3
   |**variable_id**       | 	int           |                       |powiązanie ze zmienną wyjścia


### Tablica **CUSTOMPROCESS_EXCALLOP** 

   | Kolumna                | Typ danych      |   Odwołanie           | Opis |
   | -------                | ----            | -----                 | -----|
   |**customprocesses_id**  | 	int           | CUSTOMPROCESSES **id**|odwołanie do procesu UI |
   |**intid**               | 	int           |                       |numer kolejny instrukcji
   |**name**                | 	nvarchar(100) |                       |nazwa instrukcji
   |**description**         | 	ntext         |                       |opis instrukcji
   |**asmtype**             | 	int           |                       |typ **0** - .NET DLL
   |**assembly**            | 	varchar(100)  |                       |nazwa pliku DLL
   |**clstype**             | 	varchar(100)  |                       |nazwa klasy
   |**method**              | 	varchar(100)  |                       |metoda
   |**arg0**                | 	nvarchar(max) |                       |argument 1
   |**arg1**                | 	nvarchar(max) |                       |argument 2
   |**arg2**                | 	nvarchar(max) |                       |argument 3
   |**arg3**                | 	nvarchar(max) |                       |argument 4
   |**variable_id**         | 	int           |                       |powiązanie ze zmienną wyjścia

### Tablica **CUSTOMPROCESS_LINEOP** 

   | Kolumna                | Typ danych|   Odwołanie           | Opis |
   | -------                | ----  | -----                | -----|
   |**customprocesses_id**  | 	int |CUSTOMPROCESSES **id**|odwołanie do procesu UI |
   |**intid**               | 	int |                      |numer kolejny instrukcji
   |**name**                |  	nvarchar(100) |            |nazwa instrukcji
   |**description**         | 	ntext |                    |opis instrukcji
   |**type**                | 	int |                      |typ instrukcji: **0** - pobranie linii , **1** - aktualizacja linii , **2** - czyszczenie linii, **3** - dodanie linii, **4** - kasowanie linii, **5** - pobranie nagłówka, **6** - aktualizacja nagłówka, **7** - zapisz dokument
   |**variable_id**         | 	int |                      |powiązanie ze zmienną wejścia/wyjścia

### Tablica **CUSTOMPROCESS_SCRIPTOP** 

   | Kolumna                | Typ danych      |   Odwołanie          | Opis |
   | -------                | ----            | -----                | -----|
   |**customprocesses_id**  | 	int           |CUSTOMPROCESSES **id**|odwołanie do procesu UI |
   |**intid**               | 	int           |                      |numer kolejny instrukcji
   |**name**                | 	nvarchar(100) |                      |nazwa instrukcji
   |**description**         | 	ntext         |                      |opis instrukcji
   |**type**                | 	int           |                      |typ instrukcji: **0** - MsSQL
   |**content**             | 	ntext         |                      |treść zapytania
   |**variable_id**         | 	int           |                      |powiązanie ze zmienną wyjścia


### Tablica **CUSTOMPROCESSES** 

   | Kolumna            | Typ danych      |   Odwołanie           | Opis |
   | -------            | ----            | -----                 | -----| 
   |**id**              | 	int           |                       | unikalny kod procesu UI
   |**name**            | 	nvarchar(100) |                       | nazwa procesu UI
   |**description**     | 	ntext         |                       | opis procesu UI
   |**classes_id**      | 	int           |CLASSES **id**         |odwołanie do klasy dokumentu
   |**organizations_id**| 	int           |ORGANIZATIONS **id**   | powiązanie z organizacją
   |**CreatedAt**       | 	datetime      |                       |data utworzenia
   |**UpdatedAt**       | 	datetime      |                       |data ostatniej aktualizacji
   |**globalid**        | 	varchar(36)   |                       |unikalny kod procesu UI


### Tablica **DAILYCORR_PROPERTIES** 

   | Kolumna            | Typ danych      |   Odwołanie               | Opis |
   | -------            | ----            | -----                     | -----|
   |**dailycorr_id**    | 	int           |DAILYCORRESPONDENCE **id** |powiązanie z wpisem dziennika korespondencji
   |**attribs_id**      | 	int           | CLASSATTRIBS **id**       | powiązanie z atrybutem klasy
   |**value**           | 	nvarchar(max) |                           |przypisana wartość


### Tablica **DAILYCORR_REF** 

   | Kolumna            | Typ danych |   Odwołanie               | Opis |
   | -------            | ----       | -----                     | -----|
   |**dailycorr_id**    | 	int      |DAILYCORRESPONDENCE **id** |powiązanie z wpisem dziennika korespondencji
   |**documents_id**    | 	int      |DOCUMENTS **id**           | powiązanie z dokumentem
   |**users_id**        | 	int      |USERS **id**               |powiązanie z użytkownikiem
   |**linkdate**        | 	datetime |                           |data i godzina utworzenia powiązania


### Tablica **DAILYCORR_REF** 

   | Kolumna              | Typ danych      |   Odwołanie           | Opis |
   | -------              | ----            | -----                 | -----|
   |**id**                | 	int           |                       | unikalny kod klasy dziennika korespondencji
   |**organizations_id**  | 	int           |ORGANIZATIONS **id**   | powiązanie z organizacją
   |**name**              | 	nvarchar(100) |                       |nazwa
   |**enabled**           | 	bit           |                       |czy aktywny
   |**description**       | 	ntext         |                       |opis
   |**reportctx**         | 	ntext         |                       |raport SQL
   |**CreatedAt**         | 	datetime      |                       |data utworzenia
   |**UpdatedAt**         | 	datetime      |                       |data ostatniej aktualizacji
   |**globalid**          | 	varchar(36)   |                       |unikalny kod klasy
   |**numpfx**            | 	varchar(2)    |                       |prefix 


### Tablica **DAILYCORR_REF** 

   | Kolumna              | Typ danych    |   Odwołanie           | Opis |
   | -------              | ----          | -----                 | -----|
   |**id**                | 	int         |                       | unikalny numer wpisu
   |**dailycorrclass_id** | 	int         |DAILYCORRCLASS **id**  |powiązanie z klasą dziennika korespondencji 
   |**users_id**          | 	int         |USERS **id**           |powiązanie z użytkownikiem
   |**companies_id**      | 	int         |COMPANIES **id**       |powiązanie z firmą
   |**optype**            | 	int         |                       |typ operacji **0** - wejście, **1** - wyjście, **2** - inna
   |**opdate**            | 	datetime    |                       |data operacji
   |**description**       | 	ntext       |                       |opis
   |**CreatedAt**         | 	datetime    |                       |data utworzenia wpisu dziennika
   |**UpdatedAt**         | 	datetime    |                       |data ostatniej aktualizacji wpisu dziennika
   |**docnum**            | 	varchar(32) |                       |numer wpisu

### Tablica **DEFINITIONS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**code**              | nvarchar(100) |                        | unikalny kod wpisu dla wzorca OCR
   |**description** 	  | 	ntext     |                        |opis wzorca
   |**filename**          | nvarchar(100) |                        |nazwa pliku
   |**language**          | nvarchar(100) |                        |język wzorca
   |**CreatedAt**         | 	datetime  |                        |data utworzenia wpisu
   |**UpdatedAt**         | 	datetime  |                        |data aktualizacji wpisu
   
### Tablica **DESIGNERCONNECTIONS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**dst_objid**         |      int      |                        | 
   |**designeritmintid**  |      int      |                        | 
   |**designeritmintid2** |      int      |                        | 
   |**designerlpoint**    |      int      |                        | 
   |**designerlpoint2**   |      int      |                        | 
   |**dst_objtype**       |      int      |                        | 
   
### Tablica **DESIGNERITEMS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**dst_objid**         |      int      |                        | 
   |**insintid**          |      int      |                        | 
   |**intid**             |      int      |                        | 
   |**left**              |      float    |                        | 
   |**top**               |      float    |                        | 
   |**width**             |      float    |                        |
   |**height**            |      float    |                        |
   |**dst_objtype**       |      int      |                        | 

### Tablica **DICTIONARIES** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**id**                | int |                                  | unikalny kod wpisu dla słownika
   |**name**              | nvarchar(100) |                        |nazwa słownika
   |**description** 	  | 	ntext     |                        |opis słownika
   |**CreatedAt**         | 	datetime  |                        |data utworzenia wpisu
   |**UpdatedAt**         | 	datetime  |                        |data aktualizacji wpisu
   |**organizations_id**  | int           |ORGANIZATIONS **id**    | powiązanie z organizacją
   |**globalid**          | varchar(36) |                          |nadany unikalny kod wpisu dla słownika

### Tablica **DIRECTORIES** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**id**                | int           |                        | unikalny kod wpisu dla katalogu
   |**companies_id**      | int           | COMPANIES **id**       |powiązanie z firmą
   |**directories_id** 	  | 	int       |  DIRECTORIES **id**    |powiązanie z katalogiem nadrzędnym
   |**name**         	  | nvarchar(100) |                        |nazwa katalogu
   |**description**       | 	ntext  	  |                        |opis katalogu
   |**icontype**  	  | int           |                        |typ ikony katalogu
   |**iconcolor**         | int 	  |                        |kolor ikony katalogu
   |**CreatedAt**         | 	datetime  |                        |data utworzenia wpisu
   |**UpdatedAt**         | 	datetime  |                        |data aktualizacji wpisu

### Tablica **DOCUMENTOCRRESULTS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**id**                | int           |                        |unikalny kod wpisu dla wyniku rozpoznawania OCR dla dokumentu
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem
   |**schemacode** 	  | nvarchar(100) |  DIRECTORIES **id**    |kod wybranego schematu rozpoznawania OCR
   |**title**         	  | nvarchar(255) |                        |Tytuł przypisany z OCR
   |**comments**          | 	ntext  	  |                        |
   |**marktodel**  	  | bit           |                        |

### Tablica **DOCUMENTPAGES** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**id**                | int           |                        |unikalny kod wpisu dla strony dokumentu
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem
   |**pagenum** 	  | int           |                        |numer strony dokumentu
   |**resources_id**      | int           | RESOURCES **id**       |powiązanie z zasobem pliku
   |**resources_pagenum** | int           |                        |numer strony w przypisanym zasobie
   |**marktodel**  	  | bit           |                        |
   |**rotation**  	  | int           |                        |obrót strony (np:  **0** , **90**, **180**, **270**)

### Tablica **DOCUMENTREF** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**id**                | int           |                        |unikalny kod wpisu dla powiązania
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem
   |**companies_id** 	  | int           | COMPANIES **id**       |powiązanie z firmą
   |**objecttype**        | nvarchar(50)  |                        |powiązanie z obiektem w systemie ERP
   |**objectid** 	  | nvarchar(50)  |                        |powiązanie z numerem wewnętrznym dokumentu w systemie ERP
   |**marktodel**  	  | bit           |                        |

### Tablica **DOCUMENTREFLINES** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documentrefs_id**   | int           | DOCUMENTREF **id**     |powiązanie z referncją dokumentu
   |**linenum** 	  | int           |                        |numer linii
   |**columnid**          | int           |                        |numer kolumny
   |**value** 	          | nvarchar(max) |                        |wartość

### Tablica **DOCUMENTS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**id**                | int           |                        |unikalny numer dokumentu
   |**users_id** 	  | int           | USERS **id**    	   |właściciel - powiązanie z użytkownikiem SPUMA
   |**classes_id**        | int           | CLASSESS **id**    	   |klasa - powiązanie z klasą dokumentu
   |**companies_id** 	  | int           | COMPANIES **id**       |powiązanie z firmą
   |**name** 	          | nvarchar(100) |                        |nazwa dokumentu
   |**description** 	  | ntext         |                        |opis dokumentu
   |**docdate**           | 	datetime  |                        |data dokumentu
   |**docnum**            | nvarchar(100) |                        |numer dokumentu
   |**IDDoc**             |   int         |                        |
   |**CreatedAt**         | 	datetime  |                        |data utworzenia wpisu
   |**UpdatedAt**         | 	datetime  |                        |data aktualizacji wpisu
   |**authstatus**        |   int         |                        |status autoryzacji wartości: **0** - oczekuje, **1** - zatwierdzony, **2** - odrzucony
   |**directories_id** 	  | int           | DIRECTORIES **id**     |powiązanie z katalogiem
   |**docstatus** 	  | int           |                        |status dokumentu wartości: **0** - katalog wczytane, **1** - katalog rozpoznawane, **2** - katalog do sprawdzenia, **3** - katalog repozytorium
   |**reconschemas_code** | nvarchar(100) |                        | 
   |**enterdate**         | 	datetime  |                        |data wpływu
   |**templates_id**      | 	int       | DOCUMENTS **id**       |powiązanie z dokumentem typu szablon
   |**definition_code**   | varchar(100)  |                        |
   |**ocr_code**          | varchar(100)  |                        |unikalny kod wygenerowany przez usługe OCR dla dokumentu
   |**headereditmode**    |   int         |                        |uprawnienie do edycji nagłówka dokumentu wartości: **0** - blokada, **1** - odblokowane
   |**lineseditmode**     |   int         |                        |uprawnienie do edycji linii dokumentu wartości: **0** - blokada, **1** - odblokowane
   |**headereditmode1**   |   int         |                        |uprawnienie do edycji nagłówka1 dokumentu wartości: **0** - blokada, **1** - odblokowane
   |**lineseditmode1**    |   int         |                        |uprawnienie do edycji linii1 dokumentu wartości: **0** - blokada, **1** - odblokowane
   |**headereditmode2**   |   int         |                        |uprawnienie do edycji nagłówka2 dokumentu wartości: **0** - blokada, **1** - odblokowane
   |**lineseditmode2**    |   int         |                        |uprawnienie do edycji linii2 dokumentu wartości: **0** - blokada, **1** - odblokowane
   |**canchgres**         |   bit         |                        |uprawnienie do zmiany zasobu dokumentu (zmiana wersji pliku)wartości: **0** - blokada, **1** - odblokowane
   |**sysdocnum** 	  | int           |                        |numer systemowy dokumentu nadany po wysłaniu dokumentu w obieg unikalny w obrębie firmy i klasy
   |**rm_users_id**       |   int         |                        |
   |**tmpwritemode**      |   int         |                        |uprawnienie do edycji dokumenty typu formularz wartości: **0** - blokada, **1** - odblokowane
   |**autopublish**       |   bit         |                        |
   |**grouping**          | varchar(max)  |                        |

### Tablica **DOCUMENTS_ATTACHMENTS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem jako dokument główny
   |**att_documents_id**  | int           | DOCUMENTS **id**       |powiązanie z dokumentem jako załącznik
   
### Tablica **DOCUMENTS_AUTHLOCKS** 

   | Kolumna                    | Typ danych    |   Odwołanie            	| Opis |
   | -------                    | ----          | -----                  	| -----|
   |**documents_authschemas_id**| int           | DOCUMENTS_AUTHSCHEMA **id**   |powiązanie ze dokumentem autoryzacji dla dokumentu
   |**users_id**       		| int           | USERS **id**       		|użytkownik
   |**lockat**         		| 	datetime  |                        |data zablokowania
   |**unlockat**         	| 	datetime  |                        |data odblokowania

### Tablica **DOCUMENTS_AUTHRECIPIENTS** 

   | Kolumna         		| Typ danych  	| Odwołanie| Opis |
   | -------          		| ----        	| ----- | ------| 
   |**documents_authschemas_id**| 	int 	|DOCUMENTS_AUTHSCHEMA **id**  | powiazanie ze schematem autoryzacji powiązanym z dokumentem
   |**objid**        		| 	int 	|USERS **id**, USERGROUPS **id**, AUTHSCHEMAS **id** | odwołanie do powiązanego obiektu
   |**objtype**       		| 	int 	|                    		| Typ obiektu **0** - użytkownik, **1** - grupa użytkowników, **2** - schemat autoryzacji  
   |**order**         		| 	int 	|                    | kolejność
   |**authstatus**         	| 	int 	|                    | status akceptacji danego etapu wartości: **0** - oczekuje, **1** - zatwierdzony, **2** - odrzucony
   |**comment**       		| nvarchar(1024)|          	     | dodatkowe informacje
   |**visibility**            	| 	bit 	|                    | widoczność wartości: **0** - ukryj, **1** - pokaż
   |**addinfo**     		|  nvarchar(max)|                    | dodatkowe informacje dla użytkownika do etapu zatwierdzania
   |**auth_users_id**       	| 	int 	|USERS **id**	     | użytkownik który zautoryzował dany etap
   |**srcinsintid**         	| 	int 	|                    | źródłowa instanacja schematu autoryzacji

### Tablica **DOCUMENTS_AUTHSCHEMA** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**id**                | int           |                        |unikalny numer wpisu
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem jako dokument główny
   |**name**  		  | nvarchar(100) |                        |nazwa etapu schematu zatwierdzania
   |**authmethodtype**    | 	int       |                        | rodzacj schematu: **0** - wszyscy z, **1** - jeden z, **2** - (n) z, **3** - proces autoryzacji
   |**authusrlimit**      | 	int       |                        | limit odbiorcow dla etapu
   |**authschema_id**     | 	int       | AUTHSCHEMAS **id**     | kod powiązanego schematu autoryzacji
   |**authstatus**        | 	int 	  |                    	   | status akceptacji danego etapu wartości: **0** - oczekuje, **1** - zatwierdzony, **2** - odrzucony
   |**subschema**         | 	bit       |                        | czy to podschemat wartości: **0** - nie, **1** - tak
   |**addinfo**           |  nvarchar(max)|                        | dodatkowe informacje dla użytkownika do etapu zatwierdzania
   |**insintid**          | 	int       |                        | numer instrukcji w procesie autoryzacji

### Tablica **DOCUMENTS_AUTHVAR_BASIC** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_authschemas_id**| 	int 	|DOCUMENTS_AUTHSCHEMA **id**  | powiazanie ze schematem autoryzacji powiązanym z dokumentem
   |**variable_id**        	| 	int 	|                    	      | numer zmiennej
   |**linenum**       		| 	int 	|                    	      | numer linii
   |**value**         		|nvarchar(1024)|                   	      | wartość

### Tablica **DOCUMENTS_AUTHVAR_SCHEMA** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_authschemas_id**| 	int 	|DOCUMENTS_AUTHSCHEMA **id**  | powiazanie ze schematem autoryzacji powiązanym z dokumentem
   |**variable_id**        	| 	int 	|                    	      | numer zmiennej
   |**authmethodtype**    | 	int       |                        | rodzacj schematu: **0** - wszyscy z, **1** - jeden z, **2** - (n) z, **3** - proces autoryzacji
   |**authusrlimit**      | 	int       |                        | limit odbiorcow dla etapu

### Tablica **DOCUMENTS_AUTHVAR_SCHEMARCP** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_authschemas_id**| 	int 	|DOCUMENTS_AUTHSCHEMA **id**  | powiazanie ze schematem autoryzacji powiązanym z dokumentem
   |**variable_id**        	| 	int 	|                    	      | numer zmiennej
   |**order**         		| 	int 	|                    		| kolejność
   |**objid**        		| 	int 	|USERS **id**, USERGROUPS **id**, AUTHSCHEMAS **id** | odwołanie do powiązanego obiektu
   |**objtype**       		| 	int 	|                    		| Typ obiektu **0** - użytkownik, **1** - grupa użytkowników, **2** - schemat autoryzacji  

### Tablica **DOCUMENTS_LINES** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem jako dokument główny
   |**attribs_id**        | 	int       | CLASSATTRIBS **id**    | kod powiązanego atrybutu klasy
   |**linenum**           | 	int 	  |                    	   | numer linii dokumentu
   |**value**             |  nvarchar(max)|                        | przypisana wartośc dla atrybutu danej linii dokumentu

### Tablica **DOCUMENTS_LINESOWNERS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem 
   |**linenum**           | 	int 	  |                    	   |numer linii dokumentu
   |**users_id**       	  | int           | USERS **id**       	   |użytkownik - właściciel linii
   |**createdat**         | 	datetime  |                        |data utworzenia danej linii dokumentu
   
### Tablica **DOCUMENTS_LINESREFS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem 
   |**linenum**           | 	int 	  |                    	   |numer linii dokumentu
   |**documentocrresults_id**| int        | DOCUMENTOCRRESULTS **id** |powiązanie z wynikami OCR dla danego dokumentu
   |**ocrlinenum**        | int           |                        |numer linii odczytany przez OCR
   |**attribs_id1**       | int           | CLASSATTRIBS **id**    |numer powiązanego atrybutu przypisanego w mapowaniu danych z OCR
   |**ocrname1**          | nvarchar(128) |                        |nazwa kolumny w szablonie OCR
   |**attribs_id2**       | int           | CLASSATTRIBS **id**    |numer powiązanego atrybutu przypisanego w mapowaniu danych z OCR
   |**ocrname2**          | nvarchar(128) |                        |nazwa kolumny w szablonie OCR
   |**attribs_id3**       | int           | CLASSATTRIBS **id**    |numer powiązanego atrybutu przypisanego w mapowaniu danych z OCR
   |**ocrname3**          | nvarchar(128) |                        |nazwa kolumny w szablonie OCR
   |**attribs_id4**       | int           | CLASSATTRIBS **id**    |numer powiązanego atrybutu przypisanego w mapowaniu danych z OCR
   |**ocrname4**          | nvarchar(128) |                        |nazwa kolumny w szablonie OCR

### Tablica **DOCUMENTS_MODIFICATION** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem 
   |**users_id**       	  | int           | USERS **id**       	   |użytkownik wprowadzający aktualizację na dokumencie
   |**CreatedAt**         | 	datetime  |                        |data utworzenia wpisu

### Tablica **DOCUMENTS_OCRMAP** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem 
   |**class_id** 	  | 	int       |CLASSESS **id**    	   |powiązanie z klasą dokumentu
   |**cardcode**	  | nvarchar(128) |                        |kod dostawcy z systemu ERP
   |**schemacode**	  | nvarchar(100) |                        |kod schematu rozpoznawania (wzorca OCR)
   |**ocrname**	  	  | nvarchar(100) |                        | nazwa pola OCR zgodna z wzorcem OCR
   |**attribs_id**        | int           | CLASSATTRIBS **id**    |numer powiązanego atrybutu przypisanego w mapowaniu danych z OCR
   |**maptype** 	  | 	int       |                        |typ mapowania wynikó z OCR wartości: **1** - kopiuj, **2** - wyszukaj, **3** - zapamiętaj 

### Tablica **DOCUMENTS_PROPERTIES** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem jako dokument główny
   |**attribs_id**        | int           | CLASSATTRIBS **id**    |numer powiązanego atrybutu przypisanego w mapowaniu danych z OCR
   |**value**             |  nvarchar(max)|                        | przypisana wartośc dla atrybutu danej linii dokumentu

### Tablica **DOCUMENTUSAGE** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem jako dokument główny
   |**users_id**       	  | int           | USERS **id**       	   |użytkownik wprowadzający aktualizację na dokumencie
   |**openat**            | 	datetime  |                        |data otwarcia dokumentu
   
### Tablica **EXTERNALREFS** 

   | Kolumna              | Typ danych    |   Odwołanie            | Opis |
   | -------              | ----          | -----                  | -----|
   |**documents_id**      | int           | DOCUMENTS **id**       |powiązanie z dokumentem jako dokument główny
   |**sourceid**       	  | varchar(255)  |                        |powiązanie z np.: id skrzynki POP3, IMAP, numer KSEF 
   |**foldername**        |nvarchar(32)   |                        |nazwa katalogu

### Tablica **INTERACTIVEDICTS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**                | 	int           |                    |numer unikalny
   |**name**              | 	nvarchar(100) |                    | nazwa słownika
   |**description**       | 	ntext         |                    | opis słownika
   |**scriptype**         | 	int           |                    | rodzaj skryptu wartości: **0** - MSSQL
   |**scriptctx** 	  | 	ntext         |                    | skrypt zapisany w formie tekstowej
   |**sqlconnstr**        | 	nvarchar(100) |                    | dodatkowy ciąg połączenia
   |**allowcache**        | 	bit	      |                    | 
   |**CreatedAt**        | 	datetime      |                    | data utworzenia
   |**UpdatedAt**        | 	datetime      |                    | data aktualizacji
   |**organizations_id** | 	int           |ORGANIZATIONS **id**| powiązanie z organizacją
   |**report**           | 	bit	      |                    | czy to raport  **0** - nie,  **1** - tak
   |**label**            | 	nvarchar(200) |                    | etykieta
   |**visible**          | 	bit	      |                    | widoczny  **0** - nie,  **1** - tak
   |**globalid**         | 	nvarchar(200) |                    | nadany numer unikalny

### Tablica **KSEF_DOCUMENTS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**Sess_Int_ID**       | 	int           |KSEF_SESSIONS **IntID**|powiązanie z instancją sesji połączenia z API KSEF ustanowioną dla danego tokena
   |**InvoiceReferenceNumber**| varchar(128)  |                    | numer dokumentu
   |**KsefReferenceNumber**   | varchar(128)  |                    | numer referencyjny dokumentu w KSEF
   |**InvoiceHash**       | varchar(128)      |                    | hash dokumentu
   |**InvoicingDate**      | varchar(32)      |                    | data dokumentu
   |**AcquisitionTimestamp**| varchar(32)     |                    | data dodania dokumentu do KSEF
   |**SubjectBy_NIP**  	  | varchar(32)       |                    | NIP dostawcy (wystawcy dokumentu)
   |**SubjectBy_Name** 	  | varchar(128)      |                    | nazwa Dostawcy
   |**SubjectTo_NIP** 	  | varchar(32)       |                    | NIP odbiorcy dokumentu
   |**SubjectTo_Name** 	  |  varchar(128)     |                    | nazwa odbiorcy
   |**Net** 	  	  | numeric(19,2)     |                    | kwota netto całego dokumentu
   |**Vat** 	  	  | numeric(19,2)     |                    | kwota VAT całego dokumentu
   |**Gross** 	  	  | numeric(19,2)     |                    | kwota brutto całego dokumentu
   |**Currency** 	  |  varchar(32)      |                    | waluta
   |**XmlDta** 	  	  |  xml   	      |                    | pobrany pełny XML ze strukturą dokumentu z KSEF

### Tablica **KSEF_SESSIONS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**IntID**       	  | 	int         |                    |numer przyznanej instancji sesji dla Tonekna
   |**NIP**		  | varchar(32)     |                    | NIP Firmy
   |**Pesel**		  | varchar(32)     |                    | pesel 
   |**Token**  		  | varchar(128)    |                    | token
   |**SessionToken**   	  | varchar(128)    |                    | token dla ustanowionej sesji
   |**LastCheck**         | 	datetime    |                    |data i godzina ostatniego pobrania danych z KSEF
   
### Tablica **MAILMONITORCFG** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**profile**		  | varchar(100)    |CONFIGURATION  **profile** | nazwa profilu konfiguracji
   |**SPUMAuserid**       | int             | USERS **id**       |użytkownik przypisany do automatyzacji
   |**SPUMAcompanyid** 	  | int             | COMPANIES **id**   |powiązanie z firmą
   |**SPUMAInputPath**	  | varchar(1024)   |                    | monitorowana ścieżka wejścia
   |**MonitoredPath**	  | varchar(1024)   |                    | monitorowana ścieżka 
   |**ArchivePath**	  | varchar(1024)   |                    | Ścieżka dla plików archiwum
   |**MailHost**	  | varchar(100)    |                    | POP3 Host
   |**MailUser**	  | varchar(100)    |                    | POP3 użytkownik
   |**MailPass**	  | varchar(100)    |                    | POP3 hasło
   |**MailPort**	  | int             |                    | POP3 port
   |**UseSSL**	  	  | bit             |                    | POP3 czy SSL wartości: **0** - nie, **1** - tak
   |**MatchRx**	  	  | varchar(1024)   |                    | wyrażenie regularne użyte do filtrowania treści email
   |**docctype**	  | int             |                    | rodzaj dokumentu wartości: **1** - załączniki jako strony, **2** - załączniki jako dokumenty
   |**classes_id**        | int             | CLASSESS **id**    |klasa załącznika dla docelowego dokumentu powstałego przy tej automatyzacji
   |**allowempty**	  | bit             |                    | dodaj wiadomości bez załączników wartości: **0** - nie, **1** - tak
   
### Tablica **MESSAGE_RECIPIENTS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**messages_id**       | 	int         | MESSAGES **id**    |numer powiązanej wiadomości
   |**users_id**          | int             | USERS **id**       |użytkownik przypisany do wiadomości
   |**email_adr**         | 	nvarchar(100) |                  | adres Email odbiorcy wiadomości
   |**isread**	          | bit             |                    | Czy wiadomość została odczytana wartości: **0** - nie, **1** - tak
   
### Tablica **MESSAGES** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**                | 	int         |                    |numer unikalny wiadomości
   |**users_id**          | int             | USERS **id**       |użytkownik tworzący wiadomośc
   |**dst_companies_id**  | int             | COMPANIES **id**   |powiązanie z firmą
   |**dst_documents_id**  | int             | DOCUMENTS **id**   |powiązanie z dokumentem
   |**subject**           | nvarchar(1024)  |                    | temat wiadomości
   |**content**           | ntext  	    |                    | zawartość wiadomości
   |**isread**	          | bit             |                    | Czy wiadomość została odczytana wartości: **0** - nie, **1** - tak
   |**CreatedAt**         | 	datetime    |                    | data utworzenia wiadomości
   |**UpdatedAt**         | 	datetime    |                    | data aktualizacji wiadomości
   |**issent**	          | bit             |                    | Status wysłanej wiadomości wartości: **0** - oczekuje w kolejce, **1** - wysłano poprawnie , **2** - błąd wysyłki
   |**att_document_id**   | int             | DOCUMENTS **id**   |powiązanie z dokumentem załącznika
   |**eventtype**         | 	int         |                    |rodzaj powiadomienia wartości: **0** - wiadomość wewnętrzna, **1** - Prośba o autoryzację , **2** - Autoryzacja dokumentu, **3** - Odrzucenie dokumentu, **4** - Prośba o komentarz, **5** - Skomentowano, **6** - Zmiana na dokumencie obserwowanym, **7** - Zatwierdzenie finalne dokumentu
   |**dst_documents_authschemas_id**| 	int 	|DOCUMENTS_AUTHSCHEMA **id**  | powiazanie ze schematem autoryzacji powiązanym z docelowym dokumentem

### Tablica **MODIFICATIONENTRY** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**documentmodifications_id**| int    | DOCUMENTS_MODIFICATION **id**   |powiązanie z modyfikacją zapisaną dla dokumentu
   |**objtype**       	  | 	int 	 |                     | Typ obiektu **0** - nagłówek dokumentu, **1** - strony dokumentu, **2** - zmienne systemowe , **5** - linie dokumentu
   |**objid**        	  | 	int 	 |DOCUMENTS **id**     | odwołanie do powiązanego dokumentu
   |**fieldcode**         | nvarchar(32) |                     | nazwa pola
   |**oldvalue**          |nvarchar(1024)|                     | wartość w polu była
   |**newvalue**          |nvarchar(1024)|                     | zmieniono na wartość w polu
   
### Tablica **MODULECONFIG** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**module**		  |nvarchar(100) |                     |nazwa modułu 
   |**property**  	  |nvarchar(100) |                     |parametr dla modułu
   |**type**  	 	  | 	int 	 |                     |typ danych parametru dla modułu wartości: **0** - liczba całkowita, **1** - TAK/NIE, **2** - tekst, **3** - ścieżka do pliku lub katalogu, **4** - hasło
   |**value**             |nvarchar(1024)|                     | wartość dla parametru
   |**updateat**          | 	datetime |                     | data aktualizacji wpisu
   
### Tablica **OCRFIELDS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**        	     | 	int 	    |                    | numer kolejny wpisu
   |**documentocrresults_id**| 	int 	    |DOCUMENTOCRRESULTS **id**     | odwołanie do przypisanego schematu rozpoznawania dla dokumentu
   |**name**                 |nvarchar(100)|                     | nazwa pola
   |**type**                 | 	int 	    |                    | typ pola wartości: **0** - pole tekstowe, **1** - liczba całkowita, **2** - data, **3** - liczba zmienno przecinkowa, **4** - nazwa bloku z liniami dokumentu
   |**value**                |nvarchar(max) |                     | wartość odczytana przez OCR
   |**ocrfields_id**  	     | 	int 	    |DOCUMENTOCRRESULTS **id**| identyfikator pola OCR nadrzędnego dla bloku z liniami
   |**marktodel**  	     | bit          |                     |

### Tablica **OCRLINES** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**ocrfields_id**	  | 	int 	    |OCRFIELDS **id**    | powiązanie z odczytaneym polem OCR
   |**linenum**        	  | 	int 	    |                    | numer linii
   |**linenum**        	  |  nvarchar(max)  |                    | odczytana wartość przez OCR

### Tablica **OCRPROCESSLOG** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**documents_id**      | int             | DOCUMENTS **id**   |powiązanie z dokumentem jako dokument główny
   |**order**        	  | 	int 	    |                    | kolejnośc komunikatu
   |**isread**	          | bit             |                    | czy komuikat została odczytany wartości: **0** - nie, **1** - tak
   |**message**        	  |  nvarchar(255)  |                    | treśc komunikatu błędu
   |**CreatedAt**         | 	datetime    |                    | data utworzenia wpisu
   
### Tablica **OCRRESULTPAGES** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**        	  | 	int 	    |                    | numer kolejny wpisu
   |**documentocrresults_id**| 	int 	    |DOCUMENTOCRRESULTS **id**     | odwołanie do przypisanego schematu rozpoznawania dla dokumentu
   |**pagenum**        	  | 	int 	    |                    | numer strony
   |**type**              | 	int 	    |                    | typ pola wartości: **1** - strona z liniami , **2** - standardowa strona , **3** - strona załącznika do faktury
   |**marktodel**  	  | bit             |                    |
   |**width**        	  | 	int 	    |                    | szerokość strony
   |**height**        	  | 	int 	    |                    | wysokość strony
   
### Tablica **OCRTEXTREGIONS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**ocrresultpages_id**| 	int 	    |OCRRESULTPAGES **id**     | odwołanie do rozpoznanej strony dla dokumentu
   |**pagenum**        	  | 	ntext 	    |                    | odczytane słowo przez OCR
   |**posx**        	  | 	int 	    |                    | pozycja tekstu w osi x
   |**posy**        	  | 	int 	    |                    | pozycja tekstu w osi y
   |**width**        	  | 	int 	    |                    | szerokość regionu tekstowego
   |**height**        	  | 	int 	    |                    | wysokość regionu tekstowego
   
### Tablica **ORGANIZATIONS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**        	  | 	int 	    |                    | numer kolejny wpisu
   |**code**        	  | varchar(128)    |                    | kod organizacji
   |**CreatedAt**         | 	datetime    |                    | data utworzenia wpisu
   |**UpdatedAt**         | 	datetime    |                    | data aktualizacji wpisu
   |**globalid**          | 	varchar(36) |                    | unikalny identyfikator
   
### Tablica **PAGECOMMENTS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**        	  | 	int 	    |                    | numer kolejny wpisu
   |**documentpages_id**| 	int 	    |DOCUMENTPAGES **id**| odwołanie do strony dla dokumentu
   |**commnum**        	  | 	int 	    |                    | numer kolejny komentarza
   |**users_id**          | int             | USERS **id**       |użytkownik tworzący komentarz
   |**posx**        	  | 	int 	    |                    | pozycja komentarza w osi x
   |**posy**        	  | 	int 	    |                    | pozycja komentarza w osi y
   |**width**        	  | 	int 	    |                    | szerokość komentarza
   |**height**        	  | 	int 	    |                    | wysokość komentarza
   |**marktodel**  	  | bit             |                    |


### Tablica **PERMISSIONS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**        	  | 	int 	    |                    | numer kolejny wpisu
   |**dst_objtype**       |      int        |                    |
   |**dst_objid**         |      int        |                    | 
   |**proptype**          |      int        |                    | 
   |**permtype**          |      int        |                    | 
   |**objtype**       	  | 	int 	    |                    | 
   |**objid**        	  | 	int 	    |                    | 
   |**marktodel**  	  | bit             |                    |
   |**classattribs_id**   | 	int         | ATTRIBDICTS **id** | uprawnienie do atrybutu
   |**marktodel**  	  | int             |                    |
   |**docstate** 	  | int             |                    |status dokumentu wartości: **0** - katalog wczytane, **1** - katalog rozpoznawane, **2** - katalog do sprawdzenia, **3** - katalog repozytorium
   |**authschemas_id**    | 	int          |AUTHSCHEMAS **id**  | powiązany schemat autoryzacji
   
### Tablica **PROCESS_ACTIONS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**dst_objid**         |      int        |                    |
   |**intid**             |      int        |                    | 
   |**insintid**          |      int        |                    | 
   |**insintid2**         |      int        |                    | 
   |**dst_objtype**       |      int        |                    |
   |**ptype**             |      int        |                    |


### Tablica **PROCESS_CNDFUNCTS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**dst_objid**         |      int        |                    |
   |**actionsintid**      |      int        |                    |
   |**intid**             |      int        |                    | 
   |**type**              |      int        |                    | 
   |**lvariable_id**      |      int        |                    | 
   |**cndtype**           |      int        |                    | 
   |**rvariable_id**      |      int        |                    |
   |**rconst**            | nvarchar(1024)  |                    |
   |**grptype**           |      int        |                    |
   |**grpintid**          |      int        |                    |
   |**dst_objtype**       |      int        |                    |
   |**lcolumn**           |nvarchar(100)    |                    |

### Tablica **PROCESS_VARCOLUMNS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**dst_objid**         |      int        |                    |
   |**dst_objtype**       |      int        |                    |
   |**intid**             |      int        |                    | 
   |**name**              | nvarchar(100)   |                    |
   |**type**              |      int        |                    | 
   
### Tablica **PROCESS_VARIABLES** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**dst_objid**         |      int        |                    |
   |**intid**             |      int        |                    | 
   |**name**              | nvarchar(100)   |                    |
   |**description**       |      ntext      |                    |
   |**type**              |      int        |                    | 
   |**evalcode**          | nvarchar(1024)  |                    |
   |**dst_objtype**       |      int        |                    |

### Tablica **SIGNATURES** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**        	  |  varchar(32)   |                     | numer unikalny dla sygnatury
   |**documents_id**      | int             | DOCUMENTS **id**   |powiązanie z dokumentem
   |**users_id**          | int             | USERS **id**       |użytkownik
   |**sighours**          |      int        |                    | okres ważności sygnatury w godzinach
   |**CreatedAt**         | 	datetime    |                    | data utworzenia wpisu
   
   
### Tablica **STATES** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**Country**        	  |  varchar(32)    | COUNTRIES **code** | powiązany kraj
   |**Code**        	  |  varchar(32)    |                    | kod województwa
   |**Name**        	  | nvarchar(128)   |                    | nnazwa województwa
    
### Tablica **USERGROUPS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**id**        	  |  varchar(32)   |                     |numer unikalny dla grupy
   |**name**              | nvarchar(100)   |                    |nazwa grupy
   |**description**       |      ntext      |                    |opis grupy
   |**CreatedAt**         | 	datetime    |                    | data utworzenia wpisu
   |**UpdatedAt**         | 	datetime    |                    | data aktualizacji wpisu
   |**grouprole**         |      int        |                    | rola dla grupy wartości: **0** - ogólna, **1** - twórca, **2** - administratorzy
   |**globalid**          | 	varchar(36) |                    | unikalny identyfikator
   
### Tablica **USERGROUPUSERS** 

   | Kolumna              | Typ danych      |    Odwołanie       | Opis |
   | -------              | ----            | -----              | ------| 
   |**usergroups_id**     |      int        |USERGROUPS **id**   | grupa użytkownikó
   |**users_id**          | int             | USERS **id**       |użytkownik
   
### Tablica **USERS** 

   | Kolumna              	| Typ danych      |    Odwołanie       | Opis |
   | -------              	| ----            | -----              | ------| 
   |**id**			| int             |                    |numer unikalny dla użytkownika
   |**name**			|nvarchar(100)	  |                    |nazwa użytkownika
   |**pass_md5**		|varchar(50)	  |                    |hasło zakodowane w md5
   |**isadmin**			| bit             |                    |dostęp do administratora spumy wartości: **0** - nie, **1** - tak
   |**smtp_address**		| nvarchar(100)   |                    |SMPT - adres serwera
   |**smtp_port**		| int             |                    |SMPT - port
   |**smtp_user**		|nvarchar(255)	  |                    |SMPT - użytkownik
   |**smtp_password**		| varchar(255)    |                    |SMPT - hasło
   |**email_reply**		| varchar(255)    |                    |adres email użytkownika
   |**email_template**		|ntext		  |                    |adres email szablon stopki
   |**cmppermtype**		| int             |                    |uprawnienia do firmy wartości: **0** - Wszystkie, **1** - brak, **2** - wybrane
   |**usrpermtype**		| int             |                    |uprawnienia użytkownika nie używane stara funkcjonalność
   |**clspermtype**		| int             |                    |uprawnienia klasy nie używane stara funkcjonalność
   |**CreatedAt**		| 	datetime  |                    |data utworzenia wpisu
   |**UpdatedAt**		| 	datetime  |                    |data aktualizacji wpisu
   |**commentcolor**		| int             |                    |kolor komentarzy
   |**authlevel**		| int             |                    |
   |**iscreator**		| bit             |                    |twórca wartości: **0** - nie, **1** - tak
   |**issys**			| bit             |                    |systemowy wartości: **0** - nie, **1** - tak
   |**username**		| varchar(255)    |                    |imię i nazwisko
   |**recent**			| int             |                    |ilośc ostatnich dokumentów
   |**repl**			| bit             |                    |zastępwstwo dla użytkownika wartości: **0** - nie, **1** - tak
   |**replstart**		| 	datetime  |                    |zastępwstwo data od
   |**replend**			| 	datetime  |                    |zastępwstwo data do
   |**rep_users_id**		| int             | USERS **id**       |zastępwstwo użytkownik zastępujący - pierwszy  
   |**rep_users_id2**		| int             | USERS **id**       |zastępwstwo użytkownik zastępujący - drugi 
   |**islocked**		| bit             |                    |zablokowany wartości: **0** - nie, **1** - tak
   |**visfldtp1**		| int             |                    |
   |**visfldtp2**		| int             |                    |
   |**visfldtp3**		| int             |                    |
   |**visfldtp4**		| int             |                    |
   |**organizations_id**	| int             |ORGANIZATIONS **id**| powiązanie z organizacją
   |**dailycorrclass_id**	| int             |DAILYCORRCLASS **id**|powiązanie z klasą dziennika korespondencji
   |**signature**		|image		  |                    |zdjęcie podpisu użytkownika
   |**globalid**		|varchar(36)	  |                    | unikalny identyfikator
   |**lang**			| int             |                    |język **0** - angielski, **1** - polski
   |**imap_address**		| varchar(255)    |                    |IMAP - host
   |**imap_port**		| int             |                    |IMAP - port
   |**imap_user**		|nvarchar(255)	  |                    |IMAP - użytkownik
   |**imap_password**		| varchar(255)    |                    |IMAP - hasło
   |**imap_ssl**		| bit             |                    |IMAP - ssl wartości: **0** - nie, **1** - tak
   |**imap_vflds**		| varchar(255)    |                    |IMAP - folder

### Tablica **USERS_DOCINTERFACECONFIGS** 

   | Kolumna      | Typ danych     |    Odwołanie       | Opis |
   | -------      | ----           | -----              | ------| 
   |**int_id** 	  |int             |                    | numer unikalny integracji	
   |**users_id**  |int             |USERS **id**        | użytkownik przypisany do integracji            
   |**name**	  |nvarchar(255)   |			|nazwa integracji
   |**type**	  |int             |                    |typ integracji  wartości: **0** - KSeF             
   |**company_id**|int             | COMPANIES **id**   |powiązanie z firmą              
   |**userid**	  |nvarchar(128)   |			|login do integracji
   |**password**  |nvarchar(128)   |			|hasło do integracji

### Tablica **USERS_EVENTRESTRICTIONS** 

   | Kolumna      	 | Typ danych     |    Odwołanie       | Opis |
   | -------      	 | ----           | -----              | ------| 
   |**users_id**  	 |int             |USERS **id**        | użytkownik            
   |**eventtype** 	 | 	int       |                    |rodzaj powiadomienia wartości: **0** - wiadomość wewnętrzna, **1** - Prośba o autoryzację , **2** - Autoryzacja dokumentu, **3** - Odrzucenie dokumentu, **4** - Prośba o komentarz, **5** - Skomentowano, **6** - Zmiana na dokumencie obserwowanym, **7** - Zatwierdzenie finalne dokumentu
   |**restrictiontype**  |int             |                    |typ integracji  wartości: **0** - powiadomienie eMail, **1** - wiadomości wewnętrzne 

### Tablica **USERS_EVENTRESTRICTIONS** 

   | Kolumna      	 | Typ danych     |    Odwołanie       | Opis |
   | -------      	 | ----           | -----              | ------| 
   |**users_id**  	 |int             |USERS **id**        | użytkownik  
   |**documents_id**     | int            | DOCUMENTS **id**   |powiązanie z dokumentem
   |**type** 	 	 | 	int       |                    |typ wartości: **0** - ulubiony, **1** - obserwowany

### Tablica **USERS_PERMISSIONS** 

   | Kolumna      	 | Typ danych     |    Odwołanie       | Opis |
   | -------      	 | ----           | -----              | ------| 
   |**users_id**  	 |int             |USERS **id**        | użytkownik  
   |**permtype**  	 |varchar(1)      |                    |typ uprawnienia wartości: **C** - firma
   |**permvalue**  	 |int             |COMPANIES **id**    | w zależności od typu powiązana tabela obiektu 


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
  SPUMA po przetworzeniu dokumentu przez mechanizm OCR sprawdza pola które ten mechanizm rozpoznał. Na podstawie definicji atrybutów klasy ( patrz `Pole schematu` [Klasy / Atrybuty](../manual-reference/#-atrybuty) ) przepisuje rozpoznane wartości do określonych pól. Zanim przepisze uruchamia ww procedurę. Umożliwia to zmianę wartości rozpoznanych przez OCR przed przepisaniem ich do atrybutów.

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
   Kiedy Partnerzy Handlowi rejestrowani są lokalnie (ustawienie `baza wewnętrzna` w   [konfiguracji firmy](../manual-reference#firmy)) funkcja wywoływana jest z bazy `SPUMA`. W przypadku ustawienia `zewnętrzny SOAP` uruchamiany jest z bazy ERP (np SAP Business One) 

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
- **Uwaga!!!:** Funkcja jest używana tylko gdy Partnerzy Handlowi rejestrowani są w  bazie SPUMA (ustawienie `baza wewnętrzna` w   [konfiguracji firmy](../manual-reference#firmy))
- **Obowiązkowa:** Tak
- **Opis:**
  Funkcja zwraca unikatowy kod (w ramach bazy SPUMA)  dla  nowego wpisu do tabeli `BUSINESSPARTNERDB`
- **Parametry wejściowe:**
  - `@dbname` -  Nazwa bazy zewnętrznej (z  [konfiguracji firmy](../manual-reference#firmy) ).
  - `@cardtype` - Typ klienta 

    | cardtype | Opis |
    | --- | --- |
    | `S` | Dostawca |
    | `C` | Odbiorca |

- **Oczekiwane wyjście:**
  Tekst - 250 znaków
