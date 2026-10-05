# Oplossingen

## Inleiding

Verschillende oplossingsrichtingen zijn onderzocht voor de Sign-Up Tool. De alternativen rangen van bestaande Brightspace functionaliteit (de huidige situatie), tot commerciele plannings tools en een zelfbouw applicatie. De requirements uit het vorige hoofdstuk zijn gebruikt als initiele selectie criteria. Hierbij zijn vooral de must criteria mee genomen, denk hierbij aan tijdslots, capaciteit, privacy, overzicht, Brightspace integratie, SSO etc. 

### Bright Space Groups

In de huidige situatie worden de zelfenrolment groepen van Brightspace gebruikt als tijdslots. Dit is in de huidige situatie uitgebreid besproken. Deze functionaliteit is vooral bedoeld om studenten in leergroepjes in te delen ipv assesment registratie. Dit vormt het uitgangspunt waar tegen we nieuwe oplossingen houden. 

## Overwogen oplossingen

Mogelijke oplossingen zijn gevonden door verkennend zoeken met Google en ChatGPT. Zoek termen waren gefocust op combinaties van plannings tool, zelf registratie, assesment planning, Brightspace, D2l en LTI integratie. Het doel hiervan was een brede set van mogelijke oplossingen te krijgen. Voor de initiele selectie zijn alle mogelijke oplossingen tegen de Must-requirements gehouden en tegen de beoogde workflow op basis van de huidige situatie. 
 
Om de vergelijking leesbaar te houden, zijn de Must-requirements samengevoegd in 7 groepen:  
- Tijdslots - Het creeeren en configureren van Sign-Up evenementen, metadata, tijdslots, capaciteit en slot status, en de mogelijkheid om een evenement op te zetten (FN-ETM-01, FN-ETM-02, FN-ETM-03, FN-ETM-04, FN-ETM-09, FN-DRO-04).  
- Registratie - de zelf-registratie in een evenment, het bekijken van de eigen registratie, zien van beschikbaarheid en voorkomen van dubbele registratie (FN-SR-01, FN-SR-05, FN-SR-06, FN-SR-09).  
- Docenten - Deelname en tijdslot overzicht, genereren van deelnamelijst (FN-DRO-01, FN-DRO-02, FN-DRO-05, FN-EXP-01).
- Context - linken van evenement met de educationele context, rbac via Brightspace, Brightspace integratie en SSO (FN-CON-01, FN-CON-03, NF-INT-01, NF-INT-02, NF-AUT-01, NF-AUT-02).  
- Privacy & Security - Dataminimalisatie, inzicht in eigen registratie, security-by-design, least-privilege toegange en minimale data exports (NF-PS-01, NF-PS-02, NF-PS-03, NF-PS-07, NF-PS-08, FN-EXP-04).  
- Onderhoudbaarheid - Gebruik van onderhoudbare en ondersteunde technologie, scheiding van presentatie, integratie en data (NF-MA-01, NF-MA-04).  
- Data - Simultaan gebruik zonder overplannen, duplicate registraties en particele of inconcequente registraties (NF-BDI-01).  

In de onderstaande @tbl:initial-solution-screening geeft een + voldoende bewijs dat de Must-requirements in de gegroep gedragen kunnen worden. ? geeft aan dat de oplossing de groep draagt, maar dat 1 of meer requirements kunnen niet/gedeeltelijk gecheckt worden tegen de documentatie. - zeker 1 Must-requirement conflicteerd met de beoogde functionaliteit. 

| Oplossing | Tijdslots | Reg. | Docent | Context | Priv&Sec | Onderh. | Data |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| BS Groups | - | + | + | + | - | ? | - |
| Calendly | + | ? | ? | - | ? | ? | ? |
| SimplyBook.me | + | ? | ? | - | ? | ? | ? |
| Cal.com | + | ? | ? | - | ? | ? | ? |
| TimeEdit | ? | + | ? | ? | ? | ? | ? |
| Zoom LTI Pro / Easy Scheduler | - | ? | ? | + | ? | ? | ? |
| Microsoft Bookings | + | ? | ? | - | ? | ? | ? |
| ConexED | ? | ? | ? | ? | ? | ? | ? |
| Academy Attendance | ? | + | + | + | ? | ? | ? |
| RegisterBlast | ? | ? | + | + | ? | ? | ? |
| Maatwerkoplossing | +* | +* | +* | +* | +* | +* | +* |

: Initiële screening van overwogen oplossingen tegen gegroepeerde Must-requirements {#tbl:initial-solution-screening column-widths="25,10,10,10,10,10,10,10"}

\* De maatwerk oplossing heeft geen inherente product limitaties binnen de technische mogelijkheden. Dit betekend niet dat de functionaliteit al bestaand of al aan wordt voldaan. 

### Algemene Plannings tools

Verschillende algemene plannings tools zijn overwogen, Calendly, SimpleBook.me en Cal.com. Deze producten voorzien in de basis functies die nodig zijn voor de Sign-Up Tool, zoals configurerbaarheid, tijdsduur, zelfboeken etc.  

Calendly [@calendly] is een volwassen commerciele plannings platform dat zowel individuele en groep evenmenten integreert met een kalender en identiteit platforms. Het is voornamelijk ontworpen rond afspraken tussen organisators en uitgenodigden, dan voor educationele evenementen gekoppeld aan een LMS course. Er is geen makkelijke koppeling met Brightspace gevonden. Calendly gebruikt een link en neemt dus niet de context van Brighspace mee (NF-INT-02, FN-CON-01, NF-AUT-02).  

SimplyBook.me [@simplybook] biedt een breder boeking systeem met klassen en groeps boekingen, configureerbare capaciteit, wachtlijsten en administrative functionaliteiten. Functioneel ligt dit dichterbij de vereiste registratie proces dan een basis afspraken planner. Echter is dit meer een alleenstaande boekings platform, voor een zelfstandig ondernemer. Er is geen Brightspace integratie gevonden, dit zou dus door een apart sync proces moeten gebeuren. Dit conflicteerd met de gewenste Brightspace integratie en authenticatie (NF-INT-02, NF-AUT-01, FN-CON-01).  

Cal.com [@cal.com] is een open source tool dat zelf op een server gehost kan worden en geeft dus meer technische controle. Zelf-hosting geeft ook voordelen t.a.v. data eigenaarschap en uitbreidbaarheid. Het ondersteunt individuele en team planningen. Primair is dit een planner platform en niet perse geschikt voor een LMS intregratie. Deze integratie zou zelf ontwikkelt moeten worden en effectief een maatwerk oplossing (NF-INT-02, NF-AUT-02, FN-CON-01).  

Deze producten laten zien dat planner software beschikbaar is. De grootste beperking zit niet in het maken van tijdslots maar in het integreren met de educationele content. Zonder de Brightspace integratie, is het lastig om gebruik te maken van de Brightspace context.  
Hierom zijn algemene plannings tools niet geselecteerd voor de shortlist. Hiervoor is gekeken naar producten met een duidelijke Brightspace integratie. Microsoft bookings is hierop een uitzondering door de sterke relatie met het bestaande Microsoft 365 omgeving. 

### TimeEdit

TimeEdit [@timeedit] is onderzocht omdat het academisch planning, studenten planning en registratie functionaliteit bevat. Hierbij kunnen ook acties als zelf-registratie, configureerbare groep capaciteit, registratie periodes, dit overlapt sterk met de behoeften voor de Sign-Up Tool.  
Echter, is TimeEdit voornamelijk gericht op modules, geplande activiteiten en studentengroepen. De workflow voor een sigh-up event lijkt niet aanwezig (FN-ETM-01, FN-ETM-03, FN-DRO-04). Hoewel Brightspace integratie wordt benoemt, lijkt deze meer gefocust rond de synchronisatie van courses en planningen en faciliteerd het niet een LTI 1.3 integratie voor de overdracht van authenticeerde gebruikers, course context en rollen (NF-INT-02, FN-CON-01).  
Een praktisch evalutatie was niet mogelijk door het ontbreken van een test omgeving of een video van de werking.  
TimeEdit blijft mogelijk relevant omdat de Hanze deze tool al gebruikt [@TimeEditAcademy] [@JaarverslagHanze23].

### Zoom LTI Pro / Easy Scheduler

Zoom LTI Pro [@zoom] is een relevante alternatief omdat het Easy Scheduler werkt binnen een LMS. Docenten kunne beschikbare tijdslots publiceren en studenten kunnen afspraken selecteren en annuleren vanuit de LTI interface. Hierbij wordt gebruik gemaakt van LTI 1.3 dat kan combineren met Brightspace.  
Easy Scheduler is primair geschikt voor een-op-een afspraken, in plaats van de gewenste multi-student assesments (FN-ETM-04) ook lijkt het overzichtg van studenten niet haalbaar (FN-DRO-05).  

### Microsoft Bookings

Microsoft Bookings is onderdeel van het Microsoft 365 ecosysteem. Dit wordt momenteel gebruikt door de Hanze en daarmee interresant omdat deze niet speciaal geonboard hoeft te worden. Daarmee dus ook niet een nieuw extern platform introduceerd. 
Functioneel past de werking van Bookings ook bij de gewenste workflow. Het ondersteunt configureerbare services,  beschikbaarheid en groep afspraken met een maximum aantal deelnemers. De Regisseur/Docenten beheren de services, afspraken en deelnemer informatie, terwijl Bookings wel direct integreert met Outlook en Teams. 
Echter kunnen enkele kern requirements niet geborgt worden. Microsoft ondersteunt LTI 1.3 integratie tussen Microsoft 365 en Brightspace, maar Bookings is niet een van deze applicaties. Hiermee kan er dus niet automatisch gebruik gemaakt worden van de Brighspace course context, rollen en etc. (NF-INT-02, FN-CON-01, NF-AUT-02).
Ook lijkt het zien van de overblijvende capaciteit (FN-SR-06) en de restrictie van 1 registratie per student (FN-SR-09) binnen een evenment niet mogelijk. 
Bookings is een handige tool omdat het al onderdeel is van de bestaand Microsoft-omgeving, maar maakt het verschill met de kern eisen niet goed. 

### ConexED

ConexED is een platform ontworpen voor het hoger onderwijs. Het ondersteunt het maken van afspraken, evenementen, capaciteitmangament, verslaglegging en verschillende gebruiker rolen. Binnen de beschrijvingen wordt gesproken van D2L Brighspace en ondersteuning voor SSO, hiermee wordt voldaan aan een aantal belangrijk Must-requirements van de Sign-Up Tool.  
Echter in de beschikbare documentatie wordt niet verder in gegaan op de Brightspace integratie met LTI 1.3 (NF-INT-02, FN-CON-01, NF-AUT-02). Verder is het ontoereikend gedocumenteerd of de gewenste assesment workflow bereikt kan worden (FN-ETM-01, FN-ETM-03, FN-DRO-04). Daarnaast wordt de gebruikers data gehost in de VS.  
Met deze uitdagingen is ConexED niet tot het shortlist gekomen. 

## Shortlist

Het initiele onderzoek is gebruikt om van alle mogelijk opties te reduceren tot een shortlist. Criteria hiervoor is dat er geen conflict is met een Must-requirement en dat er voldoende aanleiding is om de beoogde workflow te ondersteunen.  
Selectie voor de shortlist is geen garantie dat de oplossing ook voldoet aan alle requirements. Hiervoor is verder onderzoek en vergelijking tussen de oplossingen nodig.  
Gebaseert op deze criteria, blijven er 3 alternatieven over voor verder evaluatie:
- Academy Attendance
- RegisterBlast
- Maatwerk

### Academy Attendance

Academy Attendance [@yournextconcepts] is specifiek ontworpen voor hoger onderwijs en heeft documentatie voor Brightspace integratie. Daarnaast is het gehost binnen Europa en biedt het documentatie t.a.v. AVG.  
Academy Attendance heeft een personlijk view voor studenten, docenten en administators. De eigenschapen hiervan komen dicht bij de requirements van de Sign-Up Tool, inclusief student registratie, capaciteit management en rol afhankelijke informatie.  


### RegisterBlast

Ook deze tool [@registerblast] is specifiek ontwikkelt voor het hoger onderwijs en bevat exam planning, evenement planning en materiaal planning. Evenementen registraties kunnen datums, deadline, herplanning en rappotering bevatten. Daarnaast ondersteunt RegisterBlast LTI 1.3 en SSO. De Brightspace integratie maken dit een interessante kandidaat, maar er blijven wat vraagtekens rond Europese hosting, AVG en of het model overweg kan met de assesment werkflow van de Hanze.  

### Maatwerk

Een ander alternatief is het zelf binnen de hanze een Sign-Up Tool ontwikkelen. In tegenstelling tot een bestaand product kan deze oplossing vollidig worden aangepast op de eisen (uiteraard binnen de mogelijke technishe kaders). Het grootste voordeel is natuurlijk de controle die er is over het project. Het datamodel, gebruikerservaringen, privacy en security, en Brightspace integratie kunnen allemaal specifiek worden gemaakt, in plaats van het proces aan passen aan de beperkingen van een bestaand product.  
Hier tegenover staat natuurlijk de additionele technische verantwoordelijkheden. De applicatie dient veilig de LTI authenticatie flow te implementeren en de Brightspace gebruikers, role en context te mappen op het eigen model. Ook moet er oog blijven voor privacy, security, data minimalisatie en least-priviledge access en onderhouden worden.  
Een maatwerk implementatie geeft de best functionele oplossing, maar in de evalutatie dient naast het ontwikkel werk ook het onderhoud en de operationele kosten mee gewogen worden. 

## Conclusie

Het initiele onderzoek geeft nog niet een voorkeursoplossing, echter een gereduceerde set van mogelijke oplossingen, die in volgende hoofstukken verder uitgediept gaan worden. Academeny Attendance en RegisterBlast vallen op omdat deze specifiek voor hoger onderwijs registratie functionaliteit bieden met een gedocumenteerde Brightspace integratie. Hiermee zijn dit realistische alterantieven voor een maatwerk oplossing. De maatwerk oplossing biedt de mogelijkheid om binnen de technisch mogelijkheden aan alle eisen te voldoen. Hierstaan dan wel technische en organisatorisch verantwoordelijkheid tegenover. 
In de volgende stappen gaan Academy Attendance, RegisterBlast en een maatwerkoplossing verder uitwerken tegen alle requirements, implementatie effort, integratie mogelijkheden en lange termijn onderhoud en eigenaarschap.  