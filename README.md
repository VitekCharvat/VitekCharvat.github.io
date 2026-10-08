
## URL: https://vitekcharvat.github.io

## Soubory

- `PORTFOLIO.md`: popis portfolia, technologie a návod ke spuštění.

- `index.html`: hlavní portfolio.
- `skolni-projekty.html`: samostatný přehled školních prací.
- `style.css`: vlastní vzhled a české komentáře k náročnějším pravidlům.
- `docs/CSS-PRUVODCE.md`: vysvětlení Bootstrapu a CSS na konkrétních příkladech.
- `assets/images/`: pixelové ilustrace.
- `assets/navrh/`: schválený obrázkový návrh.
- `assets/nahledy/`: snímky hotové stránky na počítači a mobilu.
- `assets/favicon.svg`: malá ikona terminálu do záložky prohlížeče.
- `assets/OBRAZKY.md`: původ obrázků a zadání použitá k jejich tvorbě.

Všechny obrazové soubory jsou uvnitř `assets`. Náhledy v kartách jsou dekorativní HTML/CSS ilustrace, nikoli skutečné screenshoty aplikací. Používají stejnou pixelovou krajinu z `assets/images`.

## Použité knihovny

- [Bootstrap 5.3.8](https://getbootstrap.com/docs/5.3/getting-started/introduction/): CSS mřížka, karty, tlačítka, rozestupy a pomocné třídy.
- Google Fonts: [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) pro herní nadpisy a [Inter](https://fonts.google.com/specimen/Inter) pro běžné texty.
- [Font Awesome Free 6.7.2](https://fontawesome.com/): ikony načítané přes CSS, bez JavaScriptového kitu.

Na webu není žádný `<script>`, událostní obsluha ani závislost na JavaScriptu. Mobilní menu je stále viditelné a zalamuje se. Efekty najetí myší a plynulý posun obstarává CSS. Nastavení systému pro omezení pohybu se respektuje.

## Co upravit

- Jméno a texty: přímo v HTML.
- Barvy: proměnné v `:root` na začátku `style.css`.
- Obrázky: v `assets/images`; při změně názvu uprav také cesty v HTML nebo CSS.
- Projekty: změň obsah jednotlivých `<article>` a jejich `href`. Odkazy vedou na existující veřejné práce, nikoli na smyšleného správce úkolů z ukázkového návrhu.
- Nový školní projekt: přidej další Bootstrap sloupec s kartou do `skolni-projekty.html`.
- Rok v patičce je záměrně statický, mění se ručně.

## Validace v patičce

Odkaz **Ověřit HTML** rovnou spustí W3C Nu kontrolu adresy `https://vitekcharvat.github.io/`.

Odkaz **Ověřit CSS** rovnou spustí W3C CSS validátor pro stejnou adresu s profilem CSS3 SVG. Oba odkazy otevírají novou kartu a ověřují aktuálně zveřejněnou verzi webu, nikoli místní soubory.

Bootstrap a Font Awesome jsou cizí knihovny, vlastní pravidla upravuj v `style.css`.

## Výsledek kontroly (8. října 2026)

- Oba HTML soubory: W3C Nu, žádné chyby ani varování. Výsledky jsou v `docs/*.validation.json`.
- Vlastní CSS: W3C CSS Validator, profil CSS3 SVG, 0 chyb a 0 varování. Výsledek je v `docs/css-validation.xml`.
- Prohlížeč: zkontrolované desktopové rozložení 1280 px a mobilní šířky 390 a 320 px; žádné vodorovné přetékání. Přechod na školní projekty a zpět funguje. Konzole nehlásila chyby ani varování.
- V dokumentu nejsou žádné skripty. Všechny čtyři externí odkazy na konkrétní projekty odpovídaly úspěšně.
