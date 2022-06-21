Relief
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Relief in BRT.Next ten
opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeRelief’ wordt hernoemd naar ‘type’.

-   type ‘dijk’ wordt toegevoegd.

-   attribuut ‘hoogteniveau’ wordt hernoemd naar ‘relatieveHoogteligging’,
    definitie wordt en bereik -9 tot 9 wordt aangepast op BGT.

-   attribuut ‘functie’ vervalt.

-   vlakgeometrie wordt toegevoegd.

*Overzicht attributen en waarden/type van object Relief in BRT.Next*

| Attribuutnaam          | Waarde of «type»       | Geometrietype      | Kardinaliteit |
|------------------------|------------------------|--------------------|---------------|
| geometrie              | «vlak»                 |                    | 1..1          |
|                        | «lijn»                 |                    |               |
|                        | «hoge en lage zijde»   |                    |               |
| type                   | dijk                   | vlak, lijn         | 1..1          |
|                        | wal                    | lijn               |               |
|                        | steile rand, aardrand  | hoge en lage zijde |               |
|                        | talud, hoogteverschil  | hoge en lage zijde |               |
| hoogteklasse           | \< 1 meter             |                    | 1..1          |
|                        | 1 – 2,5 meter          |                    |               |
|                        | \> 2,5 meter           |                    |               |
| relatieveHoogteligging | «geheel getal [-9; 9]» |                    | 1..1          |

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
| ~~hoogteniveau~~    | ~~Het~~ hoogte~~niveau~~van het object. | **relatieveHoogteligging**[^1] | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note">Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van een geheel
getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details>

Wijzigen attribuutwaarden
-----------------------

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

*n.v.t.*

### Definitie

*n.v.t.*

### Naam+definitie

*n.v.t.*

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|----------------------------------------|
| ~~functie~~         | ~~geluid weren~~                   |

Vervallen attribuutwaarden
------------------------

*n.v.t.*

Toevoegen attributen
--------------------

*n.v.t.*

Toevoegen attribuutwaarden
------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:geometrie*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **«vlak»**        | **Vlakgeometrie**    |

*Attribuut BRT.Next:type*

| *BRT.Next:waarde* | *BRT.Next:definitie*                                                     |
|-------------------|--------------------------------------------------------------------------|
| **dijk**          | **Langgerekte ophoging in het terrein met een hoogte vanaf 1,00 meter.** |
