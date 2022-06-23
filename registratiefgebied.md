Registratief gebied
===================

Dit hoofdstuk beschrijft de wijzigingen voor het object Registratief gebied in
BRT.Next ten opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeRegistratieGebied’ wordt hernoemd naar ‘type’

-   type ‘land’ wordt hernoemd naar ‘rijk’, type ‘terriotoriale zee’ wordt
    hernoemd naar ‘maritieme zone’ met aangepaste definitie.

-   type ‘waterschap’ vervalt.

-   attribuut ‘naamOfficieel’ vervalt<br />attribuut ‘naam’ wordt nieuw toegevoegd.

-   attributen ‘naamNL’ en ‘naamFries’ vervallen<br />attribuut ‘naam:taal’ wordt
    toegevoegd met waarden ‘Nederlands’, ‘Fries’, of ‘overig’.

-   attribuut ‘naam:herkomst’ met waarden ‘BAG’, ‘BGT’, ‘BRK’, of ‘overig’ wordt
    toegevoegd.

-   puntgeometrie als attribuutwaarde van attribuut geometrie vervalt.

*Overzicht attributen en waarden/type van object Registratief gebied in
BRT.Next*

| Attribuutnaam  | Waarde of «type» | Geometrietype   | Kardinaliteit |
|----------------|------------------|-----------------|---------------|
| geometrie      | «vlak»           |                 | 1-1           |
|                | «multivlak»      |                 |               |
| type           | rijk             | vlak, multivlak | 1-1           |
|                | provincie        | vlak, multivlak |               |
|                | gemeente         | vlak, multivlak |               |
|                | maritieme zone   | vlak, multivlak |               |
| naam           | «tekst»          |                 | 1-1           |
| naam: taal     | Nederlands       |                 | 1-1           |
|                | Fries            |                 |               |
|                | overig           |                 |               |
| naam: herkomst | BAG              |                 | 1-1           |
|                | BGT              |                 |               |
|                | BRK              |                 |               |
|                | overig           |                 |               |
| nummer         | «tekst»          |                 | 0..1          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam*        | *BRT.Next:attribuutnaam* |
|--------------------------------|--------------------------|
| type~~RegistratiefGebied~~ | type                     |

### Definitie

*n.v.t.*

### Naam+definitie

*n.v.t.*

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

| *TOP10NL:waarde* | *BRT.Next:waarde* |
|------------------|-------------------|
| ~~land~~     | **rijk**          |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeRegistratiefGebied | BRT.Next:type*

| *TOP10NL:waarde*         | *TOP10NL:definitie*                                                                                                               | *BRT.Next:waarde*  | *BRT.Next:definitie*                                                                                              |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------|
| ~~territoriale zee~~ | ~~Een~~ zee~~strook, grenzend aan het landgebied van Nederland waarover de soevereiniteit van Nederland zich uitstrekt.~~ | **maritieme zone** | **Een bestuurlijk gebied op** zee**, vastgesteld oor de Dienst der Hydrografie van het Ministerie van Defensie.** |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|------------------------------------------|
| ~~naamOfficieel~~   | ~~«tekst»~~                          |
| ~~naamNL~~          | ~~«tekst»~~                          |
| ~~naamFries~~       | ~~«tekst»~~                          |

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-----------------------------------|------------------------------------------|
| geometrie                         | ~~«punt»~~                           |
| typeRegistratiefGebied|type      | ~~waterschap~~                       |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                              | *Verplicht/optioneel* | *Attribuutwaarde*             |
|--------------------------|----------------------------------------------------------|-----------------------|-------------------------------|
| **naam**                 | **De naam van het registratief gebied**                  | **Verplicht, 1**      | **«tekst»**                   |
| **naam: taal**           | **De taal van de naam van het registratief gebied.**     | **Verplicht, 1**      | **Nederlands, Fries, overig** |
| **naam: herkomst**       | **De herkomst van de naam van het registratief gebied.** | **Verplicht, 1**      | **BAG, BGT, BRK, overig**     |

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:naam:taal*

| *BRT.Next:waarde* | *BRT.Next:definitie*                       |
|-------------------|--------------------------------------------|
| **Nederlands**    | **Nederlandse taal.**                      |
| **Fries**         | **Friese taal.**                           |
| **overig**        | **Taal, niet zijnde Nederlands of Fries.** |

*Attribuut BRT.Next:naam:herkomst*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                          |
|-------------------|-------------------------------------------------------------------------------|
| **BAG**           | **Naam is afkomstig uit de Basisregistratie Adressen en Gebouwen (BAG).**     |
| **BGT**           | **Naam is afkomstig uit de Basisregistratie Grootschalige Topografie (BGT).** |
| **BRK**           | **Naam is afkomstig uit de Basisregistratie Kadaster (BRK).**                 |
| **overig**        | **Naam is afkomstig uit een bron, niet zijnde BAG, BGT of BRK.**              |
