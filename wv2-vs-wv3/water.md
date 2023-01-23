Waterdeel
=========

Dit hoofdstuk beschrijft de wijzigingen voor het object Waterdeel in BRT.Next
ten opzichte van de [vorige versie van het 
wijzigingsvoorstel](https://docs.geostandaarden.nl/brtnext/cv-im-brtnext-20221104/#waterdeel).

Overzicht
---------

Hieronder volgt een overzicht van de attributen en attribuutwaarden van het
object Waterdeel, na doorvoeren van de wijzigingen t.o.v. vorige versie
wijzigingsvoorstel.

*Overzicht attributen en waarden/type van object Waterdeel in BRT.Next*

| Attribuutnaam          | Waarde of «type»     | Geometrietype | Kardinaliteit |
|------------------------|------------------------|---------------|---------------|
| geometrie              | «vlak»                 |               | 1-1           |
|                        | «lijn»                 |               |               |
|                        | «punt»                 |               |               |
| typeWaterdeel          | waterloop              | lijn, vlak    | 1-1           |
|                        | watervlakte            | vlak          |               |
|                        | greppel, droge sloot   | lijn          |               |
|                        | zee                    | vlak          |               |
|                        | droogvallend           | vlak          |               |
|                        | droogvallend (LAT)     | vlak          |               |
|                        | bron                   | punt          |               |
|                        | water met riet         | vlak          |               |
| breedteklasse          | 0,5 - 3 meter          | lijn          | 0..1          |
|                        | 3 - 6 meter            | lijn          |               |
|                        | 6 - 12 meter           | vlak          |               |
|                        | 12 - 50 meter          | vlak          |               |
|                        | 50 - 125 meter         | vlak          |               |
|                        | \> 125 meter           | vlak          |               |
| ligging                | in sluis               | lijn, vlak    | 0..n          |
|                        | op brug                | lijn, vlak    |               |
| relatieveHoogteligging | «geheel getal [-9; 9]» |               | 1-1           |
| naam                   | «tekst»                |               | 0..n          |
| naam: herkomst         | «tekst»                |               | 0..n          |
| naam:officieel         | ja                     |               | 0..n          |
|                        | nee                    |               |               |
| naam: taal             | Nederlands             |               | 0..n          |
|                        | Fries                  |               |               |
|                        | onbekend / VoidReason  |               |               |
| sluisnaam              | «tekst»                |               | 0..1          |
| brugnaam               | «tekst»                |               | 0..1          |

Wijzigingen t.o.v. vorige versie 
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Waterdeel ten opzichte
van vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuut | wordt hernoemd naar |
|-----------|---------------------|
| type      | type**Waterdeel**     |

*Vervallen*

| Attribuut      | vervalt met attribuutwaarden |
|----------------|------------------------------|
| ~~status~~ | ~~bestaand~~                     |

### Attribuutwaarden

Geen
