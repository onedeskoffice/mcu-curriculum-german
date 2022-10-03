## Fallen: Entwurf und Ausführung

Es gibt ein paar wichtige Merkmale, die jede gute Falle haben muss. Sie müssen keinen Verdacht erregen und die Opfer mit Truhen oder seltenen Gegenständen anlocken. Sie sollten einen unterhaltsamen oder einzigartigen Mechanismus haben, denn schließlich dienen alle Minecraft-Fallen nur der Unterhaltung. Eine Falle hat drei Hauptbestandteile: den Fallenmechanismus, den Auslöser und den Köder.

1. Der erste Punkt, den man beim Bau einer Falle berücksichtigen sollte, ist der Fallenmechanismus selbst. Wie wollen Sie den Spieler, der in Ihrem Haus herumgeschnüffelt hat, in die Falle locken? Obsidian kann sehr starke Fallen darstellen, da es Diamant (und viel Zeit) erfordert, um ihn zu brechen; wenn der gefangene Spieler keine Möglichkeit hat, Obsidian zu brechen, sitzt er im Grunde fest! Wasser- und Lavafallen können einen Spieler verlangsamen und sogar töten, sind aber wesentlich schwieriger zu verstecken. Für unsere Falle werden wir Stein und Wasser verwenden. Stein ist leichter zu beschaffen als Obsidian, aber immer noch schwer zu brechen, vor allem, wenn sich der Spieler unter dem Wasser befindet, das wir ihm auf den Kopf fallen lassen werden!

1. Auslöser können viele Formen annehmen. Am offensichtlichsten sind Stolperdrähte und Druckplatten, die man auf verschiedene Weise platzieren kann, um eine Entdeckung zu vermeiden (z. B. indem man Druckplatten aus Holz nur auf Holz der gleichen Farbe legt). Aber auch Knöpfe und Hebel können verwendet werden. Sie können den Anschein erwecken, dass ein Knopf eine bestimmte Tür öffnet, während er in Wirklichkeit die Falle aktiviert. Hebel können für zwei Zwecke verwendet werden. Sie können zum Beispiel 3 Hebel haben, die als Kombinationsschloss für eine Tür dienen. Eine Kombination öffnet die Tür, während eine falsche Kombination eine Falle für den Eindringling auslöst. Unsere Falle wird eine Fallenkiste als Auslöser verwenden.

1. Eine mit Wertgegenständen gefüllte Fallentruhe dient als Köder für diese Falle. Aber auch interessante Räume, seltene Blöcke und sogar Mineneingänge können als Köder verwendet werden. Solange das Objekt etwas hat, das ein Spieler begehren würde, kann es als Köder für eine Falle dienen. Schutzfallen haben keinen wirklichen "Köder", da die Falle die Spieler nicht anlocken soll; vielmehr ist der Gegenstand, den sie schützen, in gewisser Weise der Köder. Unser Köder sind die wertvollen Gegenstände, die wir in unsere Fallenkiste legen werden.

Nachdem ihr nun die Grundlagen der Fallen kennengelernt habt, werden wir nun eine Beispielfalle mit einer Fallentruhe, Wasser und Kolben bauen.

## Fallenkästen

Fallentruhen senden ein Rotsteinsignal aus, dessen Stärke von der Anzahl der Personen abhängt, die die Truhe öffnen. Wir können dieses Signal nutzen, um eine Falle auszulösen, die für die Personen gedacht ist, die die Truhe öffnen. Beim Öffnen der Truhe wird ein Wasserfluss ausgelöst, der erst durch das Drücken einer Reset-Taste gestoppt wird.

1. Platziere irgendwo eine Fallentruhe. Sie bestehen aus einer normalen Truhe und einem Stolperdraht. Grabe ein Loch hinter der Truhe und platziere ein Stück roten Steinstaub.
![](images/appendices/appendix_4/trap_chest_placement.png)

1. Grabe ein zweites Loch und platziere einen Rotstein-Verstärker. Da die Kraft der roten Steine proportional zur Anzahl der Personen ist, die die Truhe öffnen, wird diese Falle ausgelöst, wenn nur eine Person die Truhe öffnet.
![](images/appendices/appendix_4/trap_chest_repeater.png)

1. Die Verkabelung, die dafür sorgt, dass sich das Wassertor öffnet, wenn die Truhe geöffnet wird. Es ist ein bisschen knifflig, aber weiter unten gibt es zusätzliche Bilder, denen ihr folgen könnt.
![](images/appendices/appendix_4/trap_chest_wiring.png)
![](images/appendices/appendix_4/trap_chest_wiring2.png)
![](images/anhänge/anhang_4/trap_chest_wiring3.png)

1. Dies ist das "Einbahntor", das verhindert, dass das Wasser abgestellt wird, auch wenn die Falle geschlossen ist. Wenn der Knopf auf der linken Seite gedrückt wird, wird die erste Fackel ausgeschaltet und die zweite Fackel eingeschaltet (da die erste Fackel sie nicht mehr sperrt). Jetzt deaktiviert die zweite Fackel die erste Fackel, da ihr roter Stein in den Block der ersten Fackel führt. Das Umschalten des Schalters (oder der Truhe in unserem Fall) ändert den Zustand des Schalters nicht.
![](images/appendices/appendix_4/trap_chest_flipflopexample.png)

Versucht, euch andere Ideen für Fallen auszudenken, die lustig oder nützlich sein könnten. Experimentiert und tauscht eure Ideen untereinander aus.

*# Lichtschalter

Mit Hilfe von XOR-Gattern könnt ihr ein Licht erzeugen, das ihr mit mehreren Schaltern steuern könnt. Vielleicht gibt es in eurem Haus auch Lampen, die auf diese Weise funktionieren! Jedes Licht, das mit mehreren Schaltern gesteuert werden kann, verwendet ein XOR-Gatter. Am häufigsten werden sie für die Beleuchtung von Treppenhäusern verwendet.

1. Baue eine Wand und hänge eine Redstone-Lampe daran. Bringe an jedem Ende der Wand einen Hebel an. Die Idee ist, dass die Hebel so weit entfernt sein können, wie du willst, aber dies ist eine einfache Demonstration.
![](images/section_4/xor_light_1.png)

2. Erstelle ein XOR-Gatter hinter der Wand, wobei der Ausgang in Richtung der Wand zeigt. Verwenden Sie das Referenzbild aus Abschnitt 3, wenn Sie es brauchen. Denken Sie daran, dass Sie die Hebel nicht zu platzieren brauchen, da das Redstone-Signal von den Hebeln kommt, die Sie auf der Vorderseite der Wand platziert haben. Verbinden Sie diese mit dem XOR-Gatter mit Redstone.
![](images/section_4/xor_light_2.png)

3. Führe das Redstone-Signal, das vom Ausgang des XOR-Gatters kommt, durch die Rückseite der Wand zur Lampe, wie gezeigt.
![](images/section_4/xor_light_3.png)

4. Das war's! Wenn du einen der Hebel umlegst, geht deine Lampe an. Du kannst sie so oft umlegen, wie du willst. Die Lampe leuchtet immer, egal in welche Richtung du einen der Hebel umlegst.
![](images/section_4/xor_light_4.png)
