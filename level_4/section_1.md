# Abschnitt 1: ComputerCraft-Grundlagen

## Einführung

[ComputerCraft] (http://www.computercraft.info/) ist eine Modifikation für Minecraft, bei der sich alles um Computerprogrammierung dreht. Sie ermöglicht es dir, im Spiel Computer und Schildkröten zu bauen und mit der Programmiersprache Lua Programme für sie zu schreiben. Die Erweiterung von Minecraft um die Programmierung eröffnet eine Vielzahl neuer Möglichkeiten für Automatisierung und Kreativität. Wenn du noch nie programmiert hast, ist dies eine hervorragende Möglichkeit, eine Fähigkeit aus der realen Welt in einer unterhaltsamen, vertrauten Umgebung zu erlernen.

Dies wird deine erste Erfahrung mit der ComputerCraft-Mod sein und für einige von euch ist es das erste Mal, dass ihr eine Befehlszeilenschnittstelle benutzt. Mit diesem Wissen können Sie andere Kommandozeilensoftware verwenden, und Sie erhalten eine solide Grundlage für einfache Programmierkenntnisse.

### Installation von ComputerCraft

ComputerCraft kann von [http://www.computercraft.info/download/](http://www.computercraft.info/download/) heruntergeladen werden und benötigt Forge. Der einfachste Weg, Forge und ComputerCraft zu installieren, ist die Verwendung von MultiMC von [https://multimc.org/](https://multimc.org/). Erstelle eine neue Instanz in MultiMC für Minecraft Version `1.8.9`, die neueste Version von Minecraft, die von ComputerCraft unterstützt wird. Klicke rechts auf "Instanz bearbeiten" und dann auf "Forge installieren" auf der Registerkarte _Version_:
<img src="images/section_1/install-version.png" style="width:50%">

Ziehen Sie dann die Datei `ComputerCraft1.79.jar`, die Sie von computercraft.info heruntergeladen haben, in das Fenster unter dem Reiter "Loader Mods":
<img src="images/section_1/install-loader-mods.png" style="width:50%">

<!-- BREAK -->
### Die Kommandozeile

* Öffnen Sie die ComputerCraft-Welt.
* Öffnen Sie Ihr Inventar und suchen Sie nach "Computer".
* Platziere einen _Advanced Computer_ (den gelben) auf dem Boden und klicke mit der rechten Maustaste darauf.

<img src="images/section_1/advanced-computer.png" style="width:50%">

Wenn du einen Computer platzierst und mit der rechten Maustaste darauf klickst, siehst du als Erstes das hier:
<img src="images/section_1/ccb1.png" style="width:50%">

Dies ist eine Befehlszeile. Hier können wir Wörter eingeben, um Programme auszuführen, und wir können in Ordnern nachsehen, genau wie auf einem echten Computer. Das wollen wir jetzt tun.

* Der Befehl `ls` listet den Inhalt des aktuellen Ordners (auch Verzeichnis genannt) auf.
* Der Befehl "cd" wechselt Ordner (Verzeichnisse).

Gehe wie folgt vor:

* Tippe `cd rom`
* Tippen Sie `cd programs`.
* Tippen Sie `ls`. Dies wird alle Programme im Verzeichnis _programs_ auflisten

<img src="images/section_1/ccb2.png" style="width:50%">

Als nächstes führen wir das Programm `edit` aus und sehen uns an, wie es aussieht.
Gib `edit time` ein.

<img src="images/section_1/ccb3.png" style="width:50%">

Dies ist das Programm, mit dem Sie Ihre Programme bearbeiten können. Das Programm `edit` ist alles, was Sie brauchen, um Ihren eigenen Code in ComputerCraft zu schreiben.

Beende das `edit` Programm, indem du `ctrl` (control) drückst, mit den Pfeiltasten exit auswählst und dann `enter` drückst.

### Spielen Sie das Textabenteuer Minecraft auf einem ComputerCraft-Computer.

* Tippe "adventure" ein und drücke "enter".
* Einige der Befehle, die im Adventure-Programm verfügbar sind:
  * `punch`
  * `Aufnehmen` oder `Greifen`
  * `Basteln` oder `Herstellen`
  * `go`
  * `Essen`
  * `inventory`
  * ♪ `look`
  * `Hilfe`

<img src="images/section_1/adventure.png" style="width:50%">

Falls du es noch nicht bemerkt hast: Adventure ist eigentlich nur ein textbasiertes Minecraft. Du spielst Minecraft auf einem Computer innerhalb von Minecraft.

### Peripheriegeräte

Peripheriegeräte sind Blöcke, die du neben den Computer stellst. Dann kannst du Programme auf dem Computer verwenden, um mit diesen Peripheriegeräten zu "sprechen".

#### Benutze ein Laufwerk

Öffne dein Inventar und suche nach _Disk_. Wähle das _Diskettenlaufwerk_ und lege es neben deinen Computer.

<img src="images/section_1/disk-drive.png" style="width:50%">

Legen Sie eine beliebige Musikdiskette in das Laufwerk. Klicken Sie dann wieder mit der rechten Maustaste auf Ihren Computer und starten Sie das Programm _dj_, indem Sie einfach `dj` eingeben. Es spielt die Musikdiskette, die sich im Laufwerk befindet, genau wie ein Jukebox-Block.

#### Erstelle einen Monitor

* Öffne dein Inventar und suche nach `Monitor`.
* Platziere 12 Monitore in einem Raster von 4 x 2 hoch, um einen riesigen Breitbildmonitor zu erstellen.
* Platziere einen Computer neben dem Monitor, auf der linken Seite.
  * Es ist wichtig, auf welcher Seite der Monitor steht, also sieh nach!

#### Ein Bild malen

* Klicken Sie mit der rechten Maustaste auf den Computer, um ihn zu öffnen, und geben Sie dann "Monitor rechts malen mein Bild" ein.
* Drücken Sie die Escape-Taste, um den Computer zu schließen, und schauen Sie dann auf den Monitor.

<img src="images/section_1/paint.png" style="width:50%">

Auf dem Bildschirm sollten Sie etwas sehen, das wie eine Leinwand aussieht. Versuchen Sie, mit der rechten Maustaste auf die Leinwand zu klicken, um zu malen. Klicken Sie mit der rechten Maustaste auf eine Farbe, um diese Farbe auszuwählen. Wenn Sie fertig sind, öffnen Sie den Computer erneut und drücken Sie "Strg" und dann "Enter". Dadurch wird das Bild in einer Datei mit dem Namen `mypainting` gespeichert.

* Um ein laufendes Programm zu beenden, ohne zu speichern, halten Sie `ctrl + t` gedrückt.

* Um den Computer neu zu starten, halten Sie `ctrl + r` gedrückt.

<!-- BREAK -->
## Schildkröten

<img src="images/section_1/Turtles.png" style="width:25%">

Schildkröten sind programmierbare Roboter, die du zum Sammeln von Ressourcen, zum Räumen von Gelände und für andere Aufgaben einsetzen kannst. Auf ihnen läuft ein Betriebssystem namens turtleOS, und die Programme, die sie ausführen, können auf dem internen Speicher oder auf Disketten gespeichert werden.  Es gibt Farming-, Mining-, Crafting- und Melee-Turtles. Sie werden nach dem Diamant-Werkzeug* eingeteilt, mit dem du sie ausrüstest.

Hinweis: Werkzeuge, mit denen Schildkröten ausgerüstet sind, nutzen sich nicht ab, und Schildkröten selbst sind unzerstörbar (es sei denn, du machst sie selbst kaputt).  Das macht sie zu einer der sichersten Arten, Diamantwerkzeuge zu verwenden, ganz zu schweigen von der Zeit, die sie dir sparen.

Wie jeder Roboter benötigen auch Schildkröten Treibstoff.  Sie können Energie aus allem beziehen, was in einem Ofen funktioniert, sowie aus anderen fortschrittlicheren Optionen, zu denen wir später noch kommen werden.  Verschiedene Arten von Treibstoff ergeben unterschiedliche _Brennstoffzahlen_, d.h. die Anzahl der Blöcke, die die Schildkröte mit dieser Menge Treibstoff bewegen kann.  Zum Beispiel gibt Kohle der Schildkröte 80 Treibstoff, also kann die Schildkröte 80 Blöcke bewegen.

### Tanzende Schildkröten

1. Öffne dein Inventar und suche nach "Schildkröte".
1. Lege eine oder zwei Schildkröten auf den Boden
1. Rechtsklick auf die Schildkröte
1. Führe das Programm `dance` aus

## Bewege sie

Schildkröten haben mehrere Standardprogramme, darunter das Programm "go".

1. Wähle eine Schildkröte und lege eine _Kohle_ in ihr Inventar.
2. Gib "Treibstoff" ein.
  1. Es wird angezeigt: _Treibstoffstand ist 80_.
3. Tippe _Vorwärts 10_ und sieh zu, wie es läuft!
  1. Tippe "Treibstoff" und bemerke, dass der Treibstoffstand jetzt 70 ist.
  2. Immer wenn die Schildkröte keinen Treibstoff im Inventar hat, kannst du "refuel" eingeben, um den Treibstoffstand zu überprüfen.

Das "go"-Programm hat das folgende Format:
Gehe <Richtung> <Entfernung>".

Hinweis: Für schnelles/Massentanken gibst du "refuel all" ein.

## Eingebaute Schildkrötenprogramme verwenden

### Tunnel

`tunnel` ist ein eingebautes Tunnelbau-Programm. 

`Tunnel <Länge>`

Achte darauf, dass deine Schildkröte genügend Treibstoff in Slot 1 hat! Die Schildkröte wird auch keine Fackeln platzieren, so dass der Tunnel sehr dunkel sein wird! Die Schildkröte kehrt auch nicht zu dir zurück, du musst sie also am Ende des Tunnels abholen.

### Ausgraben

`excavate` ist ein eingebautes Grabungsprogramm. Es gräbt ein Viereck gerade nach unten, bis es auf Grundgestein trifft. Es legt das, was es ausgräbt, in einer Truhe ab, die sich hinter dem Startpunkt befindet.

Ausgraben <Breite>

Achte darauf, dass deine Schildkröte genügend Treibstoff in Slot 1 hat! Die Schildkröte kehrt *zu* ihrem Startpunkt zurück. Dieses Programm hinterlässt riesige Löcher im Boden, die dich töten werden, wenn du hineinfällst. Aber sie sind praktisch für den schnellen Abstieg zu seltenen Erzebenen und zum Sammeln von Rohstoffen:
<img src="images/section_1/excavate.png" style="width:50%">

## Crafting-Schildkröten

Computer und Schildkröten, insbesondere die nützlichen, mit Werkzeugen ausgestatteten Schildkröten, sind recht teuer.

Hier ist das fortgeschrittene Computerrezept:

<img src="images/section_1/craft-advanced-computer.png" style="width:50%">

Hier ist das Schildkrötenrezept:

<img src="images/section_1/craft-turtle.png" style="width:50%">

Um eine Schildkröte auszurüsten, musst du sie mit einem brandneuen Diamantwerkzeug herstellen:

<img src="images/section_1/craft-mining-turtle.png" style="width:50%">
