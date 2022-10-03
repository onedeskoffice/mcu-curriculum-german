# Abschnitt 3: Bäume fällen

Von nun an wird der gesamte Code in diesem Buch nur noch als Text dargestellt, nicht mehr als Screenshot aus dem Spiel. Es ist immer noch derselbe Code, und er wird genauso funktionieren wie ein Bildschirmfoto.

Für diesen Abschnitt sollten wir eine andere sich wiederholende Aufgabe wählen, die wir oft erledigen müssen, und sie der Schildkröte übertragen. Nehmen wir das Häckseln von Bäumen! Das dauert eine Weile, und man kann immer mehr Holz gebrauchen.

Für dieses Programm brauchst du:

* Eine "Fortgeschrittene Bergbau-Schildkröte". (Bergbauschildkröten sind am vielseitigsten, da sie jeden Block zerbrechen können.)
* Einen Birkensprössling. Die Birke eignet sich am besten, weil sie immer gerade nach oben wächst und keine Äste hat.

Beginnen wir damit, unsere Gegenstände an den richtigen Stellen zu platzieren. Pflanze das Bäumchen in die Erde und sorge dafür, dass es auf allen Seiten genügend Platz zum Wachsen hat.

Vergiss nicht, deine Schildkröte zu beschriften, wenn du ein neues Programm erstellst. Benutze `label set treefarmer`.

<img src="images/section_3/treefarm.png" style="width:50%">

Fangen wir nun an, unser Programm zu schreiben. Du solltest deinen Code wieder in eine while-Schleife einbauen, da er immer laufen soll.

``lua
while true do

end
```

Überlege nun, was du tun musst, um einen Baum zu fällen. Zuerst musst du das Holz brechen, dann nach oben gehen (wobei du alle Blätter, die sich dir in den Weg stellen, zerbrichst) und dann wieder brechen. Sobald es keine Blöcke mehr zu fällen gibt, musst du wieder dorthin zurückgehen, wo du hergekommen bist, und deine Beute in eine Truhe legen.

Wenn du Programme wie dieses durchdenkst, bevor du sie schreibst, ist es einfacher, sie zu organisieren, und es ist wahrscheinlicher, dass dein Programm gleich beim ersten Versuch funktioniert.

Es gibt ein paar schicke Befehle, mit denen die Schildkröten sehen können, welche Art von Block vor ihnen liegt. Einer von ihnen ist `turtle.inspect()`. Wir werden diesen Befehl und eine **Variable** benutzen, um den Block vor der Schildkröte zu untersuchen. Eine Variable ist einfach ein Speicher für einige Daten. Wir können Variablen auf `true`, `false`, `elbow`, `1231241`, oder alles andere setzen, was uns einfällt.

`lua
while true do
  local erfolg, daten = turtle.inspect()
  print(daten.name)
end
```

Dieser Code setzt `success` auf `true` oder `false`, je nachdem ob er einen Block findet oder nicht. Er setzt auch `data` auf den gefundenen Block. Sie können dann `data.name` verwenden, um den Namen des Blocks als **String** zu erhalten.

Eine **Zeichenkette** ist eine Art von Daten in einem Programm. Man kann Strings, Zahlen und Boolesche Werte (die nur wahr oder falsch sind) in einem Programm haben.

Hier verwenden wir die Funktion `print()`, um den Namen auszudrucken. Wenn du diesen Code ausführst, während die Schildkröte vor einem Bäumchen steht, druckt er für immer `minecraft:sapling` aus. Sobald der Baum wächst, wird er stattdessen `minecraft:log` ausgeben.

Jetzt, wo wir wissen, auf welchen Block wir schauen, können wir anfangen, Bäume zu fällen. Stelle sicher, dass deine Schildkröte vorher aufgetankt wird!

```lua
while true do
  local success, data = turtle.inspect()
  print(data.name)
end
```


Obwohl unser Programm die ganze Zeit nach einem Element sucht, wird es nur dann etwas tun, wenn dieses Element ein `minecraft:log` ist. Wir haben dies mit einer **if/then-Anweisung** erreicht.

Eine "if/then"-Anweisung ist ähnlich wie eine "while"-Schleife, weil sie prüft, ob etwas wahr ist. Hier prüfen wir, ob das Element ein Log ist oder nicht. Wenn ja, wird der Code innerhalb der Anweisung ausgeführt, wenn nicht, wird der Code übersprungen. Der Code wird nur einmal ausgeführt, und dann wird das Programm fortgesetzt.

Wir fügen außerdem eine weitere while-Schleife in die if/then-Anweisung ein. Diese macht das Gleiche immer und immer wieder, bis keine Blöcke mehr vor der Schildkröte stehen.

Fügen wir nun den Code ein, um den Baum zu fällen.

```lua
while true do
  local success, data = turtle.inspect()
  if data.name == "minecraft:log" then
    while turtle.detect() do

    end
  end
end
```


Dieser Code hackt den Baum und bricht die Blätter ab, bis er die Spitze erreicht, und hält dann an. Danach müssen wir wieder nach unten gehen. Wir können das mit einer weiteren while-Schleife machen.

```lua
while true do
  local erfolg, daten = turtle.inspect()
  if data.name == "minecraft:log" then
    while turtle.detect() do
      turtle.dig()
      turtle.digUp()
      turtle.up()
    end
    while not turtle.detectDown() do
      turtle.down()
    end
  end
end
```

Jetzt sind wir wieder da, wo wir angefangen haben, und wir haben eine Reihe von Protokollen in unserem Inventar. Versuchen Sie, Ihr Programm auszuführen! Wenn Sie einen Fehler erhalten, suchen Sie nach der Zeilennummer in der Fehlermeldung und überprüfen Sie diese Zeile.

Vergessen Sie nicht, "Strg" + "t" gedrückt zu halten, um das Programm zu beenden.

Jetzt müssen wir nur noch eines tun: alle Protokolle löschen und auftanken. Wir können mit einigen der Logs, die wir gerade gesammelt haben, auftanken, so dass diese Schildkröte für immer ohne Eingreifen laufen kann. Wir sollten eine Truhe unter dem Startplatz der Schildkröte platzieren und die Schildkröte das Holz in die Truhe legen lassen. Du brauchst nur noch die Holzscheite aus der Truhe zu holen.



```lua
while true do
  local success, data = turtle.inspect()
  if data.name == "minecraft:log" then
    while turtle.detect() do
      turtle.dig()
      turtle.digUp()
      turtle.up()
    end
    while not turtle.detectDown() do
      turtle.down()
    end
    turtle.select(1)
    while turtle.getItemCount() > 2 do
      turtle.dropDown(1)
    end
    turtle.refuel()
  end
end
```


Es ist möglich, die Schildkröte auch Setzlinge pflanzen zu lassen, aber das erfordert viel mehr Code, und es macht mehr Spaß, das selbst herauszufinden. In der ComputerCraft-Befehlsreferenz findest du die Befehle, um das Inventar der Schildkröte nach Gegenständen zu durchsuchen.

**Juhu!** Das war dein zweites Programm, und dieses war viel komplexer. Jetzt hast du zwei langweilige und zeitraubende Dinge getan und Schildkröten gebaut, die sie für dich erledigen können!
