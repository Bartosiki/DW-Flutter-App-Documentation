# Powiadomienia

Aplikacja umożliwia wysyłanie powiadomień do użytkowników, którzy posiadją połączenie z internetem.
Głównym założeniem powiadomienień jest tworzenie przypommnień o dniu wydziału oraz informowanie użytkowników o wygranej
w [Mini-grze](o-aplikacji.md#mini-gra).

## Jak utworzyć powiadomienia?

Tworzenie powiadomień odbywa się poprzez zakładkę `Messaging` w panelu głównym `Firebase`.

> **Trzymaj się instrukcji**
>
> Tworząc nowe powiadomienie, uzupełniaj pola, które są zawarte w instrukcji. Jeżeli dane pole nie jest podane w 
> instrukcji poniżej, oznacza to, że pole to powinno zostać **PUSTE**.
>
{style="warning"}

1.  Wybierz zakładkę `Messaging`. Po wybraniu zakładki powinien ukazać się taki widok.
    ![messeging-home.png](messeging-home.png)
    bądź taki w zależności czy istnieje już jakieś powiadomienie.
    ![notifications-home.png](notifications-home.png)
2.  Następnie wybierz opcję `Create your first campaign` albo `New campaign`
3.  Z okna z wyborem wybierz `Firebase Notification message`
    ![notification-category.png](notification-category.png)
4. Kolejnym krokiem jest uzupełnienie formularza o dane które chcemy żeby powiadomienie zawierało.
    * Po prawej stronie mamy podgląd jak będzie wyglądało takie powiadomienie.*
    * `Notifiaction title` pole to jest tytułem naszej notyfikacji, którą dostanie użytkwonik
    * `Notification text` jest to tekst notyfikacji gdzie zawieramy szczegóły powiadomienia
    * (opcjonalnie)`Notification image` jest to zdjęcie, które chcemy aby się wyświetlało wraz z powiadomieniem
   ![notifiaction-form-step-1.png](notifiaction-form-step-1.png)
5. Po wypełnieniu formularza przejdź do nasępnej cześć o nazwie `Target`
    ![notification-target.png](notification-target.png)
6. W zakładce tej wybieramy docelowe platformy aplikacji gdzie powinno być dostarczone powiadomienie.
   Mamy dwie opcje android oraz ios. Wybieramy z listy najpierw platformę `android` następnie klikamy `Target another app`
   i wybieramy `ios`. **WAŻNE** zwróć uwagę czy na końcu pierwszej linijki z `android` jest słowo kluczowe `and`. Wynik:
   ![notification-target-complete.png](notification-target-complete.png)
7. Następnie przechodzimy do kroku o nazwie `Scheduling`. Tutaj możemy wybrać wiele opcji dotyczących kiedy dane powiadomienie 
   ma być dostarczone. Dostępne opcje to:
   * `now` jest to domyślna opcja, zakłada ona że powiadomienie zostanie od razu wysłane
   * `scheduled` dzięki tej opcji możemy ustawić date i godzinę o której ma zostać wysłane nasze powiadomienie
   * `daily` jest to opcja, która umożliwia cykliczne wysyłanie powiadomień. Możemy wybrać o której godzinie powiadomienie
      ma być wysyłane, ile razy dziennie oraz w jakim przedziale czasowym.
   ![notifiactions-schedule.png](notifiactions-schedule.png)
8. Omijamy zakładkę `Additional options` i klikamy od razu opcję w prawym dolnym rogu `Review`
9. Powinien nam się ukazać taki ekran ![notifications-review.png](notifications-review.png)
10. Aby wysłać powiadomienie należy nacisnąć przycisk `Publish`
11. Po wysłaniu powiadomienia powinien nam się ukazać taki ekran
    ![notifications-home.png](notifications-home.png)
    Ekran ten zawiera podstawowe informacje o parametrach jakie ustawiliśmy oraz o stanie naszych notyfikacji. Czy nadal 
    są wysyłane (status `Active`) albo już zakończone (status `Successful`).

## Jak wysłać powiadomienie do konkretnego użytkownika?

1. Aby wysłać powiadomienie użytkownikowi o tym, że wygrał mini-gre należy najpierw znaleźć go w liście użytkowników.
   * wejdź do panelu głównego firebase 
   * z panelu bocznego wybierz `Firestore Datebase` 
   * wybierz opcję `Query builder` i zbuduj zapytanie w taki sposób(używając `Add to query`)
   ![notifications-query.png](notifications-query.png)
   * poniżej(w query results) powinna wyświetlić się lista z użytkownikami którzy wygrali
   * w liście tej interesuje nas pole `Notification Token`
2. Gdy jesteśmy już w posiadaniu notifiation token wszystkich wygranych należy wejść do zakładki `Firestore Database`
3. Utwórz nową kolekcję za pomocą `Start collection` i nazwij ją `winners`
   ![winners-collection.png](winners-collection.png)
4. W nowo utworzonej kolekcji trzeba od razu dodać pierwszy `Document` podajemy tylko w polu `Document ID` jeden z tokenów
   z zapisanej listy `Notification Token` i klikamy `Save`
   ![winners-token-id.png](winners-token-id.png)
5. Nowo utworzoną kolekcję uzupełniamy dodając nowe dokumenty(jeden dla każdego `Notification Token`)
    w ten sposób wysłane zostały notyfikacje do wygranych użytkowników.