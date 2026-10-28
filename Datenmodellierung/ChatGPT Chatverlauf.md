
# Zwischentabellen bei Netzwerkförmigen Beziehungen
## 1. Ausgangslage: M:N-Beziehung

- Ein Mitarbeiter kann mehrere Aufgaben erledigen.
    
- Eine Aufgabe kann von mehreren Mitarbeitern erledigt werden.
    

Das ist eine M:N-Beziehung.

## 2. Wir erstellen die Zwischentabelle

### MITARBEITER

|MitarbeiterID (PK)|Vorname|
|---|---|
|1|Anna|
|2|Luca|

### AUFGABE

|AufgabeID (PK)|Bezeichnung|
|---|---|
|10|Putzen|
|20|Reparieren|

### MITARBEITER_HAT_AUFGABE

|MitarbeiterID (PK, FK)|AufgabeID (PK, FK)|
|---|---|
|1|10|
|1|20|
|2|10|

Die Zwischentabelle enthält also die beiden Fremdschlüssel:

- `MitarbeiterID` → verweist auf `MITARBEITER`
    
- `AufgabeID` → verweist auf `AUFGABE`
    

Zusammen bilden sie den zusammengesetzten Primärschlüssel (PK). So kann dieselbe Kombination aus Mitarbeiter und Aufgabe nicht doppelt vorkommen.

## 3. Was steht in den ursprünglichen Tabellen?

In `MITARBEITER` bleibt die Tabelle wie vorher. Du fügst dort keine Spalte `MitarbeiterHatAufgabe` hinzu.

Dasselbe gilt für `AUFGABE`: Auch dort kommt keine zusätzliche Spalte für die Zwischentabelle hinzu.

Die Verknüpfung wird ausschliesslich über `MITARBEITER_HAT_AUFGABE` hergestellt.

Merksatz: Bei einer M:N-Beziehung kommen die beiden Fremdschlüssel in die Zwischentabelle. Zusammen können sie deren zusammengesetzten Primärschlüssel bilden.

wie hat es vor der zwischentabelle ausgesehen

Gute Frage! 😊 Schauen wir an, wie es vor der Zwischentabelle ausgesehen hat.

## Vorher: M:N-Beziehung ohne Zwischentabelle

Du hast zwei Tabellen, die direkt miteinander verbunden sind:

MITARBEITER

|MitarbeiterID (PK)|Vorname|
|---|---|
|1|Anna|
|2|Luca|

M:N

Ein Mitarbeiter kann viele Aufgaben haben und eine Aufgabe viele Mitarbeiter.

AUFGABE

|AufgabeID (PK)|Bezeichnung|
|---|---|
|10|Putzen|
|20|Reparieren|

In diesem Modell gibt es noch keine Fremdschlüsselspalten für diese Beziehung. Die Beziehung ist nur konzeptionell dargestellt.

## Warum reicht das für eine relationale Datenbank nicht?

Wenn du einfach `AufgabeID` in `MITARBEITER` einfügst, könnte Anna nur eine Aufgabe direkt zugeordnet bekommen, ohne mehrere Werte in einer Spalte speichern zu müssen.

Wenn du `MitarbeiterID` in `AUFGABE` einfügst, könnte jede Aufgabe nur einem Mitarbeiter direkt zugeordnet werden.

Darum löst du die M:N-Beziehung mit einer Zwischentabelle auf:

MITARBEITER

1:N

MITARBEITER_HAT_AUFGABE

MitarbeiterID (PK, FK)

AufgabeID (PK, FK)

N:1

AUFGABE

Merke: Vorher hast du eine M:N-Beziehung. Nachher hast du zwei 1:N-Beziehungen. Die Zwischentabelle speichert, welcher Mitarbeiter welche Aufgabe erledigt.



<mark>ahh dann schaust du nicht in Aufgabe oder Mitarbeiter um zu sehen welcher mitarbeiter welche ag hat sondern im mitarbeiter_hat_aufgabe </mark>



Jaaa, genau!! 😄🎉 Du hast es verstanden!

Du schaust in `MITARBEITER_HAT_AUFGABE` nach, welcher Mitarbeiter welche Aufgabe hat.

Zum Beispiel:

|MitarbeiterID (FK)|AufgabeID (FK)|
|---|---|
|1|10|
|1|20|
|2|10|

Das bedeutet:

- Mitarbeiter 1 (Anna) hat Aufgabe 10 und 20.
    
- Mitarbeiter 2 (Luca) hat Aufgabe 10.
    
- Aufgabe 10 wird von Anna und Luca erledigt.
    

Die Namen und Aufgabenbezeichnungen findest du weiterhin in den Tabellen `MITARBEITER` und `AUFGABE`. Über die IDs in der Zwischentabelle verknüpfst du sie miteinander.

Merksatz für die Prüfung: Die Zwischentabelle speichert die Zuordnungen zwischen den beiden Tabellen. 💡



# M(c) zu M(c) wieso braucht es die Zwischentabelle
Nehmen wir dein Beispiel:

- Ein Mitarbeiter kann an mehreren Aufgaben arbeiten.
    
- Eine Aufgabe kann von mehreren Mitarbeitern bearbeitet werden.
    

Das ist eine M:N-Beziehung.

## Warum reicht eine `AufgabeID` als FK in der Mitarbeitertabelle nicht?

Wenn du die `AufgabeID` direkt in die Tabelle `Mitarbeiter` einfügst, könnte das so aussehen:

Tabelle Mitarbeiter

|MitarbeiterID|Name|AufgabeID|
|---|---|---|
|M01|Mia|A01|
|M02|Noah|A01|
|M03|Leon|A02|

Hier können zwar mehrere Mitarbeiter dieselbe Aufgabe haben. Aber ein Mitarbeiter kann nur eine Aufgabe zugeordnet bekommen, wenn du pro Mitarbeiter nur eine `AufgabeID` speicherst.

Du könntest mehrere Aufgaben-IDs in eine Zelle schreiben, aber das würde die 1. Normalform verletzen.

## Die richtige Lösung: Zwischentabelle

Mitarbeiter

MitarbeiterID (PK), Name

1:N

MitarbeiterAufgabe

MitarbeiterID (PK, FK)

AufgabeID (PK, FK)

N:1

Aufgabe

AufgabeID (PK), Bezeichnung

Die Zwischentabelle speichert jede Zuordnung als eigene Zeile:

|MitarbeiterID|AufgabeID|
|---|---|
|M01|A01|
|M01|A02|
|M02|A01|
|M03|A02|

Jetzt kann Mia an mehreren Aufgaben arbeiten, und eine Aufgabe kann mehreren Mitarbeitern zugeordnet werden.

Wichtig zu deiner Frage nach der Redundanz: Die `AufgabeID` wird nicht redundant, nur weil mehrere Mitarbeiter dieselbe Aufgabe bearbeiten. Das ist eine notwendige Wiederholung der Referenz. Problematisch wäre es, die Aufgabeninformationen selbst bei jedem Mitarbeiter erneut zu speichern.

Merksatz für die Prüfung: Eine M:N-Beziehung wird mit einer Zwischentabelle aufgelöst, die die Primärschlüssel beider Tabellen als Fremdschlüssel enthält. Meist bilden diese zusammen den zusammengesetzten Primärschlüssel der Zwischentabelle.

<mark> Wir müssen bei mc zu mc Beziehungen eine Zwischentabelle erstellen, da wir, wenn wir einfach eine neue Spalte mit dem FK einfügen nur eine einzige Aufgabe an die Mitarbeiter verteilen können, da der PK eindeutig sein muss.</mark>


# Wie erkenne ich Abhängigkeiten von Nichtschlüsselattributen auf andere Nichtschlüsselattribute (transitive Abhängigkeiten)-> 3NF nicht erreicht

Frage stellen; wenn ich A kenne; kenne ich dann direkt auch den Wert von B?
Beispiel: 

PLZ->Ort -> auch wenn KundeID der Primärschlüssel ist, bestimmt PLZ den Ort; der Ort hängt nur indirekt von der KundenID ab (da der PLZ davon abhängt)