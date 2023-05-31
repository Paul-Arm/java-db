# java-db
## Flugdatenbank


### Welche Flüge kosten weniger als 50 Euro? (Lösung: 62 Datensätze) SQL-Befehl:
`SELECT * FROM fluege WHERE Preis < 50 `

### Welche Flüge gehen von Bremen nach Hannover? (Lösung: 1 Datensatz)
SQL-Befehl: 
`SELECT * FROM fluege WHERE von LIKE "Bremen" && nach LIKE "Hannover"`

### Welche Abflugzeiten und –orte haben die Lufthansaflüge? (Lösung: 54 Datensätze)
SQL-Befehl:
`SELECT von, nach, ab FROM fluege WHERE Fluglinie LIKE 'Lufthansa';`

### Ab welchen Orten und Zeiten kann man mit Germanwings nach Münster fliegen?
(Lösung: 1 Datensatz)

`SELECT von, ab FROM fluege WHERE nach LIKE "Münster" AND Fluglinie LIKE "Germanwings";`

### 5 An welchen Orten starten welche Fluglinien die nach Frankfurt fliegen und zwischen 40,00
`Euro und 55,00 Euro kosten? Die Darstellung soll nach Abflughafen sortiert sein. 
SELECT * FROM `fluege` WHERE nach LIKE "Frankfurt" AND Preis BETWEEN 40 AND 55 ORDER BY ab;`

### 6. Wer fliegt von Berlin oder Hamburg nach Düsseldorf oder Dresden? (Lösung: 2 Datensätze)
SQL-Befehl:
`SELECT DISTINCT Flugline FROM fluege WHERE (von= "Berlin" OR von= "Hamburg") AND (nach= "Düsseldorf" OR nach= "Dresden")`