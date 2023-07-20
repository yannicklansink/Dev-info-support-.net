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
Altijd aan het begin
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

### XML Schema (XSD)
Het wordt gebruikt om de structuur en de inhoud van XML-gegevens te beschrijven en te valideren. XML-schema definieert de elementen, attributen en gegevenstypen. Schema-element ondersteunt naamruimten.