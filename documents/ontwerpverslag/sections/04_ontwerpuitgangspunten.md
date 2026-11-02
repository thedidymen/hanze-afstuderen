# Ontwerpuitgangspunten

Dit hoofdstuk legt de uitgangspunten en randvoorwaarden vast voor de Sign-Up Tool. Het ontwerp is gebaseerd op de bevindingen en de requirements uit het analyseverslag. Het doel van dit hoofdstuk is deze bevindingen te vertalen naar een samenhangende basis voor het functioneel ontwerp, de technische architectuur en de proof of concept (POC).

## Relevante Requirements

De requirements uit de analysefase vormen de basis voor het ontwerp. De MoSCoW-prioritering maakt onderscheid tussen essentiële functionaliteit en functionaliteit die later geïmplementeerd kan worden [@clegg1994]. Het ontwerp adresseert de Must-requirements en neemt daarnaast de Should-requirements mee die de registratieworkflow ondersteunen.

De requirements die het meest relevant zijn voor het ontwerp staan in @tbl:ontwerp-requirements.

| Categorie | Requirements | Ontwerpconsequenties |
|---|---|---|
| Evenementbeheer | FN-ETM-01 t/m FN-ETM-04 | Evenementen, tijdslots en capaciteit moeten configureerbaar zijn. |
| Studentregistratie | FN-SR-01, FN-SR-05, FN-SR-09 | Studenten moeten zich kunnen registreren, hun eigen registratie kunnen bekijken en dubbele registraties moeten worden voorkomen. |
| Functionaliteit voor medewerkers | FN-DRO-02, FN-DRO-04, FN-DRO-05 | Geautoriseerde medewerkers moeten evenementen kunnen configureren en deelnemersoverzichten kunnen bekijken. |
| Coursecontext en overzichten | FN-CON-01, FN-EXP-01, FN-EXP-04 | Evenementen moeten aan een course gekoppeld zijn en deelnemersgegevens mogen alleen toegankelijk zijn voor geautoriseerde gebruikers. |
| Privacy en beveiliging | NF-PS-01, NF-PS-02, NF-PS-03, NF-PS-07, NF-PS-08 | Persoonsgegevens moeten worden geminimaliseerd en toegang moet worden beperkt op basis van bevoegdheden. |
| Architectuur en integratie | NF-MA-01, NF-MA-04, NF-INT-01, NF-INT-02 | De applicatie moet onderhoudbaar zijn en geïntegreerd kunnen worden met Brightspace. |
| Authenticatie en betrouwbaarheid | NF-AUT-01, NF-AUT-02, NF-BDI-01 | Authenticatie, autorisatie en gelijktijdige registraties moeten betrouwbaar worden afgehandeld. |

: Overzicht van relevante requirements {#tbl:ontwerp-requirements}

Het complete overzicht van requirements, de bronnen en de prioritering is vastgelegd in het analyseverslag. Dit verslag legt vast hoe deze requirements worden toegepast, zonder alles uit het analyseverslag te herhalen.

## Functionele en niet-functionele ontwerpdoelen

### Functionele doelstellingen

Het primaire functionele doel is om de bestaande Brightspace Group-tool-workaround te vervangen door een specifiek registratieproces. De huidige situatie is beschreven in het analyseverslag.

Docenten en regisseurs mogen evenementen aanmaken en stellen de beschikbaarheidsperiodes vast voor één of meerdere dagen. Deze periodes worden opgedeeld in tijdslots met een configureerbare duur en capaciteit.

Het planningsproces ondersteunt pauzes en optionele lunchpauzes. De minimale groepsgrootte is niet verplicht, maar de maximale groepsgrootte is een strikte eis voor studenten.

Studenten registreren zich individueel en kunnen normaal gesproken maar één tijdslot per event reserveren. De openings- en sluitingstijd van de registratie en de annuleringsdeadline zijn onafhankelijk in te stellen. Studenten mogen hun tijdslot wijzigen zolang de registratie openstaat, ook na de annuleringsdeadline. Na de annuleringsdeadline kan er niet meer geannuleerd worden.

Docenten en regisseurs kunnen inschrijvingen van deelnemers beheren en indien nodig handmatig de capaciteit van een tijdslot overschrijden. Dit vraagt om een expliciete bevestiging.

Deze beslissingen adresseren FN-ETM-01–09, FN-SR-01–09 en FN-DRO-02–07. De exacte workflows en uitzonderingen worden beschreven in het functioneel ontwerp.

### Niet-functionele doelstellingen

De applicatie beschermt persoonlijke informatie door dataminimalisatie, role-based access control (RBAC) en course-gebaseerde autorisatie. Studenten mogen geen toegang hebben tot de identiteit of registraties van andere studenten (NF-PS-01, NF-PS-02, NF-PS-08).

De tool waarborgt de data-integriteit wanneer meerdere gebruikers tegelijkertijd registreren. Registratiewijzigingen worden atomair verwerkt om inconsistente data en onbedoelde overboeking van een tijdslot te voorkomen (NF-BDI-01).

De tool is uitbreidbaar en onderhoudbaar. De componenten hebben ieder een eigen en duidelijke verantwoordelijkheid, waardoor het mogelijk is om deze onafhankelijk te testen en te vervangen (NF-MA-01, NF-MA-04).

## Technische en organisatorische randvoorwaarden

### Brightspace-integratie

Brightspace is het Learning Management Systeem (LMS) van de Hanze. De Sign-Up Tool moet daarom toegankelijk zijn vanuit de relevante Brightspace-course (NF-INT-01).

LTI 1.3 is geselecteerd als integratiemechanisme. Deze standaard ondersteunt beveiligde communicatie van gebruikersidentiteit, rollen en coursecontext tussen het LMS en een externe tool [@1edtechLtiImplementation]. Brightspace ondersteunt LTI 1.3-registratie en deployment, inclusief de configuratie van informatie die wordt gedeeld met externe applicaties [@d2lLtiAdvantage].

De voorkeursweergave is een geïntegreerde interface binnen Brightspace.

### Technische architectuur

De Sign-Up Tool gebruikt Django, PostgreSQL en server-rendered HTML-templates. Django biedt functionaliteit voor het afhandelen van requests, templates, datamodellen en databasetransacties [@djangoDocumentation].

Daarnaast wordt gebruikgemaakt van de Brightspace UI Web Components, om te zorgen voor een consistente en herkenbare gebruikersinterface [@brightspaceUiCore].

De tool maakt gebruik van een gelaagde architectuur, met een scheiding tussen presentatie, applicatie en data. Deze scheiding sluit aan bij de architectuurkaders van de Hanze [@hanze2026applicatiekader, pp. 9-10].

De Brightspace-integratie is geïsoleerd van de kernlogica. Dit maakt ontwikkeling en testen met een gesimuleerde LTI-context mogelijk, mocht er geen Brightspace-testomgeving beschikbaar zijn.

## Ontwerpprincipes

De volgende principes vormen de basis voor het ontwerp:

1. **Scheiding van verantwoordelijkheden**

   Presentatie, logica en data hebben ieder eigen verantwoordelijkheden, in lijn met de architectuurkaders van de Hanze [@hanze2026applicatiekader, pp. 9-10].

2. **Course-based toegang**

   Evenementen behoren tot een specifieke Brightspace-context. Studenten, docenten en regisseurs hebben alleen toegang tot de functionaliteit en informatie die relevant is voor hun toegestane context (FN-CON-01, NF-AUT-02).

3. **Privacy en security by design**

   Alleen data die nodig is voor registratie en evenementbeheer wordt verwerkt. Autorisatie wordt afgedwongen door de tool. Assessmentresultaten zijn geen onderdeel van de tool (NF-PS-01, NF-PS-03, NF-PS-07).

4. **Data-integriteit**

   Registraties moeten de dataconsistentie waarborgen. De applicatie voorkomt dubbele registraties en onbedoelde capaciteitsoverschrijdingen. Bewuste overschrijdingen door de docent worden apart gelogd en vereisen bevestiging (NF-BDI-01).

5. **Configureerbaar registratieproces**

   Evenementplanning ondersteunt meerdere beschikbaarheidsperiodes, tijdslotduur, capaciteit en pauzes. Het ontwerp vermijdt afhankelijkheden die specifiek zijn voor Verpleegkunde, maar een bredere inzet binnen de Hanze blijft buiten de scope.

6. **Iteratieve ontwikkeling en validatie**

   De implementatie begint met de kernregistratieflow. Aanvullende functionaliteit wordt geselecteerd op basis van de prioriteit van de requirements, de beschikbare tijd en de technische haalbaarheid. Functionaliteit die niet geïmplementeerd of gevalideerd kan worden, wordt gedocumenteerd als beperking.