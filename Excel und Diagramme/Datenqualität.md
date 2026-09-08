## Ursachen für schlechte Datenqualität

- Probleme liegen meist in der Daten**erfassung**
#### konkrete Probleme:

- unzureichend strukturierte Eingabemasken: Je mehr Freiraum bei der Eingabe der Daten, desto unterschiedlicher ist die Erfassung der Daten (hängt vom User ab)
	- **Ergebnis**: unstrukturierte Daten, die inkonsistent gepfelgt werden
	- Werden mehr Felder angeboten, dann steigt die Daten**qualität** und die Daten**konsistenz**

- unterschiedliche Interpretation derselben Felder
	- **Ergebnis**: inkonsistente Daten trotz gleicher Erfassungsmaske
	-  *e.g.: Das Feld "Kunde" ist für jeden Mitarbeiter unterschiedlich*

- Zusammenführung von Daten aus unterschiedlichen Datenquellen
	- **Ergebnis**: bei unsauberer Arbeit: Redundanzen, Widersprüchlichkeiten und Inkonsistenzen entstehen, doppelte Kundeneinträge und widersprüchliche Informationen
	- *e.g.: Daten werden aus zwei Systemen zusammengeführt und in einem heisst eine Person "Hans Muster" und im anderen "H. Muster", das System erkennt ihn nicht als dieselbe Person

- Deklarierung von Feldern als "optional"
	- *Ergebnis*: unvollständige Datensätze, fehlende Daten -> nicht unbedingt schlecht, aber führ zu unterschiedlichen Datensätzen, was die Vollständigkeit beeinträchtigt


#### Merkmale:

- **Vollständigkeit** beschreibt, ob **alle** für einen bestimmten Zweck erforderlichen Daten vorhanden sind. Fehlende Informationen, beispielsweise eine nicht erfasste E-Mail-Adresse oder Postleitzahl, führen zu einer **eingeschränkten Nutzbarkeit** der Daten.

- **Eindeutigkeit** bedeutet, dass jeder reale Sachverhalt oder jedes Objekt **genau einmal** und **eindeutig identifizierbar** ist. Ein Kunde sollte beispielsweise nur **einmal im System existieren** und nicht unter mehreren leicht abweichenden Namen erfasst werden.

- **Redundanz** liegt vor, wenn dieselben Informationen **mehrfach gespeichert** werden. Redundante Daten entstehen häufig durch **fehlende Eindeutigkeit**, etwa wenn ein Kunde versehentlich mehrfach angelegt wird.

- **Widersprüchlichkeit** bezeichnet den Fall, dass **unterschiedliche Datensätze oder Datenquellen** voneinander abweichende Informationen zum gleichen Sachverhalt enthalten. Beispielsweise ist für denselben Kunden in einem System die Adresse „Bahnhofstrasse 10“ und in einem anderen „Bahnhofstrasse 12“ hinterlegt.

Ursache-Wirkung-Beziehung zwischen diesen Begriffen

Eine hohe Datenqualität setzt voraus, dass Daten vollständig, eindeutig und konsistent verwaltet werden und unnötige Redundanzen vermieden werden.


### Bereinigung von Daten
Ziel der Datenbereinigung ist es, fehlerhafte, unvollständige, widersprüchliche oder redundante Daten systematisch zu identifizieren und zu korrigieren.

- Dubletten werden zusammengeführt
- fehlende Werte werden ergänzt
- fehlerhafte Einträge berichtigt
- uneinheitliche Schreibweisen vereinheitlicht
- alte/nicht mehr benötigte Datensätze werden entfernt

Excel hat manuelle Datenbereinigungstools unter dem Reiter "Daten" und unter Start: Bedingte Formatierung kann man Regeln für die Datensätze festlegen


