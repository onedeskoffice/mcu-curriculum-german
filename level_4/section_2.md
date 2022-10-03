# Abschnitt 2: Cobblestone Miner

Bis jetzt haben wir nur Befehle ausgeführt, die bereits in den Schildkröten und Computern eingebaut sind. Ab diesem Abschnitt werden wir einige eigene Programme schreiben, damit die Schildkröte das tut, was wir wollen.

Beginnen wir mit einem einfachen Programm, das dafür sorgt, dass dir nie wieder der Pflasterstein ausgeht. Wenn du schon einmal einen Pflasterstein-Generator benutzt hast, ist das hier ähnlich, nur dass die Schildkröte die Steine erntet und nicht du.

Baue zunächst einen Kopfsteinpflaster-Generator. Wenn du den Pflasterstein abbaust, wird er durch neue ersetzt, wenn er zerbricht. Jetzt müssen wir unsere Schildkröte so platzieren, dass sie das Kopfsteinpflaster für uns abbauen kann. Platziere deine Schildkröte mit Blick auf das Kopfsteinpflaster und stelle eine Truhe hinter sie. Vergewissere dich, dass du eine "Bergbauschildkröte" verwendest, und um deinen Code einfacher zu schreiben, verwende eine "fortgeschrittene Bergbauschildkröte".

<img src="images/section_2/cobblefarm1.png" style="width:50%">

Jetzt müssen wir das Label unserer Schildkröte setzen, so dass sie die Programme, die wir geschrieben haben, behält, wenn wir sie jemals kaputt machen. Tippe `label set cobblefarmer` und drücke `enter`:
<img src="images/section_2/cobblefarm2.png" style="width:50%">

Herzlichen Glückwunsch! Sie haben alle notwendigen Blockplatzierungen vorgenommen. Jetzt können wir anfangen, Code zu schreiben. Tippe `edit cobblefarm` und drücke `enter`. Dadurch wird das Bearbeitungsprogramm geöffnet und Sie können mit dem Schreiben Ihres eigenen Codes beginnen:
<img src="images/section_2/cobblefarm3.png" style="width:50%">

Das Editorprogramm sieht wie folgt aus:
<img src="images/section_2/cobblefarm4.png" style="width:50%">

Da Sie `edit cobblefarm` eingegeben haben, wird Ihr Programm beim Speichern `cobblefarm` heißen. Um das Menü `Speichern/Ausführen/Beenden` zu öffnen, drücken Sie `Steuerung` oder `Strg` auf Ihrer Tastatur. Der Text in der Ecke, auf dem "Ln 1" steht, ist der Zeilenzähler. Wenn Sie Code schreiben, wird er in Zeilen aufgeteilt, genau wie beim normalen Schreiben. Wann immer ein Fehler in Ihrem Code auftritt, wird Ihnen angezeigt, in welcher Zeile der Fehler auftritt, und genau dann ist dieser Zeilenzähler wirklich nützlich.

Fangen wir an, etwas Code zu schreiben! Beginnen Sie mit dem Kopieren des unten stehenden Codes. Dies ist eine sogenannte while-Schleife. Der "while"-Befehl prüft, ob etwas wahr oder falsch ist, und führt dann den Code weiter aus, wenn es wahr ist. Der "do"-Teil teilt dem Computer mit, dass du mit der Definition der Schleife fertig bist und dass du möchtest, dass er den Code ausführt. Am Ende jeder Schleife, die du schreibst, musst du den Code "end" einfügen. Damit wird dem Programm mitgeteilt, dass der Codeabschnitt der Schleife beendet werden soll.

Da wir `while true do` geschrieben haben, wird der Code für immer laufen, weil die Anweisung `true` für sich genommen immer `true` und nicht `false` sein wird.

`lua
while true do

end
```

<img src="images/section_2/cobblefarm5.png" style="width:50%">

Als nächstes füllen wir unsere Schleife mit etwas Code. Alles, was wir für dieses Programm brauchen, sind zwei Befehle. Kopieren Sie den Code wie unten gezeigt. Der Befehl `turtle.dig()` weist die Schildkröte an, den Block vor ihr abzubauen. Sobald sie den Block abbaut, hat sie ihn in ihrem Inventar. Der zweite Befehl ist, den Pflasterstein in eine Truhe zu legen, und es sieht so aus, als hätten wir einen Fehler gemacht! Es gibt Befehle für `turtle.drop()`, `turtle.dropUp()`, und `turtle.dropDown()`, aber nichts für `turtle.dropBack()`. Stattdessen werden wir jetzt einfach `turtle.dropUp()` verwenden.

<img src="images/section_2/cobblefarm6.png" style="width:50%">

Wenn du deine zwei Zeilen Code geschrieben hast, drücke "Strg" oder "Ctrl" auf deiner Tastatur, um das Menü zu öffnen, und drücke dann "Enter", um dein Programm zu speichern. Jetzt drückst du wieder "Strg", drückst die "rechte Pfeiltaste", um auf "Beenden" zu gehen, und drückst dann "Enter", um das Editorprogramm zu schließen.

Tippe `cobblefarm` und drücke `enter`. Damit wird dein Programm gestartet! Wenn du `escape` drückst, wirst du sehen, dass deine Schildkröte Pflastersteine für dich sammelt.

Um das Kopfsteinpflaster in die Truhe zu legen, musst du die Schildkröte umdrehen und den Befehl `drop` verwenden, um das Kopfsteinpflaster in die Truhe zu legen. Ändere dein Programm wie folgt:

```lua
while true do
  turtle.dig()
  turtle.turnLeft()
  turtle.turnLeft()
  turtle.drop()
  turtle.turnLeft()
  turtle.turnLeft()
end
```

*Vergessen Sie nicht zu speichern!

<img src="images/section_2/cobblefarm7.png" style="width:50%">

Wenn die Truhe voll ist, kannst du deine Schildkröte wieder öffnen und gleichzeitig `control` und `t` gedrückt halten, um dein Programm zu beenden.

**Glückwunsch!** Du hast gerade dein erstes einfaches Programm in ComputerCraft geschrieben. In den nächsten Abschnitten werden wir mehr nützliche und komplexere Programme schreiben.
