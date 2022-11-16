---
title: "Log Zmian"
permalink: /docs/changelog/
excerpt: "Dokumetacja SPUMA - elektroniczny obieg dokumentów"
---

Wykaz zmian wprowadzonych w kolejnych wersjach programu

## 6.4.0 

:exclamation: Wymagana zmiana bazy. Przed uruchomieniem należy wykonać skrypt `zmiany_632-640.sql`


### Zmiany

- Kolorowanie komórek w liniach
- Zaznaczanie aktywnego dokumentu
- Wyzwalacza na liniach dokumentu nie związany z określoną linią. Pokazany na zakładce LINIE w stopce 
- Słowniki interaktywne w linach - parametr pobierany z innej kolumny w linii. Obsługa zmiennej systemowej `L[LID][nazwa_pola_z_linii]`
- Jeśli atrybut jest słownikiem użytkownika z dwoma wartościami Y i N to pole formatowane jest jako :white_check_mark:
- Automatyczne kasowanie pustych komentarzy
- `SPUMA ADMIN` - zmiana zachowania kontrolki wybory schematów autoryzacji dla klasy. Oddzielna lista przypisanych schematów. 
- Szyfrowanie hasła do maila (SMTP i IMAP)
- Włączenie wymagalności pola `Odpowiedz na`
- Zmiany w poczcie IMAP
   - Możliwość podawania hasła w kliencie WWW
   - Filtrowanie wiadomości po statusie `przeczytane/nieprzeczytane`
   - Filtrowanie wiadomości po statusie `ma dokumenty / nie ma`
   - Licznik przy skrzynce wiadomości z ilością nieprzeczytanych
- Rozbudowa opcji tworzenia dokumentów z mail'a IMAP
- Autowyliczenie pól sumowanych (linie dokumentu). Przycisk "wylicz przelicza dodane już linie i kwoty tam wpisane proporcjonalnie do kwoty połączonego pola nagłówka
- Formatowanie kolumn raportu ustawiane w `SPUMA ADMIN`. Możliwość ustawienia szerokości, widoczności, wyrównania, ilości po przecinku oraz sumowania.
- Jeśli w 1 kroku procesu autoryzacji wybrany jest tylko `owner` to od razu wyświetlane jest okno zatwierdzania
- Schematy techniczne tworzone automatycznie przy dodawaniu grupy użytkowników,  mają nadawane odpowiednie opisy - np `jeden z grupy x` 
- Automatyczne przypisanie języka polskiego dla nowego użytkownika 
- Zmiana zachowania dla pól  wyliczanych linii podczas importu z pliku.
  - Gdy pole jest w pliku i jest przeliczane nadpisujemy wartość pola
  - Gdy pola nie ma w pliku i jest przeliczane - przeliczamy wg algorytmu
- `SPUMA ADMIN` Możliwość wskazania schematu ręcznego w definicji uprawnień 
- Przejście do wpisów dziennika korespondencji z poziomu dokumentu.
- Zmiana niektorych ikon na material-icons
     

### Poprawki
- Problem z zaznaczaniem poprawnych obszarów tekstowych. Problem występował przy zmianie skali podglądu
- Brak Imienia i nazwiska dla wybrania użytkownika z wyboru w liście parametryzowanej autoryzacji w procesie autoryzacji z poziomu obiegu dokumentu”
- Wyświetlaniu kody zamiast wartości w następujących miejscach
  - zastępstwo
  - dziennik korespondencji typ
- Błąd filtrowania linii dla opcji `tylko niepasujące`
- `SPUMA ADMIN` - Jeśli na słowniku firmy jest zaznaczona opcja podpowiedzi powinno być wymagane uzupełnienie pola wzór. Przy pustej wartości pojawiały się nieoczekiwane wartości.
- Zablokowany użytkownik nie powinien pojawiać się na listach do wyboru na WWW (wiadomości, pytanie o user'a z grupy itp.)
- Błąd w skrzynce IMAP gdy jest tylko 1 mail


