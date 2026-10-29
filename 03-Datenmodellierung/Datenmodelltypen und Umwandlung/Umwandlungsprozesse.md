
## Regeln der Auflösung
Auflösung von Netzwerkförmigen Beziehungen erfolgt mit Hilfe einer Zwischentabelle (Transformations-Entität/assoziative Entität).
Das ist wichtig, da netzwerkförmige Beziehungen nicht in relationalen DBMS implementiert werden können.

Regeln:
1. Die Beziehung der ursprünglichen Entitäten fällt weg.
2. Es wird eine neue Entität hinzugefügt (Transformations-Entität).
3. Es werden neue Beziehungen zwischen den ursprünglichen Entitäten und der neu erstellten Transformationsentität hinzugefügt.
4. Die Kardinalitäten werden verschoben in der Position.

![Aufloesung](Aufloesung.png)
Von der Mitarbeiter-Seite:
Ein Mitarbeiter kann 0 bis unendlich Aufgaben bearbeiten.

Von der Aufgaben-Seite:
Eine Aufgabe muss von mindestens einem Mitarbeiter bearbeitet werden. Es können auch mehrere Mitarbeiter sein, also 1 bis unendlich Mitarbeiter.


- Ein Mitarbeiter hat 0 bis unendlich Einträge in der Tabelle `MitarbeiterAufgabe`.
    
- Eine Aufgabe hat 1 bis unendlich Einträge in der Tabelle `MitarbeiterAufgabe`.


## Umwandlungsprozess V1

Anleitung:
1. Primärschlüssel hinzufügen
2. m(c)-m(c) Beziehung mit Zwischentabelle auflösen
3. Fremdschlüssel hinzufügen
4. Zwischentabelle einen Primärschlüssel geben:
Bei einer Transformationsentität werden die Fremdschlüssel häufig gemeinsam zum Primärschlüssel, damit jede Zuordnung eindeutig identifiziert wird.
5. Attribute hinzufügen
![Umwandlungsprozess-V1](Umwandlungsprozess-V1.png)

## Unterschied zu Umwandlungsprozess V2
- Variante 1: Die Zwischentabelle erhält normalerweise erst nachträglich einen zusammengesetzten PK aus ihren beiden FKs.
    
- Variante 2: Die Zwischentabelle erhält wie jede andere Entität direkt einen eigenen PK, beispielsweise `MitarbeiterAufgabe-ID`.

Bei V1 werden FK1 und FK2 zusammen zum PK!

