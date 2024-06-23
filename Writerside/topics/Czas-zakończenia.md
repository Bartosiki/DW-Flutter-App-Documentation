# Czas zakończenia

Czas zakończenia wyznacza datę kiedy kończy się [Mini-gra](o-aplikacji.md#mini-gra). Po tym czasie użytkownicy nie będą 
w stanie skanować zadań, a tym samym zdobywać punktów. Po tym czasie wyznacza się wygranych a następnie wysyła do nich
[powiadomienia](Powiadomienia.md).

### Jak zmienić czas zakończenia
1. Aby zmienić czas zakończenia [Mini-gry](o-aplikacji.md#mini-gra). Należy przejść do zakładki `Firestore Database`
   w konsoli głównej `Firebase`
2. Następnie z dostępnych `Kolekcji` należy wybrać kolekcję `contestTime`
   ![contest-time.png](contest-time.png)
3. Aby edytować pole należy wybrać opcję edycji
   ![contest-time-edit.png](contest-time-edit.png)
4. Następnie należy ustawić odpowiednią datę i godzinę
   ![contest-time-edit-picker.png](contest-time-edit-picker.png)
5. Ostatnią czynnością jest kliknięcie przycisku `Update`