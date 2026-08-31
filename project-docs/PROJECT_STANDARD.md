# PROJECT STANDARD

**Informatika septima / 3. ročník gymnázia**

*Verze 1.1 - autorský standard, obsahový rámec a publikační pravidla pro tuto učebnici*

| Hlavní záměr | Vytvořit moderní webovou učebnici informatiky pro septimu osmiletého gymnázia / 3. ročník čtyřletého gymnázia. Učebnice má být publikovaná v MkDocs Material a obsahově pokrývat základy algoritmizace a programování desky Micro:bit podle ŠVP Moje škola. |
| --- | --- |

| Charakter projektu | Nejde o akademická skripta ani o dokumentaci k Micro:bitu. Výsledkem má být praktická učebnice, která vede žáka od pochopení problému přes zápis algoritmu až k vytvoření, otestování a vylepšení vlastního programu. |
| --- | --- |

## 1. Účel a rozsah projektu

Cílem je vytvořit profesionálně působící online učebnici pro 76 vyučovacích hodin informatiky.

Učebnice má vysvětlovat:

- co je algoritmus a kdy má smysl řešit problém algoritmicky,
- jak popsat zadání úlohy, vstupy, výstupy a podmínky řešení,
- jak převádět postup mezi přirozeným jazykem, diagramem a programem,
- jak rozdělit problém na menší části,
- jak používat podmínky, cykly, proměnné a seznamy,
- jak vytvořit, nahrát, spustit a otestovat program pro Micro:bit,
- jak pracovat se světelnými, zvukovými a senzorickými vstupy a výstupy,
- jak ladit program a rozpoznat problematická místa postupu,
- jak propojit dvě desky Micro:bit,
- jak připravit a obhájit jednoduchý skupinový projekt.

| Klíčový požadavek | Učebnice má být praktická, srozumitelná a přiměřená gymnaziálním žákům. Nemá působit jako seznam příkazů ani jako opis dokumentace k hardwaru. |
| --- | --- |

## 2. Závazné zdrojové materiály

Obsah učebnice stojí na těchto podkladech:

| Zdroj | Role v projektu |
| --- | --- |
| `resources/Moje_skola_osnovy_2_2022 (1).pdf`, strana PDF 170 | Závazný rámec pro výstupy a učivo předmětu Informatika septima. |
| `project-docs/PROJECT_STANDARD.md` | Interní autorský standard pro strukturu, tón a publikační pravidla. |

| Důležitý princip | ŠVP neurčuje přesné znění kapitol. Určuje požadované výstupy a učivo, které je potřeba převést do srozumitelné a praktické učebnice. |
| --- | --- |

## 3. Hlavní didaktický princip

Celá učebnice je postavená na tomto sledu:

1. pochopit problém a rozhodnout, zda je vhodný pro algoritmické řešení,
2. popsat zadání, vstupy, výstupy a podmínky,
3. zapsat postup přirozeným jazykem, diagramem nebo programem,
4. rozdělit problém na menší části,
5. použít základní programové konstrukce,
6. vytvořit program pro Micro:bit,
7. otestovat a odladit chování programu,
8. propojit program s reálným okolím pomocí senzorů a výstupů,
9. spolupracovat na projektu a vysvětlit zvolené řešení.

| Hlavní pravidlo | Nejdřív pochopit problém a navrhnout postup, až potom programovat. Micro:bit je prostředek pro ověření algoritmu v reálném světě. |
| --- | --- |

## 4. Charakter výsledné učebnice

Výsledná učebnice má působit jako soudobá školní publikace.

Požadované vlastnosti:

- srozumitelná čeština se správnou diakritikou,
- krátké a přehledné odstavce,
- jasné vysvětlení smyslu každého tématu,
- školní, praktické a experimentální příklady,
- postupné praktické úlohy,
- střídmé, ale účelné tabulky a diagramy,
- jednotná struktura napříč kapitolami,
- závěrečný projekt s Micro:bitem.

Nepoužívat:

- text bez české diakritiky,
- přehnaně marketingový nebo „AI-like“ tón,
- zbytečně abstraktní definice bez příkladu,
- příliš hutný text bez vizuálního členění,
- interní autorské poznámky v publikované části knihy,
- dlouhé návody k tlačítkům bez vysvětlení smyslu činnosti.

## 5. Aktuální struktura kurzu

Kniha je rozdělena do 10 hlavních kapitol:

1. Problém, postup a algoritmus
2. Zápis algoritmu
3. Vstupy, výstupy a podmínky
4. Cykly a opakování
5. První programy pro Micro:bit
6. Světelné a zvukové výstupy
7. Reakce na uživatele a okolí
8. Proměnné, senzory a data
9. Testování a ladění programu
10. Komunikace Micro:bitu a závěrečný projekt

| Poznámka ke struktuře | Kapitol je záměrně méně. Orientace v knize má být jednoduchá, ale uvnitř kapitol je možné pracovat s kratšími podkapitolami a praktickými úkoly. |
| --- | --- |

## 6. Lesson Authoring Guide

Při tvorbě nové kapitoly musí autor nebo AI nejdříve určit:

- jakou praktickou situaci kapitola řeší,
- jakou dovednost nebo pojem zavádí,
- na co kapitola navazuje,
- jaké výstupy ze ŠVP pokrývá,
- co má žák po přečtení umět vytvořit, vysvětlit nebo rozhodnout.

Kapitola má být psaná jako vedený výklad s praktickými příklady, ne jako encyklopedické heslo ani jako mechanický návod k programu.

### 6.1 Doporučený postup při tvorbě kapitoly

1. Projít relevantní požadavky ze ŠVP.
2. Ujasnit si praktický školní nebo projektový kontext.
3. Sepsat motivaci a výstup kapitoly.
4. Připravit výklad po menších logických blocích.
5. Doplnit tabulku, diagram, ukázkový program nebo praktický úkol tam, kde opravdu pomůže.
6. Uzavřít kapitolu tahákem, checklistem a krátkým shrnutím.

### 6.2 Jazyk a styl

- Psát česky.
- **Vždy používat správnou českou diakritiku ve studentském textu, navigaci, metadatech i autorských standardech.**
- Názvy souborů a URL mohou zůstat bez diakritiky kvůli stabilním odkazům.
- Používat přirozený učebnicový tón.
- Upřednostňovat konkrétní formulace před frázemi.
- Vysvětlovat pojmy jednoduše, ale ne zjednodušeně.
- Volit příklady ze školní praxe, běžných situací a jednoduchých experimentů s Micro:bitem.
- U moderních témat doplnit současný kontext, pokud je ŠVP formulováno obecně.

## 7. Šablona kapitoly

Aktuální standard kapitoly:

```markdown
# Kapitola X - Název

<div class="lesson-meta">
<strong>Doporučený čas:</strong> 6-8 vyučovacích hodin<br>
<strong>Výstup kapitoly:</strong> Jednou větou popiš, co má žák po kapitole umět.
</div>

## Motivace

Krátké vysvětlení, proč se téma učíme a k čemu je potřeba.

## Co se naučíš

- dovednost 1
- dovednost 2
- dovednost 3

## Výklad

Vedený výklad po menších logických blocích.

## Praktický úkol

Úkol, který vede k ověřitelnému výstupu.

## Tahák

Stručný přehled nejdůležitějších pojmů a kroků.

## Co už umím

Kontrolní seznam dovedností.

## Návaznost na ŠVP

- výstup nebo učivo ze ŠVP
- výstup nebo učivo ze ŠVP
```

## 8. Vizuální a typografický standard

Vizuální provedení je záměrně střídmé a školní.

Aktuální principy:

- theme `Material for MkDocs`,
- primární barva `blue`,
- akcent `teal`,
- přepínač `light / dark mode`,
- jednotné boxy, tabulky a odsazení,
- dobrá čitelnost na notebooku, tabletu i mobilu.

Sdílené CSS je v:

- `docs/assets/stylesheets/extra.css`

Používané prvky:

| Prvek | Účel |
| --- | --- |
| `.lesson-meta` | horní informační box kapitoly |
| Markdown tabulky | přehledy, srovnání a shrnutí |
| Mermaid diagramy | jednoduchá schémata procesů a algoritmů |

| Vizuální princip | Text musí být dobře čitelný, vzdušný a pravidelně členěný. Tabulky a diagramy mají výklad zpřehlednit, ne ho nahrazovat. |
| --- | --- |

## 9. Diagramy, tabulky a další výstupy

Pro tuto knihu platí:

- jednoduché procesy lze kreslit v Mermaid,
- algoritmy lze zapisovat přirozeným jazykem, pseudokódem, vývojovým diagramem nebo blokovým programem,
- tabulky používat pro srovnání, kontrolní seznamy a shrnutí,
- ukázkové programy držet malé a čitelné,
- obrázky používat jen tam, kde opravdu pomáhají.

| Doporučení | Pokud lze výstup rozumně vytvořit v Markdownu nebo Mermaid, má to přednost před rastrovým obrázkem. |
| --- | --- |

## 10. Standard závěrečného projektu

Závěrečný projekt má propojit hlavní oblasti učiva:

1. popis problému,
2. návrh algoritmu,
3. vstupy a výstupy,
4. podmínky a cykly,
5. proměnné a práce s daty,
6. senzory Micro:bitu,
7. světelné nebo zvukové výstupy,
8. testování a ladění,
9. případně komunikaci dvou desek,
10. prezentaci a obhajobu řešení.

Projekt má být přiměřený žákům septimy. Nemusí být rozsáhlý, ale má ukázat, že žák dokáže navrhnout postup, vytvořit funkční program, otestovat jej a srozumitelně vysvětlit.

## 11. Zásady pro zdroje a interní poznámky

Pro tuto knihu platí:

- zdrojové a metodické poznámky evidovat pouze v `project-docs/` nebo `README.md`,
- v publikované učebnici neuvádět interní redakční komentáře,
- zdroje používat jako podklad, ne jako text k přepisu,
- studentský text má být čistý, srozumitelný a s českou diakritikou.

| Redakční hranice | Co je interní podklad pro autora, nemá se automaticky objevovat v textu pro žáka. |
| --- | --- |

## 12. Repozitář a publikační konvence

Repo konvence:

| Cesta | Význam |
| --- | --- |
| `docs/` | publikovaná učebnice |
| `docs/cs/` | české kapitoly |
| `docs/assets/stylesheets/extra.css` | sdílené vizuální úpravy |
| `functions/_middleware.js` | Cloudflare Pages middleware pro Basic Auth ochranu publikovaného webu |
| `project-docs/` | interní projektová a autorská dokumentace |
| `resources/` | zdrojové podklady |

Publikace na Cloudflare Pages:

| Nastavení | Hodnota |
| --- | --- |
| Build command | `pip install -r requirements.txt && mkdocs build --strict` |
| Build output directory | `site` |
| Root directory | `/` |

Produkční web je chráněný Basic Auth middlewarem v `functions/_middleware.js`. V Cloudflare Pages musí být nastavené proměnné prostředí:

| Proměnná | Význam |
| --- | --- |
| `BASIC_USER` | Přihlašovací jméno. |
| `BASIC_PASS` | Heslo. |

Technické nastavení:

- `strict: true` se používá při buildu příkazem `mkdocs build --strict`,
- verze Pythonu je určena soubory `.python-version` a `runtime.txt`,
- `use_directory_urls` zůstává ve výchozím režimu MkDocs,
- `Material for MkDocs`,
- `pymdownx.superfences` pro Mermaid.

## 13. AI / Codex pravidla

Při práci na této učebnici platí:

- nejdříve analyzovat ŠVP a existující stav repozitáře,
- držet schválenou osnovu 10 kapitol,
- držet jednotný tón napříč kapitolami,
- vždy používat českou diakritiku v publikovaném i interním textu,
- nevkládat do publikované části interní autorské poznámky,
- nerozšiřovat osnovu bez důvodu,
- při větší změně osnovy nejdříve navrhnout úpravu v chatu.

| Důležitá zkušenost | U učebnic je konzistence důležitější než kreativní vylepšování každé kapitoly jiným stylem. |
| --- | --- |

## 14. Definition of Done

Kapitola nebo větší blok práce je hotový tehdy, když:

- odpovídá obsahovému cíli,
- pokrývá příslušné části ŠVP,
- drží se stejné struktury jako zbytek knihy,
- používá správný tón a terminologii,
- používá správnou českou diakritiku,
- má dostatečné členění, spacing a vizuální přehlednost,
- případné diagramy nebo tabulky skutečně pomáhají výkladu,
- build `mkdocs build --strict` projde bez chyby,
- změna je zařazená do navigace.

## 15. Shrnutí hlavního principu

Tato kniha stojí na jednoduché myšlence:

**Žák se nemá učit izolované bloky nebo příkazy, ale chápat, jak navrhnout postup, ověřit jej programem a zlepšovat podle výsledků testování.**

Proto má učebnice vést od:

- jasného popisu problému,
- přes návrh algoritmu,
- k programu pro Micro:bit,
- k testování, ladění a projektu,
- a nakonec ke schopnosti vlastní řešení vysvětlit a obhájit.
