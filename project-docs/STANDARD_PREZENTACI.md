# Standard prezentací

**Platnost:** učitelské prezentace k lekcím učebnice Informatika EL3.

Tento standard vychází z ověřeného provedení prezentací v APS, ale upravuje ho pro témata prezentací, algoritmů, multimediálních dokumentů a propojování kancelářských aplikací. Prezentace je opora pro výklad a společnou práci ve třídě. Není to zmenšená kapitola učebnice ani materiál určený k samostatnému čtení.

## 1. Výuková funkce

Každý snímek má jednu jasnou funkci:

- otevřít problém nebo otázku,
- vysvětlit jeden princip,
- ukázat konkrétní příklad nebo postup,
- porovnat dvě možnosti,
- zadat krátkou aktivitu,
- ověřit porozumění,
- uzavřít lekci reflexí.

Nezobrazovat na snímku obsah, který má žák pouze číst. Podrobný text, návod nebo metodický komentář patří do učebnice, pracovního listu nebo poznámek řečníka.

## 2. Rozsah a povinná stavba

- Výchozí rozsah je **7-10 snímků** na jednu lekci.
- **11-13 snímků** je možné použít, pouze když každá další stránka přináší samostatný výukový krok, příklad, aktivitu nebo kontrolu porozumění.
- Delší celek rozdělit do navazujících prezentací. **14 a více snímků** vyžaduje předchozí schválení a oddílové předěly.

Typická stavba:

1. čistý titulní snímek s názvem tématu a určením lekce,
2. 3-5 pozorovatelných cílů,
3. výchozí situace, problém nebo klíčová otázka,
4. princip vysvětlený na jednom konkrétním příkladu,
5. postup, diagram nebo ukázka v nástroji,
6. aplikace principu: volba, oprava chyby, porovnání nebo krátký úkol,
7. závěrečná reflexe připravená pro Google Forms.

Ne každá lekce potřebuje všechny mezikroky. Povinné jsou však titul, cíle, alespoň jedna aktivní kontrola porozumění a reflexe.

## 3. Didaktické pořadí pro Informatiku EL3

Výklad musí začínat smyslem, nikoli ovládáním nástroje. Doporučený sled je:

```text
situace nebo problém
        ↓
co má publikum / uživatel pochopit nebo udělat
        ↓
princip či model
        ↓
konkrétní ukázka nebo postup
        ↓
častá chyba, rozhodnutí nebo omezení
        ↓
samostatné použití a reflexe
```

### Oddělení výukových rovin

Nemíchat na jeden snímek různé roviny, pokud tím nevzniká skutečné srovnání:

- **záměr a publikum**: co má sdělení nebo algoritmus vyřešit,
- **logika**: pořadí, podmínka, vztah, struktura, rozhodnutí,
- **provedení v nástroji**: konkrétní kroky v prezentaci, tabulce, diagramu nebo programu,
- **kontrola kvality**: podle čeho poznáme, že výsledek funguje.

Například u diagramu nejprve ukázat vztah, který má obraz vyjádřit, teprve potom volbu tvarů v nástroji. U prezentace nejprve message a publikum, teprve potom rozvržení snímku nebo animaci.

## 4. Vizuální provedení

- Formát je **16:9**. Výchozí typografie je Arial nebo jiný snadno čitelný bezpatkový font dostupný na školních počítačích.
- Titul, cíle, oddílový předěl a reflexe mohou používat plnou teplou oranžovou plochu. Výkladové snímky mají světlé pozadí, velký nadpis, krátký podnadpis a oranžovou orientační linku.
- Akcenty používat střídmě: modrá pro informace nebo vstupy, tyrkysová pro postup či spolupráci, oranžová pro rozhodnutí, zvýraznění a navigaci.
- Jeden snímek má jednu dominantu: fotografii, diagram, příklad, údaj nebo otázku. Nepoužívat dekorativní výplň bez výukové funkce.
- Zachovat volné místo. Text nezmenšovat proto, aby se vešel další odstavec; obsah raději rozdělit.
- Tabulky jsou vhodné jen pro skutečné srovnání. Pro jeden rozdíl je lepší jednoduchý kontrast nebo krátký příklad.

### Diagramy a postupy

- Bloky řadit ve směru čtení a zarovnat na společnou osu.
- Spojnice vést jen mezi prvky, které spolu skutečně souvisejí. Nekřížit je a nepoužívat nahodilé diagonály.
- Šipka znamená konkrétní vztah: pořadí, tok, vliv nebo rozhodnutí. Pokud vztah neumíme pojmenovat, šipka do diagramu nepatří.
- Diagram nejdřív ukázat ve zjednodušené podobě a složitější prvek přidat až v dalším kroku nebo animaci.
- U ukázek rozhraní používat čitelný výřez, označit pouze prvek, o kterém se právě mluví, a nevkládat celý nepřehledný screenshot.

### Fotografie, data a zdroje

- Fotografie a screenshot musí ukazovat přesně ten objekt, rozhraní nebo jev, který snímek vysvětluje.
- Graf nebo číslo zařadit jen s uvedením zdroje, období a významu. Graf nesmí sloužit jen jako dekorace.
- Externí vizuály a podstatná faktická tvrzení uvést do poznámek daného snímku. Poznámky obsahují také jednu krátkou metodickou oporu: co zdůraznit, co nezjednodušovat a na jakou chybu žáků dát pozor.

## 5. Cíle, aktivita a reflexe

- Cíle formulovat pomocí pozorovatelných sloves: například `rozlišit`, `vysvětlit`, `použít`, `navrhnout`, `analyzovat`, `posoudit` nebo `obhájit`.
- Každý cíl musí mít v lekci alespoň jeden doklad: výběr vhodného typu diagramu, úpravu přeplněného slidu, rozbor chybného postupu, vytvoření prototypu nebo zdůvodnění volby.
- Aktivita není jen „pracujte ve dvojici“. Musí říkat, co žák odevzdá, ukáže nebo vysvětlí.
- Reflexe obsahuje 2-4 krátké položky navázané na cíle: škála jistoty, volba dalšího kroku, krátké vysvětlení nebo označení místa, kde žák potřebuje pomoc.

## 6. Soubory a kontrola kvality

- Osnovu prezentace ukládat do `presentations/` jako Markdown: cíle, seznam snímků, zdroje vizuálů a učitelské poznámky.
- Finální soubor ukládat do `presentations/pptx/` pod stabilním názvem bez čísla verze, například `01-prezentace-jako-sdeleni.pptx`.
- Mezikroky, exporty a pracovní soubory patří do ignorovaného build adresáře. Historii finálního PPTX vede Git.

Před předáním vždy:

1. zkontrolovat soulad cílů, snímků, aktivity a reflexe,
2. otevřít nebo vyrenderovat **každý snímek**,
3. ověřit čitelnost z projekce, překryvy, zarovnání, spojnice, fotografie, poznámky a číslování,
4. porovnat výsledný PPTX s osnovou v Markdownu,
5. ponechat v repozitáři pouze aktuální finální verzi prezentace.

## 7. Kontrolní otázky před odevzdáním

- Je titulní snímek čistý, bez obsahu nebo zbytečné osnovy?
- Ví žák po prvních dvou snímcích, co se bude učit a proč?
- Přináší každý snímek novou výukovou funkci?
- Je rozdíl mezi principem, provedením v nástroji a kontrolou kvality zřetelný?
- Dokáže žák po aktivitě něco ukázat, vysvětlit nebo obhájit?
- Je reflexe připravená tak, aby učiteli poskytla informaci pro další hodinu?
