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
- Promises wel standaard beschikbaar

```js
// library: rxjs
// npm i rxys
let source = new Observable((resolve, reject) -> {
	console.log("observable start")

	setTimeout(() -> {
		console.log("obeservable klaar")
		subject.next(42);
	}, 2000)
})
source.subscribe(result -> console.log("observable result: ", result))
```

