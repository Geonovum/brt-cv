Functioneel gebied
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Functioneel gebied in
BRT.Next ten opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#functioneel-gebied).

Overzicht
---------

*Overzicht attributen en waarden/type van object Functioneel gebied in BRT.Next*

| Attribuutnaam | Waarde of «type»                    | Geometrietype   | Kardinaliteit |
|---------------|-------------------------------------|-----------------|---------------|
| geometrie     | «vlak»                              |                 | 1-1           |
|               | «multivlak»                         |                 |               |
|               | «punt»                              |                 |               |
| type          | attractiepark                       | vlak, multivlak | 1-1           |
|               | bedrijventerrein                    | vlak, multivlak |               |
|               | begraafplaats                       | vlak, multivlak |               |
|               | botanische tuin                     | vlak, multivlak |               |
|               | bungalowpark                        | vlak, multivlak |               |
|               | caravanpark                         | vlak, multivlak |               |
|               | campus                              | vlak, multivlak |               |
|               | camping, kampeerterrein             | vlak, multivlak |               |
|               | circuit                             | vlak, multivlak |               |
|               | crossbaan                           | vlak, multivlak |               |
|               | dierentuin, safaripark              | vlak, multivlak |               |
|               | eendenkooi                          | vlak, multivlak |               |
|               | emplacement                         | vlak, multivlak |               |
|               | erebegraafplaats                    | vlak, multivlak |               |
|               | gasvoorziening, olievoorziening     | vlak, multivlak |               |
|               | gebied voor radioastronomie         | vlak, multivlak |               |
|               | golfterrein                         | vlak, multivlak |               |
|               | grafheuvel                          | vlak, multivlak |               |
|               | grindwinning, zandwinning           | vlak, multivlak |               |
|               | groeve                              | vlak, multivlak |               |
|               | haven                               | vlak, multivlak |               |
|               | heemtuin                            | vlak, multivlak |               |
|               | helikopterlandingsplaats            | vlak, multivlak |               |
|               | jachthaven                          | vlak, multivlak |               |
|               | kassengebied                        | vlak, multivlak |               |
|               | kazerne, legerplaats, vliegbasis    | vlak, multivlak |               |
|               | landgoed                            | vlak, multivlak |               |
|               | mijn                                | vlak, multivlak |               |
|               | militair oefengebied, schietterrein | vlak, multivlak |               |
|               | nationaal park                      | vlak, multivlak |               |
|               | natuurgebied                        | vlak, multivlak |               |
|               | openluchtmuseum                     | vlak, multivlak |               |
|               | openluchttheater                    | vlak, multivlak |               |
|               | park                                | vlak, multivlak |               |
|               | recreatiegebied                     | vlak, multivlak |               |
|               | renbaan                             | vlak, multivlak |               |
|               | skibaan                             | vlak, multivlak |               |
|               | sluizencomplex                      | vlak, multivlak |               |
|               | sportterrein, sportcomplex          | vlak, multivlak |               |
|               | stortplaats                         | vlak, multivlak |               |
|               | transformatorstation                | vlak, multivlak |               |
|               | vakantiepark                        | vlak, multivlak |               |
|               | verdedigingswerk                    | vlak, multivlak |               |
|               | verzorgingsplaats                   | vlak, multivlak |               |
|               | viskwekerij                         | vlak, multivlak |               |
|               | visvijvercomplex                    | vlak, multivlak |               |
|               | vliegveld, luchthaven               | vlak, multivlak |               |
|               | volkstuinen                         | vlak, multivlak |               |
|               | waterkering                         | vlak, multivlak |               |
|               | wildwissel                          | vlak, multivlak |               |
|               | woonwagencentrum                    | vlak, multivlak |               |
|               | ijsbaan                             | vlak, multivlak |               |
|               | zenderpark                          | vlak, multivlak |               |
|               | zonnepark                           | vlak, multivlak |               |
|               | ziekenhuiscomplex                   | vlak, multivlak |               |
|               | zuiveringsinstallatie               | vlak, multivlak |               |
|               | zweefvliegveldterrein               | vlak, multivlak |               |
|               | zwembadcomplex                      | vlak, multivlak |               |
|               | overig                              | vlak, multivlak |               |
|               | gevangeniscomplex                   | vlak, multivlak |               |
|               | psychiatrisch centrum               | vlak, multivlak |               |
|               | tankstation                         | vlak, multivlak |               |
|               | vliedberg                           | vlak, multivlak |               |
|               | asielzoekerscentrum                 | vlak, multivlak |               |
|               | drinkwatervoorziening               | vlak, multivlak |               |
|               | elektriciteitscentrale              | vlak, multivlak |               |
|               | geluidswering                       | vlak, multivlak |               |
| naam          | «tekst»                             |                 | 0..n          |
| soortnaam     | «tekst»                             |                 | 0..n          |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Functioneel gebied ten
opzichte van vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuut | wordt hernoemd naar       |
|-----------|---------------------------|
| type      | type**FunctioneelGebied** |

*Vervallen*

| Attribuut | vervalt met waarden |
|-----------|------------------------------|
| ~~status~~    | ~~bestaand~~                     |

### Attribuutwaarden

*Hernoemen*

| Bij attribuut         | wordt waarde                   | hernoemd naar                           |
|-----------------------|-----------------------------------------|-----------------------------------------|
| typeFunctioneelGebied | gas~~winning~~, olie~~winning~~ | gas**voorziening**, olie**voorziening** |
| typeFunctioneelGebied | psychiatrisch ~~ziekenhuiscomplex~~ | psychiatrisch **centrum**               |

*Vervallen*

| Bij attribuut         | vervalt waarde |
|-----------------------|-------------------------|
| typeFunctioneelGebied | ~~boswachterij~~        |


*Toevoegen*

| Aan attribuut         | wordt waarde toegevoegd |
|-----------------------|----------------------------------|
| typeFunctioneelGebied | **caravanpark**                  |
| typeFunctioneelGebied | **campus**                       |
| typeFunctioneelGebied | **heemtuin**                     |
| typeFunctioneelGebied | **landgoed**                     |
| typeFunctioneelGebied | **openluchttheater**             |
| typeFunctioneelGebied | **viskwekerij**                  |
| typeFunctioneelGebied | **visvijvercomplex**             |
| typeFunctioneelGebied | **zenderpark**                   |
| typeFunctioneelGebied | **asielzoekerscentrum**          |
| typeFunctioneelGebied | **drinkwatervoorziening**        |
| typeFunctioneelGebied | **elektriciteitscentrale**       |
| typeFunctioneelGebied | **geluidswering**                |

*Definitie asielzoekerscentrum, drinkwatervoorziening, electriciteitscentrale, geluidswering n.t.b.*
