Wegdeel
=======

Dit hoofdstuk beschrijft de wijzigingen voor het object Wegdeel in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Weg~~         | **type**                 |
| **fysiekVoorkomen**     | **ligging**              |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|----------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het ~~hoogte~~niveau~~van het object. | **relatieveHoogteLigging** | **Aanduiding voor de relatieve** hoogte van het object. |

*Overige opmerking:*

-   Het domein van hoogteniveau/relatieveHoogteligging wijzigt van geheel getal
    Kleiner of gelijk aan 0 naar geheel getal tussen -9 en 9.

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

| *TOP10NL:waarde*       | *BRT.Next:waarde*        |
|------------------------|--------------------------|
| straat                 | **rijbaan** straat       |
| overig                 | **rijbaan** overig       |
| parkeer~~plaats~~  | parkeer**vak**           |
| veer~~verbinding~~ | veer**dienst, pontveer** |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande classificaties wijzigen van naam (waarde) en definitie in BRT.Next

*Attribuut TOP10NL:typeWeg / BRT.Next:type*

| *TOP10NL:waarde*             | *TOP10NL:definitie*                                                                                                                                                                                                                                                                                                       | *BRT.Next:waarde*         | *BRT.Next:definitie*                                                                                                                   |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| autosnelweg                  | Wegdeel dat onderdeel is van een weg uitsluitend bestemd voor snelverkeer ~~en met gescheiden rijbanen en ongelijkvloerse kruisingen~~, daartoe aangeduid met het betreffende verkeersbord.                                                                                                                           | **rijbaan** autosnelweg   | Wegdeel dat onderdeel is van een weg uitsluitend bestemd voor snelverkeer, daartoe aangeduid met het betreffende verkeersbord.         |
| ~~hoofdweg~~             | ~~Verharde weg die is aangeduid met een E-nummer, maar niet met een A-nummer, of verharde weg die ~~onderdeel is van ~~een verbindingsroute tussen grotere plaatsen, wat blijkt uit blauwe ANWB-borden, dan wel onderdeel is van een route om eindigende A of E-routes tot een gesloten netwerk te completeren.~~ | **rijbaan autoweg**       | **Wegdeel dat** onderdeel is van **een weg uitsluitend bestemd voor snelverkeer, daartoe aangeduid met het betreffende verkeersbord.** |
| regionale weg                | ~~Verharde~~ weg die een verbinding vormt tussen bewoonde oorden of ~~grote stads~~wijken ~~en daartoe van twee kanten bewegwijzerd zijn met blauwe ANWB-richtingsborden voor autoverkeer~~.                                                                                                                  | **rijbaan** regionale weg | **Wegdeel dat onderdeel is van een** weg die een verbinding vormt tussen bewoonde oorden of tussen wijken **binnen een dorp of stad**. |
| lokale weg                   | Weg van lokaal belang ~~tussen bewegwijzerde routes~~.                                                                                                                                                                                                                                                                | **rijbaan** lokale weg    | **Wegdeel dat onderdeel is van een** weg van lokaal belang.                                                                            |
| spoorbaan~~lichaam~~[^1] | ~~Geheel van~~ rails~~, dwarsliggers e.d. waarover de trein, metro of sneltram rijdt.~~                                                                                                                                                                                                                           | spoorbaan                 | **Gebaand gedeelte voor het verkeer over** rails.                                                                                      |

[^1]: spoorbaanlichaam is onderdeel van de waardenverzameling typeLandgebruik.

*Attribuut TOP10NL:status / BRT.Next:status*

| *TOP10NL:waarde* | *TOP10NL:definitie*                      | *BRT.Next:waarde* | *BRT.Next:definitie* |
|------------------|------------------------------------------|-------------------|----------------------|
| in uitvoering    | De staat waarin het object zich bevindt. | **bestaand**      |                      |
| in gebruik       |                                          | **bestaand**      |                      |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam*   | *TOP10NL:classificaties of «datatype»*                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------|
| type                      | verbinding; kruising; overig parkeergebied                                                                   |
| hoofdverkeersgebruik      | vliegverkeer; snelverkeer; gemengd verkeer; busverkeer; fietsers, bromfietsers; voetgangers; ruiters; overig |
| verhardingsbreedte-klasse | \> 7 meter; 4 – 7 meter; 2 – 4 meter; \< 2 meter;                                                            |
| gescheidenRijbaan         | ja; nee                                                                                                      |
| aantalRijstroken          | «geheel getal»                                                                                               |
| isBAGnaam                 | ja; nee                                                                                                      |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL/BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*     |
|----------------------------------|--------------------------------------------|
| geometrie                        | «punt»                                     |
| typeWeg / type                   | parkeerplaats: carpool; parkeerplaats: P+R |
| fysiekVoorkomen / ligging        | overkluisd                                 |
| status                           | buiten gebruik                             |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie* | *Verplicht/optioneel* | *Domein*              |
|--------------------------|-------------|-----------------------|-----------------------|
| herkomst                 |             | Optioneel [0 of meer] | BAG, BGT, BRK, overig |

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:naam:herkomst*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **BAG**           |                      |
| **BGT**           |                      |
| **BRK**           |                      |
| **overig**        |                      |

*Attribuut BRT.Next:type*

| *BRT.Next:waarde*     | *BRT.Next:definitie*                                                                                                                                                                           |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OV-baan**           | Wegdeel dat uitsluitend is bestemd en gemarkeerd voor openbaar vervoer en afgescheiden is van de andere wegdelen niet uitsluitend door markering.                                              |
| **fietspad**          | Wegdeel met name bestemd voor fietsers en, indien toegestaan, bromfietsers en dat afgescheiden is van de andere wegdelen niet uitsluitend door markering.                                      |
| **voetpad**           | Wegdeel waar voetgangers gebruik van moeten maken.                                                                                                                                             |
| **voetgangersgebied** | Wegdeel alleen voor het gebruik door voetgangers, waarbij het door voetgangers te gebruiken gebied de volle breedte van de weg beslaat en het gebied een nadrukkelijk openbaar karakter heeft. |
| **ruiterpad**         | Een wegdeel primair aangelegd voor het gebruik door ruiters.                                                                                                                                   |
| **fietsveer**         | Vastgelegde route over water om voertuigen en personen over te zetten al dan niet op basis van een vaste dienstregeling.                                                                       |
| **voetveer**          | Vastgelegde route over water om voertuigen en personen over te zetten al dan niet op basis van een vaste dienstregeling.                                                                       |
| **spoorbaan**         | Gebaand gedeelte voor het verkeer over rails.                                                                                                                                                  |

**Attribuut BRT.Next:ligging**

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **op overweg**    |                      |
