Geografisch gebied
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Geografisch gebied in
BRT.Next ten opzichte van de huidige versie TOP10NL.

Overzicht
---------

*Overzicht attributen en waarden/type van object Geografisch gebied in BRT.Next*

| Attribuutnaam | Waarde of «type»      | Geometrietype   | Kardinaliteit |
|---------------|-----------------------|-----------------|---------------|
| geometrie     | «vlak»                |                 | 1-1           |
|               | «multivlak»           |                 |               |
| type          | bank, ondiepte, plaat | vlak, multivlak | 1-1           |
|               | bosgebied             | vlak, multivlak |               |
|               | duingebied            | vlak, multivlak |               |
|               | eiland                | vlak, multivlak |               |
|               | geul, vaargeul        | vlak, multivlak |               |
|               | heidegebied           | vlak, multivlak |               |
|               | heuvel, berg          | vlak, multivlak |               |
|               | kaap, hoek            | vlak, multivlak |               |
|               | polder                | vlak, multivlak |               |
|               | streek, veld          | vlak, multivlak |               |
|               | terp, wierde          | vlak, multivlak |               |
|               | wad                   | vlak, multivlak |               |
|               | watergebied           | vlak, multivlak |               |
|               | zee                   | vlak, multivlak |               |
|               | zeegat, zeearm        | vlak, multivlak |               |
| naam          | “tekst”               |                 | 0..n          |
| naam: taal    | Nederlands            |                 | 0..n          |
|               | Fries                 |                 |               |
|               | onbekend / VoidReason |                 |               |

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

*Geen.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                     | *BRT.Next:attribuutnaam* | *BRT.Next:definitie*                |
|-------------------------|---------------------------------------------------------|--------------------------|-------------------------------------|
| naam~~NL~~          | De ~~Nederlandse~~ naam van het geografisch gebied. | naam                     | De naam van het geografisch gebied. |

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

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|------------------------------------------|
| ~~naamFries~~       | ~~«tekst»~~                          |

Vervallen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-----------------------------------|------------------------------------------|
| geometrie                         | ~~«punt»~~                           |
| typeGeografischGebied\|type       | ~~overig~~                           |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie*                                         | *Verplicht/optioneel*    | *Attribuutwaarde*                            |
|--------------------------|-----------------------------------------------------|--------------------------|----------------------------------------------|
| **naam: taal**           | **De taal van de naam van het geografisch gebied.** | **Verplicht, 0 of meer** | **Nederlands; Fries; onbekend / VoidReason** |

Toevoegen attribuutwaarden
--------------------------

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:naam:taal*

| *BRT.Next:waarde*         | *BRT.Next:definitie*  |
|---------------------------|-----------------------|
| **Nederlands**            | **Nederlandse taal.** |
| **Fries**                 | **Friese taal.**      |
| **onbekend / VoidReason** | **Taal is onbekend.** |
