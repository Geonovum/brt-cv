# Terrein

Dit hoofdstuk beschrijft de wijzigingen voor het object Terrein in BRT.Next ten
opzichte van de huidige versie TOP10NL.

## Overzicht

*Overzicht attributen en waarden/type van object Terrein in BRT.Next*

| Attribuutnaam          | Waarde of «type»             | Geometrietype | Kardinaliteit |
|------------------------|------------------------------|---------------|---------------|
| geometrie              | «vlak»                       |               | 1-1           |
| typeTerrein            | akkerland                    | vlak          | 1-1           |
|                        | basaltblokken, steenglooiing | vlak          |               |
|                        | boomgaard                    | vlak          |               |
|                        | boomkwekerij                 | vlak          |               |
|                        | duin                         | vlak          |               |
|                        | fruitkwekerij                | vlak          |               |
|                        | gemengd bos                  | vlak          |               |
|                        | grasland agrarisch           | vlak          |               |
|                        | grasland overig              | vlak          |               |
|                        | griend en hakhout            | vlak          |               |
|                        | heide                        | vlak          |               |
|                        | houtwal                      | vlak          |               |
|                        | kwelder                      | vlak          |               |
|                        | loofbos                      | vlak          |               |
|                        | naaldbos                     | vlak          |               |
|                        | struiken                     | vlak          |               |
|                        | zand                         | vlak          |               |
|                        | overig                       | vlak          |               |
|                        | erf                          | vlak          |               |
|                        | rietland                     | vlak          |               |
|                        | moeras                       | vlak          |               |
| ligging                | in tunnel                    |               | 0..1          |
|                        | op brug                      |               |               |
| relatieveHoogteligging | «geheel getal [-9; 9]»       |               | 1-1           |
| brugnaam               | «tekst»                      |               | 0..1          |

## Wijzigen attributen

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| type~~Landgebruik~~ | type**Terrein**          |
| ~~fysiekVoorkomen~~ | **ligging**              |

### Definitie

*Geen.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                              | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|--------------------------------------------------|----------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het~~ hoogte~~niveau~~ van het object. | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note">Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van
een geheel getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details>

## Wijzigen attribuutwaarden

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

*Attribuut TOP10NL:fysiekVoorkomen \| BRT.Next:ligging*

| *TOP10NL:waarde*              | *BRT.Next:waarde* |
|-------------------------------|-------------------|
| op ~~vast deel van~~ brug | op brug           |

### Definitie

Onderstaande attribuutwaarden wijzigen van definitie in BRT.Next. De naam wordt
niet aangepast.

*Attribuut TOP10NL:typeLandgebruik \| BRT.Next:typeTerrein*

| *TOP10NL\|BRT.Next:waarde* | *TOP10NL:definitie*                                                                                                                                                          | *BRT.Next:definitie*                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| akkerland                  | Terrein ~~waar landbouwproducten worden verbouwd.~~                                                                                                                      | Terrein**deel in gebruik als akker, met gewassen die in een teelt roulatieschema zijn opgenomen. Kan tijdelijk zonder gewas zijn of braak liggen.** |
| boomgaard                  | Terrein met hoogstam~~mige ~~fruitbomen.                                                                                                                                 | Terrein **begroeid** met hoogstamfruitbomen.                                                                                                        |
| duin                       | ~~Terrein met grondsoort~~ zand ~~, langs de kust als natuurlijke kustverdediging, eventueel begroeid met helmgras of lage struiken.~~                               | **Verhoging of heuvel van** zand **of fijne losse aarde en verpulverd gesteente opgeworpen door wind of door stromend water.**                      |
| fruitkwekerij              | Terrein met laagstam~~mige ~~fruitbomen ~~en struiken waarvan de vruchten worden geoogst (zoals: rozenbottels,~~ bessen~~,~~ frambozen ~~, druiven, etc.)~~. | Terrein **begroeid** met laagstamfruitbomen, **druivenstokken of begroeid met heesters voor zachtfruit zoals** bessen **of** frambozen.             |
| heide                      | Terrein, overwegend begroeid met heidevegetatie ~~en wilde grassoorten.~~                                                                                                | Terrein**deel** overwegend begroeid met heide **en heideachtige** vegetatie**s**.                                                                   |
| zand                       | Terrein, ~~grondsoort~~ zand, ~~van nature zonder enige begroeiing.~~                                                                                                | Terrein**deel dat grotendeels bedekt is met** zand.                                                                                                 |

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeLandgebruik \| BRT.Next:typeTerrein*

| *TOP10NL:waarde*         | *TOP10NL:definitie*                                                                                                                                                                   | *BRT.Next:waarde*      | *BRT.Next:definitie*                                                                                                                                                                                                              |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~bos:~~ gemengd bos | ~~Oppervlak~~ begroeid met een dusdanige aantal naald- en loofbomen dat ~~de kruinen~~ een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen. | gemengd bos            | **Terreindeel** begroeid met een dusdanige aantal naald- en loofbomen dat **deze** een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                                                         |
| grasland                 | Terrein, ~~overwegend begroeid~~ met een ~~grasachtige~~ vegetatie.                                                                                                           | grasland **agrarisch** | Terrein**deel** met een vegetatie **bestaande uit grassen en of grasachtigen, en met de in graslanden voorkomende kruiden, zijnde cultuurgrasland dat in gebruik is voor de veeteelt, bijvoorbeeld als weiland of als hooiland.** |
| grasland                 | Terrein, ~~overwegend begroeid~~ met een ~~grasachtige~~ vegetatie.                                                                                                           | grasland **overig**    | Terrein**deel** met een vegetatie **bestaande uit grassen en of grasachtigen, en met de in graslanden voorkomende kruiden, dat niet in gebruik is voor agrarische doeleinden.**                                                   |
| ~~bos:~~ griend      | ~~In of aan het water gelegen~~ terrein~~, ~~begroei~~d met laagafgeknot wilgenhout t.b.v. de productie van rijshout.~~                                                   | griend **en hakhout**  | Terrein**deel met opgaande** begroei**ing van loofbomen, in een dicht groeiverband, en die periodiek wordt afgezet.**                                                                                                             |
| ~~bos:~~ loofbos     | ~~Oppervlak~~ begroeid met een dusdanige aantal loofbomen dat de kruinen een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                   | loofbos                | **Terreindeel** begroeid met een dusdanige aantal loofbomen dat deze een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                                                                       |

## Vervallen attributen

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*  |
|-------------------------|-------------------------------------------|
| ~~voorkomen~~       | ~~met riet~~; ~~dras, moerassig~~ |
| ~~naam~~            | ~~«tekst»~~                           |

<details class="note">voorkomen ‘met riet’ en ‘dras, moerassig’ worden verplaatst naar
respectievelijk typen ‘rietland’ en ‘moeras’. </details>

## Vervallen attribuutwaarden

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL/BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeLandgebruik \| typeTerrein   | ~~aanlegsteiger~~; ~~bebouwd gebied~~; ~~braakliggend~~; ~~dodenakker~~; ~~dodenakker met bos~~; ~~populieren~~; ~~spoorbaanlichaam~~ |
| fysiekVoorkomen \| ligging       | ~~overkluisd~~, ~~op beweegbaar deel van brug~~                                                                                                           |

<details class="note">type ‘aanlegsteiger’ verplaatst van object Terrein naar type
‘steiger’ van object Inrichtingselement. </details>

<details class="note">type ‘spoorbaanlichaam’ verplaatst van Terrein naar type
‘spoorbaan’ van object Spoor. </details>

## Toevoegen attributen

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*              | *Verplicht/optioneel* | *Attribuutwaarde* |
|--------------------------|--------------------------|-----------------------|-------------------|
| **brugnaam**             | **De naam van de brug.** | **Optioneel, 0..1**   | **«tekst»**       |

## Toevoegen attribuutwaarden

Onderstaande attribuutwaarden (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:typeTerrein*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                                                                                                                        |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **houtwal**       | **Terreindeel zijnde een afscheiding met beperkte breedte en beplant met bomen of struiken.**                                                                                                               |
| **kwelder**       | **Buitendijks gelegen aangeslibd land van een wad, dat bij gewone vloed niet meer onder loopt.**                                                                                                            |
| **struiken**      | **Terreindeel bedekt met niet-gecultiveerde (natuurlijke), lage, houtachtige, overblijvende planten gekenmerkt door verschillende vertakkingen dicht bij de wortel en afwezigheid van opvallende stammen.** |
| **erf**           | **Terreindeel dat bij een pand of overig bouwwerk hoort, en dat bestaat uit een mengvorm van begroeiing, verharding, en/of water.**                                                                         |
| **rietland**      | **Terreindeel overwegend begroeid met rietvegetatie.**                                                                                                                                                      |
| **moeras**        | **Terreindeel met moerasvegetatie in stilstaand water van geringe diepte zonder merkbare toe- of afvloeiing.**                                                                                              |
