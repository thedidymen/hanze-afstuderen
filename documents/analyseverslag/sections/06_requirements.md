# Requirements

## Inleiding

Dit hoofdstuk stelt de requirement van de Sign-Up tool vast. Deze requiremente beschrijven wat de toekomstige oplossing moet ondersteunen en aan welke kwaliteitsiesen voldaan moet worden. Binnen dit hoofdstuk wordt nog geen oplossingsrichting gekozen, dit doen we in latere hoofdstukken. 

De requirements zijn gebaseerd op de analyse van de huidige situatie, de stakeholder analyse en de interview transscripties. De initiele use case is het registreren van events bij Verpleegkunde, echter op langere termijn moet deze tool breed inzetbaar zijn binnen de Hanze. 

## Verkrijgen van Requirements

De requirements zijn verkregen uit de stakeholder interviews en de project docuementen. De interview zijn gebruikt om de huidige problemen, gebruikers behoeften, organisatorische beperkingen en risico's. Deze bevindingen vertalen zich in deze requirements. 
De requirement zijn geen letterlijke overzetting van de stakeholder gesprekken. Opmerkingen als: "studenten kunnem momenteel zien wie er geregistreed is in een tijdslot" vertaalt zich naar een privacy requirement: dat studenten alleen hun eigen registratie en algemene beschikbaarheid van het tijdslot mogen zien. 

Deze bronnen zijn gebruikt voor de requirement analyse:
- Vepleegkunde interview (VI), 2 maart 2026, bijlage A.
- BS&IT interview (BII), 2 maart 2026, bijlage B.
- Privacy & Security interview (PSI), 13 april 2026, bijlage C.
- Technische Kaders interview (TKI), 20 april 2026, bijlage D.
- HIP interview (HI), 11 mei 2026, bijlage E.
- Brightspace interview (BI), 1 juni 2026, bijlage F.

## Scope en Aannames

De scope van de requirement is het sign-up proces voor educationele momenten zoals praktische assesments, herexamens (praktisch), workshops of vergelijkbare activiteten waar studenten een specifiek moment moeten reserveren. De oplossing dient het proces van Verpleegkunde te ondersteunen, zonder verpleegkunde specifieke ontwerp keuzes te maken zodat er een hanze brede oplossing onstaat.

Binnen dit hoofdstuk zijn de volgende aanames gemaakt:
- Brighspace blijft de hoofd applicatie waarmee studenten en docenten interacteren met de course. 
- De sigh-up tool ondersteunt planning en registratie, geen cijfers of resultaten verwerkging. 
- De MVP richt zich op de sign-up workflow voordat integraties met planning, adminitratie system etc. worden toegevoegd. 
- Requirements die gericht zijn op toekomstige koppelingen worden als laag-prio of open requirements toegevoegd en zijn geen onderdeel van de MPV scope

## Gebruikersgroepen en Rollen

De volgende gebruikersgroepen en rolen zijn gebruikt in de requirements. Deze rollen zijn niet hetzelfde als de organisatorisch stakeholders. Ze beschrijven hoe gebruikers interacteren met het system, en welke informatie en acties gebruiken (zie {#tbl:roles}). 

| Rol | Beschrijving |
|---|---|
| Student | Registreerd voor event in Sign-up tool en kan eigen registratie bekijken |
| Docent | Gebruikt deelnemers overview ter voorbereiding en afname van assesments |
| Regiseur | Prepareerd Sign-up events |
| Functioneel Manager | Ondersteunt de applicatie |
| Technisch Manager | Onderhoud, en geeft technische ondersteuning |
| Brightspace Engineer | Ondersteun intergratie Brightspace |
| Privacy & Security | Reviewed de verwerking van persoonlijke data, toegang en logging |

: Rollentabel {#tbl:roles}

## Functionele Requirements (FN)

### Event en Tijdslotmanagement (ETM)

#### FN-ETM-01 - Creer Sign-up events

Requirements: Het systeem laat geauthoriseerde werknemers sign-up events creeren. 
Bron: VI: ~1-4 min;
Stakeholders: regisseur, docenten, functioneel manager, studenten
Uitleg: Het huidige proces laat werknemers handmatig Brightspace groepen aan maken voor elk registratie moment. De vervangingde oplossing dient dit direct te kunnen doen. 


#### FN-ETM-02 - Vastlegen meta data

Requirements: Het system laat werknemers basis informatie vastleggen: naam, datum, tijd, locatie, docent, course of module
Bron: VI: ~2, ~10 min;
Stakeholders: Regisseur, docenten, functioneel manager, studenten
Uitleg: In de huidig workflow worden datum, tijd en locatie vastgelegd in de groepnaam. Binnen de oplossing moet deze informatie als gestructureerde data worden vast gelegd. 

#### FN-ETM-03 - Gereserveerd tijd opdelen in tijdslots

Requirements: Het syteem laat medewerkers de gereserveerde tijd opdelen in meerdere registratie momenten. 
Bron: VI: ~10 min, BI ~6-8 min
Stakeholders: Regisseur, docenten, studenten
Uitleg: De kern van het probleem is niet alleen het toekennen van de totale tijd, maar ook het opdelen in registratie momenten. 

#### FN-ETM-04 - Variable capaciteit binnen een tijdslot

Requirements: Binnen een tijdslot mag er door een range van studenten ingeschreven worden, bv 3-5 per registratie. 
Bron: VI: ~0-3 min, BI ~6 min. 
Stakeholders: Regiseur, docenten, studenten
Uitleg: Binnen het huidige system laat geen makkelijke variatie toe, terwijl 1, meerdere en een range van studenten wenselijk is. 

#### FN-ETM-06 - Markeer pauze als niet registreerbaar

Requirements: De Docenten moeten een pauze kunnen nemen, in deze momenten kunnen studenten dus niet registreren. 
Bron: VI: ~8 min, BI ~7 min.
Stakeholders: Regisseur, docenten, studenten
Uitleg: Assesment block kunnenv meerdere uren duren. Het moet mogelijk zijn voor docenten om een pauze te nemen. 

#### FN-ETM-07 - De registratie moet een open en sluit moment kennen

Requirements: De registratie moet op vooraf tijdstip geopend en gesloten kunnen worden. 
Bron: VI: ~15 min.
Stakeholders: Regisseur, docenten, studenten
Uitleg: Er is een explicite vraag om het registreren te stoppen op een vooraf bepaald tijdstip. 

#### FN-ETM-08 - De registratie kent een annulerings deadline

Requirements: Er moet een annulering deadline, los van de registratie deadline komen (FN-SR-02).
Bron: VI: ~15 min.
Stakeholders: Regisseur, docenten, studenten
Uitleg: Studenten mogen registreren tot de registratie deadline, echter mogen studenten niet meer annuleren na de annulerings deadline.

#### FN-ETM-09 - Tijdslot status laten zien

Requirements: De status van een tijdslot moet zichtbaar zijn (Beschikbaar, Gedeeltelijk Beschikbaar, Vol, Niet Beschikbaar)
Bron: VI: ~0, ~3 min, BI ~10-11 min.
Stakeholders: Regisseur, docenten, studenten. 
Uitleg: Studenten en docenten moeten weten of een slot nog beschikbaar is/het aantal beschikbare plekken kunnen monitoren. 

#### FN-ETM-10 - Maak tijdslots van geimporteerde plannings data.  

Requirements: Het system zou op basis van gestructureerde planning data, bv excel sheet, tijdslots kunnen genereren, wanneer een directe integratie niet mogelijk/beschikbaar is. 
Bron: VI ~3 min, ~10 min.
Stakeholders: Regisseur, functionele manager, docenten. 
Uitleg: Het huidige proces begint met planning informatie ontvangen van uit Excel. Importeren van deze structurele data zou een reductie in handmatige stappen betekenen. 

#### FN-ETM-11 - Terugkeerende of herbruikbare events structuren

Requirements: Het systeem ondersteunt hergebruik, kopieren of hercreeren van voorgaande events voor nieuwe studiejaren. 
Bron: VI: ~1 min, ~12-14 min.
Stakeholders: Regisseur, docenten, functioneel manager.
Uitleg: Binnen het huidige proces vinden events elkaar plaats. Hergebruik reduceer het aantal handmatige stappen. 

#### FN-ETM-12 - Rollende uitgave van tijdslots

Requirements: Het system ondersteun een rollende vrijgave van tijdslots, zodat er geen of weining gaten in het rooster van de docent onstaan. 
Bron: VI: ~16 min
Stakeholders: Regisseur, docenten, studenten. 
Uitleg: Een rollende vrijgave van tijdslots voorkomt inefficiente verdeling van tijdslots over de dag. Niet een kern requirement. 


### Student Registratie

#### FN-SR-01 - Registreren voor een tijdslot

Requirements: Studenten moet zich kunnen registreren voor een tijdslot
Bron: VI: ~0 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Het zelf registreren is het centrale doel van de Sign-up tool en vervangt de huidige Brightspace groep registratie. 

#### FN-SR-02 - Deregistratie voor annulerings deadline.

Requirements: Student moet zichzelf kunnen deregistreren voor de ingestelde annulerings deadline (FN-ETM-08).
Bron: VI: ~0 min, ~15 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Het huidige proces laat studen deregistreren indien foutief ingeschreven. 

#### FN-SR-03 - Voorkom deregistratie na annulerings deadline

Requirements: Voorkomen van deregistratie na de ingestelde annulerings deadline. 
Bron: VI: ~15 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Late annulering moet tellen als een gemiste kans. 

#### FN-SR-04 - Wijzigen van registratie

Requirements: Studenten kunnen hun registratie annuleren en daarmee wijzigen binnen de annulerings regels. 
Bron: VI: ~0 min, ~15 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Binnen de regels is het wijzigen van een tijdslot toegestaan. 

#### FN-SR-05 - Eigen registratie bekijken

Requirements: Studenten kunnen de eigen registratie inzien zonder die van andere studenten te zien. 
Bron: VI: ~3 min, ~6 min, PSI: ~4 min.
Stakeholders: Regisseur, docenten, studenten, privacy en security.
Uitleg: Er is voor studenten geen reden om gegevens van andere studenten in te kunnen zien. 

#### FN-SR-06 - Beschikbaarheid is zichtbaar

Requirements: Voor studenten moet het zichtbaar zijn hoeveel ruimte er is in een tijdslot, zonder te zien wie er in zitten. 
Bron: VI: ~2-3 min,  ~6 min, HI: ~21 min, BI: ~10-11 min.
Stakeholders: Regisseur, docenten, studenten, privacy en security.
Uitleg: Binnen de huidige situatie is zichtbaar wie zich voor welk slot heeft geregistreert. Studenten hoeven deze informatie niet te zien. 

#### FN-SR-07 - Sign-up events alleen zichtbaar mits relevant.

Requirements: Het sign-up event moet alleen zichtbaar zijn voor de student mits deze relevant is voor de te volgen courses/modules
Bron: VI: ~14 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Alleen releveante informatie moet zichtbaar zijn. Dit zal ook een requirement zijn voor gebruik door andere schools binnen de Hanze.

#### FN-SR-08 - Note or comment by studens

Requirements: Studenten kunnen een comment achterlaten, mits deze functie is aangezet door de docent/regisseur.
Bron: VI: ~4 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Het huidige systeem staat geen comments toe, dit is als beperkend aangekaart. De behoefte dient gevalideerd te worden voordat dit onderdeel wordt van het MVP.  

#### FN-SR-09 - Voorkom duplicate registratie

Requirements: Studenten kunnen zich maar 1 keer registreren, tenzij anders geconfigureerd. 
Bron: VI: ~0-3 min, ~15 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Duplicate registraties ondermijnen de capaciteits management en planning. 

### Docent en Regiseur Overzicht

#### FN-SR-09 - XXX

Requirements: 
Bron: VI: ~0-3 min, ~15 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg:

### Exports

### Configuratie

## Niet Functionele requirements

### Privacy & Security

### Onderhoudbaarheid

### Integratie

### Authenticatie en Authorisatie

## Priorisatie Requirements

### Methode

### MoSCoW 

## Conclusie