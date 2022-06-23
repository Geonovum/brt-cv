Waterdeel
=========

Dit hoofdstuk beschrijft de wijzigingen voor het object Waterdeel in BRT.Next
ten opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeWater’ wordt hernoemd naar ‘type’, ‘fysiekVoorkomen’ naar
    ‘ligging’.

-   attribuut ‘hoogteniveau’ wordt hernoemd naar ‘relatieveHoogteligging’,
    definitie en attribuutwaarden worden aangepast op BGT.

-   type ‘meer, plas’ wordt hernoemd naar ‘watervlakte’, en definitie wordt
    aangepast naar BGT.

-   de definities van typen ‘waterloop’, ‘greppel, droge sloot’, ‘zee’ worden
    aangepast naar de BGT.

-   attribuut ‘status’ met waarde ‘bestaand’ wordt toegevoegd.

-   attribuut ‘naam’ met type «tekst» wordt toegevoegd.

-   attribuut ‘naam:taal’ met waarden ‘Nederlands’, ‘Fries’ of ‘overig’ wordt
    toegevoegd.

-   attribuut ‘naam:herkomst’ met waarden ‘BAG’, ‘BGT’, ‘BRK’ of ‘overig’ wordt
    toegevoegd.

-   attribuut ‘voorkomen’ vervalt<br />type ‘water met riet’ wordt toegevoegd.

-   attributen ‘voorkomen’, ‘functie’, ‘getijdeInvloed’, ‘vaarwegklasse’,
    ‘naamOfficieel’, ‘naamNL’, ‘naamFries’, ‘isBAGnaam’, en ‘hoofdafwatering’
    vervallen.

-   typen ‘bron’ en ‘overig’ en ligging ‘in afsluitbare duiker’, ‘in
    grondduiker’, ‘in afsluitbare grondduiker’ en ‘overkluisd’ vervallen.

-   breedteklassen vanaf 6 meter, dus ‘6-12 meter’ en opvolgende klassen
    vervallen

-   puntgeometrie als attribuutwaarde van attribuut geometrie vervalt.

*Overzicht attributen en waarden/type van object Waterdeel in BRT.Next*

| Attribuutnaam          | Waarde of \<type\>       | Geometrietype | Kardinaliteit |
|------------------------|--------------------------|---------------|---------------|
| geometrie              | «vlak»                   |               | 1-1           |
|                        | «lijn»                   |               |               |
| type                   | waterloop                | lijn, vlak    | 1-1           |
|                        | watervlakte              | vlak          |               |
|                        | greppel, droge sloot     | lijn          |               |
|                        | zee                      | vlak          |               |
|                        | droogvallend             | vlak          |               |
|                        | droogvallend (LAT)       | vlak          |               |
|                        | water met riet           |               |               |
| breedteklasse          | 0,5 - 3 meter            | lijn          | 0..1          |
|                        | 3 - 6 meter              | lijn          |               |
| ligging                | in sluis                 | lijn, vlak    | 0..n          |
|                        | op brug                  | lijn, vlak    |               |
|                        | in duiker                | lijn          |               |
| relatieveHoogteligging | \<geheel getal [-9<br />9]\> |               | 1-1           |
| status                 | bestaand                 |               | 1-1           |
| naam                   | \<tekst\>                |               | 0..n          |
| naam: taal             | Nederlands               |               | 0..n          |
|                        | Fries                    |               |               |
|                        | overig                   |               |               |
| naam: herkomst         | BAG                      |               | 0..n          |
|                        | BGT                      |               |               |
|                        | BRK                      |               |               |
|                        | overig                   |               |               |
| sluisnaam              | \<tekst\>                |               | 0..1          |
| brugnaam               | \<tekst\>                |               | 0..1          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Water~~       | **type**                 |
| ~~fysiekVoorkomen~~ | **ligging**              |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                   | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------------|--------------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het~~ hoogte ~~niveau~~ van het object.~~ | **relatieveHoogteligging** | **Aanduiding voor de relatieve hoogte van het object.** |

<details class="note">
Het bereik van hoogteniveau|relatieveHoogteligging wijzigt van een geheel
getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details>

Wijzigen attribuutwaarden
-------------------------

### Naam

*n.v.t*

### Definitie

Onderstaande attribuutwaarden wijzigen van definitie in BRT.Next. De naam
(waarde) wordt niet aangepast.

*Attribuut TOP10NL:typeWater | BRT.Next:type*

| *TOP10NL\|BRT.Next:waarde* | *TOP10NL:definitie*                                                                 | *BRT.Next:definitie*                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| waterloop                  | ~~Langgerekt waterdeel in de vorm van een sloot,~~ rivier, kanaal, ~~enz.~~ | **Een voor de waterbeheersing bestemde geul die meestal permanent water bevat (zoals** rivier, kanaal, **beek, sloot, gracht).** |
| greppel, droge sloot       | ~~Een in het algemeen niet watervoerende sloot.~~                               | **Een ten behoeve van de waterbeheersing gegraven geul die al dan niet met water bedekt is.**                                    |
| zee                        | Uitgestrekt oppervlak zout water ~~dat het grootste deel van de aarde bedekt.~~ | Uitgestrekt oppervlak zout water.                                                                                                |
|                            |                                                                                     |                                                                                                                                  |
|                            |                                                                                     |                                                                                                                                  |

*Attribuut TOP10NL:typeWater | BRT.Next:type*

| TOP10NL\|BRT.Next:waarde | TOP10NL:definitie                                                                                                                                                                                                           | BRT.Next:definitie                                                                                                                                                         |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| in duiker                | Gelegen in een ~~niet afsluitbare~~ koker die dient voor de instandhouding van de verbinding tussen wederzijds gelegen wateren of voor de afwatering van aangrenzende landerijen ~~, niet zijnde een grondduiker~~. | **Waterdeel** gelegen in een koker die dient voor de instandhouding van de verbinding tussen wederzijds gelegen wateren of voor de afwatering van aangrenzende landerijen. |

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeWater | BRT.Next:type*

| *TOP10NL:waarde*  | *TOP10NL:definitie*                                    | *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                      |
|-------------------|--------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------------------------------|
| ~~meer,plas~~ | Water ~~(meestal) niet gelegen in een waterloop.~~ | **watervlakte**   | **Alle oppervlakken die vrij permanent met zoet** water **zijn bedekt. (zoals meer, plas, ven, vijver).** |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                                                       |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~voorkomen~~       | ~~met riet~~                                                                                                                                                                           |
| ~~functie~~         | ~~drinkwaterbekken~~<br />~~haven~~<br />~~natuurbad~~<br />~~viskwekerij~~<br />~~vistrap~~<br />~~vloeiveld~~<br />~~waterval~~<br />~~waterzuivering~~<br />~~zwembad~~<br />~~overig~~ |
| ~~getijdeInvloed~~  | ~~ja<br />nee~~                                                                                                                                                                                |
| ~~vaarwegklasse~~   | ~~I~~<br />~~II~~<br />~~III~~<br />~~IV~~<br />~~Va~~<br />~~Vb~~<br />~~VIa~~<br />~~VIb~~<br />~~VIc~~<br />~~VII~~                                                                     |
| ~~naamOfficieel~~   | ~~«tekst»~~                                                                                                                                                                                |
| ~~naamNL~~          | ~~«tekst»~~                                                                                                                                                                                |
| ~~naamFries~~       | ~~«tekst»~~                                                                                                                                                                                |
| ~~isBAGnaam~~       | ~~ja~~<br />~~nee~~                                                                                                                                                                        |
| ~~hoofdafwatering~~ | ~~ja~~<br />~~nee~~                                                                                                                                                                        |

<details class="note">
voorkomen ‘met riet’ wordt opgenomen als type ‘water met riet’ in
BRT.Next.
</details>

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                      |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------|
| geometrie                         | ~~«punt»~~                                                                                                |
| typeWater                         | ~~bron~~<br />~~overig~~                                                                                  |
| fysiekVoorkomen | ligging        | ~~in afsluitbare duiker~~<br />~~in grondduiker~~<br />~~in afsluitbare grondduiker~~<br />~~overkluisd~~ |
| ~~breedteklasse~~             | ~~6 - 12 meter~~<br />~~12 - 50 meter~~<br />~~50 - 125 meter~~<br />~~\> 125 meter~~                     |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                                     | *Verplicht/optioneel*     | *Attribuutwaarde*             |
|--------------------------|-----------------------------------------------------------------|---------------------------|-------------------------------|
| **status**               | **De status gekoppeld aan de levenscyclus van een geo-object.** | **Verplicht, 1**          | **bestaand**                  |
| **naam**                 | **De naam van het waterdeel**                                   | **Optioneel, 0 of meer.** | **«tekst»**                   |
| **naam: taal**           | **De taal van de naam van het waterdeel.**                      | **Optioneel, 0 of meer.** | **Nederlands<br />Fries<br />overig** |
| **naam: herkomst**       | **De herkomst van de naam van het waterdeel.**                  | **Optioneel, 0 of meer.** | **BAG<br />BGT<br />BRK<br />overig**     |

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:status*

| *BRT.Next:waarde*  | *BRT.Next:definitie*                                                                           |
|--------------------|------------------------------------------------------------------------------------------------|
| **water met riet** | **Alle oppervlakken die vrij permanent met zoet water zijn bedekt en begroeid zijn met riet.** |

*Attribuut BRT.Next:status*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                          |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| **bestaand**      | **Situatie waarin het object wordt / kan worden gebruikt voor het doel waarvoor het is gebouwd / aangelegd.** |

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
