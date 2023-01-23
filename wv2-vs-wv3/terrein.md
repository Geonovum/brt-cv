Terrein
=======

Dit hoofdstuk beschrijft de wijzigingen voor het object Terrein in BRT.Next ten
opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#terrein).

Overzicht
---------

*Overzicht attributen en waarden/type van object Terrein in BRT.Next*

| Attribuutnaam          | Waarde of «type»             | Geometrietype | Kardinaliteit |
|------------------------|------------------------------|---------------|---------------|
| geometrie              | «vlak»                       |               | 1-1           |
| typeTerrein            | akkerland                    | vlak          | 1-1           |
|                        | basaltblokken, steenglooiing | vlak          |               |
|                        | boomgaard                    | vlak          |               |
|                        | boomkwekerij                 | vlak          |               |
|                        | duin                         | vlak          |               |
|                        | fruitteelt                   | vlak          |               |
|                        | gemengd bos                  | vlak          |               |
|                        | grasland agrarisch           | vlak          |               |
|                        | grasland overig              | vlak          |               |
|                        | griend en hakhout            | vlak          |               |
|                        | heide                        | vlak          |               |
|                        | houtwal                      | vlak          |               |
|                        | kwelder                      | vlak          |               |
|                        | loofbos                      | vlak          |               |
|                        | naaldbos                     | vlak          |               |
|                        | struiken                     | vlak          |               |
|                        | zand                         | vlak          |               |
|                        | overig                       | vlak          |               |
|                        | erf                          | vlak          |               |
|                        | rietland                     | vlak          |               |
|                        | moeras                       | vlak          |               |
| ligging                | in tunnel                    |               | 0..1          |
|                        | op brug                      |               |               |
| relatieveHoogteligging | «geheel getal [-9; 9]»       |               | 1-1           |
| brugnaam               | «tekst»                      |               | 0..1          |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Terrein ten opzichte van
vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuut | wordt hernoemd naar |
|-----------|---------------------|
| type      | type**Terrein**     |

### Attribuutwaarden

*Vervallen*

| Bij attribuut | vervalt waarde |
|---------------|-------------------------|
| typeTerrein   | ~~braakliggend~~    |
