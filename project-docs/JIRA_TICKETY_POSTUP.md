# Postup pro tvorbu Jira ticketů k výukovým celkům

Interní pracovní postup pro zakládání Jira ticketů k výukovým materiálům a knihám. Konkrétní pokyny pro daný předmět zadá vyučující vždy samostatně.

## Cíl

Cílem je převést osnovu předmětu, kapitoly knihy a požadavky ŠVP do přehledného backlogu v Jira.

Backlog má sloužit hlavně k plánování práce na výukových materiálech, ne jako detailní pedagogická dokumentace.

## Doporučená struktura

Výchozí jednoduchá struktura:

- jeden Jira ticket typu `Story` pro každou lekci, kapitolu nebo praktický úkol,
- komponenta určuje tematický celek,
- label určuje konkrétní předmět nebo ročník,
- priorita obvykle `Medium`,
- assignee obvykle vlastník předmětu / prostoru,
- tickety založit do backlogu.

Epicy používat pouze tehdy, pokud skutečně přidávají hodnotu:

- větší dlouhodobý balík práce,
- více fází přípravy,
- samostatné sledování postupu celého výukového bloku.

Pokud by epic pouze kopíroval komponentu, je lepší ho nevytvářet.

## Vstupy před založením ticketů

Před tvorbou ticketů ověřit:

- název předmětu / knihy,
- cílovou skupinu,
- zdrojové ŠVP a relevantní stránky,
- aktuální strukturu kapitol v `docs/`,
- případné interní mapy typu `SVP_MAPA_UCIVA_A_KOMPETENCI.md`,
- Jira projektový klíč,
- dostupné komponenty v Jira,
- požadovaný label,
- požadovaného assignee,
- zda mají vznikat pouze stories, nebo i epicy.

## Kontrola proti ŠVP

Před založením ticketů projít relevantní část ŠVP a vypsat:

- hlavní výstupy žáka,
- učivo,
- praktické dovednosti,
- průřezová témata, pokud mají být v backlogu viditelná.

Poté porovnat ŠVP s osnovou knihy:

- každý zásadní výstup musí mít oporu alespoň v jedné story,
- praktické nástroje musí být zachycené samostatně nebo v popisu příslušné story,
- drobné dílčí dovednosti není nutné nafukovat do samostatných ticketů, pokud jsou přirozenou součástí lekce.

## Šablona Story

Doporučený název:

```text
[PŘEDMĚT] Lekce X - Název lekce
```

Nebo pro praktické úkoly:

```text
[PŘEDMĚT] Úkol X - Název úkolu
```

Doporučený popis:

```markdown
Připravit a odučit lekci / praktický úkol k tématu ...

Výstup:

- žák ...
- žák ...
- žák ...

Zdroj v knize: docs/...
```

Popis story má být stručný. Detailní výklad, metodika a pracovní listy patří do repozitáře, ne do Jira ticketu.

## Komponenty

Komponenta má vyjadřovat tematickou oblast, například:

- tabulkový procesor,
- textový procesor,
- databáze,
- prezentace,
- programování,
- projekty,
- počítačové systémy.

Pokud přesná komponenta neexistuje:

1. použít nejbližší existující komponentu,
2. nebo ponechat bez komponenty,
3. novou komponentu nevytvářet bez pokynu uživatele.

## Labely

Label má jednoznačně identifikovat předmět nebo sadu materiálů.

Příklady:

- `el2`,
- `el3`,
- `aps1i`,
- `septima`,
- `db`,
- `projektove-rizeni`.

Label používat konzistentně u všech relevantních stories. Díky tomu lze později ověřit backlog jednoduchým JQL dotazem.

## Doporučený pracovní postup

1. Načíst osnovu knihy z `mkdocs.yml` nebo z adresáře `docs/`.
2. Načíst mapu ŠVP, pokud existuje v `project-docs/`.
3. Ověřit v Jira dostupný projekt, issue typy a komponenty.
4. Rozhodnout, zda se použijí pouze stories, nebo i epicy.
5. Připravit seznam plánovaných ticketů v chatu ke kontrole.
6. Po schválení uživatelem založit tickety v Jira.
7. Ověřit výsledek přes JQL.
8. Vypsat uživateli seznam vytvořených ticketů a případné poznámky.

## Ověření po založení

Po založení ticketů zkontrolovat:

```jql
project = PROJEKT AND labels = label ORDER BY key ASC
```

Ověřit:

- vznikl správný počet ticketů,
- issue type odpovídá dohodě,
- label je nastavený všude,
- komponenty dávají smysl,
- assignee je správně,
- priorita je správně,
- status je backlog / výchozí stav,
- nevznikly duplicitní nebo zbytečné epicy.

## Kontrola pokrytí ŠVP

Po založení ticketů provést krátkou kontrolu:

- které výstupy ŠVP jsou pokryté,
- zda něco nechybí,
- zda některé oblasti nejsou zbytečně roztříštěné,
- zda backlog není složitější než samotná výuka.

Pokud je některý výstup ŠVP jen drobnou součástí lekce, není nutné zakládat nový ticket. Stačí ho pohlídat v popisu existující story nebo v materiálech.

## Bezpečnostní pravidla

- Nepřidávat tickety bez výslovného potvrzení uživatele.
- Nepřidávat nové komponenty bez pokynu uživatele.
- Nemazat Jira issues automaticky.
- Pokud je potřeba změnit strukturu, nejprve shrnout návrh a počkat na potvrzení.
- Při nejistotě ověřit metadata projektu v Jira.

## Poznámka k mazání ticketů

Možnost smazat ticket závisí na samostatném Jira oprávnění `Delete Issues`. Oprávnění editovat issue nestačí. Pokud smazání není dostupné, lze ticket odpojit z používaného pohledu odebráním labelu nebo ho přesunout do hotového stavu.
