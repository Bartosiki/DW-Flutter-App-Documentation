# Wdrożenie Gemini

Gemini jest wdrożony w serwisie Google Cloud, w dokładnie tym samym projekcie w którym jest Firebase.

Cały proces połączenia aplikacji przebiega w taki sposób:

<code-block lang="plantuml">
    @startuml
    participant "Aplikacja DW" as app
    participant "Google Cloud Function" as fn
    participant "VertexAI na Google Cloud" as ai
    app->fn : Request z historią czatu
    activate fn
    fn->ai : Request do Gemini\npoprzez VertexAI
    activate ai
    return success
    deactivate ai
    fn --> app : success
    deactivate fn
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