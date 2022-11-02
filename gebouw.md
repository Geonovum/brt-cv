Gebouw
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Gebouw in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Overzicht
---------

*Overzicht attributen en waarden/type van object Gebouw in BRT.Next*

| Attribuutnaam          | Waarde of «type»                                | Geometrietype | Kardinaliteit |
|------------------------|-------------------------------------------------|---------------|---------------|
| geometrie              | «Vlak»                                          |               | 1-1           |
|                        | «Punt»                                          |               |               |
| type                   | bunker                                          | vlak          | 1..n          |
|                        | kapel                                           | vlak, punt    |               |
|                        | kas                                             | vlak          |               |
|                        | kasteel                                         | vlak          |               |
|                        | kerk                                            | vlak          |               |
|                        | kernreactor                                     | vlak          |               |
|                        | klokkentoren                                    | vlak, punt    |               |
|                        | klooster, abdij                                 | vlak          |               |
|                        | koeltoren                                       | vlak          |               |
|                        | koepel                                          | vlak          |               |
|                        | moskee                                          | vlak          |               |
|                        | opslagtank                                      | vlak          |               |
|                        | overig religieus gebouw                         | vlak          |               |
|                        | parkeergarage                                   | vlak          |               |
|                        | radiotoren, televisietoren                      | vlak          |               |
|                        | ruïne                                           | vlak          |               |
|                        | schoorsteen                                     | vlak, punt    |               |
|                        | silo                                            | vlak          |               |
|                        | synagogue                                       | vlak          |               |
|                        | stadion                                         | vlak          |               |
|                        | telecommunicatietoren                           | vlak          |               |
|                        | toren                                           | vlak, punt    |               |
|                        | uitzichttoren                                   | vlak, punt    |               |
|                        | verkeerstoren                                   | vlak          |               |
|                        | vuurtoren                                       | vlak          |               |
|                        | waterradmolen                                   | vlak          |               |
|                        | watertoren                                      | vlak          |               |
|                        | waterwoning                                     | vlak          |               |
|                        | windmolen                                       | vlak          |               |
|                        | windturbine                                     | vlak          |               |
|                        | botenhuis                                       | vlak          |               |
|                        | open loods                                      | vlak          |               |
|                        | overkapping                                     | vlak          |               |
|                        | overig                                          | vlak          |               |
| functie                | brandweerkazerne                                |               | 0..n          |
|                        | crematorium                                     |               |               |
|                        | elektriciteitscentrale                          |               |               |
|                        | gemaal                                          |               |               |
|                        | gemeentehuis                                    |               |               |
|                        | gevangenis                                      |               |               |
|                        | kunstijsbaan                                    |               |               |
|                        | observatorium                                   |               |               |
|                        | paleis                                          |               |               |
|                        | parkeren                                        |               |               |
|                        | politiebureau                                   |               |               |
|                        | psychiatrisch ziekenhuis, psychiatrisch centrum |               |               |
|                        | radarstation                                    |               |               |
|                        | religie                                         |               |               |
|                        | schaapskooi                                     |               |               |
|                        | school                                          |               |               |
|                        | sporthal                                        |               |               |
|                        | stadskantoor, hulpsecretarie                    |               |               |
|                        | universiteit                                    |               |               |
|                        | ziekenhuis                                      |               |               |
|                        | zwembad                                         |               |               |
| ligging                | ondergronds                                     |               | 0..1          |
| hoogte                 | «decimaal getal»                                |               | 0..1          |
| relatieveHoogteligging | «geheel getal [-9; 9]»                          |               | 1-1           |
| status                 | bestaand                                        |               | 1-1           |
|                        |                                                 |               |               |
| soortnaam              | «tekst»                                         |               | 0..n          |
| naam                   | «tekst»                                         |               | 0..n          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| ~~fysiekVoorkomen~~ | **ligging**              |



### Definitie

Onderstaande attributen wijzigen van definitie in BRT.Next. De naam wordt niet
aangepast.

| *TOP10NL \| BRT.Next:attribuutnaam* | *TOP10NL:definitie*                                      | *BRT.Next:definitie*                                                |
|-------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------|
| status                              | ~~De staat waarin het~~ object ~~zich bevindt.~~ | **De status gekoppeld aan de levenscyclus van een geo-**object**.** |

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                                                          | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                                     |
|-------------------------|----------------------------------------------------------------------------------------------|--------------------------------|--------------------------------------------------------------------------|
| type~~Gebouw~~      | Het type gebouw, ~~het doel waarvoor de bebouwing gebruikt wordt (gaat worden / werd).~~ | **type**                   | Het type gebouw **gebaseerd op de uiterlijke kenmerken van het gebouw.** |
| ~~hoogteniveau~~    | ~~Het~~ hoogte~~niveau~~van het object.                                              | **relatieveHoogteligging**[^2] | **Aanduiding voor de relatieve** hoogte van het object.                  |

<details class="note">
typeGebouw wordt gesplitst in twee attributen: ‘type’ (uiterlijke
verschijningsvorm) en ‘functie’(gebruik). De attribuutwaarden die verplaatsen
van typeGebouw naar functie worden als vervallen bij typeGebouw opgenomen, en
als toegevoegde attribuutwaarden bij het nieuwe attribuut ‘functie’.
</details>

<details class="note">
Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van een geheel
getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9..
</details>

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

*Attribuut TOP10NL:typeGebouw \| BRT.Next:type*

| *TOP10NL:waarde*                              | *BRT.Next:waarde* |
|-----------------------------------------------|-------------------|
| kas~~, warenhuis~~                        | kas               |
| tank                                          | **opslag**tank    |
| ~~parkeerdak, parkeerdek, ~~parkeergarage | parkeergarage     |

### Definitie

Onderstaande attribuutwaarden wijzigen van definitie in BRT.Next. De naam wordt
niet aangepast.

*Attribuut TOP10NL:typeGebouw \| BRT.Next:type*

| *TOP10NL:waarde* | *TOP10NL:definitie*                                                                                                                                                                                                                   | *BRT.Next:definitie*                                                                                                                                                       |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| windmolen        | Bebouwing t.b.v. het verrichten van arbeid (m.u.v. het opwekken van elektrische energie~~, het malen van granen en het opvijzelen van water~~), waarvoor de energie geleverd wordt door wind en opgenomen door middel van wieken. | Bebouwing t.b.v. het verrichten van arbeid (m.u.v. het opwekken van elektrische energie) waarvoor de energie geleverd wordt door wind en opgenomen door middel van wieken. |
| windturbine      | ~~Bebouwing t.b.v. het opwekken van elektrische~~ energie~~, waarvoor de energie geleverd wordt door ~~wind ~~en opgenomen wordt door middel van wieken.~~                                                                | **Turbine waarin** wind**druk omgezet wordt in mechanische** energie.                                                                                                      |

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:status \| BRT.Next:status*

| *TOP10NL:waarde*                  | *TOP10NL:definitie*                                                                                                                                                      | *BRT.Next:waarde* | *BRT.Next:definitie*                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------------------------------------------------------|
| ~~kerncentrale~~, kernreactor | ~~Centrale die met kernenergie elektriciteit opwekt (kerncentrale) /~~ Installatie voor het splijten of fuseren van atoomkernen, atoomreactor ~~(kernreactor)~~. | kernreactor       | Installatie voor het splijten of fuseren van atoomkernen. |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                                                                                                                                   |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~hoogteklasse~~    | ~~laagbouw~~; ~~hoogbouw~~                                                                                                                                                                                                                                         |
| ~~gebruiksdoel~~    | ~~bijeenkomstfunctie~~;~~celfunctie~~;~~gezondheidszorgfunctie~~;~~industriefunctie~~;~~kantoorfunctie~~;~~logiesfunctie~~;~~onderwijsfunctie~~;~~sportfunctie~~;~~winkelfunctie~~;~~woonfunctie~~;~~overige gebruiksfunctie~~ |

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeGebouw \| type                | *verplaatsen van type naar functie:* ~~brandweerkazerne~~; ~~crematorium~~; ~~elektriciteitscentrale~~; ~~gemaal~~; ~~gemeentehuis~~; ~~kerncentrale, kernreactor~~; ~~kunstijsbaan~~; ~~observatorium~~; ~~paleis~~; ~~politiebureau~~; ~~psychiatrisch ziekenhuis, psychiatrisch centrum~~; ~~radarpost~~; ~~schaapskooi~~; ~~school~~; ~~sporthal~~; ~~stadskantoor, hulpsecretarie~~; ~~universiteit~~; ~~ziekenhuis~~; ~~zwembad~~                                                                                                                                                                       |
| typeGebouw \| type                | *verplaatsen van type naar ander objecttype:* ~~dok~~,~~ tankstation~~                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| typeGebouw \| type                | ~~bezoekerscentrum~~;~~boortoren~~\~,~~brandtoren~~;;~~fabriek~~;~~fort~~;~~gevangenis~~;~~hotel~~;~~huizenblok~~;~~kliniek, inrichting, sanatorium~~;~~lichttoren~~;~~luchtwachttoren~~;~~markant gebouw~~;~~manege~~;~~militair gebouw~~;~~museum~~;~~peilmeetstation~~;~~pompstation~~;;~~postkantoor~~;~~radartoren~~;~~recreatiecentrum~~;~~reddingboothuisje~~;~~remise~~;~~stationsgebouw~~;~~tankstation~~;~~tol~~;~~transformatorstation~~;~~veiling~~;~~wegrestaurant~~;~~werf~~;~~windmolen: korenmolen~~;~~windmolen: watermolen~~;~~zendtoren~~; |
| fysiekVoorkomen \| ligging        | ~~overkluisd~~                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| status                            | ~~in gebruik~~;~~buiten gebruik~~; ~~in uitvoering~~                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

<details class="note">
de attribuutwaarden ‘brandweerkazerne’, ‘crematorium’, …, ‘zwembad’
verplaatsen van attribuut typeGebouw\|type naar attribuut functie.</details>

<details class="note">
type ‘tankstation’ verplaatst naar objecttype FunctioneelGebied; type
‘dok’ verplaatst naar objecttype Inrichtingselement.</details>

<details class="note">
status ‘in gebruik’ en ‘buiten gebruik’ worden samengevoegd tot status
‘bestaand’.</details>

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                                                   | *Verplicht/optioneel*    | *Attribuutwaarde*                                                    |
|--------------------------|-------------------------------------------------------------------------------|--------------------------|----------------------------------------------------------------------|
| **functie**              | **De functie van het gebouw, de functie waarvoor het gebouw gebruikt wordt.** | **optioneel, 0 of meer** | *zie tabel attribuut BRT.Next:functie in Toevoegen attribuutwaarden* |

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:type*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **botenhuis**     | **Gebouw boven water voor de opslag van boten.**                                                                                          |
| **open loods**    | **Niet verplaatsbaar licht gebouw met een open gevel, bestemd als berg- of werkplaats of als tijdelijk onderdak voor andere doeleinden.** |
| **overkapping**   | **Een afzonderlijk staande overdekking rustend op kolommen.**                                                                             |

*Attribuut BRT.Next:functie*


| *BRT.Next:waarde*                                   | *BRT.Next:definitie*                           |
|-----------------------------------------------------|------------------------------------------------|
| **brandweerkazerne**                                | *definitie TOP10NL 1.2*                        |
| **crematorium**                                     | *definitie TOP10NL 1.2*                        |
| **elektriciteitscentrale**                          | *definitie TOP10NL 1.2*                        |
| **gemaal**                                          | *definitie TOP10NL 1.2*                        |
| **gemeentehuis**                                    | *definitie TOP10NL 1.2*                        |
| **gevangenis**                                      | *definitie TOP10NL 1.2*                        |
| **kerncentrale, kernreactor**                       | *definitie TOP10NL 1.2*                        |
| **kunstijsbaan**                                    | *definitie TOP10NL 1.2*                        |
| **observatorium**                                   | *definitie TOP10NL 1.2*                        |
| **paleis**                                          | *definitie TOP10NL 1.2*                        |
| **parkeren**                                        | *definitie TOP10NL 1.2*                        |
| **politiebureau**                                   | *definitie TOP10NL 1.2*                        |
| **psychiatrisch ziekenhuis, psychiatrisch centrum** | *definitie TOP10NL 1.2*                        |
| **radarstation**                                    | *definitie TOP10NL 1.2*                        |
| **religie**                                         | **Gebouw in gebruik voor geloofsuitoefening.** |
| **schaapskooi**                                     | *definitie TOP10NL 1.2*                        |
| **school**                                          | *definitie TOP10NL 1.2*                        |
| **sporthal**                                        | *definitie TOP10NL 1.2*                        |
| **stadskantoor, hulpsecretarie**                    | *definitie TOP10NL 1.2*                        |
| **universiteit**                                    | *definitie TOP10NL 1.2*                        |
| **waterwoning**                                     | *definitie TOP10NL 1.2*                        |
| **ziekenhuis**                                      | *definitie TOP10NL 1.2*                        |
| **zwembad**                                         | *definitie TOP10NL 1.2*                        |

<details class="note"> attribuutwaarden van BRT.Next:functie zijn overgenomen van
TOP10NL:typeGebouw; m.u.v. waarde ‘religie’: deze classificatie is nieuw
toegevoegd aan BRT.Next.
</details>

*Attribuut BRT.Next:status*

| *BRT.Next:status* | *BRT.Next:definitie*                                                                                          |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| **bestaand**      | **Situatie waarin het object wordt / kan worden gebruikt voor het doel waarvoor het is gebouwd / aangelegd.** |
