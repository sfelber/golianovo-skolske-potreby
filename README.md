# Školské pomôcky · príprava a nákup

Interaktívny zoznam školských pomôcok pre žiakov základnej školy (1. – 9. ročník).
Aplikácia ti pomôže **pripraviť sa na nákup**: vyberieš ročníky, označíš čo už máš doma
a vygeneruješ čistý nákupný zoznam len s tým, čo naozaj treba kúpiť.

🔗 **Živá stránka:** <https://sfelber.github.io/golianovo-skolske-potreby/>

Celá aplikácia je jediný HTML súbor — funguje **offline**, bez inštalácie a bez prihlásenia.
Stav sa priebežne ukladá priamo v prehliadači.

---

## Ako to funguje — krok po kroku

Aplikácia má dva kroky, medzi ktorými prepínaš tlačidlami hore.

### Krok 1 — Príprava

1. **Vyber ročníky.** Hore v paneli klikni na číslo ročníka (1 – 9). Vybrať môžeš aj
   viac ročníkov naraz (napr. keď nakupuješ pre viac detí). Každý ročník má svoju farbu.
2. **Zadaj „už mám".** Pri položkách, ktorých treba viac kusov (napr. výkresy, zošity),
   sa zobrazí počítadlo *„Už mám:"*. Nastav koľko kusov už máš doma — aplikácia sama
   dopočíta, koľko ešte treba kúpiť.
3. **Odškrtni, čo máš doma.** Kliknutím na položku ju označíš ako *hotovú* (už ju
   netreba riešiť). Opätovným kliknutím označenie zrušíš.
4. **Generuj zoznam na nákup.** Tlačidlom *„Generovať zoznam na nákup"* prejdeš do
   Kroku 2. Vygeneruje sa čistý zoznam bez toho, čo už máš.

### Krok 2 — Nákup

- Zobrazí sa len to, **čo treba reálne kúpiť** (v správnych počtoch).
- Pri každej položke odškrtávaš, čo si hodil do košíka. Postup vidíš v ukazovateli hore.
- Späť do úpravy sa vrátiš tlačidlom *„← Úprava"*.
- Zoznam si môžeš **vytlačiť alebo uložiť ako PDF** (ikona tlačiarne).

---

## Prenos na iné zariadenie

Pripravíš si zoznam na počítači a nakupuješ s mobilom v ruke? Stav sa dá jednoducho
preniesť. Klikni na ikonu zdieľania hore vpravo a vyber jednu z možností:

- **QR kód** — na druhom zariadení ho naskenuješ a stav sa načíta automaticky.
- **Export / Import JSON** — stav uložíš ako malý súbor a prenesieš ho (AirDrop,
  WhatsApp, e-mail, Disk…), na druhom zariadení ho naimportuješ.
- **Kopírovať do schránky** — stav skopíruješ ako text a vložíš ho pri importe
  (praktické najmä na mobile).

Prenos funguje **offline** aj medzi rôznymi zariadeniami a operačnými systémami.

---

## Ako čítať číslo zošita

Číslo na zošite hovorí, aký zošit kúpiť:

| Číslica | Význam | Hodnoty |
|--------|--------|---------|
| **1.** | formát | 4 → A4, 5 → A5, 6 → A6 |
| **2.** | počet listov | číslo × 10 (napr. 2 → 20 listov) |
| **posledná** | liniatúra | 0 = čistý, 1 → 20 mm, 2 → 16 mm, 3 → 12 mm, 4 → 8 mm, 5 → štvorček 5×5 mm, 10 → štvorček 10×10 mm |

Príklad: **zošit č. 513** = A5, ~10 listov, liniatúra 12 mm.

---

## Praktické rady k nákupu

- Všetky trvalé pomôcky, odev a obuv **označ priezviskom dieťaťa**.
- Prezuvky musia mať **uzavretú pätu alebo remienok** — nie nasúvacie šľapky.
- Farby a štetce kupuj radšej od českých/nemeckých výrobcov — čínske bývajú nekvalitné.
- **Obaly** na zošity a učebnice dokúp až po ich založení, podľa počtu a veľkosti.
- Nezabudni: pomôcky treba mať pripravené **do 1. septembra**.

---

## Časté otázky

**Stratím stav, keď zavriem prehliadač?**
Nie. Stav sa priebežne ukladá v prehliadači, takže môžeš pokračovať neskôr. Ak chceš
istotu (alebo prenos na iné zariadenie), použi Export / QR kód.

**Funguje to bez internetu?**
Áno. Po prvom načítaní stránka funguje aj offline.

**Vybral som viac ročníkov — čo sa stane?**
Počty sa sčítajú a pri každej položke vidíš, koľko z nej pripadá na ktorý ročník
(farebne odlíšené) aj celkový súčet.

---

## Technické poznámky

- Jeden statický **HTML súbor** (`index.html`), bez backendu.
- Ukladanie stavu: `window.storage` s poistkou cez `localStorage`.
- Prenos stavu: QR kód (komprimovaný LZ-String v URL) alebo JSON export/import.
- Hostované cez **GitHub Pages**.

