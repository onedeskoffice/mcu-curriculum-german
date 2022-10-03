## Feuerwerk-Abschussvorrichtungen

Die Herstellung von Feuerwerkskörpern ist nicht nur eine lustige Art, Redstone-Schaltkreise zu verwenden, sondern auch notwendig, um ein großes Feuerwerk zu veranstalten! Wir starten Feuerwerkskörper mit Hilfe von Dispensern (nach oben gerichtet) und einem pulsierenden Redstone-Signal.

![](images/appendices/appendix_5/a5_dispenser.png)

Um unser Feuerwerk zu basteln, brauchen wir zwei Komponenten. Einen Feuerwerksstern und eine Feuerwerksrakete. Der Feuerwerksstern wird verwendet, um die Eigenschaften der Explosion anzupassen. Zur Herstellung eines Feuerwerkssterns werden ein Schießpulver und mindestens ein Farbstoff benötigt. Die verbleibenden Plätze in der Basteltabelle können verwendet werden, um mehrfarbige Feuerwerkskörper mit mehreren Farbstoffen oder Feuerwerkskörper mit Spezialeffekten mit Gegenständen wie Diamanten und Federn herzustellen.

![](images/appendices/appendix_5/a5_crafting_fireworks_star.png)

Als Nächstes basteln wir die Feuerwerksrakete, indem wir mindestens ein Schießpulver, Papier und einen Feuerwerksstern verwenden. Du kannst bis zu drei Schießpulverartikel hinzufügen, um die Flugdauer zu verlängern. Du kannst sogar zusätzliche Feuerwerkssterne in dieselbe Rakete stecken.

![](images/appendices/appendix_5/a5_basteln_feuerwerk_rakete.png)

Das sind die Grundlagen für die Herstellung von Feuerwerkskörpern. So sieht unser Beispielfeuerwerk aus.

![](images/anhänge/anhang_5/a5_testing_crafted_firework.png)

Tipp: Um das Feuerwerk besser sehen zu können, sollte man die Nacht mit dem Befehl `/time set 16000` einstellen.

## Launcher Arrays

Nun können wir mit der Erstellung unseres Feuerwerks fortfahren. Wir beginnen mit der Erstellung eines einfachen Feuerwerk-Arrays.

1. Wir beginnen damit, dass wir drei Dispenser auf dem Boden platzieren und zwei Redstone Dusts hinter den Dispensern platzieren. Die Dispenser sind jeweils zwei Blöcke voneinander entfernt, wobei der mittlere Dispenser zusätzlich zwei Blöcke hinter den beiden vorderen platziert wird.
![](images/anhänge/anhang_5/a5_launcher_array1_building1.png)

2. Platzieren Sie einen roten Steinwiederholer vor dem mittleren Spender und einen weiteren Wiederholer einen Block weiter seitlich, wie im Bild unten gezeigt. Stellen Sie die Repeater auf jeweils zwei Ticks ein. Dann können Sie die Redstone-Verkabelung in einer Linie anschließen, um sie zu verbinden.
![](images/appendices/appendix_5/a5_launcher_array1_building2.png)

3. Nun kannst du den dritten Repeater wieder auf zwei Ticks einstellen und den roten Steinstaub wie unten gezeigt verbinden.
![](images/anhaenge/anhang_5/a5_launcher_array1_building3.png)

4. Schließe den Redstone an den in Schritt 2 platzierten Repeater an und füge einen Hebel hinter dem mittleren Spender hinzu.
![](images/anhaenge/anhang_5/a5_launcher_array1_completed.png)

Das war's! Starten Sie die Uhr des Launcher-Arrays, indem Sie den Hebel schnell ein- und ausklappen.

![](images/appendices/appendix_5/fireworks.png)

Du kannst gerne weitere Abschussvorrichtungen hinzufügen oder komplexere Designs ausprobieren. Hier ist ein weiterer ähnlicher Entwurf mit fünf Abschussvorrichtungen.

![](images/appendices/appendix_5/a5_launcher_array2.png)

## Periodische und zufällig getaktete Abschussgeräte

Du kannst die Redstone-Uhren aus Abschnitt 2 mit den Logikgattern aus Abschnitt 3 verwenden, um spezielle Feuerwerkskörper zu bauen. Der AND-Gatter-Starter kann eine regelmäßige, periodische Abschusssequenz erzeugen. Sie können die pulsierenden Verzögerungen anpassen, indem Sie die Zeitpunkte der Wiederholer ändern. So kann man z. B. 4 Redstone-Impulse in 3 Sekunden mit einer Pause von 2 Sekunden oder 8 Impulse in 3 Sekunden mit einer Pause von 8 Sekunden erzeugen.

![](images/appendices/appendix_5/a5_AND_gate_launcher.png)

Der XOR-Gatter-Starter kann eine unregelmäßige Startsequenz erzeugen. Auch hier können Sie die Wiederholungszeiten ändern, um das scheinbar zufällige Verhalten zu ändern.

![](images/appendices/appendix_5/a5_XOR_gate_launcher_front.png)

![](images/appendices/appendix_5/a5_XOR_gate_launcher_rear.png)

Versuchen Sie selbst zu experimentieren, um die Muster zu finden, die Ihnen gefallen. Kombiniert man die Abschussvorrichtung mit den AND-Gatter- und XOR-Gatter-Abschussvorrichtungen, erhält man ein tolles Feuerwerk!
