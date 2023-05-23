overflow: hidden;
overflow: scroll;

float:left; -> niet meer gebruiken

#### flexbox
- 1 dimensional (horizontaal of verticaal)
- all direct childeren will have flex context enabled.
[A Complete Guide to Flexbox | CSS-Tricks - CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

``` css
.container {
	display: flex;
	/* flex-direction: row(default) | row-reverse | column | column-reverse; */
	/* flex-wrap: nowrap(default) | wrap | wrap-reverse; */
	/* justify-content: flex-start(default) | flex-end | center | space-between | 
	   space-around | space-evenly | start | end | left | right  */
	/* align-items: stretch | flex-start | flex-end | center | baseline | 
	   first baseline | last baseline | start | end | self-start | self-end /*
	/* align-content: flex-start | flex-end | center | space-between | space-around 
	   | space-evenly | stretch | start | end | baseline | first baseline | 
	   last baseline /*
	/* gap: 10px; row-gap: 10px; column-gap: 20px; */
	flex-flow: column wrap; /* De twee eigenschappen `flex-direction` en `flex-wrap` worden zodanig veel in combinatie met elkaar gebruikt */
}
```

``` css
.childeren {
	order: 5; /* default is 0 */
	flex-grow: 4; /* This defines the ability for a flex item to grow if necessary. */
	flex-shrink: 3; /* default 1 */
	
}
```
``` javascript
<script src= "script.js">
<script async src= "script.js">
<script defer src= "script.js">
```


#### JSON
```javascript
const profile = {
  name: 'Jane Doe',
  'favorite-game': 'Stardew Valley',
  subscriber: false
}

console.log(JSON.stringify(profile)); 

// convert json to object
const obj = JSON.parse('{"name":"John", "age":30, "city":"New York"}');
```

Local Storage: Local Storage is een mechanisme in webbrowsers waarmee webapplicaties sleutel-waardeparen persistent kunnen opslaan op de client-side. De opgeslagen gegevens blijven behouden, zelfs nadat de browser is afgesloten en opnieuw geopend. De opslagcapaciteit van Local Storage is groter dan bij andere client-side opslagmogelijkheden zoals cookies en session storage. De gegevens blijven beschikbaar totdat ze expliciet worden verwijderd door de applicatie of door de gebruiker.

Session Storage: Session Storage is een mechanisme in webbrowsers waarmee webapplicaties gegevens op de client-side kunnen opslaan, maar met een andere reikwijdte en levensduur dan Local Storage. Session Storage biedt een opslagruimte die specifiek is voor een bepaalde browsesessie. Gegevens die in Session Storage worden opgeslagen, blijven beschikbaar zolang het browservenster of tabblad geopend is. Zodra de browsesessie wordt beëindigd (door het sluiten van het venster of tabblad), worden de opgeslagen gegevens gewist en zijn ze niet langer toegankelijk. Session Storage is handig voor het tijdelijk opslaan van gegevens die alleen nodig zijn binnen de huidige sessie en die niet hoeven te worden behouden tussen verschillende bezoeken of browsersessies. Het biedt een eenvoudige interface voor het opslaan en ophalen van gegevens in de vorm van sleutel-waardeparen.

access web storage:
```js
let myValue = window.localStorage.getItme('myKey');
window.localStorage.setItem('myKey', 'myValue');
window.localStorage.removeItem('myKey');
window.localStorage.clear();
```



