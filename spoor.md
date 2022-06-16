Spoor
=====

Dit hoofdstuk beschrijft de wijzigingen voor het object Spoor in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeSpoorbaan’ wordt hernoemd naar ‘type’; ‘fysiekVoorkomen’ naar
    ‘ligging’;

-   attribuut ‘hoogteniveau’ wordt hernoemd naar / vervangen door BGT-attribuut
    ‘relatieveHoogteLigging’; BGT definitie wordt overgenomen alsook
    BGT-type/bereik van -9 tot en met 9.

-   waarde ‘enkel’ van attribuut ‘aantalSporen’ wordt hernoemd naar
    ‘enkelvoudig’,

-   statussen ‘in uitvoering’ en ‘in gebruik’ worden samengevoegd tot ‘bestaand’
    met BGT-definitie; status ‘buiten gebruik’ vervalt

-   attributen ‘typeInfrastructuur’, ‘elektrificatie’, ‘spoorbreedte’,
    ‘vervoerfunctie’, en ‘baanvaknaam’ vervallen

-   ‘dubbel’ vervalt als waarde bij aantalSporen

-   fysiekVoorkomen ‘overkluisd’ vervalt bij attribuut ligging; 

-   type ‘metro’ vervalt

-   puntgeometrie vervalt

*Overzicht attributen en waarden/type van object Spoor in BRT.Next*

| Attribuutnaam          | Waarde of “type\>           | Geometrietype | Kardinaliteit |
|------------------------|-----------------------------|---------------|---------------|
| geometrie              | «lijn»                      |               | 1-1           |
| type                   | trein                       | lijn          | 1-1           |
|                        | tram                        | lijn          |               |
|                        | sneltram                    | lijn          |               |
|                        | gemengd                     | lijn          |               |
| aantalSporen           | enkelvoudig                 |               | 1-1           |
|                        | meervoudig                  |               |               |
| ligging                | op vast deel van brug       |               | 0..n          |
|                        | op beweegbaar deel van brug |               |               |
|                        | in tunnel                   |               |               |
| relatieveHoogteLigging | “geheel getal\>             |               | 1-1           |
| status                 | bestaand                    |               | 1-1           |
| brugnaam               | «tekst»                     |               | 0..1          |
| tunnelnaam             | «tekst»                     |               | 0..1          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

De volgende attributen wijzigen van naam, of wijzigen van naam en definitie in
BRT.Next.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Spoorbaan~~   | type                     |
| ~~fysiekVoorkomen~~ | **ligging**              |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                                                                                                                                  | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------|
| hoogteniveau            | ~~Met het hoogteniveau wordt~~ de relatieve hoogte van het ~~geo-~~object weergegeven. Zo kan worden bepaald op welke wijze geo-objecten elkaar kruisen.~~ | **relatieveHoogteLigging**[^1] | **Aanduiding voor** de relatieve hoogte van het object. |

[^1]: Het domein van hoogteniveau/relatieveHoogteligging wijzigt van geheel
getal kleiner of gelijk aan 0 naar geheel getal tussen -9 en 9.

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

*Attribuut TOP10NL:aantalSporen \| BRT.Next:aantalSporen*

| TOP10NL:waarde | BRT.Next:waarde |
|----------------|-----------------|
| enkel          | enkel**voudig** |

### Definitie

n.v.t.

### Naam+definitie

Onderstaande classificaties wijzigen van naam (waarde) en definitie in BRT.Next

*Attribuut TOP10NL:status \| BRT.Next:status*

| *TOP10NL:waarde*      | *TOP10NL:definitie*                                      | *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                              |
|-----------------------|----------------------------------------------------------|-------------------|-------------------------------------------------------------------------------------------------------------------|
| ~~in uitvoering~~ | ~~De staat~~ waarin het object ~~zich bevindt.~~ | **bestaand**      | **Situatie** waarin het object **wordt / kan worden gebruikt voor het doel waarvoor het is gebouwd / aangelegd.** |
| ~~in gebruik~~    |                                                          | **bestaand**      | *idem*                                                                                                            |
|                       |                                                          |                   |                                                                                                                   |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam*    | *TOP10NL:classificaties of «datatype”*                                                     |
|----------------------------|--------------------------------------------------------------------------------------------|
| ~~typeInfrastructuur~~ | ~~verbinding~~;~~ kruising~~                                                       |
| ~~elektrificatie~~     | ~~ja~~; ~~nee~~                                                                    |
| ~~spoorbreedte~~       | ~~normaalspoor~~; ~~smalspoor~~                                                    |
| ~~vervoerfunctie~~     | ~~gemengd gebruik~~; ~~personenvervoer~~; ~~ goederenvervoer~~; ~~museumlijn |
| ~~baanvaknaam~~        | «tekst”                                                                                    |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype”* |
|-----------------------------------|----------------------------------------|
| geometrie                         | ~~«punt”~~                         |
| typeSpoorbaan \| type             | ~~metro~~                          |
| fysiekVoorkomen \| ligging        | ~~overkluisd~~                     |
| aantalSporen                      | ~~dubbel~~                         |
| status                            | ~~buiten gebruik~~                 |

Toevoegen attributen
--------------------

n.v.t.

Toevoegen classificaties
------------------------

n.v.t
