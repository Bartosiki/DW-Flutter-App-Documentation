# Wdrożenie Gemini

Gemini jest wdrożony w serwisie Google Cloud, w dokładnie tym samym projekcie w którym jest Firebase.

Cały proces połączenia aplikacji przebiega w taki sposób:

<code-block lang="plantuml">
    @startuml
    participant "Użytkownik" as user
    participant "Aplikacja DW" as app
    participant "Google Cloud Function" as fn
    participant "VertexAI na Google Cloud" as ai
    participant "Baza danych Firebase" as db
    activate user
    user->app : Wysłanie wiadomości\nw konwersacji
    activate app
    app->fn : Żądanie z historią czatu\ni nową wiadomością
    activate fn
    alt Błąd uwierzytelniania Firebase
    fn ---> app : Błąd uwierzytelniania
    app ---> user : Wyświetlenie komunikatu\nbłędu w oknie konwersacji
    end
    fn->ai : Żądanie do Gemini\npoprzez VertexAI
    activate ai
    ai->db : Żądanie do bazy danych\no wiadomość konfiguracyjną
    activate db
    return Wiadomość konfiguracyjna
    alt Błąd w procesie generacji wiadomości
    ai--->fn : Błąd generacji
    fn--->app : Błąd generacji
    app--->user : Wyświetlenie komunikatu\nbłędu w oknie konwersacji
    end
    return Odpowiedź asystenta
    deactivate ai
    fn --> app : Odpowiedź asystenta
    deactivate fn
    app --> user : Wyświetlenie odpowiedzi\nw oknie konwersacji
    deactivate app
    deactivate user
    @enduml
</code-block>

> **VertexAI**
>
> VertexAI to platforma na Google Cloud, która pozwala na tworzenie modeli ML, zarządzanie nimi, a także wdrożenie ich w aplikacjach.
> 
> Projekt wykorzystuje ją w celu komunikacji z modelem Gemini poprzez system płatności tylko za wykorzystane Tokeny (tzn. nie wdrażamy modelu na serwerze, tylko korzystamy z API).
>
{style="note"}

To znaczy:

1. Na Google Cloud stworzona jest funkcja serverless w Node.js, która wykorzystuje bibliotekę `@google-cloud/vertexai` pozwalającą na autoryzowanie się w VertexAI poprzez Service Account. 
2. Funkcja ta otrzymuje request z aplikacji DW, który zawiera historię czatu.
3. Funkcja ta przekazuje request do VertexAI, który zwraca odpowiedź.
4. Funkcja zwraca odpowiedź do aplikacji DW.

Sama funkcja posiada endpoint, który jest wywoływany przez aplikację DW, a także jest zabezpieczony tokenem, który jest generowany przez Firebase Auth.

## Jak zmienić funkcję?

Raczej nie przewidujemy zmiany działania samej funkcji, jest ona zaimplementowana w taki sposób, by działała zgodnie z modelem Gemini 1.5 Flash.

W przypadku zmiany modelu, należy skontaktować się z zespołem odpowiedzialnym za wdrożenie modelu na VertexAI, a także z zespołem odpowiedzialnym za wdrożenie funkcji na Google Cloud.