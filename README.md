# SURFaudit AZURE Policy template

> As this project is specific for the Dutch education and research institutions the rest of this article will be in Dutch.


Dit SURF project omvat een Initiative Policy Template, welke ingeladen kan worden in Microsoft Azure. In combinatie met Defender for Cloud kan men Azure resources auditen. Het is toepasbaar op alle PaaS en IaaS diensten binnen Azure. Het omvat algemene checks, en checks gebaseerd op bestaande Azure, Linux, Docker, en Kubernetes baselines, gelinkt aan de verschillende controls van het SURFaudit toetsingskader.  

Deze template is het startpunt om niveau 3 van het [SURFaudit toetsingskader](https://www.surf.nl/surfaudit-toetsingskader-beoordeel-je-informatiebeveiliging) te halen in een Microsoft cloud omgeving. De template kan worden aangepast aan de eisen en wensen van een specifieke organisatie. De template omvat uitsluitend technische controls. Procesmatige controls dienen binnen de organisatie ingevoerd te worden om volledig tot niveau 3 te komen. Alle policies zijn van het type 'audit' of 'deny' en allen zijn ingesteld op 'audit'. 

Periodiek zal deze template worden geupdate met nieuwe policies en/of aanpassingen de focus ligt dan op deprecated policies en/of nieuwe policies die in de Microsoft Security Baseline zijn toegevoegd en ook van toepassing zijn op de SURFaudit controls. Zie hiervoor het update process.

## Aandachtspunten
1. **Kosten**: Bepaalde technische controls, zoals de check op Microsoft Defender for Cloud, suggereren een mitigatie die extra kosten met zich meebrengt. Alle technische controls zijn ingesteld op 'audit' en er zijn geen 'deploy if not exist' policies, waardoor dit nooit automatisch zal gebeuren. *Het SURFaudit toetsingskader schrijft in geen geval specifieke tooling voor* om aan een bepaald niveau te voldoen. Het is dus goed mogelijk om andere tooling buiten de (betaalde) functionaliteiten van Azure te gebruiken en toch te voldoen. In dat geval kan je de control handmatig op groen zetten.
2. **Azure Landing Zone**: Het wordt aanbevolen om ook de [Azure Landing Zone architectuur](https://aka.ms/alz) te volgen om een solide basis te hebben voor een veilige Azure-omgeving. Deze template moet gebruikt worden in combinatie met een ALZ-implementatie, ALZ bevat ook afdwingingsbeleid, zoals 'deny', 'deploy if not exist', enz. Binnen de management group-structuur kan ervoor gekozen worden om onderscheid te maken tussen landing zones voor IT en bijvoorbeeld landing zones voor onderzoek, met afwijkende beleidsregels, en of afwijkende data clasificatie om zo bijvoorbeeld encryption met customer managed keys te auditten danwel af e dwingen. Dit kan met dit initiatief te deployen op lagere management group nivo inclusief verschillende geparametriseerde implementaties van deze technische Azure controls.
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

Als je snel wilt zien of je compliant bent, dan kun je vervolgens de volgende stappen volgen:
* Log in op de [Azure portal](https://portal.azure.com)
* Zoek naar Policy en klik hierop
* Op de pagina zie je een eerste overzicht van de toegekende policies en hun top-level status
* Klik op de [Preview] SURFaudit ... Policy, om in te zoomen op deze policy.
* Nu zie je op Control niveau of je compliant bent of niet
* Klik op een control en vervolgens op Policies om de policies te zien die onder deze control vallen en hun compliancy
* Klik vervolgens op de Policy om de resources te zien die al dan niet compliant zijn


## Disclaimer

Deze template dient te worden gezien als hulpmiddel om niveau 3 te bereiken. Onder geen enkele voorwaarde garandeert SURF dat deze template direct leidt tot een volledige compliancy ten aanzien van resources in de Microsoft Azure omgeving.

## Handelsmerken

Dit project kan handelsmerken of logo's bevatten voor projecten, producten of diensten. Geautoriseerd gebruik van Microsoft handelsmerken of logo's zijn onderworpen aan en moeten [Handelsmerk- en merkrichtlijnen van Microsoft](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general) volgen. Het gebruik van handelsmerken of logo's van Microsoft in gewijzigde versies van dit project mag geen verwarring veroorzaken of sponsoring door Microsoft impliceren. Elk gebruik van handelsmerken of logo's van derden is onderworpen aan het beleid van die derden.
