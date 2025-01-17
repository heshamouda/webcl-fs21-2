# webcl-fs21-2
**Klasse**: 6iCbb

Die *Aufzeichnungen* sowie der aktuelle *Punktestand* der Studierenden sind im jeweiligen Wochenchannel innerhalb von Teams verfügbar.

## Woche 10 - Vorstellung von verschiedenen Frameworks
**Datum/Uhrzeit:** 11.05.2021 - 12:15 bis 15:00

### Themen
Heute keine neuen Slides oder ein Goodie, "nur" Studierendenbeiträge
- SVG-Eyes in **Angular** (A. Gervalla, P. Mühlthaler - [Link zum Repo](https://github.com/MFJonesX/SvgEyesAngular))
  - Präsentation (Timestamps: [09:35] - [33:00])
    - Einführung in Angular allgemein. Aufbau mit TypeScript, HTML + CSS
      - [angular.json](https://angular.io/guide/workspace-config) als Konfigurationsdatei für den Workspace und das Projekt
      - [ts.config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) Konfiguration für Typescript
    - Angular bietet wie andere Frameworks auch ein cli für den einfachen Umgang (Projekt erstellen, Server mit Hot-Reloading, Build etc.)
    - Komentenaufbau für Unabhängigkeit der einzelnen Teile und Wiederverwendbarkeit
    - Services und Shared-Teile für die Verwendung in Komponenten bzw. Aufteilung von gemeinsam genutzten Strukturen
    - Man schreibt html + css mit der gleichen syntax, es ist aber nicht pur. Angular "konvertiert" die Bestandteile -> Probleme mit der Validität etc.
  - Probleme bei der Umsetzung
    - Keine Defaultwerte für die Koordinaten angegeben -> HTML wurde nicht korrekt aufgebaut
    - Debugging mittels Browserkonsole und "Durchdenken"
    - Hinweis, am besten immer immutable Datenstrukturen zu verwenden (was im Browser schwer ist) - Beispiel mit Koordinaten der Maus übergeben, statt den ganzen MouseEvent
  - Fragen & Diskussion (Am besten selbst nachschauen, waren viele und wurden umfangreich beantwortet. Timestamps: [33:30] - [01:02:55])
- SVG-Eyes in **React** (R. von Arx, C. Kym - [Link zum Repo](https://github.com/remo-vonarx/webcl-fs21-2-react-eyes))
  - Präsentation (Timestamps 2. Lektion: [04:20] - [13:55])
    - Einführung in React (Vorallem die Betrachtung der Lifecyclemethoden einer Komponente)
    - Hinweis Debug-Tools (Extensions) für verschiedene Browser
    - Vergleich mit Angular: Schlanker, weniger Vorgaben bzgl. Strukturierung der gesamten Applikation
    - Kleine Diskussion bzgl. Class-Components vs. Functional-Componentens:
      - Class-Components eher für Dinge, für welche man die Lifecycle-Methoden verwenden muss - mit einer return()-function
      - Functional-Components sind "pure" JS-Funktionen (nicht im Sinne einer "normalen" puren Funktion ohne Seiteneffekte), welche den "zu rendernden" Teil zurückgeben (Die return-function ist im Prinzip die Komponente selbst)
    - Verbesserungsvorschlag bzw. Hinweis von Herrn König:
      - Was macht die Komponente, welchen Zustand bewirtschaftet sie?
      - Dinge die für/im Komponent unveränderlich sind -> Props; Dinge die für Komponent veränderlich -> State
  - Fragen & Diskussion (Timestamps 2. Lektion: [14:10] - [32:00])
- SVG-Eyes in **Svelte** (R. Winkelmann - [Link zum Repo](https://github.com/FHNW-RW/webcl-svelte))
  - Präsentation (Timestamps 3.Lektion: [02:00] - [18:00])
    - Einführung in Svelte und Demo
    - Erklärung der Applikationsstruktur, export keyword für Funktionen
    - Sehr schlank im Vergleich zu den bereits vorgestellten Frameworks
    - Tiefergehende Erklärungen, wie die [Elementdirektiven](https://svelte.dev/docs#Element_directives) konkret verwendet wurden
    - Hinweis auf die [Reactive Deklaration](https://svelte.dev/docs#script) bzw. warum dies so verwendet wurde
    - Näherer Erläuterungen zu [Bindings](https://svelte.dev/docs#bind_element_property)
  - Einarbeitung belief sich auf etwa 2-3 Stunden, ging aber gut
  - Fragen & Diskussion (Timestamps 3. Lektion [18:00] - [26:00])
- SVG-Eyes in **VueJs** (P. Schmid, J. Hänggi - [Link zum Repo](https://github.com/Patschee/Webcl_EyesSVG_Haenggi-Schmid))
  - Präsentation (Timestamps 3. Lektion: [28:00] - [32:00])
    - Einführung in VueJs
    - Lösung mit einer einzigen Komponente, welche den bereits bestehenden Code einbettet
    - Hinweis auf das Statemanagement und die Lifecycle-Methoden
  - Fragen & Diskussion (Timestamps 3. Lektion: [34:00] - [35:00])
- Abschliessende Diskussion
  - Hypothetische Aufgabe, die SVG-Eyes zu bauen, mit Einschränkung auf eine schon bestehende Codebasis und vorgegebenem Framework
  - Abstimmung, welche Frameworks nach den Vorstellungen heute präferiert werden

### Empfohlene Aktivitäten auf nächste Woche
- Review
- Punkte im Excel checken :P

### Vergebene Aufgaben
- React (R. von Arx, C. Kym)
- SVG-Eyes in VueJs (P. Schmid, J. Hänggi)
- Svelte (L. Kern, R. Winkelmann)
- SVG-Eyes in Angular (A. Gervalla, P. Mühlthaler)

---

## Woche 9 - Custom Elements & PEP-Projektaufbau
**Datum/Uhrzeit:** 27.04.2021 - 12:15 bis 15:00

### Themen
- Heutige Goodies:
  - [Starwars Lauftext](https://css-tricks.com/snippets/css/star-wars-crawl-text/) von F. Henzmann
    - Timestamps Präsentation (1. Lektion): [02:00] - [18:00]
    - Aufbau: Ebene wird mittels Animation langsam aus dem Bildschrim "gezogen"
    - Behandelte Themen: [perspective](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective), [transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform), [transform-origin](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin)
  - [Signature Animation](./week9/svg-signature-sketch/Signature.html)
    - Timestamps Präsentation (1. Lektion): [18:00] - [41:00]
    - SVG Pfad (hier eine Signatur) soll so animiert werden, dass es so aus sieht, als würde diese live gezeichnet / geschrieben
    - Behandelte Themen: Animation mittels Stroke-Array im Pfad. Funktionsweise wird im Recording ([22:00] - [26:00]) mittels Skizze veranschaulicht
- Custom Elements HTML (Gesamte 2. Lektion [00:00] - [48:57])
  - Nutzung von selbstgebauten HTML Elemente via Tags oder createElement
  - Kurze Ausführungen bzgl. Webcomponents und wie die Begriffe vertauscht werden (Was ist ein Customelement und was Components)
  - Betrachtung des [Square-Beispiels](./week9/custom-elements/CustomElement.html)
    - Aufzeigen der Funktionsweise anhand dieses Beispiels, welche Dinge damit möglich sind und vorallem welche Schwierigkeiten sich daraus ergeben
    - Fragestellung "Was soll das Element unterstützen?" - Manche Eigenschaffen lassen sich aufgrund der Vererbung nicht ignorieren, sind jedoch für das erstellte Element praktisch irrelevant.
  - Adoption von WebComponents (Polymer etc.) nicht so breit wie erwartet. Hinweis, dass diese Dinge der Darstellung dienen aber nicht für die Applikationsstrukturierung, obwohl dies oft genau für das "missbraut".
  - Auflisten von Alternativen zu WebComponents
- Aufbau des begleitenden Projekts der Personaleinsatzplanung (Gesamte 3. Lektion [05:00] - [40:00])
  - Demo des lauffähigen Sketchs als Alternative zu Paper-Prototyp oder Figma/Adobe Xd, welcher als Prototyp zur Veranschaulichung der Idee und Grundfunktionalität dient [13:00] - [27:00]
  - Walkthrough durch den Code [28:00] - [40:00]
    - Styling und HTML [28:00] - [31:00]
    - Relationales Modell im UI [31:00] - [33:00]
    - Javascript [33:00] - [40:00]

### Empfohlene Aktivitäten auf nächste Woche
- Review

### Vergebene Aufgaben
- React (R. von Arx, C. Kym)
- SVG-Eyes in VueJs (P. Schmid, J. Hänggi)
- Svelte (L. Kern, R. Winkelmann)
- SVG-Eyes in Angular (A. Gervalla, P. Mühlthaler)

---


## Woche 8 - Animation (& SVG Teil #2)
**Datum/Uhrzeit:** 20.04.2021 - 12:15 bis 15:00

### Themen
- Heutiges Goodie: [Spotlight Effekt (Eine Art Presenter)](./week8/CssSpotlight.html) - Timestamps Präsentation (1. Lektion): [00:00] - [30:00]
  - Aufbau: Transparentes Overlay mit einer gestylten Box, welche mit einem Key-Event ein Spotlight-Effekt erzeugt
  - Behandelte Themen:  [mix-blend-mode](https://developer.mozilla.org/de/docs/Web/CSS/mix-blend-mode) und Umgang mit der Problematik von Clickevents ([pointer-events](https://developer.mozilla.org/de/docs/Web/CSS/pointer-events), user-input)
  - Von Studierenden vorgeschlagener alternativer Ansatz: Mit [filter](https://developer.mozilla.org/de/docs/Web/CSS/filter) arbeiten
  - Einschub bzgl. Guard-Clauses - Timestmaps (1.Lektion): [12:00-23:00] 
    - Begründung für [diesen Codeteil](https://github.com/WebEngineering-FHNW/webcl-fs21-2/blob/main/week8/CssSpotlight.html#L73) mit Verweis auf [c2wiki](https://wiki.c2.com/?ElseConsideredSmelly).
- Präsentation der Spezialaufgabe über Bézierkurven (P.Schmid, J.Christ)
  - Präsentation mit Einführung, historischer Hintergrund, Verbindung mit SVG und Beispiele: (2. Lektion) [02:00] - [13:00]
    - [Präsentation auf Google Slides](https://docs.google.com/presentation/d/1pT7S8bgJ_2qobJpvkMp6F8IxZadv2XO0bJxByb0Rme8)
    - [Github-Repo](https://github.com/Patschee/webcl-BezierCurve)
  - Fragen und weiterführende Diskussion sowie Inputs von D.König [13:00] - [26:00]
- Weiterführung SVG Thematik von letzter Woche
  - Vergleich mit Canvas. Wann sollte was genutzt werden?
  - Erneuter Hinweis auf die Diskrepanz beim SVG-Export von verschiedenen Tools
- Animation [51:00] - [1:55:00]
  - Nutzen von deklarativen Animationen für numerische Werte, in CSS mit transition, animation und den keyframes. Für komplexere Dinge nicht verwendbar, da nicht implizit "bekannt", was genau animiert werden muss.
  - Für komplexere Dinge "programmatische" Animationen. Nach der Verwendung von Timeouts und Intervals wurde heute die Methode mit [requestAnimationFrame()](https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame) vorgestellt.
  - Beispiel mit dem [SVG Bucket](week8/svg-bucket-sketch/Bucket.html)
  - Tweening (Berechnung von Zwischenschritte beim Animieren) mit Slope-Function (siehe [tween Folder](./week8/tween/View.html))

### Empfohlene Aktivitäten auf nächste Woche
- Review

### Vergebene Aufgaben
- CSS-Goodie (F. Henzmann)

---


## Woche 7 - SVG & Canvas
**Datum/Uhrzeit:** 13.04.2021 - 12:15 bis 15:00

### Themen
- Heutiges Goodie: [Rippleeffekt auf Buttons](./week7/CssRipple.html) - Timestamps Präsentation (1. Lektion): [00:00] - [38:00]
  - Hauptthema des [Goodies sind die CSS-Custom-Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties), welche in diesem Beispiel auch innerhalb von JS genutzt werden. Es wurden verschiedene Möglichkeiten vorgeschlagen, wie man gewisse Daten zentral halten kann, wobei diese Lösung explizit präsentiert wurde.
  - Weitere behandelte Themen: [Clip-Path](https://developer.mozilla.org/de/docs/Web/CSS/clip-path), [mix-blend-mode](https://developer.mozilla.org/de/docs/Web/CSS/mix-blend-mode), [animation mit keyframes](https://developer.mozilla.org/de/docs/Web/CSS/CSS_Animations/Using_CSS_animations) (Man beachte z.B. die Prozentangabe für den Zeitfortschritt, um das Element am Ende wieder auszublenden)
- Präsentation der Spezialaufgabe über das Multi project planning tool (D. Lagger, M. de Laat)
  - Präsentation UI und UX: (2. Lektion) [02:00] - [09:00]
  - Fragen und weiterführende Diskussion [09:00] - [44:42]
    - Diverse Inputs und Ideen für die präsentierte Lösung
- SVG & Canvas anhand des [Progress-Gauge Beispiels](./week7/canvas-gauge-sketch/View.html)
  - Intro (3. Lektion) [00:00] - [08:00]
  - Walkthrough durch den Code, mehr Details zu bestimmten Teilen (3.Lektion) [08:00] - [40:00]
  - Diskussion
    - Hinweis auf "Problematik", dass eine .onclick-Zuweisung im Gegensatz zu addEventListener destruktiv ist bzw. die bisherigen Listener überschreibt/entfernt
    - Die Verwendung von Canvas ist sehr performant und wird GPU-beschleunigt, sofern dies möglich ist.
- Weitere Beispiele (3.Lektion) [40:00] - [52:00]
  - [SVG Eyes](./week7/svg-eyes-sketch/Eyes.html)
    - Hinweis darauf, dass SVGs bei Grafiktools beim Exportieren teilweise "vereinfacht" werden bzw. Informationen verlieren und so eine inkonsistente Darstellung entsteht. Man kann sich dazu meist nur mit einer "händischen" Korrektur helfen
    - Man kann mit Caching und Ebenen arbeiten, damit man bei umfangreicherer Verwendung von Canvas nicht bei jeder Änderung das gesamte Bild neu rendern muss
  - [Steelseries Canvas](https://github.com/HanSolo/SteelSeries-Canvas)
    - Diverse UI-Elemente, welche mit Canvas umgesetzt wurden und in den Demos jeweilig "frei" konfigurierbar sind
### Empfohlene Aktivitäten auf nächste Woche
- Review

### Vergebene Aufgaben
- Einführung in Bezier-Kurven (P.Schmid, J.Christ)

---

## Woche 6 - Projector Pattern mit spezifischem CSS (CSS++)
**Datum/Uhrzeit:** 30.03.2021 - 12:15 bis 15:00

### Themen
- Heutiges Goodie: CSS Specificity (L.Kern) - Timestamps Präsentation (1. Lektion): [19:30] - [29:00]
  - Die Präsentation sowie den dazugehörigen Code findet sich in den MS Teams-Files unter Woche 6
  - Behandelte Themen: [The Cascade](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#the_cascade), [Specificity](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#specificity), [Inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#inheritance), [Specificity Calculator](https://specificity.keegan.st/) & Live-Coding
  - Anmerkungen von D. König sowie Beantwortung von Fragen: 1. Lektion: [29:00] - [34:00] & 2. Lektion: [00:00] - [09:00]
- Präsentation über die [Table Projectoren](https://github.com/WebEngineering-FHNW/webcl-fs21-2/pull/9/files) (J.Hadorn, J.Kennedy)
  - Timestamps (2. Lektion): [09:00] - [20:00]
  - Vorstellung der Änderungen innerhalb der Sturktur, welche vorgenommen wurden (Generalisierung des Codes)
  - Vorführen des Nutzens anhand des "Car.js"-Beispiels
- Projector Pattern mit spezifischem CSS
  - Einführung in die Thematik und den Nutzen (2. Lektion) [20:00] - [36:36]
    - Wie wird das CSS organiseriert, welches für den Projector spezifsich ist, wie wird es gruppiert
    - Analogie mit einem Interface in Java, in JS gelöst über die expliziten Modulexports / -imports (agiert als "Interfaceersatz")
  - Livecoding (3. Lektion) [00:00] - [21:45]
    - Mittels pageCSS im JS (als Konstante) den Style dynamisch halten & als Export angeben (geschlossene Variante - mehr Kontrolle)
    - Alternative Variante: in einem eigenen CSS-File definieren und dieses importieren (offenere Variante - mehr Flexibilität für Zusammenarbeit)
### Empfohlene Aktivitäten auf nächste Woche
- Review

### Vergebene Aufgaben
- UX/UI Gestaltungskonzept für Entwickler/Projektzuweisung (D. Lagger, M. de Laat)

---

## Woche 5 - Projector Pattern
**Datum/Uhrzeit:** 23.03.2021 - 12:15 bis 15:00

### Themen
- Heutiges [Goodie: Blurred gradient border](./week5/BackBlur.html) ([z-index](https://developer.mozilla.org/de/docs/Web/CSS/z-index), [linear-gradient()](https://developer.mozilla.org/de/docs/Web/CSS/linear-gradient()), [blur()](https://developer.mozilla.org/en-US/docs/Web/CSS/filter-function/blur()), [position](https://developer.mozilla.org/de/docs/Web/CSS/position))
  - Timestamps im Recording (1. Lektion): [4:30] - [31:30]
- Diskussion über den Modus der Punktevergabe
  - Begründung des derzeitigen Modus
  - Einführen von CSS-Goodie Aufgaben, welche Studenten bearbeiten (analog zu den anderen Vorträgen)
  - Timestamps im Recording (1. Lektion: [31:30] - [56:04])
- Präsentation der Aufgaben auf diese Woche
    - Tests für Master-Detail (O.Studer & R.von Arx)
        - Code ist in diesem Repo ([Siehe hier](./week5/person/personTest.js))
        - Timestamps im Recording (2. Lektion): Vorstellung [1:30] - [9:30], Fragen [9:30] - [19:00]
- Projector Pattern
  - Theorie (Problemstellung, Lösung, Nutzen) (Timestamps 3. Lektion: [23:00] - [46:00])
  - Livecoding innerhalb des Projekts (Timestamps 3. Lektion: [2:00] - [30:00])
### Empfohlene Aktivitäten auf nächste Woche
- Review

### Vergebene Aufgaben
- CSS-Goodie: Specificity (L.Kern)
- HTML-Table Projector (J.Hardorn & J.Kennedy)

---

## Woche 4 - Master Detail & spezialisierter Projektor
**Datum/Uhrzeit:** 16.03.2021 - 12:15 bis 15:00

### Themen
- Heutiges [Goodie: CSS Collapsible](./week4/Goodie-4-CSSCollapse.html) ([Custom-Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*), [display](https://developer.mozilla.org/de/docs/Web/CSS/display)/[visibility](https://developer.mozilla.org/de/docs/Web/CSS/visibility), [Sibling selector](https://developer.mozilla.org/de/docs/Web/CSS/Adjacent_sibling_combinator))
  - Timestamps im Recording(1. Lektion): [2:30] - [43:00]
- Präsentation der Aufgaben auf diese Woche
    - Kurzeinführung in JSDoc (L.Jacobs & R.Koch)
        - [Github Repo](https://github.com/leonievaynie/JSDoc) mit Präsentation und Beispielen
        - Timestamps im Recording (2. Lektion): Vorstellung [0:30] - [14:00], Fragen [14:00] - [29:30]
        - [Praxisbeispiel](https://github.com/mattwolf-corporation/ip6_lambda-calculus-in-js) - Projektarbeit mit einer guten Dokumentation
- Spezialisierter Projector für Person
  - Timestamps im Recording (3. Lektion gesamt)

### Empfohlene Aktivitäten auf nächste Woche
- Livecoding der 3. Lektion nachvollziehen (siehe Recording). Am besten einen Teil herauslöschen (Vorschlag: die mit "todo" markierten Stellen im Ausgangscode) und probieren, diese Teile selbst zu programmieren

### Vergebene Aufgaben
- Tests für Master-Detail vervollständigen (O.Studer & R.von Arx)

---

## Woche 3 - Attribute Projector
**Datum/Uhrzeit:** 09.03.2021 - 12:15 bis 15:00

### Themen
- Heutiges [Goodie: CSS Triangle](./week3/CSSTriangle.html) ([Border](https://developer.mozilla.org/de/docs/Web/CSS/border), [clip-path](https://developer.mozilla.org/de/docs/Web/CSS/clip-path), [Filter](https://developer.mozilla.org/de/docs/Web/CSS/filter), [box-shadow](https://developer.mozilla.org/de/docs/Web/CSS/box-shadow))
- Präsentation der Aufgaben auf diese Woche
    - Media Queries (J.Hadorn & J.Hänggi)
        - [Github Repo](https://github.com/Hazzeldorn/MediaQueriesSummary)
        - Timestamps im Recording (1. Lektion): Vorstellung [28:30] - [40:00], Fragen [40:00 - 1:02:30]
    - Master-Detail-View (L.Kern & R.Winkelmann)
        - [Github Repo](https://github.com/lukecore/webcl-fs21-2/tree/master-detail-view)
        - Timestamps im Recording (2. Lektion): Vorstellung [0:50] - [14:20]
- Attribute Projector
    - reichhaltige Attribute

### Empfohlene Aktivitäten auf nächste Woche
- Review von Attribute Projector

### Vergebene Aufgaben
- Kurzeinführung in JSDoc (L.Jacobs & R.Koch)

---

## Woche 2 - Validation, Conversion & Attribute
**Datum/Uhrzeit:** 02.03.2021 - 12:15 bis 15:00
### Themen
- Heutiges [Goodie: HTML/CSS Validierung](./week2/CSSValidation.html) eines Formulars ([Valid Pseudoklasse](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid), [Grid](https://developer.mozilla.org/de/docs/Web/CSS/CSS_Grid_Layout), [Values and Units](https://developer.mozilla.org/de/docs/Learn/CSS/Building_blocks/Values_and_units))
- Präsentation "Konvertierung und Validierung" (J.Christ, L.Dietiker)
- Nähere Betrachtung MVC
    - Mögliche Fallstricke (Falscher Dataflow, zu viele Abhängigkeiten)
    - Hierarchie MVC
- Einführung Attribute & LiveCoding Presentation-Model

### Empfohlene Aktivitäten auf nächste Woche
- Livecoding dieser Woche nochmals anschauen und nachvollziehen (Als Einstiegspunkt am besten View.html & Commit-History)

### Vergebene Aufgaben
- Master-Detail-View (L.Kern & R.Winkelmann)
- Media Queries (J.Hadorn & J.Hänggi)

---

## Woche 1 - Anschluss an WebPr finden
**Datum/Uhrzeit:** 23.02.2021 - 12:15 bis 15:00
### Themen
- Organisatorisches klären (Modulinhalt, Notengebung etc.)
- Wiedereinstieg von webpr anhand der Todo MVC-App (Onlineversion auf [*Github pages*](https://webengineering-fhnw.github.io/webcl-fs21-2/week1/todo/View.html)) mittels Codereading.

### Empfohlene Aktivitäten auf nächste Woche
- TodoMVC App durchgehen und verstehen (Vorschlag: Kommentare zum Verstandenen, Unklares und Fragen für nächste Woche notieren)
- Webpr-Kenntnisse im Allgemeinen auffrischen (u.a. Promises, Scheduler, [Arrow-Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) und weitere Konzepte, welche im Todo-Projekt verwendet werden)

### Vergebene Aufgaben
- Wie kann man Validation und Konvertierungen in die Todo-MVC App eingbauen (J.Christ, L.Dietiker)
- Protokoll / Readme nachführen (R.Bürkli)