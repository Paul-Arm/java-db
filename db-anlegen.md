## Straßenbahn 

1. Datenbank anlegen, mit Testwerten füllen und exportieren
>a) Legen Sie eine Datenbank EVAG an. 

>b) Erstellen Sie eine Tabelle Strassenbahn mit folgenden Attributen:
>>– id (int) – eindeutige Nummer der Straßenbahn 
>>– modus (boolean/tinyint) – ist true(1) falls die Straßenbahn fährt, ansonsten false(0)
>>– maxPassagiere (int) – maximal zulässige Anzahl an Personen\
>>– passagiere (int) – Anzahl der Personen, die aktuell in der Straßenbahn sind\
>>– anschaffungstag (date) – Datum der Anschaffung im Format YYYY-MM-DD

>c) Definieren Sie das Attribut id als Primärschlüssel.

>d) Füllen Sie die Tabelle mit Testdaten (mindestens 5 Straßenbahnen).

>e) Exportieren Sie die Datenbank und analysieren Sie den Inhalt der .sql-Datei.


## Lösung

```
-- Erstelle die Tabelle

CREATE TABLE strassenbahn (
  id INT(11) PRIMARY KEY,
  maxPassagiere INT(11),
  passagiere INT(11),
  anschaffungstag DATE,
  modus TINYINT(1)
);

-- Füge die Beispieldaten ein

INSERT INTO strassenbahn (id, maxPassagiere, passagiere, anschaffungstag, modus)
VALUES
  (1, 150, 120, '2022-01-15', 1),
  (2, 200, 180, '2021-09-28', 1),
  (3, 100, 80, '2023-04-05', 0),
  (4, 50, 45, '2022-11-10', 1),
  (5, 300, 250, '2023-02-19', 1);
 
```
## 2.

Formulieren Sie die SQL-Anweisungen für folgende Abfragen.

a) Liste aller Strassenbahnen mit allen Informationen.

SELECT

b) Liste aller Strassenbahnen mit der ID und maxPassagiere.
SELECT id,

c) maxPassagiere von der Strassenbahn mit der größten Anzahl von maxPassagiere.
SELECT MAX(maxPassagiere)

d) maxPassagiere von der Strassenbahn mit der kleinsten Anzahl von maxPassagiere.

e) Summe aller Passagiere die maximal in allen Strassenbahnen befördert werden können.

f) Liste aller Strassenbahnen die vor 2021 angeschafft wurden.
SELECT * FROM strassenbahn WHERE anschaffungstag<"2021-01-01";

g) Liste aller Strassenbahnen die im Jahr 2020 angeschafft wurden.

h) Liste aller Strassenbahnen die aktuell nicht fahren.

i) Liste aller Strassenbahnen die aktuell voll belegt sind.

j) Liste aller Strassenbahnen aufsteigend sortiert nach maxPassagiere.

k) ZUSATZ: ID und maxPassagiere von den Strassenbahnen mit der größten Anzahl von
maxPassagiere.