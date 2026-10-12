# Návrh backlogu EL3 podle ŠVP

Tento dokument navrhuje Jira backlog pro učebnici **Informatika EL3** podle uložené mapy ŠVP. Všechny navržené tickety mají label `el3`.

Zdroj ŠVP: [SVP_INFORMATIKA_3_ROCNIK_MAPA.md](SVP_INFORMATIKA_3_ROCNIK_MAPA.md)

## Navržené komponenty

Pokud v Jira existují odpovídající komponenty, doporučené přiřazení je:

| Komponenta | Použití |
| --- | --- |
| prezentace | kapitoly a úkoly k prezentačnímu softwaru, slidům, diagramům, datům, předvedení a spolupráci |
| algoritmizace | algoritmus, dekompozice, větvení, rozhodovací diagram, opakování a kontrola |
| multimediální dokumenty | text, obraz, zvuk, video, odkazy, interaktivní vazby, publikování |
| kancelářský software | import, export, vkládání objektů a propojení dokumentu, tabulky a prezentace |

Pokud některá komponenta v Jira neexistuje, použít nejbližší dostupnou komponentu a novou nezakládat bez potvrzení.

## Story návrhy

### Prezentace

| Ticket | Typ | Komponenta | Label | Zdroj | Pokrytí ŠVP |
| --- | --- | --- | --- | --- | --- |
| `[EL3] Lekce 1 - Prezentace jako sdělení` | Story | prezentace | `el3` | `docs/cs/01-prezentace-jako-sdeleni.md` | tvorba prezentace, práce s prezentačním softwarem, uspořádání snímků |
| `[EL3] Lekce 2 - Publikum, message a příprava` | Story | prezentace | `el3` | `docs/cs/02-publikum-message-a-priprava.md` | tvorba prezentace, volba obsahu, spolupráce |
| `[EL3] Lekce 3 - Vizuální příběh a diagramy` | Story | prezentace | `el3` | `docs/cs/03-vizualni-pribeh-a-diagramy.md` | grafická schémata, rozhodovací diagram, uspořádání informací |
| `[EL3] Lekce 4 - Data, grafy a důkazy` | Story | prezentace | `el3` | `docs/cs/04-data-grafy-a-dukazy.md` | grafy, důkazy, objekty z jiných aplikací |
| `[EL3] Lekce 5 - Design účinného slidu` | Story | prezentace | `el3` | `docs/cs/05-design-ucinneho-slidu.md` | tvorba prezentace, uspořádání snímků, čitelnost |
| `[EL3] Lekce 6 - Předvedení a týmový projekt` | Story | prezentace | `el3` | `docs/cs/06-predvedeni-a-tymovy-projekt.md` | časování, efekty, předvedení, týmová spolupráce |
| `[EL3] Úkol 1 - Prezentace pozpátku` | Story | prezentace | `el3` | `docs/ukoly/ukol-1-prezentace-pozpatku.md` | tvorba prezentace, redukce obsahu, práce se slidementem |
| `[EL3] Úkol 2 - Diagramy a struktury` | Story | prezentace | `el3` | `docs/ukoly/ukol-2-diagramy/` | grafická schémata, struktura, průběh, rozhodovací diagram, skupiny a překryvy |

### Algoritmizace

| Ticket | Typ | Komponenta | Label | Zdroj | Pokrytí ŠVP |
| --- | --- | --- | --- | --- | --- |
| `[EL3] Lekce 7.1 - Algoritmus, dekompozice a abstrakce` | Story | algoritmizace | `el3` | `docs/cs/07-algoritmy-postupy-a-rozhodovani.md` | principy algoritmizace, vlastnosti algoritmu, rozklad úlohy na menší kroky |
| `[EL3] Lekce 7.2 - Rozhodování, větvení a opakování` | Story | algoritmizace | `el3` | `docs/cs/07-algoritmy-postupy-a-rozhodovani.md` | podmínky, větve ano/ne, smyčka, návrat v procesu, kontrola výsledku |
| `[EL3] Úkol 3 - Rozhodovací diagram reálného procesu` | Story | algoritmizace | `el3` | plánovaný úkol | sestavení algoritmu konkrétní úlohy, dekompozice, znázornění algoritmu |

### Multimediální dokumenty

| Ticket | Typ | Komponenta | Label | Zdroj | Pokrytí ŠVP |
| --- | --- | --- | --- | --- | --- |
| `[EL3] Lekce 8.1 - Multimediální dokument jako celek` | Story | multimediální dokumenty | `el3` | `docs/cs/08-multimedialni-dokumenty-a-publikovani.md` | návrh dokumentu, spojení textu, obrazu, zvuku, videa a odkazů |
| `[EL3] Lekce 8.2 - Média, odkazy a interaktivní vazby` | Story | multimediální dokumenty | `el3` | `docs/cs/08-multimedialni-dokumenty-a-publikovani.md` | vkládání a formátování obrázků, zvuková a obrazová složka, hypertextové odkazy |
| `[EL3] Úkol 4 - Krátký multimediální dokument` | Story | multimediální dokumenty | `el3` | plánovaný úkol | tvorba multimediálního dokumentu, export, sdílení a kontrola výstupu |

### Kancelářský software a propojování aplikací

| Ticket | Typ | Komponenta | Label | Zdroj | Pokrytí ŠVP |
| --- | --- | --- | --- | --- | --- |
| `[EL3] Lekce 9.1 - Kancelářský balík jako propojené prostředí` | Story | kancelářský software | `el3` | `docs/cs/09-propojovani-kancelarskych-aplikaci.md` | aplikace tvořící kancelářský software jako celek, dokument, tabulka a prezentace |
| `[EL3] Lekce 9.2 - Import, export a objekty z jiných aplikací` | Story | kancelářský software | `el3` | `docs/cs/09-propojovani-kancelarskych-aplikaci.md` | import/export dat, vkládání tabulek, grafů a dalších objektů |
| `[EL3] Úkol 5 - Jeden obsah ve třech aplikacích` | Story | kancelářský software | `el3` | plánovaný úkol | komplexní dokument nad jedním tématem, kontrola PDF/PPTX výstupu |

## Kontrola pokrytí ŠVP

| Oblast ŠVP | Pokrytí v backlogu |
| --- | --- |
| jednoduché multimediální prezentace | lekce 1-6, úkol 1, úkol 2 |
| snímky, uspořádání, časování a efekty | lekce 5-6, úkol 1 |
| grafická schémata prezentací | lekce 3, úkol 2 |
| hypertextové odkazy | lekce 8.2, částečně lekce 9.2 |
| kancelářský software jako celek | lekce 9.1, úkol 5 |
| komplexní dokumenty s objekty různých aplikací | lekce 9.2, úkol 5 |
| import a export dat | lekce 9.2, úkol 5 |
| algoritmizace | lekce 7.1-7.2, úkol 3 |
| dekompozice a abstrakce | lekce 7.1, úkol 3 |
| multimediální dokumenty | lekce 8.1-8.2, úkol 4 |
| text, obraz, zvuk, interaktivní vazby | lekce 8.1-8.2, úkol 4 |
| člověk a životní prostředí | vhodné jako téma praktických úkolů 3-5 |

## Doporučený další krok

1. Ověřit skutečné názvy komponent v Jira.
2. Potvrdit, zda se budou zakládat pouze stories, nebo i epicy.
3. Po potvrzení vytvořit tickety v backlogu s labelem `el3`.
