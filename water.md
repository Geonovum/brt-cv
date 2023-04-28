# Water

Dit hoofdstuk beschrijft de wijzigingen voor het object Water in BRT.Next
ten opzichte van de huidige versie TOP10NL.

## Overzicht

*Overzicht attributen en waarden/type van object Water in BRT.Next*

| Attribuutnaam          | Waarde of \<type\>     | Geometrietype | Kardinaliteit |
|------------------------|------------------------|---------------|---------------|
| geometrie              | «vlak»                 |               | 1-1           |
|                        | «lijn»                 |               |               |
|                        | «punt»                 |               |               |
| typeWater              | waterloop              | lijn, vlak    | 1-1           |
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
| ligging                | in duiker              | lijn          | 0..n          |
|                        | in sluis               | lijn, vlak    |               |
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

## Wijzigen attributen

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Water~~         | typeWater**deel**        |
| ~~fysiekVoorkomen~~   | **ligging**              |

### Definitie

*Geen.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                   | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------------|----------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~      | ~~Het~~ hoogte ~~niveau~~ van het object.               | **relatieveHoogteligging** | **Aanduiding voor de relatieve hoogte van het object.** |

<details class="note">Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van
een geheel getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details> 

## Wijzigen attribuutwaarden

### Naam

*Attribuut TOP10NL:typeWater \| BRT.Next:type*

| TOP10NL:waarde    | BRT.Next:waarde |
|-------------------|-----------------|
| bron~~, wel~~ | bron            |

### Definitie

Onderstaande attribuutwaarden wijzigen van definitie in BRT.Next. De naam
(waarde) wordt niet aangepast.

*Attribuut TOP10NL:typeWater \| BRT.Next:type*

| *TOP10NL\|BRT.Next:waarde* | *TOP10NL:definitie*                                                                 | *BRT.Next:definitie*                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| waterloop                  | ~~Langgerekt waterdeel in de vorm van een sloot,~~ rivier, kanaal, ~~enz.~~       | **Een voor de waterbeheersing bestemde geul die meestal permanent water bevat (zoals** rivier, kanaal, **beek, sloot, gracht).** |
| greppel, droge sloot       | ~~Een in het algemeen niet watervoerende sloot.~~                                 | **Een ten behoeve van de waterbeheersing gegraven geul die al dan niet met water bedekt is.**                                    |
| zee                        | Uitgestrekt oppervlak zout water ~~dat het grootste deel van de aarde bedekt.~~   | Uitgestrekt oppervlak zout water.                                                                                                |


### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeWater / BRT.Next:type*

| *TOP10NL:waarde*  | *TOP10NL:definitie*                                    | *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                      |
|-------------------|--------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------------------------------|
| ~~meer,plas~~   | Water ~~(meestal) niet gelegen in een waterloop.~~   | **watervlakte**   | **Alle oppervlakken die vrij permanent met zoet** water **zijn bedekt. (zoals meer, plas, ven, vijver).** |

## Vervallen attributen

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                                                       |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~voorkomen~~         | ~~met riet~~                                                                                                                                                                                 |
| ~~functie~~           | ~~drinkwaterbekken~~; ~~haven~~; ~~natuurbad~~; ~~viskwekerij~~; ~~vistrap~~; ~~vloeiveld~~; ~~waterval~~; ~~waterzuivering~~; ~~zwembad~~; ~~overig~~                                       |
| ~~getijdeInvloed~~    | ~~ja; nee~~                                                                                                                                                                                  |
| ~~vaarwegklasse~~     | ~~I~~; ~~II~~; ~~III~~; ~~IV~~; ~~Va~~; ~~Vb~~; ~~VIa~~; ~~VIb~~; ~~VIc~~; ~~VII~~                                                                                                           |
| ~~naamOfficieel~~     | ~~«tekst»~~                                                                                                                                                                                  |
| ~~naamNL~~            | ~~«tekst»~~                                                                                                                                                                                  |
| ~~naamFries~~         | ~~«tekst»~~                                                                                                                                                                                  |
| ~~isBAGnaam~~         | ~~ja~~; ~~nee~~                                                                                                                                                                              |
| ~~hoofdafwatering~~   | ~~ja~~; ~~nee~~                                                                                                                                                                              |

<details class="note">voorkomen ‘met riet’ wordt opgenomen als type ‘water met riet’ in
BRT.Next. </details>

<details class="note">naamOfficieel vervalt, een nieuw attribuut ‘naam: officieel’ met
waarden ja/nee wordt toegevoegd. </details>

## Vervallen attribuutwaarden

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                      |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------|
| typeWater                         | ~~overig~~                                                                                                  |
| fysiekVoorkomen \| ligging        | ~~in afsluitbare duiker~~; ~~in grondduiker~~; ~~in afsluitbare grondduiker~~; ~~overkluisd~~               |

## Toevoegen attributen

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                           | *Verplicht/optioneel*    | *Attribuutwaarde*                           |
|--------------------------|-------------------------------------------------------|--------------------------|---------------------------------------------|
| **naam**                 | **De naam van het waterdeel**                         | **Optioneel, 0 of meer** | **«tekst»**                                 |
| **naam: taal**           | **De taal van de naam van het waterdeel.**            | **Optioneel, 0 of meer** | **Nederlands; Fries; onbekend/ VoidReason** |
| **naam: officieel**      | **Aanduiding of de naam een officiële naam betreft.** | **Optioneel, 0 of meer** | **ja / nee**                                |
| **naam: herkomst**       | **De herkomst van de naam van het waterdeel.**        | **Optioneel, 0 of meer** | **«tekst»**                                 |

<details class="note">regel: ‘naam: herkomst’, ‘naam: officieel’ en ‘naam:taal’ zijn
verplicht als naam is gevuld. </details>

## Toevoegen attribuutwaarden

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:status*

| *BRT.Next:waarde*  | *BRT.Next:definitie*                                                                           |
|--------------------|------------------------------------------------------------------------------------------------|
| **water met riet** | **Alle oppervlakken die vrij permanent met zoet water zijn bedekt en begroeid zijn met riet.** |

*Attribuut BRT.Next:naam:taal*

| *BRT.Next:waarde*        | *BRT.Next:definitie*  |
|--------------------------|-----------------------|
| **Nederlands**           | **Nederlandse taal.** |
| **Fries**                | **Friese taal.**      |
| **onbekend/ VoidReason** | **Taal is onbekend.** |
