# Úkol 3: Zadání 02 - RepairHub

Vytvořte datovou prezentaci pro vedení firmy **RepairHub**. Navazujte na společné [zadání 00 - TechFlow](00-techflow.md) a na [RepairHub v úkolu 2](../ukol-2-diagramy/02-repairhub.md). Pracujte samostatně nebo ve dvojici podle pokynů vyučujícího.

## Situace

RepairHub opravuje notebooky a mobilní telefony. Navazujete na servisní zakázku zákaznice Hany z úkolu 2.

Vedení chce porovnat tržby z jednotlivých služeb a rozhodnout, jak zkrátit dobu oprav a omezit opakované zásahy. Report se týká **prvního pololetí roku 2026**.

Připravte odpovědi na tyto otázky:

1. Jaký hlavní výsledek ukážete samotným číslem?
2. Jak se tržby vyvíjely?
3. Jak se liší výsledky jednotlivých kategorií?
4. Které opravy překročily plán a vyžadovaly opakovaný zásah?
5. Který hlášený problém budete řešit jako první a proč?

## Co vytvoříte

Odevzdáte pracovní tabulku se zdrojovými daty, vzorci a grafy a prezentaci se **šesti snímky**. V tabulkovém editoru připravte samotné hlavní číslo, spojnicový graf, sloupcový graf kategorií, zjednodušenou tabulku provozních výsledků a graf hlášených problémů. Prezentaci předvedete během **3-4 minut**.

Použijte Google Sheets a Google Slides, případně Excel a PowerPoint nebo Canvu podle pokynů vyučujícího.

## Zdrojová data

**Všechna data v tomto zadání jsou modelová a byla vytvořena pro výuku.** Nejde o skutečné výsledky existující firmy.

Stáhněte si tři soubory CSV nebo zkopírujte tabulky níže:

- [Měsíční výsledky](../../assets/ukoly/ukol-3-data-grafy/02-repairhub-mesice.csv)
- [Provozní výsledky](../../assets/ukoly/ukol-3-data-grafy/02-repairhub-provoz.csv)
- [Hlášené problémy](../../assets/ukoly/ukol-3-data-grafy/02-repairhub-kvalita.csv)

### Měsíční výsledky

| Měsíc | Plánované opravy | Dokončené opravy | Tržby: notebooky v tis. Kč | Tržby: telefony v tis. Kč | Tržby: diagnostika v tis. Kč |
| --- | --- | --- | --- | --- | --- |
| leden | 70 | 68 | 180 | 140 | 30 |
| únor | 75 | 73 | 200 | 150 | 35 |
| březen | 82 | 80 | 230 | 170 | 40 |
| duben | 90 | 84 | 250 | 180 | 45 |
| květen | 95 | 88 | 245 | 190 | 50 |
| červen | 100 | 92 | 240 | 205 | 55 |

Tržby jsou uvedeny v tisících Kč. Každá částka patří právě do jedné kategorie; součtem tří kategorií získáte celkové měsíční tržby. Data neobsahují náklady, proto z nich nelze určit zisk. Plánované a dokončené položky jsou počty za jednotlivé měsíce, nikoli peněžní částky.

### Vybrané servisní zakázky

| Zakázka | Plánovaná doba opravy ve dnech | Skutečná doba opravy ve dnech | Počet opakovaných zásahů |
| --- | --- | --- | --- |
| Hana - notebook | 3 | 3 | 0 |
| RH-202 - telefon | 2 | 4 | 1 |
| RH-203 - notebook | 4 | 7 | 2 |
| RH-204 - telefon | 2 | 2 | 0 |
| RH-205 - notebook | 5 | 6 | 1 |
| RH-206 - notebook | 3 | 2 | 0 |

Doba opravy se počítá v pracovních dnech od schválení ceny do připravenosti k předání. Opakovaný zásah znamená další opravu stejné závady po prvním testu.

Jde o **výběr šesti případů z pololetí**, nikoli o úplný seznam. Výběr nesčítejte s měsíčními výsledky a nepovažujte jeho podíly za výsledky celé firmy.

### Hlášené problémy za pololetí

| Problém | Počet hlášení |
| --- | --- |
| Čekání na náhradní díl | 16 |
| Závada se znovu projevila | 8 |
| Opožděná informace zákazníkovi | 6 |
| Chybějící vstupní údaje | 4 |
| Nedokončený výstupní test | 2 |

Jeden řádek udává počet hlášení daného typu za celé pololetí. Jedna zakázka nebo návštěva může mít více hlášení. Součet proto nevyjadřuje počet nespokojených zákazníků ani podíl chybných zakázek. Nejčetnější problém nemusí být nejzávažnější; jeho dopad a příčinu z těchto dat neznáme.

## Příprava v tabulkovém editoru

1. Založte soubor `RepairHub_data_prijmeni` a listy `mesice`, `provoz`, `kvalita` a `souhrn`.
2. Vložte zdrojová data včetně záhlaví. Při importu CSV použijte oddělovač čárku. Zkontrolujte, že číselné sloupce obsahují čísla.
3. V listu `mesice` dopočítejte součet tří kategorií pro každý měsíc.
4. V listu `souhrn` vypočítejte celkové tržby za pololetí a pololetní součet každé kategorie. Propojte je vzorci se zdrojovými daty.
5. Vypočítejte podíl dokončených položek vůči plánu za celé pololetí: součet skutečnosti vydělte součtem plánu za stejné období. Výsledek zobrazte jako procento; nepoužívejte prostý průměr měsíčních procent.
6. V listu `provoz` dopočítejte rozdíl skutečné a plánované doby ve dnech. Kladná hodnota znamená překročení plánu, nula jeho splnění a záporná hodnota kratší dobu.
7. Vyhledejte nejčetnější hlášený problém a připravte tabulku kategorií pro graf. Při řazení přesouvejte vždy celé řádky.
8. Ke každému připravovanému slidu napište jednu větu závěru a určete hodnotu, která ji dokládá.

## Co má být na snímcích

| Snímek | Otázka a obsah | Povinné zobrazení |
| --- | --- | --- |
| 1 | RepairHub: výsledky za 1. pololetí 2026. Uveďte, komu prezentujete a jaké rozhodnutí má report podpořit. | úvod |
| 2 | Jaký je hlavní výsledek? Vyberte celkové tržby za pololetí nebo vypočtený pololetní podíl. Uveďte jednotku a období. | samotné číslo a krátký popis |
| 3 | Jak se vyvíjely tržby? Zobrazte měsíční součty v pořadí leden až červen. | spojnicový graf |
| 4 | Která kategorie má největší podíl na výsledku? Porovnejte pololetní součty tržeb tří kategorií. | sloupcový graf |
| 5 | Které opravy překročily plán a vyžadovaly opakovaný zásah? Vyberte potřebné sloupce z provozní tabulky a doplňte vypočtený rozdíl. | zjednodušená tabulka |
| 6 | Který hlášený problém má dostat přednost? Porovnejte četnost problémů a navrhněte další krok. | sloupcový nebo pruhový graf a doporučení |

Navrhněte jedno opatření pro rychlejší nebo spolehlivější opravy. Doporučení formulujte jako návrh podložený zjištěním. Neuvádějte domnělou příčinu jako prokázaný fakt.

## Úprava grafů a vložení do prezentace

- Pro každý datový slide napište nadpis, který vyjadřuje závěr. Samotný název tématu, například „Výsledky“, nestačí.
- V grafech doplňte jednotky a čitelné popisky. U sloupcových a pruhových grafů nechte hodnotovou osu začínat nulou.
- Použijte neutrální barvy a jednu kontrastní barvu pro vybraný sloupec, bod nebo řádek. Zvýrazněte jednu věc.
- Dlouhé názvy problémů zobrazte raději v pruhovém grafu s vodorovnými pruhy.
- Tabulku upravte pro projekci: ponechte jen údaje potřebné k závěru a vhodně podbarvěte vybraný řádek nebo buňku.
- Grafy vložte z tabulkového editoru do prezentace. U propojených grafů po úpravě dat proveďte aktualizaci a ověřte, že slide ukazuje konečnou verzi.
- Hlavní číslo přepište do samostatného textového pole a porovnejte ho s výpočtem v tabulce.
- Na každý datový slide uveďte zdroj: `Modelová data RepairHub, 1. pololetí 2026`.
- Zkontrolujte čitelnost v režimu promítání. Používejte jednoduché 2D grafy.

Volitelně připravte pro tři kategorie také koláčový graf. Porovnejte jeho čitelnost se sloupcovým grafem a vysvětlete, který lépe podporuje váš závěr.

## Odevzdání a předvedení

Odevzdejte odkaz na pracovní tabulku a prezentaci nebo soubory `RepairHub_data_prijmeni.xlsx` a `RepairHub_data_prijmeni.pptx` podle pokynů vyučujícího. U odkazů ověřte, že je vyučující může otevřít.

Při předvedení vysvětlete hlavní závěr, zdůvodněte výběr zobrazení a doporučte další krok. Mluvte o významu dat, samotná čísla nečtěte po řádcích.

## Kontrola před odevzdáním

- Součty kategorií odpovídají celkovému výsledku.
- Číslo na slidu souhlasí s výpočtem v tabulce.
- Grafy používají správné jednotky, období a měřítko.
- Provozní výběr je označený jako výběr šesti případů.
- Každý datový slide má jasný závěr a zdroj.
- Doporučení vychází z dat a rozlišuje zjištění od domněnky.
