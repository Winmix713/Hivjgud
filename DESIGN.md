# Design System

## Designirány

A felület karaktere:

- visszafogottan prémium;
- világos információs hierarchiájú;
- termék- és tartalomközpontú;
- funkcionális, nem dekoratív;
- alacsony vizuális zajú;
- reszponzív és akadálymentes.

A vizuális rendszer célja, hogy a felhasználó gyorsan megértse:

1. mit lát;
2. miért fontos;
3. mit tehet ezután.

---

## Alapelvek

- Egy szekciónak legyen egyértelmű elsődleges fókusza.
- A termék vagy valódi tartalom legyen domináns, ne a dekoráció.
- A whitespace a hierarchia része.
- A shadow kivétel, nem alapértelmezett.
- A border és surface-váltás előnyben részesítendő.
- Új színt vagy radiust csak dokumentált indokkal vezess be.
- A pill forma funkcionális elemekhez használható.
- A UI chrome nem versenyezhet a fő tartalommal.
- A motion támogassa a megértést, ne terelje el a figyelmet.

---

## Színtokenek

### Light mode

| Token | Érték | Használat |
|---|---|---|
| `--color-bg` | `#FFFFFF` | Elsődleges háttér |
| `--color-surface` | `#F7F7F5` | Másodlagos felület |
| `--color-surface-raised` | `#FFFFFF` | Kiemelt vagy lebegő felület |
| `--color-text` | `#171717` | Elsődleges szöveg |
| `--color-text-muted` | `#686868` | Másodlagos szöveg |
| `--color-text-subtle` | `#8A8A8A` | Caption és utility szöveg |
| `--color-border` | `#E5E5E2` | Hairline border |
| `--color-accent` | `#1D5CFF` | Elsődleges interakció |
| `--color-accent-hover` | `#164BD1` | Hover állapot |
| `--color-accent-soft` | `#EAF0FF` | Enyhe accent háttér |
| `--color-success` | `#18794E` | Sikeres állapot |
| `--color-warning` | `#9A6700` | Figyelmeztetés |
| `--color-danger` | `#C6362C` | Hiba vagy veszély |

### Színhasználati szabályok

- Az accent szín elsődlegesen interaktív elemekhez tartozik.
- Ne használj új accent színt pusztán dekorációért.
- A hiba-, siker- és figyelmeztető színekhez ne kizárólag színt használj.
- A sötét felületekhez külön ellenőrizd a kontrasztot.
- Gradient csak dokumentált brand- vagy tartalmi indokkal használható.

---

## Tipográfia

### Betűcsaládok

```css
--font-sans: "Inter", "Helvetica Neue", Arial, sans-serif;
--font-display: "Inter", "Helvetica Neue", Arial, sans-serif;
--font-mono: "SFMono-Regular", Consolas, monospace;
```

### Tipográfiai skála

| Token | Méret | Line height | Használat |
|---|---:|---:|---|
| `--text-display` | `clamp(3rem, 7vw, 6.5rem)` | `0.95` | Hero headline |
| `--text-h1` | `clamp(2.5rem, 5vw, 4.5rem)` | `1.0` | Oldal főcíme |
| `--text-h2` | `clamp(2rem, 4vw, 3.25rem)` | `1.05` | Szekciócím |
| `--text-h3` | `1.5rem` | `1.15` | Kártya- vagy blokkcím |
| `--text-body-lg` | `1.25rem` | `1.5` | Lead szöveg |
| `--text-body` | `1rem` | `1.55` | Törzsszöveg |
| `--text-small` | `0.875rem` | `1.45` | Másodlagos szöveg |
| `--text-caption` | `0.75rem` | `1.35` | Caption, utility, metadata |

### Tipográfiai szabályok

- Legfeljebb négy–öt szövegszerepet használj egy komponensben.
- A display szöveg legyen karakteres, de ne veszítse el az olvashatóságát.
- Nagy headline esetén megengedett a finom negatív letter-spacing.
- Kis méretű szövegnél ne használj negatív letter-spacinget.
- A body text maximális szélessége általában `65ch`.
- A headline ne legyen indokolatlanul hosszú.

---

## Spacing

Az alap spacing rendszer 4 pixeles egységre épül.

| Token | Érték |
|---|---:|
| `--space-1` | `0.25rem` |
| `--space-2` | `0.5rem` |
| `--space-3` | `0.75rem` |
| `--space-4` | `1rem` |
| `--space-5` | `1.25rem` |
| `--space-6` | `1.5rem` |
| `--space-8` | `2rem` |
| `--space-10` | `2.5rem` |
| `--space-12` | `3rem` |
| `--space-16` | `4rem` |
| `--space-20` | `5rem` |
| `--space-24` | `6rem` |
| `--space-32` | `8rem` |

### Layoutszabályok

- A komponensek belső paddingje tokenből származzon.
- A grid gutter ne legyen véletlenszerű.
- A nagyobb szekciók kapjanak valódi vertikális ritmust.
- Ne tölts ki minden üres területet új komponenssel.
- Mobilon a spacing léptékét szükség esetén csökkentsd, de ne szüntesd meg a hierarchiát.

---

## Layout

### Container

```css
--container-max: var(--container-max);
--container-padding: clamp(1rem, 4vw, 4rem);
```

Ajánlott alapértékek:

- maximális szélesség: `1200–1440px`;
- mobil oldalsó padding: `16px`;
- tablet oldalsó padding: `24px`;
- desktop oldalsó padding: `32–64px`.

### Grid

- Marketing layout: 12 oszlopos grid.
- Product layout: 8 vagy 12 oszlopos grid.
- Dashboard layout: sűrűbb, funkcionális grid.
- Mobilon a komponensek alapértelmezett elrendezése egyoszlopos.

---

## Radius

| Token | Érték | Használat |
|---|---:|---|
| `--radius-sm` | `0.375rem` | Input, kis control |
| `--radius-md` | `0.625rem` | Button, kártya |
| `--radius-lg` | `1rem` | Kiemelt panel |
| `--radius-pill` | `999px` | Chip, filter, pill CTA |

Szabályok:

- Ne használj minden elemhez más radiusértéket.
- A pill forma csak funkcionális elemhez használható.
- A teljes szélességű szekciókat ne kerekítsd indokolatlanul.
- A radius ne helyettesítse a layout-hierarchiát.

---

## Elevation

Alapértelmezett állapotban ne használj shadow-t.

Előnyben részesített hierarchia:

1. spacing;
2. eltérő surface-szín;
3. hairline border;
4. csak szükség esetén shadow.

Tiltott alapértelmezések:

- CTA glow;
- text shadow;
- minden kártyán azonos shadow;
- dekoratív blur;
- indokolatlan glassmorphism.

---

## Komponensek

### Button

Állapotok:

- default;
- hover;
- active;
- focus-visible;
- disabled;
- loading.

Szabályok:

- minimum érintési cél: `44 × 44px`;
- legyen egyértelmű primary és secondary változat;
- ne használj egyszerre több azonos súlyú primary CTA-t;
- a loading állapotban maradjon érthető a művelet.

### Card

A kártya csak akkor használható, ha a tartalom valóban önálló egységet alkot.

Ne használj kártyát:

- pusztán dekorációként;
- minden feature automatikus konténereként;
- olyan tartalomnál, amelyet egyszerű spacinggel is el lehet választani.

### Badge és chip

Csak az alábbi esetekben használható:

- státusz;
- kategória;
- mennyiség;
- szűrő;
- bizalmi vagy termékinformáció.

### Modal és dialog

- használj szemantikus dialogot;
- legyen bezárható billentyűzettel;
- fókusz kerüljön a dialogba;
- a háttér ne legyen interaktív, ha modal állapot van.

---

## Motion

Alapértékek:

- finom hover transition;
- rövid opacity és transform átmenetek;
- mozgás csak funkcionális vagy narratív céllal;
- `prefers-reduced-motion` támogatása.

Kerüld:

- folyamatos, figyelemelterelő animációk;
- dekoratív parallax túlhasználata;
- minden elem külön animálását;
- motion használatát tartalmi hierarchia helyett.

---

## Képhasználat

A képek:

- kapcsolódjanak közvetlenül a termékhez;
- támogassák a tartalmi hierarchiát;
- rendelkezzenek megfelelő alt szöveggel;
- ne legyenek pusztán dekoratív helykitöltők;
- ne okozzanak layout shiftet.

Előnyben részesített vizuálok:

- valódi product UI;
- releváns screenshot;
- használati helyzetet bemutató kép;
- termékhez kapcsolódó diagram;
- megfelelően art-directed fotó.

---

## Responsive szabályok

Minimum támogatott nézetek:

- mobil: `320px+`;
- tablet: `768px+`;
- desktop: `1024px+`;
- nagy desktop: `1440px+`.

A mobilnézet nem az asztali layout egyszerű összenyomása.

Ellenőrizd:

- a navigációt;
- a CTA-k egymás alatti elrendezését;
- a headline tördelését;
- a grid oszlopait;
- a képek arányát;
- a táblázatok és pricing blokkok olvashatóságát;
- a touch targetek méretét.

---

## Do / Don't

### Do

- Használj valódi termékkontekstust.
- Tartsd meg az egyértelmű vizuális fókuszt.
- Használj dokumentált tokeneket.
- Részesítsd előnyben a surface-alapú hierarchiát.
- Adj minden interaktív elemnek látható állapotokat.
- Ellenőrizd mobilon és billentyűzettel is.

### Don't

- Ne használj véletlenszerű gradientet.
- Ne használj indokolatlan glow-t.
- Ne alkalmazz mindent kártyaként.
- Ne vezess be dokumentálatlan színt.
- Ne használj generikus illusztrációt termékbizonyíték helyett.
- Ne fogadd el az első AI-generált változatot review nélkül.
