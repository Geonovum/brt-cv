Spoor
=====

Dit hoofdstuk beschrijft de wijzigingen voor het object Spoor in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeSpoorbaan’ wordt hernoemd naar ‘type’, en ‘fysiekVoorkomen’
    naar ‘ligging’

-   definitie van attributen ‘aantalSporen’ en ‘status’ wijzigen.

-   attribuut ‘hoogteniveau’ wordt hernoemd naar ‘relatieveHoogteligging’,
    definitie en attribuutwaarden worden aangepast op BGT.

-   waarde ‘enkel’ van attribuut ‘aantalSporen’ wordt hernoemd naar
    ‘enkelvoudig’,

-   statussen ‘in uitvoering’ en ‘in gebruik’ worden samengevoegd tot ‘bestaand’
    met BGT-definitie<br />status ‘buiten gebruik’ vervalt.

-   attributen ‘typeInfrastructuur’, ‘elektrificatie’, ‘spoorbreedte’,
    ‘vervoerfunctie’, en ‘baanvaknaam’ vervallen.

-   ‘dubbel’ vervalt als waarde bij aantalSporen.

-   fysiekVoorkomen ‘overkluisd’ vervalt bij attribuut ligging. 

-   type ‘metro’ vervalt.

-   puntgeometrie als attribuutwaarde van attribuut geometrie vervalt.

*Overzicht attributen en waarden/type van object Spoor in BRT.Next*

| Attribuutnaam          | Waarde of «type»            | Geometrietype | Kardinaliteit |
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
| relatieveHoogteligging | «geheel getal [-9;9]»              |               | 1-1           |
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

Onderstaande attributen wijzigen van definitie in BRT.Next. De naam wordt niet
aangepast.

| *TOP10NL \| BRT.Next:attribuutnaam* | *TOP10NL:definitie*                                      | *BRT.Next:definitie*                                                  |
|-------------------------------------|----------------------------------------------------------|-----------------------------------------------------------------------|
| aantalSporen                        | ~~Het aantal sporen van~~ het spoorbaandeel.         | **Aanduiding of** het spoorbaandeel **enkelvoudig of meervoudig is.** |
| status                              | ~~De staat waarin het~~ object ~~zich bevindt.~~ | **De status gekoppeld aan de levenscyclus van een geo-**object**.**   |

### Naam+definitie

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|--------------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het ~~hoogte~~niveau~~van het object. | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note">
 Het bereik van hoogteniveau|relatieveHoogteligging wijzigt van een geheel
getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details>

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

*Attribuut TOP10NL:aantalSporen | BRT.Next:aantalSporen*

| TOP10NL:waarde | BRT.Next:waarde |
|----------------|-----------------|
| enkel          | enkel**voudig** |

### Definitie

n.v.t.

### Naam+definitie

| n.v.t. |   |   |   |
|--------|---|---|---|


Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam*    | *TOP10NL:attribuutwaarden of «datatype»*                                                   |
|----------------------------|--------------------------------------------------------------------------------------------|
| ~~typeInfrastructuur~~ | ~~verbinding~~<br />~~ kruising~~                                                       |
| ~~elektrificatie~~     | ~~ja~~<br />~~nee~~                                                                    |
| ~~spoorbreedte~~       | ~~normaalspoor~~<br />~~smalspoor~~                                                    |
| ~~vervoerfunctie~~     | ~~gemengd gebruik~~<br />~~personenvervoer~~<br />~~ goederenvervoer~~<br />~~museumlijn |
| ~~baanvaknaam~~        | ~~«tekst»~~                                                                            |

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                              |
|-----------------------------------|-----------------------------------------------------------------------|
| geometrie                         | ~~«punt»~~                                                        |
| typeSpoorbaan \| type             | ~~metro~~                                                         |
| fysiekVoorkomen \| ligging        | ~~overkluisd~~                                                    |
| aantalSporen                      | ~~dubbel~~                                                        |
| status                            | ~~in uitvoering~~<br />~~in gebruik~~[^2]<br />~~buiten gebruik~~ |

<details class="note">
status ‘in uitvoering’ en ‘in gebruik’ worden samengevoegd tot status
‘bestaand’.
</details>

Toevoegen attributen
--------------------

n.v.t.

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:status*

| *BRT.Next:status* | *BRT.Next:definitie*                                                                                          |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| **bestaand**      | **Situatie waarin het object wordt / kan worden gebruikt voor het doel waarvoor het is gebouwd / aangelegd.** |
