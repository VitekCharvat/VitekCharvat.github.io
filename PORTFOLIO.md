# Portfolio Víta Charváta

Osobní portfolio studenta IT na OA a SOŠL Opava. Ukazuje, že programuju weby a malé aplikace, a zároveň moje kreslení: úvod tvoří malovaná scéna horského jezera se stolem a notebookem, která plynule přechází do tmavé stránky.

## Obsah

Hlavní stránka má úvod s nadpisem a odkazy na projekty a GitHub, tři karty projektů (Špatní Kluci, Programovací jazyky, Python projekty), sekce O mně a Kontakt a patičku s uvedením AI a validačními tlačítky. Tlačítko Další projekty vede na podstránku se školními weby (Programovací jazyky, Giggle). Neexistující adresa ukáže vlastní stránku 404.

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
