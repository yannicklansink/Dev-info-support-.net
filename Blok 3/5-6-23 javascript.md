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