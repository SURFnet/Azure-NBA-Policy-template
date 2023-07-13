# SURFaudit AZURE Policy template

> As this project is specific for the Dutch education and research institutions the rest of this article will be in Dutch.


Dit SURF project omvat een Initiative Policy Template, welke ingeladen kan worden in Microsoft Azure. In combinatie met Defender for Cloud kan men auditen of resources in een Azure omgeving voldoen aan niveau 3 van het SURFaudit toetsingskader.

Deze template is het startpunt om niveau 3 van het [SURFaudit toetsingskader](https://www.surf.nl/surfaudit-toetsingskader-beoordeel-je-informatiebeveiliging) te halen in een Microsoft cloud omgeving. De template kan worden aangepast aan de eisen en wensen van een specifieke organisatie. De template omvat uitsluitend technische controls. Procesmatige controls dienen binnen de organisatie ingevoerd te worden om volledig tot niveau 3.


Deze template is het startpunt om aan SURFaudit niveau 3 te voldoen in een Microsoft cloud omgeving. De template kan worden aangepast aan de specifieke eisen en wensen van een organisatie. De template omvat uitsluitend technische controls. Procesmatige controls dienen binnen de organisatie ingevoerd te worden om tot een volledig dekkende compliancy te komen. Alle policies zijn van het type audit of deny en allen zijn initieel ingesteld op audit. De instelling kan bij de meeste policies worden aangepast naar deny. Er is bewust gekozen om geen modify en deploy if not exist policies te gebruiken om te voorkomen dat de policy assignment een identity met azure permisies nodig heeft. 

Periodiek zal deze template worden geupdate met nieuwe policies en/of aanpassingen de focus ligt dan op deprecated policies en/of nieuwe policies die in de Microsoft Security Baseline zijn toegevoegd en ook van toepassing zijn op de SURFaudit controls. Zie hiervoor het update process.

## Aandachts punten
1. Kosten
Houd er rekening mee dat het verkrijgen van een groen technische Azure controls, vooral bepaalde beveiligingspolicies, zoals een audit van of Microsoft Defender for Cloud is enabled, mogelijk extra kosten met zich meebrengt. Een betere beveiligingsmonitoring heeft natuurlijk waarde, maar kan dus extra kosten met zich meebrengen. Momenteel zijn alle technische controls ingesteld op 'audit' en is er geen 'deploy if not exist' policies. Dit resulteerd dat de instelling zelf bepaald of het wel of niet nodig is additionele security feautures te deployen danwel losse additionele policies te implementeren die deze automatisch configureren. 
2. Azure Landing Zone 
Het wordt aanbevolen om ook de [Azure Landing Zone architectuur](https://aka.ms/alz) te volgen om een solide basis te hebben voor een veilige Azure-omgeving. Deze template moet gebruikt worden in combinatie met een ALZ-implementatie, ALZ bevat ook afdwingingsbeleid, zoals 'deny', 'deploy if not exist', enz. Binnen de management group-structuur kan ervoor gekozen worden om onderscheid te maken tussen landing zones voor IT en bijvoorbeeld landing zones voor onderzoek, met afwijkende beleidsregels, en of afwijkende data clasificatie om zo bijvoorbeeld encryption met customer managed keys te auditten danwel af e dwingen. Dit kan met dit initiatief te deployen op lagere management group nivo inclusief verschillende geparametriseerde implementaties van deze technische Azure controls.
Het documenteren of voorbeelden van afdwingbeleid is niet opgenomen in deze template, maar zal als een toekomstige uitbreiding worden overwogen.


## Preview
Dit is de eerste versie van het Initiative Policy Template en het is bedoeld als een testversie om feedback te verzamelen. We nodigen gebruikers uit om de template te testen en eventuele opmerkingen, suggesties of verbeteringen aan te geven via Git issues of pull requests.

We waarderen alle input die kan bijdragen aan het verbeteren van de template en het maken van toekomstige versies die nog effectiever en gebruiksvriendelijker zijn. Door middel van Git issues kunnen gebruikers problemen melden, vragen stellen of suggesties doen voor nieuwe functies. Pull requests zijn ook welkom om bij te dragen aan de ontwikkeling van de template met concrete code-implementaties of documentatiewijzigingen.

We staan open voor samenwerking en willen graag dat deze template een waardevol hulpmiddel wordt voor organisaties die streven naar naleving van het SURFaudit toetsingskader in een Microsoft cloud-omgeving. Samen kunnen we de template verder verfijnen en aanpassen aan de behoeften van verschillende gebruikers.

Dank bij voorbaat voor uw bijdragen en feedback. We kijken ernaar uit om samen te werken aan de voortdurende verbetering van deze template.

![alt text](./media/Screenshot.policy.png?raw=true "SURFaudit compliancy example")

## Bijdragen

Dit project verwelkomt bijdragen en suggesties. Wanneer je een pull-verzoek indient, zal iemand van de werkgroep bij SURF er naar kijken. Zorg dat je genoeg context over de wijziging toevoegd, zodat we die snel kunnen goedkeuren.

## Implementeren op Azure

| Versie | Implementeer |
|---|---|
| 0.1.0 |[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](./docs/README.md)

## Disclaimer

Deze template dient te worden gezien als hulpmiddel om niveau 3 te bereiken. Onder geen enkele voorwaarde garandeert SURF dat deze template direct leidt tot een volledige compliancy ten aanzien van resources in de Microsoft Azure omgeving.

## Handelsmerken

Dit project kan handelsmerken of logo's bevatten voor projecten, producten of diensten. Geautoriseerd gebruik van Microsoft handelsmerken of logo's zijn onderworpen aan en moeten [Handelsmerk- en merkrichtlijnen van Microsoft](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general) volgen. Het gebruik van handelsmerken of logo's van Microsoft in gewijzigde versies van dit project mag geen verwarring veroorzaken of sponsoring door Microsoft impliceren. Elk gebruik van handelsmerken of logo's van derden is onderworpen aan het beleid van die derden.
