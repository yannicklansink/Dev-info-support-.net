
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

### Closure
Voordelen:
- data encaptulatie

Inner function heeft toegang tot de variables in de outer function, maar niet andersom.

```js
function createCustomer(id, name, city, nrOfUnpaidBills = 0) {
    // let nrOfUnpaidBills = 0;
    return {
        id,
        name,
        city,
        nrOfUnpaidBills() {
            return nrOfUnpaidBills;
        },
        buyStuff() {
            nrOfUnpaidBills++;
        },
        payBill() {
            nrOfUnpaidBills--;
        },
        toString() {
            return `id: ${this.id}\nname: ${this.name}\ncity: ${this.city}`;
        },
        badPlayer(numberObject) {
            if (nrOfUnpaidBills >= numberObject.number) {
                return true;
            }
            return false;
        }
    }
}
```


### Default parameters
```js
functio makeRequest(url, timeout = 2000, callback = () => { }) {

}
```

