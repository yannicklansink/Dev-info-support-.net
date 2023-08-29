Componenten:
- Film overzicht
- Menubalk
	- Films overzicht
	- Diensten
- Film details (MovieDetailsComponent)
- Film vertoningen (komt op film details pagina)

### Service:
- Film Service
	- Fetches the data though json api.
	- Singleton: wat het overal in de app injecteerbaar maakt.
	- BehaviorSubject: die bewaren de laatst uitgegeven waarde zodat deze op elk moment kan worden geopend. Dit is handig voor het delen van de status tussen componenten.
	- film$: is een observable, die public is gemaakt zodat componenten zich kunnen abonneren om de laatste status te krijgen.