# Portfolio Víta Charváta

Osobní portfolio začínajícího vývojáře v pixelovém herním stylu. Představuje autora, jeho webové a Python projekty a základní dovednosti.

## Vzhled a obsah

Úvod vychází z druhého, minimalistického mockupu: jméno na jednom řádku, krátké představení, tlačítko Moje projekty, textový odkaz na GitHub a pixelový počítač s průhledným pozadím. Ostatní části zachovávají výraznější herní styl prvního návrhu.

Hlavní stránka obsahuje sekce O mně, Moje projekty a Dovednosti. Odkaz Školní projekty vede na samostatný přehled školních prací. V patičce jsou odkazy na validátory HTML a CSS a uvedení použité AI.

## Technologie

- HTML5: struktura a obsah stránek.
- Bootstrap 5.3.8, pouze CSS: responzivní mřížka, karty, tlačítka a rozestupy.
- Vlastní CSS: barvy, pixelový vzhled a jednoduché úpravy pro mobil.
- Google Fonts: Press Start 2P pro nadpisy, Inter pro běžný text.
- Font Awesome Free 6.7.2: ikony.

Web nepoužívá JavaScript. CSS zůstává pod limitem 500 řádků a obsahuje české vysvětlující komentáře.

## Spuštění

Otevři `index.html` v prohlížeči. Není potřeba nic instalovat ani sestavovat. Internet je potřeba pro načtení Bootstrapu, fontů a ikon a pro návštěvu externích odkazů.

Případně v této složce spusť:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Otevři `http://127.0.0.1:8000`. Server ukončíš pomocí Ctrl+C.

## Struktura projektu

| Soubor nebo složka | Účel |
| --- | --- |
| `index.html` | Hlavní stránka portfolia. |
| `skolni-projekty.html` | Přehled školních prací. |
| `style.css` | Vlastní vzhled s komentáři. |
| `assets/images/` | Pixelové ilustrace včetně aktuálního počítače. |
| `assets/navrh/` | Původní schválený návrh. |
| `assets/nahledy/` | Náhledy hotového webu. |
| `assets/favicon.svg` | Ikona do záložky prohlížeče. |
| `assets/OBRAZKY.md` | Původ obrázků a zadání jejich tvorby. |
| `docs/CSS-PRUVODCE.md` | Vysvětlení složitějšího CSS s příklady. |
| `docs/` | Také uložené výsledky validace. |

Všechny obrázky jsou uvnitř `assets`. Náhledy v kartách jsou ilustrace vytvořené HTML a CSS, nikoli screenshoty skutečných aplikací.

## Úpravy

Texty a adresy odkazů uprav v HTML. Hlavní barvy jsou v proměnných `:root` na začátku `style.css`. Novou školní práci přidej jako další kartu v `skolni-projekty.html`. Rok v patičce je statický a mění se ručně.

Při automatickém formátování může editor rozepsat krátká CSS pravidla na více řádků. Pokud potřebuješ dodržet limit 500 řádků, po formátování počet zkontroluj.

## Validace a přístupnost

Odkazy Ověřit HTML a Ověřit CSS rovnou spustí W3C validaci adresy `https://vitekcharvat.github.io/` v nové kartě. Kontrolují zveřejněnou verzi webu. CSS validátor používá profil CSS3 SVG.

Stránka má zvýraznění odkazů při ovládání klávesnicí, odkaz Přeskočit na obsah a popisy obrázků. Respektuje nastavení systému pro omezení pohybu.

## Použití AI

Bylo použito AI | [GPT-6 Astra](https://chatgpt.com/s/cx_6ac7fca7abec8191a3a4ad97ed4f1198)

Odkaz vede na veřejně sdílený snímek této konverzace. Sdílený snímek se automaticky neaktualizuje o další zprávy. Pixelové ilustrace vznikly pomocí vestavěného nástroje ImageGen.
