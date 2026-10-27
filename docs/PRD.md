# PRD: Nové portfolio Víta Charváta (B2 Horské jezero)

[Česky](#cesky) | [English](#english)

<a id="cesky"></a>

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

---

<a id="english"></a>

# PRD: Vít Charvát's New Portfolio (B2 Mountain Lake)

27 Oct 2026 · Vít Charvát

## Summary

We'll build a new personal portfolio at vitekcharvat.github.io based on design **B2 Mountain Lake**. The intro will be a single painted scene that blends smoothly into a dark page, and below it a calm website with projects and contact details. The new website replaces the current pixel-art portfolio.

The source is the B2 frame on the "Portfolio – 5 směrů" canvas, page Kolo 2. I'll only start building once you approve this document.

## Problem

The current website is game-style pixel art and doesn't come across the way you want: your drawing isn't visible in it. The audit from 26 Oct also found factual bugs that the new website has to fix.

| What's wrong | Impact |
| --- | --- |
| The "Cvičení z 8. září" link returns a 404 | Visitors hit a broken page |
| On the Google Search card, the screen reader reads "z 8. září" | Accessibility bug from copy-pasting |
| Contact only through GitHub | Clients and the school can't write to you directly |
| Open Graph tags and sitemap.xml are missing | Shared links have no preview, Google indexes the site worse |
| Your role on Špatníkluci.cz isn't clear | The strongest project looks unverifiable |
| README and PORTFOLIO.md don't match the code | Confusing for anyone who opens the repository |

## Goals and success metrics

The website is done when all of these are true:

- [ ] Within 5 seconds it's clear this is a programmer: the heading "Programuju weby a malé aplikace." (I build websites and small apps.), the laptop with code in the painting and the GitHub link are visible without scrolling.
- [ ] The painting blends into the page with no visible edge (the desk is the same color as the page, #26323A).
- [ ] The W3C validator reports 0 errors in the HTML and in the custom CSS.
- [ ] There is no `<script>` anywhere on the website.
- [ ] At widths of 320, 390, 768, 1280 and 1440 px the page can't be scrolled sideways and diacritics in headings aren't clipped.
- [ ] Text contrast is at least 4.5 : 1, focus is visible, controls are at least 44 px and the website respects reduced motion.
- [ ] Lighthouse on mobile scores at least 90 in performance, accessibility, SEO and best practices.
- [ ] All links work (0× 404) and external ones are checked by hand.
- [ ] A shared link shows a preview with an image (Open Graph) and sitemap.xml exists.

## Scope

We're building three pages and everything they need for sharing and search.

**We build:**

1. `index.html`: header with navigation, intro with the B2 painting, Projects (3 cards), More projects button, About me, Contact, footer.
2. `skolni-projekty.html`: the More projects subpage in the same style, without the large painting. I'll show a design on the canvas before building it.
3. `404.html`: a custom page for addresses that don't exist.
4. The B2 painting as an image in several sizes, plus an image for the share preview.
5. `sitemap.xml`, `robots.txt`, page descriptions and Open Graph tags.
6. Updated `README.md` and `PORTFOLIO.md`.

**We don't build:** JavaScript, a blog, an English version, a light/dark mode switch or a contact form. A form wouldn't work without JavaScript and a server, so an e-mail link is enough.

## Content

The text comes from the B2 mockup. Feel free to edit it right here, it'll go into the website exactly as written.

| Section | Content |
| --- | --- |
| Navigation | Vít Charvát (link to top), Projekty, O mně, Kontakt (Projects, About me, Contact) |
| Intro, heading | Programuju weby a malé aplikace. (I build websites and small apps.) |
| Intro, text | Jsem Vít Charvát. Píšu v HTML, CSS a Pythonu, a protože jsem dřív kreslil, záleží mi i na tom, jak věci vypadají. (I'm Vít Charvát. I write HTML, CSS and Python, and because I used to draw, I also care about how things look.) |
| Intro, buttons | Projects (jumps to the section), GitHub (github.com/VitekCharvat) |
| Project 1 | Špatní Kluci. Company website, live. A website for an Ostrava company that supplies communication technology to professionals. HTML, CSS. Link spatnikluci.cz |
| Project 2 | Programming Languages. School website. Which languages are used for games, AI, websites and mobile apps, with a code sample for each field. HTML, CSS |
| Project 3 | Python Projects. Experiments. Small programs outside the browser. Python. Link to the Small-Python-Projects repository |
| Below projects | More projects button, leads to the subpage |
| Subpage | Programming Languages and Giggle (my own search engine modeled on Google: home page, images, advanced search, forms). The 8 September exercise is dropped. |
| About me | I study and I code. Drawing taught me to look at the whole picture, and that is how I look at websites today: what you see first, where your eyes go next and where you should click. I work with HTML, CSS, Python, Git and GitHub. |
| Contact | Get in touch. vitcharvat08@gmail.com and github.com/VitekCharvat |
| Footer | Left: © 2026 Vít Charvát, AI was used with a link. Right: Validate HTML and Validate CSS buttons (W3C, open in a new tab). |

## Design

I'm building from the B2 frame on the canvas. These values come from it.

| Element | Value |
| --- | --- |
| Page | background #26323A, cards #2E3B43 with border #3D4B53 |
| Text | #EEF0EE, muted #C4CDCF and #A3AFB3 |
| Accent | #F2C29B: project labels, link underlines |
| Text on the sky in the intro | #12202B and #1C2A35 |
| Headings | Newsreader 500, intro heading 48–84 px |
| Body text | Figtree 400–600, 17–19 px |
| Layout | content width at most 1280 px, 3 project cards side by side, stacked below 760 px |
| Buttons | rounded, at least 52 px tall; validation buttons in the footer 44 px |

**The B2 painting:** a mountain lake in the morning with peaks in a pink glow reflected in the water, a pine tree on the right, a wooden desk with a laptop (code), a mug and a sketchbook. The sky leaves room for the heading in the top left. On mobile the painting sits under the text, cropped to the center.

**Icons (Font Awesome):** GitHub next to GitHub links, an envelope next to the e-mail, an external arrow next to external links. Nothing more, so the rest stays calm.

## Technical

The website will be HTML and CSS only on GitHub Pages; the only bigger decision is how to embed the painting.

- **No JavaScript.** No `<script>`, everything in HTML and CSS.
- **Bootstrap 5.3 as CSS only** from a CDN: grid, spacing and utility classes. Styling is handled by a custom `style.css` loaded after Bootstrap.
- **Google Fonts:** Newsreader and Figtree with Czech characters, with `display=swap`.
- **Font Awesome Free 6.7** from a CDN, only the icons from the Design section.
- **Hosting:** GitHub Pages from the `main` branch of the VitekCharvat.github.io repository.
- **The painting as an image, not code.** In the mockup the painting is an SVG with filters (noise, blur, color blending). Browsers render it slowly, especially on mobile, and Safari may render it differently. I recommend converting it to WebP in three widths (960, 1440 and 2880 px) plus a narrower crop for mobile, inserted with `<picture>`. The source SVG stays in the repository.
- **Old files:** I'll only delete the pixel images, old screenshots and validation outputs in `docs/` with your approval.

## Plan

I'm building in your folder on the `redesign` branch, so the live website doesn't change until we merge. Steps marked "waiting on you" won't happen without your approval.

1. Approval of this PRD (waiting on you).
2. A quick design of the More projects subpage and the 404 page on the canvas.
3. Converting the B2 painting to WebP and an image for the share preview (1200 × 630 px).
4. Building `index.html` and `style.css`.
5. Subpage, 404, sitemap.xml, robots.txt and meta tags.
6. Checks: W3C, Lighthouse, widths 320–1440 px, all links, keyboard navigation.
7. Updating README.md and PORTFOLIO.md.
8. Deleting old files (waiting on you).
9. Merging into `main` and publishing on GitHub Pages (waiting on you). From then on, everyone who opens the website sees the new version.

## Risks

The biggest risk is the size of the painting; the rest have simple fixes.

| Risk | What to do |
| --- | --- |
| The painting as an image slows down loading | WebP in the right sizes, target under 300 kB on mobile, other images load only on scroll |
| Bootstrap overrides custom styles | Custom CSS loaded after Bootstrap, only the grid and utility classes used from Bootstrap |
| Google Fonts or the icon CDN are unavailable | Fallback system fonts, the website works without icons too |
| The painting is an SVG sketch, not a hand-made digital painting | If you want a different painting later, only the image gets swapped, the page stays |
| The old website disappears as soon as we merge into `main` | Building on a branch, merging only after checks and your approval |

## Open questions

These questions won't block the build, but I need answers before publishing.

- [ ] What was your role on Špatníkluci.cz (design, code, deployment)? I'll add it to the project description.
- [ ] Where should the link after "Bylo použito AI" (AI was used) lead: to the shared Claude conversation, or somewhere else?
- [ ] The button below the projects: "Další projekty" (More projects), or just "Další" (More)?
- [ ] Do you want LinkedIn or another profile in the contact section?
- [ ] Can I delete the old pixel images and the files in `docs/` once it's done?
- [ ] Do you agree with the painting as a WebP image instead of SVG in the code?
