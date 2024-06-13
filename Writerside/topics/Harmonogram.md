# Harmonogram

Konfiguracja harmonogramu polega na dodawaniu kolejnych **wydarzeń** (prelekcji lub szkoleń) do kalendarza wewnątrz aplikacji.

## Skład harmonogramu

> **Trzymaj się struktury**
>
> Dodając nową prelekcję lub szkolenie, upewnij się że struktura dodanego wydarzenia zgadza się z bazową i nie zawiera żadnych literówek / różnic w kapitalizacji liter.
>
{style="warning"}

| Pole        | Typ                | Przykład                                |
|-------------|--------------------|-----------------------------------------|
| title       | string             | Automatyzacja środowiska testowego      |
| category    | string (Category)  | improvement                             |
| description | string             | Uruchamiaj testy szybko i automatycznie |
| partner     | string             | TestersCO                               |
| room        | string             | E2                                      |
| timeStart   | timestamp          | July 2, 2024 at 12:00:00 AM UTC+2       |
| timeEnd     | timestamp          | July 2, 2024 at 13:00:00 AM UTC+2       |
| type        | string (EventType) | lecture                                 |



## Jak dodać wydarzenie?

1. W menu przedstawionym w sekcji [Konfiguracja aplikacji](Konfiguracja-aplikacji.md#nawigacja-po-platformie-firebase) wybierz `Firestore Database`
2. Wybierz zakładkę events, powinieneś mieć taki widok:
   ![events.png](events.png)
3. Kliknij `+ Add document`, powinno otworzyć ci się okienko
4. Wybierz `Auto-ID` i uzupełnij wszystkie pola (możesz w tym okienku uzupełnić jedno, i potem z normalnego widoku dodać resztę)
5. Po uzupełnieniu wszystkich pól zgodnie z instrukcją powinieneś już widzieć dodane wydarzenie w kalendarzu w aplikacji
   > **Nie widać wydarzenia?**
   >
   > Jeśli nie widzisz dodanego wydarzenia, sprawdź najpierw czy nie ustawiłeś dat początku i zakończenia przed dzisiejszą datą, a potem upewnij się, że nie popełniłeś literówki w żadnej nazwie pola, oraz w żadnej typowanej wartości.
   >
   {style="note"}

## Usuwanie / edytowanie

Edytowanie wydarzenia przebiega w bardzo prosty sposób, możesz dowolnie edytować każde pole (pod warunkiem, że zgadza się ono z narzuconą strukturą).

Chcąc usunąć wydarzenie, wystarczy w środkowej kolumnie znaleźć ten "dokument", który odpowiada wydarzeniu które chcesz usunąć. Po najechaniu na niego możesz kliknąć trzy kropki i wybrać `Delete document`. 