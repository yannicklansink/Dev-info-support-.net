# HTML CSS JS

## Algemeen

1. Wat is het nut van een `<th>` element en wat betekent `<td colspan="4"></td>`?
	1. th: table header, als kopcel voor een table. 
	2. colspan = 4 breed.

3. Wat wordt bedoeld met de term 'semantische elementen' en waarom is dit relevant?
	1. Vooral bedoelt voor screenreaders en seo om de webpagina beter te begrijpen.

5. Wat wordt in css verband bedoeld met specificity?
	1. De cascading van een opgemaakt html element 

7. Is de volgende stelling 100% waar?
	1. waar
   _Een block element heeft als `display` property de waarde `block` en neemt de gehele breedte in beslag. Er kan bovendien een `height` en `width` ingesteld worden._

1. Is de volgende stelling 100% waar?
	1. waar
   _Een inline element heeft als `display` property de waarde `inline` en gebruikt niet de gehele breedt. Er kunnen geen `height` en `width` ingesteld worden._

1. Een collega heeft getypt:

   (html)

   ```html  
<div id="header>  
   ```

   (css)

   ```css  
   div#header {  
     background-color: darkblue;  
     color: white;  
   }  
   ```

   Wat adviseer je en waarom?
	   Ik adviseer geen div te gebruiken, maar een header element.

---

## CSS

In html staat:

```html  
<section id="toeslagen">  
<article class="card">  
<ul>  
<li>Kinderopvang</li>  
<li>Huurtoeslag</li>  
</ul>  
</article>  
<article class="card">  
<ul>  
<li>Huurtoeslag</li>  
<li>Zorgtoeslag</li>  
</ul>  
</article>  
</section>  
```

1. We willen elk `article` meer 'volume' geven (ruimte direct rond de content). Hoe?

   a. article { padding: 10px; }
	   .card { padding: 10px; } 
   b. section { padding: 10px; }\  
	   #toeslagen {padding:10px;}
   c. article { margin: 10px; }
	   .card { margin: 10px;}
   d. section { margin: 10px; }
	   #toeslagen {margin;10px;}
			
1. Op welke 3 manieren kunnen we css koppelen zodat we een article kunnen opmaken?
	1. inline css (minst aan te raden, wordt gebruikt bij frameworks vaak)
	2. een style sheet toevoegen
	3. internal css (niet aan te raden)

3. Beschrijf het verschil tussen de CSS selectors:

   - `article.card`  selecteert alle article elementen met de class card
   - `article`  selecteert aleen articles
   - `.card` selecteert alleen card class

4. Beschrijf het verschil tussen de CSS selectors:

   - `section>article`  selecteert alle article elementen die direct kinderen zijn van een section element
   - `section article` selecteert alle article elementen die in de DOM zitten van alle sections.

---

## CSS echte site

Ga naar <https://belastingen.arnhem.nl>.

1. Als we de browser smaller maken worden de cards **Particulier** en **Bedrijf** onder elkaar getoond. Hoe heet deze wijze van design?
	1. responsive design

Open de Devtools en selecteer de kop **Bedrijf**. Kies het tabje _Styles_.

1. Waar is de styling voor het `<h2>` element gedefinieerd? Klik op de link, het tabje _Sources_ wordt geopend. Bekijk de css en klik daarna weer op het tabje _Styles_.
	1. in de style.css file

Bekijk de card **Bedrijf**. Klik met de rechtermuisknop op de pagina en kies `View page source` (CTRL+U). Vind de html van het form **Bedrijf**.

1. Waarom is het belangrijk dat een `<h2>` heading is gebruikt bij Bedrijf?  
	1. voor structuur en hierarchie.
2. Waarom staat _U kunt hier namens het bedrijf inloggen._ in een `<p>` element?  
	1. Dat geeft het beste weer wat voor element het is
3. Waarom wordt de class "login-form" gebruikt?  
	1. Om de juiste benaming te geven aan wat het voor element is.
4. Leg de betekenis uit van alle attributen in het `<form>` element.  
	1. <form id="kc-form-login" class="" action="https://belastingen.arnhem.nl/auth/realms/Arnhem/login-actions/authenticate?code=AeklIZWKj_kYBidPlFHav-boErlI_3So47QF7zOleq8&amp;execution=9da8b180-ed17-4972-bf20-92f3d74a6140&amp;client_id=egouw&amp;tab_id=gXTai-zqD9Y" method="post">

<div class="form-group">

<label class="control-label title-label">RSIN</label>

<input id="username" class="form-input" name="username" type="text" autofocus autocomplete="off" />

</div>

<div class="form-group">

<label class="control-label title-label">Aanslagbiljetnummer / Aangiftebiljetnummer</label>

<input id="password" class="form-input" name="password" type="password" autocomplete="off" />

</div>

<input class="btn-login pull-right} btn-primary btn-lg" name="login" id="kc-login" type="submit" value="login"/>

5. Waarom en hoe zijn er labels gebruikt?  
	1. Voor de toegankelijkheid van het form
6. Waarom staan `<label>` en `<input>` binnen een `<div>`? 
	1. Om het te onderscheiden van elkaar, dit kan als reden hebben om het te stylen
7. Leg de betekenis uit van alle attributen in het `<input>` element.
	id="username" class="form-input" name="username" type="text" autofocus autocomplete="off" 
	id = om het te koppelen
	class = om het te stylen
	name = om het te bedoemen. 
	type = wat voor soort input het is
	autocomplete = om aan te geven dat autocomplete niet kan

Open van deze website het bestand `style.css`.

1. Er staat o.a:

   ```css  
   #contact-information .heading,  : voor alle id contact-information en daarbinnen een heading class
   #footer_columns .column h1,  : 
   #footer_columns .column h2,  
   #footer_columns .column h3,  
   #footer_columns .column h4 {  
     display: block;  
     font-size: 14px;  
     color: #428bca;  
     margin-bottom: 0.5em;  
     font-weight: bold;  
     margin-top: 0.5em;  
   }  
   ```

   Leg uit wat de selector betekent inclusief alle properties.

1. Er staat ook een media query:

   ```css  
   @media (max-width: 992px) {  
     /* ... */

     .contentrow {  
       width: 100%;  
       margin-left: auto;  
       margin-right: auto;  
       overflow: hidden;  
     }

     .header #logo {  
       margin: 0 auto;  
       text-align: center;  
     }

     .header-info {  
       margin-bottom: 20px;  
     }

     h1 {  
       margin-top: 20px !important;  
     }  
   }  
   ```

   Leg uit wat de bedoeling is van deze media query? Wordt in dit css bestand een 'mobile-first' benadering gehanteerd?