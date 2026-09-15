*Referenz: [Daten_Formate/Json.md · KES · TBZ-IT-Informatik / modules for students / m162 · GitLab](https://gitlab.com/ch-tbz-it/Stud/m162/-/blob/KES/Daten_Formate/Json.md)*


(JavaScript Object Notation)
- Easy to Read/Write
- API's and Configs
- Integrates Easily With Most Languages

## JSON Types
- Strings
- Numbers
- Booleans
- null
- Arrays
- Objects {"key" : "value"} {"age" : 30}

## Notation
{
	"key" : "value",
	 "key": "value"
}

## Ein Element
```
{
  "name": "Max",
  "alter": 16,
  "schueler": true,
  "note": 5.5,
  "hobbys": ["Fussball", "Gaming", "Musik"],
  "adresse": {
    "strasse": "Bahnhofstrasse 10",
    "stadt": "Zürich"
  }
}
```

## Mehrere Elemente
```
{
  "personen": [
    {
      "name": "Max",
      "alter": 16,
      "adresse": {
        "strasse": "Bahnhofstrasse 10",
        "stadt": "Zürich"
      }
    },
    {
      "name": "Anna",
      "alter": 17,
      "adresse": {
        "strasse": "Hauptstrasse 5",
        "stadt": "Bern"
      }
    }
  ]
}

Merke:
`[]` = mehrere Personen  
`{}` = eine Person bzw. ein Objekt

```
[AuftragJSONSteckbrief](AuftragJSONSteckbrief.md)
[AuftragJSONAdressdatenInterpretieren](AuftragJSONAdressdatenInterpretieren.md)

