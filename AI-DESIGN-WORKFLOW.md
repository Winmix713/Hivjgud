# AI-Assisted Frontend Design Workflow

## Cél

Ez a dokumentum szabályozza, hogyan tervezzünk, építsünk, értékeljünk és finomítsunk frontend felületeket AI coding agentek segítségével.

A cél:

- következetes brand- és design system létrehozása;
- a felület valódi termékkontekstushoz igazítása;
- a generikus, „AI-generated” vizuális minták elkerülése;
- a design iteráció dokumentálása;
- a reszponzív és akadálymentes működés biztosítása;
- a vizuális minőség ismételhető és auditálható javítása.

---

## Alapelv

Ne általános kéréssel indítsd a fejlesztést:

> Build a beautiful modern landing page.

A promptnak tartalmaznia kell:

- a termék célját;
- a célcsoportot;
- a fő felhasználói feladatot;
- az üzleti vagy konverziós célt;
- a vizuális rendszert;
- a használható komponenseket;
- a referenciákat;
- a kerülendő megoldásokat;
- az elfogadási kritériumokat.

Minden fontos UI-feladat előtt ellenőrizd az alábbi fájlokat:

1. `PRODUCT.md`
2. `DESIGN.md`
3. `AGENTS.md`
4. releváns referenciaanyagok
5. az adott feature briefje

---

## Standard workflow

1. `PRODUCT.md` létrehozása vagy frissítése
2. `DESIGN.md` létrehozása vagy frissítése
3. `AGENTS.md` szabályainak rögzítése
4. Referenciák összegyűjtése és annotálása
5. Feature vagy page brief elkészítése
6. Első implementáció
7. Design critique
8. Célzott javítások
9. UI polish
10. Implementációs és akadálymentességi audit
11. Automatikus detektálás
12. Manuális responsive review

---

## Impeccable használata

| Feladat | Parancs | Cél |
|---|---|---|
| Projekt indítása | `/impeccable init` | Kezdeti design- és termékkontekstus létrehozása |
| Új feature építése | `/impeccable craft` | Új képernyő vagy komponens strukturált létrehozása |
| Design review | `/impeccable critique` | Vizuális és UX-problémák azonosítása |
| UI finomítása | `/impeccable polish` | Spacing, hierarchia, ritmus és részletek javítása |
| Implementáció ellenőrzése | `/impeccable audit` | Reszponzivitás, konzisztencia és hozzáférhetőség ellenőrzése |
| Élő iteráció | `/impeccable live` | Variánsok kipróbálása futó alkalmazásban |
| Design dokumentálása | `/impeccable document` | Meglévő UI-ból `DESIGN.md` létrehozása |
| Automatikus detektálás | `npx impeccable detect` | Gyakori design- és implementációs problémák keresése |

---

## Taste Skill

A Taste Skill az AI által generált frontendek vizuális minőségét és változatosságát javítja.

Nem helyettesíti a projekt design systemét. A `DESIGN.md` és az `AGENTS.md` mindig elsőbbséget élvez.

### Hangolási paraméterek

| Paraméter | Alacsony érték | Magas érték |
|---|---|---|
| `DESIGN_VARIANCE` | Konzervatív, stabil layout | Karakteres, aszimmetrikus, art-directed layout |
| `MOTION_INTENSITY` | Finom átmenetek | Erősebb scroll- és komponensmozgások |
| `VISUAL_DENSITY` | Sok whitespace | Információsűrű, product-first felület |

### Ajánlott értékek

| Felülettípus | Variance | Motion | Density |
|---|---:|---:|---:|
| Prémium marketing landing | 6–8 | 3–5 | 3–5 |
| SaaS/product landing | 4–6 | 2–4 | 5–7 |
| Dashboard/admin | 2–4 | 1–3 | 6–8 |
| Prémium termékbemutató | 4–6 | 2–4 | 2–4 |

---

## Referenciaalapú tervezés

Minden fontos UI-feladathoz használj legalább egy releváns referenciát:

- screenshot;
- URL;
- Figma frame;
- annotált kép;
- meglévő belső komponens;
- konkrét `DESIGN.md`-szabály.

A referencia nem pixelpontos másolásra szolgál. A cél:

- a layout-ritmus átvétele;
- az információs hierarchia megértése;
- a komponensarányok meghatározása;
- a megfelelő vizuális hangulat kialakítása;
- az art direction pontosítása.

A márkaazonosító elemeket, szövegeket, színeket és képeket nem szabad automatikusan másolni.

---

## Anti-AI-slop szabályok

### Kerülendő megoldások

- Indokolatlan lila vagy kék gradient.
- Dekoratív glow CTA-kon és headline-okon.
- Shadow minden komponensen.
- Véletlenszerű floating badge-ek.
- Túlméretezett eyebrow szövegek.
- Generikus 3D illusztrációk.
- Túlzott glassmorphism vagy blur.
- Egyforma feature-card rácsok minden szekcióban.
- A termékhez nem kapcsolódó AI-képek.
- Konkrét bizonyíték nélküli marketingállítások.
- Döntést nem támogató pricing section.
- Az első generált változat automatikus elfogadása.

### Elvárt alternatívák

| Probléma | Előnyben részesített megoldás |
|---|---|
| Dekoratív gradient | Surface-váltás, képi atmoszféra vagy tipográfiai kontraszt |
| Generikus illusztráció | Valódi product UI, releváns mockup vagy termékfotó |
| Sok shadow | Border, surface hierarchy, spacing vagy kontraszt |
| Véletlen badge | Csak valós státusz, kategória vagy bizalomjelzés |
| Általános „modern” prompt | Konkrét layout-, token- és komponensutasítás |
| Egyforma card-rács | Tartalomhoz igazított, változatos kompozíció |

---

## Critique szabályok

A critique során legfeljebb öt, legnagyobb hatású problémát azonosíts.

Minden problémához adj:

1. rövid diagnózist;
2. magyarázatot, hogy miért probléma;
3. konkrét javítási javaslatot;
4. érintett komponenst vagy tokent;
5. prioritást: `high`, `medium` vagy `low`.

Ne tervezd újra az egész oldalt, ha néhány célzott módosítás is elég.

---

## Definition of Done

Egy UI-feladat akkor kész, ha:

- összhangban van a `PRODUCT.md` céljaival;
- a `DESIGN.md` tokenjeit használja;
- nem vezet be dokumentálatlan vizuális nyelvet;
- reszponzív minden támogatott breakpointon;
- működik billentyűzettel;
- megfelelő kontrasztot biztosít;
- látható fókuszállapotokat használ;
- szemantikus HTML-t alkalmaz;
- a képek megfelelő alt szöveget kapnak;
- a CTA-k és a vizuális hierarchia egyértelműek;
- nem használ termékidegen vizuális elemeket;
- átment critique és audit körön;
- legalább egy célzott iteráción átesett.
