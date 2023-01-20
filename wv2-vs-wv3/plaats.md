Plaats
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Plaats in BRT.Next ten
opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#plaats).

Overzicht
---------

*Overzicht attributen en waarden/type van object Plaats in BRT.Next*

| Attribuutnaam   | Waarde of «type»           | Geometrietype   | Kardinaliteit |
|-----------------|----------------------------|-----------------|---------------|
| geometrie       | «vlak»                     |                 | 1-1           |
|                 | «multivlak»                |                 |               |
| typePlaats      | woonkern                   | vlak, multivlak | 1-1           |
|                 | industriekern              | vlak, multivlak |               |
|                 | recreatiekern              | vlak, multivlak |               |
|                 | gehucht                    | vlak, multivlak |               |
|                 | buurtschap                 | vlak, multivlak |               |
|                 | historische bebouwingskern | vlak, multivlak |               |
| bebouwdeKom     | ja                         |                 | 1-1           |
|                 | nee                        |                 |               |
| aantalIwoners   | «geheel getal»             |                 | 1-1           |
| naam            | «tekst»                    |                 | 1..n          |
| naam: herkomst  | «taal»                     |                 | 1..n          |
| naam: officieel | ja                         |                 | 1..n          |
|                 | nee                        |                 |               |
| naam: taal      | Nederlands                 |                 | 1..n          |
|                 | Fries                      |                 |               |
|                 | onbekend / VoidReason      |                 |               |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Plaats ten opzichte van
vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuutnaam | wordt hernoemd naar |
|---------------|---------------------|
| type          | type**Plaats**      |

### Attribuutwaarden

Geen
