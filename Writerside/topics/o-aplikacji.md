# O aplikacji

## Czym jest aplikacja Dzień Wydziału EEIA?
Aplikacja Dzień Wydziału EEIA to aplikacja mobilna dedykowana Dniu Wydziału EEIA.

Ma ona na celu ułatwienie uczestnikom Dnia Wydziału EEIA dostęp do informacji o wydarzeniu, takich jak:
- harmonogram wydarzenia,
- informacje o prelegentach,
- mapę wydarzenia,
- informacje o sponsorach.

## Jakie są funkcjonalności aplikacji?

Aplikacja pozwala na dostęp do informacji o wydarzeniu, takich jak harmonogram, informacje o prelegentach, mapę wydarzenia oraz informacje o sponsorach.

Umożliwia ona również możliwość zapisywania się na wybrane prelekcje.

Poza częścią informacyjną aplikacja posiada również mini-grę, w której uczestnicy mogą zdobywać punkty za wykonywanie zadań (tj. skanowanie kodów QR umieszczonych w różnych miejscach na terenie wydarzenia).

Oprócz tego, aplikacja posiada wbudowanego inteligentnego asystenta, który odpowiada na pytania uczestników dotyczące wydarzenia.

Bardzo istotną funkcjonalnością aplikacji jest jej konfigurowalność. Została ona stworzona w taki sposób, by mogła być wykorzystywana co roku podczas Dnia Wydziału EEIA. Więcej zostało opisane w sekcji [Konfiguracja aplikacji](Konfiguracja-aplikacji.md).

## Jak korzystać z aplikacji?

Aplikacja jest dostępna na systemy Android oraz iOS. Aby z niej skorzystać, należy ją pobrać ze sklepu Google Play lub App Store.

## Dla kogo jest przeznaczona aplikacja?

Aplikacja jest przeznaczona dla uczestników Dnia Wydziału EEIA, którzy chcą mieć dostęp do informacji o wydarzeniu w jednym miejscu, a także chcą wziąć udział w mini-grze oraz skorzystać z inteligentnego asystenta, czyli dla:
- studentów,
- pracowników naukowych,
- przedstawicieli firm,
- przyszłych studentów.


# O autorach

## Kto stworzył aplikację Dzień Wydziału EEIA?

Aplikacja Dzień Wydziału EEIA została stworzona przez studentów Wydziału Elektrotechniki, Elektroniki, Informatyki i Automatyki Politechniki Lódzkiej. W skład zespołu wchodzą:
- Aleksander Golus
- Bartosz Chadryś
- Mateusz Kłos
- Igor Joński
- Jakub Miśko


## Write content
%product% supports two types of markup: Markdown and XML.
When you create a new help article, you can choose between two topic types, but this doesn't mean you have to stick to a single format.
You can author content in Markdown and extend it with semantic attributes or inject entire XML elements.

## Inject XML
For example, this is how you inject a procedure:

<procedure title="Inject a procedure" id="inject-a-procedure">
    <step>
        <p>Start typing and select a procedure type from the completion suggestions:</p>
        <img src="completion_procedure.png" alt="completion suggestions for procedure" border-effect="line"/>
    </step>
    <step>
        <p>Press <shortcut>Tab</shortcut> or <shortcut>Enter</shortcut> to insert the markup.</p>
    </step>
</procedure>

## Add interactive elements

### Tabs
To add switchable content, you can make use of tabs (inject them by starting to type `tab` on a new line):

<tabs>
    <tab title="Markdown">
        <code-block lang="plain text">![Alt Text](new_topic_options.png){ width=450 }</code-block>
    </tab>
    <tab title="Semantic markup">
        <code-block lang="xml">
            <![CDATA[<img src="new_topic_options.png" alt="Alt text" width="450px"/>]]></code-block>
    </tab>
</tabs>

### Collapsible blocks
Apart from injecting entire XML elements, you can use attributes to configure the behavior of certain elements.
For example, you can collapse a chapter that contains non-essential information:

#### Supplementary info {collapsible="true"}
Content under a collapsible header will be collapsed by default,
but you can modify the behavior by adding the following attribute:
`default-state="expanded"`

### Convert selection to XML
If you need to extend an element with more functions, you can convert selected content from Markdown to semantic markup.
For example, if you want to merge cells in a table, it's much easier to convert it to XML than do this in Markdown.
Position the caret anywhere in the table and press <shortcut>Alt+Enter</shortcut>:

<img src="convert_table_to_xml.png" alt="Convert table to XML" width="706" border-effect="line"/>

## Feedback and support
Please report any issues, usability improvements, or feature requests to our
<a href="https://youtrack.jetbrains.com/newIssue?project=WRS">YouTrack project</a>
(you will need to register).

You are welcome to join our
<a href="https://jb.gg/WRS_Slack">public Slack workspace</a>.
Before you do, please read our [Code of conduct](https://plugins.jetbrains.com/plugin/20158-writerside/docs/writerside-code-of-conduct.html).
We assume that you’ve read and acknowledged it before joining.

You can also always email us at [writerside@jetbrains.com](mailto:writerside@jetbrains.com).

<seealso>
    <category ref="wrs">
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/markup-reference.html">Markup reference</a>
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/manage-table-of-contents.html">Reorder topics in the TOC</a>
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/local-build.html">Build and publish</a>
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/configure-search.html">Configure Search</a>
    </category>
</seealso>