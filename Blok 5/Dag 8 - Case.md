
### Service:
- Film Service
	- Fetches the data though json api.
	- Singleton: wat het overal in de app injecteerbaar maakt.
	- BehaviorSubject: die bewaren de laatst uitgegeven waarde zodat deze op elk moment kan worden geopend. Dit is handig voor het delen van de status tussen componenten.
	- film$: is een observable, die public is gemaakt zodat componenten zich kunnen abonneren om de laatste status te krijgen. Het zorgt voor immutabiliteit, door een observable te exposeren zijn andere delen van de applicatie niet in staat de interne state te wijzigen.

### Componenten
- Film Overzicht
- Movie Details
	- Houdt een film$ observables als variabele. Hier wordt op geabonneerd in de ngOnInt() door het krijgen van de id uit de URL. 
	- Gebruikt een object van key value pairs, waar pairs een string array is. Deze wordt gevuld in de groupTijden methode waarbij de tijden parameter wordt gegroepeerd op date en time. 
- Menu Balk
- Diensten
- Page Not Found
- Reserveren

### Pipes
- Date Formatter



### Code explainers:
```html
<ng-container *ngIf="film$ | async as film">
async pipe abonneerd zich op een film$ observable, zodat wanneer er een nieuwe waarde wordt gepusht deze automatisch wordt geupdate. De 'as film' maakt een template variable.
```

```html
<div *ngFor="let group of groupedTijden | keyvalue">
ngFor loopt door alle groups in groupedTijden.
De keyvalue pipe wordt gebruikt om het object groupedTijden te converteren naar een array van key value pairs.
<ng-container *ngFor="let tijd of group.value; let last = last">
let last = last is beschikbaar door angular waarmee kan worden gekeken of de loop op de laatste item zit in de array.
```