#### agenda
daily scrum
code review
conversions
operators
(control structures)
arrays
objecten
functions

### Default value
```js
function doeIets(arg) {
	return (arg ?? 0) * 2;
}
/* 
De nullish coalescing operator (`??`) is een logische operator die de waarde van zijn linker operand teruggeeft als het niet null of undefined is. Anders geeft het de waarde van zijn rechter operand terug.
*/
```

Document Object Model (DOM) heeft properties
HTML heeft attributen

event.preventDefaullt();
Gebruikt voor het submitten van een form.
Gebruik 'submit' en form.

### Conversion
impliciet conversie: vindt automatisch plaats
expliciet conversie: handmatige instructies van de ontwikkelaar om gegevenstypen te converteren

```js
// impliciet
console.log("5" * 2); // 10
console.log(5 + true); // true wordt 1, us 6
console.log("d" * 2); // NaN
console.log("20" == 20); // true

// expliciet
console.log(Number('20') + 18); // 38 (en niet 2038)
Boolean()
String()
BigInt()
```

![[Pasted image 20230530112109.png]]

```js
// object literal
const auto = {
    brand: 'Opel',
    length: 2.5
}

// array literal
const arr = [1,2,3]
```

valueOf() returns het object. Dit kan je overriden met een eigen waarde.

JavaScript calls the `valueOf` method to [convert an object to a primitive value](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#type_coercion). You rarely need to invoke the `valueOf` method yourself; JavaScript automatically invokes it when encountering an object where a primitive value is expected.

### function as class
```js
class Viool {
    aantalSnaren;
    constructor(aantalSnaren) {
        this.aantalSnaren = aantalSnaren;
    }
}

// Zelfde als het schrijven van een class. Syntax van vroeger. Dit noem je een constructor.
// function Viool(aantalSnaren) {
//     this.aantalSnaren = aantalSnaren;
// }
```

### Optionele ketting ?.
```js
const afgiftedatumopgevraagd = passpoort?.afgifteDatum ?? 'n/a';
```
1. Optionele Ketting operator (`?.`): Deze operator stelt je in staat om eigenschappen van een object op te vragen, zelfs als een deel van de ketting mogelijk null of undefined is, zonder dat er een fout optreedt.
2. Nullish Coalescing operator(`??`): Deze operator keert de waarde aan zijn linkerzijde terug als het niet null of undefined is, anders wordt de waarde aan zijn rechterzijde teruggegeven.

### strict mode
elke javascript file begint met 'use strict'
- not a statement, but a literal expression
- The purpose of `"use strict"` is to indicate that the code should be executed in "strict mode"
- With strict mode, you can not, for example, use undeclared variables.
- Strict mode makes it easier to write "zekere" JavaScript.

### variadic  function
```js
// rest argument
function telOp(...args) {
	return args.reduce((prev, elem) => prev + elem, 0) 
}

console.log(telOp(1, 2, 3))
```




