Relief
======

Dit hoofdstuk beschrijft de wijzigingen voor het object Relief in BRT.Next ten
opzichte van de [vorige versie van het
wijzigingsvoorstel](https://geonovum.github.io/brt-next-cv/#relief).

Overzicht
---------

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

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Relief ten opzichte van
vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuutnaam | wordt hernoemd naar |
|---------------|---------------------|
| type          | type**Relief**      |

### Attribuutwaarden

*Vervallen*

| Bij attribuut | vervalt waarde of «type» |
|---------------|--------------------------|
| geometrie     | ~~«vlak»~~               |
| typeRelief    | ~~dijk~~                 |


