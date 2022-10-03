# Abschnitt 3: Logische Gatter

Logische Gatter sind ein grundlegender Baustein für digitale Schaltungen. Sie führen _boolean_ Funktionen aus und haben normalerweise 2 Eingänge und 1 Ausgang

## UND

Das UND-Gatter führt die logische UND-Funktion aus, die mathematisch wie eine Multiplikation funktioniert.

In Minecraft nimmt dein UND-Gatter zwei Redstone-Eingänge an, die entweder EIN oder AUS sein können.  Die Ausgabe hängt von der Kombination der Eingänge ab:
<img src="images/section_3/gate_AND.png" style="width:50%">

ON AND ON => ON  
ON AND OFF => OFF  
OFF AND ON => OFF  
OFF AND OFF => OFF  

Probieren Sie dies an dem obigen Tor aus und sehen Sie, was passiert. Denke daran, dass ein Hebel AUS ist, wenn er nach oben zeigt.

## Wahrheitstabellen

Wahrheitstabellen sind eine einfache Möglichkeit, die verschiedenen Ausgänge von Logikgattern bei unterschiedlichen Eingängen zu organisieren.  
Bei boolescher Logik wird "EIN" durch "Wahr" oder "1" und "AUS" durch "Falsch" oder "0" ersetzt. Das AND-Gatter könnte zum Beispiel so aussehen:

WAHR UND WAHR => WAHR  
WAHR UND FALSCH => FALSCH  
FALSCH UND WAHR => FALSCH  
FALSCH UND FALSCH => FALSCH  

Das ist dasselbe wie:  
1 UND 1 => 1  
1 UND 0 => 0  
0 UND 1 => 0  
0 UND 0 => 0  

Wir können dies weiter vereinfachen und in einer Tabelle darstellen:  

Eingabe | Eingabe | Ausgabe
--- | --- | ---
1 | 1 | 1
1 | 0 | 0
0 | 1 | 0
0 | 0 | 0

<!--BREAK-->
## ODER

Das ODER-Gatter gibt nur dann AUS, wenn beide Eingänge AUS sind. Ist einer der Eingänge EIN oder sind beide EIN, so ist der Ausgang EIN:
<img src="images/section_3/gate_OR.png" style="width:50%">

Eingang | Eingang | Ausgang
--- | --- | ---
1 | 1 | 1
1 | 0 | 1
0 | 1 | 1
0 | 0 | 0

<!--BREAK-->
## NOT

Ein NOT-Gatter hat nur einen Eingang und kehrt diesen einfach um. Ein EIN-Eingang führt zu einem AUS-Ausgang, und umgekehrt:
<img src="images/section_3/gate_NOT.png" style="width:50%">

Eingang | Ausgang
--- | ---
0 | 1
1 | 0  

<!--BREAK-->
*# NOR

Ein NOR-Gatter ist einfach ein ODER-Gatter mit umgekehrten Ausgängen. Ein NOR-Gatter gibt also nur dann EIN aus, wenn beide Eingänge AUS sind. Andernfalls ist der Ausgang AUS:
<img src="images/section_3/gate_NOR.png" style="width:50%">

Eingang | Eingang | Ausgang
--- | --- | ---
1 | 1 | 0
1 | 0 | 0
0 | 1 | 0
0 | 0 | 1

<!--BREAK-->
## NAND

So wie ein NOR-Gatter die entgegengesetzten Ausgänge eines OR-Gatters hat, hat ein NAND-Gatter die entgegengesetzten Ausgänge eines AND-Gatters. Es gibt nur dann AUS, wenn beide Eingänge EIN sind. Wenn einer der Eingänge AUS ist, ist der Ausgang EIN:
<img src="images/section_3/gate_NAND.png" style="width:50%">

Eingang | Eingang | Ausgang
--- | --- | ---
1 | 1 | 0
1 | 0 | 1
0 | 1 | 1
0 | 0 | 1

<!--BREAK-->
## XOR

Ein XOR-Gatter (ex-or) wird auch als "exklusives ODER"-Gatter bezeichnet. Es gibt nur dann EIN aus, wenn einer der beiden Hebel EIN ist. Wenn beide Hebel entweder aus oder ein sind, wird es AUS ausgeben:
<img src="images/section_3/gate_XOR_front.png" style="width:50%">

<img src="images/section_3/gate_XOR_back.png" style="width:50%">

Eingabe | Eingabe | Ausgabe
--- | --- | ---
1 | 1 | 0
1 | 0 | 1
0 | 1 | 1
0 | 0 | 0

## Referenz

Dieses Diagramm enthält die meisten der Logikgatter, die wir besprochen haben, sowie einige weitere, die Sie vielleicht nützlich finden.

<img src="images/section_3/redstone_diagrams.jpg" style="width:50%">
