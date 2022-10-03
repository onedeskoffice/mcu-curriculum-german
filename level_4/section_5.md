# Abschnitt 5: Der Raum

Schreiben wir ein Programm, um einen einfachen Raum zu bauen: `edit room`

Der erste Schritt besteht darin, die Argumente zu überprüfen, um sicherzustellen, dass sie so sind, wie du sie brauchst.

Dazu benutzen wir den Code `local tArgs = {...}`, der die Argumente in dein Programm lädt.

```lua
local tArgs = {...}

if #tArgs ~= 3 then
  print ("Usage: room <l> <w> <h>")
  return false
end
for i=1,3 do
  if tonumber(tArgs[i]) < 1 then
    print("Usage: room <l> <w> <h>")
    return false
  end
end
```

Dieser Codeblock nimmt Argumente entgegen und prüft, ob es 3 davon gibt und ob alle Zahlen größer als 1 sind.
Wenn dies nicht der Fall ist, wird eine Zeile ausgegeben, die dem Benutzer mitteilt, wie er das Programm ausführen soll.

Jetzt nehmen wir die drei Argumente und weisen sie den richtigen Variablen zu.

```lua
length = tArgs[1]
width = tArgs[2]
height = tArgs[3]
```


Und wir tanken die Schildkröte auf.

```lua
turtle.select(1)
turtle.refuel()

if turtle.getFuelLevel() < 150 then
  print("Fuel level too low.")
  return false
end
```
Hier wählen wir den ersten Slot und laden die Schildkröte mit Treibstoff aus diesem Slot.

Dieses Programm wird auch ein paar Funktionen haben. Dies ist unsere erste Funktion. Sie sucht nach Gegenständen, die in Slot 2 beginnen, dem Slot direkt nach dem Treibstoff-Slot. Beachte, dass sie nicht überprüft, ob es sich um platzierbare Gegenstände handelt, und dass sie dich nicht davon abhält, ein Haus aus Karotten zu bauen.

```lua
function findItems()
  local slot = 2
  while slot < 16 do
    if turtle.getItemCount(slot) < 1  then
      slot = slot + 1
    else
      turtle.select(slot)
      return true
    end
  end
  return false
end
```

Diese Funktion baut eine einzelne Reihe von Blöcken auf, indem sie eine for-Schleife verwendet, um sie zu stoppen, wenn sie die gewünschte Länge erreicht hat.

```lua
function buildRow(rowLen)
  for i = 1, rowLen, 1 do
    findItems()
    turtle.placeDown()
    turtle.forward()
  end
end
```

Diese Funktion ruft die Funktion `buildRow()` auf und verwendet dabei die Variablen, die wir zuvor festgelegt haben, um eine ganze Schicht des Hauses zu erstellen. Beachte, dass sie sich jedes Mal nach rechts dreht. Das bedeutet, dass Sie das Haus in der linken unteren Ecke beginnen müssen.

```lua
function buildLayer()
  turtle.up()
  buildRow(length)
  turtle.turnRight()
  buildRow(width)
  turtle.turnRight()
  buildRow(length)
  turtle.turnRight()
  buildRow(width)
  turtle.turnRight()
end
```

Nun, da wir nützliche Funktionen haben, die wir aufrufen können, können wir den Teil des Programms schreiben, der die Dinge erledigt!

```lua
for i=1, height, 1 do
  buildLayer()
end
```

Alles, was dies tut, ist, buildLayer() für die Anzahl der Schichten aufzurufen, die Sie mit `Höhe` angegeben haben

**Und wir sind fertig!** Füttere deine Schildkröte mit Kohle und einem Baumaterial und starte das Programm mit `Raum <Länge> <Breite> <Höhe>`

Jetzt bist du mit den wichtigsten Teilen von Level 4 fertig! Hoffentlich hast du eine gute Vorstellung davon, wie du in Zukunft deine eigenen Programme schreiben kannst. Wenn Sie Fragen haben, fragen Sie uns, und denken Sie daran, *das Wiki ist Ihr Freund*: [http://www.computercraft.info/wiki/Main_Page](http://www.computercraft.info/wiki/Main_Page)
