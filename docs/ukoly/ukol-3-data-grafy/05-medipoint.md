# Úkol 3: Zadání 05 - MediPoint

Vytvořte datovou prezentaci pro vedení firmy **MediPoint**. Navazujte na společné [zadání 00 - TechFlow](00-techflow.md) a na [MediPoint v úkolu 2](../ukol-2-diagramy/05-medipoint.md). Pracujte samostatně nebo ve dvojici podle pokynů vyučujícího.

## Situace

MediPoint je fiktivní zdravotní centrum z úkolu 2. Tentokrát připravujete provozní přehled pro jeho vedení.

Vedení potřebuje porovnat využití služeb a čekání na vyšetření, aby lépe naplánovalo objednávání. Report se týká **prvního pololetí roku 2026**.

Připravte odpovědi na tyto otázky:

1. Jaký hlavní výsledek ukážete samotným číslem?
2. Jak se počet návštěv vyvíjel během pololetí?
3. Jak se liší výsledky jednotlivých kategorií?
4. Ve kterých provozních blocích průměrné čekání překračuje cíl?
5. Který hlášený problém budete řešit jako první a proč?

## Co vytvoříte

Odevzdáte pracovní tabulku se zdrojovými daty, vzorci a grafy a prezentaci se **šesti snímky**. V tabulkovém editoru připravte samotné hlavní číslo, spojnicový graf, sloupcový graf kategorií, zjednodušenou tabulku provozních výsledků a graf hlášených problémů. Prezentaci předvedete během **3-4 minut**.

Použijte Google Sheets a Google Slides, případně Excel a PowerPoint nebo Canvu podle pokynů vyučujícího.

## Zdrojová data

**Všechna data v tomto zadání jsou modelová a byla vytvořena pro výuku.** Nejde o skutečné výsledky existující firmy.

Stáhněte si tři soubory CSV nebo zkopírujte tabulky níže:

- [Měsíční výsledky](../../assets/ukoly/ukol-3-data-grafy/05-medipoint-mesice.csv)
- [Provozní výsledky](../../assets/ukoly/ukol-3-data-grafy/05-medipoint-provoz.csv)
- [Hlášené problémy](../../assets/ukoly/ukol-3-data-grafy/05-medipoint-kvalita.csv)

### Měsíční výsledky

| Měsíc | Nabízené termíny | Uskutečněné návštěvy | Preventivní prohlídky: počet návštěv | Kontrolní návštěvy: počet návštěv | Laboratorní odběry: počet návštěv |
| --- | --- | --- | --- | --- | --- |
| leden | 600 | 520 | 180 | 220 | 120 |
| únor | 620 | 550 | 190 | 230 | 130 |
| březen | 650 | 600 | 210 | 240 | 150 |
| duben | 650 | 610 | 220 | 240 | 150 |
| květen | 680 | 630 | 230 | 240 | 160 |
| červen | 700 | 650 | 240 | 250 | 160 |

Počty návštěv jsou uvedeny v celých číslech. Tři kategorie se nepřekrývají. Podíl uskutečněných návštěv a nabízených termínů vyjadřuje využití kapacity.

### Vybrané provozní bloky

| Provozní blok | Cílové čekání v min | Průměrné čekání v min | Počet návštěv v bloku |
| --- | --- | --- | --- |
| Prevence - pondělí | 15 | 25 | 20 |
| Kontroly - úterý | 15 | 18 | 24 |
| Odběry - středa | 10 | 8 | 30 |
| Prevence - čtvrtek | 15 | 35 | 18 |
| Kontroly - pátek | 15 | 15 | 22 |
| Odběry - pátek | 10 | 12 | 28 |

Každá uskutečněná návštěva patří právě do jedné ze tří kategorií; jejich součet odpovídá sloupci uskutečněných návštěv. Nabízené termíny tvoří kapacitu pro stejné služby. Provozní blok je část pracovního dne pro danou službu. Čekání je průměr za daný blok, nikoli údaj o konkrétní osobě. Data jsou zcela smyšlená.

Jde o **výběr šesti případů z pololetí**, nikoli o úplný seznam. Výběr nesčítejte s měsíčními výsledky a nepovažujte jeho podíly za výsledky celé firmy.

### Hlášené problémy za pololetí

| Problém | Počet hlášení |
| --- | --- |
| Čekání nad sjednaný čas | 24 |
| Nejasné pokyny před návštěvou | 13 |
| Změna termínu ze strany centra | 8 |
| Obtížné telefonické spojení | 6 |
| Chybné potvrzení rezervace | 3 |

Jeden řádek udává počet hlášení daného typu za celé pololetí. Jedna zakázka nebo návštěva může mít více hlášení. Součet proto nevyjadřuje počet nespokojených zákazníků ani podíl chybných zakázek. Nejčetnější problém nemusí být nejzávažnější; jeho dopad a příčinu z těchto dat neznáme.

## Příprava v tabulkovém editoru

1. Založte soubor `MediPoint_data_prijmeni` a listy `mesice`, `provoz`, `kvalita` a `souhrn`.
2. Vložte zdrojová data včetně záhlaví. Při importu CSV použijte oddělovač čárku. Zkontrolujte, že číselné sloupce obsahují čísla.
3. V listu `mesice` dopočítejte součet tří kategorií pro každý měsíc.
4. V listu `souhrn` vypočítejte celkový počet uskutečněných návštěv za pololetí a pololetní součet každé kategorie. Propojte je vzorci se zdrojovými daty.
5. Vypočítejte využití nabízených termínů za celé pololetí: součet skutečnosti vydělte součtem plánu za stejné období. Výsledek zobrazte jako procento; nepoužívejte prostý průměr měsíčních procent.
6. V listu `provoz` dopočítejte rozdíl průměrného a cílového čekání v minutách. Kladná hodnota znamená překročení cíle, nula jeho splnění a záporná hodnota kratší čekání.
7. Vyhledejte nejčetnější hlášený problém a připravte tabulku kategorií pro graf. Při řazení přesouvejte vždy celé řádky.
8. Ke každému připravovanému slidu napište jednu větu závěru a určete hodnotu, která ji dokládá.

## Co má být na snímcích

| Snímek | Otázka a obsah | Povinné zobrazení |
| --- | --- | --- |
| 1 | MediPoint: výsledky za 1. pololetí 2026. Uveďte, komu prezentujete a jaké rozhodnutí má report podpořit. | úvod |
| 2 | Jaký je hlavní výsledek? Vyberte celkový počet uskutečněných návštěv za pololetí nebo vypočtený pololetní podíl. Uveďte jednotku a období. | samotné číslo a krátký popis |
| 3 | Jak se vyvíjel počet návštěv? Zobrazte měsíční součty v pořadí leden až červen. | spojnicový graf |
| 4 | Která kategorie má největší podíl na výsledku? Porovnejte pololetní součty návštěv tří kategorií. | sloupcový graf |
| 5 | Ve kterých provozních blocích průměrné čekání překračuje cíl? Vyberte potřebné sloupce z provozní tabulky a doplňte vypočtený rozdíl. | zjednodušená tabulka |
| 6 | Který hlášený problém má dostat přednost? Porovnejte četnost problémů a navrhněte další krok. | sloupcový nebo pruhový graf a doporučení |

Navrhněte jednu změnu objednávání nebo komunikace s návštěvníky. Doporučení formulujte jako návrh podložený zjištěním. Neuvádějte domnělou příčinu jako prokázaný fakt.

## Úprava grafů a vložení do prezentace

- Pro každý datový slide napište nadpis, který vyjadřuje závěr. Samotný název tématu, například „Výsledky“, nestačí.
- V grafech doplňte jednotky a čitelné popisky. U sloupcových a pruhových grafů nechte hodnotovou osu začínat nulou.
- Použijte neutrální barvy a jednu kontrastní barvu pro vybraný sloupec, bod nebo řádek. Zvýrazněte jednu věc.
- Dlouhé názvy problémů zobrazte raději v pruhovém grafu s vodorovnými pruhy.
- Tabulku upravte pro projekci: ponechte jen údaje potřebné k závěru a vhodně podbarvěte vybraný řádek nebo buňku.
- Grafy vložte z tabulkového editoru do prezentace. U propojených grafů po úpravě dat proveďte aktualizaci a ověřte, že slide ukazuje konečnou verzi.
- Hlavní číslo přepište do samostatného textového pole a porovnejte ho s výpočtem v tabulce.
- Na každý datový slide uveďte zdroj: `Modelová data MediPoint, 1. pololetí 2026`.
- Zkontrolujte čitelnost v režimu promítání. Používejte jednoduché 2D grafy.

Volitelně připravte pro tři kategorie také koláčový graf. Porovnejte jeho čitelnost se sloupcovým grafem a vysvětlete, který lépe podporuje váš závěr.

## Odevzdání a předvedení

Odevzdejte odkaz na pracovní tabulku a prezentaci nebo soubory `MediPoint_data_prijmeni.xlsx` a `MediPoint_data_prijmeni.pptx` podle pokynů vyučujícího. U odkazů ověřte, že je vyučující může otevřít.

Při předvedení vysvětlete hlavní závěr, zdůvodněte výběr zobrazení a doporučte další krok. Mluvte o významu dat, samotná čísla nečtěte po řádcích.

## Kontrola před odevzdáním

- Součty kategorií odpovídají celkovému výsledku.
- Číslo na slidu souhlasí s výpočtem v tabulce.
- Grafy používají správné jednotky, období a měřítko.
- Provozní výběr je označený jako výběr šesti případů.
- Každý datový slide má jasný závěr a zdroj.
- Doporučení vychází z dat a rozlišuje zjištění od domněnky.
