Spoor
=====

Dit hoofdstuk beschrijft de wijzigingen voor het object Spoor in BRT.Next ten
opzichte van de [vorige versie van het 
wijzigingsvoorstel](https://docs.geostandaarden.nl/brtnext/cv-im-brtnext-20221104/#spoor).

Overzicht
---------

Hieronder volgt een overzicht van de attributen en attribuutwaarden van het
object Spoor, na doorvoeren van de wijzigingen t.o.v. vorige versie
wijzigingsvoorstel.

*Overzicht attributen en waarden/type van object Spoor in BRT.Next*

| Attribuutnaam          | Waarde of «type»            | Geometrietype | Kardinaliteit |
|------------------------|-----------------------------|---------------|---------------|
| geometrie              | «lijn»                      |               | 1-1           |
|                        | «vlak»                      |               |               |
| typeSpoor              | trein                       | lijn          | 1-1           |
|                        | tram                        | lijn          |               |
|                        | sneltram                    | lijn          |               |
|                        | metro                       | lijn          |               |
|                        | gemengd                     | lijn          |               |
|                        | spoorbaan                   | vlak          |               |
| aantalSporen           | enkelvoudig                 |               | 1-1           |
|                        | meervoudig                  |               |               |
| elektrificatie         | ja                          |               | 1-1           |
|                        | nee                         |               |               |
| ligging                | op vast deel van brug       |               | 0..n          |
|                        | op beweegbaar deel van brug |               |               |
|                        | in tunnel                   |               |               |
| relatieveHoogteligging | «geheel getal»              |               | 1-1           |
| status                 | bestaand                    |               | 1-1           |
| brugnaam               | «tekst»                     |               | 0..1          |
| tunnelnaam             | «tekst»                     |               | 0..1          |

attribuut ‘aantalSporen’ en ‘elektrificatie’ is alleen verplicht voor objecten
Spoor met lijngeometrie.

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Spoor ten opzichte van
vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuut | wordt hernoemd naar |
|-----------|---------------------|
| type      | type**Spoor**       |

### Attribuutwaarden

Geen
