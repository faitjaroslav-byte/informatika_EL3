# Standard banky otázek a testů

**Platnost:** otázky, testy a koncepty Google Forms pro učebnici Informatika EL3.

Cílem není při každém testu znovu vymýšlet otázky. Nejdříve vzniká malá, ověřená a verzovaná banka. Z ní se potom sestavují různé testy pro konkrétní lekce, termíny a úrovně obtížnosti.

```text
kapitola a její výstupy
        ↓
kandidátní otázky se zdroji
        ↓
nezávislá obsahová kontrola
        ↓
schválená banka
        ↓
výběr varianty testu
        ↓
neveřejný koncept ve Forms a kontrola učitele
```

## 1. Co patří do banky

Do banky patří pouze otázky se stavem `approved`. Každá položka musí obsahovat:

- stabilní ID otázky,
- přiřazení k jedné nebo více lekcím,
- ověřovaný výstup učení,
- kognitivní úroveň: `remember`, `understand`, `apply` nebo `analyze`,
- obtížnost: `easy`, `medium` nebo `hard`,
- bodovou hodnotu,
- znění pro žáka, možnosti a správné řešení,
- stručné vysvětlení správné odpovědi pro učitele,
- odůvodnění distraktorů u uzavřených otázek,
- přesný zdroj v učebnici: cesta, nadpis a rozsah řádků,
- výsledek nezávislé kontroly a stav schválení.

Budoucí technická implementace ukládá banky například do `quiz-generator/question-bank/`. Konfigurace pro Google, OAuth tokeny, návrhy formulářů, exporty odpovědí ani běhy testů do Gitu nepatří.

## 2. Vznik banky

Pro jednu ucelenou lekci připravit nejméně **15 různých kandidátních otázek**. Pro blok několika kratších lekcí je vhodné mít alespoň 25-30 schválených otázek, aby šlo vytvářet smysluplně odlišné varianty.

Postup:

1. Vypsat 3-5 pozorovatelných výstupů lekce.
2. Ke každému výstupu připravit otázky nejméně na dvou úrovních, typicky `understand` a `apply`.
3. U každé otázky uvést přesné zdrojové místo v učebnici; otázka nesmí ověřovat informaci, která nebyla vyučována nebo není v dodaném materiálu.
4. Provést nezávislou kontrolu obsahu, jazyka, správného řešení, distraktorů a vhodnosti pro Forms.
5. Do banky přidat jen položky bez závažné vady. Nejasné nebo duplicitní otázky vrátit k přepracování, nikoli „opravovat za pochodu“ v hotovém testu.

Otázky upravené tak, že se mění význam, správná odpověď nebo rozsah ověřovaného výstupu, se znovu kontrolují a schvalují.

## 3. Kvalita formulace

### Povinná pravidla

- Otázka musí být samostatně srozumitelná. Když navazuje na situaci, musí ji popsat přímo v zadání.
- Ověřovat má dovednost, ne schopnost uhodnout z délky či nápadnosti možnosti.
- Každá uzavřená otázka má právě jednu jednoznačně nejlepší odpověď, pokud zadání výslovně neříká, že je správných více.
- Distraktory musí být věcně uvěřitelné a odpovídat typickému omylu žáka. Nesmí být absurdní, stylisticky nápadné ani pouhou negací správné volby.
- Nepoužívat „všechny uvedené možnosti“, „žádná z možností“ ani záporné otázky. Pokud se záporu nelze vyhnout, zvýraznit jej a pečlivě testovat srozumitelnost.
- Používat češtinu s diakritikou, stručné věty a terminologii shodnou s učebnicí.
- Pokud žák vybírá řešení, musí být v zadání uvedeno kritérium volby: účel, omezení, cílová skupina, zdroj dat, chyba nebo očekávaný výsledek.

### Vhodné typy otázek pro tento předmět

| Typ | K čemu se hodí | Příklad obsahu |
| --- | --- | --- |
| Jedna volba | přesný pojem, příčina, nejlepší další krok | volba výstupu pro publikum, typ diagramu, oprava chyby |
| Více voleb | více nezávisle správných vlastností | prvky kvalitního grafu, kroky kontroly exportu |
| Scénář | použití principu v konkrétní situaci | návrh slidu pro školní akci, výběr formátu pro sdílení |
| Krátká odpověď | vlastní vysvětlení pojmu nebo odůvodnění | proč je slide přeplněný, proč je diagram nejasný |
| Číselná / datová úloha | jednoduché čtení tabulky nebo grafu | kontrola osy grafu, výpočet podílu |
| Otevřená odpověď | návrh, rozbor, obhajoba rozhodnutí | zhodnocení prototypu multimediálního dokumentu |

Přiřazování a řazení se do Google Forms převádí na mřížky. Ty bývají na menším displeji špatně čitelné a první verze generátoru je neumí plně automaticky hodnotit. Proto je nepoužívat jako výchozí typ; raději je rozdělit do několika krátkých scénářových nebo jednobodových otázek.

## 4. Složení testu

Výchozí test má **10-15 otázek** a odpovídá vyučovanému času. U každého testu určit:

- vybrané lekce,
- počet otázek a odhad času,
- profil obtížnosti,
- požadované pokrytí výstupů,
- jedinečný `seed` pro variantu,
- název bez zkratky, které žáci nerozumějí.

### Profily obtížnosti

| Profil | Převládající činnosti | Typické použití |
| --- | --- | --- |
| `foundation` | zapamatování a porozumění | krátké ověření po úvodu do tématu |
| `balanced` | porozumění a použití, menší podíl analýzy | běžný test po lekci nebo bloku |
| `challenge` | použití a analýza, méně přímých definic | pokročilé ověření, opakování nebo dobrovolná výzva |

Test nesmí být jen sadou definic. U běžného profilu `balanced` má alespoň třetina otázek vyžadovat použití, porovnání, opravu nebo zdůvodnění. Každý vybraný výstup se má objevit alespoň jednou, pokud učitel vědomě neurčí jinak.

Výběr možností i pořadí otázek promíchat deterministicky podle `seed`. Stejný seed musí vytvořit stejnou variantu; nový seed vytváří jinou, ale obsahově srovnatelnou variantu. Správná odpověď nesmí systematicky vycházet na stejnou pozici.

## 5. Google Forms a vyhodnocení

- Automaticky hodnotitelné jsou zejména otázky s jednou nebo více volbami a správně nastavenou odpovědí.
- Krátké textové, číselné, přiřazovací, řadicí a otevřené položky považovat za ručně kontrolované, dokud konkrétní implementace neprokáže opak.
- Náročnější otevřená otázka má mít krátké hodnoticí vodítko: očekávané prvky odpovědi a počet bodů.
- Nově vytvořený formulář zůstává konceptem se zavřeným příjmem odpovědí. Učitel před zveřejněním kontroluje náhled na počítači i telefonu, klíč, body, název a nastavení zveřejnění výsledků.
- Koncepty ukládat do předem určené složky na Disku a přidávat časovou značku do názvu. Opětovné spuštění se stejným schváleným obsahem má vrátit existující koncept, nikoli vytvořit duplicitu.

## 6. Povinná kontrola před schválením

Kontrola hodnotí každou otázku alespoň v těchto bodech:

1. věcná správnost a shoda se zdrojem,
2. jednoznačnost zadání i klíče,
3. srozumitelný český jazyk,
4. kvalita distraktorů a odolnost proti hádání,
5. přiměřená kognitivní náročnost,
6. čitelnost a proveditelnost v Google Forms,
7. absence duplicit v bance i ve vybraném testu.

Výsledek kontroly je `pass`, `revise` nebo `reject`. Teprve `pass` dovoluje změnit stav na `approved`.

## 7. Kontrolní otázky před zveřejněním

- Víme, který výstup každá otázka ověřuje?
- Je otázka řešitelná z výuky a uvedeného materiálu?
- Je správná odpověď skutečně nejlepší a vysvětlitelná?
- Obsahuje test přiměřenou směs porozumění, použití a analýzy?
- Jsou možnosti i pořadí promíchané bez rozbití klíče?
- Je každá položka čitelná v náhledu Google Forms?
- Zůstává formulář neveřejný, dokud jej učitel vědomě nezveřejní?
