# Challenge - Garten Aufräumen

Ein Roboter soll den Garten aufräumen. Der Garten hat verschiedene Bereiche. Jeder Bereich hat einen Buchstaben. In einem Bereich kann sich genau ein Gegenstand, z.B. ein Trampolin, Stuhl oder Ball, befinden. Mindestens einer der Bereiche ist immer frei.

Nun soll der Roboter die Gegenstände nach ihrer Masse sortieren und in die richtigen Bereiche bringen. Der schwerste Gegenstand gehört in den Bereich A, der Zweitschwerste in den Bereich B und so weiter. Dabei kann der Roboter nur einen Gegenstand zur Zeit transportieren und diesen nur in einem freien Bereich absetzen. Um Gegnstände zu nehmen oder abzusetzen muss der Roboter sich in dem Bereich befinden. Der Roboter darf zu jedem Zeitpunkt mit oder ohne Gegenstand überall entlangfahren.

Gegeben sind die Massen der Gegenstände in Kilogramm und eine Karte vom Garten. Das Dateiformat geht wie folgt:

```sh
A=100
C=
B=400

.............
.............
..A.....B....
.....C.......
.............
......$......
```

- In den ersten Zeilen der Datei befinden sich die Buchstaben der Bereiche mit den zugehörigen Gewichten von den Gegenständen, die sich dort befinden. Bereiche ohne Gewichtsangabe sind frei. Zudem werden Buchstaben nie ausgelassen, es kann also nur einen Bereich D geben, wenn es die Bereiche A, B, und C gibt. Die Anzahl der Bereiche ist aber variabel.
- Eine Leerzeile beendet den Abschnitt mit den Angaben zu den Bereichen
- Darauf folgt eine genordete Karte. Dabei steht:
    - ein Punkt für Rasen,
    - ein Buchstabe für einen Bereich,
    - das Dollar (`$`) Zeichen für die Startposition des Roboters.

Schreibe ein Programm, das ausgibt, was der Roboter tun muss, um seine Aufgabe zu erfüllen. Es gibt die Befehle `fahre_norden`, `fahre_osten`, `fahre_sueden`, `fahre_westen`, `nehme_gegenstand` und `setze_gegenstand_ab`. Hinter den Befehlen zum Fahren soll immer stehen, wie häufig sie durchgeführt werden sollen, damit die Ausgabe besser lesbar ist.

Die Ausgabe des Programms für das Beispiel sollte in etwa so aussehen:

```
fahre_norden 3
fahre_westen 4
nehme_gegenstand
fahre_osten 3
fahre_süden 1
setze_gegenstand_ab
fahre_norden 1
fahre_osten 3
nehme_gegenstand
fahre_westen 6
setze_gegenstand_ab
fahre_osten 3
fahre_süden 1
nehme_gegenstand_auf
fahre_norden 1
fahre_osten 3
setze_gegenstand_ab
```

