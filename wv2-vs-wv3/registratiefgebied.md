Registratief gebied
===================

Dit hoofdstuk beschrijft de wijzigingen voor het object Registratief gebied in
BRT.Next ten opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#registratief-gebied).

Overzicht
---------

*Overzicht attributen en waarden/type van object Registratief gebied in
BRT.Next*

| Attribuutnaam          | Waarde of «type»      | Geometrietype   | Kardinaliteit |
|------------------------|-----------------------|-----------------|---------------|
| geometrie              | «vlak»                |                 | 1-1           |
|                        | «multivlak»           |                 |               |
| typeRegistratiefGebied | land                  | vlak, multivlak | 1-1           |
|                        | provincie             | vlak, multivlak |               |
|                        | gemeente              | vlak, multivlak |               |
|                        | maritieme zone        | vlak, multivlak |               |
| naam                   | «tekst»               |                 | 1-1           |
| naam: taal             | Nederlands            |                 | 1..n          |
|                        | Fries                 |                 |               |
|                        | onbekend / VoidReason |                 |               |
| naam: herkomst         | «tekst»               |                 | 1..n          |
| naam: officieel        | ja                    |                 | 1..n          |
|                        | nee                   |                 |               |
| nummer                 | «tekst»               |                 | 0..1          |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object RegistratiefGebied ten
opzichte van vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuut | wordt hernoemd naar        |
|-----------|----------------------------|
| type      | type**RegistratiefGebied** |

### Attribuutwaarden

*Hernoemen*

| Bij attribuut          | wordt attribuutwaarde | hernoemd naar |
|------------------------|-----------------------|---------------|
| typeRegistratiefGebied | rijk                  | \~\~land\~\~  |
