Linten: checken of de code format juist is, zodat het niet compileert bij CI.

Add build policy:
[Git branch policies and settings - Azure Repos | Microsoft Learn](https://learn.microsoft.com/en-us/azure/devops/repos/git/branch-policies?view=azure-devops&tabs=browser)Branch policies help teams protect their important branches of development. Policies enforce your team's code quality and change management standards. This article describes how to set and manage branch policies. For an overview of all repository and branch policies and settings, see Git repository settings and policies.

### branches workflow
Long-lived feature branches
- Met een story/branch
- voordeel: niet werkende applicatie op story branch is toegestaan
- nadeel: kans op merge hell

Short-lived feature branches
- Zonder story/branch
- voordeel: geen merge hell
- nadeel: niet werkende applicatie mag niet

### Agile Software Engineering Practices
#### Multidisciplinary teams:
Je moet als teams lid meerder rollen kunnen opnemen en uitvoeren. Een coder moet ook kunnen testen of designs maken. 
Voordeel:
- Als er een teams lid wegvalt, vanwege ziekte, kan een ander teams lid de functie oppakken.
- Betere communicatie door begrip.
- Betere besluiten nemen door verschillende perspectieven.

Wat je wilt vanuit een team lid (T-shaped):
Generatlist:  Breed bekend met IT
Specialist: Specifieke kennis van 1 ding

#### Project Aristotle:
onderzoek bij google, waarom er van heel veel teams, een paar teams de beste zijn. Dus best practices, 5 key dynamics:
- Psychological Safety - veilige omgeving
- Dependability - vertrouwen hebben in je teamleden 
- Structure en Clarity - heel duidelijk doel (en afspraken)
- Meaning - motivatie waar je aan werkt
- Impact - wat je bereikt, herkenning?

