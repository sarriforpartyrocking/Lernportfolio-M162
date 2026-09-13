*Referenz: [Daten_Formate/Zeichencodierung.md · KES · TBZ-IT-Informatik / modules for students / m162 · GitLab](https://gitlab.com/ch-tbz-it/Stud/m162/-/blob/KES/Daten_Formate/Zeichencodierung.md?ref_type=heads)*
Zeichenkodierung stellt sich die Frage **wie** Daten abgespeichert werden.
Jedes Zeichen wird auf der Festplatte oder im Speicher binär abgespeichert.![[asciibasic.gif]]
Der ASCII-Code benötigt 7 Bit für das Speichern, da mit 7 bit 2^7 (128) Zustände gespeichert werden können.
Hierbei wird das Zeichen 65 (Dec) und "A" gleich repräsentiert (01000001 (hier 1 Byte= 8Bit)).

Aber wie unterscheidet ein Computer zwischen ASCII-Zeichenwert und 64 als numerischen Wert?
Die Bits sind immer gleich. Aber:

- Interpretation als **Integer** → `65`
- Interpretation als **ASCII-Zeichen** → `'A'`

Das Programm bzw. der Datentyp legt also fest, was die Bits bedeuten.
<mark>Bits haben nicht von sich aus eine Bedeutung. Der Kontext bestimmt, wie sie interpretiert werden.</mark>

## 8-Bit Zeichensätze
- ASCII: **7 Bit → 128 Zeichen**
- 8-Bit-Zeichensätze: **8 Bit → 256 Zeichen**
- **ANSI**: Erweiterung von ASCII, v. a. bei Windows/Mac
- Verschiedene Länder → verschiedene **Codepages**
- **ISO/IEC 8859-1 (Latin-1)**: häufig in Europa, enthält z. B. **Umlaute**

## Unicode 
- Ziel: alle Sprachen der Welt in einem Zeichensatz zu vereinen (**Uni**code)
- Anfangs mit 16-Bit codiert; dann auf 32-Bit umgestellt (100'000 verschiedene Zeichen)
- Jedes Zeichen wird mit 4 Byte abgespeichert (4 * 8= 32 Stellen(==UTF-32))

## UTF-8
- am häufigsten verwendeten Kodierung für Unicode-Zeichen
- Speicherplatz kann von einem bis zu vier Byte betragen (die ersten 128 Zeichen entsprechen der ASCII-Tabelle, nachher werden mehr Stellen benötigt)->Häufig verwendete Zeichen benötigen dabei **weniger Bytes/Speicherplatz**, während andere Zeichen mehr Speicherplatz benötigen.
- im Mai 2017 verwendeten 89,0 % aller Websites UTF-8, im März 2018 bereits 91,4 % und im März 2020 95%



