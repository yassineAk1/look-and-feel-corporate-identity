# Look and Feel - Corporate Identity

## Formulieren

Tijdens deze sprint hebben we een gedeelde stylesheet gemaakt. Daarin staan kleuren, typografie en het begin van een aantal formulierelementen beschreven, in de huisstijl van de opdrachtgever. Als de code goed opgezet is—met herbruikbare _classes_ en _custom properties_—is de gedeelde stylesheet ook te gebruiken in je eigen project.

Met formulierelementen hebben we nog niet veel gedaan, maar dat gaan we in deze workshop veranderen.

### Aanpak

Eerst ga je onderzoeken wat HTML aan verschillende formulierelementen biedt, en wat je hiermee kunt doen. Goede HTML is altijd Stap 1. Daarna ga je uitzoeken welke CSS _properties_ en _values_ specifiek voor dit soort formulierelementen zijn. We gaan de gedeelde stylesheet uitbreiden met een aantal generieke, herbruikbare stijlen, en deze toepassen in de leertaak.

In de Code & Design Review van komende vrijdag gaan we kijken hoe je formulierelementen en styling daarvan hebt toegepast in de leertaak.

## HTML voor formulierelementen (20 minuten)

Zoals je in de HTML van de styleguide repository misschien al hebt gezien, zijn er verschillende invoervelden (`<input>` types) die je kunt gebruiken in je werk. Elk `type` attribuut verandert de werking van het invoerveld in verschillende browsers.

Onderzoek met je tafel aan de hand van de MDN bronnen hieronder welke verschillende `<input>` types er zijn, en schrijf deze allemaal op het whiteboard. Schets bij elk type een voorbeeld, en schrijf bij elk type een uniek ander attribuut dat iets verandert aan de werking van dat formulierelement. Onderzoek bijvoorbeeld wat de `min`, `step` of `multiple` attributen doen, en bij welke types. Open `edu.nl/ptpvy` op je telefoon, en markeer op het whiteboard welke types een andere functionaliteit hebben tussen verschillende browsers en operating systems, als je iets probeert in te voeren.

💪 Wil je meer uitdaging? Laat dan ook per `<input>` type op het whiteboard zien (met een schets of uitleg) of het `list` attribuut hierop gebruikt kan worden, en wat dat doet.

### Bronnen

- [`<input>`: The HTML Input element @ MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)


## Formulierelementen stylen (30 minuten)

Voor het stylen van formulierelementen biedt CSS een hoop leuke extra's. Natuurlijk kun je kleuren, borders en bijvoorbeeld het lettertype van een formulierelement veranderen, maar in CSS zijn ook een aantal dingen specifiek voor formulierelementen beschikbaar. En die gaan we nu onderzoeken.

Op het whiteboard staan een aantal `<input>` types. Verdeel een aantal types eerlijk over de tafel, zodat iedereen 2 tot 4 types krijgt, waar die nog niet mee gewerkt heeft. Open je code editor, maak een blanco HTML pagina, `inputs.html`, en sla deze op in de repo van je Learning Journal/Digital Garden. Maak een leeg CSS bestand, `inputs.css`, en link deze in je HTML. Schrijf de basic HTML voor de input types die jij hebt gekregen. Analyseer en onderzoek voor die types met onderstaande bron welke specifieke CSS je kunt gebruiken, en schets en bouw daarmee een paar kleine demo's. Daag jezelf uit door _selectors_, _properties_ en/of _values_ toe te passen, die je nog niet eerder hebt gebruikt of gezien. Schrijf als je klaar bent op het whiteboard bij “jouw” `<input>` types met een andere kleur een CSS _selector_, _property_, of _value_ die je gebruikt hebt in je code. Bespreek opvallende dingen met elkaar, en leg je demo uit aan anderen.

💅 Snel klaar, en wil je meer uitdaging? Maak een aantal demo's van hoe je `:user-invalid` kunt combineren met verschillende `<input>` types en attributen.

### Bronnen

- [CSS voor `<input>` elements @ MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#css)


## De gedeelde stylesheet uitbreiden (30 minuten)

De styleguide die je samen met je projectgroep hebt gemaakt, bevat een aantal standaard formulierelementen. Waarschijnlijk heb je een deel al gestyled, en een deel nog niet. We gaan nu een aantal elementen samen stylen, waardoor ook formulierelementen en de interactie daarbinnen de _look & feel_ van de opdrachtgever krijgen.

Via de `accent-color` property in CSS kun je de huisstijl van de opdrachtgever relatief makkelijk toepassen op een aantal invoervelden, zoals radio's en checkboxen. Met de _`:focus` selector_ kun je de _focus state_ van een invoerelement aanpassen. Beide staan beschreven in de bronnen hieronder. Overleg met je projectgroep hoe je deze twee toe kunt passen op een manier die ook herbruikbaar is in je eigen project (als je formulierelementen gebruikt). Bespreek ook weer welke _classnames_ je hiervoor gaat gebruiken. Verdeel eventueel de verschillende input types binnen het team, maak issues aan per type, en _assign_ deze aan de juiste teamleden. Kijk of je de _custom properties_ van bijvoorbeeld kleuren kunt hergebruiken binnen de styling voor de formulierelementen.

🎯 Zoek je meer uitdaging met je team? Voeg dan ook formulierelementen zoals `<select>` en `<textarea>` toe aan je styleguide en stylesheet, en maak daar ook passende styling voor. Of voeg styling voor bijvoorbeeld de `:required` en `:user-invalid` _states_ toe.

### Bronnen

- [accent-color @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/accent-color)
- [:focus @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)
- [:user-invalid @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:user-invalid)

## Hoe nu verder? (rest van de dag)

Bedenk voor je opdrachtgever welke formulierelementen je gaat toevoegen. Misschien is er wel een contactpagina, of een mogelijkheid tot reageren op artikelen, of een nieuwsbrief waar je je voor aan kunt melden, of een pagina waar je een profiel op kunt aanmaken?

Maak een issue aan voor dat onderdeel van de website, beschrijf wat je gaat maken, voeg je schetsen en ontwerpen toe, begin met een HTML prototype, ga door met een One Column Layout en maak uiteindelijk een responsive formulier, wat je ook test. Werk _gestructureerd_ en _iteratief_ en hergebruik hierbij elementen en styling uit de styleguide en gedeelde stylesheet. Als hierdoor wijzigingen komen in de styleguide, bespreek die dan met je team, en verdeel het werk.


💯 In Semester 1 maken we vooral _prototypes_. In Semester 2 gaan we die ook werkend maken. Voor nu is het dus prima als je je alleen op de juiste HTML van je formulier focust.
