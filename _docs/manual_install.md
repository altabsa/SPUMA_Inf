---
title: "Instalacja"
permalink: /docs/manual-install/
excerpt: "Dokumetacja SPUMA - instrukcja instalacji"
---
# Wstęp
Niniejszy dokument jest instrukcją ręcznej instalacji systemu obiegu dokumentów SPUMA.
Dodatkowo zawiera  instalacje opcjonalne 
-  mechanizmy OCR
-  połączenia z SAP Business One (SAP)
-  dane DEMO

# Wymagania
## Serwer
- System operacyjne Windows 7 i wyżej (32 lub 64 bit) lub system serwerowy Windows serwer 2003 i wyżej
- Serwer MSSQL w wersji 2005 i wyżej
- IIS od wersji 6.0 wzwyż lub inny serwer HTML (np. WAMP)
- Zainstalowane biblioteki Microsoft .Net w wersjach 2.0 i 4.2.7
- *(opcjonalnie)* Biblioteki DI dla SAP Business One w wersji 9.0 lub wyżej
 
## Stanowisko robocze
- Dowolny system operacyjny  z przeglądarką (Chrome, Safari, Firefox lub Edge)

❗ Aplikacja nie będzie działac poprawnie na przegladarkach Interet Explorer

# Architektura aplikacji
![s1](https://user-images.githubusercontent.com/13116051/139230518-bdcea49a-f026-44f9-8741-7542914e810e.png)

**SPUMA DataService** - Serwer danych (usługa Windows) odpowiadający za komunikacje z bazą danych (na serwerze SQL)

**Serwer WWW** - Serwer hostujacy aplikację  kliencką SPUMA (HTML5). (IIS , Apache itp)

**Spuma Administrator** - Aplikacja (.exe) dla administartora systemu

**Spuma DTS** - WebService (IIS) służacy do wymiay danych z zewnętrznymi aplikacjami (API)

# Instalacja serwera
## Baza SQL
Bazę instalujemy poprzez skrypt zawarty w pliku [SpumaNewDB](SPUMA_NewDB.sql)

>**Uwaga:** Instalacja ustawiona jest na domyślną instancję o nazwie SPUMA. Jeśli nazwa jest inna, należy ją zmienić w pliku  `SPUMA_NewDB.sql` w części `:SETVAR DBName "SPUMA"`

Skrypt wywołujemy z SQL Server Managment Studio (SSMS) lub z linii poleceń 

>**Uwaga:** Jeśli skrypt wywoływany jest z SSMS należy ustawić SQLCMD Mode


![Jeśli skrypt wywoływany jest z SSMS należy ustawić SQLCMD Mode](https://user-images.githubusercontent.com/13116051/139239467-6ebc4c9c-2214-44db-be59-16bcffe387aa.png)

## Pliki

Na serwerze należy utworzyć (najlepiej w lokalizacji `c:\spuma\`) następującą strukturę katalogów
- **SERVER**
Zawiera
	- usługę `SPUMA_DataService` -  serwis wymiany danych  dla SPUMA,
	- aplikację administracyjną `SPUMA_Admin`,
	- aplikacje pomocniczą `SPUMA_Host` do wywoływania bibliotek innych systemów (m in. SAP Business One).
	- aplikacje pomocniczą `SBOBusinessPartner` do obsługi Partnerów Handlowych z SAP Business One
	- aplikację `SPUMA_DTS` do wsadowego importu danych do SPUMA z plików XML (opcjonalnie)
- **MAIN**
	- Aplikacja WWW – front-end systemu SPUMA (HTML5)
- **OCR** *(opcjonalnie – jeśli serwer OCR lokalny)*
	- Usługa OCR 

> **Uwaga:** Jeżeli serwerem WWW jest IIS należy do katalogu SPUMA nadać uprawnienia dla zapisu i odczytu dla IUSR  oraz użytkownika uruchamiające usługę SPUMA_DataService

Pliki przegrywamy z FTP i umieszczamy w katalogach.

Przed następnym krokiem  należy zmienić plik `spuma.ini` i zmienić dane połączeniowe do bazy SQL.
```
DataSource=servername
UserID=sa
Password=plaintextpass
DBName=SPUMA
```
❗ Hasło do bazy podajemy niezaszyfrowane. Serwis zaszyfruje je przy pierwszym uruchomieniu. ❗

## Konfiguracja wstępna

Wstępna konfiguracja odbywa się przez program `SPUMA_Admin`.

![SPUMA Admin login form](https://user-images.githubusercontent.com/13116051/139413759-fb4a04b2-110f-4285-b15e-c6909f805317.png)

Bez podawania loginu i hasła naciskamy Zaloguj. Pojawią się ustawienia inicjalne

![i3](https://user-images.githubusercontent.com/13116051/139413809-bc673f28-7e01-43a2-b766-743802c260a5.png)
  

> **Uwaga:** Konfiguracja usługi OCR (SOS) ustawiona jest na serwer testowy. Proszę po starcie zmienić wg danych otrzymanych od sprzedawcy systemu

Teraz należy dokończyć konfiguracje bezpośrednio w programie `SPUMA_Admin`. 

### Konfiguracja

Należy wybrać zakładkę konfiguracja i wybrać pierwszy wpis (config)
W tym momencie aplikacja stworzy domyślne wpisy konfiguracyjne.

> Kompletny opis konfiguracji opisany jest w innej części tego dokumentu.

Poniżej ustawienia na które powinno się zwrócić uwagę przed startem serwisu SPUMA_DataService 
<a id='konfiguracja1' href='konfiguracja1' hidden='true'></a>
#### OGÓLNE
`Client ID` – id klienta dla serwera OCR (patrz instalacja OCR)

#### DATASERVICE
`POLICYPORT` –port zasad do otwarcia połączenia TCP (dla danych binarnych)

> **Uwaga:**  Gdy zainstalowanych jest  więcej niż jedna usługa w pozostałych instalacjach ustawić 0

`POLICYALLOWEDPORTS` – porty które mogą być przydzielane  w ramach  zasad 

> **Uwaga:**  Gdy zainstalowanych jest  więcej niż jedna usługa, wpis  ma znaczenie tylko w instalacji gdzie ustawiony jest POLICYPORT

`PORT` – port dla danych binarnych,  na którym usługa obsługuje klienta Silverlight oraz klienta mobilnego  (otworzyć na firewalll’u)
`HTTPPORT`  – Port na którym usługa obsługuje klienta WWW (otworzyć na firewalll’u)
`REQTIMEOUT` – czas oczekiwania na usługę (w sek.)
`MAXTHREADS` – ilość jednoczesnych wątków serwisu  (najlepiej zostawić 10)


#### SBOBUSINESSPARTNER
Patrz  [Konfiguracja SBOBUSINESSPARTNER](#konf_sbobusinesspartner)

#### SAPB1UTILS
patrz  [konfiguracja SAPB1Utils](#konf_sapb1utils)
### <a id='firmy1' href='firmy1' hidden='true'></a>Firmy
Należy wybrać zakładkę `Firmy` i wybrać domyślny wpis (OEC Computers)

#### OGÓLNE
`NAZWA`–  Nazwa firmy jaka będzie widoczna w katalogu
`BAZA` – Nazwa bazy SAP

#### PARTNERZY HANDLOWI
TYP POŁĄCZENIA
- `zewnętrzny SOAP` – Klient (PH) pobierane i aktualizowane w sap (zostawić jak instalacja z SAP)
- `baza wewnętrzna` – PH w bazie SPUMY (instalacja bez SAP)

## Instalacja SPUMA_DATASERVICE

Serwis instaluje się przez wywołanie pliku `installAndRun_release.bat`

> **Uwaga:**  Jeśli istnieje już jeden serwis SPUMA_DATASERVICE przed uruchomieniem należy wyedytować pliki:
> 
>     installAndRun_release.bat
>     startDataService.bat
>     stopDataService.bat
>     uninstall.bat
> 
> oraz nadać unikatową nazwę serwisowi w polu `/ServiceName=????` oraz
zastąpić tą nazwą startowanie i zatrzymywania usługi przy poleceniach **start** i **stop**

Wynikiem działania powinna być uruchomiona usługa SPUMA_DATASERVICE. Aby to sprawdzić należy uruchomić panel usług (Start/Uruchom – wpisać `services.msc`)

> **Uwaga:**  W razie problemów informacje o błędach będą widoczne w pliku `servicelog.txt`


# Instalacja aplikacji klienckiej
## Aplikacja WWW
Po przegraniu wymaganych plików do katalogu `Main` należy ustawić w aplikacji prawidłowy port   serwisu danych w pliku   `assets\config\config.json`. 

Wpisy do zmiany:

    "DATASERVICE_ADR": "localhost:4801"

Zamieniamy adres i port na zgodny z konfiguracja serwera ( Zakładka `DATASERVICE/HTTPPORT`) .


## Konfiguracja IIS
- Uruchomić Menedżer IIS
- PPM :computer_mouse: na Default Web Site
- Dodaj Katalog Wirtulany (Add Virtual Directory)
	- Alias SPUMA
	- Ścieżka fizyczna - podać ścieżkę do katalogu MAIN

![IIS Configuration](https://user-images.githubusercontent.com/13116051/139416855-ea95b877-9f57-4f11-82bc-b4583f81c9a4.png)

> **Uwaga:**  Jeśli jeż już zainstalowana aplikacja o nazwie SPUMA można zmienić nazwę na dowolną inna.
Poprawność instalacji należy sprawdzić przez wpisanie w przeglądarkę adresu `http://localhost/SPUMA/`

# Czynności po instalacji
Czynności które opcjonalnie można wykonać po instalacji systemu:
- Zainstalować OCR  [instrukcja](../manual-ocrinst/)
- Zainstalować DTSSERVICE (odrębny dokument)
- W konfiguracji podpiąć się pod OCR Altab (adres `dc.serwis-altab.pl` port `1099`) 

> Ważny jest tu identyfikator klienta z zakładki `Konfiguracja/Ogólne/Client ID`

- Wczytanie danych demo  (odrębny dokument)
