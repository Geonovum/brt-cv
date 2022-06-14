Spoor
=====

Dit hoofdstuk beschrijft de wijzigingen voor het object Spoor in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Wijzigen attributen
-------------------

De volgende attributen wijzigen van naam, of wijzigen van naam en definitie in
BRT.Next.

### Naam

De volgende attributen wijzigen van naam, of wijzigen van naam en definitie in
BRT.Next.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| typeSpoorbaan           | type                     |
| fysiekVoorkomen         | ligging                  |

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                                                                                                                                  | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------|
| hoogteniveau            | ~~Met het hoogteniveau wordt~~ de relatieve hoogte van het ~~geo-~~object weergegeven. Zo kan worden bepaald op welke wijze geo-objecten elkaar kruisen.~~ | **relatieveHoogteLigging** | **Aanduiding voor** de relatieve hoogte van het object. |

*Toelichting:*

-   Het domein van hoogteniveau/relatieveHoogteligging wijzigt van geheel getal
    kleiner of gelijk aan 0 naar geheel getal tussen -9 en 9.

Wijzigen classificaties
-----------------------

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

*Attribuut TOP10NL:aantalSporen \| BRT.Next:aantalSporen*

| TOP10NL:waarde | BRT.Next:waarde |
|----------------|-----------------|
| enkel          | enkel**voudig** |

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

| *TOP10NL:attribuutnaam*    | *TOP10NL:classificaties of «datatype»*                                                     |
|----------------------------|--------------------------------------------------------------------------------------------|
| ~~typeInfrastructuur~~ | ~~verbinding~~;~~ kruising~~                                                       |
| ~~elektrificatie~~     | ~~ja~~; ~~nee~~                                                                    |
| ~~spoorbreedte~~       | ~~normaalspoor~~; ~~smalspoor~~                                                    |
| ~~vervoerfunctie~~     | ~~gemengd gebruik~~; ~~personenvervoer~~; ~~ goederenvervoer~~; ~~museumlijn |
| ~~baanvaknaam~~        | «tekst»                                                                                    |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-----------------------------------|----------------------------------------|
| geometrie                         | ~~«punt»~~                         |
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
