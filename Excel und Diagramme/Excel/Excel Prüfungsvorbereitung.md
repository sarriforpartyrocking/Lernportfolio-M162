### Power Query öffnen
Tabelle anklicken; Abfrage; Bearbeiten; Power Query Editor öffnet sich

### Duplikate entfernen
"Zeilen entfernen"; "Duplikate entfernen"
Hinweis: Um Duplikate, die bei allen Spalten übereinstimmen zu löschen, muss man auch alle Spalten anklicken!

### Kategorien vereinheitlichen
"Werte ersetzen"; zu suchenden Wert eingeben

### Datentyp festlegen
"Datentyp festlegen" anklicken und für jede Spalte auswählen welcher Datentyp sich darin befindet

---

### Tabelle benennen
"Eigenschaften"

### Leere Zellen markieren
"Start" ; "Bedingte Formatierung"


---
### Wichtige Operatoren

`SUMME(Bereich)`  
→ Addiert alle Zahlen im angegebenen Bereich.  
Beispiel: `=SUMME(E2:E10)`

`MITTELWERT(Bereich)`  
→ Berechnet den Durchschnitt.  
Beispiel: `=MITTELWERT(E2:E10)`

`MIN(Bereich)`  
→ Gibt den kleinsten Wert zurück.  
Beispiel: `=MIN(E2:E10)`

`MAX(Bereich)`  
→ Gibt den grössten Wert zurück.  
Beispiel: `=MAX(E2:E10)`

### Bedingte Funktionen

`WENN(Bedingung;Dann;Sonst)`  
→ Prüft eine Bedingung und gibt abhängig davon einen Wert zurück.  
Beispiel: `=WENN(E2>10000;"hoch";"tief")`

`SUMMEWENN(Bereich;Kriterium;Summenbereich)`  
→ Addiert nur Werte, bei denen eine Bedingung erfüllt ist.  
Beispiel: `=SUMMEWENN(C2:C17;"Jaspreet";E2:E17)`

→ Sucht **Jaspreet** in Spalte C und addiert die passenden Werte aus Spalte E.

`ZÄHLENWENN(Bereich;Kriterium)`  
→ Zählt, wie oft eine Bedingung erfüllt ist.  
Beispiel: `=ZÄHLENWENN(C2:C17;"Jaspreet")`

→ Zählt, wie oft **Jaspreet** vorkommt.

### Logische Funktionen

`UND(Bedingung1;Bedingung2)`  
→ **Alle** Bedingungen müssen wahr sein.

Beispiel:  
`=WENN(UND(E2>10000;F2>3000);"Erfolg";"")`

`ODER(Bedingung1;Bedingung2)`  
→ **Mindestens eine** Bedingung muss wahr sein.

Beispiel:  
`=WENN(ODER(C2="Jaspreet";C2="Charley");E2+F2;"")`