Gebouw
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Gebouw in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeGebouw’ wordt gesplitst in een attribuut ‘type’ en een
    attribuut ‘functie’.

-   de volgende typenGebouw verplaatsen naar attribuut functie:
    'brandweerkazerne', 'crematorium', 'elektriciteitscentrale', 'gemaal',
    'gemeentehuis', 'kerncentrale, kernreactor', 'kunstijsbaan',
    'observatorium', 'paleis', 'parkeerdak, parkeerdek, parkeergarage',
    'politiebureau', 'radarpost', 'religie', 'schaapskooi', 'school',
    'sporthal', 'stadskantoor, hulpsecretarie', 'universiteit', 'zwembad'

-   de volgen typenGebouw vervallen: 'bezoekerscentrum', 'brandtoren', 'dok',
    'fabriek', 'fort', 'gevangenis', 'hotel', 'huizenblok', 'kliniek,
    inrichting, sanatorium', 'lichttoren', 'luchtwachttoren', 'markant gebouw',
    'manege', 'militair gebouw', 'museum', 'peilmeetstation', 'pompstation',
    'psychiatrisch ziekenhuis, psychiatrisch centrum', 'postkantoor',
    'radartoren', 'recreatiecentrum', 'reddingboothuisje', 'remise',
    'stationsgebouw', 'synagoge', 'tank', 'tanstation', 'tol',
    'transformatorstation', 'veiling', 'wegrestaurant', 'werf', 'windmolen:
    korenmolen', 'windmolen: watermolen', 'windturbine', 'zendtoren',
    'ziekenhuis'

-   type ‘kas, warenhuis’ wordt hernoemd naar ‘kas’, type ‘kerncentrale,
    kernreactor’ wordt hernoemd naar ‘kernreactor’ met aangepaste definitie.

-   functie ‘religie’ wordt toegevoegd.

-   type ‘waterwoning’ wordt toegevoegd.

-   fysiekVoorkomen ‘overkluisd’ vervalt bij attribuut ligging.

-   attribuut ‘hoogteniveau’ wordt hernoemd naar ‘relatieveHoogteligging’,
    definitie wordt en bereik -9 tot 9 wordt aangepast op BGT.

-   de definitie van attribuut ‘status’ wordt aangepast naar BGT<br />

-   statussen ‘in gebruik’ en ‘buiten gebruik’ worden samengevoegd tot
    ‘bestaand’ met BGT-definitie, en status ‘in uitvoering’ vervalt.

-   attributen ‘hoogteklasse’ en ‘gebruiksdoel’ vervallen.

*Overzicht attributen en waarden/type van object Gebouw in BRT.Next*

| Attribuutnaam          | Waarde of «type»                      | Geometrietype | Kardinaliteit |
|------------------------|---------------------------------------|---------------|---------------|
| geometrie              | «Vlak»                                |               | 1-1           |
|                        | «Punt»                                |               |               |
| type                   |                                       |               | 1..n          |
|                        | boortoren                             | vlak, punt    |               |
|                        | bunker                                | vlak          |               |
|                        | kapel                                 | vlak, punt    |               |
|                        | kas                                   | vlak          |               |
|                        | kasteel                               | vlak          |               |
|                        | kerk                                  | vlak          |               |
|                        | kernreactor                           | vlak          |               |
|                        | klokkentoren                          | vlak, punt    |               |
|                        | klooster, abdij                       | vlak          |               |
|                        | koeltoren                             | vlak          |               |
|                        | koepel                                | vlak          |               |
|                        | moskee                                | vlak          |               |
|                        | overig religieus gebouw               | vlak          |               |
|                        | parkeerdak, parkeerdek, parkeergarage | vlak          |               |
|                        | radiotoren, televisietoren            | vlak          |               |
|                        | ruïne                                 | vlak          |               |
|                        | schoorsteen                           | vlak, punt    |               |
|                        | silo                                  | vlak          |               |
|                        | stadion                               | vlak          |               |
|                        | telecommunicatietoren                 | vlak          |               |
|                        | toren                                 | vlak, punt    |               |
|                        | uitzichttoren                         | vlak, punt    |               |
|                        | verkeerstoren                         | vlak          |               |
|                        | vuurtoren                             | vlak          |               |
|                        | waterradmolen                         | vlak          |               |
|                        | watertoren                            | vlak          |               |
|                        | waterwoning                           | vlak          |               |
|                        | windmolen                             | vlak          |               |
|                        | overig                                | vlak          |               |
| functie                |                                       |               | 0..n          |
|                        | brandweerkazerne                      |               |               |
|                        | crematorium                           |               |               |
|                        | elektriciteitscentrale                |               |               |
|                        | gemaal                                |               |               |
|                        | gemeentehuis                          |               |               |
|                        | kunstijsbaan                          |               |               |
|                        | observatorium                         |               |               |
|                        | paleis                                |               |               |
|                        | parkeerdak, parkeerdek, parkeergarage |               |               |
|                        | politiebureau                         |               |               |
|                        | radarpost                             |               |               |
|                        | religie                               |               |               |
|                        | schaapskooi                           |               |               |
|                        | school                                |               |               |
|                        | sporthal                              |               |               |
|                        | stadskantoor, hulpsecretarie          |               |               |
|                        | universiteit                          |               |               |
|                        | zwembad                               |               |               |
| fysiekVoorkomen        | ondergronds                           |               | 0..1          |
| hoogte                 | «decimaal getal»                      |               | 0..1          |
| relatieveHoogteligging | «geheel getal [-9<br />9]»                |               | 1-1           |
| status                 | bestaand                              |               | 1-1           |
|                        |                                       |               |               |
| soortnaam              | «tekst»                               |               | 0..n          |
| naam                   | «tekst»                               |               | 0..n          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

n.v.t.

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
| ~~hoogteniveau~~    | ~~Het ~~hoogte~~niveau~~van het object.                                              | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object.                  |

<details class="note">typeGebouw wordt gesplitst in twee attributen: ‘type’ (uiterlijke
verschijningsvorm) en ‘functie’”(gebruik). De attribuutwaarden die verplaatsen
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

*Attribuut TOP10NL:typeGebouw | BRT.Next:type*

| *TOP10NL:waarde*       | *BRT.Next:waarde* |
|------------------------|-------------------|
| kas~~, warenhuis~~ | kas               |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:status | BRT.Next:status*

| *TOP10NL:waarde*                  | *TOP10NL:definitie*                                                                                                                                                      | *BRT.Next:waarde* | *BRT.Next:definitie*                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------------------------------------------------------|
| ~~kerncentrale~~, kernreactor | ~~Centrale die met kernenergie elektriciteit opwekt (kerncentrale) /~~ Installatie voor het splijten of fuseren van atoomkernen, atoomreactor ~~(kernreactor)~~. | kernreactor       | Installatie voor het splijten of fuseren van atoomkernen. |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                                                                                                                                   |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~hoogteklasse~~    | ~~laagbouw~~<br />~~hoogbouw~~                                                                                                                                                                                                                                         |
| ~~gebruiksdoel~~    | ~~bijeenkomstfunctie~~<br />~~celfunctie~~<br />~~gezondheidszorgfunctie~~<br />~~industriefunctie~~<br />~~kantoorfunctie~~<br />~~logiesfunctie~~<br />~~onderwijsfunctie~~<br />~~sportfunctie~~<br />~~winkelfunctie~~<br />~~woonfunctie~~<br />~~overige gebruiksfunctie~~ |

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*  |
|-----------------------------------|-------------------------------------------|
| typeGebouw \| type                | ~~brandweerkazerne~~<br />~~crematorium~~<br />~~elektriciteitscentrale~~<br />~~gemaal~~<br />~~gemeentehuis~~<br />~~kerncentrale, kernreactor~~<br />~~kunstijsbaan~~<br />~~observatorium~~<br />~~paleis~~<br />~~parkeerdak, parkeerdek, parkeergarage~~<br />~~politiebureau~~<br />~~radarpost~~<br />~~religie~~<br />~~schaapskooi~~<br />~~school~~<br />~~sporthal~~<br />~~stadskantoor, hulpsecretarie~~<br />~~universiteit~~<br />~~zwembad~~[^3] |
| typeGebouw \| type                | ~~bezoekerscentrum~~<br />~~brandtoren~~<br />~~dok~~<br />~~fabriek~~<br />~~fort~~<br />~~gevangenis~~<br />~~hotel~~<br />~~huizenblok~~<br />~~kliniek, inrichting, sanatorium~~<br />~~lichttoren~~<br />~~luchtwachttoren~~<br />~~markant gebouw~~<br />~~manege~~<br />~~militair gebouw~~<br />~~museum~~<br />~~peilmeetstation~~<br />~~pompstation~~<br />~~psychiatrisch ziekenhuis, psychiatrisch centrum~~<br />~~postkantoor~~<br />~~radartoren~~<br />~~recreatiecentrum~~<br />~~reddingboothuisje~~<br />~~remise~~<br />~~stationsgebouw~~<br />~~synagoge~~<br />~~tank~~<br />~~tanstation~~<br />~~tol~~<br />~~transformatorstation~~<br />~~veiling~~<br />~~wegrestaurant~~<br />~~werf~~<br />~~windmolen: korenmolen~~<br />~~windmolen: watermolen~~<br />~~windturbine~~<br />~~zendtoren~~<br />~~ziekenhuis~~[^4] |
| fysiekVoorkomen                   | ~~overkluisd~~ |
| status                            | ~~in gebruik~~<br />~~buiten gebruik~~[^5]<br />~~in uitvoering~~ |

<details class="note"> De attribuutwaarden ‘brandweerkazerne’, ‘crematorium’, …, ‘zwembad’
verplaatsen van attribuut typeGebouw\|type naar attribuut functie.
</details>
<details class="note">: typeGebouw ‘tank’, ‘windturbine’, ‘dok’ verplaatsen naar type van object
Inrichtingselement.
</details>
<details class="note">: status ‘in gebruik’ en ‘buiten gebruik’ worden samengevoegd tot status
‘bestaand’.
</details>
Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                                                   | *Verplicht/optioneel*    | *Domein*                                                             |
|--------------------------|-------------------------------------------------------------------------------|--------------------------|----------------------------------------------------------------------|
| **functie**              | **De functie van het gebouw, de functie waarvoor het gebouw gebruikt wordt.** | **optioneel, 0 of meer** | *zie tabel attribuut BRT.Next:functie in Toevoegen attribuutwaarden* |

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:functie*

| *BRT.Next:waarde*                         | *BRT.Next:definitie*                            |
|-------------------------------------------|-------------------------------------------------|
| **brandweerkazerne**                      | *definitie TOP10NL 1.2*                         |
| **crematorium**                           | *definitie TOP10NL 1.2*                         |
| **elektriciteitscentrale**                | *definitie TOP10NL 1.2*                         |
| **gemaal**                                | *definitie TOP10NL 1.2*                         |
| **gemeentehuis**                          | *definitie TOP10NL 1.2*                         |
| **kerncentrale, kernreactor**             | *definitie TOP10NL 1.2*                         |
| **kunstijsbaan**                          | *definitie TOP10NL 1.2*                         |
| **observatorium**                         | *definitie TOP10NL 1.2*                         |
| **paleis**                                | *definitie TOP10NL 1.2*                         |
| **parkeerdak, parkeerdek, parkeergarage** | *definitie TOP10NL 1.2*                         |
| **politiebureau**                         | *definitie TOP10NL 1.2*                         |
| **radarpost**                             | *definitie TOP10NL 1.2*                         |
| **religie**                           | **Gebouw in gebruik voor geloofsuitoefening.**  |
| **schaapskooi**                           | *definitie TOP10NL 1.2*                         |
| **school**                                | *definitie TOP10NL 1.2*                         |
| **sporthal**                              | *definitie TOP10NL 1.2*                         |
| **stadskantoor, hulpsecretarie**          | *definitie TOP10NL 1.2*                         |
| **universiteit**                          | *definitie TOP10NL 1.2*                         |
| **waterwoning**                           | *definitie TOP10NL 1.2*                         |
| **zwembad**                               | *definitie TOP10NL 1.2*                         |


<details class="note">Attribuutwaarden van BRT.Next:functie zijn overgenomen van
TOP10NL:typeGebouw<br />m.u.v. waarde 'religie': deze classificatie is nieuw toegevoegd aan BRT.Next.
</details>

*Attribuut BRT.Next:status*

| *BRT.Next:status* | *BRT.Next:definitie*                                                                                          |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| **bestaand**      | **Situatie waarin het object wordt / kan worden gebruikt voor het doel waarvoor het is gebouwd / aangelegd.** |
