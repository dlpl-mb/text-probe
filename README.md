7 Sekunden Spiel
Einführung @unplugged
Das Ziel dieses Spiels ist es, nach genau 7 Sekunden einen Knopf zu drücken !

Ein micro:bit mit Blick auf eine 7-Sekunden-Stoppuhr

Dieses Spiel ist vom Flipping Panckakes Spiel inspiriert .

Schritt 1
Der Player startet den Timer durch Drücken der Taste A . Fügen Sie den Code hinzu, um Code auszuführen, wenn ||input:button A is pressed||.

input.onButtonPressed(Button.A, function () {
	
})
Schritt 2
Wir müssen uns die Zeit merken, zu der die Taste gedrückt wurde, damit wir später die verstrichene Zeit berechnen können. Fügen Sie Code hinzu, um das ||input:running time||in einer ||variables:start||Variablen zu speichern .

let start = 0
input.onButtonPressed(Button.A, function () {
    // @highlight
    start = input.runningTime()
})
Schritt 3
Zeigen Sie etwas auf dem Bildschirm an, damit der Benutzer weiß, dass der Timer gestartet wurde...

let start = 0
input.onButtonPressed(Button.A, function () {
    start = input.runningTime()
    // @highlight
    basic.showIcon(IconNames.Chessboard)
})
Schritt 4
Der Player stoppt den Timer durch Drücken der Taste B . Fügen Sie den Code hinzu, um Code auszuführen, wenn ||input:button B is pressed||.

input.onButtonPressed(Button.B, function () {
	
})
Schritt 5
Berechne die verstrichene Zeit als ||input:running time|| ||math:minus|| ||variables:start||und speichere sie in einer neuen Variablen ||variables:elapsed||.

let start = 0
let elapsed = 0
input.onButtonPressed(Button.B, function () {
    // @highlight
    elapsed = input.runningTime() - start
})
Schritt 6
Berechnen Sie die ||variables:score||des Spiels , wie die ||math:absolute value||von der ||math:difference||der ||variables:elapsed||Zeit von 7 Sekunden, die 7000 Millisekunden.

let start = 0
let elapsed = 0
let score = 0
input.onButtonPressed(Button.B, function () {
    elapsed = input.runningTime() - start
    // @highlight
    score = Math.abs(elapsed - 7000)
})
Schritt 7
Zeigen Sie die Punktzahl auf dem Bildschirm an und Ihr Spiel ist fertig!

let start = 0
let elapsed = 0
let score = 0
input.onButtonPressed(Button.B, function () {
    elapsed = input.runningTime() - start
    score = Math.abs(elapsed - 7000)
    // @highlight
    basic.showNumber(score)
})


> Diese Seite bei [https://dlpl-mb.github.io/text-probe/](https://dlpl-mb.github.io/text-probe/) öffnen

## Als Erweiterung verwenden

Dieses Repository kann als **Erweiterung** in MakeCode hinzugefügt werden.

* öffne [https://makecode.microbit.org/](https://makecode.microbit.org/)
* klicke auf **Neues Projekt**
* klicke auf **Erweiterungen** unter dem Zahnrad-Menü
* nach **https://github.com/dlpl-mb/text-probe** suchen und importieren

## Dieses Projekt bearbeiten ![Build Status Abzeichen](https://github.com/dlpl-mb/text-probe/workflows/MakeCode/badge.svg)

Um dieses Repository in MakeCode zu bearbeiten.

* öffne [https://makecode.microbit.org/](https://makecode.microbit.org/)
* klicke auf **Importieren** und dann auf **Importiere URL**
* füge **https://github.com/dlpl-mb/text-probe** ein und klicke auf Importieren

## Blockvorschau

Dieses Bild zeigt den Blockcode vom letzten Commit im Master an.
Die Aktualisierung dieses Bildes kann einige Minuten dauern.

![Eine gerenderte Ansicht der Blöcke](https://github.com/dlpl-mb/text-probe/raw/master/.github/makecode/blocks.png)

#### Metadaten (verwendet für Suche, Rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
