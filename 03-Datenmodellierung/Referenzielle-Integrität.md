Referenzielle Integrität bedeutet in der Datenmodellierung, dass Beziehungen zwischen Tabellen korrekt und konsistent bleiben. Das wird durch Fremdschlüssel (Foreign Keys) sichergestellt, die auf einen existierenden Datensatz in einer anderen Tabelle verweisen müssen.

Beispiel:

- Tabelle Kunde: Enthält alle Kunden mit einer eindeutigen `KundenID`.
- Tabelle Bestellung: Enthält Bestellungen mit einer `KundenID` als Fremdschlüssel.

Wenn eine Bestellung die `KundenID = 5` enthält, muss in der Tabelle `Kunde` ein Kunde mit dieser ID existieren. Andernfalls wird die referenzielle Integrität verletzt.

Merksatz: Referenzielle Integrität stellt sicher, dass Fremdschlüssel immer auf gültige Datensätze verweisen und keine ungültigen Beziehungen zwischen Tabellen entstehen.