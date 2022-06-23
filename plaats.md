Plaats
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Plaats in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeGebied’ wordt hernoemd naar ‘type’.

-   type ’deelkern’ wordt hernoemd naar ‘woonkern historisch’.

-   typen ‘stadsdeel’, ‘wijk’, ‘buurt’, ‘waterschap’ vervallen.

-   attribuut ‘naamOfficieel’ vervalt<br />attribuut ‘naam’ wordt nieuw toegevoegd.

-   attributen ‘naamNL’ en ‘naamFries’ vervallen<br />attribuut ‘naam:taal’ wordt
    toegevoegd met waarden ‘Nederlands’, ‘Fries’, of ‘overig’.

-   attribuut ‘naam:herkomst’ met waarden ‘BAG’, ‘BGT’, ‘BRK’, of ‘overig’ wordt
    toegevoegd.

-   attributen ‘bebouwdeKom’, ‘isBAGwoonplaats’ en ‘aantalInwoners’ vervallen.

-   puntgeometrie als attribuutwaarde van attribuut geometrie vervalt.

*Overzicht attributen en waarden/type van object Plaats in BRT.Next*

| Attribuutnaam  | Waarde of «type»    | Geometrietype   | Kardinaliteit |
|----------------|---------------------|-----------------|---------------|
| geometrie      | «vlak»              |                 | 1-1           |
|                | «multivlak»         |                 |               |
| type           | woonkern            | vlak, multivlak | 1-1           |
|                | industriekern       | vlak, multivlak |               |
|                | recreatiekern       | vlak, multivlak |               |
|                | gehucht             | vlak, multivlak |               |
|                | buurtschap          | vlak, multivlak |               |
|                | woonkern historisch | vlak, multivlak |               |
| naam           | «tekst»             |                 | 1-1           |
| naam: taal     | Nederlands          |                 | 1-1           |
|                | Fries               |                 |               |
|                | overig              |                 |               |
| naam: herkomst | BAG                 |                 | 1-1           |
|                | BGT                 |                 |               |
|                | BRK                 |                 |               |
|                | overig              |                 |               |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Gebied~~      | type                     |

### Definitie

*n.v.t.*

### Naam+definitie

n.v.t.

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

| *TOP10NL:waarde* | *BRT.Next:waarde*           |
|------------------|-----------------------------|
| ~~deel~~kern | **woon**kern **historisch** |

### Definitie

*n.v.t.*

### Naam+definitie

*n.v.t.*

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|------------------------------------------|
| ~~bebouwdeKom~~     | ~~ja~~<br />~~nee~~                  |
| ~~isBAGwoonplaats~~ | ~~ja~~<br />~~nee~~                  |
| ~~naamNL~~      | ~~«tekst»~~                          |
| ~~naamFries~~      | ~~«tekst»~~                          |


Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*     |
|-----------------------------------|----------------------------------------------|
| geometrie                         | ~~«punt»~~                               |
| typeGebied\|type                  | ~~stadsdeel~~<br />~~wijk~~<br />~~buurt~~ |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                | *Verplicht/optioneel* | *Attribuutwaarde*             |
|--------------------------|--------------------------------------------|-----------------------|-------------------------------|
| **naam**                 | **De naam van de plaats.**                 | **Verplicht, 1**      | **«tekst»**                   |
| **naam: taal**           | **De taal van de naam van de plaats.**     | **Verplicht, 1**      | **Nederlands<br />Fries<br />overig** |
| **naam: herkomst**       | **De herkomst van de naam van de plaats.** | **Verplicht, 1**      | **BAG<br />BGT<br />BRK<br />overig**     |

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
