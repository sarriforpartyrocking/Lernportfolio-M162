*Referenz: [Daten_Formate/Datentypen.md · KES · TBZ-IT-Informatik / modules for students / m162 · GitLab](https://gitlab.com/ch-tbz-it/Stud/m162/-/blob/KES/Daten_Formate/Datentypen.md)*


![Datentypen](/Anhaenge/Datentypen.jpg)
<br>
# Primitive Datentypen
| Datentyp                                 | Bezeichnung                                          | Wertebereich                                               | Operationen                                              |
| ---------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- |
| **Ganze Zahlen**                         | `BIGINT`, `INT`, `INTEGER`, `LONG`, `SMALLINT`, …    | Meist 32 Bit: \( -2^{31} \dots 2^{31}-1 \), auch 16/64 Bit | `+`, `-`, `*`, `<`, `>`, `=`, Division mit Rest, Modulo  |
| **Natürliche Zahlen**                    | `BYTE`, `CARDINAL`, `NATURAL`, `UNSIGNED`, `WORD`, … | Meist 32 Bit: \(0 \dots 2^{32}-1\), auch 8/16/64 Bit       | `+`, `-`, `*`, `<`, `>`, `=`, Division mit Rest, Modulo  |
| **Festkommazahlen** (auch Dezimalzahlen) | `DEC`, `DECIMAL`, `NUMERIC`, `CURRENCY`, `COMP-3`, … | Abhängig von der maximalen Stellenanzahl                   | `+`, `-`, `*`, `<`, `>`, `=`, Division mit Rest, Modulo  |
| **Aufzählungstypen**                     | `ENUM`, `SET` oder implizit                          | Frei wählbar, z. B. `SCHWARZ`, `ROT`, `BLAU`, `GELB`       | `<`, `>`, `=`                                            |
| **Boolean**                              | `BOOL`, `BOOLEAN`, `LOGICAL`                         | `TRUE`, `FALSE`                                            | `NOT`, `AND`, `OR`, `XOR`, `NOR`, `NAND`, `=`, `≠`       |
| **Zeichen**                              | `CHAR`, `CHARACTER`                                  | Alle Zeichen eines Zeichensatzes, z. B. Buchstaben         | `<`, `>`, `=`, Konvertierung in `INTEGER`, …             |
| **Gleitkommazahlen**                     | `FLOAT`, `DOUBLE`, `REAL`, `SINGLE`, `HALF`, …       | Verschiedene Definitionen                                  | `+`, `-`, `*`, `/`, `<`, `>`, `=`                        |
| **Zeiger**                               | `POINTER`, `ACCESS`, `IntPtr`, `*`                   | Adresse eines Basistyps                                    | Referenz, Dereferenzierung, teilweise `+`, `-`, `*`, `/` |
| **Konstanter Nullzeiger**                | `NULL`, `VOID`, `None`, `NIL`, `Nothing`             | Kein eigener Wertebereich                                  | `=`                                                      |
## Speicherbedarf von primitiven Datentypen:
| Datentyp  |   Speicherplatz | Typischer Wertebereich           |
| --------- | --------------: | -------------------------------- |
| `boolean` |         1 Byte* | `true` / `false`                 |
| `char`    |         1 Byte* | ein Zeichen                      |
| `byte`    |          1 Byte | 0–255                            |
| `short`   | 2 Byte = 16 Bit | −32'768 bis 32'767               |
| `int`     | 4 Byte = 32 Bit | −2'147'483'648 bis 2'147'483'647 |
| `long`    | 8 Byte = 64 Bit | sehr grosse ganze Zahlen         |
| `float`   | 4 Byte = 32 Bit | Kommazahlen                      |
| `double`  | 8 Byte = 64 Bit | genauere Kommazahlen             |

# Komplexe Datentypen
| Datentyp | Bezeichnung | Wertebereich | Operationen |
|---|---|---|---|
| **Zeichenkette fester Länge** | `Array of CHAR`, `CHAR(n)`, `CHAR[n]` | Alle möglichen Zeichenketten mit fester Länge | Stringfunktionen (Teilstring, Konkatenation), `<`, `>`, `=` |
| **Zeichenkette variabler Länge** | `String`, `Array of CHAR`, `VARCHAR`, `CLOB`, `Text` | Zeichenketten variabler Länge | Stringfunktionen (Teilstring, Länge, Konkatenation), `<`, `>`, `=` |
| **Datum & Zeit** | `DATE`, `TIME`, `DATETIME`, `TIMESTAMP` | Verschiedene Definitionen, z. B. Datum und Uhrzeit | `+`, `-` teilweise möglich, Vergleich mit `=` oder Methoden |
| **Binäre Datenobjekte** | `BLOB`, Bild, Audio, Video, … | Binäre Datenobjekte variabler Länge | Länge, Konkatenation, `=` |
| **Verbund / Struktur** | `RECORD`, `STRUCT`, `CLASS` | Folge verschiedener Komponenten, die unterschiedliche Datentypen haben können | Vergleich, Zuweisung |

# Wie werden Datentypen im Speicher abgelegt?

## Memory Management
Java: 
Die beiden Hauptspeicher sind die beiden *Speichertypen* **Heap** und **Stack**. Stack speichert die einfachen/primitiven Datentypen, während Heap für die zusammengesetzen/komplexen verantwortlich ist. Auf die komplexen Datentypen wird mit einem Pointer aus dem Stack referenziert: 
<br>
![MemoryManagement](/Anhaenge/MemoryManagement.png)

[DatentypenAufgabe](DatentypenAufgabe.md)
