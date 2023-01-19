Inrichtingselement
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Inrichtingselement in
BRT.Next ten opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#inrichtingselement).

Overzicht
---------

*Overzicht attributen en waarden/type van object Inrichtingselement in BRT.Next*

| Attribuutnaam           | Waarde of «type»       | Geometrietype | Kardinaliteit |
|-------------------------|------------------------|---------------|---------------|
| geometrie               | «punt»                 |               | 1-1           |
|                         | «lijn»                 |               |               |
|                         | «vlak»                 |               |               |
|  typeInrichtingselement | baken                  | punt          | 1-1           |
|                         | bomenrij               | lijn          |               |
|                         | boom                   | punt          |               |
|                         | botenhelling           | punt          |               |
|                         | busstation             | punt          |               |
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
|                         | kilometerpaal spoorweg | punt          |               |
|                         | kilometerpaal water    | punt          |               |
|                         | klokkenstoel           | punt          |               |
|                         | kruis                  | punt          |               |
|                         | luchtvaartlicht        | punt          |               |
|                         | markant object         | punt          |               |
|                         | metrostation           | punt          |               |
|                         | muur                   | lijn          |               |
|                         | paal                   | punt          |               |
|                         | paalwerk               | lijn          |               |
|                         | peilschaal             | punt          |               |
|                         | pijler                 | vlak, punt    |               |
|                         | plaatsnaambord         | lijn, punt    |               |
|                         | radiotelescoop         | punt          |               |
|                         | scheepvaartlicht       | punt          |               |
|                         | sluisdeur              | lijn, punt    |               |
|                         | sneltramhalte          | punt          |               |
|                         | steiger                | lijn, vlak    |               |
|                         | stormvloedkering       | lijn          |               |
|                         | strandpaal             | punt          |               |
|                         | strekdam               | lijn          |               |
|                         | stuw                   | lijn, punt    |               |
|                         | treinstation           | punt          |               |
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

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Inrichtingselement ten
opzichte van vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuutnaam | wordt hernoemd naar        |
|---------------|----------------------------|
| type          | type**Inrichtingselement** |

*Vervallen*

| Attribuut      | vervalt met attribuutwaarden |
|----------------|------------------------------|
| ~~status~~ | ~~bestaand~~             |

### Attribuutwaarden

*Vervallen*

| Bij attribuut          | vervalt attribuutwaarde |
|------------------------|-------------------------|
| typeInrichtingselement | ~~vliedberg~~       |

*Toevoegen*

| Aan attribuut          | wordt attribuutwaarde toegevoegd |
|------------------------|----------------------------------|
| typeInrichtingselement | **dukdalf**                      |
