# Konfiguracja aplikacji

Aplikacja została stworzona w taki sposób, by mogła być wykorzystywana co roku podczas Dnia Wydziału EEIA. Jest ona
konfigurowalna, co pozwala na dostosowanie jej do aktualnych potrzeb organizatorów wydarzenia.

> **Firebase**
>
> Do konfiguracji aplikacji warto znać najmniejsze podstawy platformy Firebase, jednak nie jest to konieczne.
>
> Firebase pozwala na zarządzanie bazą danych poprzez interfejs graficzny, i to właśnie tam znajduje się cała
> konfiguracja aplikacji.
>
{style="note"}

## Strona konfiguracyjna - Firebase

Cała konfiguracja przebiega za pomocą platformy Firebase, dostępnej
pod [tym linkiem](https://console.firebase.google.com/u/0/project/dw-flutter-app/overview).

### Zanim zaczniesz

1. Zaloguj się do [Firebase](https://console.firebase.google.com/u/0/project/dw-flutter-app/overview) poprzez konto
   samorządowe.
   > **Konto samorządowe**
   >
   > Email konta samorządowego: `i.nazwisko@samorzad.p.lodz.pl`, gdzie `i` to inicjał imienia.
   >
   > Jeśli nie masz dostępu do konta samorządowego, skontaktuj się z aktualnym koordynatorem działu IT WRSu lub z
   przewodniczącym WRSu.
   >
   {style="tip"}

2. Skontaktuj się z aktualnym koordynatorem działu IT WRSu, by ten przyznał ci dostęp do platformy Firebase.

## Nawigacja po platformie Firebase

1. Po zalogowaniu się do platformy Firebase powinieneś zobaczyć cały panel, jeżeli go jeszcze nie widzisz wybierz
   projekt `dw-flutter-app`. A tak wygląda panel:
   ![firebase-panel.png](firebase-panel.png)
2. Po lewej powinieneś zobaczyć menu, z tego menu będziemy wykorzystywali głównie opcje ` Firebase Database`, `Storage`
   oraz `Messaging`.
   ![left-menu.png](left-menu.png)

## Co jest konfigurowalne?

Co w aplikacji jest konfigurowalne?
<procedure title="📅 Harmonogram wydarzenia" id="harmonogram_wydarzenia">
   <p>
      Można skonfigurować cały harmonogram wydarzenia, wszystkie prelekcje, ich godziny rozpoczęcia i zakończenia, pomieszczenia, w których się odbywają, a także informacje o prelegentach.
   </p>
</procedure>

<procedure title="📷 Zadania QR" id="zadania_qr">
   <p>
      Można skonfigurować zadania QR, które uczestnicy będą musieli wykonać, aby zdobyć punkty.
   </p>
</procedure>

<procedure title="🤝 Partnerzy" id="partnerzy">
   <p>
        Można skonfigurować informacje o partnerach, którzy wspierają wydarzenie. W tym loga, oraz nazwy.
   </p>
</procedure>

<procedure title="🍀 Patroni" id="patroni">
   <p>
        Można skonfigurować informacje o patronach wydarzenia. W tym loga, oraz nazwy.
   </p>
</procedure>

<procedure title="🟦 Kolor aplikacji" id="kolor_aplikacji">
   <p>
      W aplikacji można zmienić kolorystykę, dostosowując ją do aktualnego wydarzenia. Wszystkie kolory aplikacji są pochodne od głównego, skonfigurowanego koloru.
   </p>
</procedure>

<procedure title="⏰ Czas końca konkursu kodów QR" id="czas_konca_konkursu">
   <p>
        Można skonfigurować czas zakończenia konkursu kodów QR. Po tym czasie uczestnicy nie będą mogli zdobywać punktów. Wszyscy uczestnicy zostaną poinformowani o zakończeniu konkursu w postaci powiadomienia w telefonie.
   </p>
</procedure>

<procedure title="✨ Prompt instrukcji asystenta" id="system_prompt">
   <p>
       Prompt instrukcji asystenta to wiadomość, która nadaje kontekst rozmowy asystentowi oraz udostępnia mu wszystkie informacje o wydarzeniu, z których może skorzystać podczas rozmowy.
   </p>
</procedure>

<procedure title="🔔 Powiadomienia" id="powiadomienia">
   <p>
       Można skonfigurować powiadomienia, które będą wysyłane do użytkowników aplikacji. Wszystkie powiadomienia są wysyłane z poziomu platformy Firebase, a konkretnie z zakładki <code>Messaging</code>.
   </p>
</procedure>

<procedure title="🗺️ Mapy wydarzenia" id="mapa_wydarzenia">
   <p>
      Można skonfigurować mapy wydarzenia dla parteru oraz piętra.
   </p>
</procedure>

<seealso style="cards">


    <category ref="app-config">


<a href="Kolor.md"></a>


        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/markup-reference.html">Markup reference</a>


        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/manage-table-of-contents.html">Reorder topics in the TOC</a>


        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/local-build.html">Build and publish</a>


    </category>


</seealso>