# Úkol 3: Zadání 00 - TechFlow datový report - učitelský manuál

Tento manuál je napsaný jako scénář do hodiny. Cílem je udržet tempo: studenti postupují společně s vyučujícím, nic zbytečně nehledají a po každém kroku mají jasný kontrolní výsledek.

## Výsledek hodiny

Na konci má každý student nebo dvojice:

- tabulku se čtyřmi listy: `mesice`, `projekty`, `kvalita`, `souhrn`,
- vypočtené hlavní hodnoty,
- vytvořené tři grafy a jednu zjednodušenou tabulku,
- prezentaci se šesti snímky,
- připravené krátké vysvětlení hlavního závěru.

## Příprava před hodinou

Otevřete si zadání v učebnici:

```text
Úkoly -> 3. Data, grafy a důkazy -> 00. TechFlow datový report
```

Zkontrolujte, že jsou dostupné CSV soubory:

```text
docs/assets/ukoly/ukol-3-data-grafy/00-techflow-mesice.csv
docs/assets/ukoly/ukol-3-data-grafy/00-techflow-projekty.csv
docs/assets/ukoly/ukol-3-data-grafy/00-techflow-kvalita.csv
```

Připravte si na projektor:

- Google Sheets nebo Excel,
- Google Slides nebo PowerPoint,
- zadání úkolu v učebnici.

Pokud chcete šetřit čas, nechte studenty data nekopírovat ručně, ale použít CSV odkazy ze zadání.

## Doporučená minutáž

| Čas | Část | Výstup |
| --- | --- | --- |
| 0-5 min | zadání situace | studenti ví, komu a proč prezentují |
| 5-15 min | založení tabulky a listů | data jsou vložená do tří listů |
| 15-30 min | výpočty | list `souhrn` obsahuje hlavní hodnoty |
| 30-50 min | grafy v tabulce | vznikne číslo, spojnicový graf, sloupcový graf, tabulka a graf kvality |
| 50-75 min | prezentace | vznikne 6 snímků |
| 75-85 min | kontrola | studenti opraví čitelnost a zdroje |
| 85-90 min | krátké ukázky | 1-2 skupiny odprezentují výsledek |

Pro dvě vyučovací hodiny rozdělte práci po části `grafy v tabulce`.

## 0-5 min: zadání situace

### Co říct

TechFlow je fiktivní firma, která prodává senzory, instalaci a webový přehled pro sledování spotřeby energie ve výrobních halách. Vedení firmy chce krátký datový report za první pololetí 2026.

Nechceme ukázat všechna data. Chceme z dat vybrat hlavní závěry a udělat z nich čitelnou prezentaci.

### Co ukázat

Na tabuli nebo na projektoru nechte viditelné tyto otázky:

1. Jak silný je celkový výsledek?
2. Jak se výsledek vyvíjel v čase?
3. Která část nabídky přináší největší tržby?
4. Jak dobře se daří realizovat projekty?
5. Který problém s kvalitou se má řešit jako první?

### Kontrola

Studenti mají chápat, že každá otázka potřebuje jiné zobrazení: číslo, trend, porovnání, tabulku nebo graf problému.

## 5-15 min: založení tabulky

### Krok 1: nový soubor

Studenti vytvoří nový soubor:

```text
TechFlow_data_prijmeni
```

### Krok 2: listy

Studenti vytvoří čtyři listy:

```text
mesice
projekty
kvalita
souhrn
```

### Krok 3: vložení dat

Do listů vloží data:

| List | Zdroj |
| --- | --- |
| `mesice` | měsíční výsledky |
| `projekty` | realizované projekty |
| `kvalita` | problémy s kvalitou |

### Kontrola

Na konci této části mají studenti v tabulce:

- v listu `mesice` 6 řádků dat za leden až červen,
- v listu `projekty` 6 projektů,
- v listu `kvalita` 5 problémů.

## 15-30 min: pomocné výpočty

V této části pracujte pomalu a společně. Studenti mají pochopit, že prezentace bude stát na několika odvozených hodnotách, ne na celé pracovní tabulce.

### Krok 1: celkové měsíční tržby

Na listu `mesice` přidejte nový sloupec:

```text
Celkové tržby v tis. Kč
```

Do buňky `I2` vložte vzorec:

```text
=F2+G2+H2
```

Vzorec zkopírujte do řádků `I3:I7`.

Kontrolní hodnoty:

| Měsíc | Celkové tržby v tis. Kč |
| --- | ---: |
| leden | 315 |
| únor | 420 |
| březen | 485 |
| duben | 600 |
| květen | 585 |
| červen | 525 |

### Krok 2: souhrn hlavních čísel

Na listu `souhrn` vytvořte tabulku:

| A | B |
| --- | --- |
| Hodnota | Výsledek |
| Celkové tržby |  |
| Úspěšnost nabídek |  |
| Tržby senzory |  |
| Tržby instalace |  |
| Tržby web |  |
| Projekty předané včas |  |
| Nejčastější problém |  |

Použijte tyto vzorce:

| Buňka | Výpočet |
| --- | --- |
| `B2` | `=SUM(mesice!I2:I7)` |
| `B3` | `=SUM(mesice!C2:C7)/SUM(mesice!B2:B7)` |
| `B4` | `=SUM(mesice!F2:F7)` |
| `B5` | `=SUM(mesice!G2:G7)` |
| `B6` | `=SUM(mesice!H2:H7)` |
| `B7` | `=COUNTIF(projekty!F2:F7;"<=0")` |
| `B8` | `Senzor byl dočasně offline` |

Pokud tabulkový editor používá anglické oddělovače, upravte poslední vzorec:

```text
=COUNTIF(projekty!F2:F7,"<=0")
```

### Kontrola

Očekávané výsledky:

| Hodnota | Výsledek |
| --- | ---: |
| Celkové tržby | 2930 tis. Kč |
| Úspěšnost nabídek | 59 % |
| Tržby senzory | 1590 tis. Kč |
| Tržby instalace | 860 tis. Kč |
| Tržby web | 480 tis. Kč |
| Projekty předané včas | 3 |

Upozorněte studenty, že `2930 tis. Kč` lze na slidu napsat jako `2,93 mil. Kč`.

## 30-50 min: grafy a zobrazení v tabulce

Vytvářejte grafy společně a vždy se ptejte: Jakou otázku tím odpovídáme?

### Výstup A: samotné číslo

Otázka:

```text
Jak silný je celkový výsledek?
```

Výsledek pro slide:

```text
2,93 mil. Kč
```

Věta k číslu:

```text
TechFlow měl za první pololetí tržby 2,93 mil. Kč.
```

Tady není potřeba graf. Samotné číslo je silnější než zbytečný obrázek.

### Výstup B: spojnicový graf vývoje tržeb

Otázka:

```text
Jak se tržby vyvíjely v čase?
```

Data:

- osa X: `mesice!A2:A7`,
- hodnoty: `mesice!I2:I7`.

Typ grafu:

```text
spojnicový graf
```

Doporučený název grafu:

```text
Tržby rostly do dubna, potom mírně klesly
```

Úpravy:

- osa Y: jednotka `tis. Kč`,
- bez 3D efektů,
- bez zbytečné legendy, pokud je jen jedna řada,
- zvýrazněte duben nebo nejvyšší bod.

### Výstup C: sloupcový graf podle typu tržeb

Otázka:

```text
Která část nabídky přináší největší tržby?
```

Na listu `souhrn` připravte malou tabulku:

| Typ tržeb | Tržby v tis. Kč |
| --- | ---: |
| senzory | 1590 |
| instalace | 860 |
| web | 480 |

Typ grafu:

```text
sloupcový graf
```

Doporučený název grafu:

```text
Největší část tržeb tvoří senzory
```

Úpravy:

- zvýrazněte sloupec `senzory`,
- ostatní sloupce nechte neutrální,
- osa Y: `tis. Kč`.

### Výstup D: zjednodušená tabulka projektů

Otázka:

```text
Jak dobře se daří realizovat projekty?
```

Na slide nepatří celá pracovní tabulka. Vyberte jen:

| Projekt | Zpoždění ve dnech | Test napoprvé | Úplnost dat |
| --- | ---: | --- | ---: |
| Orion | 0 | ano | 98 % |
| NovaSteel | 3 | ne | 94 % |
| DeltaFood | -1 | ano | 99 % |
| KovoPlus | 7 | ne | 91 % |
| AlfaPlast | 0 | ano | 97 % |
| PrintWorks | 2 | ano | 95 % |

Doporučený závěr:

```text
Největší riziko je projekt KovoPlus: má největší zpoždění a nejnižší úplnost dat.
```

Úpravy:

- zvýrazněte řádek `KovoPlus`,
- nepoužívejte příliš malé písmo,
- odstraňte sloupce, které pro závěr nepotřebujete.

### Výstup E: sloupcový graf problémů s kvalitou

Otázka:

```text
Který problém s kvalitou se má řešit jako první?
```

Data:

- kategorie: `kvalita!A2:A6`,
- hodnoty: `kvalita!B2:B6`.

Typ grafu:

```text
sloupcový graf
```

Doporučený název grafu:

```text
Nejčastější problém je dočasný výpadek senzoru
```

Úpravy:

- seřaďte problémy od nejvyšší hodnoty po nejnižší,
- zvýrazněte první sloupec,
- dlouhé popisky zkraťte nebo zalomte.

### Kontrola

Po této části mají studenti:

- jedno hlavní číslo,
- spojnicový graf,
- sloupcový graf tržeb,
- zjednodušenou tabulku projektů,
- sloupcový graf kvality.

## 50-75 min: tvorba prezentace

Studenti vytvoří prezentaci:

```text
TechFlow_data_prijmeni
```

### Snímek 1: úvod

Nadpis:

```text
TechFlow: datový report za 1. pololetí 2026
```

Podnadpis:

```text
Krátký report pro vedení firmy
```

Poznámka pro učitele:

Tady stačí jednoduchý titulní slide. Nezdržujte se designem.

### Snímek 2: hlavní číslo

Hlavní prvek:

```text
2,93 mil. Kč
```

Doprovodná věta:

```text
Celkové tržby za první pololetí 2026.
```

Zdroj:

```text
Modelová data TechFlow, 1. pololetí 2026
```

Kontrola:

Číslo má být dominantní. Na slidu nemá být žádná tabulka.

### Snímek 3: vývoj tržeb

Vložte spojnicový graf.

Doporučený nadpis:

```text
Tržby rostly do dubna, potom mírně klesly
```

Kontrola:

- je čitelná osa Y,
- je jasné, že hodnoty jsou v tis. Kč,
- graf nemá zbytečnou legendu.

### Snímek 4: typy tržeb

Vložte sloupcový graf.

Doporučený nadpis:

```text
Největší část tržeb tvoří senzory
```

Kontrola:

- senzory jsou zvýrazněné,
- instalace a web jsou v neutrální barvě,
- osy a jednotky jsou srozumitelné.

### Snímek 5: projekty

Vložte zjednodušenou tabulku projektů.

Doporučený nadpis:

```text
KovoPlus je nejrizikovější projekt
```

Kontrola:

- tabulka je zkrácená,
- řádek KovoPlus je zvýrazněný,
- text je čitelný při projekci.

### Snímek 6: kvalita a doporučení

Vložte sloupcový graf problémů s kvalitou.

Doporučený nadpis:

```text
Nejčastější problém je dočasný výpadek senzoru
```

Doporučení:

```text
Další krok: zkontrolovat stabilitu senzorů a způsob upozornění při výpadku.
```

Kontrola:

Slide má obsahovat graf a jedno doporučení. Ne dlouhý odstavec.

## 75-85 min: rychlá kontrola před předvedením

Nechte studenty projít prezentaci podle této tabulky:

| Kontrola | Otázka |
| --- | --- |
| pointa | Je na každém slidu jasný závěr? |
| typ zobrazení | Odpovídá graf otázce? |
| jednotky | Víme, zda jde o tis. Kč, procenta nebo dny? |
| zvýraznění | Je zvýrazněná jedna důležitá věc, ne celý slide? |
| čitelnost | Je graf čitelný z poslední lavice? |
| zdroj | Je uveden zdroj dat? |

Rychlá věta pro studenty:

```text
Když publikum do pěti sekund nepozná, co je hlavní, slide ještě není hotový.
```

## 85-90 min: krátké předvedení

Vyberte 1-2 skupiny nebo nechte studenty prezentovat ve dvojicích navzájem.

Každá prezentace má odpovědět:

1. Jaký je hlavní závěr?
2. Který graf byl nejvhodnější a proč?
3. Co by mělo vedení firmy řešit dál?

Doporučený čas:

```text
3-4 minuty na skupinu
```

## Hotové závěry pro učitele

Tyto závěry můžete použít, pokud studenti váhají:

- Celkové tržby TechFlow za první pololetí jsou 2,93 mil. Kč.
- Tržby rostly do dubna, potom mírně klesly.
- Nejvíce peněz přinášejí senzory.
- Včas byly předány 3 ze 6 projektů.
- Nejrizikovější projekt je KovoPlus.
- Nejčastější problém s kvalitou je dočasný výpadek senzoru.
- Doporučení: zaměřit se na stabilitu senzorů a projektové řízení u rizikových zakázek.

## Časté problémy a rychlá oprava

| Problém | Co říct studentovi |
| --- | --- |
| Na slidu je celá tabulka | Vyber jen řádky nebo sloupce, které podporují závěr. |
| Nadpis je jen `Tržby` | Napiš do nadpisu, co z grafu plyne. |
| Graf nemá jednotky | Doplň `tis. Kč`, `%` nebo `dny`. |
| Všechno je barevné | Neutrálně nech všechno kromě jedné důležité hodnoty. |
| Spojnicový graf je použit pro typy tržeb | Pro porovnání kategorií použij sloupcový graf. |
| Koláčový graf je nepřehledný | Použij sloupcový graf, pokud jde o porovnání. |
| Písmo je malé | Odeber detail nebo rozděl obsah do jednoduššího zobrazení. |

## Hodnocení

Doporučené bodování:

| Oblast | Body |
| --- | ---: |
| správně připravená data a výpočty | 4 |
| vhodný výběr grafů a tabulky | 4 |
| čitelnost a úprava slidů | 4 |
| jasné závěry u jednotlivých slidů | 4 |
| krátké ústní vysvětlení | 4 |

Celkem: 20 bodů.

## Varianta pro rychlejší studenty

Rychlejší studenti mohou doplnit:

- druhou variantu grafu a vysvětlení, proč je horší nebo lepší,
- slide s doporučením pro další čtvrtletí,
- porovnání původního neupraveného grafu a finálního grafu pro prezentaci,
- krátký handout s plnou tabulkou pro vedení firmy.
