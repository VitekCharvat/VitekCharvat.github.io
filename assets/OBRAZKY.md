# Obrázky

[Česky](#cesky) | [English](#english)

<a id="cesky"></a>

Všechny obrázky webu jsou ve složce `assets`. Vznikly 28. 10. 2026 pro nový design „Opava za soumraku“.

## Soubory

| Soubor | Rozměr | Velikost | K čemu |
| --- | --- | --- | --- |
| `kresba/opava-obloha.svg` | viewBox 2400 × 950 | 3 kB | vrstva 1: nebe po pruzích, slunce, hvězdy a ptáci |
| `kresba/opava-mesto.svg` | viewBox 2400 × 950 | 40 kB | vrstva 2: kopce Nízkého Jeseníku a Opava s okny, která se rozsvěcují |
| `kresba/opava-pole.svg` | viewBox 2400 × 950 | 10 kB | vrstva 3: pole s brázdami, spodek má barvu stránky (#18191b) |
| `images/projekty/spatnikluci.webp` | 1200 × 1500 px | 78 kB | náhled webu spatnikluci.cz |
| `images/projekty/jazyky.webp` | 1200 × 1500 px | 58 kB | náhled webu Programming Languages |
| `images/projekty/giggle.webp` | 1200 × 1500 px | 22 kB | náhled Giggle |
| `images/projekty/giggle-obrazky.webp` | 1200 × 1500 px | 23 kB | Giggle, hledání obrázků (podstránka) |
| `images/projekty/giggle-hledani.webp` | 1200 × 1500 px | 28 kB | Giggle, pokročilé hledání (podstránka) |
| `images/projekty/giggle-formular.webp` | 1200 × 1500 px | 47 kB | Giggle, stránka s formuláři (podstránka) |
| `images/og-image.jpg` | 1200 × 630 px | 56 kB | náhled při sdílení odkazu (Open Graph) |
| `favicon.svg` | viewBox 64 × 64 | 1 kB | ikona v záložce: Hláska před sluncem |

Widget Bakaláři a ukázka kódu v Pythonu nejsou obrázky, ale HTML přímo v `index.html` (widget podle vzhledu z `BakalariRozvrh.js`, kód je `countdown.py` z repozitáře Small-Python-Projects).

## Původ

**Kresbu Opavy** nakreslil Claude (AI od Anthropic) přímo v kódu SVG podle zadání Víta Charváta. Jde o volnou kresbu, ne o překreslenou fotku. Jako vodítko pro tvar věží a pohled od jihu posloužily fotky z Wikimedia Commons: [Opava-panorama-from-south](https://commons.wikimedia.org/wiki/File:Opava-panorama-from-south.jpg) (Multimotyl) a [Hláska, radnice Opava](https://commons.wikimedia.org/wiki/File:Hl%C3%A1ska,_radnice_Opava_-_panoramio.jpg) (Vladimír Jadrný). Kresba je ve třech vrstvách, aby se při načtení stránky dala každá rozpohybovat zvlášť. Animace oken, majáku na komíně, ptáků a slunce jsou přímo v SVG (`<style>` na začátku souboru) a vypnou se, když má uživatel omezený pohyb.

**Screenshoty** jsou Vítovy vlastní weby, vyfocené 28. 10. 2026 v prohlížeči Chrome bez okna (okno 1000 × 1250 px, zvětšení 1,2) a uložené jako WebP v kvalitě 82.

**Náhled pro sdílení** je výřez úvodu hlavní stránky v šířce 1200 px, bez navigace a tlačítka.

## Jak obrázky upravit

- Kresba: SVG soubory jdou upravit v textovém editoru, každý tvar je na vlastním řádku. Barvy odpovídají proměnným ze `style.css`. Všechny tři vrstvy musí mít stejný `viewBox`, jinak na sebe nesednou.
- Screenshot: otevři web v okně 1000 × 1250 px, vyfoť ho a ulož jako WebP 1200 × 1500 px pod stejným názvem.
- Náhled pro sdílení: otevři `index.html` v okně 1200 × 630 px, skryj navigaci a tlačítko a ulož snímek jako JPG v kvalitě 84.

## Malba z předchozího návrhu

Soubory `images/hero-jezero-*.webp` a `src/hero-jezero.svg` patří k předchozímu návrhu B2 Horské jezero. Nový web je nepoužívá; smažou se až po schválení. Starší obrázky jsou v historii Gitu ve větvi `main`.

---

<a id="english"></a>

# Images

All website images are in the `assets` folder. They were made on 28 Oct 2026 for the new "Opava at dusk" design.

## Files

| File | Dimensions | Size | Purpose |
| --- | --- | --- | --- |
| `kresba/opava-obloha.svg` | viewBox 2400 × 950 | 3 kB | layer 1: banded sky, the sun, stars and birds |
| `kresba/opava-mesto.svg` | viewBox 2400 × 950 | 40 kB | layer 2: the Nízký Jeseník hills and Opava with windows that light up |
| `kresba/opava-pole.svg` | viewBox 2400 × 950 | 10 kB | layer 3: fields with furrows, the bottom is the page colour (#18191b) |
| `images/projekty/spatnikluci.webp` | 1200 × 1500 px | 78 kB | preview of spatnikluci.cz |
| `images/projekty/jazyky.webp` | 1200 × 1500 px | 58 kB | preview of the Programming Languages website |
| `images/projekty/giggle.webp` | 1200 × 1500 px | 22 kB | preview of Giggle |
| `images/projekty/giggle-obrazky.webp` | 1200 × 1500 px | 23 kB | Giggle, image search (subpage) |
| `images/projekty/giggle-hledani.webp` | 1200 × 1500 px | 28 kB | Giggle, advanced search (subpage) |
| `images/projekty/giggle-formular.webp` | 1200 × 1500 px | 47 kB | Giggle, the forms page (subpage) |
| `images/og-image.jpg` | 1200 × 630 px | 56 kB | link share preview (Open Graph) |
| `favicon.svg` | viewBox 64 × 64 | 1 kB | browser tab icon: Hláska in front of the sun |

The Bakaláři widget and the Python code sample aren't images but HTML right in `index.html` (the widget follows the look of `BakalariRozvrh.js`, the code is `countdown.py` from the Small-Python-Projects repository).

## Origin

**The drawing of Opava** was made by Claude (an AI by Anthropic) directly in SVG code, following Vít Charvát's brief. It's a free drawing, not a traced photo. Photos from Wikimedia Commons served as a guide for the shape of the towers and the view from the south: [Opava-panorama-from-south](https://commons.wikimedia.org/wiki/File:Opava-panorama-from-south.jpg) (Multimotyl) and [Hláska, radnice Opava](https://commons.wikimedia.org/wiki/File:Hl%C3%A1ska,_radnice_Opava_-_panoramio.jpg) (Vladimír Jadrný). The drawing has three layers so each one can move on its own when the page loads. The animations of the windows, the chimney's warning light, the birds and the sun live inside the SVG (`<style>` at the top of the file) and switch off when the visitor has reduced motion turned on.

**The screenshots** are Vít's own websites, captured on 28 Oct 2026 in headless Chrome (a 1000 × 1250 px window at 1.2 zoom) and saved as WebP at quality 82.

**The share preview** is a crop of the home page intro at 1200 px wide, without the navigation and the button.

## How to change the images

- Drawing: the SVG files can be edited in a text editor, every shape is on its own line. The colours match the variables in `style.css`. All three layers must keep the same `viewBox`, otherwise they won't line up.
- Screenshot: open the website in a 1000 × 1250 px window, capture it and save it as a 1200 × 1500 px WebP under the same name.
- Share preview: open `index.html` in a 1200 × 630 px window, hide the navigation and the button and save the capture as a JPG at quality 84.

## Painting from the previous design

The files `images/hero-jezero-*.webp` and `src/hero-jezero.svg` belong to the previous design, B2 Mountain Lake. The new website doesn't use them; they'll be deleted only after approval. Older images are in the Git history on the `main` branch.
