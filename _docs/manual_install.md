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

# Sprawdzenie instalacji
**proszę** tu dodac tekst
