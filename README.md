# 🧠 20minfantasy: Optimal Team Configuration

Du willst gerade auch das optimale Team finden, um beim **20min Fantasy** zu gewinnen?  
Ich habe hier ein paar spannende Analysen und Visualisierungen erstellt.

## tl;dr

Scheiss auf Stürmer, wir spielen 5-4-1 mit Marvin Hitz odr Brecher!

Schaue diese zwei grafiken an 
und das Ende:

## Datenbasis

Einige [Daten](docs/data.csv) haben wir zur Verfügung – heruntergeladen von  
["20min/json/fantasy/stats_centre_table.json"](https://fantasy.20min.ch/json/fantasy/stats_centre_table.json)

Wir haben den Datensatz zusätzlich erweitert um:
- `averagePoints_per_price`
- `totalPoints_per_price`

Insgesamt enthält der Datensatz **312 Spieler** mit folgenden Spalten:

```python
['playerId', 'squadId', 'firstName', 'lastName', 'displayName',
 'position', 'price', 'gameWeekPoints', 'averagePoints', 'last3Average',
 'bonusPoints', 'totalPoints', 'percentSelected', 'form', 'goals',
 'assists', 'minutesPlayed', 'shotsOnTarget', 'chancesCreated',
 'tackles', 'cleanSheet', 'saves', 'goalsConceded', 'yellowCards',
 'redCards', 'ownGoals', 'penaltyMisses', 'penaltySaves', 'bonusPpm',
 'dribbles', 'crosses', 'offsides', 'passCompletionRate',
 'interceptions', 'blocks', 'foulsWon', 'foulsMade', 'goalsOutsideArea',
 'errorsLeadingToGoal', 'totalPoints_per_price', 'averagePoints_per_price']

```


##  🏆  Top 20 Spieler nach TotalPoints per Price

Nun wollen wir jedoch die Spieler, die **nicht overpriced** sind.

Wir schauen uns die **20 Spieler** an, die am meisten **Punkte pro Preis** geholt haben:

**Position Breakdown:**  
GK: 9 | DEF: 6 | MID: 4 | FWD: 1


| Name    | Pos | Total Punkte | Ø Punkte | Preis | Total Punkte / Preis |
|----------------|----------|-------------|----------------|-------|------------------------|
| M. Hitz        | GK       | 183         | 5.1            | 7.5   | 24.4              |
| Y. Brecher     | GK       | 181         | 4.8            | 7.5   | 24.1              |
| X. Shaqiri     | MID      | 265         | 7.8            | 11.0  | 24.1              |
| J. Hammel      | GK       | 164         | 4.4            | 7.0   | 23.4              |
| S. Kapino      | GK       | 160         | 4.8            | 7.0   | 22.9              |
| M. Stevanovic  | MID      | 224         | 5.9            | 10.0  | 22.4              |
| K. Letica      | GK       | 142         | 4.2            | 6.5   | 21.8              |
| D. Schmid      | DEF      | 165         | 4.7            | 8.0   | 20.6              |
| L. Zigi        | GK       | 132         | 3.5            | 6.5   | 20.3              |
| P. Loretz      | GK       | 132         | 3.5            | 6.5   | 20.3              |
| D. Rrudhani    | MID      | 150         | 4.8            | 7.5   | 20.0              |
| M. Poaty       | DEF      | 117         | 3.2            | 6.0   | 19.5              |
| A. Saipi       | GK       | 117         | 3.4            | 6.0   | 19.5             |
| N. Dussenne    | DEF      | 143         | 4.3            | 7.5   | 19.1            |
| P. Dorn        | DEF      | 133         | 3.6            | 7.0   | 19.0              |
| B. Traoré      | FWD      | 170         | 4.7            | 9.0   | 18.9          |
| A. Sanches     | MID      | 158         | 5.6            | 8.5   | 18.6            |
| T. Fayulu      | GK       | 110         | 3.1            | 6.0   | 18.3           |
| N. Lavanchy    | DEF      | 100         | 2.8            | 5.5   | 18.2           |
| M. Gómez       | DEF      | 109         | 2.9            | 6.0   | 18.2   



Sehr spannend, dass **Torhüter Platz 1 & 2** ausmachen – und insgesamt **9 GKs** in den Top 20 sind.  
Auch interessant: **Nur 1 Stürmer** ist vertreten.

Vielleicht war es eine ungewöhnliche Saison – aber es deutet darauf hin, dass man lieber ein **5-4-1** als ein **4-3-3** spielen sollte.



## 📈 Top 20 nach Average Points per Price  
*(nur Spieler mit >900 Minuten Spielzeit, ohne Torhüter, da diese auch hier wieder klar dominieren)*

Da die vorherige Statistik Spieler benachteiligt, die verletzt waren oder erst zur Winterpause kamen, betrachten wir nun die **durchschnittlichen Punkte pro Preis**.

---

**Position Breakdown:**  
DEF: 10 | MID: 9 | FWD: 1



| Name   | Pos |Total Punkte| Ø Punkte | Preis 	|Ø Punkte / Preis |	Min gespielt| 
|-|-|-|-|-|-|-|
| 	X. Shaqiri 	    |MID 	|265 	|7.8 	|11.0 	|0.71 	|2618|
| 	P. Otele 	    |MID 	|95 	|5.3 |	8.0 	|0.68 	|1020|
| 	A. Sanches 	    |ID 	|158 	|5.6 	|8.5 	|0.66	|2371|
| 	B. Kololli 	    |MID 	|95 	|4.5 	|7.0 	|0.64	|1208|
| 	D. Rrudhani 	|MID 	|150 	|4.8 	|7.5 	|0.64  	|2189|
| 	S. Rouiller 	|DEF 	|112 	|4.0 	|6.5 	|0.62 	|2419|
| 	C. Fassnacht 	|MID 	|104 	|5.8 	|9.5 	|0.61 	|1440|
| 	M. Stevanovic 	|MID 	|224 	|5.9 	|10.0 	|0.59  	|3179|
| 	D. Schmid 	    |DEF 	|165 	|4.7 	|8.0 	|0.59 	|2922|
| 	L. Lüthi 	    |DEF 	|92 	|3.5 	|6.0 	|0.58  	|2340|
| 	L. Benito 	    |DEF 	|86 	|3.2 	|5.5 	|0.58  	|2246|
| 	C. Tsawa 	    |MID 	|47 	|2.9 	|5.0 	|0.58  	|1000|
| 	N. Dussenne 	|DEF 	|143 	|4.3 	|7.5 	|0.57  	|2937|
| 	K. Sow 	        |DEF 	|83 	|2.8 	|5.0 	|0.56 	|2320|
| 	A. Barisic      |DEF 	|99 	|3.3 	|6.0 	|0.55  	|2424|
| 	K. Hajrizi      |DEF 	|36 	|2.4 	|4.5 	|0.53  	|1272|
| 	B. Freimann     |DEF 	|47 	|2.4 	|4.5 	|0.53  	|1409|
| 	M. Poaty        |DEF 	|117 	|3.2 	|6.0 	|0.53  	|2956|
| 	S. Zuber        |MID 	|94 	|4.7 	|9.0 	|0.52  	|1767|
| 	B. Traoré       |FWD 	|170 	|4.7 	|9.0 	|0.52 	|2411|


💡 **Fazit**:  
Hier tauchen interessante **Neuzugänge** wie *Otele* und *Fassnacht* auf.  
Erneut zeigt sich: **Stürmer liefern kaum Value**, während nun **Mittelfeldspieler und Verteidiger** klar dominieren.




FOglende Zwei grafiken helfen euch, alle Spieler zu untersuchen. 


Wenn Ihr selbst noch suchen / filtern wollt, hier habt ihr alle SPieler:

< Tabelle mit allen Spielern. mit diesen col, alle sortierbar und filterbar: 

'firstName', 'lastName',position', totalPoints, 'minutesPlayed' ,'averagePoints', 'price', 'totalPoints_per_price', 'averagePoints_per_price'

Zeigen nur die ersten 30 entries. >


Die folgenden Abbildungen helfen euch, eures Team zu picken. 


--> Zwei  HTML files..


## 🧠 Das perfekte Team

Nun möchten wir das perfekte Team finden. Dafür vereinfachen wir die Constraints etwas:

Da **Stürmer** im Vergleich zu anderen Positionen deutlich schwächer in *Points per Price* und *Average Points per Price* abschneiden, nehmen wir an, dass die optimale Formation entweder ein **5-4-1** oder ein **4-5-1** ist.

Wir versuchen also, die besten **11 bzw. 12 Spieler** zu finden. Die übrigen Positionen werden mit den **günstigsten Spielern** aufgefüllt:

- Im Sturm gibt es nur **einen 4-Millionen-Spieler** und einige wenige für 4.5 Mio.
- Ein schlechter Torwart kostet ca. **3.5 Millionen**.
- Ergänzt wird die Ersatzbank mit einem beliebigen **4-Millionen-Spieler** aus dem Mittelfeld oder der Verteidigung (je nach Formation).

Das bedeutet:
- **16 Mio** Budget gehen bei der 11-Spieler-Optimierung für günstige Bankspieler weg
- **12 Mio** bei 12-Spieler-Auswahl

#### 📋 Übersicht der Constraints

| Spielerzahl | Budget | DEF | MID | FWD |
|-------------|--------|-----|-----|-----|
| 11 Spieler  | 84 Mio | 4–5 | 4–5 | 1   |
| 12 Spieler  | 88 Mio | 4–5 | 4–5 | 1–2 |

---

### 🔝 Top 11 nach Total Points  
**Kosten:** 84.00 Mio  
**Total Points:** 1688
**Avg Points:** 153.4




| Name    | Pos | Preis | Ø Punkte | Total Punkte |
|------------------|----------|--------|----------------|---------------|
|N. Lavanchy 	| DEF 	 	| 5.5 	|2.8 	|100
|N. Dussenne 	| DEF 		| 7.5 	|4.3 |	143
|A. Ciganiks 	| DEF 		| 5.0 	|2.6 	|90
|M. Poaty 	  | DEF 		| 6.0 	|3.2 |	117
|	D. Schmid 	| DEF 	 	|8.0 	|4.7 |	165
|B. Traoré  	| FWD 		|9.0 	|4.7 	|170
|Y. Brecher 	| GK 	  	|7.5 	|4.8 	|181
|	X. Shaqiri 	| MID 		|11.0 	|7.8 |	265
|	M. Di Giusto 	| MID 	|8.5 	|3.9 	|149
|	A. Sanches 	| MID 		|8.5 |	5.6| 	158
|	D. Rrudhani |	MID 	|7.5 	|4.8 	|150


---

### 🔝 Top 12 nach Total Points  
**Kosten:** 88.00 Mio  
**Total Points:** 1738
**Avg Points:** 144.8

| Name    | Pos | Preis | Ø Punkte | Total Punkte |
|------------------|----------|-------|----------------|---------------|
|    N. Lavanchy |  DEF|5.5|2.8|100|
 |   N. Dussenne | DEF|7.5|4.3|143|
 |   A. Ciganiks | DEF|5.0|2.6 |	90|
 |   M. Poaty | DEF|6.0|3.2 |	117|
 |   D. Schmid | DEF|8.0|4.7 |	165|
 |   B. Traoré | FWD|9.0|4.7 	|170|
 |   T. Berdayes | FWD|6.5|2.9 |	106|
 |   Y. Brecher | GK|7.5|4.8 |	181|
 |   X. Shaqiri | MID|11.0|7.8 |	265|
 |   B. Toma | MID|6.0|2.7|93|
 |   A. Sanches | MID|8.5|5.6 |	158|
 |   D. Rrudhani | MID|7.5|4.8 |	150|



--- 
### 🔝 Top 11 nach Average Points (min. 900 Minuten)

**Kosten:** 84.00 Mio  
**Average Points (Schnitt):** 4.86

| Name    | Pos |   Preis | Ø Punkte | Total Punkte | Min gespielt |
|------------------|----------|--------|----------------|---------------|------------------|
| 	L. Benito 	|DEF 	| 	5.5 |	3.2 |	86 |	2246|
| 	S. Rouiller|DEF 	| 	6.5 |	4.0 |	112 	|2419|
| 	N. Dussenne|DEF 	| 	7.5 |	4.3 |	143 |	2937|
| 	D. Schmid|DEF 	| 	8.0 	|4.7 |	165 |	2922|
| 	G. Koutsias|FWD 	| 	6.0 |	3.1 |	61 |	1241|
| 	J. Frick|GK 	| 	6.0 	|4.9 |64 |	1170|
| 	X. Shaqiri|MID 	| 	11.0 |	7.8 |	265 |	2618|
| 	C. Fassnacht|MID 	| 	9.5 	|5.8 |	104 |	1440|
| 	P. Otele|MID 	| 	8.0 	|5.3 |	95 |	1020|
| 	A. Sanches|MID 	| 	8.5 	|5.6 |	158 |	2371|
| 	D. Rrudhani|MID 	| 	7.5 |	4.8 |	150 |	2189|


### 🔝Top 12 nach Average Points (min. 900 Minuten)

**Kosten:** 88.00 Mio  
**Average Points (Schnitt):** 5.07


| Name    | Pos |   Preis | Ø Punkte | Total Punkte | Min gespielt |
|------------------|----------|--------|----------------|---------------|------------------|
| 	S. Rouiller|DEF 	| 	6.5|4.0|112|2419|
| 	N. Dussenne|DEF 	| 	7.5|4.3|143|2937|
| 	D. Schmid|DEF 	| 	8.0|4.7|165|2922|
| 	K. Sow 	|DEF 	| 	5.0|2.8|83|2320|
| 	L. Lüthi 	|DEF 	| 	6.0|3.5|92|2340|
| 	C. Bedia 	|FWD 	| 	7.0|3.6|62|1093|
| 	J. Frick 	|GK 	| 	6.0|4.9|64|1170|
| 	X. Shaqiri 	|MID 	| 	11.0|7.8|265|2618|
| 	B. Kololli 	|MID 	| 	7.0 	|4.5|95|1208|
| 	P. Otele 	|MID 	| 	8.0 	|5.3|95|1020|
| 	A. Sanches 	|MID 	| 	8.5 	|5.6|158|2371|
| 	D. Rrudhani 	|MID 	| 	7.5 	|4.8|150|2189|

