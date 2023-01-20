Gebouw
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Gebouw in BRT.Next ten
opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#gebouw).

Overzicht
---------

*Overzicht attributen en waarden/type van object Gebouw in BRT.Next*

| Attribuutnaam          | Waarde of «type»                                | Geometrietype | Kardinaliteit |
|------------------------|-------------------------------------------------|---------------|---------------|
| geometrie              | «Vlak»                                          |               | 1-1           |
|                        | «Punt»                                          |               |               |
| typeGebouw             | bunker                                          | vlak, punt    | 1..n          |
|                        | kapel                                           | vlak, punt    |               |
|                        | kas                                             | vlak          |               |
|                        | kasteel                                         | vlak          |               |
|                        | kerk                                            | vlak          |               |
|                        | kernreactor                                     | vlak          |               |
|                        | klokkentoren                                    | vlak, punt    |               |
|                        | klooster, abdij                                 | vlak          |               |
|                        | koeltoren                                       | vlak          |               |
|                        | koepel                                          | vlak          |               |
|                        | moskee                                          | vlak          |               |
|                        | opslagtank                                      | vlak          |               |
|                        | overig religieus gebouw                         | vlak          |               |
|                        | parkeergarage                                   | vlak, punt    |               |
|                        | radiotoren, televisietoren                      | vlak          |               |
|                        | ruïne                                           | vlak          |               |
|                        | schoorsteen                                     | vlak, punt    |               |
|                        | silo                                            | vlak          |               |
|                        | synagoge                                        | vlak          |               |
|                        | stadion                                         | vlak          |               |
|                        | telecommunicatietoren                           | vlak          |               |
|                        | toren                                           | vlak, punt    |               |
|                        | uitzichttoren                                   | vlak, punt    |               |
|                        | verkeerstoren                                   | vlak          |               |
|                        | vuurtoren                                       | vlak          |               |
|                        | waterradmolen                                   | vlak          |               |
|                        | watertoren                                      | vlak          |               |
|                        | waterwoning                                     | vlak          |               |
|                        | windmolen                                       | vlak          |               |
|                        | windturbine                                     | vlak          |               |
|                        | botenhuis                                       | vlak          |               |
|                        | open loods                                      | vlak          |               |
|                        | overkapping                                     | vlak          |               |
|                        | overig                                          | vlak          |               |
| functie                | bezoekerscentrum                                |               | 0..n          |
|                        | brandweerkazerne                                |               |               |
|                        | crematorium                                     |               |               |
|                        | elektriciteitscentrale                          |               |               |
|                        | gemaal                                          |               |               |
|                        | gemeentehuis                                    |               |               |
|                        | gevangenis                                      |               |               |
|                        | kunstijsbaan                                    |               |               |
|                        | observatorium                                   |               |               |
|                        | paleis                                          |               |               |
|                        | parkeren                                        |               |               |
|                        | politiebureau                                   |               |               |
|                        | psychiatrisch ziekenhuis, psychiatrisch centrum |               |               |
|                        | radarstation                                    |               |               |
|                        | reddingsstation                                 |               |               |
|                        | religie                                         |               |               |
|                        | remise                                          |               |               |
|                        | schaapskooi                                     |               |               |
|                        | school                                          |               |               |
|                        | sporthal                                        |               |               |
|                        | stadskantoor, hulpsecretarie                    |               |               |
|                        | universiteit                                    |               |               |
|                        | ziekenhuis                                      |               |               |
|                        | zwembad                                         |               |               |
| ligging                | ondergronds                                     |               | 0..1          |
| hoogte                 | «decimaal getal»                                |               | 0..1          |
| relatieveHoogteligging | «geheel getal [-9; 9]»                          |               | 1-1           |
| status                 | bestaand                                        |               | 1-1           |
| soortnaam              | «tekst»                                         |               | 0..n          |
| naam                   | «tekst»                                         |               | 0..n          |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Gebouw ten opzichte van
vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuut | wordt hernoemd naar |
|-----------|---------------------|
| type      | type**Gebouw**      |


### Attribuutwaarden

*Toevoegen*

| Aan attribuut | wordt attribuutwaarde toegevoegd |
|---------------|----------------------------------|
| functie       | **bezoekerscentrum**             |
| functie       | **reddingsstation**              |
| functie       | **remise**                       |

N.B. definities n.t.b.

*Geometrietypen*

| Voor attribuutwaarde | is geometrietype aangepast naar |
|----------------------|---------------------------------|
| bunker               | vlak**, punt**                  |
| parkeergarage        | vlak**, punt**                  |
