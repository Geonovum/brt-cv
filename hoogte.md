Hoogte
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Hoogte in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeHoogte’ wordt hernoemd naar ‘type’.

-   typen ‘peil’, ‘peil:’ en ‘peil:’ vervallen.

-   referentievlak ‘OLW’ vervalt.

*Overzicht attributen en waarden/type van object Hoogte in BRT.Next*

| Attribuutnaam  | Waarde of «type» | Definitie                                                                                                                         | Geometrietype | Kardinaliteit |
|----------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------|---------------|---------------|
| geometrie      | «lijn»           |                                                                                                                                   |               | 1-1           |
|                | «punt»           |                                                                                                                                   |               |               |
| type           | dieptelijn       | BRT: Lijn gevormd door punten met gelijke waterdiepte.                                                                            | lijn          | 1-1           |
|                | dieptepunt       | BRT: Punt waarvan de waterdiepte bekend is t.o.v. het referentievlak.                                                             | punt          |               |
|                | hoogtelijn       | BRT: Lijn die punten van gelijke hoogte met elkaar verbindt.                                                                      | lijn          |               |
|                | hoogtepunt       | BRT: Punt in de kaart, waarvan de hoogte bekend is ten opzichte van het referentievlak.                                           | punt          |               |
|                | hoogwaterlijn    | BRT: Lijn die de grens van het water aangeeft als de waterstand op zijn hoogst.                                                   | lijn          |               |
|                | laagwaterlijn    | BRT: Lijn die de grens van het water aangeeft als de waterstand op zijn laagst is.                                                | lijn          |               |
| hoogte         | «decimaal getal» | BRT: Hoogte van het object t.o.v. het referentievlak in meters met een nauwkeurigheid van 1 decimeter. / De diepte van het water. |               | 1-1           |
| referentievlak | NAP              | BRT: Het referentievlak waarop de hoogte van het object gebaseerd is.                                                             |               | 1-1           |
|                | LAT              |                                                                                                                                   |               |               |
|                | GHW              |                                                                                                                                   |               |               |

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

*n.v.t.*

### Naam+definitie

*n.v.t.*

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

*n.v.t.*

### Definitie

*n.v.t.*

### Naam+definitie

*n.v.t.*

Vervallen attributen
--------------------

n.v.t.

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*    |
|-----------------------------------|-------------------------------------------|
| typeHoogte\|type                  | ~~peil~~<br/>~~peil:~~<br/>~~peil:~~ |
| referentievlak                    | ~~OLW~~                               |

Toevoegen attributen
--------------------

*n.v.t.*

Toevoegen classificaties
------------------------

*n.v.t.*
