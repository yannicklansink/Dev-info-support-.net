
spread operator on objects
```js
// copy van person 
const obj1 = {...person, taal: 'Mandarijn'} 

const product = {
	id: 2,
	titel: 'wasmand',
}

product.titel = 'wasmandjes';
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

