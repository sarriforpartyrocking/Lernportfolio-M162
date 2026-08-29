Objekte zur Speicherung und Organisation von Daten werden "Datenstruktur" genannt, da sie dafür verantwortlich sind, Daten anzuordnen und zu verknüpfen. Dabei Unterscheidet man zwischen Strukturierten und Unstrukturierten Daten

# Strukturierte Daten
Strukturierte Daten folgen einem **vordefinierten Schema**, das die Organisation in **Zeilen und Spalten** festlegt. Jede Spalte repräsentiert ein Attribut (z. B. Name, Adresse, Telefonnummer), und jede Zeile einen einzelnen Datensatz. Sie sind **quantitativ (zählbar und messbar) und standardisiert (nach einheitlichen und festgelegten Regeln )**, wodurch Computer und Menschen sie effizient verarbeiten können. Typische Merkmale sind:

- Einheitliche Attribute für alle Datensätze
- Einhaltung eines festen Formats oder Datenmodells
- Leichte Speicherung in **relationalen Datenbanken** oder **Data Warehouses**
- Effiziente Abfrage und Analyse mit **SQL** oder anderen Datenbanktools

## Merkmale
- Sie sind vollständig sortiert oder sortierbar.
- Sie können nach mehreren Kriterien sortiert werden.
- Das Suchen nach einem sortierten Kriterium ist einfach und schnell.
- Das Einfügen von Daten ist aufwändig, da die passende Stelle gesucht werden muss.


# Unstrukturierte Daten
Unstrukturierte Daten folgen **keinem vordefinierten Schema**, das ihre Organisation in Zeilen und Spalten festlegt. Sie besitzen keine einheitliche Struktur und können in unterschiedlichen Formaten vorliegen, beispielsweise als Texte, Bilder, Videos, Audiodateien oder Dokumente. Die enthaltenen Informationen sind häufig **qualitativ (beschreibend und nicht direkt zählbar) und nicht standardisiert (ohne einheitlich festgelegte Regeln)**, wodurch ihre Verarbeitung und Analyse für Computer aufwendiger sein kann. Typische Merkmale sind:

- Keine einheitlichen Attribute oder feste Struktur für alle Daten
- Unterschiedliche Formate und Inhalte
- Speicherung beispielsweise in **Dateisystemen, Cloud-Speichern oder Data Lakes**
- Analyse häufig mithilfe von **KI, Machine Learning oder Text- und Bildverarbeitung**

## Merkmale
- Sie sind nicht sortiert.
- Das Suchen nach sortierten Werten ist aufwändig.
- Das Einfügen von Daten geht einfach und ist fast überall möglich.

## Strukturierung von unstrukturierten Daten 
### Textanalyse und Textmining
Textmining analysiert grosse Mengen an Text, erkennt darin relevante **Begriffe und Zusammenhänge** und macht diese für weitere Analysen nutzbar.
### Maschinelles Lernen
Maschinelles Lernen ist besonders bei großen Datenmengen effektiv, erfordert jedoch geeignete **Trainingsdaten, Training und Überwachung** und ist nicht für jede Anwendung geeignet.

### Linguistisches Verfahren
Ein **linguistisches Verfahren** versucht, anhand von **sprachlichen Regeln und dem Kontext** herauszufinden, welche Bedeutung gemeint ist. Dieses Verfahren verhindert Ambiguität und ist schneller als das maschinelle Lernen

# Organisation von Daten
Die Art wie Informationen sortiert sind und wie auf sie zugegriffen werden kann

### Strukturierungsgrad von Daten
**Textdaten**; unstrukturierte Daten; keine Einschränkungen an die Struktur; beschränkte Auswertemöglichkeiten
**Tabellendaten**; mässig strukturiert; Typ: entweder Text oder Zahl; Gut geeignet für Analysen und Vergleiche
**Datenbanken**; stark strukturierte Daten; bestehen aus zwei bis vielen hundert Tabellen in Form von Datensätzen; Daten in einzelnen Tabellen sind stark abhängig voneinander; sehr gute Auswertungsmöglichkeiten

