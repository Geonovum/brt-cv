# Spoor

Dit hoofdstuk beschrijft de wijzigingen voor het object Spoor in BRT.Next ten
opzichte van de huidige versie TOP10NL.

## Overzicht

*Overzicht attributen en waarden/type van object Spoor in BRT.Next*

| Attribuutnaam          | Waarde of «type»             | Geometrietype | Kardinaliteit |
|------------------------|------------------------------|---------------|---------------|
| geometrie              | «lijn»                       |               | 1-1           |
|                        | «vlak»                       |               |               |
| typeSpoor              | trein                        | lijn          | 1-1           |
|                        | tram                         | lijn          |               |
|                        | sneltram                     | lijn          |               |
|                        | metro                        | lijn          |               |
|                        | gemengd                      | lijn          |               |
|                        | spoorbaan                    | vlak          |               |
| aantalSporen           | enkelvoudig                  |               | 1-1           |
|                        | meervoudig                   |               |               |
| elektrificatie         | ja                           |               | 1-1           |
|                        | nee                          |               |               |
| vervoerfunctie         | personenvervoer              |               | 1-1           |
|                        | goederenvervoer              |               |               |
|                        | personen- en goederenvervoer |               |               |
|                        | museumlijn                   |               |               |
| ligging                | op vast deel van brug        |               | 0..n          |
|                        | op beweegbaar deel van brug  |               |               |
|                        | in tunnel                    |               |               |
| relatieveHoogteligging | «geheel getal»               |               | 1-1           |
| status                 | bestaand                     |               | 1-1           |
|                        | in aanbouw                   |               |               |
| brugnaam               | «tekst»                      |               | 0..1          |
| tunnelnaam             | «tekst»                      |               | 0..1          |

<details class="note"> attribuut ‘aantalSporen’, ‘elektrificatie’ en ‘vervoerfunctie’ is
alleen verplicht voor objecten Spoor met lijngeometrie. </details>

## Wijzigen attributen

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

De volgende attributen wijzigen van naam, of wijzigen van naam en definitie in
BRT.Next.

| *TOP10NL:attribuutnaam* | *BRT.Next:attribuutnaam* |
|-------------------------|--------------------------|
| typeSpoor~~baan~~ | typeSpoor                |
| ~~fysiekVoorkomen~~ | **ligging**              |

### Definitie

Onderstaande attributen wijzigen van definitie in BRT.Next. De naam wordt niet
aangepast.

| *TOP10NL \| BRT.Next:attribuutnaam* | *TOP10NL:definitie*                                      | *BRT.Next:definitie*                                                  |
|-------------------------------------|----------------------------------------------------------|-----------------------------------------------------------------------|
| aantalSporen                        | ~~Het aantal sporen van~~ het spoorbaandeel.         | **Aanduiding of** het spoorbaandeel **enkelvoudig of meervoudig is.** |
| status                              | ~~De staat waarin het~~ object ~~zich bevindt.~~ | **De status gekoppeld aan de levenscyclus van een geo-object.**       |

### Naam+definitie

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|----------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~  | ~~Het~~ hoogte~~niveau~~van het object. | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note"> Het bereik van hoogteniveau|relatieveHoogteligging wijzigt van
een geheel getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.
</details>

## Wijzigen attribuutwaarden

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

Onderstaande attribuutwaarden wijzigen van naam (waarde) in BRT.Next. De
definitie wordt niet aangepast.

*Attribuut TOP10NL:aantalSporen \| BRT.Next:aantalSporen*

| TOP10NL:waarde | BRT.Next:waarde |
|----------------|-----------------|
| enkel          | enkel**voudig** |

### Definitie

Geen.

### Naam+definitie

Onderstaande attribuutwaarden wijzigen van naam (waarde) en definitie in BRT.Next.

*Attribuut TOP10NL\|BRT.Next:status*

| *TOP10NL:waarde* | *TOP10NL:definitie*          |*BRT.Next:waarde*| *BRT.Next:definitie*                                                             |
|------------------|------------------------------|-----------------|----------------------------------------------------------------------------------|
| in ~~uitvoering~~| ~~Het~~ object ~~is in~~ aanleg. | in **aanbouw**  | Object **waarvan de feitelijke bouw, verbouw of** aanleg **is aangevangen**. |  


## Vervallen attributen

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam*    | *TOP10NL:attribuutwaarden of «datatype»* |
|----------------------------|------------------------------------------|
| ~~typeInfrastructuur~~ | ~~verbinding~~; ~~kruising~~  |
| ~~spoorbreedte~~     | ~~normaalspoor~~; ~~smalspoor~~|
| ~~baanvaknaam~~      | ~~«tekst»~~                        |

## Vervallen attribuutwaarden

Onderstaande attribuutwaarden of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»*                          |
|-----------------------------------|-------------------------------------------------------------------|
| geometrie                         | ~~«punt»~~                                                  |
| fysiekVoorkomen \| ligging        | ~~overkluisd~~                                              |
| aantalSporen                      | ~~dubbel~~                                                  |
| status                            | ~~in gebruik~~; ~~buiten gebruik~~ |


## Toevoegen attributen

Geen.

## Toevoegen attribuutwaarden

Onderstaande attribuutwaarden worden toegevoegd aan BRT.Next.

*Attribuut BRT.Next:geometrie*

| *BRT.Next:status* | *BRT.Next:definitie*                               |
|-------------------|----------------------------------------------------|
| **vlak**          | **De vlakgeometrie van een spoor object.** |

<details class="note">regel: vlakgeometrie alleen bij Spoor van het type ‘spoorbaan’
</details>

*Attribuut BRT.Next:typeSpoor*

| *BRT.Next:status*            | *BRT.Next:definitie*                              |
|------------------------------|---------------------------------------------------|
| **spoorbaan**~~lichaam~~ | **Gebaand gedeelte voor het verkeer over rails.** |

<details class="note">type ‘spoorbaan’ verplaatst van objecttype Terrein naar objecttype
Spoor.</details> 

*Attribuut BRT.Next:status*

| *BRT.Next:status* | *BRT.Next:definitie*                                                                                               |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| **bestaand**      | **Object dat in gebruik is genomen of als gebruiksgereed kan worden beschouwd, dan wel buiten gebruik is gesteld** |
| **in aanbouw**    | **Object waarvan de feitelijke bouw, verbouw of aanleg is aangevangen.**                                           |
