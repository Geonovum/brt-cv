Functioneel gebied
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Functioneel gebied in
BRT.Next ten opzichte van de huidige versie TOP10NL.

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
|               | boswachterij                        | vlak, multivlak |               |
|               | botanische tuin                     | vlak, multivlak |               |
|               | bungalowpark                        | vlak, multivlak |               |
|               | camping, kampeerterrein             | vlak, multivlak |               |
|               | circuit                             | vlak, multivlak |               |
|               | crossbaan                           | vlak, multivlak |               |
|               | dierentuin, safaripark              | vlak, multivlak |               |
|               | eendenkooi                          | vlak, multivlak |               |
|               | emplacement                         | vlak, multivlak |               |
|               | erebegraafplaats                    | vlak, multivlak |               |
|               | gaswinning, oliewinning             | vlak, multivlak |               |
|               | gebied voor radioastronomie         | vlak, multivlak |               |
|               | golfterrein                         | vlak, multivlak |               |
|               | grafheuvel                          | vlak, multivlak |               |
|               | grindwinning, zandwinning           | vlak, multivlak |               |
|               | groeve                              | vlak, multivlak |               |
|               | haven                               | vlak, multivlak |               |
|               | helikopterlandingsplaats            | vlak, multivlak |               |
|               | jachthaven                          | vlak, multivlak |               |
|               | kassengebied                        | vlak, multivlak |               |
|               | mijn                                | vlak, multivlak |               |
|               | militair oefengebied, schietterrein | vlak, multivlak |               |
|               | kazerne, legerplaats, vliegbasis    | vlak, multivlak |               |
|               | nationaal park                      | vlak, multivlak |               |
|               | natuurgebied                        | vlak, multivlak |               |
|               | openluchtmuseum                     | vlak, multivlak |               |
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
|               | vliegveld, luchthaven               | vlak, multivlak |               |
|               | volkstuinen                         | vlak, multivlak |               |
|               | waterkering                         | vlak, multivlak |               |
|               | wildwissel                          | vlak, multivlak |               |
|               | woonwagencentrum                    | vlak, multivlak |               |
|               | ijsbaan                             | vlak, multivlak |               |
|               | zonnepark                           | vlak, multivlak |               |
|               | ziekenhuiscomplex                   | vlak, multivlak |               |
|               | zuiveringsinstallatie               | vlak, multivlak |               |
|               | zweefvliegveldterrein               | vlak, multivlak |               |
|               | zwembadcomplex                      | vlak, multivlak |               |
|               | overig                              | vlak, multivlak |               |
|               | gevangeniscomplex                   | vlak, multivlak |               |
|               | psychiatrisch ziekenhuiscomplex     | vlak, multivlak |               |
|               | tankstation                         | vlak, multivlak |               |
|               | vliedberg                           | vlak, multivlak |               |
| naam          | «tekst»                             |                 | 0..n          |
| soortnaam     | «tekst»                             |                 | 0..n          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam*       | *BRT.Next:attribuutnaam* |
|-------------------------------|--------------------------|
| type~~FunctioneelGebied~~ | type                     |

### Definitie

*Geen.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                     | *BRT.Next:attribuutnaam* | *BRT.Next:definitie*                |
|-------------------------|---------------------------------------------------------|--------------------------|-------------------------------------|
| naam~~NL~~          | De ~~Nederlandse~~ naam van het functionele gebied. | naam                     | De naam van het functionele gebied. |

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

*Geen.*

### Definitie

Onderstaande attribuutwaarden wijzigen van definitie in BRT.Next. De naam wordt
niet aangepast.

*Attribuut TOP10NL:typeFunctioneelGebiedandgebruik \| BRT.Next:type*

| *TOP10NL\|BRT.Next:waarde*          | *TOP10NL:definitie*                                                                                                                                                                                                                       | *BRT.Next:definitie*                                                                                      |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| militair oefengebied, schietterrein | ~~Militair kamp voor het houden van schietoefeningen met zware vuurwapens (artillerie schietkamp). / Terrein ingericht voor het schieten op doelen (schietkamp). /~~ Terrein waar militairen oefenen ~~(militair oefenterrein).~~ | **Gebied** waar militairen oefenen, **gebied voor het houden van schietoefeningen** met zware vuurwapens. |

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeFunctioneelGebied \| BRT.Next:type*

| *TOP10NL:waarde*          | *TOP10NL:definitie*                                                                | *BRT.Next:waarde*                    | *BRT.Next:definitie*                                                      |
|---------------------------|------------------------------------------------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|
| helikopterlandingsterrein | ~~Terrein~~ dat als landings- en ~~vertrek~~plaats dient voor helikopters. | **helikopterlandingsplaats**         | Gebied dat **dient** als landings- en **opstijg**plaats voor helikopters. |

| kazerne, legerplaats      | Gebouw~~(-encomplex) bestemd tot huisvesting van soldaten.~~                   | kazerne, legerplaats, **vliegbasis** | **Terrein met militaire** gebouw**en en infrastructuur.**                 |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|------------------------------------------|
| ~~naamFries~~       | ~~«tekst»~~                          |

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeFunctioneelGebied\|type       | ~~gaswinning~~; ~~oliewinning~~; ~~grindwinning~~; ~~zandwinning~~                                                                                                                                                                                                                                                                                                                                                                                           |
| typeFunctioneelGebied\|type       | ~~campus~~; ~~caravanpark~~; ~~kartingbaan~~; ~~gebied met hoge objecten~~; ~~gebouwencomplex~~; ~~heemtuin~~; ~~infiltratiegebied~~; ~~landgoed~~; ~~milieustraat~~; ~~mosselbank~~; ~~openluchttheater~~; ~~plantsoen~~; ~~productie-installatie~~; ~~slipschool~~; ~~tennispark~~; ~~tuincentrum~~; ~~viskwekerij~~; ~~visvijvercomplex~~; ~~werf~~; ~~windturbinepark~~; ~~zenderpark~~; ~~zoutwinning~~ |

<details class="note">
 typen ‘gaswinning’ en ‘oliewinning’ worden samengevoegd tot ‘gaswinning,
oliewinning’; ‘grindwinning’ en ‘zandwinning’ tot ‘grindwinning, zandwinning’.
</details>

Toevoegen attributen
--------------------

Geen.

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:type*

| *BRT.Next:waarde*                   | *BRT.Next:definitie*                                                                                                                                            |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **gaswinning, oliewinning**         | **Gebied met installatie(s) t.b.v. de winning of transport van aardgas en / of aardolie.**                                                                      |
| **grindwinning, zandwinning**       | **Gebied waar winning van grind en/ of zand plaatsvind (in dagbouw of d.m.v. zuigen).**                                                                         |
| **gevangeniscomplex**               | **Een terrein met voorzieningen waar personen in verzekerde bewaring worden gesteld.**                                                                          |
| **psychiatrisch ziekenhuiscomplex** | **Het geheel van gebouwen die tezamen een psychiatrisch ziekenhuiscomplex vormen.**                                                                             |
| **tankstation**                     | **Een terrein met voorzieningen waar motorbrandstof, olie, lucht en koelwater kunnen worden verkregen en / of elektrische voertuigen kunnen worden opgeladen.** |
| **vliedberg**                       | **Kunstmatige heuvel waarop men bij overstromingen kan vluchten.**                                                                                              |
