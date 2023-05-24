#### Wat we gaan doen vandaag (dit blok?)
Baseline Assessment
Global Language Overview
Types
Conversions (impliciet en expliciet) -> expliciet is zelf opgegeven
Operators
Control Structures
Arrays
Objects
Functions
Destructuring
Classes
Modules

---------------------------------------

typeof('hallo')
return: string

typeof undefined
return: undefined <- is een primitive number

typeof null
return: object

Convert javascript oude code naar nieuwe javascript syntax.
- transpiler(Babel) <- meest gebruikt.
- transpiler is een speciaal soort type compiler

#### Baseline assessment
1. true
2. true
3. false
4. true
5. false
6. '22'
7. error
8. 4.0
9. ?
10. ?
11. ?
12. null
13. ?
14. ?
15. ?


== | let niet op het type
en === | let wel op het type

NaN = Not a Number (date type: number)

Falsey values: undefined, null, NaN, 0, "", false

let ijsco; (type: undefined)

statically typed: C#, java
	variable is bekend bij het compileren
dynamically typed: Python, JS
	variable is bekend bij pas bij runtime en worden pas daar bepaalt.
	kunnen op elk moment wijzigen

#### functions
```js
// function expression (anonymous)
let plus = function (a, b) {
	return a + b;
}

// untyped
function add (a, b) {
	return a + b;
}
```

#### arrays
```js
// untyped
let a = [1, true, 'long'];

// extensible
let first = a[0];
a.title = 'list';
a[3] - 'last';
```

#### classes
```js
class MagicCalculator {
	magicMultiplier = 3.14;

	calculate() {
		
	}
}

// annonymous classes.
let Component = class { /*  */ }

// operators
let x = 2
x ? 2 : 3 -> ternary operator

```

#### Built-in types
![[Pasted image 20230524132029.png]]

shift + alt + up/down | duplicate line