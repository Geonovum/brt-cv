Inrichtingselement
==================

Dit hoofdstuk beschrijft de wijzigingen voor het object Inrichtingselement in
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
| type~~Inrichtingselement~~ | **type**                 |

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

Onderstaande classificaties wijzigen van naam (waarde) in BRT.Next. De definitie
wordt niet aangepast.

*Attribuut TOP10NL:typeInrichtingselement / BRT.Next:type*

| *TOP10NL:waarde*        | *BRT.Next:waarde*     |
|-------------------------|-----------------------|
| ~~baak~~[^2]        | **baken**             |
| ~~kaap~~2           | **baken**             |
| ~~GPS~~ kernnetpunt | **GNSS** kernnetpunt  |
| kilometerpaal           | kilometerpaal **weg** |

[^2]: TOP10NL-typen ‘baak’ en ‘kaap’ worden samengevoegd tot ‘baken’ in BRT.Next

### Definitie

*n.v.t.*

### Naam+definitie

Onderstaande classificaties wijzigen van naam (waarde) en definitie in BRT.Next

*Attribuut TOP10NL:typeWeg / BRT.Next:type*

| *TOP10NL:waarde*                   | *TOP10NL:definitie*                                                                                                                                                                                                                                                                                                                                                            | *BRT.Next:waarde* | *BRT.Next:definitie*                                                                                                                                      |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| geluids~~wering~~              | Constructie ten behoeve van het terugdringen van geluidsoverlast.                                                                                                                                                                                                                                                                                                              | geluids**scherm** | BGT: Een scheiding bedoeld om geluidshinder in de buitenlucht te verminderen.                                                                             |
| hek~~werk~~                    | Begrenzing van een terrein in de vorm van een afrastering.                                                                                                                                                                                                                                                                                                                     | hek               | Een hekwerk of schutting, typisch ten behoeve van erfafscheiding.                                                                                         |
| ~~aanleg~~steiger              | ~~In het water uitstekende brug of pier, breder dan 2 meter, gebruikt om personen en goederen aan~~ wal ~~te brengen.~~                                                                                                                                                                                                                                                | steiger           | **Vaste (niet drijvende) waterbouwkundige constructie voor het aanleggen van schepen en bedoeld om deze schepen vanaf de** wal **te laden en te lossen.** |
| strekdam~~, krib, golfbreker~~ | Dam in de richting van de loop van de rivier of kanaal, ter beveiliging van de oevers of brugpijlers of tot beperking van de rivier tot een bepaalde breedte (strekdam). Golfslagbreker of stroombreker langs de kust en in rivieren, staat loodrecht op de oever/kust (krib). Een uit steenglooiing of stortsteen bestaand object bedoelt voor oeverbescherming (golfbreker). | strekdam          | BGT: Constructie in het water ter verdediging van de kust/oever.                                                                                          |

Vervallen attributen
--------------------

Onderstaande attributen en bijbehorende classificaties of datatypen vervallen in
BRT.Next.

| *TOP10NL:attribuutnaam* | *TOP10NL:classificaties of «datatype»* |
|-------------------------|----------------------------------------|
| ~~breedte~~         | ~~«decimaal getal»~~               |

Vervallen classificaties
------------------------

Onderstaande classificaties of datatypen vervallen bij een attribuut in
BRT.Next. Het attribuut blijft wel bestaan.

| *TOP10NL\|BRT.Next:attribuutnaam* | *TOP10NL:classificaties of «datatype»*                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeInrichtingselement \| type    | ~~dukdalf~~;~~gaswinning~~;~~golfmeetpaal~~;~~havenhoofd~~;~~helikopterlandingsplatform~~;~~kilometerraaibord~~;~~kilometerraaipaal~~;~~koedam~~;~~kogelvanger schietbaan~~;~~kraan~~;~~leiding~~;~~metrostation~~;~~oliepompinstallatie~~;~~radiobaken~~;~~RD punt~~;~~schietbaan~~;~~seinmast~~;~~tol~~;~~verkeersgeleider~~;~~zichtbaar wrak~~ |

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
| **open loods**    |                      |
| **overkapping**   |                      |
| **bassin**        |                      |
| **bezinkbak**     |                      |
| **opslagtank**    |                      |
| **windturbine**   |                      |
| **botenhuis**     |                      |
| **waterwoning**   |                      |
|                   |                      |
