# Look and Feel - Corporate Identity

## Code/Design Review Stylesheet

Deze week heb je geleerd hoe je een styleguide maakt voor een opdrachtgever. Een huisstijl is de visuele identiteit van een organisatie. Hieronder vallen naam, beeldmerk, kleuren, typografie, vormentaal (stramienen/vlakken/curves/opmaak) en fotografiestijl. Jullie hebben de huisstijl van de opdrachtgever geanalyseerd, een interface inventory gemaakt en een styleguide samengesteld. Vervolgens hebben jullie dit omgezet in een gedeelde stylesheet, die je de rest van deze sprint met je team onderhoudt. 

### Aanpak
Vandaag ga je aan de slag met een code-review op de repo 'Look and Feel - Styleguide' van 2 andere groepen. Vervolgens ga je met jouw groepje de ontvangen issues toewijzen (assignen) aan teamleden. Post de link van jullie Look and Feel Styleguide in de Teams channel 'Sprint 4' samen met jullie projectnaam. 

## Code-review Look and Feel - Styleguide
1. Bekijk in Teams welke groepjes er mee doen voor een code review op de repo van de Look and Feel Styleguide. Kies twee teams uit die je samen gaat reviewen. Voeg een emoji toe bij het uitgekozen team. Zorg ervoor dat elk team minimaal één review ontvangt. 

_Herhaal onderstaande checklist voor twee groepen. Je voert deze code review uit met de gehele groep. Bepaal met elkaar wie de issues schrijft._

2. Pak samen met jullie mentor de repo erbij van de groep die je gaat reviewen. Bekijk met elkaar de `index.html` en de `styleguide-[teamnaam].css`. 
   - Controleer of de juiste link naar de stylesheet gedeeld is. Is het duidelijk hoe je de stylesheet kunt implementeren in je eigen project? 

3. **Code Review Checklist**: Doorloop de volgende vragen om de kwaliteit van de stylesheet te beoordelen. Schiet waar nodig een issue in.

   - **Indeling van de stylesheet**: Is de structuur van de stylesheet logisch? Zijn secties goed ingedeeld (bijv. kleuren, typografie, knoppen) zodat ze eenvoudig terug te vinden zijn?
   
   - **Consistente naamgeving**: Is de naamgeving consisitent? Kijk of er een consistente schrijfwijze is gekozen (zoals kebab-case voor CSS-variabelen of selectors, bijvoorbeeld `--font-size-large`).
   
   - **Naamgeving en begrijpelijkheid**: Is de naamgeving van variabelen en classes gemakkelijk te volgen? Hoe hebben jullie dit als team gedaan? Wat nemen jullie mee naar het eigen project? En wat kan het team dat jullie reviewen daar nog in verbeteren? Maak daar een issue voor aan.

   - **Volledigheid van de stylesheet**: Bevat de stylesheet voldoende elementen en states voor een volledige implementatie? Let op states zoals hover, active en focus voor links en knoppen, en controleer of formulieren (inputvelden, foutmeldingen) ook zijn opgenomen. Pak waar nodig het Figma bestand erbij om te kijken of de belangrijkste elementen terug te vinden zijn in de styleguide. 

   - **Gebruik van custom properties**: Worden custom properties juist ingezet? Beschrijven de CSS custom properties waar de kleur voor gebruikt wordt, in plaats van welke kleur het is? En worden de custom properties op de juiste plaats toegepast? Bijvoorbeeld, worden custom properties op de `:root` gedefinieerd? Is dat een bewuste keuze? Of zou het ook op de body kunnen?

   - **Herhaling van code**: Bekijk of er onnodige herhaling van code is. Als vaak dezelfde stijlen worden herhaald, kijk dan of dit simpeler kan door custom properties of herbruikbare classes te gebruiken.


---

## Issues toewijzen en samenwerking bespreken
Klaar met de twee code reviews? Ga dan samen aan de slag met de issues die jullie hebben ontvangen.
1. Bekijk samen met jullie mentor de issues die jullie zelf hebben ontvangen. Vraag waar nodig toelichting.
2. Overleg met elkaar wie welk issue gaat oppakken. _Assign_ vervolgens een issue aan het teamlid dat deze taak gaat oppakken.
3. Bespreek ook hoe de samenwerking deze week is gegaan; komen jullie de gemaakte afspraken na? Kunnen jullie nog nieuwe afspraken maken voor de komende twee weken? Voeg dit toe aan het issue met jullie teamcanvas. 
4. Klaar? Je kunt nu individueel de issues die aan jou zijn toegewezen gaan oplossen. Sluit de issues wanneer ze zijn opgelost met een duidelijke toelichting van wat je hebt gedaan en de bijbehorende commit.


