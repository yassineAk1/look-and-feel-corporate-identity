# Look and Feel - Corporate Identity

## Styleguide

Ontwerp en maak op basis van de huisstijl een *styleguide* voor een opdrachtgever.



### Huisstijl

Een huisstijl is de visuele identiteit van een organisatie. Het symbolische gedeelte van de bedrijfsidentiteit.
Hieronder vallen naam, beeldmerk, kleuren, typografie (lettertype), vormentaal (stramienen/vlakken/curves/opmaak) en fotografiestijl.

![](fdnd-huisstijl.png)
*De huisstijl van FDND bestaat uit verschillende kleuren, vormen, typografie en gebruik van beeldmateriaal.*

Waarom heeft een bedrijf/instelling/organisatie een huisstijl nodig?
Het zorgt voor herkenbaarheid en het geeft de gebruiker een ervaring. Het laat zien wat de gebruiker/bezoeker kan verwachten. Als de visuele eigenschappen van een identiteit consistent worden vormgegeven, onstaat er vertrouwen bij de gebruiker.

### Huisstijlen toepassen met behulp van een Styleguide

Een frontender moet in staat zijn om een huisstijl goed toe te passen. Om dit te bereiken, moet je eerst een huisstijl analyseren: Wat zijn de eigenschappen van de huisstijl en hoe hebben ze vorm gekregen? Hoe gedragen deze eigenschappen zich? Wat is het idee erachter?

Een styleguide is essentieel voor het begrijpen en toepassen van een huisstijl. Een styleguide geeft voorbeelden en uitleg over hoe iets eruit moet zien. Een styleguide helpt bij het ontwerpen en bouwen van een website, zodat de verschillende elementen consistent worden toegepast.

![](fdnd-styleguide-1.png)
*In de styleguide van FDND staat uitgelegd hoe de vormen en kleuren moeten worden toegepast.*

> Style guides are an important tool for web development today, especially in large, complex web applications. They help document styles and patterns, keep designers and developers in sync, and greatly help to organize and distill complex interfaces. ([Lambert, 2016](https://www.smashingmagazine.com/2016/05/creating-a-living-style-guide-case-study/))

## Aanpak

### Interface inventory

Je begint met het in kaart brengen van alle onderdelen van de huisstijl en gemaakte websites. Het resultaat is een *interface inventory*, een verzameling van alle gemaakte interface elementen zoals typografie, images, media, buttons en andere formulier elementen.
 
 1. Jullie gaan met de studenten die dezelfde opdracht hebben de onderdelen van de huisstijl verzamelen in het Figma document van de opdrachtgever (of maak een gedeeld Figma bestand aan als die er nog niet is).
 2. Kopieer de artboards van de [Interface Inventory template](https://www.figma.com/design/Tox75iooqru0EvV3iLbkHw/Interface-Inventory?node-id=0-1&node-type=canvas&t=sZLKnogq564gwWdl-0) naar jullie Figma document, in een nieuwe Page, genaamd “Interface inventory”.
 3. Verzamel per categorie van de interface inventory alle gemaakte en gebruikte stijlen:
 - Maak screenshots van alle onderdelen van de websites die jullie hebben gemaakt
 - Maak screenshots van alle onderdelen van het aangeleverde ontwerp van de opdrachtgever
 - Maak screenshots van alle onderdelen van de door jullie gemaakte Figma ontwerpen
 4. Bespreek de interface inventory met een mentor, zodat jullie een goed beeld krijgen van de verschillende onderdelen die in gebruik zijn.

![](interface-inventory-buttons-brad-frost.jpg)
*Voorbeeld van een Interface inventory van alle buttons die gebruikt worden op een bank website. Bron [Interface Inventory van Brad Frost](https://bradfrost.com/blog/post/interface-inventory/)*

<!--
#### interface inventory template

- Typography
    - Headings: headings, titels, subtitles, ...
    - Text elements: paragraphs, blockquotes, ...
    - Lists: bulleted, numbered, definition, ...
- Images
    - Logo's
    - Icons
    - Content images: different content images with borders, white space, ...
    - Image with captions
- Media
    - Video player
    - Audio player
    - Slideshow players
- Tables 
- Buttons
- Forms
    - Text inputs: text, email, url, password, ...
    - Select menu's
    - Radio/Checkbox Inputs
- Navigation
    - Primary Navigation
    - Tabs
    - Breadcrumbs
- Components
    - Carousels
    - Accordions
- ...
-->

### Styleguide samenstellen

Nu je een inventarisatie hebt gemaakt van alle onderdelen kunnen jullie een styleguide maken. 
Bepaal voor de basiselementen kleur, typografie en formulier elementen hoe die eruit moeten zien, door deze stappen te volgen:

1. Bespreek het verzamelde materiaal uit de _interface inventory_ en onderzoek of je overeenkomsten kunt ontdekken tussen de verschillende huisstijl onderdelen.
2. Kopieer de artboards van de [Styleguide template](https://www.figma.com/design/Tox75iooqru0EvV3iLbkHw/Interface-Inventory?node-id=9-5&node-type=canvas&t=EdEg1vNpxJgTyUlm-0) naar jullie Figma document. 
3. Maak een ontwerp voor de verschillende huisstijl onderdelen: 
- Bepaal de verschillende kleuren voor de huisstijl in RGB of HSL formaat, maak een voorbeeld en schrijf een korte uitleg.
- Bepaal alle typografische elementen zoals headings, text, links, lijsten en/of tabellen, ontwerp voorbeelden en schrijf een korte uitleg.
- Bepaal de formulier elementen zoals buttons, inputs, selects en radio's, ontwerp voorbeelden en schrijf een korte uitleg.

### Gedeelde Stylesheet maken

Op basis van de styleguide gaan jullie een gezamenlijke stylesheet maken. 
Jullie gaan als team één stylesheet maken met de basis elementen van de huisstijl zoals de kleuren, typografie en formulier elementen. Later deze sprint ga je die misschien uitbreiden met meer gedeelde elementen.
Zo zorg je ervoor dat op verschillende websites de huisstijl consistent wordt toegepast.

#### Samenwerking

Slechts één teamlid forkt de repo [Look and Feel - Styleguide](https://github.com/fdnd-task/look-and-feel-styleguide) voor deze opdracht. Deze persoon voegt de teamleden toe als 'Collaborators': Ga naar de Settings van de repository, klik op Collaborators en voeg de GitHub accounts van de overige teamleden toe.

Nu kunnen alle teamleden samenwerken op die repository, door deze allemaal te _Clonen_ (downloaden). Alle teamleden kunnen nu op hun eigen computer onderdelen van de website coderen, en hun aanpassingen en wijzigingen committen en pushen naar jullie gezamenlijke repository.

Omdat het maken en beheren van een gezamenlijke stylesheet een teamopdracht is, zullen jullie ook goede afspraken moeten maken en bedenken hoe je hier samen aan gaat werken. Vul gezamenlijk een [teamcanvas](https://github.com/fdnd-task/your-tribe-squad-page/blob/main/docs/team-canvas.md) in en bewaar deze in de styleguide repo.

#### Instructies Stylesheet
1. Hernoem het [CSS file `styleguide.css`](https://github.com/fdnd-task/look-and-feel-styleguide/blob/main/styleguide.css) naar jullie opdrachtgever (bijvoorbeeld `styleguide-ad-connect.css`, `styleguide-buurtcampuskrant.css`, `styleguide-milledoni.css`, `styleguide-smarter-cities.css`, `styleguide-embassy-free-mind.css` of `styleguide-snappthis.css`), en pas de [link erheen](https://github.com/fdnd-task/look-and-feel-styleguide/blob/main/index.html#L8) aan. Hier gaan jullie de CSS schrijven voor de huisstijl. Een begin van de HTML staat al klaar, maar dit mag je natuurlijk helemaal naar wens aanpassen en uitbreiden.
2. Ontwerp en maak de CSS voor de verschillende huisstijl onderdelen (componenten). Overleg met het team hoe jullie de CSS classes gaan noemen. Schrijf de afspraken over bijvoorbeeld classnames en code conventies in de Readme van de styleguide repo.
3. Zet de gezamenlijke stylesheet live door de repo te publiceren met GitHub Pages (en pas [de link in de styleguide](https://github.com/fdnd-task/look-and-feel-styleguide/blob/main/index.html#L16-L17) aan). 
4. Gebruik de rest van deze sprint de gezamenlijke stylesheet in je eigen project en pas je code aan, zodat je de nieuwe classes gebruikt (of gaat gebruiken). Jouw CSS zal kleiner worden, omdat een deel al in de gezamenlijke stylesheet staat.
5. Zorg dat tijdens deze sprint jullie veranderingen in de styleguide bijhouden met issues, zodat iemand uit het team het kan aanpassen. 

### Bronnen

- [What is a style guide and how to create one?](https://www.figma.com/resource-library/what-is-a-style-guide/)
- [Interface Inventory](https://bradfrost.com/blog/post/interface-inventory/)

Voorbeelden van Styleguides:
- [Decathlon Design System](https://www.decathlon.design/726f8c765/p/75e137-digital-overview) 
- [Familysearch Styleguide](https://www.familysearch.org/frontier/styleguide/)
