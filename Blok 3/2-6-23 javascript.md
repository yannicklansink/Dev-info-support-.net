```js
console.log('ik wordt geprint');
let log = console.log;
log('hello')
```

### Mysterien rondom 'this'
'this' kan alleen binnen een functie gebruikt worden. 

```js
function chat() {
	console.log('Aan het chatttttten')
	console.log(this); // -> global object nodejs
	console.log(this); // -> kan ook window zijn in browser
}
```

### ES Modules
Een indeling van JavaScript-modules die de officiële standaardindeling is om JavaScript-code te verpakken voor hergebruik

module bundlers:
- rollup.js
- Vite
- webpack
- parcel

deze maken van alle lose files naar 1 gecomplieerd file
dit is beter voor:
- performance
- betere development proces
- quality checks
- functional purposes


