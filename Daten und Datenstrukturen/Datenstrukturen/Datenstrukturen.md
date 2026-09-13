# Datenstrukturen
*Referenz:[Daten_Formate/StrukturierteDaten.md · KES · TBZ-IT-Informatik / modules for students / m162 · GitLab](https://gitlab.com/ch-tbz-it/Stud/m162/-/blob/KES/Daten_Formate/StrukturierteDaten.md?ref_type=heads)*

Datenstrukturen bestimmen, **wie Daten organisiert, gespeichert und verarbeitet werden**.

## Datensatz / Record / Tupel

- Enthält **mehrere zusammengehörige Werte**
- Werte können **unterschiedliche Datentypen** haben
- Feste Anzahl und Reihenfolge
- Beispiel: `(ID=12, Name=Hans, Alter=20)`
- Entspricht ungefähr **einer Zeile in einer Tabelle**


Der kleine Unterschied liegt eher in der **Bezeichnung und im Kontext**:

- **Tupel** → mathematisch/fachsprachlich in relationalen Datenbanken
- **Datensatz** → deutscher allgemeiner Begriff
- **Record** → englischer Begriff


![Datensatz](/Anhaenge/Datensatz.png)


Alle drei können eine **Zeile mit zusammengehörigen Attributwerten** meinen.

> **Tupel = Datensatz = Record = eine Zeile einer Relation (Tabelle).**


## Array

- Speichert **mehrere Werte** vom **gleichen Datentyp**
- Zugriff über einen **Index**
- Kann mehrdimensional sein
- Beispiel: `[12, 45, 23, 38]`
- **Assoziatives Array (Dictionary):** Zugriff über einen Schlüssel statt über einen numerischen Index

## Verkettete Liste

- Speichert **beliebig viele Elemente** mit unterschiedlichem Datentyp
- Es muss keine Grösse von Beginn an definiert werden
- Jedes Element enthält einen **Verweis auf das nächste Element**
- Elemente können einfach eingefügt oder gelöscht werden
- Beispiel: Musik-Playlist
- **Analogie:** Zug mit verbundenen Wagen
- Der Knoten kennt **nur** seinen Nachfolger, der letzte Zeiger hat den "Nullzeiger", da dieser auf nichts zeigt

![VerketteteListe](/Anhaenge/VerketteteListe.png)

**Suchen**: Durch Liste hindurch iterieren (dauert lange)
**Einfügen**: Element wird eingeschoben und Zeiger vom Vorgänger zeigt nun auf das neue Element; der Zeiger des neuen Element widerum auf das nächste
Wird ein Element am Schluss eingefügt, so wird der Nullzeiger des Vorgängers jetzt zum normalen Zeiger und der Zeiger vom Element wird zum Nullzeiger
**Löschen**: Zeiger vom Vorgänger zeigt nun auf das Element des nächsten Elements (Abbildung: Zeiger von 2 zeigt nun auf 4)
Wird das Element am Schluss gelöscht so wird der Zeiger des Vorgängers zum Nullzeiger (Abbildung: 4 hat nun den Nullzeiger).
## Stack / Stapelspeicher / Kellerspeicher

- Prinzip: **LIFO** (*Last In, First Out*)
- Das zuletzt eingefügte Element wird zuerst entfernt
- `push` → Element hinzufügen
- `pop` → oberstes Element entfernen
- `peek/top` → oberstes Element anschauen
- **Analogie:** Metro; der letzte der einsteigt, ist der erste der aussteigt

## Queue / Warteschlange

- Prinzip: **FIFO** (*First In, First Out*)
- Das zuerst eingefügte Element wird zuerst entfernt
- `enqueue` → Element hinzufügen
- `dequeue` → erstes Element entfernen
- **Analogie:** Warteschlange

![Queue](/Anhaenge/Queue.png)

## Priority Queue / Vorrangwarteschlange

- Elemente besitzen eine **Priorität**
- Höchste Priorität wird zuerst verarbeitet
- Reihenfolge ist daher **nicht unbedingt FIFO**
- Wird häufig mit **Heaps** umgesetzt
- **Analogie:** VIP-Warteschlange
- Dequeue liefert das Objekt mit der höchsten priorität


![Vorrangwarteschlange](/Anhaenge/Vorrangwarteschlange.png)
## Graph

- Besteht aus **Knoten und Verbindungen**
- Ein Knoten kann mit **mehreren anderen Knoten** verbunden sein
- Verbindungen können ein- oder zweiseitig sein
- Beispiel: GPS / Strassennetz

![Graph](/Anhaenge/Graph.png)

## Baum

- **Spezielle Form eines Graphen**
- Knoten besitzen **eingehende** Verbindungen zu weiteren Knoten
- Ein Knoten kann mehrere **Kinder** haben
- **Binärbaum:** maximal 2 Kinder pro Knoten
- Suchbäume ermöglichen **schnelles Finden von Elementen**, da nicht alles abgesucht werden muss.
- Gesuchtes Element in linker oder rechter Hälfte; Suchoperationen können reduziert werden
- Das letzte Element wird Blatt genannt

## Heap

- Baumstruktur für **Prioritätswarteschlangen**
- Spezieller Baum
- Wichtig: `insert`, `remove`, `extractMin`
- Ermöglicht schnelles Finden des Elements mit der höchsten/niedrigsten Priorität

![Heap](/Anhaenge/Heap.png)

## Hashtabelle

- Speicherposition wird direkt über einen **Hashwert berechnet**
- Dadurch ist **sehr schnelles Suchen** möglich
- Wird häufig für **Schlüssel-Wert-Paare** verwendet
- **Hash-Kollision:** Zwei verschiedene Daten erzeugen **denselben Hashwert** und würden somit auf dieselbe Speicherposition zeigen. (Lösung: anderen Speicherplatz finden oder mehrere Werte an einem Platz verwalten. )
- Beispiel: `Name → Telefonnummer`

![Hashtabelle](/Anhaenge/Hashtabelle.png)

[DatenstrukturenAufgabe](DatenstrukturenAufgabe.md)
