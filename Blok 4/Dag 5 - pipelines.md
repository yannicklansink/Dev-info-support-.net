azure-pipelines.yml
[YAML schema reference | Microsoft Learn](https://learn.microsoft.com/en-us/azure/devops/pipelines/yaml-schema/?view=azure-pipelines)
```yml
  #comment!
services:
 - app: admin-console
  port: 7000
  versions:
  - 1.4
  - 1.7
  deployed: false
```

- Pipeline
    - Stage A
        - Job 1
            - Step 1.1
            - Step 1.2
            - ...
        - Job 2
            - Step 2.1
            - Step 2.2
            - ...
    - Stage B
        - ...

### Pipelines:
Pipelines combineert continue integratie (CI) en continue levering (CD) om code te testen, bouwen en te leveren.

- Voor automatisering
- Voor software compileren
- Voor testen runnen

Trigger -> Pipeline -> Stage -> Steps

### Pipeline Variables
- Met variabelen kan je belangrijke gegevens in verschillende delen van de pipeline plaatsen. 
- Het meest gebruikelijke gebruik van een variabele is het definiëren van een waarde die in een pijplijn kan worden gebruikt. 
- Alle variabelen worden opgeslagen als tekenreeksen en kunnen tijdens runtime worden gewijzigd.
- Niet helemaal veilig

Artifact: 
Gecompileerde code

### Yaml
YAML is a data serialization language
- xml
- json

YAML Ain't Markup Language
- not intended to be a markup language for document markup



