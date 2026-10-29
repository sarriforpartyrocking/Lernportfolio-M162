
# KI generierte Zusammenfassung:

## 1. Ziel

Das logische Entity-Relationship-Diagramm (ERD) wird in ein physisches Datenmodell überführt. Dabei wird festgelegt, wie die Daten konkret in einer relationalen Datenbank gespeichert werden.

## 2. Unterschiede zwischen logischem und physischem Datenmodell

|Logisches Datenmodell|Physisches Datenmodell|
|---|---|
|Beschreibt Entitäten und Beziehungen|Beschreibt konkrete Tabellen und Spalten|
|Definiert Attribute|Definiert Datentypen|
|Legt Primär- und Fremdschlüssel logisch fest|Setzt Schlüssel in der Datenbank um|
|Unabhängig vom konkreten Datenbanksystem|Auf ein Datenbanksystem abgestimmt|

## 3. Schritte der Umwandlung

1. **Entitäten in Tabellen umwandeln:** Jede Entität wird zu einer Tabelle.
    
2. **Attribute in Spalten umwandeln:** Die Attribute einer Entität werden zu Spalten.
    
3. **Primärschlüssel definieren:** Jede Tabelle erhält einen Primärschlüssel (PK), der jeden Datensatz eindeutig identifiziert.
    
4. **Beziehungen umsetzen:** Beziehungen werden mithilfe von Fremdschlüsseln (FK) oder zusätzlichen Tabellen umgesetzt.
    
5. **Datentypen festlegen:** Für jede Spalte wird ein geeigneter Datentyp definiert.
    
6. **Integritätsregeln festlegen:** `NOT NULL`, `UNIQUE` und `CHECK` sichern die Gültigkeit der Daten.
    
7. **Redundanzen prüfen:** Die Tabellenstruktur wird auf unnötige doppelte Daten überprüft.
    

## 4. Umsetzung der Kardinalitäten

- **1:1 (eins zu eins):** Ein Fremdschlüssel mit einer `UNIQUE`-Bedingung stellt sicher, dass jeder Datensatz höchstens einem anderen Datensatz zugeordnet ist.
    
- **1 (eins zu viele):** Der Fremdschlüssel wird auf der n-Seite gespeichert.
    
- **n (viele zu viele):** Eine zusätzliche Zwischentabelle verbindet die beiden Tabellen. Sie enthält normalerweise die Fremdschlüssel beider Tabellen.