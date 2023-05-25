# Relief

Dit hoofdstuk beschrijft de wijzigingen voor het object Relief in BRT.Next ten
opzichte van de huidige versie TOP10NL.

## Overzicht

*Overzicht attributen en waarden/type van object Relief in BRT.Next*

| Attribuutnaam          | Waarde of «type»       | Geometrietype      | Kardinaliteit |
|------------------------|------------------------|--------------------|---------------|
| geometrie              | «lijn»                 |                    | 1..1          |
|                        | «hoge en lage zijde»   |                    |               |
| typeRelief             | wal                    | lijn               | 1..1          |
|                        | steile rand, aardrand  | hoge en lage zijde |               |
|                        | talud, hoogteverschil  | hoge en lage zijde |               |
| hoogteklasse           | \< 1 meter             |                    | 1..1          |
|                        | 1 – 2,5 meter          |                    |               |
|                        | \> 2,5 meter           |                    |               |
| relatieveHoogteligging | «geheel getal [-9; 9]» |                    | 1..1          |

## Wijzigen attributen

De attributen in deze paragraaf wijzigen van naam, wijzigen van definitie, of
wijzigen van naam en definitie in BRT.Next.

### Naam

*Geen.*

### Definitie

*Geen.*

### Naam+definitie

Onderstaande attributen wijzigen van naam en definitie in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:definitie*                             | *BRT.Next:attribuutnaam*   | *BRT.Next:definitie*                                    |
|-------------------------|-------------------------------------------------|----------------------------|---------------------------------------------------------|
| ~~hoogteniveau~~      | ~~Het~~ hoogte~~niveau~~ van het object.   | **relatieveHoogteligging** | **Aanduiding voor de relatieve** hoogte van het object. |

<details class="note">Het bereik van hoogteniveau\|relatieveHoogteligging wijzigt van een geheel getal kleiner of gelijk aan 0 naar geheel getal van -9 tot en met 9.</details>

## Wijzigen attribuutwaarden

De attribuutwaarden in deze paragraaf wijzigen van naam (waarde), wijzigen van
definitie, of wijzigen van naam (waarde) en definitie in BRT.Next

### Naam

*Geen.*

### Definitie

*Geen.*

### Naam+definitie

*Geen.*

## Vervallen attributen

Onderstaande attributen en bijbehorende attribuutwaarden of datatypen vervallen
in BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:attribuutwaarden of «datatype»* |
|-------------------------|------------------------------------------|
| ~~functie~~         | ~~geluid weren~~                     |

## Vervallen attribuutwaarden

Geen.
 

## Toevoegen attributen

*Geen.*

## Toevoegen attribuutwaarden

*Geen.*
