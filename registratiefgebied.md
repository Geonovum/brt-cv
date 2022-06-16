Registratief gebied
===================

Dit hoofdstuk beschrijft de wijzigingen voor het object Registratief gebied in
BRT.Next ten opzichte van de huidige versie TOP10NL.

Wijzigen attributen
-------------------

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

Onderstaande attributen wijzigen van naam in BRT.Next. De definitie wordt niet
aangepast.

| *TOP10NL:attribuutnaam*        | *BRT.Next:attribuutnaam* |
|--------------------------------|--------------------------|
| type~~RegistratiefGebied~~ | type                     |

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                                    | *BRT.Next:attribuutnaam* | *BRT.Next:definitie*                 |
|-------------------------|--------------------------------------------------------|--------------------------|--------------------------------------|
| naam~~Officieel~~   | De ~~officiële~~ naam van het registratief gebied. | naam                     | De naam van het registratief gebied. |

Wijzigen classificaties
-----------------------

De classificaties in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

| *TOP10NL:waarde*         | *BRT.Next:waarde*  |
|--------------------------|--------------------|
| ~~land~~             | **rijk**           |
| ~~territoriale zee~~ | **maritieme zone** |

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
| ~~naamNL~~[^1]      | ~~«tekst»~~                        |
| ~~naamFries~~1      | ~~«tekst»~~                        |

[^1]: TOP10NL-attributen naamNL en naamFries met datatype «tekst» worden
vervangen door attribuut naam:taal met attribuutwaarden ‘Nederlands’; ‘Fries’;
‘overig’ in BRT.Next.

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-----------------------------------|----------------------------------------|
| geometrie                         | ~~«punt»~~                         |
| typeRegistratiefGebied\|type      | ~~waterschap~~                     |

Toevoegen attributen
--------------------

Onderstaande attributen worden toegevoegd aan BRT.Next.

| *BRT.Next:Attribuutnaam* | *Definitie* | *Verplicht/optioneel*     | *Domein*                      |
|--------------------------|-------------|---------------------------|-------------------------------|
| **naam: taal**           |             | **Optioneel, 0 of meer.** | **Nederlands; Fries; overig** |
| **naam: herkomst**       |             | **Optioneel, 0 of meer.** | **BAG; BGT; BRK; overig**     |

Toevoegen classificaties
------------------------

Onderstaande classificaties (waarden) worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:naam:taal*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **Nederlands**    |                      |
| **Fries**         |                      |
| **overig**        |                      |

*Attribuut BRT.Next:naam:herkomst*

| *BRT.Next:waarde* | *BRT.Next:definitie* |
|-------------------|----------------------|
| **BAG**           |                      |
| **BGT**           |                      |
| **BRK**           |                      |
| **overig**        |                      |
