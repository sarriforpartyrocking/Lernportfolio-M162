*Referenz: [Datenmodellierung/Theorie_Datenmodellierung.md · KES · TBZ-IT-Informatik / modules for students / m162 · GitLab](https://gitlab.com/ch-tbz-it/Stud/m162/-/blob/KES/Datenmodellierung/Theorie_Datenmodellierung.md)*
## 1. Was sind Redundanzen?

Redundanzen sind mehrfach gespeicherte Daten.

Wenn alles in einer einzigen Tabelle gespeichert wäre:

|Kunde|Adresse|Bestellung|
|---|---|---|
|Gustav Meier|Zürich|Laptop|
|Gustav Meier|Zürich|Maus|
|Beat Merz|Bern|Tastatur|

Gustav Meier und seine Adresse stehen zweimal in der Tabelle. Das ist eine Redundanz.

Problem: Wenn Gustav umzieht, muss man Adresse an mehreren Stellen ändern. Wird eine Stelle vergessen, vermindert das die Datenqualität.

## 2. Drei Anomalien

### **Einfüge-Anomalie**
Man wählt den PK so, dass er nicht eindeutig ist.

Beispiel: Man nimmt den Namen einer Person als PK und sobald eine Person mit demselben Namen als Datensatz eingetragen wird, gibt es eine Kollision.

### **Änderungs-Anomalie**
Dieselbe Information muss an mehreren Stellen geändert werden.

Beispiel: Gustav zieht um. Man ändert seine Adresse bei einer Bestellung, vergisst aber die zweite. Jetzt hat er in der Datenbank zwei verschiedene Adressen.


### **Lösch-Anomalie**
Beim Löschen bestimmter Daten gehen ungewollt weitere Informationen verloren.

Beispiel: Beat löscht seine einzige Bestellung. Wenn Kunde und Bestellung in derselben Zeile gespeichert sind, verschwindet dadurch auch seine Adresse aus der Datenbank.

## 3. Wie verhindert man das?

Man teilt die Daten in mehrere Tabellen auf, zum Beispiel:

**Kundentabelle**

|Kunden-ID|Name|Adresse|
|---|---|---|
|1|Gustav Meier|Zürich|
|2|Beat Merz|Bern|


**Bestellungstabelle**

|Bestell-ID|Kunden-ID|Produkt|
|---|---|---|
|101|1|Laptop|
|102|1|Maus|
|103|2|Tastatur|

Jetzt wird Gustav nur einmal als Kunde gespeichert. Seine Bestellungen werden über die Kunden-ID (den Foreign-Key) mit ihm verknüpft.

Dadurch werden Redundanzen reduziert und die Datenqualität bleibt erhalten.