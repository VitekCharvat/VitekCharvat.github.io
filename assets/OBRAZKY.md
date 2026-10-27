# Obrázky

Všechny obrázky webu jsou ve složce `assets`. Vznikly v říjnu 2026 pro redesign portfolia podle návrhu B2 Horské jezero (zadání je v `PRD.md`).

## Soubory

| Soubor | Rozměr | Velikost | K čemu |
| --- | --- | --- | --- |
| `images/hero-jezero-2880.webp` | 2880 × 1920 px | 66 kB | úvodní malba pro velké a retina displeje |
| `images/hero-jezero-1440.webp` | 1440 × 960 px | 35 kB | úvodní malba pro běžný desktop |
| `images/hero-jezero-960.webp` | 960 × 640 px | 24 kB | úvodní malba pro menší okna |
| `images/hero-jezero-mobil-1080.webp` | 1080 × 1440 px | 25 kB | výřez na výšku pro mobily s vysokým rozlišením |
| `images/hero-jezero-mobil-720.webp` | 720 × 960 px | 18 kB | výřez na výšku pro mobily |
| `images/og-image.jpg` | 1200 × 630 px | 67 kB | náhled při sdílení odkazu (Open Graph) |
| `src/hero-jezero.svg` | viewBox 1440 × 960 | 33 kB | zdroj malby, vyrábějí se z něj všechny obrázky výše |
| `favicon.svg` | 64 × 64 | 8 kB | ikona v záložce prohlížeče |

## Původ

Malbu i ikonu vytvořil Claude (AI od Anthropic) jako SVG podle zadání Víta Charváta. Nejde o fotku ani o obrázek z fotobanky. Všechny soubory obsahují metadata Content Credentials (C2PA), která uvádějí, že vznikly s pomocí AI; u každého obrázku tvoří asi 6 kB, u ikony většinu její velikosti.

Scéna: ranní horské jezero, vrcholky v růžové záři a jejich odraz ve vodě, borovice vpravo a v popředí dřevěný stůl s notebookem (na obrazovce kód), hrnkem a skicákem s kresbou hor. Malířský vzhled dělají filtry SVG (šum, posun okrajů, rozostření a prolínání barev). Deska stolu má stejnou barvu jako stránka (#26323A), takže malba plynule přechází do webu.

Ikona `favicon.svg` je zjednodušená hora ve stejných barvách.

## Jak obrázky vyrobit znovu

Při úpravě malby se mění jen `src/hero-jezero.svg`. Ostatní soubory se z něj vyrobí takhle:

1. Otevři SVG v prohlížeči ve velikosti 1440 × 960 px a vyfoť ho s dvojnásobným rozlišením (2880 × 1920 px PNG).
2. Desktop: zmenši na šířku 2880, 1440 a 960 px a ulož jako WebP v kvalitě 72–78.
3. Mobil: vyřízni prostředek obrázku (vodorovně od 720 do 2160 px, celá výška), zmenši na 1080 × 1440 a 720 × 960 px a ulož jako WebP.
4. Náhled pro sdílení: vyřízni pás od 408 px shora do spodního okraje, zmenši na 1200 × 630 px a ulož jako JPG v kvalitě 84.

## Použití na webu

Úvodní malba se vkládá přes `<picture>`, aby si prohlížeč sám vybral výřez a velikost:

```html
<picture>
  <source media="(max-width: 760px)"
          srcset="assets/images/hero-jezero-mobil-720.webp 720w,
                  assets/images/hero-jezero-mobil-1080.webp 1080w"
          sizes="100vw">
  <img src="assets/images/hero-jezero-1440.webp"
       srcset="assets/images/hero-jezero-960.webp 960w,
               assets/images/hero-jezero-1440.webp 1440w,
               assets/images/hero-jezero-2880.webp 2880w"
       sizes="100vw" width="1440" height="960"
       alt="Malba: ranní výhled od stolu s notebookem na horské jezero, ve kterém se zrcadlí vrcholky hor."
       fetchpriority="high">
</picture>
```

## Odstraněné obrázky

Pixelové ilustrace starého webu (`pixel-computer.png`, `pixel-landscape.png`, `pixel-workspace.png`), náhledy starého webu, původní návrh a stará ikona terminálu byly 27. 10. 2026 odstraněny. Pořád jsou v historii Gitu ve větvi `main`.
