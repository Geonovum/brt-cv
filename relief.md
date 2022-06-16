Relief
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Relief in BRT.Next ten
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
| type~~Relief~~      | type                     |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*       | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|--------------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~    | ~~Het ~~hoogte~~niveau~~van het object. | **relatieveHoogteLigging**[^1] | **Aanduiding voor de relatieve** hoogte van het object. |

[^1]: Het domein van hoogteniveau/relatieveHoogteligging wijzigt van geheel
getal Kleiner of gelijk aan 0 naar geheel getal tussen -9 en 9.

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

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-------------------------|----------------------------------------|
| ~~functie~~         | ~~geluid weren~~                   |

Vervallen classificaties
------------------------

*n.v.t.*

Toevoegen attributen
--------------------

*n.v.t.*

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:geometrie*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **«vlak»**        | Vlakgeometrie        |

*Attribuut BRT.Next:type*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **dijk**          |                      |
