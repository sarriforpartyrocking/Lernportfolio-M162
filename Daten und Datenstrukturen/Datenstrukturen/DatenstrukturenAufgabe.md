#### Fragestellung 1

Sie müssen eine Adressliste verwalten mit mehreren 100 Datensätzen. Welche Strukturen kommen in Frage und warum?

Ein Datensatz/Record/Tupel würde Sinn machen, da man mehrere zusammengehörige Werte darin speichern kann, die unterschiedliche Datentypen enthalten können (z.B. Strassenname = String,  Hausnummer = int etc.). Diese Tupels könnte man nun in einem Array speichern, da Tupels den gleichen Datentyp haben.

Möglich wäre auch eine verkettete Liste, man müsste zwar durch alle gespeicherten Werte durch iterieren, um den gesuchten Wert zu finden, was sehr lange dauern würde, aber möglich wäre.
#### Fragestellung 2

Sie müssen viele Werte speichern und mit wenig Zeitverlust darauf zugreifen können. Welche Strukturen kommen in Frage und warum?

Ein Baum wäre eine gute Wahl, da dort nicht alles abgesucht werden muss um einen bestimmten Wert zu finden.

#### Fragestellung 3

Sie müssen einen Sortieralgorithmus für Zahlen programmieren. Welche Strukturen kommen in Frage und warum?

Für einen Sortieralgorithmus kommen insbesondere Arrays bzw. Listen infrage. Sie ermöglichen den Zugriff auf mehrere Elemente, sodass diese miteinander verglichen und vertauscht werden können. Auch ein Keller wäre grundsätzlich möglich, ist aber aufgrund des LIFO-Prinzips weniger flexibel, da nur auf das oberste Element direkt zugegriffen werden kann.

#### Fragestellung 4

Die Universität Zürich hatte in jedem Semester das Problem, dass ihre Server überlastet waren während der Modulregistrierung in neuen Semestern. Jeder Student wollte so schnell als möglich einen Platz für spezifische Vorlesungen reservieren, weil die Plätze jeweils limitiert sind. Dabei mussten die offenen Modulregistrierungs-Anfragen geschickt gespeichert werden.

Mit welcher Struktur kann man dieses Problem lösen (und wurde so auch gelöst)

Die Struktur Warteschlange würde sich eignen, da sie nach dem FIFO-Prinzip agiert. Heisst damit der Server nicht überlastet wird, können so viele Schüler ins Portal wie Platz ist und wenn ein Schüler die Website verlässt, kann ein neuer hinein.