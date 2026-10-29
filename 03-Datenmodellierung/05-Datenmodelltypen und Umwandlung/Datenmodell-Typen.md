Es gibt drei Typen von Datenmodellen:

## Konzeptionelles Datenmodell
Das konzeptionelle Datenmodell beschreibt, welche Daten in einem System vorkommen und wie diese miteinander zusammenhängen.

- Entitäten ohne Attribute

![Konzeptionelles-Datenmodell|269](Anhaenge/Konzeptionelles-Datenmodell.png)


## Logisches Datenmodell
Das logische Datenmodell beschreibt, wie die Daten strukturiert werden, damit sie in einer Datenbank abgebildet werden können. Es baut auf dem konzeptionellen Datenmodell auf.

- Attribute sind definiert 
- m(c)-m(c)-Beziehungen werden in der Regel durch eine zusätzliche Zwischentabelle aufgelöst. Beispiel: Mehrere Studenten besuchen mehrere Kurse. Dafür erstellt man eine Tabelle `Teilnahme`, die Studenten und Kurse miteinander verbindet. ->[Umwandlungsprozesse](Umwandlungsprozesse.md)
- Datentypen *können* definiert sein

![Logisches-Datenmodell](Anhaenge/Logisches-Datenmodell.png)

 [Vom logischen zum physischen Modell](VonLogischzuPhysisch.md)
## Physisches Datenmodell
Das physische Modell enthält alle Details, die für die Umsetzung auf einem spezifischen DBMS(Datenbank Management System) notwendig sind.

- Alle Regeln eines logischen Schemas werden eingehalten.
- Datentypen und andere Eigenschaften eines spezifischen DBMS werden konkret verwendet.
- Verwenden Sie ein DBMS spezifisches Tool (SQL-Workbench)

![Physisches-Datenmodell](Anhaenge/Physisches-Datenmodell.png)