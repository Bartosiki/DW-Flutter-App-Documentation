# Zadania QR

Konfiguracja harmonogramu polega na dodawaniu kolejnych **zadan QR** do listy zadań wewnątrz aplikacji.

## Skład zadania

> **Trzymaj się struktury**
>
> Dodając nowe zadanie, upewnij się że struktura dodanego zadania zgadza się z bazową i nie zawiera żadnych literówek / różnic w kapitalizacji liter.
>
{style="warning"}

| Pole        | Typ    | Przykład                               |
|-------------|--------|----------------------------------------|
| title       | string | Is it real?                            |
| description | string | Find living green walls                |
| points      | number | 15                                     |
| qrCode      | string | a9de65861c92d54043f781c67be7f99f       |


## Jak dodać zadanie?

1. W menu przedstawionym w sekcji [Konfiguracja aplikacji](Konfiguracja-aplikacji.md#nawigacja-po-platformie-firebase) wybierz `Firestore Database`
2. Wybierz zakładkę `tasks`, powinieneś mieć taki widok:
   ![tasks.png](tasks.png)
3. Kliknij `+ Add document`, powinno otworzyć ci się okienko
4. Wybierz `Auto-ID` i uzupełnij wszystkie pola (możesz w tym okienku uzupełnić jedno, i potem z normalnego widoku dodać resztę)
5. Po uzupełnieniu wszystkich pól zgodnie z instrukcją powinieneś już widzieć dodane zadanie w liście zadań w aplikacji
   > **Nie widać zadania?**
   >
   > Jeśli nie widzisz dodanego zadania upewnij się, że nie popełniłeś literówki w żadnej nazwie pola, oraz w żadnej typowanej wartości, oraz że każdy `taskId` jest unikalny
   >
   {style="note"}



## Usuwanie / edytowanie

Edytowanie zadania przebiega w bardzo prosty sposób, możesz dowolnie edytować każde pole (pod warunkiem, że zgadza się ono z narzuconą strukturą).

Chcąc usunąć zadanie, wystarczy w środkowej kolumnie znaleźć ten "dokument", który odpowiada zadaniu które chcesz usunąć. Po najechaniu na niego możesz kliknąć trzy kropki i wybrać `Delete document`. 