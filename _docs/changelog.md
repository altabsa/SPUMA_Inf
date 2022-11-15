# Log Zmian
Wykaz zmian wprowadzonych w kolejnych wersjach programu

## 6.4.0 

:exclamation: Wymagana zmiana bazy. Przed uruchomnieniem należy wykonać skrypt `zmiany_632-640.sql`


### Zmiany

- Kolorowanie komórek w liniach
- Zaznaczanie aktywnego dokumentu
- Wyzwalacza na liniach dokumentu nie związany z okreslonbą linią. Pokazany na zakładce LINIE w stopce 
- Słowniki interaktywne w linach - parametr pobierany z innej kolumny w linii. Obsługa zmiennej systemowej `L[LID][nazwa_pola_z_linii]`
- Jeśli atrybut jest słownikiem użytkownika z dwoma wartościami Y i N to pole formatowane jest jako :white_check_mark:
- Automatyczbne kasowanie pustych komentarzy
- `SPUMA ADMIN` - zmiana zachowania kontrolki wybory schematów autoryzacji dla klasy. Oddzilena lista przypisanych schematów. 
- Szyfrowanie hasła do maila (SMTP i IMAP)
- Włączenie wymagalności pola `Odpowiedz na`
- Zmiany w poczcie IMAP
   - Możliwość podawania hasła w kliencie WWW
   - Filtrowanie wiadomości po statusie `przeczytane/nieprzeczytane`
   - Filtrowanie wiadomości po statusie `ma dokumenty / nie ma`
   - Licznik przy skrzynce wiadomości z ilością nieprzeczytanych
- Rozbudowa opcji tworzenia dokumentów z mail'a IMAP
- Autowyliczenie pól sumowanych (linie dokumentu). Przycisk "wylicz przelicza dodane juz linie i kwoty tam wpisane propocjonalnie do kwoty połączonego pola nagłówka
- Formatowanie kolumn raportu ustawiane w `SPUMA ADMIN`. Możliwość ustawienia szerokości, widoczności, wyrównania, ilośći po przecinku oraz sumowania.
- Jeśli w 1 kroku procesu autoryzacji wybrany jest tylko `owner` to od razu wyświetla ne jest okno zatwierdzania
- Schematy technicze tworzone automatycznie przy dodawaniu grupy użytkowników,  mają nadawane odpowiednie opisy - np `jeden z grupy x` 
  
  
   
  

### Poprawki
- Problem z zaznaczaniem poprawnych obszarów tekstowych. Problem występował przy zmianie skali podglądu
- Brak Imienia i nazwiska dla wybrania użytkownika z wyboru w liście parametryzowanej autoryzacji w procesie autoryzacji z poziomu obiegu dokumentu”
- Wyświetlaniu kody zamiast wartości w następujących miejscach
  - zastępstwo
  - dziennik korespondencji typ
- Błąd fitlrowania linii dla opcji `tylko nieapusujące`
- `SPUMA ADMIN` - Jeśli na słowniku firmy jest zaznaczona opcja podpowiedzi powinno być wymagane uzupełnienie pola wzór. Przy pustej wartości pojawiały sie nieoczekiwane wartości.
- Zablokowany użytkownik nie powinien pojawiać się na listach do wyboru na WWW (wiadomości, pytanie o user'a z grupy itp)
-  
