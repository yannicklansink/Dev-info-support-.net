### Agenda
- Reactive programming
- Routing basics
- Internals
- Signals

Reactivity

### Observables:
- soort event listeners? (voor event handeling)
- async operaties
- .subscribe()
- Promises wel standaard beschikbaar.
- Verschil is:
	- promise heeft maar 1 resultaat (asynchroon)
	- observables is een stream van data/resultaten (asynchroon)
- Observables zijn lazy - geen subscribers? Geen werk.
- vergelijkbaar met LINQ

```js
// library: rxjs
// npm i rxys
let source = new rxjs.Observable((resolve, reject) -> {
	console.log("observable start")

	setTimeout(() -> {
		console.log("obeservable klaar")
		subject.next(42);
	}, 2000)
})
let subscription = source
	.pipe(rxjs.operators.map(x -> x * 10)) // transformatie op inkomende stream
	.subscribe(result -> console.log("observable result: ", result))

subscription.unsubscribe();
```

Observables worden gebruikt in Angular bij de:
- eventemitter
- routing params
- httpclient .get()
- forms

3 kinds of subjects:
- Subject
- Behaviorsubject
- Repeatsubject

the idea of using a `BehaviorSubject` (or any Subject) is to hold onto the current value and allow multiple parts of your app to listen for changes to that value. When you want to update the value, you use the `next` method of the Subject to push a new value to it.

### Routing 
SPA => Single Page Application
- 1 pagina
	- geen harde refreshes meer
- Andere pagina's inladen:
	- Alle content wordt met eerste request laden (default angular)
	- Lazy loading => als de gebruiker naar pagina X toegaat, dan je dan bij de server de template voor pagina X ophaalt, op de achtergrond, via javascript.

Routing aan de praat krijgen met Angular:
1. al je routes definieren
2. `<router-outlet></router-outlet>` waar de verschillende content pagina getoond worden
3. Routermodule
4. pagina maken