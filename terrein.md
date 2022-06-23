Terrein
=======

Dit hoofdstuk beschrijft de wijzigingen voor het object Terrein in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeLandgebruik’ wordt hernoemd naar ‘type’, ‘fysiekVoorkomen’
    naar ‘ligging’.

-   attribuut ‘hoogteniveau’ wordt hernoemd naar ‘relatieveHoogteligging’,
    definitie en attribuutwaarden worden aangepast op BGT.

-   typen ‘akkerland’, ‘boomkwekerij’, ‘fruitkwekerij’, ‘bos: gemengd bos’,
    ‘bos: griend’, ‘bos: loofbos’ en ‘bos: naaldbos’, worden hernoemd naar
    respectievelijk ‘bouwland’, ‘boomteelt’, ‘fruitteelt’, ‘gemengd bos’,
    ‘griend en hakhout’, ‘loofbos’ en ‘naaldbos’.

-   voorkomen ‘met riet’ en ‘dras, moerassig’ worden verplaatst naar
    respectievelijk typen ‘rietland’ en ‘moeras’.

-   type ‘grasland’ wordt opgesplitst in typen ‘grasland agrarisch’ en ‘grasland
    overig’.

-   de definities van typen ‘braakliggend’, ‘duin’, ‘heide’ en ‘zand’ zijn
    aangepast naar de BGT.

-   typen ’ houtwal’, ‘kwelder’, ‘struiken’ en ‘erf’ worden toegevoegd.

-   fysiekVoorkomen ‘op vast deel van brug’ wordt hernoemd naar ligging ‘op
    brug’.

-   attributen ‘voorkomen’ en ‘naam’ vervallen.

-   type ‘spoorbaanlichaam’ verplaatst van object Terrein naar type ‘spoorbaan’
    van object Wegdeel.

-   type ‘aanlegsteiger’ verplaatst van object Terrein naar type ‘steiger’ van
    object Inrichtingselement.

-   typen ‘dodenakker’, ‘dodenakker met bos’, ‘boomgaard’, ‘populieren’ en
    ‘bebouwd gebied’ vervallen.

-   fysiekVoorkomen ‘overkluisd’ en ‘op beweegbaar deel van brug’ vervallen bij
    ligging.

-   puntgeometrie als attribuutwaarde van attribuut geometrie vervalt.

*Overzicht attributen en waarden/type van object Terrein in BRT.Next*

| Attribuutnaam          | Waarde of «type»             | Geometrietype | Kardinaliteit |
|------------------------|------------------------------|---------------|---------------|
| geometrie              | «vlak»                       |               | 1-1           |
| type                   | basaltblokken, steenglooiing | vlak          | 1-1           |
|                        | bouwland                     | vlak          |               |
|                        | boomteelt                    | vlak          |               |
|                        | braakliggend                 | vlak          |               |
|                        | duin                         | vlak          |               |
|                        | fruitteelt                   | vlak          |               |
|                        | gemengd bos                  | vlak          |               |
|                        | grasland agrarisch           | vlak          |               |
|                        | grasland overig              | vlak          |               |
|                        | griend en hakhout            | vlak          |               |
|                        | heide                        | vlak          |               |
|                        | houtwal                      | vlak          |               |
|                        | kwelder                      | vlak          |               |
|                        | loofbos                      | vlak          |               |
|                        | naaldbos                     | vlak          |               |
|                        | struiken                     |               |               |
|                        | zand                         | vlak          |               |
|                        | overig                       | vlak          |               |
|                        | erf                          | vlak          |               |
|                        | rietland                     | vlak          |               |
|                        | moeras                       | vlak          |               |
| ligging                | in tunnel                    |               | 0..1          |
|                        | op brug                      |               |               |
| relatieveHoogteligging | «geheel getal [-9;9]»       |               | 1-1           |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Landgebruik~~ | **type**                 |
| ~~fysiekVoorkomen~~ | **ligging**              |
| ~~voorkomen~~       | **type**                 |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                              | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|--------------------------------------------------|--------------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het~~ hoogte~~niveau~~ van het object. | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note"> Het bereik van hoogteniveau|relatieveHoogteligging wijzigt van een geheel
getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details>

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

*Attribuut TOP10NL:fysiekVoorkomen | BRT.Next:ligging*

| *TOP10NL:waarde*              | *BRT.Next:waarde* |
|-------------------------------|-------------------|
| op ~~vast deel van~~ brug | op brug           |

### Definitie

*Attribuut TOP10NL:typeLandgebruik | BRT.Next:type*

| *TOP10NL\|BRT.Next:waarde* | *TOP10NL:definitie*                                                                                                                            | *BRT.Next:definitie*                                                                                                              |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| braakliggend               | ~~Een stuk grond dat geen functie vervult of niet wordt onderhouden, met uitzondering van landbouwgrond.~~                                 | **Terreindeel waar geen verharding of aaneengesloten vegetatie aanwezig is, niet zijnde zand. Braakliggend valt hier wel onder.** |
| duin                       | ~~Terrein met grondsoort~~ zand ~~, langs de kust als natuurlijke kustverdediging, eventueel begroeid met helmgras of lage struiken.~~ | **Verhoging of heuvel van** zand **of fijne losse aarde en verpulverd gesteente opgeworpen door wind of door stromend water.**    |
| heide                      | Terrein, overwegend begroeid met heidevegetatie ~~en wilde grassoorten.~~                                                                  | Terrein**deel** overwegend begroeid met heide **en heideachtige** vegetatie**s**.                                                 |
| zand                       | Terrein, ~~grondsoort~~ zand, ~~van nature zonder enige begroeiing.~~                                                                  | Terrein**deel dat grotendeels bedekt is met** zand.                                                                               |

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeWeg | BRT.Next:type*

| *TOP10NL:waarde*         | *TOP10NL:definitie*                                                                                                                                                                              | *BRT.Next:waarde*      | *BRT.Next:definitie*                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~akker~~land        | Terrein ~~waar landbouwproducten worden verbouwd.~~                                                                                                                                          | **bouw**land           | Terrein**deel in gebruik als akker, met gewassen die in een teelt roulatieschema zijn opgenomen. Kan tijdelijk zonder gewas zijn of braak liggen.**                                                                               |
| boom~~kwekerij~~     | ~~Terrein, overwegend~~ in gebruik ~~t.b.v.~~ het ~~op~~kweken van bomen ~~(inclusief coniferen en sparren) en struiken, waarbij de hoogte van de aanplant niet van belang is.~~ | boom**teelt**          | **Grond** in gebruik **voor** het kweken van **jonge siergewassen,** bomen **enz. ten behoeve van een later gebruik elders.**                                                                                                     |
| fruit~~kwekerij~~    | Terrein met ~~laagstammige~~ fruitbomen ~~en struiken waarvan de vruchten worden geoogst (zoals: rozenbottels, bessen, frambozen, druiven, etc.).~~                                      | fruit**teelt**         | Terrein**deel begroeid** met fruitbomen **in de vorm van hoogstam en laagstamboomgaard, druiven of kleinfruit.**                                                                                                                  |
| ~~bos:~~ gemengd bos | ~~Oppervlak~~ begroeid met een dusdanige aantal naald- en loofbomen dat ~~de kruinen~~ een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.            | gemengd bos            | **Terreindeel** begroeid met een dusdanige aantal naald- en loofbomen dat **deze** een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                                                         |
| grasland                 | Terrein, ~~overwegend begroeid~~ met een ~~grasachtige~~ vegetatie.                                                                                                                      | grasland **agrarisch** | Terrein**deel** met een vegetatie **bestaande uit grassen en of grasachtigen, en met de in graslanden voorkomende kruiden, zijnde cultuurgrasland dat in gebruik is voor de veeteelt, bijvoorbeeld als weiland of als hooiland.** |
| grasland                 | Terrein, ~~overwegend begroeid~~ met een ~~grasachtige~~ vegetatie.                                                                                                                      | grasland **overig**    | Terrein**deel** met een vegetatie **bestaande uit grassen en of grasachtigen, en met de in graslanden voorkomende kruiden, dat niet in gebruik is voor agrarische doeleinden.**                                                   |
| ~~bos:~~ griend      | ~~In of aan het water gelegen~~ terrein~~, ~~ begroei~~d met laagafgeknot wilgenhout t.b.v. de productie van rijshout.~~                                                              | griend **en hakhout**  | Terrein**deel met opgaande** begroei**ing van loofbomen, in een dicht groeiverband, en die periodiek wordt afgezet.**                                                                                                             |
| ~~bos:~~ loofbos     | ~~Oppervlak~~ begroeid met een dusdanige aantal loofbomen dat de kruinen een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                              | loofbos                | **Terreindeel** begroeid met een dusdanige aantal loofbomen dat deze een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                                                                       |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*     |
|-------------------------|----------------------------------------------|
| ~~voorkomen~~       | ~~met riet~~<br />~~dras, moerassig~~ |
| ~~naam~~            | ~~«tekst»~~                              |

<details class="note"> 
voorkomen ‘met riet’ en ‘dras, moerassig’ worden verplaatst naar
respectievelijk typen ‘rietland’ en ‘moeras’.
</details>

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL/BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                               |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeLandgebruik | type          | ~~aanlegsteiger~~[^3]<br />~~bebouwd gebied~~<br />~~dodenakker~~<br />~~dodenakker met bos~~<br />~~boomgaard~~<br />~~populieren~~<br />~~spoorbaanlichaam~~[^4] |
| fysiekVoorkomen | ligging       | ~~overkluisd~~, ~~op beweegbaar deel van brug~~                                                                                                                |

[^3]: type ‘aanlegsteiger’ verplaatst van object Terrein naar type ‘steiger’ van
object Inrichtingselement

[^4]: type ‘spoorbaanlichaam’ verplaatst van Terrein naar type ‘spoorbaan’ van
object Wegdeel.

Toevoegen attributen
--------------------

n.v.t.

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:type*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                                                                                                                        |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **houtwal**       | **Terreindeel zijnde een afscheiding met beperkte breedte en beplant met bomen of struiken.**                                                                                                               |
| **kwelder**       | **Buitendijks gelegen aangeslibd land van een wad, dat bij gewone vloed niet meer onder loopt.**                                                                                                            |
| **struiken**      | **Terreindeel bedekt met niet-gecultiveerde (natuurlijke), lage, houtachtige, overblijvende planten gekenmerkt door verschillende vertakkingen dicht bij de wortel en afwezigheid van opvallende stammen.** |
| **erf**           | **Terreindeel dat bij een pand of overig bouwwerk hoort, dat niet nader wordt ingewonnen en dat bestaat uit een mengvorm van begroeiing, verharding, en/of water.**                                         |
| **rietland**      | **Terreindeel overwegend begroeid met rietvegetatie.**                                                                                                                                                      |
| **moeras**        | **Terreindeel met moerasvegetatie in stilstaand water van geringe diepte zonder merkbare toe- of afvloeiing.**                                                                                              |
|                   |                                                                                                                                                                                                             |
