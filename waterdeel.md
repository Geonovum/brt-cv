Waterdeel
=========

Dit hoofdstuk beschrijft de wijzigingen voor het object Waterdeel in BRT.Next
ten opzichte van de huidige versie TOP10NL.

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
| ~~hoogteniveau~~    | ~~Het~~ hoogte ~~niveau~~ van het object.~~ | **relatieveHoogteLigging**[^1] | **Aanduiding voor de relatieve hoogte van het object.** |

[^1]: Het domein van hoogteniveau/relatieveHoogteligging wijzigt van geheel
getal Kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.

Wijzigen classificaties
-----------------------

### Naam

*n.v.t*

### Definitie

Onderstaande classificaties wijzigen van definitie in BRT.Next. De naam (waarde)
wordt niet aangepast.

| *TOP10NL/BRT.Next:waarde* | *TOP10NL:definitie*                                                                 | *BRT.Next:definitie*                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| waterloop                 | ~~Langgerekt waterdeel in de vorm van een sloot,~~ rivier, kanaal, ~~enz.~~ | **Een voor de waterbeheersing bestemde geul die meestal permanent water bevat (zoals** rivier, kanaal, **beek, sloot, gracht).** |
| greppel, droge sloot      | ~~Een in het algemeen niet watervoerende sloot.~~                               | **Een ten behoeve van de waterbeheersing gegraven geul die al dan niet met water bedekt is.**                                    |
| zee                       | Uitgestrekt oppervlak zout water ~~dat het grootste deel van de aarde bedekt.~~ | Uitgestrekt oppervlak zout water.                                                                                                |

### Naam+definitie

Onderstaande classificaties wijzigen van naam (waarde) en definitie in BRT.Next

*Attribuut TOP10NL:typeWater / BRT.Next:type*

| *TOP10NL:waarde* | *TOP10NL:definitie*                            | *BRT.Next:waarde* | *BRT.Next:definitie*                                                                              |
|------------------|------------------------------------------------|-------------------|---------------------------------------------------------------------------------------------------|
| meer,plas        | Water (meestal) niet gelegen in een waterloop. | watervlakte       | Alle oppervlakken die vrij permanent met zoet water zijn bedekt. (zoals meer, plas, ven, vijver). |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                                                                                                         |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~voorkomen~~       | ~~‘met riet’~~[^2]                                                                                                                                                                         |
| ~~functie~~         | ~~drinkwaterbekken~~; ~~haven~~; ~~natuurbad~~; ~~viskwekerij~~; ~~vistrap~~; ~~vloeiveld~~; ~~waterval~~; ~~waterzuivering~~; ~~zwembad~~; ~~overig~~ |
| ~~getijdeInvloed~~  | ~~ja; nee~~                                                                                                                                                                                |
| ~~vaarwegklasse~~   | ~~I~~; ~~II~~; ~~III~~; ~~IV~~; ~~Va~~; ~~Vb~~; ~~VIa~~; ~~VIb~~; ~~VIc~~; ~~VII~~                                                                     |
| ~~naamOfficieel~~   | ~~«tekst»~~                                                                                                                                                                                |
| ~~naamNL~~          | ~~«tekst»~~                                                                                                                                                                                |
| ~~naamFries~~       | ~~«tekst»~~                                                                                                                                                                                |
| ~~isBAGnaam~~       | ~~ja~~; ~~nee~~                                                                                                                                                                        |

[^2]: voorkomen ‘met riet’ wordt opgenomen als type ‘water met riet’ in
BRT.Next.

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                        |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------|
| geometrie                         | ~~«punt»~~                                                                                                |
| typeWater                         | ~~bron~~; ~~overig~~                                                                                  |
| fysiekVoorkomen \| ligging        | ~~in afsluitbare duiker~~; ~~in grondduiker~~; ~~in afsluitbare grondduiker~~; ~~overkluisd~~ |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                                 | *Verplicht/optioneel* | *Domein*                  |
|--------------------------|-------------------------------------------------------------|-----------------------|---------------------------|
| **status**               | De status gekoppeld aan de levenscyclus van een geo-object. | Verplicht, 1          | bestaand                  |
| **naam**                 | De naam van het waterdeel                                   | Optioneel, 0 of meer. | «tekst»                   |
| **naam: taal**           |                                                             | Optioneel, 0 of meer. | Nederlands; Fries; overig |
| **naam: herkomst**       |                                                             | Optioneel, 0 of meer. | BAG; BGT; BRK; overig     |

*Toelichting/opmerking:*

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:status*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                                                              |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| **bestaand**      | Wegdeel dat uitsluitend is bestemd en gemarkeerd voor openbaar vervoer en afgescheiden is van de andere wegdelen niet uitsluitend door markering. |

*Attribuut BRT.Next:naam:taal*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **Nederlands**    |                      |
| **Fries**         |                      |
| **overig**        |                      |

*Attribuut BRT.Next:naam:herkomst*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **BAG**           |                      |
| **BGT**           |                      |
| **BRK**           |                      |
| **overig**        |                      |
