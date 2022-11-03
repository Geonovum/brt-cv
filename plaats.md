Plaats
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Plaats in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Overzicht
---------

*Overzicht attributen en waarden/type van object Plaats in BRT.Next*

| Attribuutnaam   | Waarde of «type»           | Geometrietype   | Kardinaliteit |
|-----------------|----------------------------|-----------------|---------------|
| geometrie       | «vlak»                     |                 | 1-1           |
|                 | «multivlak»                |                 |               |
| type            | woonkern                   | vlak, multivlak | 1-1           |
|                 | industriekern              | vlak, multivlak |               |
|                 | recreatiekern              | vlak, multivlak |               |
|                 | gehucht                    | vlak, multivlak |               |
|                 | buurtschap                 | vlak, multivlak |               |
|                 | historische bebouwingskern | vlak, multivlak |               |
| bebouwdeKom     | ja                         |                 | 1-1           |
|                 | nee                        |                 |               |
| aantalIwoners   | «geheel getal»             |                 | 1-1           |
| naam            | «tekst»                    |                 | 1..\*         |
| naam: herkomst  | «taal»                     |                 | 1..\*         |
| naam: officieel | ja                         |                 | 1..\*         |
|                 | nee                        |                 |               |
| naam: taal      | Nederlands                 |                 | 1..\*         |
|                 | Fries                      |                 |               |
|                 | onbekend / VoidReason      |                 |               |

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

| *TOP10NL:waarde* | *BRT.Next:waarde*              |
|------------------|--------------------------------|
| ~~deel~~kern | **historische bebouwings**kern |

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
| ~~isBAGwoonplaats~~ | ~~ja~~; ~~nee~~                  |
| ~~naamNL~~      | ~~«tekst»~~                          |
| ~~naamFries~~1      | ~~«tekst»~~                          |

<details class="note"> TOP10NL-attributen naamNL en naamFries met datatype «tekst» worden
vervangen door attribuut naam:taal met attribuutwaarden ‘Nederlands’; ‘Fries’;
‘onbekend / VoidReason’ in BRT.Next.
</details>

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*     |
|-----------------------------------|----------------------------------------------|
| geometrie                         | ~~«punt»~~                               |
| typeGebied\|type                  | ~~stadsdeel~~;~~wijk~~;~~buurt~~ |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                           | *Verplicht/optioneel*    | *Attribuutwaarde*                            |
|--------------------------|-------------------------------------------------------|--------------------------|----------------------------------------------|
| **naam**                 | **De naam van de plaats.**                            | **Verplicht, 1 of meer** | **«tekst»**                                  |
| **naam: herkomst**       | **De herkomst van de naam van de plaats.**            | **Verplicht, 1 of meer** | **«tekst»**                                  |
| **naam: officieel**      | **Aanduiding of de naam een officiële naam betreft.** | **Verplicht, 1 of meer** | **ja/nee**                                   |
| **naam: taal**           | **De taal van de naam van de plaats.**                | **Verplicht, 1 of meer** | **Nederlands; Fries; onbekend / VoidReason** |

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:naam:taal*

| *BRT.Next:waarde*         | *BRT.Next:definitie*  |
|---------------------------|-----------------------|
| **Nederlands**            | **Nederlandse taal.** |
| **Fries**                 | **Friese taal.**      |
| **onbekend / VoidReason** | **Taal is onbekend.** |
