# Registratief gebied

Dit hoofdstuk beschrijft de wijzigingen voor het object Registratief gebied in
BRT.Next ten opzichte van de huidige versie TOP10NL.

## Overzicht

*Overzicht attributen en waarden/type van object Registratief gebied in
BRT.Next*

| Attribuutnaam          | Waarde of «type»      | Geometrietype   | Kardinaliteit |
|------------------------|-----------------------|-----------------|---------------|
| geometrie              | «vlak»                |                 | 1-1           |
|                        | «multivlak»           |                 |               |
| typeRegistratiefGebied | land                  | vlak, multivlak | 1-1           |
|                        | provincie             | vlak, multivlak |               |
|                        | gemeente              | vlak, multivlak |               |
|                        | maritieme zone        | vlak, multivlak |               |
| naam                   | «tekst»               |                 | 1-1           |
| naam: taal             | Nederlands            |                 | 1..n          |
|                        | Fries                 |                 |               |
|                        | onbekend / VoidReason |                 |               |
| naam: herkomst         | «tekst»               |                 | 1..n          |
| naam: officieel        | ja                    |                 | 1..n          |
|                        | nee                   |                 |               |
| nummer                 | «tekst»               |                 | 0..1          |

## Wijzigen attributen

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Geen

### Definitie

*Geen.*

### Naam+definitie

*Geen.*

## Wijzigen attribuutwaarden

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

*Geen.*

### Definitie

*Geen.*

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL|BRT.Next:typeRegistratiefGebied*

| *TOP10NL:waarde*         | *TOP10NL:definitie*                                                                                                               | *BRT.Next:waarde*  | *BRT.Next:definitie*                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| ~~territoriale zee~~ | ~~Een~~ zee~~strook, grenzend aan het landgebied van Nederland waarover de soevereiniteit van Nederland zich uitstrekt.~~ | **maritieme zone** | **Een bestuurlijk gebied op** zee\*\*, vastgesteld oor de Dienst der Hydrografie van het Ministerie van Defensie.\*\* |

## Vervallen attributen

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|------------------------------------------|
| ~~naamOfficieel~~   | ~~«tekst»~~                          |
| ~~naamNL~~          | ~~«tekst»~~                          |
| ~~naamFries~~       | ~~«tekst»~~                          |

## Vervallen attribuutwaarden

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-----------------------------------|------------------------------------------|
| geometrie                         | ~~«punt»~~                           |
| typeRegistratiefGebied            | ~~waterschap~~                       |

## Toevoegen attributen

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                           | *Verplicht/optioneel*                                    | *Attribuutwaarde*                            |
|--------------------------|-------------------------------------------------------|----------------------------------------------------------|----------------------------------------------|
| **naam**                 | **De naam van het registratief gebied**               | **Verplicht, 1 of meer**                                 | **«tekst»**                                  |
| **naam: herkomst**       | **De taal van de naam van het registratief gebied.**  | **De herkomst van de naam van het registratief gebied.** | **«tekst»**                                  |
| **naam: officieel**      | **Aanduiding of de naam een officiële naam betreft.** | **Verplicht, 1 of meer**                                 | **ja/nee**                                   |
| **naam: taal**           | **De taal van de naam van het registratief gebied.**  | **Verplicht, 1 of meer**                                 | **Nederlands; Fries; onbekend / VoidReason** |

## Toevoegen attribuutwaarden

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:naam:taal*

| *BRT.Next:waarde*         | *BRT.Next:definitie*  |
|---------------------------|-----------------------|
| **Nederlands**            | **Nederlandse taal.** |
| **Fries**                 | **Friese taal.**      |
| **onbekend / VoidReason** | **Taal is onbekend.** |
