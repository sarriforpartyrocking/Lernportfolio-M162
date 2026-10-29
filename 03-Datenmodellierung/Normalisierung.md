*Referenz: [Datenmodellierung/__Theorie_Normalisierung__.md · main · TBZ-IT-Informatik / modules for students / m162 · GitLab](https://gitlab.com/ch-tbz-it/Stud/m162/-/blob/main/Datenmodellierung/__Theorie_Normalisierung__.md?ref_type=heads)*

# Normalformen
Normalformen geben vor, wie man Daten so in Entitäten trennen kann, dass keine Redundanzen mehr bestehen

### Normalform 1
In der 1NF  darf jedes Attribut pro Tabellenzelle nur einen einzelnen, unteilbaren Wert enthalten.

### Normalform 2
In der 2NF muss jedes Nichtschlüsselattribut vom ganzen Schlüssel abhängen, nicht nur von einem Teil davon. (Einzelne Tabellen pro Entität)
### Normalform 3
In der 3NF hängt jedes Nichtschlüsselattribut direkt vom Schlüssel ab, nicht über ein anderes Nichtschlüsselattribut.