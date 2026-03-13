# Responsive Login Page

Dieses Projekt ist die Lösung für die Programmieraufgabe "Responsive Login Page". Es wurde eine statische Webseite mit HTML und CSS erstellt, die alle Anforderungen aus dem PDF erfüllt.

## Struktur

Das Projekt besteht aus den folgenden Dateien:

- `index.html`: Enthält die semantische Struktur der Webseite, inklusive Header, Content-Bereich mit Text und Login-Formular sowie einen Footer.
- `style.css`: Beinhaltet das gesamte Styling, von Layout und Farben bis hin zu responsiven Anpassungen und Animationen.
- `README.md`: Diese Datei, die das Projekt und die getroffenen Entscheidungen dokumentiert.

## Design- und Implementierungsentscheidungen

Bei der Umsetzung wurden die Aufgaben aus dem PDF schrittweise abgearbeitet. Hier sind die zentralen Entscheidungen pro Aufgabe erläutert:

### Aufgabe 1: Layout festlegen

Das Grundlayout (Header, Content, Footer) wurde mit **Flexbox** realisiert. Der `<body>`-Tag wurde zu einem Flex-Container mit `display: flex` und `flex-direction: column`. Dadurch ordnen sich die Hauptbereiche automatisch untereinander an. Der Content-Bereich (`<div class="content">`) erhielt `flex-grow: 1`, damit er den gesamten verfügbaren vertikalen Raum zwischen Header und Footer einnimmt. Dies ist eine robuste und moderne Methode für solche Standard-Layouts.

### Aufgabe 2: Elemente einmitten

Um den Text auf breiten Bildschirmen lesbar zu halten und nicht am Rand "kleben" zu lassen, wurden drei CSS-Eigenschaften kombiniert:

1.  `padding`: Ein Innenabstand im `.content`-Container sorgt für den nötigen Leerraum zu den Bildschirmrändern.
2.  `max-width`: Eine maximale Breite für den `.content`-Container verhindert, dass die Textzeilen auf sehr grossen Monitoren zu lang und damit schwer lesbar werden.
3.  `margin: 0 auto`: Zentriert den `.content`-Block horizontal auf der Seite, sobald die maximale Breite erreicht ist.

### Aufgabe 3: Farben und Schriften

Für das Design wurde ein modernes **Dark-Theme** gewählt. Dies ist oft augenschonender und wirkt elegant. Die Farbpalette besteht aus:

-   **Hintergrund**: Ein dunkler, bläulich-violetter `linear-gradient` (`#1a1a2e` zu `#0f3460`).
-   **Text**: Ein helles Grau (`#e0e0e0`) für den Fliesstext, um einen guten, aber nicht zu harten Kontrast zu schaffen.
-   **Akzentfarbe**: Ein kräftiges Pink/Rot (`#e94560`) für wichtige Elemente wie den Header/Footer-Rand, Überschriften und den Button, um die Aufmerksamkeit des Nutzers zu lenken.

Als Schriftart wurde **Inter** via Google Fonts gewählt. Sie ist eine sehr gut lesbare, neutrale Sans-Serif-Schrift, die sich hervorragend für User Interfaces eignet.

### Aufgabe 4: Styling und Formular hinzufügen

Das Login-Formular wurde als separater Block (`<div class="login-box">`) innerhalb des Content-Bereichs implementiert.

-   **Layout**: Die Formular-Elemente (Labels, Inputs, Button) wurden ebenfalls mit `display: flex` und `flex-direction: column` untereinander angeordnet. Ein `gap` sorgt für konsistente Abstände.
-   **Design**: Der Kasten erhielt einen dezenten `border` und abgerundete Ecken (`border-radius: 16px`) für ein weicheres Aussehen. Ein leichter `backdrop-filter: blur(6px)` und eine semi-transparente Hintergrundfarbe lassen den Kasten modern und wie 
ein "Glas"-Element über dem Hintergrund erscheinen (Glassmorphism-Effekt).
-   **Button-Animation**: Der "Absenden"-Button hat eine `transition` für die Eigenschaften `background-color`, `transform` und `box-shadow`. Bei `:hover` (Mouseover) ändert sich die Hintergrundfarbe, der Button bewegt sich leicht nach oben (`transform: translateY(-2px)`) und erhält einen Schatten, was ihm eine interaktive und dreidimensionale Anmutung verleiht.

## Entscheidung zur Repository-Struktur

Für die Abgabe wurde ein **neues, sauberes Verzeichnis** erstellt. Dies hat mehrere Vorteile gegenüber der Erweiterung oder Überschreibung eines bestehenden Repositories:

-   **Klarheit**: Das Repository enthält nur den Code, der für diese spezifische Aufgabe relevant ist. Es gibt keine Ablenkungen durch alte oder andere Projekte.
-   **Einfachheit**: Ein neues Repository ist am einfachsten zu bewerten. Der Prüfer muss nicht nach Branches suchen oder den Verlauf analysieren, um die richtige Version zu finden.
-   **Professionalität**: Es demonstriert die Fähigkeit, ein Projekt von Grund auf sauber zu strukturieren und zu versionieren.

Ein Branch wäre eine gute Option in einem grösseren, laufenden Projekt gewesen, aber für eine isolierte Aufgabe wie diese ist ein dediziertes Repository die beste Wahl.
