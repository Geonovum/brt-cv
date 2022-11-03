Bijlage: Wijzigingen t.o.v. consultatieversie 28 juni 2022
==========================================================

Wegdeel
-------

-   Schrappen van type ‘hoofdweg’ is teruggedraaid, opgenomen als type ‘rijbaan
    hoofdweg’, definitie is aangepast. Type ‘rijbaan autoweg’ geldt nu als
    toevoeging met een eigen definitie gebaseerd op BGT.

-   Schrappen van attribuut ‘verhardingsbreedteklasse’ is teruggedraaid.

-   Type van nieuw attribuut 'naam:herkomst' is gewijzigd van een waardenlijst
    naar vrij tekstveld.

Spoor
-----

-   Schrappen van type ‘metro’ is teruggedraaid.

-   Type ‘spoorbaan’(lichaam) is verplaatst van objecttype Terrein naar Spoor.

-   Geometrietype ‘vlak’ is toegevoegd voor type ‘spoorbaan’

-   Regel is toegevoegd dat attribuut aantalSporen alleen voorkomt bij
    lijngeometrie.

-   Schrappen van attribuut ‘elektrificatie’ is teruggedraaid.

Waterdeel
---------

-   Schrappen van geometrietype «punt» is teruggedraaid.

-   Schrappen van type ‘bron, wel’ is teruggedraaid, hernoemd naar ‘bron’.

-   geometrietype ‘vlak’ van type ‘water’ is gespecificeerd.

-   Schrappen van breedteklasse ‘6 - 12 meter’, ‘12 - 50 meter’, ‘50 - 125
    meter’, ‘\> 125 meter’ is teruggedraaid.

-   ligging ‘in duiker’ is geschrapt.

-   Type van nieuw attribuut 'naam:herkomst' is gewijzigd van een waardenlijst
    naar vrij tekstveld.

-   naam:taal ‘overig’ is hernoemd naar ‘onbekend/ VoidReason’, definitie is
    aangepast.

-   Regel toegevoegd dat naam: herkomst, naam:officieel en naam:taal verplicht
    attributen zijn als naam gevuld is.

Terrein
-------

-   Hernoemen van type ‘akkerland’ naar ‘bouwland’ (definitie wel aangepast naar
    BGT), type ‘boomkwekerij’ naar ‘boomteelt’, type ‘fruitkwekerij’ naar
    ‘fruitteelt’ (definitie wel minimaal aangepast) is teruggedraaid.

-   Schrappen van type ‘boomgaard’ is teruggedraaid, definitie is minimaal
    aangepast.

-   geometrie ‘vlak’ van type ‘struiken’ is gespecificeerd.

-   zinsnede ‘dat niet nader wordt ingewonnen’ in definitie van type ‘erf’ is
    geschrapt.

-   Optioneel attribuut ‘brugnaam’ is toegevoegd.

-   Voetnoot is aangepast: Spoorbaanlichaam verplaatst niet van objecttype
    Terrein naar objecttype Wegdeel, maar van objecttype Terrein naar objecttype
    Spoor.

Gebouw
------

-   type ‘boortoren’ is geschrapt (komt niet voor).

-   geometrietype ‘punt’ is toegevoegd aan type ‘bunker’

-   schrappen van type ‘tank’ is teruggedraaid, hernoemd naar ‘opslagtank’ met
    BGT definitie.

-   schrappen type ‘parkeerdak, parkeerdek, parkeergarage’ is teruggedraaid,
    type is hernoemd naar ‘parkeergarage’, definitie is aangepast, en
    geometrietype ‘punt’ is toegevoegd voor dit type.

-   schrappen type ‘synagoge’ is teruggedraaid

-   definitie van type ‘windmolen’ is gewijzigd

-   schrappen van type ‘windturbine’ is teruggedraaid, definitie is aangepast
    aan BGT.

-   typen ‘botenhuis’, ‘open loods’ en ‘overkapping’ zijn toegevoegd.

-   schrappen van typen ‘gevangenis’, ‘psychiatrisch ziekenhuis, psychiatrisch
    centrum’, en ‘ziekenhuis’ is teruggedraaid, typen zijn opgenomen bij
    attribuut ‘functie’

-   functie ‘parkeerdak, parkeerdek, parkeergarage’ is hernoemd naar ‘parkeren’,
    ‘radarpost’ is hernoemd naar ‘radarstation’.

-   attribuut ‘fysiekVoorkomen’ is hernoemd naar ‘ligging’

Inrichtingselement
------------------

-   schrappen van type ‘metrostation’ is teruggedraaid.

-   type ‘bassin’ is vervangen door type ‘dok’ en type ‘zwembad’

-   typen ‘opslagtank’, ‘windturbine’ en ‘botenhuis’ zijn verplaatst naar Gebouw

Relief
------

-   definitie van nieuw type ‘dijk’ is aangepast.

Hoogte
------

Geen

Registratief gebied
-------------------

-   Kardinaliteit van attribuut ‘naam:herkomst’ en ‘naam: taal’ gewijzigd naar 1
    of meer (1..\*)

-   Schrappen van attibuut ‘naamOfficieel’ teruggedraaid, hernoemd naar ‘naam:
    Officieel’, type aangepast naar waardenlijst ja/nee.

-   naam:taal ‘overig’ is hernoemd naar ‘onbekend/ VoidReason’, definitie is mee
    aangepast.

-   Type van nieuw attribuut 'naam:herkomst' is gewijzigd van een waardenlijst
    naar vrij tekstveld.

Geografisch gebied
------------------

-   Toevoegen attribuut ‘naamKartografisch’ is teruggedraaid.

-   Attribuut ‘naam: taal’ is toegevoegd
