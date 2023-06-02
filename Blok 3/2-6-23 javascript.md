```js
console.log('ik wordt geprint');
let log = console.log;
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



