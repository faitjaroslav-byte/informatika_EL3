# Úkol 3: Zadání 00 - TechFlow datový report

V tomto úkolu společně připravíme krátkou datově zaměřenou prezentaci. Budeme simulovat situaci, kdy firma potřebuje ukázat výsledky za první pololetí a rozhodnout, na co se má zaměřit dál.

Nejde o to vytvořit co nejvíce grafů. Cílem je vybrat vhodný způsob zobrazení podle otázky, kterou má slide zodpovědět.

Budeme pracovat ve dvojici nebo společně podle pokynů vyučujícího. Použijeme tabulkový editor a prezentační nástroj, například Google Sheets a Google Slides.

## Situace

Navazujeme na fiktivní firmu **TechFlow s.r.o.** z úkolu 2. Firma vyvíjí senzorové řešení pro sledování spotřeby energie ve výrobních halách. Prodává senzory, instalaci a webový přehled.

Vedení firmy chce na poradě vidět, jak si firma vede za první pololetí roku 2026. Máte připravit krátkou prezentaci, která odpoví na tyto otázky:

1. Jak silný je celkový výsledek?
2. Jak se výsledek vyvíjel v čase?
3. Která část nabídky přináší největší tržby?
4. Jak dobře se daří realizovat projekty?
5. Který problém s kvalitou se má řešit jako první?

## Co vytvoříte

Odevzdáte nebo ukážete:

- pracovní tabulku v tabulkovém editoru,
- několik grafů připravených ze stejných dat,
- krátkou prezentaci se šesti snímky,
- krátké předvedení, ve kterém vysvětlíte hlavní závěr.

## Zdrojová data

Data jsou fiktivní a slouží pouze pro výukový úkol. Můžete je zkopírovat z této stránky nebo stáhnout jako CSV:

- [měsíční výsledky](../../assets/ukoly/ukol-3-data-grafy/00-techflow-mesice.csv)
- [realizované projekty](../../assets/ukoly/ukol-3-data-grafy/00-techflow-projekty.csv)
- [problémy s kvalitou](../../assets/ukoly/ukol-3-data-grafy/00-techflow-kvalita.csv)

### Měsíční výsledky

| Měsíc | Poptávky | Schválené nabídky | Plánované instalace | Dokončené instalace | Tržby senzory v tis. Kč | Tržby instalace v tis. Kč | Tržby web v tis. Kč |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| leden | 8 | 4 | 3 | 2 | 180 | 90 | 45 |
| únor | 10 | 6 | 4 | 4 | 240 | 120 | 60 |
| březen | 12 | 7 | 5 | 4 | 260 | 150 | 75 |
| duben | 14 | 9 | 6 | 6 | 330 | 180 | 90 |
| květen | 13 | 8 | 6 | 5 | 310 | 170 | 105 |
| červen | 11 | 6 | 5 | 5 | 270 | 150 | 105 |

### Realizované projekty

| Projekt | Zákazník | Počet linek | Plánované předání | Skutečné předání | Zpoždění ve dnech | Test napoprvé | Úplnost dat |
| --- | --- | ---: | --- | --- | ---: | --- | ---: |
| Orion | Orion Manufacturing | 5 | 2026-04-15 | 2026-04-15 | 0 | ano | 98 % |
| NovaSteel | NovaSteel | 3 | 2026-04-30 | 2026-05-03 | 3 | ne | 94 % |
| DeltaFood | DeltaFood | 2 | 2026-05-10 | 2026-05-09 | -1 | ano | 99 % |
| KovoPlus | KovoPlus | 4 | 2026-05-20 | 2026-05-27 | 7 | ne | 91 % |
| AlfaPlast | AlfaPlast | 3 | 2026-06-05 | 2026-06-05 | 0 | ano | 97 % |
| PrintWorks | PrintWorks | 2 | 2026-06-18 | 2026-06-20 | 2 | ano | 95 % |

### Problémy s kvalitou

| Problém | Počet případů |
| --- | ---: |
| Senzor byl dočasně offline | 6 |
| Zákazník dodal pozdě podklady | 5 |
| Nejasné pojmenování linek | 4 |
| Nedostatečné zaškolení uživatelů | 3 |
| Nevhodný formát exportu dat | 2 |

## Práce v tabulce

V tabulkovém editoru připravte:

1. list `mesice` se zdrojovou tabulkou měsíčních výsledků,
2. list `projekty` se seznamem projektů,
3. list `kvalita` s problémy s kvalitou,
4. pomocné výpočty, ze kterých půjde vytvořit grafy.

Dopočítejte zejména:

- celkové měsíční tržby,
- úspěšnost nabídek,
- součet tržeb podle typu nabídky,
- počet projektů předaných včas,
- nejčastější problém s kvalitou.

## Grafy a zobrazení

Připravte alespoň tato zobrazení:

| Otázka | Vhodné zobrazení |
| --- | --- |
| Jaký je jeden hlavní výsledek? | samotné číslo |
| Jak se vyvíjely tržby v čase? | spojnicový graf |
| Která část nabídky vydělala nejvíce? | sloupcový graf |
| Které projekty měly zpoždění nebo horší kvalitu dat? | tabulka |
| Který problém s kvalitou je nejčastější? | sloupcový graf, případně koláčový graf |

U každého grafu napište jednu větu závěru. Nestačí nadpis typu "Tržby". Nadpis nebo věta u grafu má říkat, co z dat plyne.

## Struktura prezentace

Prezentace bude mít šest snímků:

| Snímek | Obsah | Povinný prvek |
| --- | --- | --- |
| 1 | TechFlow: datový report za 1. pololetí 2026. Komu prezentujete a proč. | úvod |
| 2 | Jeden hlavní výsledek firmy. | samotné číslo a věta závěru |
| 3 | Vývoj celkových tržeb po měsících. | spojnicový graf |
| 4 | Porovnání tržeb podle typu nabídky. | sloupcový graf |
| 5 | Přehled realizovaných projektů. | zjednodušená tabulka |
| 6 | Nejčastější problém s kvalitou a doporučení dalšího kroku. | graf a závěr |

## Pravidla pro datové slidy

- Každý slide má jednu hlavní pointu.
- Graf musí mít jasné jednotky a popsané osy.
- Pokud používáte barvy, zvýrazněte jen to, co je pro závěr důležité.
- Tabulku zkraťte tak, aby se dala přečíst při projekci.
- Uveďte zdroj: `Modelová data TechFlow, 1. pololetí 2026`.
- Nepoužívejte 3D grafy ani dekorativní efekty.

## Předvedení

Prezentaci předvedete za 3-4 minuty. Při předvedení řekněte:

1. jaký je hlavní závěr,
2. proč jste pro každý slide zvolili právě tento typ zobrazení,
3. co byste vedení TechFlow doporučili řešit dál.

## Název souboru

Odevzdaný soubor pojmenujte:

```text
TechFlow_data_prijmeni.pptx
```
