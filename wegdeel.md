Wegdeel
=======

Dit hoofdstuk beschrijft de wijzigingen voor het object Wegdeel in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeWeg’ wordt hernoemd naar ‘type’, ‘fysiekVoorkomen naar
    ‘ligging’, en ‘hoofdGeometrie’ naar ‘geometrie’.

-   typen, ‘overig’, en ‘veerverbinding’ worden hernoemd naar respectievelijk
    ‘rijbaan overig’ en ‘veerdienst, pontveer’.

-   typen ‘autosnelweg’, ‘hoofdweg’, ‘regionale weg’, ‘lokale weg’, ‘straat’,
    en ‘parkeerplaats’ worden hernoemd naar respectievelijk
    BGT-functies ‘rijbaan autosnelweg’, ‘rijbaan autoweg’, ‘rijbaan regionale
    weg’, ‘rijbaan lokale weg’, ‘rijbaan straat’ en ‘parkeervak’,
    en de definities worden aangepast o.m. naar de BGT-definities.
	
-   typeLandgebruik 'spoorbaanlichaam' wordt verplaatst van object Terrein naar type 'spoorbaan' van Wegdeel, met aangepaste definitie naar BGT.

-   typen ‘OV-baan’, ‘fietspad’, ‘voetpad’, ‘voetgangersgebied’, ‘ruiterpad’,
    ‘fietsveer’, en ‘voetveer’ worden toegevoegd.

-   typen ‘parkeerplaats: carpool’ en ‘parkeerplaats: P+R’ vervallen.

-   fysiekVoorkomen ‘overkluisd’ vervalt bij attribuut ligging, en ‘op overweg’
    wordt toegevoegd aan attribuut ligging.

-   attribuut ‘hoogteniveau’ wordt hernoemd naar ‘relatieveHoogteligging’,
    definitie wordt en bereik -9 tot 9 wordt aangepast op BGT.

-   statussen ‘in uitvoering’ en ‘in gebruik’ worden samengevoegd tot ‘bestaand’
    met BGT-definitie, en status ‘buiten gebruik’ vervalt.

-   attributen ‘hartGeometrie’, ‘typeInfrastructuur’, ‘hoofdverkeersgebruik’,
    ‘verhardingsbreedte-klasse’, ‘gescheidenRijbaan’, ‘aantalRijstroken’
    ‘isBAGnaam’ vervallen.

-   attribuut ‘herkomst’ met waarden ‘BAG’, ‘BGT’, ‘BRK’ of ‘overig’ wordt
    toegevoegd.

-   puntgeometrie vervalt.

*Overzicht attributen en waarden/type van object Wegdeel in BRT.Next*

| Attribuutnaam          | Waarde of \<type\>          | Geometrietype | Kardinaliteit |
|------------------------|-----------------------------|---------------|---------------|
| geometrie              | «vlak»                      |               | 1 -1          |
|                        | «lijn»                      |               |               |
| type                   | rijbaan autosnelweg         | vlak          | 1..n          |
|                        | rijbaan autoweg             | vlak          |               |
|                        | rijbaan regionale weg       | vlak          |               |
|                        | rijbaan lokale weg          | vlak          |               |
|                        | rijbaan straat              | vlak          |               |
|                        | rijbaan overig              | vlak          |               |
|                        | parkeervlak                 | vlak          |               |
|                        | OV-baan                     | vlak          |               |
|                        | fietspad                    | vlak, lijn    |               |
|                        | voetpad                     | vlak, lijn    |               |
|                        | voetgangersgebied           | vlak          |               |
|                        | ruiterpad                   | vlak, lijn    |               |
|                        | startbaan, landingsbaan     | vlak          |               |
|                        | rolbaan, platform           | vlak          |               |
|                        | veerdienst, pontveer        | lijn          |               |
|                        | fietsveer                   | lijn          |               |
|                        | voetveer                    | lijn          |               |
|                        | spoorbaan                   | vlak          |               |
| ligging                | op vast deel van brug       |               | 0..n          |
|                        | op beweegbaar deel van brug |               |               |
|                        | op rotonde                  |               |               |
|                        | op oprit / afrit            |               |               |
|                        | op knooppuntverbinding      |               |               |
|                        | op overweg                  |               |               |
|                        | in tunnel                   |               |               |
| verhardingstype        | verhard                     |               | 1-1           |
|                        | half verhard                |               |               |
|                        | onverhard                   |               |               |
|                        | onbekend                    |               |               |
| relatieveHoogteligging | «geheel getal [-9;9]»       |               | 1-1           |
| status                 | bestaand                    |               | 1-1           |
| naam                   | «tekst»                     |               | 0..n          |
| naam: herkomst         | BAG                         |               | 0..n          |
|                        | BGT                         |               |               |
|                        | BRK                         |               |               |
|                        | overig                      |               |               |
| A-wegnummer            | «tekst»                     |               | 0..n          |
| N-wegnummer            | «tekst»                     |               | 0..n          |
| E-wegnummer            | «tekst»                     |               | 0..n          |
| S-wegnummer            | «tekst»                     |               | 0..n          |
| afritnummer            | «tekst»                     |               | 0..1          |
| afritnaam              | «tekst»                     |               | 0..1          |
| knooppuntnaam          | «tekst»                     |               | 0..1          |
| brugnaam               | «tekst»                     |               | 0..1          |
| tunnelnaam             | «tekst»                     |               | 0..1          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Weg~~         | type                     |
| ~~fysiekVoorkomen~~ | **ligging**              |
| ~~hoofdG~~eometrie  | **g**eometrie            |

### Definitie

Onderstaande attributen wijzigen van definitie in BRT.Next. De naam wordt niet
aangepast.

| *TOP10NL \| BRT.Next:attribuutnaam* | *TOP10NL:definitie*                                                                                                        | *BRT.Next:definitie*                                                                                                              |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| startbaan, landingsbaan             | ~~Strook grond waar~~ vlieg~~tuigen kunnen~~ opstijgen en/of landen.                                               | **Wegdeel uitsluitend bedoeld voor** vlieg**verkeer ten behoeve van het** opstijgen en/of landen.                                 |
| rolbaan, platform                   | ~~Afgebakende taxibaan op een vliegveld (rolbaan). / Terrein voor geparkeerd staande~~ vliegtuigen ~~(platform)~~. | **Wegdeel uitsluitend bedoeld voor vliegverkeer ten behoeve van het taxiën van vliegtuigen of het parkeren van** vliegtuigen**.** |

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|--------------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het ~~hoogte~~niveau~~van het object. | **relatieveHoogteligging**[^1] | **Aanduiding voor de relatieve** hoogte van het object. |

<details class='note'>Het bereik van hoogteniveau|relatieveHoogteligging wijzigt van een geheel
getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details>

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

*Attribuut TOP10NL:typeWeg \|BRT.Next:type*

| *TOP10NL:waarde*       | *BRT.Next:waarde*        |
|------------------------|--------------------------|
| overig                 | **rijbaan** overig       |
| veer~~verbinding~~ | veer**dienst, pontveer** |

### Definitie

Onderstaande attribuutwaarden wijzigen van definitie in BRT.Next. De naam wordt
niet aangepast.

| *TOP10NL \| BRT.Next:attribuutnaam* | *TOP10NL:definitie*                                      | *BRT.Next:definitie*                                                |
|-------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------|
| status                              | ~~De staat waarin het~~ object ~~zich bevindt.~~ | **De status gekoppeld aan de levenscyclus van een geo-**object**.** |

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeWeg / BRT.Next:type*

| *TOP10NL:waarde*             | *TOP10NL:definitie*                                                                                                                                                                                                                                                                                                       | *BRT.Next:waarde*         | *BRT.Next:definitie*                                                                                                                   |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| autosnelweg                  | Wegdeel dat onderdeel is van een weg uitsluitend bestemd voor snelverkeer ~~en met gescheiden rijbanen en ongelijkvloerse kruisingen~~, daartoe aangeduid met het betreffende verkeersbord.                                                                                                                           | **rijbaan** autosnelweg   | Wegdeel dat onderdeel is van een weg uitsluitend bestemd voor snelverkeer, daartoe aangeduid met het betreffende verkeersbord.         |
| ~~hoofdweg~~             | ~~Verharde weg die is aangeduid met een E-nummer, maar niet met een A-nummer, of verharde weg die ~~onderdeel is van ~~een verbindingsroute tussen grotere plaatsen, wat blijkt uit blauwe ANWB-borden, dan wel onderdeel is van een route om eindigende A of E-routes tot een gesloten netwerk te completeren.~~ | **rijbaan autoweg**       | **Wegdeel dat** onderdeel is van **een weg uitsluitend bestemd voor snelverkeer, daartoe aangeduid met het betreffende verkeersbord.** |
| regionale weg                | ~~Verharde~~ weg die een verbinding vormt tussen bewoonde oorden of ~~grote stads~~wijken ~~en daartoe van twee kanten bewegwijzerd zijn met blauwe ANWB-richtingsborden voor autoverkeer~~.                                                                                                                  | **rijbaan** regionale weg | **Wegdeel dat onderdeel is van een** weg die een verbinding vormt tussen bewoonde oorden of tussen wijken **binnen een dorp of stad**. |
| lokale weg                   | Weg van lokaal belang ~~tussen bewegwijzerde routes~~.                                                                                                                                                                                                                                                                | **rijbaan** lokale weg    | **Wegdeel dat onderdeel is van een** weg van lokaal belang.                                                                            |
| straat                       | Weg van zeer plaatselijk belang, gelegen binnen bebouwd gebied.                                                                                                                                                                                                                                                           | **rijbaan** straat        | **Wegdeel dat onderdeel is van een** weg van zeer plaatselijk belang, gelegen binnen bebouwd gebied.                                   |
| parkeer~~plaats~~        | ~~Parkeergelegenheid voor meerdere~~ voertuigen ~~in de openlucht.~~                                                                                                                                                                                                                                              | parkeer**vak**            | **Wegdeel bestemd voor het parkeren van motor**voertuigen.                                                                             |
| spoorbaan~~lichaam~~ | ~~Geheel van~~ rails~~, dwarsliggers e.d. waarover de trein, metro of sneltram rijdt.~~                                                                                                                                                                                                                           | spoorbaan                 | **Gebaand gedeelte voor het verkeer over** rails.                                                                                      |

<details class="note">
typeLandgebruik 'spoorbaanlichaam' wordt verplaatst van object Terrein naar type 'spoorbaan' van Wegdeel.
</details>

*Attribuut TOP10NL:status \| BRT.Next:status*

| *TOP10NL:waarde*      | *TOP10NL:definitie*                      | *BRT.Next:waarde* | *BRT.Next:definitie* |
|-----------------------|------------------------------------------|-------------------|----------------------|
| ~~in uitvoering~~ | De staat waarin het object zich bevindt. | **bestaand**      |                      |
| ~~in gebruik~~    |                                          | **bestaand**      |                      |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam*           | *TOP10NL:waarde of «type»*                                                                                                                                                           |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~hartGeometrie                 | ~~«punt»~~, ~~«lijn»~~                                                                                                                                                       |
| ~~typeInfrastructuur~~        | ~~verbinding~~<br /> ~~kruising~~<br /> ~~overig parkeergebied~~                                                                                                                   |
| ~~hoofdverkeersgebruik~~      | ~~vliegverkeer~~<br /> ~~snelverkeer~~<br /> ~~gemengd verkeer~~<br /> ~~busverkeer~~<br /> ~~fietsers~~, ~~bromfietsers~~<br /> ~~voetgangers~~<br /> ~~ruiters~~<br /> ~~overig~~ |
| ~~verhardingsbreedte-klasse~~ | ~~\> 7 meter~~<br /> ~~4 – 7 meter~~<br /> ~~2 – 4 meter~~<br /> ~~\< 2 meter~~<br />                                                                                                    |
| ~~gescheidenRijbaan~~         | ~~ja~~<br /> ~~nee~~                                                                                                                                                              |
| ~~aantalRijstroken~~          | ~~«geheel getal»~~                                                                                                                                                               |
| ~~isBAGnaam~~                 | ~~ja~~<br /> ~~nee~~                                                                                                                                                              |

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:waarde of «type»*                                            |
|-----------------------------------|-----------------------------------------------------------------------|
| geometrie                         | ~~«punt»~~                                                        |
| typeWeg \| type                   | ~~parkeerplaats: carpool~~<br/> ~~parkeerplaats: P+R~~            |
| fysiekVoorkomen \| ligging        | ~~overkluisd~~                                                    |
| status                            | ~~in uitvoering~~<br/> ~~in gebruik~~<br/> ~~buiten gebruik~~ |

<details class="note">status ‘in uitvoering’ en ‘in gebruik’ worden samengevoegd tot status
‘bestaand’.
</details>

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                  | *Verplicht/optioneel*     | *Domein*                  |
|--------------------------|----------------------------------------------|---------------------------|---------------------------|
| **herkomst**             | **De herkomst van de naam van het wegdeel.** | **Optioneel [0 of meer]** | **BAG, BGT, BRK, overig** |

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:type*

| *BRT.Next:waarde*     | *BRT.Next:definitie*                                                                                                                                                                               |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OV-baan**           | **Wegdeel dat uitsluitend is bestemd en gemarkeerd voor openbaar vervoer en afgescheiden is van de andere wegdelen niet uitsluitend door markering.**                                              |
| **fietspad**          | **Wegdeel met name bestemd voor fietsers en, indien toegestaan, bromfietsers en dat afgescheiden is van de andere wegdelen niet uitsluitend door markering.**                                      |
| **voetpad**           | **Wegdeel waar voetgangers gebruik van moeten maken.**                                                                                                                                             |
| **voetgangersgebied** | **Wegdeel alleen voor het gebruik door voetgangers, waarbij het door voetgangers te gebruiken gebied de volle breedte van de weg beslaat en het gebied een nadrukkelijk openbaar karakter heeft.** |
| **ruiterpad**         | **Een wegdeel primair aangelegd voor het gebruik door ruiters.**                                                                                                                                   |
| **fietsveer**         | **Vastgelegde route over water om fietsers en voetgangers over te zetten al dan niet op basis van een vaste dienstregeling.**                                                                      |
| **voetveer**          | **Vastgelegde route over water om voetgangers over te zetten al dan niet op basis van een vaste dienstregeling.**                                                                                  |

**Attribuut BRT.Next:ligging**

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                         |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| **op overweg**    | **Een gelijkvloerse kruising van een wegdeel en een wegdeel type ov-baan met spoor type trein of sneltram.** |

*Attribuut BRT.Next:status*

| *BRT.Next:status* | *BRT.Next:definitie*                                            |
|-------------------|-----------------------------------------------------------------|
| **bestaand**      | **De status gekoppeld aan de levenscyclus van een geo-object.** |

*Attribuut BRT.Next:naam:herkomst*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                      |
|-------------------|-------------------------------------------------------------------------------------------|
| **BAG**           | Naam van het wegdeel is afkomstig uit de Basisregistratie Adressen en Gebouwen (BAG).     |
| **BGT**           | Naam van het wegdeel is afkomstig uit de Basisregistratie Grootschalige Topografie (BGT). |
| **BRK**           | Naam van het wegdeel is afkomstig uit de Basisregistratie Kadaster (BRK).                 |
| **overig**        | Naam van het wegdeel is afkomstig uit een andere bron.                                    |
