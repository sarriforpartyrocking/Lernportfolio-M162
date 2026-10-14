*Referenz: [Datenmodellierung/Theorie_Datenmodellierung.md · KES · TBZ-IT-Informatik / modules for students / m162 · GitLab](https://gitlab.com/ch-tbz-it/Stud/m162/-/blob/KES/Datenmodellierung/Theorie_Datenmodellierung.md)*

Assoziationen bestehen aus Kardinalitäten und Bezeichnungen:

## Kardinalität und Bezeichnung
### Kardinalität
**Kardinalität**: Mengenangabe, die sagt wie viele Entitäten es in der Beziehung gibt:
	- Beispiel: Es kann **m viele** Mitarbeiter in **einer** Abteilung geben: 
	![Kardinalität|474](/Anhaenge/Kardinalität.png)
	

### Bezeichnungen
**Bezeichnungen**: Zeigt, wie man die Beziehung deuten muss; je nach Bezeichnung ändern sich die Kardinalitäten:
	- Beispiel: Viele Mitarbeiter **arbeiten für** eine Abteilung; die Bezeichnung könnte aber auch sein: Viele Mitarbeiter **sind** einer Abteilung **zugewiesen**:
	- 
	![Bezeichnung|491](/Anhaenge/Bezeichnung.png)


## Die vier Beziehungstypen
| Abkürzung | Erklärung                                                      |
| --------- | -------------------------------------------------------------- |
| 1         | Genau ein Datensatz                                            |
| c         | Kein oder genau ein Datensatz                                  |
| m         | Mindestens ein Datensatz. Kann auch unendlich viele haben.     |
| mc        | Beliebig viele Datensätze. Also kein, ein oder unendlich viele |
### Kombinationen der Beziehungstypen

![Beziehungstypen-Kombinationen](/Anhaenge/Beziehungstypen-Kombinationen.png)
#### Die drei Beziehungstypen in der Abbildung

##### 1. Hierarchische Beziehungen – dunkelgrau

C = konditionell, weil die Beziehung nicht zwingend bestehen muss – sie kann also auch 0 sein.

Sie beschreiben eine Über- und Unterordnung. Eine Einheit ist beispielsweise einer anderen unterstellt.

Beispiel: Abteilungsleiter → Mitarbeiter.

In der Matrix sind diejenigen Felder, die eine 1 enthalten, hierarchisch zu verstehen. Wenn es von einer Entität nur eine Instanz gibt, steht diese hierarchisch über den anderen Entitäten. Beispielsweise gibt es Mitarbeiter, wobei es unwichtig ist, wie viele es sind. Ohne die übergeordnete Entität können diese Mitarbeiter jedoch nicht existieren.


##### 2. Konditionelle Beziehungen – hellgrau

Sie beschreiben Beziehungen, die von bestimmten Bedingungen abhängig sind.

Beispiel: Ein Mitarbeiter wird einer Abteilung nur zugeteilt, wenn eine bestimmte Voraussetzung erfüllt ist.

In der Matrix sind diejenigen Felder, die eine konditionelle Beziehung darstellen, von einer bestimmten Bedingung abhängig. Das bedeutet, dass eine Entität nur dann existiert oder relevant ist, wenn eine bestimmte Voraussetzung erfüllt ist. Ist diese Bedingung nicht erfüllt, besteht die Beziehung zwischen den Entitäten nicht.

**Beispiel**: Ein Mitarbeiter erhält nur dann einen Firmenwagen, wenn seine Position im Unternehmen dies voraussetzt. Die Beziehung zwischen dem Mitarbeiter und dem Firmenwagen ist somit konditionell, da sie nur unter einer bestimmten Bedingung besteht.


##### 3. Netzwerkförmige Beziehungen – weiss

Sie beschreiben Verbindungen und Zusammenarbeit ohne zwingende Über- oder Unterordnung.

In der Matrix sind diejenigen Felder, die eine netzwerkförmige Beziehung darstellen, dadurch gekennzeichnet, dass eine Entität mit mehreren anderen Entitäten verbunden sein kann. Dabei können die Entitäten untereinander in unterschiedlichen Beziehungen stehen, sodass ein Netzwerk entsteht.

**Beispiel**: Ein Mitarbeiter kann an mehreren Projekten arbeiten, und an jedem Projekt können mehrere Mitarbeiter beteiligt sein. Dadurch entsteht eine netzwerkförmige Beziehung zwischen Mitarbeitern und Projekten.

