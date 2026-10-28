# Portfolio Víta Charváta

[Česky](#cesky) | [English](#english)

<a id="cesky"></a>

Osobní portfolio studenta IT na OA a SOŠL Opava. Ukazuje, že programuju weby a malé aplikace. Úvod tvoří kresba Opavy za soumraku, viděná z polí na jihu: Hláska, kostelní věže, paneláky s rozsvícenými okny a pruhovaný komín teplárny. Kresba se po krocích ztmavuje, až z ní zbude jen barva stránky, a pod ní stojí jméno přes celou šířku obrazovky.

## Obsah

Web je v angličtině. Hlavní stránka má úvod se jménem, jednou větou a tlačítkem See projects. Projekty jsou rejstřík velkých jmen (Špatní Kluci, Bakaláři Timetable, Programming Languages, Python Projects, More projects); na počítači ukazuje rámeček vpravo náhled projektu, na kterém je myš nebo focus, na mobilu má každý projekt svůj obrázek. Následuje About me (fakta, odstavec, nástroje a časová osa), Contact (e-mail, GitHub, Opava) a patička s odkazy, validací a uvedením AI. Podstránka More projects ukazuje školní weby a tři screenshoty zblízka. Neexistující adresa ukáže vlastní stránku 404 se stejnou kresbou.

## Technologie

- HTML5 a vlastní CSS, žádný JavaScript.
- Bootstrap 5.3.8 jen jako CSS (mřížka a `visually-hidden`).
- Google Fonts Hanken Grotesk, Font Awesome Free 6.7.2.
- Kresba jako tři vrstvy SVG v `assets/kresba/`, screenshoty projektů jako WebP.
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
- Barvy, písmo a velikosti: proměnné v `:root` na začátku `style.css`.
- Velikost jména: `--vel-monument` ve `vw`, naladěná tak, aby jméno vyplnilo šířku na jeden řádek.
- Kresba: SVG soubory v `assets/kresba/` (viz `assets/OBRAZKY.md`).
- Nový projekt: další `<li class="projekt">` v seznamu a stejný obrázek do `.ramecek` na stejné pořadí. CSS počítá s nejvýš pěti projekty, pro šestý přidej řádek s `:nth-child(6)`.
- Nová stránka: přidej ji i do `sitemap.xml`.

## Přístupnost

Odkaz pro přeskočení navigace, viditelný focus, ovládací prvky vysoké aspoň 44 px, kontrast textu aspoň 4,5 : 1, náhled projektů ovladatelný i klávesnicí a respektování omezeného pohybu.

---

<a id="english"></a>

# Vít Charvát's Portfolio

A personal portfolio of an IT student at OA a SOŠL Opava. It shows that I build websites and small apps. The intro is a drawing of Opava at dusk, seen from the fields to the south: the Hláska tower, church towers, panel blocks with lit windows and the striped heating plant chimney. The drawing darkens step by step until only the page colour is left, and below it the name stands across the full width of the screen.

## Content

The website is in English. The home page has an intro with the name, one sentence and a See projects button. The projects are an index of large names (Špatní Kluci, Bakaláři Timetable, Programming Languages, Python Projects, More projects); on a computer a frame on the right shows a preview of the project under the mouse or keyboard focus, on a phone each project has its own picture. Then come About me (facts, a paragraph, tools and a timeline), Contact (e-mail, GitHub, Opava) and a footer with links, validation and the AI credit. The More projects subpage shows the school websites and three close-up screenshots. An address that doesn't exist shows a custom 404 page with the same drawing.

## Technology

- HTML5 and custom CSS, no JavaScript.
- Bootstrap 5.3.8 as CSS only (the grid and `visually-hidden`).
- Google Fonts Hanken Grotesk, Font Awesome Free 6.7.2.
- The drawing as three SVG layers in `assets/kresba/`, project screenshots as WebP.
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
- Colours, font and sizes: variables in `:root` at the top of `style.css`.
- Name size: `--vel-monument` in `vw`, tuned so the name fills the width on one line.
- Drawing: the SVG files in `assets/kresba/` (see `assets/OBRAZKY.md`).
- New project: another `<li class="projekt">` in the list and the same picture in `.ramecek` in the same position. The CSS handles up to five projects; for a sixth, add a line with `:nth-child(6)`.
- New page: add it to `sitemap.xml` too.

## Accessibility

A skip link past the navigation, visible focus, controls at least 44 px tall, text contrast of at least 4.5 : 1, a project preview that works with the keyboard too, and support for reduced motion.
