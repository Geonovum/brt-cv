Geografisch gebied
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Geografisch gebied in
BRT.Next ten opzichte van de huidige versie TOP10NL.

Samenvatting
------------

Samengevat worden de volgende wijzigingen voorgesteld:

-   attribuut ‘typeGeografischGebied’ wordt hernoemd naar ‘type’;
    attribuutwaarde ‘overig’ vervalt.

-   attribuut ‘naamNL’ wordt hernoemd naar ‘naam’ met iets aangepaste definitie.

-   attribuut ‘naamFries’ vervalt

-   attribuut ‘naamKartografisch’ wordt toegevoegd met datatype «tekst»

-   puntgeometrie vervalt bij attribuut geometrie

*Overzicht attributen en waarden/type van object Geografisch gebied in BRT.Next*

| Attribuutnaam     | Waarde of “type”      | Geometrietype   | Kardinaliteit |
|-------------------|-----------------------|-----------------|---------------|
| geometrie         | “vlak”                |                 | 1 à 1         |
|                   | “multivlak”           |                 |               |
| type              | bank, ondiepte, plaat | vlak, multivlak | 1 à 1         |
|                   | bosgebied             | vlak, multivlak |               |
|                   | duingebied            | vlak, multivlak |               |
|                   | eiland                | vlak, multivlak |               |
|                   | geul, vaargeul        | vlak, multivlak |               |
|                   | heidegebied           | vlak, multivlak |               |
|                   | heuvel, berg          | vlak, multivlak |               |
|                   | kaap, hoek            | vlak, multivlak |               |
|                   | polder                | vlak, multivlak |               |
|                   | streek, veld          | vlak, multivlak |               |
|                   | terp, wierde          | vlak, multivlak |               |
|                   | wad                   | vlak, multivlak |               |
|                   | watergebied           | vlak, multivlak |               |
|                   | zee                   | vlak, multivlak |               |
|                   | zeegat, zeearm        | vlak, multivlak |               |
| naam              | “tekst”               |                 | 0 à N         |
| naamKartografisch | “tekst”               |                 | 0 à 1         |

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam*       | *BRT.Next:attribuutnaam* |
|-------------------------------|--------------------------|
| type~~GeografischGebied~~ | type                     |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam* | *BRT.Next:definitie* |
|-------------------------|-------------------------------------------------|--------------------------|----------------------|
| naam~~NL~~          | De Nederlandse naam van het geografisch gebied. | naam                     |                      |

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
| ~~naamFries~~1      | ~~«tekst»~~                        |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-----------------------------------|----------------------------------------|
| geometrie                         | ~~«punt»~~                         |
| typeGeografischGebied\|type       | ~~overig~~                         |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie* | *Verplicht/optioneel* | *Domein*    |
|--------------------------|-------------|-----------------------|-------------|
| **naamKartografisch**    |             | **Optioneel, 0 of 1** | **«tekst»** |

Toevoegen classificaties
------------------------

*n.v.t.*
