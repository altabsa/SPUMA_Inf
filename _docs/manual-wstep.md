---
title: "Informacje ogólne"
permalink: /docs/manual-intro/
excerpt: "Dokumetacja SPUMA - elektroniczny obieg dokumentów"
---

# Wstęp
Spuma :copyright: to rozbudowany system klasy DMS (Document Managment System - Sytem Zarządzania Dokumentami).
Jego głównym zadaniem to zarządzanie, przetwarzanie , porządkowanie i sterowanie przepływem dokumentacji w firmie.

# System DMS
Systemy DMS to narzędzia informatyczne pozwalające na przetwarzanie róznych dokumentów powstających w firmach. Przetwarzanie najczęsciej dotyczy:
 - papierowych jak i elektronicznych  dokumentów wewnętrznych firmy takich jak
   - zarządzenia,
   - zapotrzebowania,
   - dokumenty działu HR,
   - polecenia wyjazdu i rozliczenia ich,
   - atesty,
   - polisy 
   - i inne
 - papierowych jak i elektronicznych  dokumentów wpływających do firmy
   - z  zamówienia od klientów, 
   - faktury, 
   - listy
   - i inne
   
Systemy te wspomaga w szczególny sposób wspomagają obszar gromadzenia i organizowania zasobów wiedzy.

Aplikacje DMS bardzo często wykorzystują narzędzia OCR (Optical Character Recognition) przetwarzające dokumenty z formy papierowej (graficznej) w formę tekstową, dającą się w prosty sposób indeksować i zapisywać we wszelkiego rodzaju komputerowych bazach danych.

# Główne funkcje systemu
- Digitalizacja dokumentów  (OCR)
	 - OCR podstawowy (rozpoznawanie i indeksowanie słów)
	 - OCR zaawansowany ( rozpoznawanie określonych pól na dokumentach)
 - Przechowywanie dokumentów 
	 - Kategoryzowane repozytorium (katalogi)  
	 - Dane przechowywane w bazie 
	 - Definiowanie  klasy dokumentu
	 - Rozbudowane możliwości wyszukiwania:
		 - po atrybutach
		 - po słowach kluczowych
		 - po rozpoznanych przez  OCR słowach
 - Zabezpieczanie dostępu
	 - Definiowanie użytkowników i grup
	 - Rozbudowany system uprawnień 	 
	 - Szyfrowany przesył danych
 - Opisywanie dokumentów
	 - Opisywanie atrybutami zarówno standardowymi jak i własnymi
	 - Opisywanie tabelaryczne (np. koszty dla poszczególnych pozycji)
	 - Mechanizm komentarzy 
	 - Kojarzenie dokumentów ze sobą
 - Definiowanie klas dokumentów
	 - Tworzenie własnych atrybutów
	 - Tworzenie zarówno słowników statycznych jak i interaktywnych, pobierających dane  z dowolnego źródła SQL
 - Zatwierdzanie dokumentów
	 - Predefiniowane schematy zatwierdzeń
	 - Edycja schematów Ad-Hoc
	 - Interaktywne procesy zatwierdzeń ( kolejne kroki zależne od poprzednich)
	 - Automatyczne powiadomienia
	 - Poczta wewnętrzna
 - Analizy
	 - Raporty
	 - Filtry
	 - Grupowanie
	 - Alarmy
 - Generowanie dokumentów
	 - Dokumenty własne (edytor  dokumentów online) 
	 - Dokumenty tworzone z szablonów (wnioski urlopowe , delegacje itp)
 - Pozostałe
	 - Dzienniki korespondencji z konfigurowalnymi atrybutami
	 - Definiowanie operacji automatycznych (np księgowania do sytemu ERP)
	 - Powiązania z systemem ERP (baza klientów , podgląd dekretów)
	 - Definiowanie zastępstw

# Architektura platformy
![s1](https://user-images.githubusercontent.com/13116051/139230518-bdcea49a-f026-44f9-8741-7542914e810e.png)

**SPUMA DataService** - Serwer danych (usługa Windows) odpowiadający za komunikacje z bazą danych (na serwerze SQL)

**Serwer WWW** - Serwer hostujacy aplikację  kliencką SPUMA (HTML5). (IIS , Apache itp)

**Spuma Administrator** - Aplikacja (.exe) dla administartora systemu

**Spuma DTS** - WebService (IIS) służacy do wymiay danych z zewnętrznymi aplikacjami (API)



# Baza Danych
[Opis bazy danych](../manual-dbhelp/)

# Instalacja
[Instrukcja instalacji](../manual-install/)

# Opis funkcji systemu
[Podręcznik funkcji systemu](../manual-reference/)
