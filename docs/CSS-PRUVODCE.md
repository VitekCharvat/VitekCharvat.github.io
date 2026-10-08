# Jak funguje CSS tohoto portfolia

HTML popisuje obsah. Bootstrap dodává hotové stavební části a rozložení. `style.css` je načtený až za ním a přidává pixelový vzhled. Níže jsou vysvětlené skutečné příklady z projektu.

## 1. Bootstrap: dvanáct sloupců

```html
<div class="row g-4">
  <div class="col-12 col-md-6 col-lg-4">…</div>
</div>
```

`row` vytvoří řádek mřížky, který má dvanáct dílů. `col-12` zabere na mobilu celý řádek, `col-md-6` od 768 px polovinu a `col-lg-4` od 992 px třetinu. Karty tak automaticky přecházejí z jednoho do dvou a potom tří sloupců. `g-4` přidává mezery mezi sloupci i řádky. `container` omezuje šířku obsahu a vycentruje ho.

`d-flex` zapíná flexbox. `align-items-center` zarovnává položky napříč jeho hlavní osou. `gap-3` přidává rozestupy. `flex-wrap` dovoluje zalomení. Tyto třídy už poskytuje Bootstrap, proto je znovu nepíšeme do vlastního CSS.

## 2. Proměnné a dědičnost

```css
:root { --green: #b2ec83; }
.project-link { color: var(--green); }
```

`--green` je pojmenovaná hodnota. `var(--green)` ji dosadí. Přepsáním jediné proměnné změníš všechny prvky, které ji používají. `:root` je kořen dokumentu, takže proměnné jsou dostupné v celé stránce. Názvy začínající `--bs-` jsou proměnné Bootstrapu. Například `--bs-body-font-family` nastavuje výchozí písmo stránky.

Vlastní styl načítáme poslední, ale neznamená to, že automaticky přepíše úplně vše. Rozhoduje také přesnost selektoru a `!important`. Proto barvy Bootstrap tlačítek měníme přes jejich proměnné a rozestupy nepřebíjíme zbytečnými pravidly.

## 3. Plynulá velikost textu: clamp()

```css
font-size: clamp(1.4rem, 4.2vw, 3.35rem);
```

Text chce mít velikost `4.2vw`, tedy 4,2 % šířky okna. `clamp()` ho ale omezí: nejméně `1.4rem`, nejvíce `3.35rem`. `rem` vychází z velikosti písma kořene dokumentu, obvykle 16 px. Nadpis se tak přizpůsobí obrazovce a jméno se vejde na jeden řádek.

## 4. Velikost a vycentrování ilustrace

```css
.hero-art { max-width: 25rem; margin-inline: auto; }
.hero-art img { display: block; width: 100%; height: auto; image-rendering: pixelated; }
```

`max-width` omezuje ilustraci na 25 rem, běžně 400 px. `margin-inline: auto` rozdělí volné místo vlevo a vpravo rovnoměrně, takže obrázek zůstane uprostřed svého sloupce. Bootstrap dává textu od šířky `lg` sedm dílů a ilustraci pět dílů mřížky. Na menších obrazovkách jsou pod sebou.

## 5. Ostrý herní stín

```css
box-shadow: 4px 4px 0 #06111c;
```

První hodnota posouvá stín doprava, druhá dolů. Třetí určuje rozmazání. Nula vytvoří ostrý stín připomínající starou herní grafiku. `text-shadow` funguje podobně pro samotná písmena. Stíny zůstávají u ikony v sekci O mně a u náhledů projektů. Úvodní ilustrace je bez rámečku.

## 6. Obrázky a pozadí

`width: 100%` přizpůsobí obrázek šířce rodiče, `height: auto` zachová původní proporce. Rozměry v HTML pomáhají prohlížeči rezervovat místo ještě před načtením obrázku. `image-rendering: pixelated` při změně rozměrů preferuje ostré pixely; samo o sobě nezmění fotografii v pixel art. PNG v úvodu má průhledné pozadí, a tak přirozeně zapadá do stránky.

V patičkovém panelu je přes krajinu položené průhledné tmavé pozadí:

```css
background-image:
  linear-gradient(rgba(9, 24, 39, 0.15), rgba(9, 24, 39, 0.35)),
  url("assets/images/pixel-landscape.png");
```

První vrstva je nahoře. Poslední číslo v `rgba()` znamená neprůhlednost od 0 do 1. Přechod ztmaví krajinu, takže text zůstává čitelný. Cesta `url()` v CSS se počítá vzhledem k umístění CSS souboru.

## 7. Odkazy ve stejné výšce

Karta má Bootstrap `h-100`. Její tělo používá `d-flex flex-column`, takže obsah skládá shora dolů. Třída `mt-auto` na odkazu spotřebuje zbývající volný prostor nad odkazem. Odkazy tak končí u spodku karet i tehdy, když mají popisy jinou délku.

## 8. Zvýraznění odkazů bez JavaScriptu

```css
.project-link:hover { text-decoration: underline; }
```

`:hover` platí při najetí myší. Odkaz na projekt se podtrhne, takže je vidět, na co míříš. Tlačítka mění barvu pomocí Bootstrapu a našich barevných proměnných. Karty ani tlačítka se neposouvají. Na dotykové obrazovce není najetí myší potřeba, odkaz zůstává běžně použitelný.

## 9. Mobilní rozložení a přístupnost

`@media (max-width: 575.98px)` spustí pravidla jen v menším okně. Zmenšujeme odsazení a nadpisy; sloupce dál řídí Bootstrap. Navigace se zalomí, nepotřebuje skript ani rozbalovací nabídku.

`:focus-visible` přidává obrys odkazu při ovládání klávesnicí. Vyzkoušej Tab a Enter. První odkaz „Přeskočit na obsah“ se objeví po stisku Tab a přeskočí navigaci. Dekorativní ikony mají `aria-hidden="true"`, aby je čtečka nečetla jako další obsah.

`@media (prefers-reduced-motion: reduce)` respektuje systémové omezení pohybu. Vypne plynulé posouvání stránky i barevný přechod tlačítek.

## Malé cvičení

Změň `--green`, otevři stránku a sleduj, co se přebarvilo. Potom změň první projekt z `col-lg-4` na `col-lg-6` a zkus různě široké okno. Nakonec změny vrať. Tím uvidíš rozdíl mezi vlastním vzhledem a Bootstrap rozložením.
