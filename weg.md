# Weg

Dit hoofdstuk beschrijft de wijzigingen voor het object Weg in BRT.Next ten
opzichte van de huidige versie TOP10NL.

## Overzicht

*Overzicht attributen en waarden/type van object Weg in BRT.Next*

| Attribuutnaam            | Waarde of «type»            | Geometrietype | Kardinaliteit |
|--------------------------|-----------------------------|---------------|---------------|
| geometrie                | «vlak»                      |               | 1 -1          |
|                          | «lijn»                      |               |               |
| typeWeg                  | autosnelweg                 | vlak          | 1..n          |
|                          | autoweg                     | vlak          |               |
|                          | hoofdweg                    | vlak          |               |
|                          | regionale weg               | vlak          |               |
|                          | lokale weg                  | vlak          |               |
|                          | straat                      | vlak          |               |
|                          | overig                      | vlak          |               |
|                          | parkeerplaats               | vlak          |               |
|                          | OV-baan                     | vlak          |               |
|                          | fietspad                    | vlak, lijn    |               |
|                          | voetpad                     | vlak, lijn    |               |
|                          | voetgangersgebied           | vlak          |               |
|                          | startbaan, landingsbaan     | vlak          |               |
|                          | rolbaan, platform           | vlak          |               |
|                          | veerverbinding              | lijn          |               |
|                          | fietsveer                   | lijn          |               |
|                          | voetveer                    | lijn          |               |
| ligging                  | op vast deel van brug       |               | 0..n          |
|                          | op beweegbaar deel van brug |               |               |
|                          | op rotonde                  |               |               |
|                          | op oprit / afrit            |               |               |
|                          | op knooppuntverbinding      |               |               |
|                          | op overweg                  |               |               |
|                          | in tunnel                   |               |               |
| verhardingsbreedteklasse | \> 7 meter                  |               |               |
|                          | 4 – 7 meter                 |               |               |
|                          | 2 – 4 meter                 |               |               |
|                          | \< 2 meter                  |               |               |
| verhardingstype          | verhard                     |               | 1-1           |
|                          | half verhard                |               |               |
|                          | onverhard                   |               |               |
|                          | onbekend                    |               |               |
| gescheidenRijbaan        | ja                          |               | 1-1           |
|                          | nee                         |               |               |
| relatieveHoogteligging   | «geheel getal [-9;9]»       |               | 1-1           |
| status                   | bestaand                    |               | 1-1           |
|                          | in aanbouw                  |               |               |
| naam                     | «tekst»                     |               | 0..n          |
| naam: herkomst           | «tekst»                     |               | 0..n          |
| A-wegnummer              | «tekst»                     |               | 0..n          |
| N-wegnummer              | «tekst»                     |               | 0..n          |
| E-wegnummer              | «tekst»                     |               | 0..n          |
| S-wegnummer              | «tekst»                     |               | 0..n          |
| afritnummer              | «tekst»                     |               | 0..1          |
| afritnaam                | «tekst»                     |               | 0..1          |
| knooppuntnaam            | «tekst»                     |               | 0..1          |
| brugnaam                 | «tekst»                     |               | 0..1          |
| tunnelnaam               | «tekst»                     |               | 0..1          |

## Wijzigen attributen

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| typeWeg                 | typeWeg**deel**          |
| ~~fysiekVoorkomen~~     | **ligging**              |
| ~~hoofdG~~eometrie      | **g**eometrie            |

<details class="note"> Aan geometrie wordt de volgende regel toegevoegd: *“Een smalle
berm (\< 6m) is geen onderdeel van het wegvlak."* --END NOTE--

### Definitie

Onderstaande attributen wijzigen van definitie in BRT.Next. De naam wordt niet
aangepast.

| *TOP10NL \| BRT.Next:attribuutnaam* | *TOP10NL:definitie*                                      | *BRT.Next:definitie*                                            |
|-------------------------------------|----------------------------------------------------------|-----------------------------------------------------------------|
| status                              | ~~De staat waarin het~~ object ~~zich bevindt.~~ | **De status gekoppeld aan de levenscyclus van een geo-object.** |

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|----------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het ~~hoogte~~niveau~~van het object. | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note"> Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van
een geheel getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9..
</details>

## Wijzigen attribuutwaarden

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Geen

### Definitie

Onderstaande attribuutwaarden wijzigen van definitie in BRT.Next. De naam wordt
niet aangepast.

*Attribuut TOP10NL:typeWeg \|BRT.Next:type*

| *TOP10NL \| BRT.Next:waarde* | *TOP10NL:definitie*                                                                                                                                                                                                                                                                                               | *BRT.Next:definitie*                                                                                                                                                                                                                                                                                                                              |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| autosnelweg                  | Weg dat onderdeel is van een weg uitsluitend bestemd voor snelverkeer ~~en met gescheiden rijbanen en ongelijkvloerse kruisingen~~, daartoe aangeduid met het betreffende verkeersbord.                                                                                                                   | Weg dat onderdeel is van een weg uitsluitend bestemd voor snelverkeer, daartoe aangeduid met het betreffende verkeersbord.                                                                                                                                                                                                                    |
| hoofdweg                     | ~~Verharde weg die~~ is aangeduid met een E-nummer, maar niet met een A-nummer, of verharde weg die onderdeel is van een verbindingsroute tussen grotere plaatsen, wat blijkt uit blauwe ANWB-borden, dan wel onderdeel is van een route om eindigende A of E-routes tot een gesloten netwerk te completeren. | Weg, **niet zijnde een autosnelweg of autoweg,** dat is aangeduid met een E-nummer, maar niet met een A-nummer, of verharde weg die onderdeel is van een verbindingsroute tussen grotere plaatsen, wat blijkt uit blauwe ANWB-borden, dan wel onderdeel is van een route om eindigende A of E-routes tot een gesloten netwerk te completeren. |
| regionale weg                | ~~Verharde~~ weg die een verbinding vormt tussen bewoonde oorden of ~~grote stads~~wijken ~~en daartoe van twee kanten bewegwijzerd zijn met blauwe ANWB-richtingsborden voor autoverkeer~~.                                                                                                          | **Weg dat onderdeel is van een** weg die een verbinding vormt tussen bewoonde oorden of tussen wijken **binnen een dorp of stad**.                                                                                                                                                                                                            |
| lokale weg                   | Weg van lokaal belang ~~tussen bewegwijzerde routes~~.                                                                                                                                                                                                                                                        | **Weg dat onderdeel is van een** weg van lokaal belang.                                                                                                                                                                                                                                                                                       |
| straat                       | Weg van zeer plaatselijk belang, gelegen binnen bebouwd gebied.                                                                                                                                                                                                                                                   | **Weg dat onderdeel is van een** weg van zeer plaatselijk belang, gelegen binnen ~~bebouwd~~ gebied **met bebouwing**.                                                                                                                                                                                                                    |
| parkeerplaats                | Parkeergelegenheid voor meerdere voertuigen in de openlucht.                                                                                                                                                                                                                                                      | Parkeergelegenheid voor **het parkeren van** meerdere voertuigen in de openlucht **met een aparte toegang vanaf de doorgaande weg.**                                                                                                                                                                                                              |
| startbaan, landingsbaan      | ~~Strook grond waar~~ vlieg~~tuigen kunnen~~ opstijgen en/of landen.                                                                                                                                                                                                                                      | **Weg uitsluitend bedoeld voor** vlieg**verkeer ten behoeve van het** opstijgen en/of landen van **vliegtuigen**.                                                                                                                                                                                                                             |
| rolbaan, platform            | ~~Afgebakende taxibaan op een vliegveld (rolbaan). / Terrein voor geparkeerd staande~~ vliegtuigen ~~(platform)~~.                                                                                                                                                                                        | **Weg uitsluitend bedoeld voor vliegverkeer ten behoeve van het taxiën of het parkeren van** vliegtuigen.                                                                                                                                                                                                                                     |

### Naam+definitie

Geen

## Vervallen attributen

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam*      | *TOP10NL:waarde of «type»*                                                                                                                                                           |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~hartGeometrie~~        | ~~«punt»~~; ~~«lijn»~~                                                                                                                                                       |
| ~~typeInfrastructuur~~   | ~~verbinding~~; ~~kruising~~; ~~overig verkeersgebied~~                                                                                                                  |
| ~~hoofdverkeersgebruik~~ | ~~vliegverkeer~~; ~~snelverkeer~~; ~~gemengd verkeer~~; ~~busverkeer~~; ~~fietsers~~, ~~bromfietsers~~; ~~voetgangers~~; ~~ruiters~~; ~~overig~~ |
| ~~aantalRijstroken~~     | ~~«geheel getal»~~                                                                                                                                                               |
| ~~isBAGnaam~~            | ~~ja~~; ~~nee~~                                                                                                                                                              |

## Vervallen attribuutwaarden

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:waarde of «type»*                                                           |
|-----------------------------------|--------------------------------------------------------------------------------------|
| geometrie                         | ~~«punt»~~                                                                       |
| typeWeg                       | ~~spoorbaanlichaam~~; ~~parkeerplaats: carpool~~; ~~parkeerplaats: P+R~~ |
| fysiekVoorkomen \| ligging        | ~~overkluisd~~                                                                   |
| status                            | ~~in uitvoering~~; ~~in gebruik~~; ~~buiten gebruik~~                    |

<details class="note"> Type ‘spoorbaanlichaam’ verplaatst naar type ‘spoorbaan’ van
objecttype Spoor. --END NOTE--

<details class="note"> status ‘in uitvoering’ en ‘in gebruik’ worden samengevoegd tot
status ‘bestaand’. --END NOTE--

## Toevoegen attributen

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                  | *Verplicht/optioneel*     | *Domein*    |
|--------------------------|----------------------------------------------|---------------------------|-------------|
| **naam:herkomst**        | **De herkomst van de naam van het wegdeel.** | **Optioneel [0 of meer]** | **«tekst»** |

## Toevoegen attribuutwaarden

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:type*

| *BRT.Next:waarde*     | *BRT.Next:definitie*                                                                                                                                                                               |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **autoweg**           | **Weg dat onderdeel is van een weg uitsluitend bestemd voor snelverkeer, daartoe aangeduid met het betreffende verkeersbord.**                                                                 |
| **OV-baan**           | **Weg dat uitsluitend is bestemd en gemarkeerd voor openbaar vervoer en afgescheiden is van de andere wegdelen niet uitsluitend door markering.**                                              |
| **fietspad**          | **Weg met name bestemd voor fietsers en, indien toegestaan, bromfietsers en dat afgescheiden is van de andere wegdelen niet uitsluitend door markering.**                                      |
| **voetpad**           | **Weg waar voetgangers gebruik van moeten maken.**                                                                                                                                             |
| **voetgangersgebied** | **Weg alleen voor het gebruik door voetgangers, waarbij het door voetgangers te gebruiken gebied de volle breedte van de weg beslaat en het gebied een nadrukkelijk openbaar karakter heeft.** |
| **fietsveer**         | **Vastgelegde route over water om fietsers en voetgangers over te zetten al dan niet op basis van een vaste dienstregeling.**                                                                      |
| **voetveer**          | **Vastgelegde route over water om voetgangers over te zetten al dan niet op basis van een vaste dienstregeling.**                                                                                  |

**Attribuut BRT.Next:ligging**

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                         |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| **op overweg**    | **Een gelijkvloerse kruising van een wegdeel en een wegdeel type ov-baan met spoor type trein of sneltram.** |

*Attribuut BRT.Next:status*

| *BRT.Next:status* | *BRT.Next:definitie*                                                                                               |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| **bestaand**      | **Object dat in gebruik is genomen of als gebruiksgereed kan worden beschouwd, dan wel buiten gebruik is gesteld** |
| **in aanbouw**    | **Object waarvan de feitelijke bouw, verbouw of aanleg is aangevangen.**                                           |
