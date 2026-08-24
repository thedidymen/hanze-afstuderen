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

Requirements: Binnen een tijdslot is de capaciteit configureerbaar. 
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
Stakeholders: Regisseur, functionel manager, docenten. 
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
Uitleg: Het huidige proces laat studen deregistreren indien foutief ingeschreven. Late annulering moet tellen als een gemiste kans.

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

To do: uitzoeken hoe de structuur binnen brightspace werkt. Module => Course => studenten / Module => Course => klas/docent => studenten / of nog iets anders... waar werkt de Sign-Up tool? course niveau / klas niveau

#### FN-DRO-01 - Samenvatten deelnemers overzicht

Requirements: De tool moet een overzicht geven van de registreerde studenen voor het event
Bron: VI: ~1 min, ~3-4 min, ~6 min.
Stakeholders: Regisseur, docenten.
Uitleg: Docenten moeten binnen brightspace elke groep openen om te zien wie er geregistreerd hebben. Een samenvatten overzicht helpt met de voorbereiding. 

#### FN-DRO-02 - Groepsindeling overzicht op basis van tijdslot

Requirements: De tool moet een overzicht geven van alle tijdslots, inclusief geregistrede studenten en resterende capaciteit
Bron: VI: ~3-6 min, ~13-14 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Docenten moeten weten welke studenten wanneer komen, niet alleen de deelnemers lijst. 

#### FN-DRO-03 - Event beschrijving

Requirements: De tool geeft ruimte voor voorbereidings informatie voor studenten, zoals de activiteit, eisen of andere status informatie die nodig is. 
Bron: VI: ~3-4 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Docenten willen weten welk assesment een student doet en of de requirements, zoals een vaardighedenkaart aan zijn voldaan. 

To do: uitzoeken wie hier iets moet doen... eisen van uit de docent of invul oefening vanuit de student?

#### FN-DRO-04 - Setup van een event

Requirements: De regisseur/functioneel manager/docent moet event kunnen opzetten zonder technische hulp. 
Bron: VI: ~4-6 min.
Stakeholders: Regisseur, docenten.
Uitleg: Er moet geen externe afhankelijkheid zijn om events te kunnen opzetten. 

#### FN-DRO-05 - Overview van alle deelnemers van een event

Requirements: Geauthoriseerde docenten moeten alle deelnemers van een event kunnen inzien, als die nodig is voor de uitvoering van het assesment
Bron: VI: ~6 min, PSI: ~4 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security.
Uitleg: Docenten kunnen een assesment uitvoeren voor collega's en hebben daarmee een event level overview nodig en niet alleen hun eigen studenten. 

To do: Zie hier boven, uitzoeken wat hier nu echt de functionele eis is. 

#### FN-DRO-07 - Handmatige registratie studenten

Requirements: Docenten/regisseurs kunnen handmatig een student registreren voor een event of tijdslot
Bron: VI: ~12-14 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security.
Uitleg: Studenten moeten handmatig kunnen toegevoegd worden. Ter ondersteuning van uitzonderlijke zaken waar zelfregistratie niet toereikend is. 

#### FN-DRO-08 - Bulk registratie studenten

Requirements: Studenten moeten in bulk geregistreerd kunnen worden voor operationele efficentie
Bron: VI: ~3 min, ~10 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Bulk registratie maakt het process veel sneller.

To do: uitzoeken hoe dit zou moeten werken. Brightspace quicklist, of een excel toevoegen?

#### FN-DRO-09 - Bewerk en verwijder events

Requirements: Event moet bewerken en verwijdert worden, maar met safeguard voor open registraties
Bron: ? assignment brief
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Regisseurs en docenten moeten een event kunnen opzetten, bewereken en verwijderen. De implementatie moet wel safeguards hebben zodra er registraties zijn voor een event. 

To do: bron vaststellen, safeguard uitwerken.

#### FN-DRO-10 - Manage event status

Requirements: Regiseurs en docenten moeten de status van een event kunnen veranderen, zoals: voorlopige versie, open, gesloten, archief. 
Bron: VI: ~15 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Explicite statusen maken de levencycle van het event duidelijk en begrijpbaar. 

### Exports

To Do: Dubbelen met vorig groep?

#### FN-EXP-01 - Genereer deelnemers lijst

Requirements: Docenten en regisseurs mogen deelnemerlijsten genereren. 
Bron: VI: ~1 min, ~3-4 min.
Stakeholders: Regisseur, docenten.
Uitleg: Voor de voorbereiding en uitvoer van een event mogen docenten deelnemerlijsten maken. 

#### FN-EXP-02 - Filter deelnemers list per event, datum of docent

Requirements: Deelnemerlijsten kunnen gefilterd worden op event, datum, docent (tijdslot?)
Bron: VI: ~3-4 min, ~13-14 min.
Stakeholders: Regisseur, docenten.
Uitleg: Docenten moeten weten wie, wanneer, op welke dag (voor welk event) komen, ipv 1 platte lijst.

#### FN-EXP-03 - Ondersteun export of printbare versie

Requirements: Er moet een export of printbare versie te maken zijn van de lijst. 
Bron: VI: ~1 min, ~3-4 min, ~10 min.
Stakeholders: Regisseur, docenten.
Uitleg: De huidige workflow maakt gebruik van Excel en handgemaakte lijsten. Een uitdraai helpt de docenten gebruik te maken van het schema buiten de tool. 

#### FN-EXP-04 - Beperk data export tot het minimum 

Requirements: De geexporteerde data moet compleet, functioneel en minimaal zijn voor de doeleinden waarvoor het wordt gebruikt. 
Bron: VI: ~2 min, PSI: ~8 min, ~32-33 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: De deelnamelijst bevat personlijke data van studenten, een export moet de data minimaliseren. 

### Configuratie

#### FN-CON-01 - Koppelen aan programma en course context

Requirements: Events moeten gekopppeld worden aan een programma, course, klas of andere relevante context.
Bron: VI: ~14 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Studenten moeten alleen toegang krijgen tot relevante evenementen. Er dient een logische scheiding te zijn tussen programmas. 

#### FN-CON-02 - Evenementen hebben een default setting

Requirements: Een evenement heeft defaults settings die configureerbaar zijn, zoals slot lengte, capaciteit, annulerings deadline en zichtbaarheid. 
Bron: VI: ~10-16 min.
Stakeholders: Regisseur, docenten.
Uitleg: Het opzetten van een evenement is repetatief werk. Het instellen van defaults reduceert handmatige setup. 

To Do: is het uitschrijven van instelbare settings niet handiger? Mist dat niet?

#### FN-CON-03 - Role based toegang

Requirements: Toegang tot de tool wordt gebaseerd op de gebruikers role, zoals regisseur, docent, student, beheerder
Bron: VI: ~4-6 min, PSI: ~4 min.
Stakeholders: Regisseur, docenten, studenten, beheerder.
Uitleg: Verschillende rollen hebben verschillende functionaliteit en zichtbaarheid. Role configuratie is vereist voor de ondersteuning van gebruik en privacy.

To Do: Deze moet beter worden uitgewerkt. Check de bronnen. 

#### FN-CON-04 - Ondersteun generiek gebruik van de Tool

Requirements: De tool moet generiek te gebruiken zijn. 
Bron: VI: ~2 min, PSI: ~8 min, ~32-33 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: De tool moet voorkomen dat het Verpleegkunde specifieke workflow ondersteunt. Het ontwerp voor de tool is generiek en kan Hanze breedt processen ondersteunen.  

#### FN-CON-05 - Scheiding tussen verschillende schools

Requirements: De tool ondersteunt een logische scheiding tussen schools, courses.
Bron: VI: ~11 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: Er is een duidelijke scheiding tussen schools, courses binnen de tool.

To do: waarin verschilt deze requirement van FN-CON-01

## Niet Functionele requirements

### Privacy & Security

#### NF-PS-01 - Dataminimalisatie

Requirements: De tool moet alleen data verwerken en opvragen die noodzakelijk is voor het sign-up process.
Bron: PSI: ~8 min, ~32-33 min. 
Stakeholders: Docenten, studenten, privacy & security, functioneel manager.
Uitleg: Door dataminimalisatie neemt het risico op een privacy en security risco's af.

To do: Verpleegkunde noemt deze requirement ook... waar?

#### NF-PS-02 - Alleen eigen registratie zichtbaar

Requirements: De tool laat alleen de eigen registratie zien. Studenten krijgen geen inzicht in d e registraties van andere studenten. 
Bron: VI: ~2 min, ~6 min, PSI: ~4-8 min, HI: ~21 min.
Stakeholders: Docenten, studenten, privacy & security, functioneel manager.
Uitleg: Binnen de huidige tool kunnen studenten de registratie informatie van andere studenten inzien. Dit is een privacy probleem. 

#### NF-PS-03 - De tool registreert geen beoordelings data

Requirements: De tool registeerd geen geen cijfers of beoordelingen. 
Bron: PSI: ~4-8 min, HI: ~19-21 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.
Uitleg: Becijfering gebeurt binnen de bestaande tooling en maakt geen onderdeel uit van deze tool. 

#### NF-PS-04 - Documenteer data flows

Requirements: Data flows binnen de applicatie moeten worden gedocumenteerd. 
Bron: PSI: ~8 min, ~32-33 min.
Stakeholders: Privacy & security, BS&IT, functioneel management, technisch management.
Uitleg: Dataflows van persoonsgegeven dient inzichtelijk te zijn. 

#### NF-PS-05 - Privacy Quickscan

Requirements: Het project dient een privacy quickscan te doen. 
Bron: PSI: ~32-33 min.
Stakeholders: Privacy & security, BS&IT, Verpleegkunde.
Uitleg: Het project dient een privacy quickscan te doen voordat echte personlijke data door de tool word gebruikt.

To do: Stakeholderlijst checken of we deze zo willen uitbreiden. 

#### NF-PS-06 - Verwerkingsovereenkomst indien gebruik externe partij

Requirements: Bij verwerking van persoonlijke data door een externe partij dient er een verwerkingsovereenkomst opgesteld te worden. 
Bron: VI: PSI: ~8 min, ~32 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.
Uitleg: Om te voldoen aan de AVG dient er een verwerkingsovereenkomst opgezet te worden voor de verwerking van persoonlijke data. 

#### NF-PS-07 - Security-by-design

Requirements: De Sign-up tool dient ontworpen te worden volgens het Security-by-design principe.
Bron: PSI: ~10 min.
Stakeholders: Privacy & security, functioneel manager, technisch manager.
Uitleg: Security (en privacy) dienen door het hele process heen mee genomen te worden. Hierbij moet gekozen worden voor de veiligste praktische default. 

#### NF-PS-08 - Least privilege

Requirements: De tool geeft gebruikers alleen permissies die nodig zijn voor het uitvoeren van hun rol en taak. 
Bron: VI: ~4-6 min, PSI: ~10 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.
Uitleg: De tool behandels personlijke data en verschillende rollen en taken vereisen een verschillende zichtbaarheid. Least privilege reduceert privacy en security risico. 

#### NF-PS-09 - Data retentie en verwijderings regels

Requirements: De Sign-up tool moet vastleggen hoelang registratie data bewaard wordt en wanneer het wordt verwijderd of gearchiveerd. 
Bron: PSI: ~32-33 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.
Uitleg: De tool verwerkt personlijke data. Regels zijn nodig om te zorgen voor doelbinding en ter voorkoming van onnodige opslag.

### Onderhoudbaarheid

#### NF-MA-01 - Onderhoudbaar en breed gedragen technology

Requirements: De technische oplossing moet gebruik maken van breed gedragen technieken. 
Bron: BII: ~6-8 min, TKI: ~7-9 min, HI: ~3-6 min.
Stakeholders: BS&IT, technisch manager, collabspace.
Uitleg: De benodigde kennis en kunde om de applicatie te onderhouden moet op breed gedragen technologien gebaseerd zijn. Hiermee moet de applicatie makkelijk overdraagbaar zijn en het onderhoud geen specialisisch kennnis vereisen. 

To Do: stakeholders?

#### NF-MA-02 - Eigenaarschap en onderhoud

Requirements: Voordat de oplossing operationeel wordt, is duidelijk waar het eigenaarschap en het onderhoud van de applicatie ligt.
Bron: BII: ~2-5 min, HI: ~3-6 min.
Stakeholders: BS&IT, HIP, technisch manager.
Uitleg: BS&IT en HIP benoemen continuiteit, eigenaarschap en onderhoud als een kritisch punt tijdens de transitie van poc naar producttie. 


#### NF-MA-04 - Scheiding van presentatie, integratie, data.

Requirements: De architectuur van de Sign-up tool maakt een scheiding tussen presentatie-, integratie- en de data-laag.
Bron: BII: ~11 min, architectuurkaders.
Stakeholders: BS&IT, HIP, technisch manager.
Uitleg: De scheiding van lagen maakt de applicatie beter te onderhouden en te beveiligen. Daarnaast dwingt de scheiding tot expliciete keuzes tav verwerking en opslag. 

To Do: architectuurkaders uitzoeken. 

#### NF-MA-05 - Code review en QA

Requirements: Het development proces zou code reviews en kwaliteits controlles moeten faciliteren voordat het in productie gaat. 
Bron: BII: ~2-6 min, HI: ~3-5 min.
Stakeholders: BS&IT, HIP, technisch manager.
Uitleg: Code review en kwaliteitscontrole verkleinen de kans op fouten en zorgen voor technisch verantwoorde keuzes. Daarnaast helpt dit met kennisdeling, consistente code en onderhoudbaarheid. 

#### NF-MA-06 - Documenteer technische keuzes

Requirements: Groote technische keuze moeten gedocumenteerd en beargumenteerd worden. 
Bron: BII: ~6-8 min.
Stakeholders: BS&IT, HIP, technisch manager.
Uitleg: Technische keuze dienen onderbouwt te worden.

### Integratie

#### NF-INT-01 - Sign-up tool toegankelijk vanuit Brightspace

Requirements: De Sign-up tool moet toegankelijk zijn vanuit de relevante Brightspace content. 
Bron: VI: ~6-7 min, BI: ~10-14 min.
Stakeholders: Regisseur, docenten, studenten, Brightspace engineers.
Uitleg: Brigthspace is de LMS vanuit de Hanze die studenten en docenten gebruiken om het onderwijs digitaal aan te bieden. 

To Do: Stakeholder: Brightspace engineers. 

#### NF-INT-02 - Gebruik het Brightspace intergratie mechansime

Requirements: De oplossing gebruikt een goedgekeurde Brightspace integratie mechanisme. Als toepasbaar kan de LTI 1.3 / LTI Advantage gebruikt worden om veilig de geauthenticeerde gebruiker en course context op te halen. 
Bron: BI: ~10-14 min, ~19-20 min.
Stakeholders: Regisseur, docenten, studenten, Brightspace engineers, technisch manager.
Uitleg: LTI is het brightspace mechanisme om een externe applicatie te integreren binnen Brightspace. 


### Authenticatie en Authorisatie

#### NF-AUTH-01 — De Sign-up tool moet gebruik maken van Single Sign On (SSO)

Requirements: De tool moet gebruik maken van de beschikbare SSO binnen de Hanze. Als de tool gebruikt wordt vanuit een geauthenticeerde Hanze omgeving, dient deze context hergebruikt te worden.
Bron: PSI: ~15 min, BI: ~10-14 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, Brightspace engineers.
Uitleg: SSO is de normale toegangs route tot de Hanze systemen. 

#### NF-AUTH-02 — Ondersteuning van role-based access control (RBAC)

Requirements: De tool ondersteunt RBAC voor de gebruikers. 
Bron: VI: ~4-6 min, PSI: ~4 min, ~10 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.
Uitleg: Verschillende rolen gebruiken en zien verschillende functionaliteiten binnen de applicatie en hebben daarnaast toegang tot verschillende data. 

#### NF-AUTH-03 — Multi tenant

Requirements: 
Bron: VI: ~11-14 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.
Uitleg: 

To Do: 1 multi tenant requirment, waarschijnlijk hier. 
to Do: dit is toch ook een requirement van BS&IT?

### Betrouwbaarheid en data integriteit

#### NF-BDI-01 — De tool moet overweg kunnen met simultaan gebruik

Requirements: De Sign-up tool voorkomt dat leerlingen kunnen overboeken op een tijdslot of dat een leerling 2 keer kan registreren. Bij een falende actie moet niet leiden tot een gedeeltelijke, tegenstrijdige of mislijdende data registratie. 
Bron: VI: ~0-3 min, ~10-11 min, ~15-16 min, HI: ~5-6 min.
Stakeholders: Regisseur, docenten, studenten.
Uitleg: De tool moet een single point of truth zijn tav de geregistreerde tijdslots. 

#### NF-BDI-02 — Ondersteunt monitoring en logging

Requirements: De tool ondersteunt de logging en monitoring vereisten die van toepassing zijn op de Hanze systemen voordat het in productie wordt genomen. 
Bron: PSI: ~10-11 min, TKI: ~4-6 min.
Stakeholders: privacy & security, technisch manager.
Uitleg: Monitoring en logging helpen met het ontdekken operationele problemen, onderzoeken van incidenten en ondersteunen technische management van de applicatie.  

To Do: dit is nog erg algemeen, kan dit concreter?

#### NF-BDI-03 — Audit trail

Requirements: De tool logt registraties en administrative wijzigingen, waaronder acteur, actie en tijdstip, zodat de acties geaudit kunnen worden. 
Bron: BII: ~4-5 min, PSI: ~10-11 min.
Stakeholders: privacy & security, technisch manager.
Uitleg: Wijzigingen in registraties en events configuratie kunnen effect hebben op studenten en de planning. Door deze op te slaan is het mogelijk te reconstrueren wat er is gebeurt. 

To do: NF-BDI-02 en NF-BDI-03 fact checken in de interviews en aanscherpen, nuanceren... mogelijk hetzelfde?

### Template:

#### NF-BDI-01 — XXX

Requirements: 
Bron: VI: ~1 min, BII: ~1 min, PSI: ~1 min, TKI: ~1 min, HI: ~1 min, BI: ~1 min.
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.
Uitleg: 

To Do: template weghalen. 

## Priorisatie Requirements

### Methode

### MoSCoW 

## Conclusie