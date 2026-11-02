# Ontwerpuitgangspunten

Dit hoofdstuk legt de uitgangspunten en randvoorwaarden vast voor de Sign-Up Tool. Het ontwerp is gebaseerd op de bevindingen en de requirements uit het analyseverslag. Het doel van dit hoodstuk is deze bevindingen de vertalen naar een samenhangende basis voor het functioneel ontwerp, technische architectuur en proof of concept (POC).

## Relevante Requirements

De requirements uit de analyse fase geven de basis voor het ontwerp. De MoSCoW prioritizering geven het onderscheid tussen essentiele functionaliteit en functionaliteit dat later geimplmenteerd kan worden [@clegg1994]. Het ontwerp addressseert de Must-requirments, daarnaast implementeer het ook de Should-requirement die de registratieworkflow ondersteuenen. 

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

Het complete overzicht van requirements, de bronnen en prioritisering is vastgelegd in het analyseverslag. Dit verslag legt vast hoe deze requirements toegepast worden, zonder alles te herhalen uit het anaylyse verslag. 

## Functionele en niet-functionele ontwerpdoelen

### Functionele doelstellingen

Het primary functionele doel is om de bestaand Brightspace Group-tool workaround te vervangen met een toegewijd registratie proces. De huidige situatie is beschreven in het analyseverslag. 

Docenten en regisseurs mogen evenementen aanmaken en stellen de beschikbaarheid periode vast over 1 of meer dagen. Deze periodes zijn opgedeeld in registratie vakkken met een configureerbare duur en capaciteit. 

Het plannings proces ondersteunt pauzes en mogelijk lunchpaze. De minimum groepsgrote is niet verplicht, maar de maximum grote is een strikte eis voor studenten. 

Studenten registreren individueel en kunnen normaal maar 1 tijdslot claimen per event. Registratie opening, sluiting en annuleringsdeadline zijn onafhankelijk in te stellen. Studenten mogen hun tijdslot wijzigen zolang de registratie open staat, ook na de annuleringsdeadline. Na de annuleringsdealine kan er niet meer geannuleerd worden. 

Docenten en regisseurs kunnen inschrijvingen van deelnemers beheren en handmatig de capaciteit van een tijdslot overschrijven, indien nodig. Dit vraagt om een expliciete bevestiging.

Deze beslissingen addresseren FN-ETM-01–09, FN-SR-01–09 en FN-DRO-02–07. De exacte workflows en uitzonderingen worden beschreven in het functioneel ontwerp

### Niet functionele doelstellingen

De applicatie beschermt personlijke informatie door dataminimalisatie, role-based acces control (RBAC) en course-gebaseerde authorisatie. Studenten moeten geen toegang hebben tot de indentiteiten of registraties van andere studenten (NF-PS-01, NF-PS-02, NF-PS-08). 

De tool waarborgt de data integriteit zodra meerder gebruikers tegelijkertijd registreren. Registratieveranderingen worden atomair verwerkt, ter voorkoming van inconsistente data en overboeken van een tijdslot (NF-BDI-01).

De tool is uitbreidbaar en onderhoudbaar. De componenten hebben ieder een eigen en duidelijke verantwoording, waardoor het mogelijk wordt om deze te vervangen en onafhankelijk te testen (NF-MA-01, NF-MA-04). 

## Technische en organisatorische randvoorwaarden

### Brightspace integratie

Brightspace is het Learning Management Systeem (LMS) van de Hanze. De Sign-Up Tool moet daarvoor dus toegankelijk zijn vanuit de relevante Brightspace course (NF-INT-01). 

LTI 1.3 is geselecteerd als integratie mechanisme. Deze standaard ondersteunt beveiligde communicatie van gebruikerindentiteit, rollen en course context tussen het LMS en een externe tool [@1edtechLtiImplementation]. Brightspace ondersteunt LTI 1.3 registratie en deployment, inclusief configuratie van de informatie die wordt gedeeld met externe applicaties [@d2lLtiAdvantage]. 

De geprefereerde presentatie is een geintegreerde interface in Brightspace. 

### Technische architectuur

De Sign-Up Tool gebruikt Django, PostgreSQL en server-rendered HTML templates. Django geeft de functionaleit voor requests, templates, data modelen en database transacties [@djangoDocumentation].

Daarnaast wordt er gebruikgemaakt van de Brightspace UI Web Components, om te zorgen voor een consistente en bekende gebruikersinterface [@brightspaceUiCore].

De tool maakt gebruik van een gelaagde architectuur, hierin is een scheiding van presentatie, applicatie en data. Deze scheiding sluit aan bij de architectuurkaders van de Hanze [@hanze2026applicatiekader, pp. 9-10].

De Brightspace integratie is geisoleerd van de core logica. Dit laat ontwikkeling en testen met een gesimuleerde LTI context toe, mocht er geen Brightspace test omgeving zijn. 

## Ontwerpprincipes

De volgende principes vormen de basis voor het ontwerp:

1. Seggregatie van verantwoordelijkheden

Presentatie, logica en data hebben eigen verantwoordelijkeheiden, in lijn met de architectuurkaders van de Hanze [@hanze2026applicatiekader, pp. 9-10].

2. Course-based toegang

Evenementen behoren tot een specifieke Brightspace-context. Studenten, docenten en regisseurs hebben alleen toegang to de functionalitei en informatie die relevant is voor hun toegestane context (FN-CON-01, NF-AUT-02).

3. Privacy en security by design

Alleen data nodig voor registratie en evenement management is verwerkt. Authorisatie is afgedwongen door de tool. Assesment restultaten zijn geen onderdeel van de tool (NF-PS-01, NF-PS-03, NF-PS-07).

4. Data integriteit

Registraties preserveren data consistentie. De applicatie voorkomt dubbele registraties en capaciteit overschreidingen. Intentionele overschrijdingen door de docent worden apart gelogd en vereisen bevestiging (NF-BDI-01).

5. Configureerbaar registratie proces

Evenement planning ondersteunt meerdere beschikbaarheid periodes, tijdslotduur, capaciteit en pauzes. The ontwerp vermijdt afhankelijkheden die verpleegkunde specifiek zijn, echter blijft een bredere Hanze inzet buiten scope. 

6. Iterative ontwikkeling en validatie

De implementatie begint met een core registratie flow. Additionele functionaliteit is geselecteerd op de requirments prioriteit, beschikbare tijd en technische haalbaarheid. Features die niet geimplmenteerd of gevalideerd kunnen worden, worden gedocumenteerd als beperking. 