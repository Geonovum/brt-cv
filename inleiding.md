# Inleiding

In opdracht van het ministerie van BZK werkt het Kadaster aan een
doorontwikkeling van de BRT. Deze “BRT.Next” zal zijn gebaseerd op de BGT, de
BAG, andere bestaande bronnen en eigen inwinning. De BRT.Next wordt in
samenwerking met DiS-Geo ontwikkeld, waarbij afstemming wordt gezocht met de
landelijke Samenhangende Objectenregistratie. Het productieproces van de diverse
(toekomstige) producten wordt geoptimaliseerd door gebruik te maken van
algoritmes voor automatische objectvorming en generalisatie.

Er zijn gebruikerssessies gehouden waarin de bevindingen tijdens de ontwerpfase
van de nieuwe BRT.Next met gebruikers gedeeld zijn. Ook was er de mogelijkheid
om een reactie te geven op een eerste opzet van het nieuwe datamodel voor
BRT.Next.

De ervaringen uit deze gebruikerssessies en consultatie zijn de afgelopen
periode gebruikt bij het samenstellen van een nieuw informatiemodel voor
BRT.Next. Het is belangrijk om te beseffen dat de datamodellen van de BAG en de
BGT hiervoor het uitgangspunt zijn. Daar waar mogelijk is de inhoud daarvan 1 op
1 overgenomen. Daarnaast is ieder object en iedere eigenschap uit het
informatiemodel van TOP10NL geanalyseerd, vergeleken met de andere
basisregistraties en vanuit meerdere aspecten bekeken. Is het bijvoorbeeld
topografie, cartografie of informatie, wat is het gebruik en het bijhoud-proces
van dit object of deze eigenschap. Op basis van deze analyse is voor ieder
object en iedere eigenschap één van onderstaande keuzes gemaakt in het nieuwe
informatiemodel:

-   Harmoniseren vanwege andere registratie (BGT, BAG, “SOR”, …)

-   Behouden in BRT.Next

-   Op een andere manier opnemen in BRT.Next

-   Vervallen, want werd (nog) niet bijgehouden in de BRT

-   Vervallen, want niet (meer) relevant voor de nieuwe BRT.Next-producten (bv.
    niet op kaart)

-   Vervallen, want niet passend bij BRT.Next

-   Toegevoegd aan BRT.Next

## Wijzigingsvoorstel BRT.Next

In drie consultaties heeft het Kadaster het nieuwe informatiemodel voorgelegd
aan de gebruikers van de BRT. Dit wijzigingsvoorstel is het resultaat van de
drie consultaties. Deze versie wordt met het ministerie van BZK besproken en
vervolgens vastgesteld als “BRT.Next Informatiemodel versie 1.0”.

Deze versie van het informatiemodel BRT.Next is gemaakt voor het BRT.Next
product op schaal 1:10.000 en beschrijft welke objecten en eigenschappen er
vastgelegd worden in BRT.Next. Algemene objectkenmerken, zoals de identificatie,
attributen voor de levensloop van een object en visualisatiecode, zijn nu nog
niet opgenomen in deze consultatie. Voor deze attributen wil het Kadaster zo
veel mogelijk aansluiten bij de standaarden en bij TOP10NL.

Het informatiemodel kan tijdens het realiseren van het product nog licht
aangepast worden doordat op dit moment het hele proces nog niet bekend is. Als
voorbeeld is het generalisatieproces van o.a. de BGT en BAG op schaal 1:1.000
naar de BRT.Next op schaal 1:10.000 nog niet ontwikkeld. Hierover zal het
Kadaster u blijven informeren.

In dit wijzigingsvoorstel worden alle wijzigingen beschreven van de huidige
TOP10NL (WAS) naar de nieuwe BRT.Next (WORDT).

Al uw vragen of opmerkingen over het wijzigingsvoorstel van BRT.Next stelt u per
email aan
[brt@kadaster.nl](file:///C:\Users\A.deBoer\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\M7F255CS\brt@kadaster.nl).

## Leeswijzer

De voorgestelde wijzigingen in de BRT.Next t.o.v. TOP10NL zijn in dit document
gemarkeerd: ~~tekst met deze opmaak~~ komt te vervallen, **tekst met deze
opmaak** wordt toegevoegd.

In de desktopversie van het wijzigingsvoorstel wordt een schakelknop in het
venster rechts onderin getoond, waarmee u de wijzigingen aan (zichtbaar) of uit
(verborgen) kunt zetten.

De wijzigingen worden in een vaste structuur gepresenteerd. Elk objecttype
begint met een tabel met de attributen en attribuutwaarden voor dit object na
het doorvoeren van de wijzigingen. Vervolgens wordt per objecttype beschreven
welke attributen en attribuutwaarden wijzigen, vervallen of worden toegevoegd.

We hanteren in dit document de term ‘attribuut’ voor een kenmerk of eigenschap
van een object; de term ‘attribuutwaarde’ voor het type of de waarde dat een
attribuut kan aannemen.

Een attribuut of attribuutwaarde kan op drie manieren wijzigen:

1.  de naam van het attribuut of attribuutwaarde wijzigt; de definitie wijzigt
    niet.

2.  de definitie van het attribuut of attribuutwaarde wijzigt; de naam wijzigt
    niet.

3.  de naam en definitie van het attribuut of de attribuutwaarde wijzigen.

Als twee attribuutwaarden worden samengevoegd tot één nieuwe attribuutwaarde
wordt dit in het document beschreven als het laten vervallen van twee
attribuutwaarden en het toevoegen van een nieuwe attribuutwaarde, met in de
toelichting (voetnoot) dat er sprake is van een samenvoeging.

Bij meerdere objectklassen is de modellering van ‘de naam van een object’
aangepast. Waar er in TOP10NL meerdere naam-attributen waren (bijvoorbeeld:
Naam_Nederlands, Naam_Fries en Naam_officieel) worden in BRT.Next de taal, de
herkomst en de aanduiding of een naam officieel is per naam aangegeven. Hiervoor
zijn de attributen “naam: taal”, “naam: herkomst” en “naam: officieel” in het
model opgenomen en die attributen beschrijven de eigenschappen van een naam van
een object.
