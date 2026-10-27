# Portfolio Víta Charváta

[Česky](#cesky) | [English](#english)

<a id="cesky"></a>

Osobní portfolio studenta IT na OA a SOŠL Opava. Ukazuje, že programuju weby a malé aplikace, a zároveň moje kreslení: úvod tvoří malovaná scéna horského jezera se stolem a notebookem, která plynule přechází do tmavé stránky.

## Obsah

Web je v angličtině. Hlavní stránka má úvod s nadpisem a odkazy na projekty a GitHub, čtyři karty projektů (Špatní Kluci, Bakaláři Timetable, Programming Languages, Python Projects), sekce About me a Contact a patičku s uvedením AI a validačními tlačítky. Tlačítko More projects vede na podstránku se školními weby (Programming Languages, Giggle). Neexistující adresa ukáže vlastní stránku 404.

## Technologie

- HTML5 a vlastní CSS, žádný JavaScript.
- Bootstrap 5.3.8 jen jako CSS.
- Google Fonts Newsreader a Figtree, Font Awesome Free 6.7.2.
- Malba jako WebP přes `<picture>`: na desktopu 960/1440/2880 px, na mobilu výřez na výšku 720/1080 px.
- Open Graph tagy, `sitemap.xml` a `robots.txt`.
- Hosting: GitHub Pages z větve `main`.

`style.css` má pod 500 řádků a české komentáře u složitějších pravidel.

## Spuštění

Otevři `index.html` v prohlížeči, nic se neinstaluje. Pro funkční 404 a absolutní cesty spusť v této složce:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

a otevři `http://127.0.0.1:8000`.

## Úpravy

- Texty a odkazy: přímo v HTML.
- Barvy a písma: proměnné v `:root` na začátku `style.css`.
- Malba: uprav `assets/src/hero-jezero.svg` a obrázky vyrob znovu podle `assets/OBRAZKY.md`.
- Nový projekt: další `<li>` s kartou v seznamu `.karty`.
- Nová stránka: přidej ji i do `sitemap.xml`.

## Přístupnost

Odkaz pro přeskočení navigace, viditelný focus, ovládací prvky vysoké aspoň 44 px, kontrast textu aspoň 4,5 : 1 a respektování omezeného pohybu.

---

<a id="english"></a>

# Vít Charvát's Portfolio

A personal portfolio of an IT student at OA a SOŠL Opava. It shows that I build websites and small apps, and it also shows my drawing: the intro is a painted scene of a mountain lake with a desk and a laptop, which blends smoothly into the dark page.

## Content

The website is in English. The home page has an intro with a heading and links to the projects and GitHub, four project cards (Špatní Kluci, Bakaláři Timetable, Programming Languages, Python Projects), the About me and Contact sections, and a footer with the AI credit and validation buttons. The More projects button leads to a subpage with school websites (Programming Languages, Giggle). An address that doesn't exist shows a custom 404 page.

## Technology

- HTML5 and custom CSS, no JavaScript.
- Bootstrap 5.3.8 as CSS only.
- Google Fonts Newsreader and Figtree, Font Awesome Free 6.7.2.
- The painting is WebP via `<picture>`: 960/1440/2880 px on desktop, a portrait crop at 720/1080 px on mobile.
- Open Graph tags, `sitemap.xml` and `robots.txt`.
- Hosting: GitHub Pages from the `main` branch.

`style.css` is under 500 lines and has Czech comments on the trickier rules.

## Running it

Open `index.html` in a browser, nothing needs to be installed. For a working 404 page and absolute paths, run this in the folder:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

and open `http://127.0.0.1:8000`.

## Making changes

- Text and links: directly in the HTML.
- Colors and fonts: variables in `:root` at the top of `style.css`.
- Painting: edit `assets/src/hero-jezero.svg` and rebuild the images following `assets/OBRAZKY.md`.
- New project: another `<li>` with a card in the `.karty` list.
- New page: add it to `sitemap.xml` too.

## Accessibility

A skip link past the navigation, visible focus, controls at least 44 px tall, text contrast of at least 4.5 : 1, and support for reduced motion.
