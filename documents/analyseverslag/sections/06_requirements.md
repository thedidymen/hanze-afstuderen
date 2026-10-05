# Requirements

## Inleiding

Dit hoofdstuk stelt de requirements van de Sign-Up Tool vast. Deze requirements beschrijven wat de toekomstige oplossing moet ondersteunen en aan welke kwaliteitseisen moet worden voldaan. Binnen dit hoofdstuk wordt nog geen oplossingsrichting gekozen, dat gebeurt in latere hoofdstukken. 

De requirements zijn gebaseerd op de analyse van de huidige situatie, de stakeholderanalyse en de interviewtranscripten. De initiële usecase is het registreren van events bij Verpleegkunde. Op langere termijn moet deze tool echter breed inzetbaar zijn binnen de Hanze. 

## Verkrijgen van Requirements

De requirements zijn afgeleid uit de stakeholderinterviews en de projectdocumenten. De interviews zijn gebruikt om de huidige problemen, gebruikersbehoeften, organisatorische beperkingen en risico's in kaart te brengen. Deze bevindingen zijn vertaald naar requirements. 
De requirements zijn geen letterlijke weergave van de stakeholdergesprekken. Een opmerking als: "studenten kunnen momenteel zien wie er geregistreerd is in een tijdslot" vertaalt zich bijvoorbeeld naar een privacyrequirement: studenten mogen alleen hun eigen registratie en de algemene beschikbaarheid van het tijdslot zien. 

Deze bronnen zijn gebruikt voor de requirementsanalyse:  
- Verpleegkunde-interview (VI), 2 maart 2026, bijlage A.  
- BS&IT interview (BII), 2 maart 2026, bijlage B.  
- Privacy & Security interview (PSI), 13 april 2026, bijlage C.  
- Technische Kaders interview (TKI), 20 april 2026, bijlage D.  
- HIP interview (HI), 11 mei 2026, bijlage E.  
- Brightspace interview (BI), 1 juni 2026, bijlage F.

## Scope en Aannames

De scope van de requirements is het sign-upproces voor educatieve momenten, zoals praktijkassessments, praktische herexamens, workshops of vergelijkbare activiteiten waarvoor studenten een specifiek moment moeten reserveren. De oplossing moet het proces van Verpleegkunde ondersteunen zonder Verpleegkunde-specifieke ontwerpkeuzes te maken, zodat een Hanzebrede oplossing ontstaat.
Binnen dit hoofdstuk zijn de volgende aannames gemaakt:  
- Brightspace blijft de hoofdapplicatie waarmee studenten en docenten werken met de course.  
- De Sign-Up Tool ondersteunt planning en registratie, maar geen cijfer- of resultaatverwerking.  
- De MVP richt zich op de sign-upworkflow voordat integraties met plannings- en administratiesystemen worden toegevoegd.  
- Requirements die gericht zijn op toekomstige koppelingen worden als laag-prioriteit- of open requirements toegevoegd en maken geen deel uit van de MVP-scope.  

## Gebruikersgroepen en Rollen

De volgende gebruikersgroepen en rollen worden gebruikt in de requirements. Deze rollen zijn niet hetzelfde als de organisatorische stakeholders. Ze beschrijven hoe gebruikers met het systeem werken en welke informatie en acties zij gebruiken (zie @tbl:roles). 

| Rol | Beschrijving |
|---|---|
| Student | Registreert zich voor een event in de Sign-Up Tool en kan de eigen registratie bekijken |
| Docent | Gebruikt het deelnemersoverzicht ter voorbereiding op en afname van assessments |
| Regisseur | Bereidt sign-upevents voor |
| Functioneel manager | Ondersteunt de applicatie |
| Technisch manager | Onderhoudt de applicatie en biedt technische ondersteuning |
| Brightspace-engineer | Ondersteunt de Brightspace-integratie |
| Privacy & Security | Beoordeelt de verwerking van persoonsgegevens, toegangsrechten en logging |

: Rollentabel {#tbl:roles}

## Requirements

De requirements zijn onderverdeeld in functionele en niet-functionele requirements. De functionele requirements (FN) beschrijven het gedrag en de mogelijkheden van de Sign-Up Tool voor gebruikers. Denk hierbij aan het creëren van evenementen, het registreren voor tijdslots en het maken van een deelnemersoverzicht. Ze zijn gegroepeerd op basis van de workflow die ze ondersteunen. 

Niet-functionele requirements (NF) beschrijven de beperkingen en kwaliteitseisen waarbinnen de functionaliteiten moeten werken. Deze bevatten privacy- en security-eisen, onderhoudbaarheid, integratie, authenticatie, autorisatie en data-integriteit. Deze requirements zijn niet altijd direct zichtbaar, maar bepalen mede of een oplossing geschikt is voor de Hanzeomgeving. 

Elke requirement bevat een bron, relevante stakeholders en een uitleg. 

## Functionele Requirements

### Event en Tijdslotmanagement (ETM)

#### FN-ETM-01 - Creëer sign-upevents

Requirements: Het systeem laat geautoriseerde medewerkers sign-upevents creëren.  
Bron: VI: ~1-4 min;  
Stakeholders: regisseur, docenten, functioneel manager, studenten.  
Uitleg: In het huidige proces maken medewerkers voor elk registratiemoment handmatig Brightspace-groepen aan. De vervangende oplossing moet dit rechtstreeks kunnen ondersteunen.  


#### FN-ETM-02 - Vastleggen van metadata

Requirements: Het systeem laat medewerkers basisinformatie vastleggen: naam, datum, tijd, locatie, docent en course of module.  
Bron: VI: ~2, ~10 min;  
Stakeholders: Regisseur, docenten, functioneel manager, studenten.  
Uitleg: In de huidige workflow worden datum, tijd en locatie vastgelegd in de groepsnaam. Binnen de oplossing moet deze informatie als gestructureerde data worden vastgelegd.  

#### FN-ETM-03 - Gereserveerde tijd opdelen in tijdslots

Requirements: Het systeem laat medewerkers de gereserveerde tijd opdelen in meerdere registratiemomenten.  
Bron: VI: ~10 min, BI ~6-8 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: De kern van het probleem is niet alleen het toekennen van de totale tijd, maar ook het opdelen ervan in registratiemomenten.  

#### FN-ETM-04 - Capaciteit van tijdslots

Requirements: Binnen een event moet het mogelijk zijn om de capaciteit van tijdslots te bepalen. De oplossing moet zowel individuele als groepsregistraties ondersteunen, bijvoorbeeld één of meerdere studenten per tijdslot.  
Bron: VI: ~0-3 min, BI ~6 min.  
Stakeholders: regisseur, docenten, studenten.  
Uitleg: Binnen het huidige systeem is de capaciteit van registratiemomenten beperkt flexibel in te richten. Voor verschillende assessments kan een andere groepsgrootte nodig zijn. De oplossing moet daarom verschillende capaciteiten voor events kunnen ondersteunen, zonder dat voor ieder afzonderlijk tijdslot een afwijkende capaciteit hoeft te worden ingesteld.  

#### FN-ETM-06 - Markeer pauzes als niet registreerbaar

Requirements: Docenten moeten een pauze kunnen nemen. Tijdens deze momenten kunnen studenten zich niet registreren.  
Bron: VI: ~8 min, BI ~7 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Assessmentblokken kunnen meerdere uren duren. Docenten moeten daarom de mogelijkheid hebben om pauzes in te plannen.  

#### FN-ETM-07 - De registratie heeft een openings- en sluitingstijd

Requirements: De registratie moet op vooraf bepaalde tijdstippen geopend en gesloten kunnen worden.  
Bron: VI: ~15 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Er is expliciet gevraagd om de registratie op een vooraf bepaald tijdstip te kunnen sluiten.  

#### FN-ETM-08 - De registratie heeft een annuleringsdeadline

Requirements: Er moet een annuleringsdeadline komen die losstaat van de registratiedeadline (FN-SR-02).  
Bron: VI: ~15 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Studenten mogen zich registreren tot de registratiedeadline, maar kunnen niet meer annuleren na de annuleringsdeadline.  

#### FN-ETM-09 - Tijdslotstatus tonen

Requirements: De status van een tijdslot moet zichtbaar zijn (beschikbaar, gedeeltelijk beschikbaar, vol of niet beschikbaar).  
Bron: VI: ~0, ~3 min, BI ~10-11 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Studenten en docenten moeten kunnen zien of een tijdslot nog beschikbaar is en hoeveel plekken beschikbaar zijn.  

#### FN-ETM-10 - Genereer tijdslots op basis van geïmporteerde planningsgegevens

Requirements: Het systeem kan op basis van gestructureerde planningsgegevens, bijvoorbeeld een Excel-bestand, tijdslots genereren wanneer een directe integratie niet mogelijk of beschikbaar is.  
Bron: VI ~3 min, ~10 min.  
Stakeholders: Regisseur, functioneel manager, docenten.
Uitleg: Het huidige proces begint met het ontvangen van planningsinformatie uit Excel. Het importeren van deze gestructureerde gegevens zou het aantal handmatige stappen verminderen.  

#### FN-ETM-11 - Terugkerende of herbruikbare eventstructuren

Requirements: Het systeem ondersteunt het hergebruiken, kopiëren of opnieuw aanmaken van eerdere events voor nieuwe studiejaren.  
Bron: VI: ~1 min, ~12-14 min.  
Stakeholders: Regisseur, docenten, functioneel manager.  
Uitleg: Binnen het huidige proces vinden events periodiek plaats. Hergebruik vermindert het aantal handmatige stappen.  

#### FN-ETM-12 - Rollende vrijgave van tijdslots

Requirements: Het systeem ondersteunt een rollende vrijgave van tijdslots, zodat er geen of weinig gaten in het rooster van de docent ontstaan.  
Bron: VI: ~16 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Een rollende vrijgave van tijdslots voorkomt een inefficiënte verdeling van tijdslots over de dag. Dit is geen kernrequirement.  


### Student Registratie

#### FN-SR-01 - Registreren voor een tijdslot

Requirements: Studenten moeten zich kunnen registreren voor een tijdslot.  
Bron: VI: ~0 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Zelfregistratie is het centrale doel van de Sign-Up Tool en vervangt de huidige registratie via Brightspace-groepen.  

#### FN-SR-02 - Deregistratie vóór de annuleringsdeadline

Requirements: Studenten moeten zich kunnen deregistreren tot de ingestelde annuleringsdeadline (FN-ETM-08).  
Bron: VI: ~0 min, ~15 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: In het huidige proces kunnen studenten zich deregistreren als ze zich per ongeluk hebben ingeschreven. Een late annulering moet tellen als een gemiste kans.  

#### FN-SR-04 - Registratie wijzigen

Requirements: Studenten kunnen hun registratie annuleren en daarmee wijzigen binnen de annuleringsregels.  
Bron: VI: ~0 min, ~15 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Binnen de gestelde regels is het wijzigen van een tijdslot toegestaan.  

#### FN-SR-05 - Eigen registratie bekijken

Requirements: Studenten kunnen de eigen registratie inzien zonder die van andere studenten te zien.  
Bron: VI: ~3 min, ~6 min, PSI: ~4 min.  
Stakeholders: Regisseur, docenten, studenten, privacy en security.  
Uitleg: Studenten hoeven geen gegevens van andere studenten te kunnen inzien.  

#### FN-SR-06 - Beschikbaarheid tonen

Requirements: Voor studenten moet het zichtbaar zijn hoeveel ruimte er is in een tijdslot, zonder te zien wie er in zitten.  
Bron: VI: ~2-3 min,  ~6 min, HI: ~21 min, BI: ~10-11 min.  
Stakeholders: Regisseur, docenten, studenten, privacy en security.  
Uitleg: In de huidige situatie is zichtbaar wie zich voor welk tijdslot heeft geregistreerd. Studenten hoeven deze informatie niet te zien.  

#### FN-SR-07 - Sign-upevents alleen zichtbaar wanneer relevant

Requirements: Een sign-upevent moet alleen zichtbaar zijn voor een student wanneer het relevant is voor de courses of modules die deze student volgt.  
Bron: VI: ~14 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Alleen relevante informatie moet zichtbaar zijn. Dit is ook een requirement voor gebruik door andere schools binnen de Hanze.  

#### FN-SR-08 - Notitie of opmerking van studenten

Requirements: Studenten kunnen een opmerking achterlaten als deze functie is ingeschakeld door de docent of regisseur.  
Bron: VI: ~4 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Het huidige systeem staat geen opmerkingen toe; dit is als beperking aangekaart. De behoefte moet worden gevalideerd voordat deze functie onderdeel wordt van de MVP.  

#### FN-SR-09 - Voorkom dubbele registraties

Requirements: Studenten kunnen zich maar één keer registreren, tenzij dit anders is geconfigureerd.  
Bron: VI: ~0-3 min, ~15 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Dubbele registraties ondermijnen het capaciteitsmanagement en de planning.  

### Docent en regisseur Overzicht

TODO: Uitzoeken hoe de structuur binnen Brightspace werkt: Module → course → studenten, Module → course → klas/docent → studenten, of een andere structuur. Op welk niveau werkt de Sign-Up Tool: course- of klasniveau?

#### FN-DRO-01 - Samenvattend deelnemersoverzicht

Requirements: De tool moet een overzicht geven van de geregistreerde studenten voor het event.  
Bron: VI: ~1 min, ~3-4 min, ~6 min.  
Stakeholders: Regisseur, docenten.  
Uitleg: Docenten moeten in Brightspace elke groep openen om te zien wie zich heeft geregistreerd. Een samenvattend overzicht helpt bij de voorbereiding.  

#### FN-DRO-02 - Groepsindelingsoverzicht per tijdslot

Requirements: De tool moet een overzicht geven van alle tijdslots, inclusief geregistreerde studenten en de resterende capaciteit.   
Bron: VI: ~3-6 min, ~13-14 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Docenten moeten weten welke studenten wanneer komen, niet alleen beschikken over een deelnemerslijst.  

#### FN-DRO-03 - Eventbeschrijving

Requirements: De tool biedt ruimte voor voorbereidingsinformatie voor studenten, zoals informatie over de activiteit, eisen of andere statusinformatie.  
Bron: VI: ~3-4 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Docenten willen weten welk assessment een student doet en of aan de requirements is voldaan, bijvoorbeeld of een vaardighedenkaart is afgetekend.  

TODO: Uitzoeken wie deze informatie aanlevert: gaat het om eisen van de docent of om een invuloefening voor de student?

#### FN-DRO-04 - Een event instellen

Requirements: De regisseur, functioneel manager of docent moet een event zonder technische hulp kunnen opzetten.  
Bron: VI: ~4-6 min. 
Stakeholders: Regisseur, docenten.  
Uitleg: Er mag geen externe afhankelijkheid zijn voor het opzetten van events.  

#### FN-DRO-05 - Overzicht van alle deelnemers aan een event

Requirements: Geautoriseerde docenten moeten alle deelnemers aan een event kunnen inzien als dat nodig is voor de uitvoering van het assessment.  
Bron: VI: ~6 min, PSI: ~4 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security.  
Uitleg: Docenten kunnen een assessment voor collega's uitvoeren en hebben daarom een evenementoverzicht nodig, niet alleen een overzicht van hun eigen studenten.  

TODO: Zie hierboven. Uitzoeken wat de functionele eis precies is. 

#### FN-DRO-07 - Studenten handmatig registreren

Requirements: Docenten en regisseurs kunnen een student handmatig registreren voor een event of tijdslot.  
Bron: VI: ~12-14 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security.  
Uitleg: Studenten moeten handmatig kunnen worden toegevoegd ter ondersteuning van uitzonderlijke situaties waarin zelfregistratie niet toereikend is.  

#### FN-DRO-08 - Studenten in bulk registreren

Requirements: Studenten moeten in bulk geregistreerd kunnen worden voor operationele efficiëntie.  
Bron: VI: ~3 min, ~10 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Bulksgewijze registratie maakt het proces veel sneller.  

TODO: Uitzoeken hoe dit zou moeten werken: via een Brightspace-quicklist of door een Excel-bestand toe te voegen?

#### FN-DRO-09 - Events bewerken en verwijderen

Requirements: Events moeten kunnen worden bewerkt en verwijderd, met waarborgen voor open registraties.  
Bron: ? assignment brief.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Regisseurs en docenten moeten een event kunnen opzetten, bewerken en verwijderen. De implementatie moet waarborgen bieden zodra er registraties voor een event zijn.  

TODO: Bron vaststellen en waarborgen uitwerken.

#### FN-DRO-10 - Eventstatus beheren

Requirements: Regisseurs en docenten moeten de status van een event kunnen wijzigen, bijvoorbeeld naar concept, open, gesloten of gearchiveerd.  
Bron: VI: ~15 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Expliciete statussen maken de levenscyclus van het event duidelijk en begrijpelijk.  

### Exports

TODO: Nagaan of deze eisen overlappen met de vorige groep.

#### FN-EXP-01 - Deelnemerslijst genereren

Requirements: Docenten en regisseurs mogen deelnemerlijsten genereren.  
Bron: VI: ~1 min, ~3-4 min.  
Stakeholders: Regisseur, docenten.  
Uitleg: Docenten mogen deelnemerslijsten maken ter voorbereiding op en uitvoering van een event.  

#### FN-EXP-02 - Deelnemerslijst filteren op event, datum of docent

Requirements: Deelnemerlijsten kunnen gefilterd worden op event, datum, docent (tijdslot?).  
Bron: VI: ~3-4 min, ~13-14 min.  
Stakeholders: Regisseur, docenten.  
Uitleg: Docenten moeten kunnen zien wie wanneer komt en op welke dag (voor welk event), in plaats van één ongesorteerde lijst.  

#### FN-EXP-03 - Export of afdrukbare versie ondersteunen

Requirements: Er moet een export of afdrukbare versie van de lijst gemaakt kunnen worden.  
Bron: VI: ~1 min, ~3-4 min, ~10 min.  
Stakeholders: Regisseur, docenten.  
Uitleg: De huidige workflow maakt gebruik van Excel en handgemaakte lijsten. Een uitdraai helpt de docenten gebruik te maken van het schema buiten de tool.  

#### FN-EXP-04 - Data-export beperken tot het minimum

Requirements: De geëxporteerde data moet volledig en functioneel zijn en beperkt blijven tot wat noodzakelijk is voor het beoogde gebruik.  
Bron: VI: ~2 min, PSI: ~8 min, ~32-33 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: De deelnemerslijst bevat persoonsgegevens van studenten. De export moet daarom zo min mogelijk gegevens bevatten.  

### Configuratie

#### FN-CON-01 - Koppelen aan programma- en coursecontext

Requirements: Events moeten gekoppeld kunnen worden aan een programma, course, klas of andere relevante context.  
Bron: VI: ~14 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Studenten mogen alleen toegang krijgen tot relevante evenementen. Er moet een logische scheiding zijn tussen programma's.  

#### FN-CON-02 - Evenementen hebben standaardinstellingen

Requirements: Een evenement heeft configureerbare standaardinstellingen, zoals slotlengte, capaciteit, annuleringsdeadline en zichtbaarheid.  
Bron: VI: ~10-16 min.  
Stakeholders: Regisseur, docenten.  
Uitleg: Het opzetten van een evenement is repetitief werk. Het instellen van standaardwaarden vermindert handmatige handelingen.  

TO DO: is het uitschrijven van instelbare settings niet handiger? Mist dat niet?

#### FN-CON-03 - Rolgebaseerde toegang

Requirements: Toegang tot de tool is gebaseerd op de gebruikersrol, zoals regisseur, docent, student of beheerder.  
Bron: VI: ~4-6 min, PSI: ~4 min.  
Stakeholders: Regisseur, docenten, studenten, beheerder.  
Uitleg: Verschillende rollen hebben verschillende functionaliteiten en zichtbaarheid. Rolconfiguratie is nodig om gebruik en privacy te ondersteunen.  

TODO: Deze requirement verder uitwerken en de bronnen controleren. 

#### FN-CON-04 - Generiek gebruik van de tool ondersteunen

Requirements: De tool moet generiek te gebruiken zijn.  
Bron: VI: ~2 min, PSI: ~8 min, ~32-33 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: De tool moet niet alleen de Verpleegkunde-specifieke workflow ondersteunen. Het ontwerp is generiek en kan processen binnen de hele Hanze ondersteunen.  

#### FN-CON-05 - Verschillende schools scheiden

Requirements: De tool ondersteunt een logische scheiding tussen schools en courses.  
Bron: VI: ~11 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: Binnen de tool is er een duidelijke scheiding tussen schools en courses.  

TODO: Nagaan waarin deze requirement verschilt van FN-CON-01.

## Niet-functionele requirements

### Privacy & Security

#### NF-PS-01 - Dataminimalisatie

Requirements: De tool moet alleen data verwerken en opvragen die noodzakelijk is voor het sign-up proces.  
Bron: PSI: ~8 min, ~32-33 min.  
Stakeholders: Docenten, studenten, privacy & security, functioneel manager.  
Uitleg: Dataminimalisatie vermindert privacy- en securityrisico's.  

TODO: Nagaan waar Verpleegkunde deze requirement ook noemt.

#### NF-PS-02 - Alleen eigen registratie zichtbaar

Requirements: De tool laat alleen de eigen registratie zien. Studenten krijgen geen inzicht in de registraties van andere studenten.  
Bron: VI: ~2 min, ~6 min, PSI: ~4-8 min, HI: ~21 min.  
Stakeholders: Docenten, studenten, privacy & security, functioneel manager.  
Uitleg: Binnen de huidige tool kunnen studenten de registratiegegevens van andere studenten inzien. Dit is een privacyprobleem.  

#### NF-PS-03 - De tool registreert geen beoordelingsgegevens

Requirements: De tool registreert geen cijfers of beoordelingen.  
Bron: PSI: ~4-8 min, HI: ~19-21 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.  
Uitleg: Beoordeling vindt plaats binnen de bestaande tooling en maakt geen onderdeel uit van deze tool.  

#### NF-PS-04 - Gegevensstromen documenteren

Requirements: Gegevensstromen binnen de applicatie moeten worden gedocumenteerd.  
Bron: PSI: ~8 min, ~32-33 min.  
Stakeholders: Privacy & security, BS&IT, functioneel management, technisch management.  
Uitleg: Gegevensstromen van persoonsgegevens moeten inzichtelijk zijn.  

#### NF-PS-05 - Privacyquickscan

Requirements: Het project moet een privacyquickscan uitvoeren.
Bron: PSI: ~32-33 min.  
Stakeholders: Privacy & security, BS&IT, Verpleegkunde.  
Uitleg: Het project moet een privacyquickscan uitvoeren voordat de tool echte persoonsgegevens verwerkt.  

TODO: Controleren of de stakeholderlijst op deze manier moet worden uitgebreid. 

#### NF-PS-06 - Verwerkingsovereenkomst met externe partij

Requirements: Als een externe partij persoonsgegevens verwerkt, moet er een verwerkingsovereenkomst worden opgesteld.  
Bron: VI: PSI: ~8 min, ~32 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.  
Uitleg: Om te voldoen aan de AVG moet er een verwerkingsovereenkomst worden opgesteld voor de verwerking van persoonsgegevens.  

#### NF-PS-07 - Security by design

Requirements: De Sign-Up Tool moet worden ontworpen volgens het security-by-designprincipe.  
Bron: PSI: ~10 min.  
Stakeholders: Privacy & security, functioneel manager, technisch manager.  
Uitleg: Security en privacy moeten gedurende het hele proces worden meegenomen. Daarbij moet worden gekozen voor de veiligste praktische standaardinstelling.  

#### NF-PS-08 - Least privilege

Requirements: De tool geeft gebruikers alleen permissies die nodig zijn voor het uitvoeren van hun rol en taak.  
Bron: VI: ~4-6 min, PSI: ~10 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.  
Uitleg: De tool verwerkt persoonsgegevens. Verschillende rollen en taken vereisen verschillende toegangsrechten. Least privilege vermindert privacy- en securityrisico's.  

#### NF-PS-09 - Bewaar- en verwijderingsregels voor gegevens

Requirements: De Sign-Up Tool moet vastleggen hoelang registratiegegevens worden bewaard en wanneer ze worden verwijderd of gearchiveerd.  
Bron: PSI: ~32-33 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.  
Uitleg: De tool verwerkt persoonsgegevens. Er zijn regels nodig om doelbinding te waarborgen en onnodige opslag te voorkomen.  

### Onderhoudbaarheid

#### NF-MA-01 - Onderhoudbare en breed gedragen technologie

Requirements: De technische oplossing moet gebruikmaken van breed gedragen technologieën.  
Bron: BII: ~6-8 min, TKI: ~7-9 min, HI: ~3-6 min.  
Stakeholders: BS&IT, technisch manager, collabspace.  
Uitleg: De kennis en vaardigheden die nodig zijn om de applicatie te onderhouden, moeten gebaseerd zijn op breed gedragen technologieën. Hierdoor moet de applicatie eenvoudig overdraagbaar zijn en mag het onderhoud geen specialistische kennis vereisen.  

TODO: Stakeholders controleren.

#### NF-MA-02 - Eigenaarschap en onderhoud

Requirements: Voordat de oplossing operationeel wordt, is duidelijk waar het eigenaarschap en het onderhoud van de applicatie ligt.  
Bron: BII: ~2-5 min, HI: ~3-6 min.  
Stakeholders: BS&IT, HIP, technisch manager.  
Uitleg: BS&IT en HIP benoemen continuïteit, eigenaarschap en onderhoud als kritieke punten tijdens de transitie van PoC naar productie.  


#### NF-MA-04 - Scheiding van presentatie, integratie en data

Requirements: De architectuur van de Sign-Up Tool scheidt de presentatie-, integratie- en datalaag.  
Bron: BII: ~11 min, architectuurkaders.  
Stakeholders: BS&IT, HIP, technisch manager.  
Uitleg: De scheiding van lagen maakt de applicatie beter onderhoudbaar en veiliger. Daarnaast dwingt de scheiding tot expliciete keuzes ten aanzien van verwerking en opslag.  

TODO: Architectuurkaders uitzoeken. 

#### NF-MA-05 - Codereviews en kwaliteitsborging

Requirements: Het ontwikkelproces moet codereviews en kwaliteitscontroles faciliteren voordat de applicatie in productie gaat.  
Bron: BII: ~2-6 min, HI: ~3-5 min.  
Stakeholders: BS&IT, HIP, technisch manager.  
Uitleg: Code review en kwaliteitscontrole verkleinen de kans op fouten en zorgen voor technisch verantwoorde keuzes. Daarnaast helpt dit met kennisdeling, consistente code en onderhoudbaarheid.  

#### NF-MA-06 - Technische keuzes documenteren

Requirements: Grote technische keuzes moeten worden gedocumenteerd en onderbouwd.  
Bron: BII: ~6-8 min.  
Stakeholders: BS&IT, HIP, technisch manager.  
Uitleg: Technische keuzes moeten worden onderbouwd.  

### Integratie

#### NF-INT-01 - Sign-Up Tool toegankelijk vanuit Brightspace

Requirements: De Sign-Up Tool moet toegankelijk zijn vanuit de relevante Brightspace content.  
Bron: VI: ~6-7 min, BI: ~10-14 min.  
Stakeholders: Regisseur, docenten, studenten, Brightspace engineers.  
Uitleg: Brightspace is de LMS vanuit de Hanze die studenten en docenten gebruiken om het onderwijs digitaal aan te bieden.  

TO DO: Stakeholder: Brightspace engineers. 

#### NF-INT-02 - Gebruik het Brightspace-integratiemechanisme

Requirements: De oplossing gebruikt een goedgekeurd Brightspace-integratiemechanisme. Indien toepasbaar wordt LTI 1.3/LTI Advantage gebruikt om de geauthenticeerde gebruiker en coursecontext veilig op te halen.  
Bron: BI: ~10-14 min, ~19-20 min.  
Stakeholders: Regisseur, docenten, studenten, Brightspace engineers, technisch manager.  
Uitleg: LTI is het Brightspace-mechanisme om een externe applicatie binnen Brightspace te integreren.  


### Authenticatie en autorisatie

#### NF-AUT-01 — De Sign-Up Tool gebruikt SSO

Requirements: De tool moet gebruikmaken van de beschikbare SSO binnen de Hanze. Als de tool vanuit een geauthenticeerde Hanzeomgeving wordt gebruikt, moet deze context worden hergebruikt.  
Bron: PSI: ~15 min, BI: ~10-14 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, Brightspace engineers.  
Uitleg: SSO is de gebruikelijke toegangsroute tot de systemen van de Hanze.  

#### NF-AUT-02 — Ondersteuning van RBAC

Requirements: De tool ondersteunt role-based access control (RBAC) voor gebruikers.  
Bron: VI: ~4-6 min, PSI: ~4 min, ~10 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.  
Uitleg: Verschillende rollen gebruiken en zien verschillende functionaliteiten binnen de applicatie en hebben toegang tot verschillende gegevens.  

#### NF-AUT-03 - Multitenancy

Requirements:  
Bron: VI: ~11-14 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.  
Uitleg:  

TODO: Eén multitenancyrequirement, waarschijnlijk hier. Nagaan of dit ook een requirement van BS&IT is.

### Betrouwbaarheid en data-integriteit

#### NF-BDI-01 — De tool moet overweg kunnen met gelijktijdig gebruik

Requirements: De Sign-Up Tool voorkomt dat studenten een tijdslot overboeken of zich twee keer registreren. Een mislukte actie mag niet leiden tot een gedeeltelijke, tegenstrijdige of misleidende gegevensregistratie.  
Bron: VI: ~0-3 min, ~10-11 min, ~15-16 min, HI: ~5-6 min.  
Stakeholders: Regisseur, docenten, studenten.  
Uitleg: De tool moet één betrouwbare bron zijn voor de geregistreerde tijdslots.  

#### NF-BDI-02 — Monitoring en logging ondersteunen

Requirements: Voordat de tool in productie wordt genomen, moet deze voldoen aan de vereisten voor logging en monitoring die van toepassing zijn op Hanze-systemen.  
Bron: PSI: ~10-11 min, TKI: ~4-6 min.  
Stakeholders: privacy & security, technisch manager.  
Uitleg: Monitoring en logging helpen operationele problemen te ontdekken, incidenten te onderzoeken en het technisch beheer van de applicatie te ondersteunen.  

TODO: Deze requirement is nog erg algemeen. Kan deze concreter worden geformuleerd?

#### NF-BDI-03 — Audittrail

Requirements: De tool registreert aanmeldingen en administratieve wijzigingen, waaronder de actor, de actie en het tijdstip, zodat deze acties kunnen worden gecontroleerd.  
Bron: BII: ~4-5 min, PSI: ~10-11 min.  
Stakeholders: privacy & security, technisch manager.  
Uitleg: Wijzigingen in registraties en eventconfiguraties kunnen gevolgen hebben voor studenten en de planning. Door deze wijzigingen vast te leggen, kan worden gereconstrueerd wat er is gebeurd.  

TODO: NF-BDI-02 en NF-BDI-03 controleren aan de hand van de interviews en aanscherpen of nuanceren. Mogelijk overlappen ze.

### Template

#### NF-BDI-01 — XXX

Requirements:  
Bron: VI: ~1 min, BII: ~1 min, PSI: ~1 min, TKI: ~1 min, HI: ~1 min, BI: ~1 min.  
Stakeholders: Regisseur, docenten, studenten, privacy & security, functioneel manager.  
Uitleg:  

TO DO: template weghalen. 

## Prioritering van requirements

De vastgestelde requirements verschillen in belang voor het project. Alle requirements vertegenwoordigen een behoefte, beperking of kwaliteitsdoel. Ze hoeven echter niet allemaal op hetzelfde moment te worden geïmplementeerd. Om onderscheid te maken, worden de requirements geprioriteerd. Daarbij wordt onderscheid gemaakt tussen requirements die noodzakelijk zijn voor de initiële versie en requirements die kunnen worden uitgesteld zonder dat de oplossing onbruikbaar wordt. 

### Methode

De MoSCoW-methode is geïntroduceerd door Clegg en Barker in CASE Method Fast-Track: A RAD Approach [@clegg1994]. Hierbij wordt onderscheid gemaakt tussen vier categorieën: Must, Should have, Could have en Won't have.   

De categorie Must bevat de requirements die essentieel zijn voor het project. Zonder deze requirements kan de applicatie haar doel niet bereiken. Should-requirements zijn belangrijk en worden verwacht, maar zijn niet noodzakelijk voor een werkbare oplossing. Daarnaast zijn er requirements die wenselijk en praktisch zijn, maar een beperkte invloed hebben op de bruikbaarheid van de applicatie. Deze vallen in de categorie Could. De laatste categorie is Won't. Deze requirements worden in deze release expliciet niet gerealiseerd en kunnen voor een latere release worden overwogen. 

| Score | Belang | Noodzaak |
|---|---|---|
| 1 | Weinig bijdrage aan het project | Niet vereist voor de MVP |
| 2 | Beperkt voordeel | Gemakkelijk uitstelbaar of een eenvoudige workaround |
| 3 | Nuttige toevoeging aan de workflow | Uitstel veroorzaakt ongemak of extra handmatig werk |
| 4 | Grote toevoeging aan de workflow of aan een stakeholderbehoefte | Uitstel veroorzaakt veel extra werk; een workaround is nog mogelijk |
| 5 | Ondersteunt het projectdoel | Bijna onmisbaar |

: Criteria-tabel {#tbl:criteria}

De MoSCoW-methode is handig om onderscheid te maken tussen de hoofdcategorieën, maar biedt geen houvast voor een verdere verdeling. Daarom krijgen requirements een score. Deze score is het product van het belang en de noodzaak van een requirement. Beide worden zo goed mogelijk ingeschat op een schaal van 1 tot 5, zie tabel @tbl:criteria.

De numerieke prioriteit volgt uit de onderstaande functie:  

$$
Priority(r)=
\begin{cases}
\infty, & \text{if } r \text{ is a Must Have}\\
Importance(r)\times Necessity(r), & \text{otherwise}
\end{cases}
$$  

waarbij $P$ de prioriteit, $I$ het belang en $N$ de noodzaak van requirement $r$ voorstellen.

De prioriteitsscore wordt berekend voor de categorieën buiten Must. Aan de Must-requirements moet altijd worden voldaan; daarom hebben ze effectief een prioriteitsscore van oneindig. 

### MoSCoW

Voor de Must-have-requirements is het oneindigheidssymbool (∞) gebruikt. Aan elke Must-have moet worden voldaan om tot een oplossing te komen. Er is dus geen onderling verschil in het belang van deze requirements. 

De andere requirements zijn primair ingedeeld in hoofdcategorieën, met de prioriteitsscore als verdere verdeling. Hoewel is geprobeerd een zo objectief mogelijke lijst op te stellen, blijft de uiteindelijke score subjectief. In tabel @tbl:moscowpriority wordt de relatie tussen de MoSCoW-categorieën en de prioriteitsscore weergegeven. 

| MoSCoW-value | Priority-score |
|---|---|
| Must | ∞ |
| Should | 15-20 |
| Could | 8-12 |
| Won't | 1-6 |

: MoSCoW-prioriteitstabel {#tbl:moscowpriority}

De classificatie van de requirements richt zich eerst op het kernproces: het creëren van evenementen en het registreren daarvoor. Daarna verschuift de aandacht naar de processen voor docenten. Tot slot volgen de meer niet-functionele requirements, zoals security, privacy en onderhoudbaarheid. 

| ID | Requirement | MoSCoW | Imp. | Nec. | Prio. |
|---|---|---|---:|---:|---:|
| FN-ETM-01 | Sign-upevents creëren | Must | ∞ | ∞ | ∞ |
| FN-ETM-02 | Metadata vastleggen | Must | ∞ | ∞ | ∞ |
| FN-ETM-03 | Gereserveerde tijd opdelen in tijdslots | Must | ∞ | ∞ | ∞ |
| FN-ETM-04 | Capaciteit van tijdslots | Must | ∞ | ∞ | ∞ |
| FN-ETM-09 | Tijdslotstatus tonen | Must | ∞ | ∞ | ∞ |
| FN-ETM-06 | Pauzes markeren als niet registreerbaar | Should | 5 | 4 | 20 |
| FN-ETM-07 | Registratie heeft een openings- en sluitingstijd | Should | 5 | 4 | 20 |
| FN-ETM-08 | Registratie heeft een annuleringsdeadline | Should | 4 | 4 | 16 |
| FN-ETM-11 | Terugkerende of herbruikbare eventstructuren | Could | 4 | 3 | 12 |
| FN-ETM-12 | Rollende vrijgave van tijdslots | Could | 4 | 3 | 12 |
| FN-ETM-10 | Tijdslots genereren uit geïmporteerde planningsgegevens | Won't | 2 | 2 | 4 |
|  |  |  |  |  |  |
| FN-SR-01 | Registreren voor een tijdslot | Must | ∞ | ∞ | ∞ |
| FN-SR-05 | Eigen registratie bekijken | Must | ∞ | ∞ | ∞ |
| FN-SR-06 | Beschikbaarheid is zichtbaar | Must | ∞ | ∞ | ∞ |
| FN-SR-09 | Dubbele registraties voorkomen | Must | ∞ | ∞ | ∞ |
| FN-SR-07 | Sign-upevents alleen zichtbaar wanneer relevant | Should | 5 | 4 | 20 |
| FN-SR-02 | Deregistratie vóór de annuleringsdeadline | Should | 4 | 4 | 16 |
| FN-SR-04 | Wijzigen van registratie | Should | 4 | 4 | 16 |
| FN-SR-08 | Notitie of opmerking van studenten | Won't | 2 | 1 | 2 |
|  |  |  |  |  |  |
| FN-DRO-01 | Samenvattend deelnemersoverzicht | Must | ∞ | ∞ | ∞ |
| FN-DRO-02 | Groepsindelingsoverzicht per tijdslot | Must | ∞ | ∞ | ∞ |
| FN-DRO-04 | Een event instellen | Must | ∞ | ∞ | ∞ |
| FN-DRO-05 | Overzicht van alle deelnemers aan een event | Must | ∞ | ∞ | ∞ |
| FN-DRO-07 | Studenten handmatig registreren | Should | 4 | 4 | 16 |
| FN-DRO-09 | Events bewerken en verwijderen | Should | 4 | 4 | 16 |
| FN-DRO-10 | Eventstatus beheren | Could | 3 | 3 | 9 |
| FN-DRO-03 | Eventbeschrijving | Could | 4 | 2 | 8 |
| FN-DRO-08 | Studenten in bulk registreren | Won't | 3 | 2 | 6 |
|  |  |  |  |  |  |
| FN-EXP-01 | Deelnemerslijst genereren | Must | ∞ | ∞ | ∞ |
| FN-EXP-04 | Data-export beperken tot het minimum | Must | ∞ | ∞ | ∞ |
| FN-EXP-03 | Export of afdrukbare versie ondersteunen | Should | 4 | 4 | 16 |
| FN-EXP-02 | Deelnemerslijst filteren op event, datum of docent | Should | 4 | 3 | 12 |
|  |  |  |  |  |  |
| FN-CON-01 | Koppelen aan programma- en coursecontext | Must | ∞ | ∞ | ∞ |
| FN-CON-03 | Rolgebaseerde toegang | Must | ∞ | ∞ | ∞ |
| FN-CON-02 | Evenementen hebben standaardinstellingen | Should | 4 | 3 | 12 |
| FN-CON-04 | Generiek gebruik van de tool ondersteunen | Won't | 4 | 1 | 4 |
| FN-CON-05 | Verschillende schools scheiden | Won't | 5 | 1 | 5 |
|  |  |  |  |  |  |
| NF-PS-01 | Dataminimalisatie | Must | ∞ | ∞ | ∞ |
| NF-PS-02 | Alleen eigen registratie zichtbaar | Must | ∞ | ∞ | ∞ |
| NF-PS-03 | Geen beoordelingsgegevens registreren | Must | ∞ | ∞ | ∞ |
| NF-PS-07 | Security-by-design | Must | ∞ | ∞ | ∞ |
| NF-PS-08 | Least privilege | Must | ∞ | ∞ | ∞ |
| NF-PS-09 | Bewaar- en verwijderingsregels voor gegevens | Should | 4 | 4 | 16 |
| NF-PS-04 | Gegevensstromen documenteren | Could | 4 | 3 | 12 |
| NF-PS-05 | Privacyquickscan | Could | 4 | 2 | 8 |
| NF-PS-06 | Verwerkingsovereenkomst met externe partij | Won't | 5 | 1 | 5 |
|  |  |  |  |  |  |
| NF-MA-01 | Onderhoudbare en breed gedragen technologie | Must | ∞ | ∞ | ∞ |
| NF-MA-04 | Scheiding van presentatie, integratie en data | Must | ∞ | ∞ | ∞ |
| NF-MA-06 | Technische keuzes documenteren | Should | 4 | 5 | 20 |
| NF-MA-05 | Codereviews en kwaliteitsborging | Should | 4 | 4 | 16 |
| NF-MA-02 | Eigenaarschap en onderhoud | Could | 5 | 2 | 10 |
|  |  |  |  |  |  |
| NF-INT-01 | Sign-Up Tool toegankelijk vanuit Brightspace | Must | ∞ | ∞ | ∞ |
| NF-INT-02 | Brightspace-integratiemechanisme gebruiken | Must | ∞ | ∞ | ∞ |
|  |  |  |  |  |  |
| NF-AUT-01 | De Sign-Up Tool gebruikt SSO | Must | ∞ | ∞ | ∞ |
| NF-AUT-02 | Ondersteuning van RBAC | Must | ∞ | ∞ | ∞ |
| NF-AUT-03 | Multitenancy | Won't | 5 | 1 | 5 |
|  |  |  |  |  |  |
| NF-BDI-01 | De tool moet overweg kunnen met gelijktijdig gebruik | Must | ∞ | ∞ | ∞ |
| NF-BDI-02 | Monitoring en logging ondersteunen | Should | 4 | 5 | 20 |
| NF-BDI-03 | Audittrail | Should | 4 | 4 | 16 |

: Prioritering requirements {#tbl:requirement-priorities column-widths="24,90,14,7,7,7"}

## Conclusie

De requirements laten zien dat de Sign-Up Tool niet alleen een vervanging is voor de registratie via Brightspace-groepen. De kern is een gecontroleerd sign-upproces waarin docenten registratiemomenten kunnen configureren en studenten zich kunnen registreren zonder persoonsgegevens van anderen bloot te stellen.

De functionele requirements beschrijven de workflow van het proces, terwijl de niet-functionele requirements vastleggen hoe de tool binnen de Hanzeomgeving kan worden geïmplementeerd. Privacy, toegangsbeheer, Brightspace-integratie, onderhoudbaarheid en data-integriteit zijn daarbij onderdeel van de oplossing, niet slechts toevoegingen na de functionele implementatie. 

De prioritering bepaalt de scope voor de eerste implementatie. De Must-haves vormen de basis van wat gerealiseerd moet worden. Aan de Should- en Could-haves kan worden gewerkt als de tijd en technische haalbaarheid dit toelaten. De Won't-haves worden in deze ronde niet gerealiseerd, maar wel gedocumenteerd voor de toekomst. 

Deze requirements vormen de criteria waaraan mogelijke oplossingen worden getoetst. In de volgende hoofdstukken evalueren we de mogelijke oplossingen.  