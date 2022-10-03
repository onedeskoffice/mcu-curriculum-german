# Abschnitt 4: Anwendungen von logischen Gattern

## Verschlossene Türen

Manchmal möchte man verhindern, dass jemand eine Tür mit einem Schloss betritt. Mit einem Hebel auf der Innenseite können Sie verhindern, dass die Tür geöffnet wird, wenn der Hebel nicht in einem bestimmten Zustand ist.

1. Platziere eine Tür und errichte eine Mauer um die Tür. Ein Knopf sollte einen Block von der Tür entfernt platziert werden; sein Block darf die Tür nicht berühren, sonst wird er die Tür jedes Mal öffnen.
<img src="images/section_4/locked_door_initial.png" style="width:50%">

1. Die Position des Schlosshebels in der Tür.
<img src="images/section_4/locked_door_lever.png" style="width:50%">

1. Wiederholer, die das Signal des roten Steins von Knopf und Hebel weiterleiten. Achte darauf, die Steinschicht unter ihnen zu platzieren, damit sie von Knopf und Hebel mit Strom versorgt werden.
<img src="images/section_4/locked_door_repeaters.png" style="width:50%">

1. Ein UND-Gatter. Die beiden Eingänge sind der Hebel und der Knopf, und der Ausgang geht an die Tür. Der Ausgang wird nur dann eingeschaltet, wenn sowohl der Knopf als auch der Hebel eingeschaltet sind.
<img src="images/section_4/locked_door_AND.png" style="width:50%">

1. Der rote Stein, der den Ausgang des UND-Gatters zu dem Block direkt unter der Tür leitet. Jetzt öffnet sich die Tür nur noch, wenn der Hebel umgelegt und der Knopf gedrückt wird.
<img src="images/section_4/locked_door_redstone.png" style="width:50%">
