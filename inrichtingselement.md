Inrichtingselement
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Inrichtingselement in
BRT.Next ten opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeInrichtingselement’ wordt hernoemd naar ‘type’.

-   de volgen typen vervallen: 'dukdalf', 'gaswinning', 'golfmeetpaal',
    'havenhoofd', 'helikopterlandingsplatform', 'kilometerraaibord',
    'kilometerraaipaal', 'koedam', 'kogelvanger schietbaan', 'kraan', 'leiding',
    'metrostation', 'oliepompinstallatie', 'radiobaken', 'RD punt',
    'schietbaan', 'seinmast', 'tol', 'verkeersgeleider', 'zichtbaar wrak'.

-   typen ‘geluidswering’, ‘GPS kernnetpunt’, ‘hekwerk’ en ‘strekdam, krib,
    golfbreker’ worden hernoemd naar respectievelijk ‘geluidsscherm’, ‘GPS
    kernnetpunt’, ‘hek’ en ‘strekdam met aangepaste definities.

-   typeLandgebruik ‘aanlegsteiger’ verplaatst van object Terrein naar type
    ‘steiger’ van object Inrichtingselement.

-   de volgende typen worden toegevoegd: 'open loods', 'overkapping', 'bassin',
    'bezinkbak', 'opslagtank', 'windturbine', 'botenhuis'

-   fysiekVoorkomen ‘overkluisd’ vervalt bij attribuut ligging.

-   attribuut ‘hoogteniveau’ wordt hernoemd naar ‘relatieveHoogteligging’,
    definitie wordt en bereik -9 tot 9 wordt aangepast op BGT.

-   attribuut ‘status’ met waarde ‘bestaand’ wordt toegevoegd.

-   attributen ‘breedte’ vervalt.

-   vlakgeometrie wordt toegevoegd.

*Overzicht attributen en waarden/type van object Inrichtingselement in BRT.Next*

| Attribuutnaam          | Waarde of «type»       | Geometrietype | Kardinaliteit |
|------------------------|------------------------|---------------|---------------|
| geometrie              | «punt»                 |               | 1-1           |
|                        | «lijn»                 |               |               |
|                        | «vlak»                 |               |               |
|  type                  | baken                  | punt          | 1-1           |
|                        |                        |               |               |
|                        | bomenrij               | lijn          |               |
|                        | boom                   | punt          |               |
|                        | botenhelling           | punt          |               |
|                        | busstation             | punt          |               |
|                        | calamiteitendoorgang   | lijn          |               |
|                        | gedenkteken, monument  | punt          |               |
|                        | geluidsscherm          | lijn          |               |
|                        | GNSS kernnetpunt       | punt          |               |
|                        | grenspunt              | punt          |               |
|                        | heg, haag              | lijn          |               |
|                        | hek                    | lijn          |               |
|                        | hoogspanningsleiding   | lijn          |               |
|                        | hoogspanningsmast      | punt          |               |
|                        | hunebed                | punt          |               |
|                        | kabelbaan              | lijn          |               |
|                        | kabelbaanmast          | punt          |               |
|                        | kilometerpaal weg      | punt          |               |
|                        | kilometerpaal spoorweg | punt          |               |
|                        | kilometerpaal water    | punt          |               |
|                        | klokkenstoel           | punt          |               |
|                        | kruis                  | punt          |               |
|                        | luchtvaartlicht        | punt          |               |
|                        | markant object         | punt          |               |
|                        | muur                   | lijn          |               |
|                        | open loods             | vlak          |               |
|                        | overkapping            | vlak          |               |
|                        | paal                   | punt          |               |
|                        | paalwerk               | lijn          |               |
|                        | peilschaal             | punt          |               |
|                        | pijler                 | vlak, punt    |               |
|                        | plaatsnaambord         | lijn, punt    |               |
|                        | radiotelescoop         | punt          |               |
|                        | scheepvaartlicht       | punt          |               |
|                        | sluisdeur              | lijn, punt    |               |
|                        | sneltramhalte          | punt          |               |
|                        | steiger                | lijn, vlak    |               |
|                        | stormvloedkering       | lijn          |               |
|                        | strandpaal             | punt          |               |
|                        | strekdam               | lijn          |               |
|                        | stuw                   | lijn, punt    |               |
|                        | treinstation           | punt          |               |
|                        | uitzichtpunt           | punt          |               |
|                        | vlampijp               | punt          |               |
|                        | vliedberg              | punt          |               |
|                        | wegafsluiting          | lijn, punt    |               |
|                        | wegwijzer              | punt          |               |
|                        | windmolentje           | punt          |               |
|                        | zendmast               | punt          |               |
|                        | overig                 | lijn, punt    |               |
|                        | bassin                 | vlak          |               |
|                        | bezinkbak              | vlak          |               |
|                        | opslagtank             | vlak          |               |
|                        | windturbine            | vlak          |               |
|                        | botenhuis              | vlak          |               |
| hoogte                 | «decimaal getal»       |               | 0..1          |
| relatieveHoogteligging | «geheel getal [-9<br />9]» |               | 1-1           |
| status                 | bestaand               |               | 1-1           |
| naam                   | «tekst»                |               | 0..1          |
| soortnaam              | «tekst»                |               | 0..1          |
| nummer                 | «tekst»                |               | 0..1          |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam*        | *BRT.Next:attribuutnaam* |
|--------------------------------|--------------------------|
| type~~Inrichtingselement~~ | **type**                 |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|--------------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het~~ hoogte~~niveau~~van het object. | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note">Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van een geheel
getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
<details>

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

*Attribuut TOP10NL:typeInrichtingselement / BRT.Next:type*

| *TOP10NL:waarde*        | *BRT.Next:waarde*     |
|-------------------------|-----------------------|
| ~~baak~~        | **baken**             |
| ~~kaap~~         | **baken**             |
| ~~GPS~~ kernnetpunt | **GNSS** kernnetpunt  |
| kilometerpaal           | kilometerpaal **weg** |

<details class="note">
TOP10NL-typen ‘baak’ en ‘kaap’ worden samengevoegd tot ‘baken’ in BRT.Next
</details>

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande classificaties wijzigen van naam (waarde) en definitie in BRT.Next

*Attribuut TOP10NL:typeWeg / BRT.Next:type*

| *TOP10NL:waarde*                   | *TOP10NL:definitie*                                                                                                                                                                                                                                                                                                                                                                            | *BRT.Next:waarde*    | *BRT.Next:definitie*                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| geluids~~wering~~              | ~~Constructie ten behoeve van het terugdringen van geluidsoverlast.~~                                                                                                                                                                                                                                                                                                                      | geluids**scherm**    | **Een scheiding bedoeld om geluidshinder in de buitenlucht te verminderen.**                                                                              |
| ~~GPS~~ kernnetpunt            | Punt geschikt voor ~~GPS~~ metingen. (Kan een steen of bout zijn).                                                                                                                                                                                                                                                                                                                         | **GNSS** kernnetpunt | Punt geschikt voor **GNSS** metingen. (Kan een steen of bout zijn).                                                                                       |
| hek~~werk~~                    | ~~Begrenzing van een terrein in de vorm van een afrastering.~~                                                                                                                                                                                                                                                                                                                             | hek                  | **Een hekwerk of schutting, typisch ten behoeve van erfafscheiding.**                                                                                     |
| ~~aanleg~~steiger              | ~~In het water uitstekende brug of pier, breder dan 2 meter, gebruikt om personen en goederen aan~~ wal ~~te brengen.~~                                                                                                                                                                                                                                                                | steiger              | **Vaste (niet drijvende) waterbouwkundige constructie voor het aanleggen van schepen en bedoeld om deze schepen vanaf de** wal **te laden en te lossen.** |
| strekdam~~, krib, golfbreker~~ | ~~Dam in de richting van de loop van de rivier of kanaal, ter beveiliging van de~~ oever~~s of brugpijlers of tot beperking van de rivier tot een bepaalde breedte (strekdam). Golfslagbreker of stroombreker langs de kust en in rivieren, staat loodrecht op de oever/kust (krib). Een uit steenglooiing of stortsteen bestaand object bedoelt voor oeverbescherming (golfbreker).~~ | strekdam             | **Constructie in het water ter verdediging van de kust/**oever.                                                                                           |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-------------------------|----------------------------------------|
| ~~breedte~~         | ~~«decimaal getal»~~               |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeInrichtingselement \| type    | ~~dukdalf~~<br />~~gaswinning~~<br />~~golfmeetpaal~~<br />~~havenhoofd~~<br />~~helikopterlandingsplatform~~<br />~~kilometerraaibord~~<br />~~kilometerraaipaal~~<br />~~koedam~~<br />~~kogelvanger schietbaan~~<br />~~kraan~~<br />~~leiding~~<br />~~metrostation~~<br />~~oliepompinstallatie~~<br />~~radiobaken~~<br />~~RD punt~~<br />~~schietbaan~~<br />~~seinmast~~<br />~~tol~~<br />~~verkeersgeleider~~<br />~~zichtbaar wrak~~ |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                                     | *Verplicht/optioneel* | *Attribuutwaarde* |
|--------------------------|-----------------------------------------------------------------|-----------------------|-------------------|
| **status**               | **De status gekoppeld aan de levenscyclus van een geo-object.** | **verplicht, 1**      | **bestaand**      |

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:geometrie*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **«vlak»**        | Vlakgeometrie        |

*Attribuut BRT.Next:type*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                                                  |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| **open loods**    | Niet verplaatsbaar licht gebouw met een open gevel, bestemd als berg- of werkplaats of als tijdelijk onderdak voor andere doeleinden. |
| **overkapping**   | Een afzonderlijk staande overdekking rustend op kolommen.                                                                             |
| **bassin**        | **Waterbak zoals een zwembad of een dok.**                                                                                            |
| **bezinkbak**     | **Een gesloten reservoir waarin het afvalwater tijdelijk wordt opgevangen met een slibreinigende voorziening.**                       |
| **opslagtank**    | Opslagfaciliteit voor vloeistoffen, gassen of energie.                                                                                |
| **windturbine**   | Turbine waarin winddruk omgezet wordt in mechanische energie.                                                                         |
| **botenhuis**     | Gebouw boven water voor de opslag van boten.                                                                                          |

*Attribuut BRT.Next:status*

| *BRT.Next:status* | *BRT.Next:definitie*                                                                                          |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| **bestaand**      | **Situatie waarin het object wordt / kan worden gebruikt voor het doel waarvoor het is gebouwd / aangelegd.** |
