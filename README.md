# Portfolio Víta Charváta

[Česky](#cesky) | [English](#english)

<a id="cesky"></a>

## URL: https://vitekcharvat.github.io

Osobní portfolio ve stylu „Opava za soumraku“: nahoře kresba Opavy od jihu (Hláska, kostelní věže, paneláky a komín teplárny), která se po krocích ztmaví do barvy stránky, pod ní jméno přes celou šířku. Podrobnější popis je v `PORTFOLIO.md`. Texty na webu jsou v angličtině.

## Soubory

- `index.html`: hlavní stránka (úvod s kresbou, Projects, About me, Tools, Contact).
- `skolni-projekty.html`: podstránka More projects se školními cvičeními (zatím Giggle) a screenshoty.
- `404.html`: stránka pro neexistující adresu (GitHub Pages ji použije sám).
- `style.css`: celý vlastní vzhled s českými komentáři.
- `sitemap.xml`, `robots.txt`: pro vyhledávače.
- `assets/kresba/`: kresba Opavy ve třech vrstvách SVG (nebe, město, pole).
- `assets/images/projekty/`: screenshoty projektů ve WebP.
- `assets/images/og-image.jpg`: náhled při sdílení odkazu.
- `assets/favicon.svg`: ikona v záložce (Hláska před sluncem).
- `assets/OBRAZKY.md`: původ obrázků a jak je vyrobit znovu.
- `docs/`: zadání, citace a podklady k předchozímu návrhu (nejsou součást webu).
- `googlea39b896c1462c2f5.html`: ověření webu pro Google Search Console, nemazat.

## Použité knihovny

- [Bootstrap 5.3.8](https://getbootstrap.com/docs/5.3/getting-started/introduction/), jen CSS: mřížka (`row`, `col-*`) a třída `visually-hidden`.
- Google Fonts: [Hanken Grotesk](https://fonts.google.com/specimen/Hanken+Grotesk) pro celý web.
- [Font Awesome Free 6.7.2](https://fontawesome.com/): ikona GitHubu a šipky.

Na webu není žádný `<script>`. Výměna náhledu u projektů (najetí myší nebo Tab) funguje jen přes CSS selektor `:has()`.

## Pohyb

Při načtení se kresba rozsvítí a vyjede, jméno vystoupá a v oknech se postupně rozsvítí světla, na komíně bliká maják a přes nebe letí ptáci. Animace v kresbě jsou přímo v souborech SVG. Kdo má v systému omezený pohyb, vidí rovnou hotový stav.

Animace řízené posouváním stránky (`animation-timeline`) web nepoužívá, protože je W3C CSS Validator zatím nezná a hlásil by je jako chyby.

## Validace

Tlačítka Validate HTML a Validate CSS v patičce spustí W3C validaci zveřejněné stránky v nové kartě.

Kontrola 28. 10. 2026: všechny tři HTML soubory W3C Nu bez chyb i varování, `style.css` W3C CSS Validator (CSS3 + SVG) 0 chyb a 1 varování (CSS proměnné se nekontrolují). Stránka nepřetéká do strany při šířkách 390, 768 a 1440 px.

## Použití AI

Bylo použito AI | [CITACE](docs/citace.md)

Odkaz CITATIONS v patičce webu vede na `citace.md` na GitHubu. Tam jsou odkazy na všechny konverzace s AI a další zdroje, doplňují se ručně.

---

<a id="english"></a>

# Vít Charvát's Portfolio

## URL: https://vitekcharvat.github.io

A personal portfolio in the "Opava at dusk" style: at the top, a drawing of Opava from the south (the Hláska tower, church towers, panel blocks and the heating plant chimney) that darkens step by step into the page colour, and below it the name across the full width. A more detailed description is in `PORTFOLIO.md`. The website text is in English.

## Files

- `index.html`: home page (intro with the drawing, Projects, About me, Tools, Contact).
- `skolni-projekty.html`: the More projects subpage with school exercises (Giggle for now) and screenshots.
- `404.html`: page for addresses that don't exist (GitHub Pages uses it automatically).
- `style.css`: all custom styling, with comments in Czech.
- `sitemap.xml`, `robots.txt`: for search engines.
- `assets/kresba/`: the drawing of Opava in three SVG layers (sky, town, fields).
- `assets/images/projekty/`: project screenshots in WebP.
- `assets/images/og-image.jpg`: link share preview.
- `assets/favicon.svg`: browser tab icon (Hláska in front of the sun).
- `assets/OBRAZKY.md`: where the images came from and how to rebuild them.
- `docs/`: brief, citations and material for the previous design (not part of the website).
- `googlea39b896c1462c2f5.html`: site verification for Google Search Console, do not delete.

## Libraries

- [Bootstrap 5.3.8](https://getbootstrap.com/docs/5.3/getting-started/introduction/), CSS only: the grid (`row`, `col-*`) and the `visually-hidden` class.
- Google Fonts: [Hanken Grotesk](https://fonts.google.com/specimen/Hanken+Grotesk) for the whole website.
- [Font Awesome Free 6.7.2](https://fontawesome.com/): the GitHub icon and arrows.

The website has no `<script>` at all. The project preview swap (mouse hover or Tab) works with the CSS `:has()` selector only.

## Motion

On load the drawing fades in and rises, the name slides up, windows light up one after another, the warning light on the chimney blinks and birds fly across the sky. The animations inside the drawing live in the SVG files themselves. Anyone with reduced motion turned on sees the finished state straight away.

The website doesn't use scroll-driven animations (`animation-timeline`), because the W3C CSS Validator doesn't know them yet and would report them as errors.

## Validation

The Validate HTML and Validate CSS buttons in the footer run W3C validation of the published page in a new tab.

Check on 28 Oct 2026: all three HTML files pass W3C Nu with no errors or warnings, and `style.css` passes the W3C CSS Validator (CSS3 + SVG) with 0 errors and 1 warning (CSS variables aren't checked). The page doesn't overflow sideways at widths of 390, 768 and 1440 px.

## Use of AI

AI was used | [CITATIONS](docs/citace.md)

The CITATIONS link in the website footer leads to `citace.md` on GitHub. It lists links to all AI conversations and other sources, and it's updated by hand.
