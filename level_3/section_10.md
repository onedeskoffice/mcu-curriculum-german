# Kommando-Blöcke

> Ein Befehlsblock ist eine Redstone-Komponente, die bei Aktivierung Befehle ausführen kann. Er kann im Survival-Modus nicht legal erworben werden und wird hauptsächlich auf Multiplayer-Servern und in benutzerdefinierten Karten verwendet.

## Üben Sie die grundlegenden Befehle, die für Befehlsblöcke verfügbar sind.

Erstellen Sie eine neue kreative Welt.

Um einen Befehlsblock zu erhalten, gib den Befehl "/Gebe <Spielername> Befehlsblock" ein.

Platziere den Befehlsblock und klicke ihn mit der rechten Maustaste an. Gib nun den Befehl `/give` in den Befehlsblock ein. Dies gibt dem nächsten Spieler eine Eisenspitzhacke, zum Beispiel:

`/give @p iron_pickaxe`

Klicken Sie auf "Fertig" und setzen Sie dann eine Schaltfläche auf den Befehlsblock, indem Sie die Schaltfläche gedrückt halten und mit der Umschalttaste auf den Befehlsblock klicken. (Ein Befehlsblock führt Befehle aus, wenn er durch Redstone-Power aktiviert wird.) Aktiviere dann den Befehlsblock, indem du mit der rechten Maustaste auf die Schaltfläche klickst. Du erhältst eine eiserne Spitzhacke.

## Befehlsblock-Referenz

Einige der anderen nützlichen Befehle für die Verwendung in Befehlsblöcken sind:

* `say`, `tell`, `msg` und `w` (whisper), um Nachrichten an einen oder mehrere Spieler zu übermitteln.
  `Sagen <Spieler> <Nachricht>`
* `clear <player> [item] [data] [maxCount] [dataTag]` löscht das Inventar eines Spielers, oder nur die in den Argumenten angegebenen Gegenstände
* `effect <player> <effect> [seconds] [amplifier] [hideParticles]` gibt dem anvisierten Spieler oder der Entität den angegebenen Effekt für die angegebene Zeit (Standard ist 30 Sekunden). Es gibt auch `effect <player> clear`
* `Spielmodus <Modus> [Spieler]`
* `Sound <Sound> <Spieler> [x] [y] [z] [Lautstärke] [Tonhöhe] [Mindestlautstärke]`
* `setblock <x> <y> <z> <Kachelname> [dataValue]`
* `summon <Einheitsname> [x] [y] [z]`
* `testfor <Spieler> [dataTag]`
* `Zeit setzen <Wert>`
* `toggledownfall`
* `tp [Zielspieler] <Zielspieler>` oder `tp [Zielspieler] <x> <y> <z>`
* `Wetter <klar|Regen|Gewitter> [Dauer in Sekunden]`
* `xp <Betrag> [Spieler]`

Alle in Chevrons eingeschlossenen Parameter (wie z.B. `<Betrag>`) sind erforderlich, während alle in Klammern eingeschlossenen Parameter (wie z.B. `[Lautstärke]`) optional sind.

## Kommunikation mit einem Spieler mit Befehlsblöcken

In dieser Übung werden wir Befehlsblöcke verwenden, um einen Spieler vor einem drohenden Unheil zu warnen.

Es gibt einige verschiedene Arten von Befehlsblöcken:

* ein Befehlsblock ("Impulse") wird versuchen, seinen Befehl einmal auszuführen
* ein Ketten-Befehlsblock ("Chain") versucht erst dann, seinen Befehl auszuführen, wenn ein anderer Befehlsblock vor ihm seinen eigenen Befehl ausführt
* ein Wiederholungs-Befehlsblock ("Repeat") versucht, seinen Befehl bei jedem Spieltick auszuführen, bis er nicht mehr aktiviert wird

Der erste Block verwendet einen `testfor`-Befehl, der dann einen `say`-Block aktiviert, wenn ein Spieler einen bestimmten Radius betritt:

![](images/appendices/appendix_6/chain-impulse-command-blocks.png)

![](images/anhaenge/anhang_6/kette-kommando-block-0.png)

![](images/anhaenge/anhang_6/kette-befehl-block.png)

## Bewegen eines Spielers auf einer Karte mit Befehlsblöcken

Schauen wir uns nun an, wie man ein einfaches Sicherheitssystem für sein Haus mit Hilfe eines Befehlsblocks und einer Druckplatte bauen kann.

* Platziere zunächst eine Druckplatte vor deiner Tür.
* Achten Sie darauf, dass der Spieler auf die Platte tritt, wenn er zur Tür geht.
* Platziere nun einen Befehlsblock unter der Druckplatte, so dass er aktiviert wird, wenn auf die Platte getreten wird.

![](images/appendices/appendix_6/teleport-door-setup.png)

* Nun gehst du zum Befehlsblock und gibst `/tp @p[r=<radius>,name=!<yourname>] <x> <y> <z>` ein.

![](images/appendices/appendix_6/teleport-door-command.png)

Wenn wir diesen Befehl aufschlüsseln, haben wir `/tp`, das ist der Befehl zum Teleportieren von Spielern. Dann haben wir den Spezifizierer `@p`, der besagt, dass dieser Befehlsblock auf Spieler wirkt. Der `@p`-Befehl benötigt Argumente, `r=` für den Radius und `name=` für die Spieler, die teleportiert werden sollen. Die Einstellung des Radius ist einfach. Das Setzen des Namens ist jedoch ein wenig interessant. Hier verwenden wir die Operation `!`, was `NICHT` bedeutet. Genau wie in Redstone wird damit die Ausgabe eines Befehls invertiert. Im Moment benutzen wir sie, um sicherzustellen, dass jeder Spieler, der `NICHT` du bist, teleportiert wird, während du sicher bleibst. Der letzte Teil des Befehls ist der Ort, an den teleportiert werden soll, den ihr anstelle von "<x> <y> <z>" in den Befehl einfügt. Die Tilda `~` wird verwendet, um die aktuelle Position des Spielers zu repräsentieren; das Teleportieren nach `~ ~ ~` würde den Spieler überhaupt nicht bewegen! Wir können auch eine Zahl zur Tilda addieren oder subtrahieren, z.B. `~ ~ ~-2`, um den Spieler 2 Blöcke zurück zu bewegen.

Hier ist ein Aufbau mit einer Redstone-Schaltung, also keine Druckplatte erforderlich!

![](images/appendices/appendix_6/teleport-door-with-circuit.png)

Hier ist der letzte Befehl, der sicherstellt, dass ein Benutzer vorbeikommt:

![](images/appendices/appendix_6/teleport-door-with-not-name.png)

## Einem Spieler Gegenstände mit Befehlsblöcken geben

Der Befehl `/give` ist einer der vielseitigeren Befehle, die in Befehlsblöcken verwendet werden können. In diesem Abschnitt werden wir ein paar gute Anwendungen auflisten.

# Befehlsblock "Spawner"

In diesem Abschnitt werden wir zwei Befehlsblöcke verwenden, die einen benutzerdefinierten Mob-Spawner erzeugen, sobald sich ein Spieler in einer bestimmten Entfernung von der Vorrichtung befindet.

Er ist den anderen Befehlsschaltungen, die wir bereits gebaut haben, sehr ähnlich, mit der Ausnahme, dass er nicht einfach `/say` verwendet oder alle Spieler in der Nähe teleportiert, sondern bedingt Zombies spawnen lässt, wenn Spieler in der Nähe sind.

Der erste Schritt besteht darin, eine einfache Uhrenschaltung zu erstellen, die den Befehlsblock mit Strom versorgt und erkennt, wenn sich ein Spieler in einem bestimmten Radius befindet.

Der erste Befehlsblock verwendet den `testfor`-Befehl, um auf einen Spieler innerhalb von _N_ Blöcken zu testen. Es ist ein normaler Befehlsblock mit den Standardeinstellungen, wie wir sie zuvor verwendet haben.

Der nächste Befehlsblock wird zwei besondere Eigenschaften haben. Die erste ist, dass er ein Befehlsblock vom Typ _chain_ sein wird. Er wird erst ausgeführt, wenn der Block "testfor" ausgeführt wird. Die zweite besondere Eigenschaft ist, dass es sich um einen _bedingten_ Befehlsblock handelt. Ein Befehlsblock im bedingten Modus führt seinen Befehl erst aus, wenn der Befehlsblock hinter ihm erfolgreich ausgeführt wurde. Dieser Block wird also erst dann ausgeführt, wenn der `testfor`-Block erfolgreich ausgeführt wurde (er findet einen Spieler innerhalb seines definierten Radius).

Dieser `/summon`-Befehl wird Zombies mit dem Namen "Braaaaains" erzeugen, die Lederkappen tragen (damit sie tagsüber nicht verbrennen).

`/summon minecraft:zombie ~ ~1 ~ {CustomName:Braaaaains,CustomNameVisible:1,ArmorItems:[{},{},{},{},{id: "minecraft:leather_helmet",Count:1}]}`

![](images/anhaenge/anhang_6/spawner.png)

![](images/anhaenge/anhang_6/spawner-testfor.png)

![](images/anhaenge/anhang_6/spawner-summon-conditional.png)

## Spawner Upgrades Herausforderung

Sobald du einen funktionierenden Spawner hast, versuche, diese Upgrades herauszufinden:

1. Spawn mehr als ein Mob auf einmal, in verschiedenen Bereichen um den Spawner.
1. Füge einen Schalter hinzu, um den Spawner ein- und auszuschalten, indem du den ersten Uhrenkreis zu einer schaltbaren Schleife machst.

# Automatische Brücke

In diesem Abschnitt werden wir einen kleinen Prototyp einer automatischen Einwegbrücke bauen.

Der Aufbau unseres automatischen Brückenkonzepts (images/appendices/appendix_6/bridge-redstone_complete.png)

Die Konstruktion besteht aus vier Befehlsblöcken, um die Brücke zu erstellen, und vier Befehlsblöcken, um diese Blöcke nach der Überquerung wieder in die Luft zu bringen. Wir verwenden den Befehl `setblock` mit relativen Positionen, so dass die folgenden Beispiele darauf beruhen, dass die Befehlsblöcke in genau der gleichen relativen Position zur Brücke stehen. Du musst das aber nicht tun - du kannst einfach die relativen Koordinaten auf der Grundlage der Platzierung deiner Befehlsblöcke anpassen.

![Setblock-Befehl zum Platzieren der Brückensteine](images/appendices/appendix_6/bridge-setblock_stone.png)

![Setblock-Befehl, um die Brückensteine durch Luft zu ersetzen.](images/appendices/appendix_6/bridge-setblock_air.png)

Du kannst deine Befehlsblöcke testen, indem du eine Schaltfläche auf ihnen platzierst (Umschalt-Klick, um eine Schaltfläche auf einem Befehlsblock zu platzieren). Sobald du die "setblock"-Befehle eingestellt hast und sie korrekt funktionieren, verbinde deine Befehlsblöcke mit den Druckplatten über Redstone-Staub, wie im ersten Screenshot oben gezeigt. Verstecken Sie nun Ihre Befehlsblöcke und den Redstone!

Nicht betreten!](images/appendices/appendix_6/bridge-do_not_enter.png)

## Mach es besser

Der obige Build ist eher ein Proof-of-Concept. Es ist ziemlich leicht zu erkennen, dass die Druckplatten die Brücke auslösen, und außerdem ist sie nicht besonders abschreckend. Eine Verbesserung wäre, einen Detektorblock zu verwenden, um festzustellen, wann sich ein Spieler von einer Seite nähert und die Brückenblöcke oder die Luft entsprechend zu platzieren. Verwenden Sie die Techniken unserer "Spawner"-Vorrichtung, um eine Uhr zu erstellen, die einen "Testfor"-Befehlsblock antreibt.

Redstone-Brücke mit Detektorblock statt Druckplatten](images/appendices/appendix_6/bridge-with_detector_block.png)

![Testfor-Befehl. Deine Koordinaten werden anders sein! (Oder du könntest einfach einen großen Radius nehmen)](images/appendices/appendix_6/bridge-testfor_block.png)

Teste nun den Befehl `testfor` nur für deinen Spieler. Du könntest es sogar zu einer Fallenbrücke machen, die nur dich passieren lässt und die Blöcke in Luft verwandelt, wenn ein anderer Spieler versucht, sie zu überqueren.

## Referenzen

* [minecraftcommand.science](https://minecraftcommand.science/) -- "Mehrere minecraft vanilla JSON-Generatoren für all deine `/give` und `/summon` Bedürfnisse."
* Minecraft Mobspawner und Beschwörungsgenerator: [http://minecraft.tools/en/spawn.php](http://minecraft.tools/en/spawn.php)
* Minecraft-Wiki-Befehlsreferenz: [http://minecraft.gamepedia.com/Commands](http://minecraft.gamepedia.com/Commands)
