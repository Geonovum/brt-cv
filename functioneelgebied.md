Functioneel gebied
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Functioneel gebied in
BRT.Next ten opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeGeografischGebied’ wordt hernoemd naar ‘type’;

-   typen 'campus', 'caravanpark', 'kartingbaan', 'gebied met hoge objecten',
    'gebouwencomplex', 'heemtuin', 'infiltratiegebied', 'landgoed',
    'milieustraat', 'mosselbank', 'openluchttheater', 'plantsoen',
    'productie-installatie', 'slipschool', 'tennispark', 'tuincentrum',
    'viskwekerij', 'visvijvercomplex', 'werf', 'windturbinepark', 'zenderpark',
    'zoutwinning' vervallen

-   typen ‘gaswinning’ en ‘oliewinning’ worden samengevoegd tot ‘gaswinning,
    oliewinning’; ‘grindwinning’ en ‘zandwining’ tot ‘grindwinning, zandwinning’

-   typen ‘gevangenis’, ‘psychiatrisch ziekenhuiscomplex’, en ‘tankstation’ van
    object Gebouw verplaatsen naar typen van FunctioneelGebied

-   functie ‘waterzuivering’ van Waterdeel verplaatst naar type van Functioneel
    gebied.

-   attribuut ‘naamNL’ wordt hernoemd naar ‘naam’ met iets aangepaste definitie.

-   attribuut ‘naamFries’ vervalt.

*Overzicht attributen en waarden/type van object Functioneel gebied in BRT.Next*

| Attribuutnaam | Waarde of \<type\>              | Geometrietype   | Kardinaliteit |
|---------------|---------------------------------|-----------------|---------------|
| geometrie     | \<vlak\>                        |                 | 1-1           |
|               | \<multivlak\>                   |                 |               |
|               | \<punt\>                        |                 |               |
| type          | attractiepark                   | vlak, multivlak | 1-1           |
|               | bedrijventerrein                | vlak, multivlak |               |
|               | begraafplaats                   | vlak, multivlak |               |
|               | boswachterij                    | vlak, multivlak |               |
|               | botanische tuin                 | vlak, multivlak |               |
|               | bungalowpark                    | vlak, multivlak |               |
|               | camping, kampeerterrein         | vlak, multivlak |               |
|               | circuit                         | vlak, multivlak |               |
|               | crossbaan                       | vlak, multivlak |               |
|               | dierentuin, safaripark          | vlak, multivlak |               |
|               | eendenkooi                      | vlak, multivlak |               |
|               | emplacement                     | vlak, multivlak |               |
|               | erebegraafplaats                | vlak, multivlak |               |
|               | gaswinning, oliewinning         | vlak, multivlak |               |
|               | gebied voor radioastronomie     | vlak, multivlak |               |
|               | golfterrein                     | vlak, multivlak |               |
|               | grafheuvel                      | vlak, multivlak |               |
|               | grindwinning, zandwinning       | vlak, multivlak |               |
|               | groeve                          | vlak, multivlak |               |
|               | haven                           | vlak, multivlak |               |
|               | helikopterlandingsplaats        | vlak, multivlak |               |
|               | jachthaven                      | vlak, multivlak |               |
|               | kassengebied                    | vlak, multivlak |               |
|               | mijn                            | vlak, multivlak |               |
|               | militair oefengebied            | vlak, multivlak |               |
|               | militair terrein                | vlak, multivlak |               |
|               | nationaal park                  | vlak, multivlak |               |
|               | natuurgebied                    | vlak, multivlak |               |
|               | openluchtmuseum                 | vlak, multivlak |               |
|               | park                            | vlak, multivlak |               |
|               | recreatiegebied                 | vlak, multivlak |               |
|               | renbaan                         | vlak, multivlak |               |
|               | skibaan                         | vlak, multivlak |               |
|               | sluizencomplex                  | vlak, multivlak |               |
|               | sportterrein, sportcomplex      | vlak, multivlak |               |
|               | stortplaats                     | vlak, multivlak |               |
|               | transformatorstation            | vlak, multivlak |               |
|               | vakantiepark                    | vlak, multivlak |               |
|               | verdedigingswerk                | vlak, multivlak |               |
|               | verzorgingsplaats               | vlak, multivlak |               |
|               | vliegveld, luchthaven           | vlak, multivlak |               |
|               | volkstuinen                     | vlak, multivlak |               |
|               | waterkering                     | vlak, multivlak |               |
|               | wildwissel                      | vlak, multivlak |               |
|               | woonwagencentrum                | vlak, multivlak |               |
|               | ijsbaan                         | vlak, multivlak |               |
|               | zonnepark                       | vlak, multivlak |               |
|               | ziekenhuiscomplex               | vlak, multivlak |               |
|               | zuiveringsinstallatie           | vlak, multivlak |               |
|               | zweefvliegveldterrein           | vlak, multivlak |               |
|               | zwembadcomplex                  | vlak, multivlak |               |
|               | overig                          | vlak, multivlak |               |
|               | gevangenis                      | vlak, multivlak |               |
|               | psychiatrisch ziekenhuiscomplex | vlak, multivlak |               |
|               | tankstation                     | vlak, multivlak |               |
|               | waterzuivering                  | vlak, multivlak |               |
| naam          | \<tekst\>                       |                 | 0..n          |
| soortnaam     | \<tekst\>                       |                 | 0..n          |

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

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                     | *BRT.Next:attribuutnaam* | *BRT.Next:definitie*                |
|-------------------------|---------------------------------------------------------|--------------------------|-------------------------------------|
| naam~~NL~~          | De ~~Nederlandse~~ naam van het functionele gebied. | naam                     | De naam van het functionele gebied. |

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

*n.v.t.*

### Definitie

*n.v.t.*

### Naam+definitie

n.v.t.

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-------------------------|----------------------------------------|
| ~~naamFries~~1      | ~~«tekst»~~                        |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeFunctioneelGebied\|type       | ~~gaswinning~~;~~oliewinning~~; ~~grindwinning~~; ~~zandwinning~~[^1]                                                                                                                                                                                                                                                                                                                                                                                           |
| typeFunctioneelGebied\|type       | ~~campus~~;~~caravanpark~~;~~kartingbaan~~;~~gebied met hoge objecten~~;~~gebouwencomplex~~;~~heemtuin~~;~~infiltratiegebied~~;~~landgoed~~;~~milieustraat~~;~~mosselbank~~;~~openluchttheater~~;~~plantsoen~~;~~productie-installatie~~;~~slipschool~~;~~tennispark~~;~~tuincentrum~~;~~viskwekerij~~;~~visvijvercomplex~~;~~werf~~;~~windturbinepark~~;~~zenderpark~~;~~zoutwinning~~ |

[^1]: typen ‘gaswinning’ en ‘oliewinning’ worden samengevoegd tot ‘gaswinning,
oliewinning’; ‘grindwinning’ en ‘zandwinning’ tot ‘grindwinning, zandwinning’.

Toevoegen attributen
--------------------

n.v.t.

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:type*

| *BRT.Next:waarde*                        | *BRT.Next:definitie* |
|------------------------------------------|----------------------|
| **gaswinning. oliewinning**              |                      |
| **grindwinning. zandwinning gevangenis** |                      |
| **psychiatrisch ziekenhuiscomplex**      |                      |
| **tankstation**                          |                      |
| **waterzuivering**                       |                      |
