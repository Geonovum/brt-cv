# Inrichtingselement

Dit hoofdstuk beschrijft de wijzigingen voor het object Inrichtingselement in
BRT.Next ten opzichte van de huidige versie TOP10NL.

## Overzicht

*Overzicht attributen en waarden/type van object Inrichtingselement in BRT.Next*

| Attribuutnaam           | Waarde of «type»       | Geometrietype | Kardinaliteit |
|-------------------------|------------------------|---------------|---------------|
| geometrie               | «punt»                 |               | 1-1           |
|                         | «lijn»                 |               |               |
|                         | «vlak»                 |               |               |
|  typeInrichtingselement | baken                  | punt          | 1-1           |
|                         | bomenrij               | lijn          |               |
|                         | boom                   | punt          |               |
|                         | botenhelling           | punt          |               |
|                         | calamiteitendoorgang   | lijn          |               |
|                         | dukdalf                | punt          |               |
|                         | gedenkteken, monument  | punt          |               |
|                         | geluidsscherm          | lijn          |               |
|                         | GNSS kernnetpunt       | punt          |               |
|                         | grenspunt              | punt          |               |
|                         | heg, haag              | lijn          |               |
|                         | hek                    | lijn          |               |
|                         | hoogspanningsleiding   | lijn          |               |
|                         | hoogspanningsmast      | punt          |               |
|                         | hunebed                | punt          |               |
|                         | kabelbaan              | lijn          |               |
|                         | kabelbaanmast          | punt          |               |
|                         | kilometerpaal weg      | punt          |               |
|                         | kilometerpaal spoor    | punt          |               |
|                         | kilometerpaal water    | punt          |               |
|                         | klokkenstoel           | punt          |               |
|                         | kruis                  | punt          |               |
|                         | luchtvaartlicht        | punt          |               |
|                         | markant object         | punt          |               |
|                         | muur                   | lijn          |               |
|                         | paal                   | punt          |               |
|                         | paalwerk               | lijn          |               |
|                         | peilschaal             | punt          |               |
|                         | pijler                 | vlak, punt    |               |
|                         | plaatsnaambord         | lijn, punt    |               |
|                         | radiotelescoop         | punt          |               |
|                         | scheepvaartlicht       | punt          |               |
|                         | sluisdeur              | lijn, punt    |               |
|                         | steiger                | lijn, vlak    |               |
|                         | stormvloedkering       | lijn          |               |
|                         | strandpaal             | punt          |               |
|                         | strekdam               | lijn          |               |
|                         | stuw                   | lijn, punt    |               |
|                         | uitzichtpunt           | punt          |               |
|                         | vlampijp               | punt          |               |
|                         | wegafsluiting          | lijn, punt    |               |
|                         | wegwijzer              | punt          |               |
|                         | windmolentje           | punt          |               |
|                         | zendmast               | punt          |               |
|                         | overig                 | lijn, punt    |               |
|                         | dok                    | vlak          |               |
|                         | zwembad                | vlak          |               |
|                         | bezinkbak              | vlak          |               |
| hoogte                  | «decimaal getal»       |               | 0..1          |
| relatieveHoogteligging  | «geheel getal [-9; 9]» |               | 1-1           |
| naam                    | «tekst»                |               | 0..1          |
| soortnaam               | «tekst»                |               | 0..1          |
| nummer                  | «tekst»                |               | 0..1          |

## Wijzigen attributen

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

*Geen.*

### Definitie

*Geen.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|----------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het~~ hoogte~~niveau~~van het object. | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note"> Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van
een geheel getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9..
</details>

## Wijzigen attribuutwaarden

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

*Attribuut TOP10NL:typeInrichtingselement \| BRT.Next:typeInrichtingselement*

| *TOP10NL:waarde*               | *BRT.Next:waarde*     |
|--------------------------------|-----------------------|
| ~~baak~~                   | **baken**             |
| ~~kaap~~                   | **baken**             |
| kilometerpaal                  | kilometerpaal **weg** |
| kilometerpaal spoor~~weg~~ | kilometerpaal spoor   |

<details class="note"> TOP10NL-typen ‘baak’ en ‘kaap’ worden samengevoegd tot ‘baken’ in
BRT.Next --END NOTE--

### Definitie

*Geen.*

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in
BRT.Next

*Attribuut TOP10NL:typeInrichtingselement \| BRT.Next:typeInrichtingselement*

| *TOP10NL:waarde*                   | *TOP10NL:definitie*                                                                                                                                                                                                                                                                                                                                                                            | *BRT.Next:waarde*    | *BRT.Next:definitie*                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| geluids~~wering~~              | ~~Constructie ten behoeve van het terugdringen van geluidsoverlast.~~                                                                                                                                                                                                                                                                                                                      | geluids**scherm**    | **Een scheiding bedoeld om geluidshinder in de buitenlucht te verminderen.**                                                                              |
| ~~GPS~~ kernnetpunt            | Punt geschikt voor ~~GPS~~ metingen. (Kan een steen of bout zijn).                                                                                                                                                                                                                                                                                                                         | **GNSS** kernnetpunt | Punt geschikt voor **GNSS** metingen. (Kan een steen of bout zijn).                                                                                       |
| hek~~werk~~                    | ~~Begrenzing van een terrein in de vorm van een afrastering.~~                                                                                                                                                                                                                                                                                                                             | hek                  | **Een hekwerk of schutting, typisch ten behoeve van erfafscheiding.**                                                                                     |
| ~~aanleg~~steiger              | ~~In het water uitstekende brug of pier, smaller dan 2 meter, gebruikt om personen en goederen aan~~ wal ~~te brengen.~~                                                                                                                                                                                                                                                               | steiger              | **Vaste (niet drijvende) waterbouwkundige constructie voor het aanleggen van schepen en bedoeld om deze schepen vanaf de** wal **te laden en te lossen.** |
| strekdam~~, krib, golfbreker~~ | ~~Dam in de richting van de loop van de rivier of kanaal, ter beveiliging van de~~ oever~~s of brugpijlers of tot beperking van de rivier tot een bepaalde breedte (strekdam). Golfslagbreker of stroombreker langs de kust en in rivieren, staat loodrecht op de oever/kust (krib). Een uit steenglooiing of stortsteen bestaand object bedoelt voor oeverbescherming (golfbreker).~~ | strekdam             | \*\*Constructie in het water ter verdediging van de kust/\*\*oever.                                                                                       |

## Vervallen attributen

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|------------------------------------------|
| ~~breedte~~         | ~~«decimaal getal»~~                 |

## Vervallen attribuutwaarden

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeInrichtingselement            | ~~busstation~~; ~~gaswinning~~; ~~golfmeetpaal~~; ~~havenhoofd~~; ~~helikopterlandingsplatform~~; ~~kilometerraaibord~~; ~~kilometerraaipaal~~; ~~koedam~~; ~~kogelvanger schietbaan~~; ~~kraan~~; ~~metrostation~~; ~~leiding~~; ~~oliepompinstallatie~~; ~~radiobaken~~; ~~RD punt~~; ~~schietbaan~~; ~~seinmast~~; ~~sneltramhalte~~; ~~treinstation~~; ~~tol~~; ~~verkeersgeleider~~; ~~vliedberg~~; ~~zichtbaar wrak~~ |

\--START NOTE—typen ‘gaswinning’, ‘helikopterlandingsplatform’,
‘oliepompinstallatie’, ‘vliedberg’, ‘busstation’, ‘metrostation’,
‘sneltramhalte’, ‘treinstation’, ‘tol’ verplaatsen naar objecttype Functioneel
gebied. --END NOTE—

\--START NOTE—typen ‘kilometerraaibord’ en ‘kilometerraaipaal’ worden hernoemd
naar ‘kilometerpaal water’. --END NOTE—

## Toevoegen attributen

*Geen.*

## Toevoegen attribuutwaarden

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:geometrie*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **«vlak»**        | **Vlakgeometrie**    |

*Attribuut BRT.Next:typeInrichtingselement*

| *BRT.Next:waarde*       | *BRT.Next:definitie*                                                                                            |
|-------------------------|-----------------------------------------------------------------------------------------------------------------|
| **dok**                 | **Constructie bedoeld om schepen uit het water te halen en vervolgens weer in het water te laten.**             |
| **zwembad**             | **Constructie in de vorm van een bassin bedoeld om in te zwemmen**                                              |
| **bezinkbak**           | **Een gesloten reservoir waarin het afvalwater tijdelijk wordt opgevangen met een slibreinigende voorziening.** |
| **kilometerpaal water** | **Paal waarop de kilometrering van een water wordt aangegeven.**                                                |
