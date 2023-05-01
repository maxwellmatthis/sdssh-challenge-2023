# Challenge - Garten Aufräumen

Ein Roboter soll einen Garten aufräumen.
Der Garten hat verschiedene durchbuchstabierte Bereiche.
In einem Bereich kann sich genau ein Gegenstand (z.B. ein Ball oder ein Stuhl) befinden.
Mindestens einer der Bereiche ist immer frei.

Nun soll der Roboter die Gegenstände nach ihrer Masse sortieren und in die richtigen Bereiche bringen.
Der schwerste Gegenstand gehört in den Bereich A, der Zweitschwerste in den Bereich B und so weiter.
Dabei kann der Roboter nur einen Gegenstand zurzeit transportieren und diesen nur in einem freien Bereich absetzen.
Um Gegenstände zu nehmen oder abzusetzen muss der Roboter sich in dem Bereich befinden.
Der Roboter darf zu jedem Zeitpunkt mit oder ohne Gegenstand überall entlangfahren.

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

- In den ersten Zeilen der Datei befinden sich die Buchstaben der Bereiche mit den zugehörigen Gewichten von den Gegenständen, die sich dort befinden.
  Bereiche ohne Gewichtsangabe sind frei.
  Zudem werden Buchstaben nie ausgelassen, es kann also nur einen Bereich D geben, wenn es die Bereiche A, B, und C gibt.
  Die Anzahl der Bereiche ist aber variabel.
- Eine Leerzeile beendet den Abschnitt mit den Angaben zu den Bereichen
- Darauf folgt eine genordete Karte. Dabei steht:
    - ein Punkt für Rasen,
    - ein Buchstabe für einen Bereich,
    - das Dollar (`$`) Zeichen für die Startposition des Roboters.

Dieses Beispiel und Weitere zum Testen befinden sich im [Material Ordner](./material).

## Aufgabe

Schreibe ein Programm, das dem Roboter Anweisungen gibt, um den Garten gemäß den Anforderungen aufzuräumen.
Dafür müssen die Befehle `fahre_norden`, `fahre_osten`, `fahre_sueden`, `fahre_westen`, `gegenstand_aufheben` und `gegenstand_absetzen` durch Zeilenumbrüche getrennt hintereinander ausgegeben werden.
Um einen Befehl mehrfach auszuführen, kann eine natürliche Zahl durch ein Leerzeichen getrennt hinter dem Befehl ausgegeben werden.

Das Programm darf in einer beliebigen Programmiersprache geschrieben werden.
Wenn die Sprache nicht gängig ist, sollte eine kurze Anleitung zum Ausführen mit dabei sein.

Die Ausgabe des Programms für das Beispiel sollte in etwa so aussehen:

```
fahre_norden 3
fahre_westen 4
gegenstand_aufheben
fahre_osten 3
fahre_süden 1
gegenstand_absetzen
fahre_norden 1
fahre_osten 3
gegenstand_aufheben
fahre_westen 6
gegenstand_absetzen
fahre_osten 3
fahre_süden 1
gegenstand_aufheben
fahre_norden 1
fahre_osten 3
gegenstand_absetzen
```

