Terrein
=======

Dit hoofdstuk beschrijft de wijzigingen voor het object Terrein in BRT.Next ten
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
| type~~Landgebruik~~ | **type**                 |
| ~~fysiekVoorkomen~~ | **ligging**              |
| ~~voorkomen~~       | **type**                 |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                              | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|--------------------------------------------------|--------------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het~~ hoogte~~niveau~~ van het object. | **relatieveHoogteLigging**[^1] | **Aanduiding voor de relatieve** hoogte van het object. |

[^1]: Het domein van hoogteniveau/relatieveHoogteligging wijzigt van geheel
getal Kleiner of gelijk aan 0 naar geheel getal tussen -9 en 9.

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

*Attribuut TOP10NL:fysiekVoorkomen \| BRT.Next:ligging*

| *TOP10NL:waarde*              | *BRT.Next:waarde* |
|-------------------------------|-------------------|
| op ~~vast deel van~~ brug | op brug           |

### Definitie

*n.v.t.*

*Attribuut TOP10NL:typeWeg / BRT.Next:type*

| *TOP10NL\|BRT.Next:waarde* | *TOP10NL:definitie*                                                                                                                            | *BRT.Next:definitie*                                                                                                              |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| braakliggend               | ~~Een stuk grond dat geen functie vervult of niet wordt onderhouden, met uitzondering van landbouwgrond.~~                                 | **Terreindeel waar geen verharding of aaneengesloten vegetatie aanwezig is, niet zijnde zand. Braakliggend valt hier wel onder.** |
| duin                       | ~~Terrein met grondsoort~~ zand ~~, langs de kust als natuurlijke kustverdediging, eventueel begroeid met helmgras of lage struiken.~~ | **Verhoging of heuvel van** zand **of fijne losse aarde en verpulverd gesteente opgeworpen door wind of door stromend water.**    |
| heide                      | Terrein, overwegend begroeid met heidevegetatie ~~en wilde grassoorten.~~                                                                  | Terrein**deel** overwegend begroeid met heide **en heideachtige** vegetatie**s**.                                                 |
| zand                       | Terrein, ~~grondsoort~~ zand, ~~van nature zonder enige begroeiing.~~                                                                  | Terrein**deel dat grotendeels bedekt is met** zand.                                                                               |

### Naam+definitie

Onderstaande classificaties wijzigen van naam (waarde) en definitie in BRT.Next

*Attribuut TOP10NL:typeWeg / BRT.Next:type*

| *TOP10NL:waarde*                    | *TOP10NL:definitie*                                                                                                                                                                              | *BRT.Next:waarde*      | *BRT.Next:definitie*                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ~~akker~~land                   | Terrein ~~waar landbouwproducten worden verbouwd.~~                                                                                                                                          | **bouw**land           | Terrein**deel in gebruik als akker, met gewassen die in een teelt roulatieschema zijn opgenomen. Kan tijdelijk zonder gewas zijn of braak liggen.**                                                                               |
| boom~~kwekerij~~                | ~~Terrein, overwegend~~ in gebruik ~~t.b.v.~~ het ~~op~~kweken van bomen ~~(inclusief coniferen en sparren) en struiken, waarbij de hoogte van de aanplant niet van belang is.~~ | boom**teelt**          | **Grond** in gebruik **voor** het kweken van **jonge siergewassen,** bomen **enz. ten behoeve van een later gebruik elders.**                                                                                                     |
| fruit~~kwekerij~~               | Terrein met ~~laagstammige~~ fruitbomen ~~en struiken waarvan de vruchten worden geoogst (zoals: rozenbottels, bessen, frambozen, druiven, etc.).~~                                      | fruit**teelt**         | Terrein**deel begroeid** met fruitbomen **in de vorm van hoogstam en laagstamboomgaard, druiven of kleinfruit.**                                                                                                                  |
| ~~bos:~~ gemengd bos            | ~~Oppervlak~~ begroeid met een dusdanige aantal naald- en loofbomen dat ~~de kruinen~~ een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.            | gemengd bos            | **Terreindeel** begroeid met een dusdanige aantal naald- en loofbomen dat **deze** een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                                                         |
| grasland                            | Terrein, ~~overwegend begroeid~~ met een ~~grasachtige~~ vegetatie.                                                                                                                      | grasland **agrarisch** | Terrein**deel** met een vegetatie **bestaande uit grassen en of grasachtigen, en met de in graslanden voorkomende kruiden, zijnde cultuurgrasland dat in gebruik is voor de veeteelt, bijvoorbeeld als weiland of als hooiland.** |
| grasland                            | Terrein, ~~overwegend begroeid~~ met een ~~grasachtige~~ vegetatie.                                                                                                                      | grasland **overig**    | Terrein**deel** met een vegetatie **bestaande uit grassen en of grasachtigen, en met de in graslanden voorkomende kruiden, dat niet in gebruik is voor agrarische doeleinden.**                                                   |
| ~~bos:~~ griend                 | ~~In of aan het water gelegen~~ terrein~~, ~~begroei~~d met laagafgeknot wilgenhout t.b.v. de productie van rijshout.~~                                                              | griend **en hakhout**  | Terrein**deel met opgaande** begroei**ing van loofbomen, in een dicht groeiverband, en die periodiek wordt afgezet.**                                                                                                             |
| ~~bos:~~ loofbos                | ~~Oppervlak~~ begroeid met een dusdanige aantal loofbomen dat de kruinen een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                              | loofbos                | **Terreindeel** begroeid met een dusdanige aantal loofbomen dat deze een min of meer gesloten geheel vormen of, na volgroeiing van de bomen, zullen vormen.                                                                       |
| ~~aanleg~~steiger               | ~~In het water uitstekende brug of pier, breder dan 2 meter, gebruikt om personen en goederen aan~~ wal ~~te brengen.~~                                                                  | steiger                | **Vaste (niet drijvende) waterbouwkundige constructie voor het aanleggen van schepen en bedoeld om deze schepen vanaf de** wal **te laden en te lossen.**                                                                         |
| ~~overig~~                      | ~~De waarde van het objectkenmerk is bekend, maar anders dan de genoemde waarden. Een niet nader omschreven gebruiksbestemming.~~                                                            | **erf**                | **Terreindeel dat bij een pand of overig bouwwerk hoort, dat niet nader wordt ingewonnen en dat bestaat uit een mengvorm van begroeiing, verharding, en/of water.**                                                               |
| met riet[^2]                        | Aanduiding dat er riet op het terrein voorkomt of dat het drassig/moerassig is.                                                                                                                  | riet**land**           |                                                                                                                                                                                                                                   |
| ~~dras, ~~moeras~~sig~~[^3] | ~~Aanduiding dat er riet op het~~ terrein ~~voorkomt of dat het drassig/~~moeras~~sig is.~~                                                                                          | moeras                 | Terrein**deel met** moeras**vegetatie in stilstaand water van geringe diepte zonder merkbare toe- of afvloeiing.**                                                                                                                |

[^2]: ‘met riet’ van TOP10NL:voorkomen wordt opgenomen als ‘rietland’ van
BRT.Next:type

[^3]: ‘dras, moerassig’ van TOP10NL:voorkomen wordt opgenomen als ‘moeras’ van
BRT.Next:type

*Attribuut TOP10NL:status / BRT.Next:status*

| *TOP10NL:waarde* | *TOP10NL:definitie*                      | *BRT.Next:waarde* | *BRT.Next:definitie* |
|------------------|------------------------------------------|-------------------|----------------------|
| in uitvoering    | De staat waarin het object zich bevindt. | **bestaand**      |                      |
| in gebruik       |                                          | **bestaand**      |                      |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-------------------------|----------------------------------------|
| ~~naam~~            | ~~«tekst»~~                        |
| ~~bebouwd gebied~~  | ~~ja~~; ~~nee~~                |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL/BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                              |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------|
| typeLandgebruik \| type          | ~~dodenakker~~; ~~dodenakker met bos~~; ~~boomgaard~~; ~~populieren~~; ~~spoorbaanlichaam~~[^4] |

[^4]: spoorbaanlichaam wordt opgenomen als type spoorbaan bij Wegdeel.

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie* | *Verplicht/optioneel* | *Domein*              |
|--------------------------|-------------|-----------------------|-----------------------|
| herkomst                 |             | Optioneel [0 of meer] | BAG, BGT, BRK, overig |

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:type*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                                                                                                                        |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **houtwal**       | **Terreindeel zijnde een afscheiding met beperkte breedte en beplant met bomen of struiken.**                                                                                                               |
| **kwelder**       | **Buitendijks gelegen aangeslibd land van een wad, dat bij gewone vloed niet meer onder loopt.**                                                                                                            |
| **struiken**      | **Terreindeel bedekt met niet-gecultiveerde (natuurlijke), lage, houtachtige, overblijvende planten gekenmerkt door verschillende vertakkingen dicht bij de wortel en afwezigheid van opvallende stammen.** |
