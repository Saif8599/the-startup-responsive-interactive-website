# Design Challenge: Rebuild the Funda Listing Detail Page

## Inhoudsopgave

- [Over Funda](#over-funda)
- [Wat ik heb gedaan](#wat-ik-heb-gedaan)
- [Eisen](#eisen)
- [Kenmerken](#kenmerken)
- [Code Conventions](#code-conventions)
  - [Ademruimte en inspringen](#ademruimte-en-inspringen)
  - [Volgorde en nesten van CSS selectors](#volgorde-en-nesten-van-css-selectors)
  - [Nesten van media queries](#nesten-van-media-queries)
  - [Naamgeving](#naamgeving)
- [Licentie](#licentie)

## Over Funda

Funda is een toonaangevende organisatie in Nederland, gevestigd in Amsterdam, die onroerend goed op de Nederlandse markt aanbiedt via haar website **funda.nl**. Met ongeveer 68 miljoen bezoeken per maand (waarvan 4 miljoen unieke bezoekers), is funda.nl een van de drukst bezochte woningwebsites in Nederland. De website biedt een uitgebreid overzicht van huizen die te koop staan, gepresenteerd door vastgoedmakelaars.

Funda speelt een belangrijke rol in een van de grootste beslissingen in iemands leven: het kopen of verkopen van een woning. Dit proces kan zowel spannend als uitdagend zijn, en Funda streeft ernaar om de gebruikers zoveel mogelijk te ondersteunen.

## Wat ik heb gedaan

In dit project heb ik de **Listing Detail Page (LDP)** van Funda herbouwd. Dit was een praktijkopdracht waarin ik verschillende vaardigheden heb toegepast, zoals layout, responsive design en toegankelijkheid.

- **HTML en CSS**: Ik heb de complete pagina opgebouwd met **semantische HTML** en **CSS**. Alle inhoud is handmatig toegevoegd (geen externe API's of databases gebruikt).
- **Responsief ontwerp**: De pagina is volledig responsief gemaakt, met gebruik van **media queries** voor mobiel, tablet en desktop.
- **Toegankelijkheid**: Er is speciale aandacht besteed aan de toegankelijkheid van de website door het gebruik van semantische HTML en het implementeren van juiste **ARIA-attributen** waar nodig.
- **Geen JavaScript**: Hoewel JavaScript niet verplicht was, heb ik ervoor gekozen om dit niet te gebruiken, omdat het niet noodzakelijk was voor deze opdracht.

## Eisen

- Volg het **Figma ontwerp** voor de layout.
- Je kunt een beetje creatief zijn als je bepaalde onderdelen wilt verbeteren, maar blijf binnen de grenzen van het ontwerp.
- Zorg ervoor dat de pagina op verschillende apparaten goed werkt door gebruik te maken van **media queries**.
- De code moet **toegankelijk** zijn, dus gebruik semantische HTML-elementen en geschikte ARIA-attributen waar nodig.
- **De media viewer moet correct werken**: Zorg ervoor dat de gebruiker door de media kan navigeren door middel van miniaturen of andere interactieve elementen.

## Kenmerken

Voor dit project heb ik **HTML** en **CSS** gebruikt om de layout en de structuur van de pagina te bouwen. De HTML is opgebouwd met semantische elementen om de toegankelijkheid en leesbaarheid te verbeteren, zoals `<header>`, `<footer>`, en `<section>` tags. CSS is gebruikt voor de styling, waarbij een **mobile-first** benadering is gevolgd en **media queries** zijn toegepast om de pagina responsive te maken voor verschillende schermformaten (mobiel, tablet, desktop). 

Er is geen JavaScript gebruikt, omdat de focus ligt op de layout en styling. Interactieve elementen zoals de media viewer werken zonder de noodzaak van JavaScript, door gebruik te maken van CSS voor overgangseffecten en visuele interactie.

## Code Conventions

Hieronder worden de codeconventies beschreven die zijn toegepast om de code overzichtelijk en onderhoudbaar te houden.

### Ademruimte en inspringen
- **Inspringen**: 2 spaties of 1 tab per niveau voor consistentie.
- **Inline elementen**: Altijd op dezelfde regel geplaatst.
- **Block elementen**: Altijd op een nieuwe regel geplaatst.

**Voorbeeld HTML**:
```html
<div class="media-titel">
  <h1>Foto's</h1>
  <span class="totale-images">10</span>
</div>
```
---
### Volgorde en nesten van CSS selectors

**Volgorde van selectors**:
   - De CSS is gestructureerd in dezelfde volgorde als de HTML, zodat de code makkelijk te volgen is.
   - Begin met algemene styling (bijv. `body`) en werk naar specifieke secties toe (bijv. `.header`, `.footer`).

**Nesten van selectors**:
   - Geneste elementen in de HTML worden op dezelfde manier genest in de CSS.
   - Groepeer selectors per sectie, inclusief bijbehorende subelementen.
   - Voeg duidelijke opmerkingen toe voor elke sectie om het snel te herkennen.

```css
/* Algemene styling */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

/* Header styling */
.header {
  background-color: #f4f4f4;
  padding: 20px;

  /* Geneste navigatie */
  .nav {
    display: flex;
    justify-content: space-between;

    /* Links in de navigatie */
    a {
      text-decoration: none;
      color: #333;
    }
  }
}

/* Footer styling */
.footer {
  background-color: #222;
  color: #fff;
  text-align: center;
  padding: 10px;
}
```
---
### Nesten van media queries

Om de CSS overzichtelijker en onderhoudbaar te maken, zijn media queries genest bij de betreffende selectors. Dit zorgt ervoor dat alle styling van een element, inclusief de responsive aanpassingen, op één plek te vinden is.

**Structuur van media queries**:
   - Media queries staan direct onder de styling van de desbetreffende selector.

**Opmaak en voorbeeld**:
   - Media queries worden netjes genest met voldoende inspringing om het te verduidelijken.

**Voorbeeld CSS met geneste media queries**:
```css
/* Algemene styling */
.container {
  padding: 10px;
  background-color: #f9f9f9;

  @media (min-width: 768px) {
    padding: 20px;
  }

  @media (min-width: 1024px) {
    padding: 30px;
  }
}

/* Header styling */
.header {
  font-size: 16px;

  @media (min-width: 768px) {
    font-size: 18px;
  }

  @media (min-width: 1024px) {
    font-size: 20px;
  }
}
```
---
### Naamgeving

Bij het schrijven van HTML, CSS, en JavaScript is consistente en beschrijvende naamgeving cruciaal voor leesbaarheid en onderhoudbaarheid. Hier zijn de conventies die we hebben gevolgd, inclusief voorbeelden en richtlijnen.

1. **HTML Naamgeving**:
   - Gebruik beschrijvende en semantische class- en id-namen.
   - Gebruik kebab-case voor alle class- en id-namen.
   - Zorg ervoor dat de naam de inhoud of functie van het element beschrijft.

**Voorbeeld HTML**:
```html
<!-- Media gallery -->
<section class="media-viewer">
  <article class="media-main">
    <form class="cta-media-main"></form>
    <p class="positie-indicator"></p>
    <ul class="media-thumbnails"></ul>
  </article>
</section>
```
## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).


