Gebouw
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Gebouw in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

n.v.t.

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                                                                                  | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                                              |
|-------------------------|----------------------------------------------------------------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------|
| type~~Gebouw~~      | Het type gebouw, ~~het doel waarvoor de bebouwing gebruikt wordt (gaat worden / werd).~~                         | **type**[^1]                   | Het type gebouw **gebaseerd op de uiterlijke kenmerken van het gebouw.**          |
| type~~Gebouw~~      | Het ~~type~~ gebouw, ~~het doel~~ waarvoor de ~~bebouwing~~ gebruikt wordt ~~(gaat worden / werd).~~ | **functie1**                   | De **functie van het** gebouw, de functie waarvoor het **gebouw** gebruikt wordt. |
| ~~hoogteniveau~~    | ~~Het ~~hoogte~~niveau~~van het object.                                                                      | **relatieveHoogteLigging**[^2] | **Aanduiding voor de relatieve** hoogte van het object.                           |

[^1]: typeGebouw wordt gesplitst in twee attributen: ‘type’ (uiterlijke
verschijningsvorm) en ‘functie’”(gebruik). De classificaties die verplaatsen van
typeGebouw naar functie worden als vervallen bij typeGebouw opgenomen, en als
toegevoegd bij functie.

[^2]: Het domein van hoogteniveau/relatieveHoogteligging wijzigt van geheel
getal Kleiner of gelijk aan 0 naar geheel getal tussen -9 en 9.

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

*Attribuut TOP10NL:typeGebouw / BRT.Next:type*

| *TOP10NL:waarde*       | *BRT.Next:waarde* |
|------------------------|-------------------|
| kas~~, warenhuis~~ | kas               |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande classificaties wijzigen van naam (waarde) en definitie in BRT.Next

*Attribuut TOP10NL:status / BRT.Next:status*

| *TOP10NL:waarde* | *TOP10NL:definitie* | *BRT.Next:waarde* | *BRT.Next:definitie* |
|------------------|---------------------|-------------------|----------------------|
| in gebruik       |                     | **bestaand**      |                      |
| buiten gebruik   |                     | **bestaand**      |                      |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                                                                                                                                                                                     |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~hoogteklasse~~    | ~~laagbouw~~; ~~hoogbouw~~                                                                                                                                                                                                                                         |
| ~~gebruiksdoel~~    | ~~bijeenkomstfunctie~~;~~celfunctie~~;~~gezondheidszorgfunctie~~;~~industriefunctie~~;~~kantoorfunctie~~;~~logiesfunctie~~;~~onderwijsfunctie~~;~~sportfunctie~~;~~winkelfunctie~~;~~woonfunctie~~;~~overige gebruiksfunctie~~ |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL/BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeGebouw \| type               | ~~brandweerkazerne~~;~~crematorium~~;~~elektriciteitscentrale~~;~~gemaal~~;~~gemeentehuis~~;~~kerncentrale, kernreactor~~;~~kunstijsbaan~~;~~observatorium~~;~~paleis~~;~~parkeerdak, parkeerdek, parkeergarage~~;~~politiebureau~~;~~radarpost~~;~~religie~~;~~schaapskooi~~;~~school~~;~~sporthal~~;~~stadskantoor, hulpsecretarie~~;~~universiteit~~;~~zwembad~~[^3]                                                                                                                                                                                                                                                                                                                                                            |
| typeGebouw \| type               | ~~bezoekerscentrum~~;~~brandtoren~~;~~dok~~;~~fabriek~~;~~fort~~;~~gevangenis~~;~~hotel~~;~~huizenblok~~;~~kliniek, inrichting, sanatorium~~;~~lichttoren~~;~~luchtwachttoren~~;~~markant gebouw~~;~~manege~~;~~militair gebouw~~;~~museum~~;~~peilmeetstation~~;~~pompstation~~;~~psychiatrisch ziekenhuis, psychiatrisch centrum~~;~~postkantoor~~;~~radartoren~~;~~recreatiecentrum~~;~~reddingboothuisje~~;~~remise~~;~~stationsgebouw~~;~~synagoge~~;~~tank~~;~~tanstation~~;~~tol~~;~~transformatorstation~~;~~veiling~~;~~wegrestaurant~~;~~werf~~;~~windmolen: korenmolen~~;~~windmolen: watermolen~~;~~windturbine~~;~~zendtoren~~;~~ziekenhuis~~ |
| fysiekVoorkomen                  | ~~overkluisd~~                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| status                           | ~~in uitvoering~~                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

[^3]: Deze classificaties vervallen bij typeGebouw\|type, maar worden opgenomen
bij attribuut functie in BRT.Next.

Toevoegen attributen
--------------------

n.v.t.

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:functie*[^4]

[^4]: classificaties van BRT.Next:functie zijn overgenomen van
TOP10NL:typeGebouw; m.u.v. religie: deze classificatie is nieuw toegevoegd.

| *BRT.Next:waarde*                         | *BRT.Next:definitie* |
|-------------------------------------------|----------------------|
| **brandweerkazerne**                      |                      |
| **crematorium**                           |                      |
| **elektriciteitscentrale**                |                      |
| **gemaal**                                |                      |
| **gemeentehuis**                          |                      |
| **kerncentrale, kernreactor**             |                      |
| **kunstijsbaan**                          |                      |
| **observatorium**                         |                      |
| **paleis**                                |                      |
| **parkeerdak, parkeerdek, parkeergarage** |                      |
| **politiebureau**                         |                      |
| **radarpost**                             |                      |
| **religie**[^5]                           |                      |
| **schaapskooi**                           |                      |
| **school**                                |                      |
| **sporthal**                              |                      |
| **stadskantoor, hulpsecretarie**          |                      |
| **universiteit**                          |                      |
| **zwembad**                               |                      |

[^5]: classificatie ‘religie’ bij functie is nieuw in BRT.Next, en niet
overgenomen van typeGebouw in TOP10NL.
