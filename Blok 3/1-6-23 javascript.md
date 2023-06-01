
spread operator on objects
```js
// copy van person 
const obj1 = {...person, taal: 'Mandarijn'} 

let product = {
	id: 2,
	titel: 'wasmand',
}
// muterende code
product.titel = 'wasmandjes'; 

// niet-muterende code. beter voor frameworks
product = {...product, titel: 'wasmandjes2'};


```

### set- and getters
```js
let watch = {
    model: 'ABC123',      
    color: 'silver',      
    get fullName() {
        return `${this.model} in the color: ${this.color}`
    },
    set fullName(value) {
        let parts = value.split(" in the color: ");
        this.model = parts[0];
        this.color = parts[1];
    },
    toString: function() {
        return `Watch Model: ${this.model}\nColor: ${this.color}\nIn Stock: ${this.isInStock}\nPrice: ${this.price}`;
    },
};
```

### Property initializer shorthand
```js
function creatPerson(name, age) {
	return {
		name,
		age,
	}
}

// zelfde als
function creatPerson(name, age) {
	return {
		name = name;
		age = age;
	}
}
```

