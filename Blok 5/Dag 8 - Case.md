
### Service:
- Film Service
	- Fetches the data though json api.
	- Singleton: wat het overal in de app injecteerbaar maakt.
	- BehaviorSubject: die bewaren de laatst uitgegeven waarde zodat deze op elk moment kan worden geopend. Dit is handig voor het delen van de status tussen componenten.
	- film$: is een observable, die public is gemaakt zodat componenten zich kunnen abonneren om de laatste status te krijgen. Het zorgt voor immutabiliteit, door een observable te exposeren zijn andere delen van de applicatie niet in staat de interne state te wijzigen.

### Componenten
- Film Overzicht
- Movie Details
- Menu Balk
- Diensten
- Page Not Found

### Pipes
- Date Formatter



### Code explainers:
