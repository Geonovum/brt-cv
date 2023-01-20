Geografisch gebied
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Geografisch gebied in
BRT.Next ten opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#geografisch-gebied).

Overzicht
---------

*Overzicht attributen en waarden/type van object Geografisch gebied in BRT.Next*

| Attribuutnaam         | Waarde of «type»      | Geometrietype   | Kardinaliteit |
|-----------------------|-----------------------|-----------------|---------------|
| geometrie             | «vlak»                |                 | 1-1           |
|                       | «multivlak»           |                 |               |
| typeGeografischGebied | bank, ondiepte, plaat | vlak, multivlak | 1-1           |
|                       | bosgebied             | vlak, multivlak |               |
|                       | duingebied            | vlak, multivlak |               |
|                       | eiland                | vlak, multivlak |               |
|                       | geul, vaargeul        | vlak, multivlak |               |
|                       | heidegebied           | vlak, multivlak |               |
|                       | heuvel, berg          | vlak, multivlak |               |
|                       | kaap, hoek            | vlak, multivlak |               |
|                       | polder                | vlak, multivlak |               |
|                       | streek, veld          | vlak, multivlak |               |
|                       | terp, wierde          | vlak, multivlak |               |
|                       | wad                   | vlak, multivlak |               |
|                       | watergebied           | vlak, multivlak |               |
|                       | zee                   | vlak, multivlak |               |
|                       | zeegat, zeearm        | vlak, multivlak |               |
| naam                  | “tekst”               |                 | 0..n          |
| naam: taal            | Nederlands            |                 | 0..n          |
|                       | Fries                 |                 |               |
|                       | onbekend / VoidReason |                 |               |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object GeografischGebied ten
opzichte van vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuut | wordt hernoemd naar       |
|-----------|---------------------------|
| type      | type**GeografischGebied** |

### Attribuutwaarden

Geen
