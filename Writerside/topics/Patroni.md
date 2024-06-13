# Patroni

Konfiguracja patronów polega na dodawaniu kolejnych **patronów i ich logo** do listy widocznej w ustawieniach profilu w aplikacji.

Konfiguracja jest bardzo podobna jak dla [partnerów](Partnerzy.md).

## Skład patrona

> **Trzymaj się struktury**
>
> Dodając nowego patrona, upewnij się że struktura zgadza się z bazową i nie zawiera żadnych literówek / różnic w kapitalizacji liter.
>
{style="warning"}

| Pole        | Typ                  | Przykład    |
|-------------|----------------------|-------------|
| imageSrc    | string               | Truvant.png |
| name        | string               | Truvant     |



## Jak dodać patrona?
Dodanie patrona oprócz samego uzupełnienia `Firestore Database` wymaga również skorzystania z zakładki `Storage`.

1. W menu przedstawionym w sekcji [Konfiguracja aplikacji](Konfiguracja-aplikacji.md#nawigacja-po-platformie-firebase) wybierz `Storage`
2. Przejdź do `patrons`
3. Wybierz `Upload file` i wrzuć logo patrona
   ![patrons-storage.png](patrons-storage.png)
4. Zdjęcie powinno zostać wrzucone, teraz należy uzupełnić bazę
5. W menu przedstawionym w sekcji [Konfiguracja aplikacji](Konfiguracja-aplikacji.md#nawigacja-po-platformie-firebase) wybierz `Firestore Database`
6. Wybierz zakładkę `patrons`, powinieneś mieć taki widok:
   ![patrons-firestore.png](patrons-firestore.png)
3. Kliknij `+ Add document`, powinno otworzyć ci się okienko
4. Wybierz `Auto-ID` i uzupełnij wszystkie pola (możesz w tym okienku uzupełnić jedno, i potem z normalnego widoku dodać resztę)
5. Po uzupełnieniu wszystkich pól zgodnie z instrukcją powinieneś już widzieć dodanego patrona w liście patronów w aplikacji w ustawieniach profilu.
   > **Nie widać patrona?**
   >
   > Jeśli nie widzisz dodanego patrona upewnij się, że nie popełniłeś literówki w żadnej nazwie pola, oraz w żadnej typowanej wartości, oraz że zdjęcie jest poprawnie wrzucone.
   >
   {style="note"}



## Usuwanie / edytowanie

Edytowanie patrona przebiega w bardzo prosty sposób, możesz dowolnie edytować każde pole (pod warunkiem, że zgadza się ono z narzuconą strukturą).

Chcąc usunąć patrona, wystarczy w środkowej kolumnie patronów znaleźć ten "dokument", który odpowiada wydarzeniu które chcesz usunąć. Po najechaniu na niego możesz kliknąć trzy kropki i wybrać `Delete document`. Dobrze jeśli również usuniesz zdjęcie patrona ze `Storage`. 