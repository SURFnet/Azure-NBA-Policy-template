# NBA Compliancy initiative template opbouw

De template is opgebouwd door controls NBA die al naar ISO en NIST is gemapped te vergelijken met de Azure policies voor deze compliance frameworks, daarnaast is de NBA gemapped naar controls in de Microsoft Security Baseline. Door deze opzet zullen toekomstige updates die op bestaande Azure policies plaatsvinden makkelijker worden. Het up to date blijven met de nieuwe ontwikklingen en dus ook nieuwe of deprecated policies.

De mapping van de Azure policies die gebruikt voor deze template zijn beschikbaar in [NBA Control Policy mapping excel](./PolicyList.xlsx)


## Implementeren op Azure

Het implementeren van de template kan op 2 niveaus: 
- Op management group niveau; aanbevolen voor Enterprise en grotere implementaties.
- Op subscription niveau; aanbevolen voor testen of kleinere implementaties.

Om de template te implementeren op management group niveau kunnen additionele rechten vereist zijn.
Meer informatie hierover vind u op: [Toegang verhogen](https://docs.microsoft.com/nl-nl/azure/role-based-access-control/elevate-access-global-admin)

| Versie | Doel | Implementeer |
|---|---|---|
| 0.1.0 | Management group level | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSURFnet%2FAzure-NBA-Policy-template%2Fmain%2FARM%2FNBA-azuredeploy-managementgroup.json) |
| 0.1.0 | Subscription level | [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSURFnet%2FAzure-NBA-Policy-template%2Fmain%2FARM%2FNBA-azuredeploy-subscription.json) |

Na de implementatie van de initiative template die deze toegewezen te worden aan een Azure abonnement.
Dit gebeurt automatisch indien gekoppeld door een Management group of handmatig door toewijzing aan een Azure abonnement.

## Toevoegen nalevingsbeleid in Defender for Cloud

Het dashboard voor naleving van regelgeving toont uw geselecteerde nalevingsstandaarden met alle vereisten, waarbij ondersteunde vereisten worden toegepast op toepasselijke beveiligingsevaluaties. De status van deze evaluaties weerspiegelt uw naleving van de standaard.

> ⚠️ Na het toevoegen van initiative template en het koppelen aan de subscriptions kan het tot 24 uur duren voordat deze in het dashboard voor naleving van regelgeving wordt getoond.

Gebruik het dashboard voor naleving van regelgeving om uw aandacht te richten op de hiaten in de naleving van uw gekozen standaarden en voorschriften. Deze gerichte weergave stelt u ook in staat om uw naleving gedurende een periode continu te bewaken binnen dynamische cloud- en hybride omgevingen.

Selecteer naleving van regelgeving in het menu van Defender for Cloud.

Bovenaan het scherm ziet u een dashboard met een overzicht van uw nalevingsstatus en de set ondersteunde nalevingsvoorschriften. U ziet uw algemene nalevingsscore en het aantal door te geven versus mislukte evaluaties die aan elke standaard zijn gekoppeld.

## Implementatie stappen nalevings dashboard

Selecteer een tabblad voor een nalevingsstandaard die voor u relevant is (1). Indien de gewenste standaard niet zichtbaar is klikt u op de 3 punten. 

U ziet op welke abonnementen de standaard wordt toegepast (2) en de lijst met alle besturingselementen voor die standaard (3). 

Voor de toepasselijke besturingselementen kunt u de details bekijken van het doorgeven en mislukken van evaluaties die zijn gekoppeld aan dat besturingselement (4) en het aantal betrokken resources (5). 

Sommige besturingselementen zijn grijs weergegeven. Aan deze besturingselementen zijn geen Evaluaties van Defender for Cloud gekoppeld. Controleer hun vereisten en beoordeel ze in uw omgeving. Sommige hiervan kunnen procesgerelateerd zijn in plaats van technisch.

Meer informatie hierover vind u op: [Uw regelnaleving verbeteren](https://docs.microsoft.com/nl-nl/azure/defender-for-cloud/regulatory-compliance-dashboard) 

## Aandachtspunten
Zoals hieronder is het gebruik van meerdere governance framework een aanrader. Denk aan CIS framework en blijf de Microsoft cloud security benchmark gebruiken omdat deze framework uitgebreide implementatie documentatie heeft ook van controls die niet via een Azure policy te valideren is.

![alt text](../media/Screenshot.governance.png?raw=true "compliancy steps")
