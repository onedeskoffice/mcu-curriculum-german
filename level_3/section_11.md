# Sortieren

Zu den Sortiervorrichtungen gehören NOT-Gatter, Komparatoren und die Ausnutzung der besonderen Eigenschaften von Trichtern.

![](images/appendices/appendix_7/sorter-first_circuit.png)

Hier ist ein Screenshot einer einfachen Sortierschaltung. Die Konfiguration der Trichter ist hier wichtig: Die untere Reihe der Trichter muss an den Truhen befestigt werden (Umschalt-Klick, um einen Trichter an einer Truhe zu befestigen) (und um zwei Truhen nebeneinander zu platzieren, wechseln Sie normale Truhen mit gefangenen Truhen ab) und die obere Reihe der Trichter muss an den Vergleichern befestigt werden (Umschalt-Klick, um einen Trichter an der **Seite** des Vergleichers zu befestigen). Hier machen wir uns eine besondere Eigenschaft der Komparatoren zunutze:

Wenn ein Komparator neben einem Container platziert wird, liefert er eine Ausgabe, die auf dem Prozentsatz des belegten Platzes im Container basiert. siehe [minecraft.gamepedia.com/Redstone_Comparator](http://minecraft.gamepedia.com/Redstone_Comparator)

Es gibt einige spezifische Mathematik auf den obigen Link, um zu bestimmen, wie der Komparator, um Ausgabe zu erhalten, aber mit dem Trichter ist es einfach genug, füllen Sie einfach den Trichter, bis Sie die Ausgabe auftreten sehen. In diesem Fall werden wir den Trichter so füllen, dass jeder zusätzliche Gegenstand das Redstone-Signal erzeugt, das wiederum den Trichter darunter mit Strom versorgt. Dabei wird auch eine besondere Eigenschaft von Trichtern ausgenutzt:

Wenn der Trichter mit Redstone betrieben wird, kann er keine Gegenstände aus dem Inventar der Blöcke direkt über ihm nehmen, keine Gegenstände in ein angeschlossenes Inventar legen oder Gegenstände aus der Umgebung aufsaugen. Ein Hopper unter ihm kann jedoch immer noch Gegenstände aus seinem Inventar nehmen und ein Hopper über oder neben ihm kann immer noch Gegenstände in ihn legen. siehe [minecraft.gamepedia.com/Hopper](http://minecraft.gamepedia.com/Hopper)

Baue genug von der Schaltung, um das Ausgangssignal des oberen Trichters zu testen. Lege einen einzelnen Gegenstand der Art, die du sortieren willst, in den ersten Schlitz des Trichters. Lege einen einzelnen Gegenstand, der nicht durch die Sortiermaschine kommen soll, in die restlichen Schlitze. Füllen Sie den **letzten** Schlitz, bis Sie ein Signal erhalten, und nehmen Sie dann einen Gegenstand heraus. Jetzt können nur noch diese beiden Gegenstände in den Trichter gelangen, und der Trichter darunter wird aus dem ersten Schlitz (dem Gegenstandstyp, den du sortieren willst) genommen, sobald ein weiterer Gegenstand im obersten Trichter landet.

Schauen Sie sich nun noch einmal den Screenshot oben an und vervollständigen Sie die Schaltung. Die Idee ist, das Signal vom oberen Trichter zum unteren Trichter zu senden. Dies könnte auf verschiedene Arten geschehen (andere Entwürfe betreiben klebrige Kolben mit Redstone-Blöcken), aber wir versuchen, die Größe unseres Sortierers auf ein Minimum zu beschränken. Die Konfiguration lautet: Komparator → zwei Blöcke mit Redstone-Staub → Redstone-Fackel. Dadurch entsteht ein NICHT-Gatter, die Fackel leuchtet so lange, wie kein Signal vom Komparator kommt. Dann zurück zum unteren Trichter mit einem Redstone-Staub und zwei Verstärkern. Solange der untere Teil der Schaltung mit Strom versorgt wird (es befinden sich nicht genügend Gegenstände im oberen Trichter, um den oberen Teil der Schaltung mit Strom zu versorgen), nimmt der untere Trichter keine Gegenstände aus dem Trichter darüber auf.

Sie können nun diesen Teil des Sortierers testen, indem Sie die sortierten Gegenstände in den Trichter legen. Sie sollten sofort in den unteren Trichter und dann in die Truhe fallen (mit einer Ausnahme - der einzige Nachteil dieses Designs ist, dass ein Gegenstand im unteren Trichter bleibt).

![](images/appendices/appendix_7/sorter-testing_hopper.png)

Nun wollen wir eine ähnliche Schaltung für den nächsten Artikel, den wir sortieren wollen, erstellen. Das Problem ist, dass die gleiche Schaltung, wenn wir sie bauen, die nächste stören würde. Also muss diese Schaltung ein wenig geändert werden. Sie geht einen weiteren Block nach unten, bringt das Signal zurück nach vorne und setzt das NOT-Gate unter den Trichter. Sehen Sie sich die Screenshots unten an und verwenden Sie das fertige Beispiel als Referenz, wenn Sie nicht weiterkommen. Beachten Sie, dass der Komparator auf einer Steinplatte sitzt.

![](images/appendices/appendix_7/sorter-second_circuit_one.png)

![](images/appendices/appendix_7/sorter-second_circuit_two.png)

## Fertigstellen

Vervollständigen Sie nun Ihre Sortiermaschine mit zwei wichtigen letzten Handgriffen:

1. Eine Möglichkeit, die Maschine zu beladen (siehe die Beispielkarte, wenn du Probleme hast, dir eine gute Lösung dafür auszudenken).
1. Eine "Auffangtruhe" für Gegenstände, für die es keine spezielle Truhe in der Maschine gibt.

Wenn du genug Zeit hast, kannst du deine Maschine auch größer machen (füge abwechselnde Reihen mit jedem Sortierkreislauf-Typ hinzu).
