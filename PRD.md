# PRD: Nové portfolio Víta Charváta (B2 Horské jezero)

27. 10. 2026 · Vít Charvát

## Shrnutí

Postavíme nové osobní portfolio na vitekcharvat.github.io podle návrhu **B2 Horské jezero**. V úvodu bude jedna malovaná scéna, která plynule přechází do tmavé stránky, a pod ní klidný web s projekty a kontaktem. Nový web nahradí současné pixelové portfolio.

Podklad je rám B2 na plátně „Portfolio – 5 směrů“, stránka Kolo 2. Stavět začnu až po tvém schválení tohoto dokumentu.

## Problém

Současný web je herní pixel art a nepůsobí tak, jak chceš: není v něm vidět tvoje kreslení. Audit z 26. 10. navíc našel věcné chyby, které musí nový web vyřešit.

| Co je špatně | Dopad |
| --- | --- |
| Odkaz „Cvičení z 8. září“ vrací 404 | Návštěvník narazí na nefunkční stránku |
| U karty Google Search čte čtečka „z 8. září“ | Chyba přístupnosti z kopírování |
| Kontakt jen přes GitHub | Klient ani škola ti nemůžou napsat přímo |
| Chybí Open Graph tagy a sitemap.xml | Sdílený odkaz nemá náhled, Google web hůř indexuje |
| U Špatníkluci.cz není poznat tvoje role | Nejsilnější projekt působí neověřitelně |
| README a PORTFOLIO.md neodpovídají kódu | Matoucí pro každého, kdo otevře repozitář |

## Cíle a měřítka úspěchu

Web je hotový, až platí všechny body:

- [ ] Do 5 vteřin je jasné, že jde o programátora: nadpis „Programuju weby a malé aplikace.“, notebook s kódem v malbě a odkaz na GitHub jsou vidět bez posouvání.
- [ ] Malba přechází do stránky bez viditelného okraje (stůl má stejnou barvu jako stránka, #26323A).
- [ ] W3C validátor hlásí 0 chyb v HTML i ve vlastním CSS.
- [ ] Na celém webu není žádný `<script>`.
- [ ] Při šířkách 320, 390, 768, 1280 a 1440 px nejde stránka posouvat do strany a diakritika v nadpisech se neořezává.
- [ ] Kontrast textu je aspoň 4,5 : 1, focus je vidět, ovládací prvky mají aspoň 44 px a web respektuje omezení pohybu.
- [ ] Lighthouse na mobilu dává aspoň 90 ve výkonu, přístupnosti, SEO i osvědčených postupech.
- [ ] Všechny odkazy fungují (0× 404) a externí jsou ověřené ručně.
- [ ] Sdílený odkaz ukáže náhled s obrázkem (Open Graph) a existuje sitemap.xml.

## Rozsah

Stavíme tři stránky a vše, co potřebují ke sdílení a vyhledávání.

**Stavíme:**

1. `index.html`: hlavička s navigací, úvod s malbou B2, Projekty (3 karty), tlačítko Další projekty, O mně, Kontakt, patička.
2. `skolni-projekty.html`: podstránka Další projekty ve stejném stylu, bez velké malby. Návrh ukážu na plátně před stavbou.
3. `404.html`: vlastní stránka pro neexistující adresu.
4. Malba B2 jako obrázek v několika velikostech a obrázek pro náhled při sdílení.
5. `sitemap.xml`, `robots.txt`, popisy stránek a Open Graph tagy.
6. Aktualizovaný `README.md` a `PORTFOLIO.md`.

**Nestavíme:** JavaScript, blog, anglickou verzi, přepínač světlého a tmavého režimu ani kontaktní formulář. Formulář by bez JavaScriptu a serveru nefungoval, stačí odkaz na e-mail.

## Obsah

Texty jsou z mockupu B2. Uprav je klidně přímo tady, do webu půjdou tak, jak tu budou.

| Sekce | Obsah |
| --- | --- |
| Navigace | Vít Charvát (odkaz nahoru), Projekty, O mně, Kontakt |
| Úvod, nadpis | Programuju weby a malé aplikace. |
| Úvod, text | Jsem Vít Charvát. Píšu v HTML, CSS a Pythonu, a protože jsem dřív kreslil, záleží mi i na tom, jak věci vypadají. |
| Úvod, tlačítka | Projekty (skočí na sekci), GitHub (github.com/VitekCharvat) |
| Projekt 1 | Špatní Kluci. Firemní web, běží naostro. Web pro ostravskou firmu, která dodává komunikační technologie profesionálům. HTML, CSS. Odkaz spatnikluci.cz |
| Projekt 2 | Programovací jazyky. Školní web. V čem se programují hry, AI, weby nebo mobilní aplikace, každý obor s ukázkou kódu. HTML, CSS |
| Projekt 3 | Python projekty. Experimenty. Malé programy mimo prohlížeč. Python. Odkaz na repozitář Small-Python-Projects |
| Pod projekty | Tlačítko Další projekty, vede na podstránku |
| Podstránka | Programovací jazyky a Giggle (vlastní vyhledávač podle Googlu: hlavní strana, obrázky, pokročilé hledání, formuláře). Cvičení z 8. září vyřazeno. |
| O mně | Studuju a programuju. Kreslení mě naučilo dívat se na celek, a stejně se dneska dívám na web: co uvidíš první, kam se podíváš potom a kde máš kliknout. Pracuju s HTML, CSS, Pythonem, Gitem a GitHubem. |
| Kontakt | Napiš mi. vitcharvat08@gmail.com a github.com/VitekCharvat |
| Patička | Vlevo © 2026 Vít Charvát, Bylo použito AI s odkazem. Vpravo tlačítka Ověřit HTML a Ověřit CSS (W3C, otevřou se v nové kartě). |

## Design

Stavím podle rámu B2 na plátně. Tyhle hodnoty z něj vycházejí.

| Prvek | Hodnota |
| --- | --- |
| Stránka | pozadí #26323A, karty #2E3B43 s okrajem #3D4B53 |
| Text | #EEF0EE, tlumený #C4CDCF a #A3AFB3 |
| Akcent | #F2C29B: popisky projektů, podtržení odkazů |
| Text na nebi v úvodu | #12202B a #1C2A35 |
| Nadpisy | Newsreader 500, nadpis úvodu 48–84 px |
| Běžný text | Figtree 400–600, 17–19 px |
| Rozložení | šířka obsahu nejvýš 1280 px, 3 karty projektů vedle sebe, pod 760 px pod sebou |
| Tlačítka | zaoblená, výška aspoň 52 px; validační tlačítka v patičce 44 px |

**Malba B2:** ranní horské jezero s vrcholky v růžové záři a jejich odrazem ve vodě, borovice vpravo, dřevěný stůl s notebookem (kód), hrnkem a skicákem. Nebe nechává vlevo nahoře místo pro nadpis. Na mobilu je malba pod textem a oříznutá na střed.

**Ikony (Font Awesome):** GitHub u odkazů na GitHub, obálka u e-mailu, šipka ven u externích odkazů. Víc ne, ať zbytek zůstane klidný.

## Technika

Web bude jen HTML a CSS na GitHub Pages; jediné větší rozhodnutí je, v jaké podobě vložit malbu.

- **Bez JavaScriptu.** Žádný `<script>`, všechno v HTML a CSS.
- **Bootstrap 5.3 jen jako CSS** z CDN: mřížka, rozestupy a pomocné třídy. Vzhled řeší vlastní `style.css` načtený za Bootstrapem.
- **Google Fonts:** Newsreader a Figtree s českými znaky, s `display=swap`.
- **Font Awesome Free 6.7** z CDN, jen ikony z části Design.
- **Hosting:** GitHub Pages z větve `main` repozitáře VitekCharvat.github.io.
- **Malba jako obrázek, ne jako kód.** V mockupu je malba SVG s filtry (šum, rozostření, prolínání barev). Prohlížeč ji kreslí pomalu, hlavně na mobilu, a Safari ji může vykreslit jinak. Doporučuju ji převést do WebP ve třech šířkách (960, 1440 a 2880 px) plus užší výřez pro mobil a vložit přes `<picture>`. Zdrojové SVG zůstane v repozitáři.
- **Staré soubory:** pixelové obrázky, staré náhledy a validační výstupy v `docs/` smažu až s tvým souhlasem.

## Plán

Stavím ve tvé složce ve větvi `redesign`, takže živý web se nezmění, dokud ho nesloučíme. Kroky označené „čeká na tebe“ neudělám bez tvého souhlasu.

1. Schválení tohoto PRD (čeká na tebe).
2. Rychlý návrh podstránky Další projekty a stránky 404 na plátně.
3. Převod malby B2 do WebP a obrázek pro náhled při sdílení (1200 × 630 px).
4. Stavba `index.html` a `style.css`.
5. Podstránka, 404, sitemap.xml, robots.txt a meta tagy.
6. Kontrola: W3C, Lighthouse, šířky 320–1440 px, všechny odkazy, ovládání klávesnicí.
7. Aktualizace README.md a PORTFOLIO.md.
8. Smazání starých souborů (čeká na tebe).
9. Sloučení do `main` a zveřejnění na GitHub Pages (čeká na tebe). Od té chvíle uvidí nový web každý, kdo ho otevře.

## Rizika

Největší riziko je velikost malby; ostatní mají jednoduché řešení.

| Riziko | Co s tím |
| --- | --- |
| Malba jako obrázek zpomalí načítání | WebP ve správných velikostech, na mobilu cíl do 300 kB, ostatní obrázky se načtou až při posunu |
| Bootstrap přebije vlastní styly | Vlastní CSS načtené za Bootstrapem, z Bootstrapu jen mřížka a pomocné třídy |
| Google Fonts nebo CDN s ikonami nejsou dostupné | Záložní systémová písma, web funguje i bez ikon |
| Malba je náčrt v SVG, ne ruční digitální malba | Když budeš chtít později jinou malbu, vymění se jen obrázek, stránka zůstane |
| Starý web zmizí hned po sloučení do `main` | Stavba ve větvi, sloučení až po kontrole a tvém souhlasu |

## Otevřené otázky

Stavbu tyhle otázky nezastaví, ale odpovědi potřebuju před zveřejněním.

- [ ] Jakou roli jsi měl na Špatníkluci.cz (návrh, kód, nasazení)? Doplním ji do popisu projektu.
- [ ] Kam má vést odkaz za „Bylo použito AI“: na sdílenou konverzaci s Claude, nebo jinam?
- [ ] Tlačítko pod projekty: „Další projekty“, nebo jen „Další“?
- [ ] Chceš v kontaktu i LinkedIn nebo jiný profil?
- [ ] Můžu po dokončení smazat staré pixelové obrázky a soubory v `docs/`?
- [ ] Souhlasíš s malbou jako obrázkem WebP místo SVG v kódu?
