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
// convert json to object
const obj = JSON.parse('{"name":"John", "age":30, "city":"New York"}');

// 
```


