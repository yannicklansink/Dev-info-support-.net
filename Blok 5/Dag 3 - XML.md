### XML betekenis
Met Extensible Markup Language (XML) kunt u gegevens op een deelbare manier definiëren en opslaan. XML ondersteunt informatie-uitwisseling tussen computersystemen zoals websites, databases en toepassingen van derden.

Elementen:
Herkenbaar aan tags
```xml
<title>Professional XML</title>
```

Attributen:
```xml
<author fname="Yannick" />
```

XML declaratie
Altijd aan het begin van een document.
```xml
Kan ook version 1.1, maar 1.0 wordt meest gebruikt.
<?xml version="1.0"?> 
```

Processing instruction
Voor de processor om het document to processen.
```xml
<?MyPackageInformation Dit boek moet wel ingebonden zijn?>
```

Character data
Geef je aan dat het character data is aan processor
```xml
<title><![CDATA[22 > 20 & this is how we excape character data]]</title>
```

Regels:
- top level element moet precies 1 element zijn.
- file moet beginnen met <?xml version="1.0"?>
- elk element moet omgeven zijn door <>
- attribute moet uniek zijn in het element
- attribute moet een waarde hebben en tussen "" staan.
- mag geen < en & in tags gebruiken
- XML is case sensitive

Encoding in XML betekent
- de character set -> geeft aan welke character je mag gebruiken "UTF-8", "UTF-16"...
- encoding -> 



### XML Schema (XSD)
Het wordt gebruikt om de structuur en de inhoud van XML-gegevens te beschrijven en te valideren. XML-schema definieert de elementen, attributen en gegevenstypen. Schema-element ondersteunt naamruimten.