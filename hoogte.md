Hoogte
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Hoogte in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Overzicht
---------

*Overzicht attributen en waarden/type van object Hoogte in BRT.Next*

| Attribuutnaam  | Waarde of «type» | Geometrietype | Kardinaliteit |
|----------------|------------------|---------------|---------------|
| geometrie      | «lijn»           |               | 1-1           |
|                | «punt»           |               |               |
| type           | dieptelijn       | lijn          | 1-1           |
|                | dieptepunt       | punt          |               |
|                | hoogtelijn       | lijn          |               |
|                | hoogtepunt       | punt          |               |
|                | hoogwaterlijn    | lijn          |               |
|                | laagwaterlijn    | lijn          |               |
| hoogte         | «decimaal getal» |               | 1-1           |
| referentievlak | NAP              |               | 1-1           |
|                | LAT              |               |               |
|                | GHW              |               |               |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| TOP10NL:attribuutnaam | BRT.Next:attribuutnaam |
|-----------------------|------------------------|
| type~~Hoogte~~    | type                   |

### Definitie

*Geen.*

### Naam+definitie

*Geen.*

Wijzigen attribuutwaarden
-------------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

*Geen.*

### Definitie

*Geen.*

### Naam+definitie

*Geen.*

Vervallen attributen
--------------------

Geen.

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                      |
|-----------------------------------|---------------------------------------------------------------|
| typeHoogte\|type                  | ~~peil~~;~~peil: zomerpeil~~;~~peil winterpeil:~~ |
| referentievlak                    | ~~OLW~~                                                   |

Toevoegen attributen
--------------------

*Geen.*

Toevoegen attribuutwaarden
--------------------------

*Geen.*
