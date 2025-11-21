# Look and Feel - Corporate Identity

## Stylesheet

Je hebt na de Sprint Planning in Figma een styleguide gemaakt en een gezamenlijke stylesheet met de huisstijl van de opdrachtgever. Slechts één teamlid heeft de repo 'Look and Feel - Styleguide' voor deze opdracht geforkt. Hier staat de gezamenlijke stylesheet die jullie allemaal gaan gebruiken voor je eigen opdracht. 

Vandaag ga je leren hoe je een gestructureerd CSS file kan maken met  _classes_ en _Custom Properties_. 

### Aanpak

Eerst ga je analyseren wat voor CSS strategie grote websites gebruiken. Daarna ga je met behulp van Custom Properties jullie gezamenlijke stylesheet structuren. Tot slot ga je het gezamenlijke stylesheet inladen en leren hoe je de styles kan toepassen op je project. 


## CSS strategie
Naarmate er meer CSS in je project komt, bijvoorbeeld als je gaat samenwerken aan een project, wordt het steeds belangrijker om een CSS strategie (met elkaar) te bepalen.

### Opdracht

![](CSS-strategie.png)
*Met behulp van de Devtools kun je onderzoeken wat de CSS strategie van een website is.*

Onderzoek op 3 verschillende websites hoe CSS is toegepast voor een `h2` en `button` element, met onderstaande vragen.

#### Beantwoord deze vragen op het whiteboard:
- Welke element-selectoren en class-selectoren zijn gebruikt?
- Welke properties staan er in welke selectoren?
- Wat valt op aan de naamgeving van classes en eventuele custom properties?

#### Onderzoek deze websites:  
- https://css-tricks.com/  
- https://www.smashingmagazine.com/  
- https://fdnd.nl/


## Custom Properties
Met Custom Properties kun je zelf een CSS `property` bedenken, daar een `value` in bewaren, en die op meerdere plekken gebruiken. Hiermee zorg je voor _DRY code_, wat de code beter leesbaar, makkelijker onderhoudbaar en sneller maakt. Dit is vooral fijn voor developers.

```css
.card {
  --ruimte: 1.2rem;
  padding: var(--ruimte);
  margin: var(--ruimte);
}
```

Sterker nog, je kunt de values dynamisch aanpassen, en op die manier slimme styling schrijven, zoals:

```css
.button {
  --lightness: 30%;
  background: hsl(200 100% var(--lightness));

  &:hover, &:focus {
    --lightness: 25%;
  }
}
```

Veel tutorials gebruiken de `:root` selector (het _hoogste_ element in de DOM) om custom properties op te zetten. Door _inheritance_ in CSS zijn die properties in de hele onderliggende DOM bekend:

```css
:root {
  --primary-color: red;
  --secondary-color: blue;
}
h1 {
  color: var(--primary-color);
}
p {
  background-color: var(--primary-color);
}
```

Dit is hetzelfde als:

```css
html {
  --primary-color: red;
  --secondary-color: blue;
}
h1 {
  color: var(--primary-color);
}
p {
  background-color: var(--primary-color);
}
```

De `:root` selector is dus 'gewoon' de `html` selector. Voor “globale variabelen”, die overal in je DOM beschikbaar moeten zijn, is dit een handige manier van custom properties gebruiken.

Maar custom properties zijn veel krachtiger dan alleen globale variabelen. Je kunt hiermee snel verschillende stijlen voor bijvoorbeeld een knop maken, wat handig is in een styleguide.

Met bijvoorbeeld de volgende HTML:

```html
<button class="button">Knop</button>
<button class="button button-ok">OK</button>
<button class="button button-cancel">Annuleren</button>
```

En deze CSS:

```css
.button {
  --kleur: 200;
  --lichtheid: 30%;
  background: hsl(var(--kleur) 100% var(--lichtheid));
  color: #fff;

  &:hover, &:focus {
    --lichtheid: 25%;
  }

  &:active {
    --lichtheid: 20%;
  }
}

.button-ok {
  --kleur: 100;
}
.button-cancel {
  --kleur: 20;
}
```

Speel hier maar eens mee in bijvoorbeeld een CodePen of je Learning Journal.

### Opdracht

Jullie hebben een gezamenlijke stylesheet gemaakt met de styling voor de kleuren, typografie en formulier elementen. 

Bekijk welke elementen in de gezamenlijke stylesheet geschreven kunnen worden met custom properties. Denk bijvoorbeeld aan kleuren, font-sizes, borders, breedtes en/of hoogtes van elementen. Als waardes vaker voorkomen, kun je custom properties gebruiken.

Bespreek met een mentor de custom properties, classnames en code conventies die jullie hebben toegepast. 
Schets het 'ontwerp' van jullie stylesheet op het whiteboard en noteer zo nodig aanpassingen over bijvoorbeeld classnames en code conventies.

### Bronnen

- [Using CSS custom properties (variables)](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [CSS Custom Properties Guide](https://css-tricks.com/a-complete-guide-to-custom-properties/)

<!-- - [Breaking CSS Custom Properties out of :root Might Be a Good Idea](https://css-tricks.com/breaking-css-custom-properties-out-of-root-might-be-a-good-idea/) -->

### Opdracht Light & Dark mode (advanced)
Als je al ervaring hebt met custom properties kun je proberen een Light & Dark mode te maken. 
Een Light & Dark mode op de website helpt gebruikers om de website beter te kunnen bekijken in verschillende omstandigheden.

Implementeer een Dark Theme met custom properties die werkt op basis van de voorkeuren van de gebruiker. 
Custom properties kunnen hierbij helpen om onnodige herhaling van bijvoorbeeld CSS values voor kleuren te voorkomen. 

- Gebruik het artikel [Dark Mode in CSS](https://css-tricks.com/dark-modes-with-css/)
- Voor nog meer tips en tricks kun je het artikel [CSS color-scheme-dependent colors with light-dark()](https://web.dev/articles/light-dark) lezen
- CodePen voorbeeld van Sanne: https://codepen.io/shooft/pen/wBGajQZ

## CSS inladen
Nu je met je team een [gezamenlijke stylesheet hebt gemaakt](https://github.com/fdnd-task/look-and-feel-corporate-identity/blob/main/docs/styleguide.md#instructies-stylesheet) (en deze live hebt gezet via GitHub Pages), kan je deze gebruiken in jouw eigen project. 
Voeg deze toe aan de `<head>` van je eigen HTML document in jouw project (en pas de juiste link aan). 
Dan heb je dus twee CSS files gelinkt, wat er zo uit ziet:

```html
<link rel="stylesheet" href="https://githubnaam-van-de-forker-uit-jullie-team.github.io/look-and-feel-styleguide/styleguide.css">
<link rel="stylesheet" href="style.css">
```

### CSS principes
Maar welke styling wordt nu uitgevoerd als je `classes` gebruikt uit de huisstijl en uit je eigen stylesheet?

```html
<h2 class="heading-red green">Welke kleur krijgt deze heading?<h2>
```

Voor het uitvoeren van CSS gebruikt de browser de CSS principes _Cascade_, _Specificity_, en _Inheritance_.
De _Cascade_ betekent dat de volgorde van de CSS bepalend is voor welke style wordt uitgevoerd.
_Specificity_ betekent dat een browser bepaalt welke styling het meest belangrijk is.
_Inheritance_ betekent dat (sommige) styles worden doorgegeven van _parent_ aan geneste-elementen.

### Cascade
"Cascade" betekent letterlijk "waterval".  
Hiermee wordt bedoeld dat, als er meerdere stijlen van toepassing zijn op een element, de volgorde bepaalt hoe styles worden toegepast.
Het idee is dat stijlen in een bepaalde volgorde "vallen", en dat bepaalt welke stijl het laatste is en dus wordt uitgevoerd.

### Specificity
Browsers berekenen welke style het belangrijkst is en wordt uitgevoerd.   
Een element selector is het minst specifiek en krijgt een _weight_ van `0 0 0 1`.   
Een class selector krijgt `0 0 1 0`.   
Een ID selector krijgt `0 1 0 0`.   
En een inline-style krijgt een _weight_ van `1 0 0 0`, die style krijgt dus voorang op de id-, class- en element-selectors. 

![](specificity-css-tricks.png)  
*Browsers berekenen welke styling belangrijk is. Hoe specifieker de styling hoe hoger de specificity. Bron [Specifics on CSS Specificity](https://css-tricks.com/specifics-on-css-specificity/)*

Hoe kan je de specificity uitrekenen? Stel je hebt deze HTML:
```html
<ul id="web-technologies">
   <li>HTML</li>
   <li class="favorite">CSS</li>
   <li>JS</li>
</ul>
```
De `<li>` items zijn zwart door deze gecombineerde element en id selector:
```css
ul#web-technologies li {
   font-weight: normal;
   font-size: 12px;
   color: black;
}
```
Nu wil je een `<li>` een andere kleur geven met de class `favorite`. 
Wordt de kleur nu rood?
```css
.favorite {
  color: red;
  font-weight: bold;
}
```
De `<li>` blijft zwart want de selector `ul#web-technologies li` is specifieker dan de class selector `.favorite`. 
De _weight_ van de class selector is `0 0 1 0`, de _weight_ van de gecombineerde selector is `0 1 0 2`. 10 < 102 ...

💪🏼 In de voorbeeld stylesheet, die jullie geforkt hebben, staat `@layer`. Wist je dat je hiermee invloed kunt uitoefenen op de volgorde van de cascade? [Lees meer over Cascade Layers](https://css-tricks.com/css-cascade-layers/).


### Opdracht
Voor deze opdracht ga je spelen met de CSS principes _Cascade_ en _Specificity_ om te leren hoe dat werkt. 
Je gaat 4 experimenten doen. 
Beantwoord de bijhorende vragen in je Learning Journal en probeer uit te leggen wat er gebeurt. 

Open je code editor en maak een blanco HTML pagina, noem het file `specificity.html`, en sla deze op in jouw i-love-web repo. 
Maak een leeg CSS file, noem het `specificity.css`, sla het op in dezelfde map als het HTML file. 
Voeg de gemeenschappelijke stylesheet toe in de `<head>` van het HTML file en daaronder het lege CSS file. 
Dat ziet er dan zo uit in de HTML: 
```html
<link rel="stylesheet" href="https://de-forker-uit-jullie-team.github.io/look-and-feel-styleguide/styleguide.css">
<link rel="stylesheet" href="specificity.css">
```

#### Element selector
Maak een `<h2>` element aan in het HTML file en geef het een bijhorende class uit de gezamenlijke stijlesheet. Maak nog een `<h2>` element aan zonder class. Nu staat er zoiets in het HTML file: 
```html
<h2 class="heading-medium">Ik ben een heading, welke kleur krijg ik?</h2>
<h2>Ik ben ook een heading, welke kleur krijg ik?</h2>
```
Maak nu een element selector in `specificity.css` met een andere kleur dan in de huisstijl staat. 
```css
h2 {
    color: purple;
}
```
Wordt de heading nu paars? 
Of wordt de huisstijl uitgevoerd? 
Kan je bedenken waarom dit gebeurt?

#### Class selector
Voeg nog een `<h2>` element toe met een class uit de gezamenlijke stijlesheet en voeg een tweede class toe. 
```html
<h2 class="heading-medium green">Ik ben een heading met twee classes</h2>
```
Maak de class aan in `specificity.css` en geeft het een andere kleur.
```css
.green {
    color: green;
}
```
Welke kleur krijgt de heading met twee classes? 
Krijgt het de kleur van de huisstijl of wordt de andere class uitgevoerd?
Waarom krijgt de heading die kleur?

#### Class volgorde
Voeg nu aan `specificity.css` een class toe met dezelfde naam als al in de gezamenlijke stylesheet staat. 
Geef de class een andere kleur. Dat ziet er dan zo uit:
```css
.heading-medium {
    color: pink;
}
```
Welke kleur hebben de headings nu? 
Probeer te beschrijving waarom de heading die kleur heeft? 

#### ID selector
Voeg nog een `<h2>` element toe met de class uit de gezamenlijke stijlesheet en voeg een ID toe
```html
<h2 class="heading-medium test" id="heading">Ik ben een heading met een ID</h2>
```
Maak een id selector in `specificity.css` met een andere kleur.
```css
#heading {
    color: yellow;
}
```
Welke kleur krijgt de heading? 
De kleur van de id-selector of 'wint' de class uit de gezamenlijke stylesheet?
Waarom is dat?

#### Bronnen
Als je meer wil leren over het principe Specificity van CSS kun je hier meer lezen: 

- [Cascade, specificity, and inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)
- [Specifics on CSS Specificity](https://css-tricks.com/specifics-on-css-specificity/)
