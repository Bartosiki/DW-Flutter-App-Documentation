# Partnerzy

Konfiguracja partnerów polega na dodawaniu kolejnych **partnerów i ich logo** do listy widocznej w ustawieniach profilu w aplikacji.

## Skład partnera

> **Trzymaj się struktury**
>
> Dodając nowego partnera, upewnij się że struktura zgadza się z bazową i nie zawiera żadnych literówek / różnic w kapitalizacji liter.
>
{style="warning"}

| Pole        | Typ                  | Przykład    |
|-------------|----------------------|-------------|
| imageSrc    | string               | Truvant.png |
| name        | string               | Truvant     |
| package     | string (PackageType) | silver      |



## Jak dodać partnera?
Dodanie partnera oprócz samego uzupełnienia `Firestore Database` wymaga również skorzystania z zakładki `Storage`.

1. W menu przedstawionym w sekcji [Konfiguracja aplikacji](Konfiguracja-aplikacji.md#nawigacja-po-platformie-firebase) wybierz `Storage`
2. Przejdź do `partners`
3. Wybierz `Upload file` i wrzuć logo partnera
   ![partners-storage.png](partners-storage.png)
4. Zdjęcie powinno zostać wrzucone, teraz należy uzupełnić bazę
5. W menu przedstawionym w sekcji [Konfiguracja aplikacji](Konfiguracja-aplikacji.md#nawigacja-po-platformie-firebase) wybierz `Firestore Database`
6. Wybierz zakładkę partners, powinieneś mieć taki widok:
   ![partners-firestore.png](partners-firestore.png)
3. Kliknij `+ Add document`, powinno otworzyć ci się okienko
4. Wybierz `Auto-ID` i uzupełnij wszystkie pola (możesz w tym okienku uzupełnić jedno, i potem z normalnego widoku dodać resztę)
5. Po uzupełnieniu wszystkich pól zgodnie z instrukcją powinieneś już widzieć dodanego partnera w liście partnerów w aplikacji w ustawieniach profilu.
   > **Nie widać partnera?**
   >
   > Jeśli nie widzisz dodanego partnera upewnij się, że nie popełniłeś literówki w żadnej nazwie pola, oraz w żadnej typowanej wartości, oraz że zdjęcie jest poprawnie wrzucone.
   >
   {style="note"}



## Usuwanie / edytowanie

Edytowanie partnera przebiega w bardzo prosty sposób, możesz dowolnie edytować każde pole (pod warunkiem, że zgadza się ono z narzuconą strukturą).

Chcąc usunąć partnera, wystarczy w środkowej kolumnie partnerów znaleźć ten "dokument", który odpowiada wydarzeniu które chcesz usunąć. Po najechaniu na niego możesz kliknąć trzy kropki i wybrać `Delete document`. Dobrze jeśli również usuniesz zdjęcie partnera ze `Storage`.