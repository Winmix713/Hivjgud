# AI Coding Agent Rules

## Projektkontekstus

A projekt célját és a célcsoportot a `PRODUCT.md` tartalmazza.

A vizuális rendszer elsődleges forrása a `DESIGN.md`.

Az AI coding agent minden UI-feladat előtt köteles ellenőrizni:

- `PRODUCT.md`
- `DESIGN.md`
- az érintett feature vagy page briefet;
- a releváns referenciaanyagokat;
- a meglévő komponenseket.

---

## Általános szabályok

- Ne hozz létre új vizuális nyelvet dokumentált indok nélkül.
- Ne használj új színt, fontot, radiust vagy shadow-t token nélkül.
- Ne másold le pixelpontosan a referenciákat.
- Ne használj generikus, termékidegen illusztrációt.
- Ne tervezz újra működő komponenseket szükségtelenül.
- Először a meglévő komponenseket és tokeneket keresd meg.
- A módosítás legyen a lehető legkisebb, amely megoldja a problémát.
- A kritikus döntéseket röviden dokumentáld.

---

## Technológiai szabályok

- Stack: `[TECHNOLÓGIAI STACK]`
- Styling: `[CSS / Tailwind / CSS Modules / styled-components]`
- Komponensrendszer: `[KOMPONENSKÖNYVTÁR]`
- Tesztelés: `[TESZTELÉSI ESZKÖZÖK]`
- Lint és formázás: `[ESLINT / PRETTIER / EGYÉB]`

A kódot a meglévő projektstruktúrához igazítsd.

Ne vezess be új függőséget, ha a feladat meglévő eszközökkel megoldható.

---

## Komponenshasználat

Új komponens létrehozása előtt:

1. keresd meg, létezik-e megfelelő komponens;
2. ellenőrizd annak variánsait;
3. használd a meglévő tokeneket;
4. csak indokolt esetben hozz létre új komponenst;
5. az új komponenshez adj állapotokat és használati szabályt.

Minden interaktív komponens támogassa:

- a default állapotot;
- a hover állapotot;
- az active állapotot;
- a `focus-visible` állapotot;
- a disabled állapotot;
- szükség esetén a loading és error állapotot.

---

## Accessibility minimum

Minden felületnek:

- szemantikus HTML-t kell használnia;
- billentyűzettel kezelhetőnek kell lennie;
- látható fókuszállapotot kell biztosítania;
- megfelelő kontrasztot kell használnia;
- legalább `44 × 44px` érintési célokat kell alkalmaznia;
- nem támaszkodhat kizárólag színre;
- megfelelő labelt és hibajelzést kell biztosítania;
- a képekhez megfelelő alt szöveget kell adnia.

Ne használj `div` elemet button vagy link helyett.

---

## Responsive minimum

Minden új UI-t ellenőrizni kell:

- mobilnézetben;
- tablet nézetben;
- desktop nézetben;
- hosszú és rövid szöveggel;
- billentyűzettel;
- zoomolt nézetben;
- loading és error állapotban.

A layout ne függjön kizárólag egyetlen viewportmérettől.

---

## UI-minőségi szabályok

Kerüld:

- indokolatlan gradienteket;
- glow-effekteket;
- túlzott shadow-használatot;
- véletlenszerű badge-eket;
- generikus 3D illusztrációkat;
- túl sok azonos kártyát;
- üres marketingállításokat;
- dokumentálatlan motiont.

Előnyben részesítsd:

- a világos hierarchiát;
- a surface- és spacing-alapú strukturálást;
- a valódi termékbizonyítékot;
- a visszafogott elevationt;
- a konzisztens tipográfiát;
- a termékhez kapcsolódó tartalmat.

---

## Módosítási folyamat

Minden UI-módosításnál:

1. olvasd el a releváns dokumentációt;
2. azonosítsd a konkrét problémát;
3. keresd meg a legkisebb megfelelő módosítást;
4. implementáld a módosítást;
5. futtasd a lintet és a teszteket;
6. ellenőrizd a responsive viselkedést;
7. ellenőrizd a billentyűzetes működést;
8. készíts rövid összefoglalót a változásról.

Ne módosíts egyszerre több, egymástól független vizuális területet review nélkül.

---

## Definition of Done

A feladat akkor kész, ha:

- a megfelelő dokumentációt követte;
- meglévő tokeneket és komponenseket használt;
- nincs dokumentálatlan új vizuális döntés;
- működik a támogatott breakpointokon;
- működik billentyűzettel;
- rendelkezik látható fókuszállapottal;
- a loading, error és empty state kezelve van;
- a tesztek és lint ellenőrzések sikeresek;
- a design critique elvégezhető;
- a módosítás röviden dokumentálva lett.
