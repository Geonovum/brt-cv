Plaats
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Plaats in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeGebied’ wordt hernoemd naar ‘type’, ‘naamOfficieel’ naar
    ‘naam’.

-   type ’deelkern’ wordt hernoemd naar ‘woonkern historisch’.

-   typen ‘stadsdeel’, ‘wijk’, ‘buurt’, ‘waterschap’ vervallen.

-   attributen ‘naamNL’ en ‘naamFries’ worden samengevoegd tot attribuut
    ‘naam:taal’ met waarden ‘Nederlands’, ‘Fries’, of ‘overig’.

-   attribuut ‘naam:herkomst’ met waarden ‘BAG’, ‘BGT’, ‘BRK’, of ‘overig’ wordt
    toegevoegd.

-   attributen ‘bebouwdeKom’, ‘isBAGwoonplaats’ en ‘aantalInwoners’ vervallen.

-   puntgeometrie vervalt.

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

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie* | *BRT.Next:attribuutnaam* | *BRT.Next:definitie*   |
|-------------------------|---------------------|--------------------------|------------------------|
| naam~~Officieel~~   |                     | naam                     | De naam van de plaats. |

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

| *TOP10NL:waarde* | *BRT.Next:waarde*           |
|------------------|-----------------------------|
| ~~deel~~kern | **woon**kern **historisch** |

### Definitie

*n.v.t.*

### Naam+definitie

*n.v.t.*

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-------------------------|----------------------------------------|
| ~~bebouwdeKom~~     | ~~ja~~<br /> ~~nee~~                |
| ~~isBAGwoonplaats~~ | ~~ja~~<br /> ~~nee~~                |
| ~~naamNL~~[^1]      | ~~«tekst»~~                        |
| ~~naamFries~~1      | ~~«tekst»~~                        |

[^1]: TOP10NL-attributen naamNL en naamFries met datatype «tekst» worden
vervangen door attribuut naam:taal met attribuutwaarden ‘Nederlands’<br /> ‘Fries’<br />
‘overig’ in BRT.Next.

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*       |
|-----------------------------------|----------------------------------------------|
| geometrie                         | ~~«punt»~~                               |
| typeGebied\|type                  | ~~stadsdeel~~<br />~~wijk~~<br />~~buurt~~ |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                | *Verplicht/optioneel*     | *Domein*                      |
|--------------------------|--------------------------------------------|---------------------------|-------------------------------|
| **naam: taal**           | **De taal van de naam van de plaats.**     | **Optioneel, 0 of meer.** | **Nederlands<br />Fries<br />overig** |
| **naam: herkomst**       | **De herkomst van de naam van de plaats.** | **Optioneel, 0 of meer.** | **BAG<br />BGT<br />BRK<br />overig**     |

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

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
