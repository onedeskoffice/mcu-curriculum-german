# Abschnitt 4: Fortgeschrittener Bergbau

Ein weiteres nützliches Programm! Du kannst dieses Programm auf eine Wand richten und es gräbt einen zwei Blöcke hohen und einen Block breiten Tunnel. Außerdem platziert es alle 8 Blöcke Fackeln.

```
Tunnel bearbeiten
```

Wir werden dieses Programm mit **Funktionen** aufbauen. Funktionen benutzt man in komplexeren Programmen, damit man nicht den ganzen Code immer wieder in denselben Block eintippen muss. Stellen Sie sich eine Funktion als etwas vor, das eine Sache wirklich gut macht, und wenn Sie sie zusammenfügen, erledigen sie eine komplexe Aufgabe.

Die erste Funktion, die wir schreiben, prüft, ob die Schildkröte auf festem Boden steht, und wenn nicht, wird sie einen Block unter sich platzieren. Du definierst Funktionen wie diese.

```lua
Funktion placeFloorBlock()
  if not turtle.detectDown() then
    turtle.select(3)
    if turtle.placeDown() then
      return true
    end
    print("Platzierung des Bodens fehlgeschlagen")
    return false
  end
end
```

Jetzt kannst du `placeFloorBlock()` irgendwo anders in diesem Programm verwenden und es wird diesen Code ausführen.

Die nächste Funktion prüft, ob die Schildkröte noch Treibstoff hat. Wenn sie sieht, dass der Treibstoff knapp wird, wird sie versuchen, aus dem Inventarplatz 1 aufzutanken.

```lua
function fuel()
  if turtle.getFuelLevel() < 25 then
    turtle.select(1)
    if turtle.refuel(1) then
      return true
    end
    print("Refuelling Failed")
    return false
  end
end
```

Sie sehen, dass diese Funktion true zurückgibt, wenn das Tanken erfolgreich war, und false, wenn nicht.

Unsere nächste Funktion gräbt unseren Tunnel. Die Grundidee dieser while- und if-Schleife ist, dass die Schildkröte gräbt, wenn sie sich nicht vorwärts bewegt, und wenn sie nicht graben kann, greift sie an. Sie erkennt auch die Blöcke über ihr und gräbt auch diese.

```lua
function DigAndMove()
  while not turtle.forward() do
    if not turtle.dig() then
      turtle.attack()
    end
  end
  while turtle.detectUp() do
    turtle.digUp()
    sleep(0.5)
  end
  placeFloorBlock()
end
```

Diese Funktion dreht die Schildkröte um. Das sollte offensichtlich sein.

```lua
function turnAround()
  turtle.turnLeft()
  turtle.turnLeft()
end
```

Diese Funktion dreht die Schildkröte nach rechts, gräbt einen Block aus, prüft, ob der Block nicht zugeschüttet wurde, und legt dann eine Fackel in die Lücke. Wenn es ihr nicht gelingt, eine Fackel zu platzieren, gibt sie false zurück, andernfalls gibt sie true zurück.

```lua
function placeTorch()
  turtle.turnRight()
  turtle.dig()
  if not turtle.detect() then
    turtle.select(2)
    if turtle.place() then
      turtle.turnLeft()
      return true
    end
  end
  print("Place Torch Failed")
  turtle.turnLeft()
  return false
end
```

Hier setzen wir zwei Variablen, eine für die Länge, die du als Argument angibst, und eine, die im `moveBack` Abschnitt des Codes verwendet wird.

```lua
local tArgs = { ... }
local length = tonumber(tArgs[1])
local moveBack = 0
```

Der Teil `tArgs[1]` des obigen Codes ist ein **Argument**. Und ein Argument ist etwas, das Sie einem Programm geben, wenn Sie es ausführen. Wenn du ein Programm wie `go forward 10` ausführst, dann ist dein erstes Argument (`tArgs[1]`) `forward` und dein zweites Argument (`tArgs[2]`) ist `10`.

Jetzt fügen wir alles zusammen.

* Zuerst tanken wir die Schildkröte auf, indem wir `fuel()` aufrufen.
* Dann rufen wir `DigAndMove()` auf, um die Schildkröte einen Tunnelabschnitt vorwärts zu bewegen.
* Wir erhöhen die Variable `blocksMovedForward`, um zu verfolgen, wo wir uns befinden.
* Als nächstes prüfen wir, ob der Block, in dem wir uns befinden, ein Vielfaches von 8 ist.
* Wenn ja, rufen wir die Funktion `placeTorch()` auf.
* Am Ende drehen wir die Schildkröte um und gehen unsere Schritte zurück zum Anfang des Tunnels.

```lua
local blocksMovedForward = 0
while blocksMovedForward < length do
  fuel()
  DigAndMove()
  blocksMovedForward = blocksMovedForward + 1

  -- Add torch every 8 blocks
  if (blocksMovedForward % 8) == 0 then
    placeTorch()
  end

  if blocksMovedForward == length then
    turnAround()
    while moveBack < length do
      turtle.forward()
      sleep(1)
      print("Taking step: ")
      print(moveBack)
      moveBack = moveBack + 1
    end
  end
end
```

<img src="images/section_4/tunnel-inventory.png" style="width:25%">

Dies ist das Inventar der Schildkröte, das das Programm benötigt: Treibstoff in Slot 1, Fackeln in Slot 2 und Bodenblöcke in Slot 3.

Rufen Sie das Programm auf und übergeben Sie die Variable length:

```
tunnel 50
```

...gräbt einen Tunnel, der 50 Blöcke lang ist.

Wenn Sie Probleme mit dem obigen Programm haben, versuchen Sie, es mit dem folgenden Befehl von Pastebin zu kopieren:

```
pastebin get Taenfb85 pastedTunnel
```

Dadurch wird ein Programm namens _pastedTunnel_ erstellt, das den Code unter [https://pastebin.com/Taenfb85](https://pastebin.com/Taenfb85) verwendet (eine Kopie des Tunnelprogramms).

Vergleichen Sie das kopierte Programm mit Ihrem, um die Unterschiede festzustellen.

Dies war ein langer Weg, aber er ermöglicht es Ihnen, Diamanten viel einfacher zu finden. Versuchen Sie, bis zur Ebene 12 oder 13 zu graben und sechs Schildkröten, die dieses Programm ausführen, mit einem Abstand von 2 Blöcken dazwischen aufzustellen. Du wirst im Handumdrehen reich an Diamanten sein.
