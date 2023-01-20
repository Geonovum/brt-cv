Hoogte
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Hoogte in BRT.Next ten
opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#hoogte).

Overzicht
---------

*Overzicht attributen en waarden/type van object Hoogte in BRT.Next*

| Attribuutnaam  | Waarde of «type» | Geometrietype | Kardinaliteit |
|----------------|------------------|---------------|---------------|
| geometrie      | «lijn»           |               | 1-1           |
|                | «punt»           |               |               |
| typeHoogte     | dieptelijn       | lijn          | 1-1           |
|                | dieptepunt       | punt          |               |
|                | hoogtelijn       | lijn          |               |
|                | hoogtepunt       | punt          |               |
|                | hoogwaterlijn    | lijn          |               |
|                | laagwaterlijn    | lijn          |               |
| hoogte         | «decimaal getal» |               | 1-1           |
| referentievlak | NAP              |               | 1-1           |
|                | LAT              |               |               |
|                | GHW              |               |               |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Hoogte ten opzichte van
vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuutnaam | wordt hernoemd naar |
|---------------|---------------------|
| type          | type**Hoogte**      |

### Attribuutwaarden

Geen
