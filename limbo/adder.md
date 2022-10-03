## Redstone-Addierer-Schaltung

Eine _Adder_ verwendet logische Gatter, um eine Addition durchzuführen. Es gibt drei Eingänge für die gesamte Schaltung: A, B und Übertrag. Der Übertrag ist das Ergebnis der vorherigen Addition (man denke an den Übertrag einer 1 bei der Addition großer Zahlen). Die beiden Ausgänge sind das Ergebnis und der Übertrag für die nächste Addition.

Dieses Diagramm zeigt die allgemeine Struktur eines Addierers.  
Hinweis: Ein Punkt bedeutet, dass die beiden Linien des roten Steins miteinander verbunden sein sollten.  Andere Überschneidungen sollten nicht verbunden werden.

Ein Diagramm für einen Addierer. (adder_img/adder_diagram.png)

Sieh dir die Logikgatter an, um zu verstehen, wie der Addierer funktioniert.

Jetzt werden wir einen Addierer mit Redstone bauen! Folgen Sie den Schritten so gut Sie können. Dies ist eine komplexe Schaltung, also stellen Sie ruhig Fragen. Die Türen am Ende stellen den Ausgang dar. Das Türchen auf der linken Seite steht für den normalen Ausgang, das Türchen auf der rechten Seite für den Übertrag. Eine offene Tür ist eine 1 und eine geschlossene Tür ist eine 0.

Es gibt drei Eingänge, also achten Sie darauf, jeden einzelnen mit einem Zeichen zu versehen. Hebel sind am besten geeignet, da man sie leicht zwischen EIN und AUS umschalten kann.

Die drei Eingangshebel](adder_img/adder_inputs.png)

Als nächstes bauen wir zwei XOR-Gatter. Das erste (links; wir nennen es XOR-Gatter 1) erhält Eingaben von A und B. Das zweite (XOR-Gatter 2) erhält Eingaben von der Ausgabe des ersten Gatters und dem Übertrag.

Die ursprünglichen XOR-Gatter](adder_img/adder_XORs.png)

Eine zweite Perspektive auf die XOR-Gatter.

![Eine Rückwärtsansicht der XOR-Gatter](adder_img/adder_XORs_backwards.png)

Dieses UND-Gatter nimmt den Übertrag und den Ausgang des XOR-Gatters 1 als Eingang. Der blaue Kreis zeigt, wo der Ausgang des Gatters 1 zu diesem UND-Gatter hinauf und hinüber geht.

Das erste UND-Gatter. (adder_img/adder_AND.png)

Das zweite UND-Gatter. Dieses Gatter nimmt die Eingaben der ursprünglichen Eingänge A und B auf. Beachten Sie, wie es und der Ausgang des anderen UND-Gatters kombiniert werden und zur Tür gehen, die den Übertrag darstellt.

Das zweite UND-Gatter. (adder_img/adder_AND_2.png)

Zwei Übersichten des gesamten Addierers aus verschiedenen Perspektiven.

![Ein Überblick über den gesamten Addierer.](adder_img/adder_overview.png)  

![Ein zweiter Überblick über den Addierer](adder_img/adder_overview_backwards.png)
