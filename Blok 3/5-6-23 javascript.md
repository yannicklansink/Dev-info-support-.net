- asynchroon werken
- sets en maps

// iife functie
// word uitgevoerd door de interperter direct
```js
(async () => {
    const dataResults = await haalOp();
    console.log(dataResults);
    addUser(dataResults);
})(); 
```


### async function
```js
async function haalOp() {
    try {
        const resp = await fetch('https://randomuser.me/api/?results=4');
        const data = await resp.json();
        return data.results;
    } catch(err) {
        console.error('foutje', err);
    }
}
```

### sets
```js
// cannot contain duplicates
// common to check the set to see if a values is present

// implement set
const mySet1 = new Set();

mySet1.add(1); // Set(1) { 1 }
mySet1.add(5); // Set(2) { 1, 5 }
mySet1.add(5); // Set(2) { 1, 5 }
mySet1.add("some text"); // Set(3) { 1, 5, 'some text' }
const o = { a: 1, b: 2 };
mySet1.add(o);

mySet1.delete(1);
const boolean = mySet1.has(5); // deletes 5
set.clear(); // deletes everything

// --------------------------
for (const item of mySet1) {
  console.log(item);
} // 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5

for (const item of mySet1.keys()) {
  console.log(item);
} // 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5

for (const item of mySet1.values()) {
  console.log(item);
} // 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5

// key and value are the same here
for (const [key, value] of mySet1.entries()) {
  console.log(key);
} // 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5


```


### maps
```js
// key value pairs
// key is unique
// use for ... of loop

// implement map
const map1 = new Map();

map1.set('a', 1);
map1.set('b', 2);
map1.set('c', 3);

console.log(map1.get('a'));
// Expected output: 1

map1.delete('b');

map1.forEach((value, key) => {
  console.log(`${key} = ${value}`);
});
```