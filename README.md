Ontwerp en maak een responsive website voor een startup.

De instructies voor deze opdracht staan in: [INSTRUCTIONS.md](https://github.com/fdnd-task/the-startup-responsive-interactieve-website/blob/main/docs/INSTRUCTIONS.md)

# Titel
Media Viewer rebuild

## Beschrijving
Overzicht van de Opdracht
Het doel van deze opdracht is het herbouwen van de Media Viewer binnen de Listing Detail Page (LDP). De nadruk ligt op het ontwikkelen van een layout met semantische en toegankelijke HTML en CSS. JavaScript kan optioneel worden gebruikt, maar interactie van elementen is niet vereist.

De layout moet ontworpen worden volgens een mobile-first aanpak, met responsive breakpoints voor mobiel, tablet en desktop.

## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met JS gedaan en hoe? -->

## Code Conventions

Hieronder worden de codeconventies beschreven die zijn toegepast om de code overzichtelijk en onderhoudbaar te houden.

---

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

## Bronnen

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).


