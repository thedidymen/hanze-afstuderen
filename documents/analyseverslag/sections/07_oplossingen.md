# Oplossingen

## Inleiding

Verschillende oplossingsrichtingen zijn onderzocht voor de Sign-Up Tool. De alternativen rangen van bestaande Brightspace functionaliteit (de huidige situatie), tot commerciele plannings tools en een zelfbouw applicatie. De requirements uit het vorige hoofdstuk zijn gebruikt als initiele selectie criteria. Hierbij zijn vooral de must criteria mee genomen, denk hierbij aan tijdslots, capaciteit, privacy, overzicht, Brightspace integratie, SSO etc. 

## Bright Space Groups

In de huidige situatie worden de zelfenrolment groepen van Brightspace gebruikt als tijdslots. Dit is in de huidige situatie uitgebreid besproken. Deze functionaliteit is vooral bedoeld om studenten in leergroepjes in te delen ipv assesment registratie. Dit vormt het uitgangspunt waar tegen we nieuwe oplossingen houden. 

## Algemene Plannings tools

Verschillende algemene plannings tools zijn overwogen, Calendly, SimpleBook.me en Cal.com. Deze producten voorzien in de basis functies die nodig zijn voor de Sign-Up Tool, zoals configurerbaarheid, tijdsduur, zelfboeken etc.  

Calendly [@calendly] is een volwassen commerciele plannings platform dat zowel individuele en groep evenmenten integreert met een kalender en identiteit platforms. Het is voornamelijk ontworpen rond afspraken tussen organisators en uitgenodigden, dan voor educationele evenementen gekoppeld aan een LMS course. Er is geen makkelijke koppeling met Brightspace gevonden. Calendly gebruikt een link en neemt dus niet de context van Brighspace mee (NF-INT-02, FN-CON-01, NF-AUT-02).  

SimplyBook.me [@simplybook] biedt een breder boeking systeem met klassen en groeps boekingen, configureerbare capaciteit, wachtlijsten en administrative functionaliteiten. Functioneel ligt dit dichterbij de vereiste registratie proces dan een basis afspraken planner. Echter is dit meer een alleenstaande boekings platform, voor een zelfstandig ondernemer. Er is geen Brightspace integratie gevonden, dit zou dus door een apart sync proces moeten gebeuren. Dit conflicteerd met de gewenste Brightspace integratie en authenticatie (NF-INT-02, NF-AUT-01, FN-CON-01).  

Cal.com [@cal.com] is een open source tool dat zelf op een server gehost kan worden en geeft dus meer technische controle. Zelf-hosting geeft ook voordelen t.a.v. data eigenaarschap en uitbreidbaarheid. Het ondersteunt individuele en team planningen. Primair is dit een planner platform en niet perse geschikt voor een LMS intregratie. Deze integratie zou zelf ontwikkelt moeten worden en effectief een maatwerk oplossing (NF-INT-02, NF-AUT-02, FN-CON-01).  

Deze producten laten zien dat planner software beschikbaar is. De grootste beperking zit niet in het maken van tijdslots maar in het integreren met de educationele content. Zonder de Brightspace integratie, is het lastig om gebruik te maken van de Brightspace context.  
Hierom zijn algemene plannings tools niet geselecteerd voor de shortlist. Hiervoor is gekeken naar producten met een duidelijke Brightspace integratie. Microsoft bookings is hierop een uitzondering door de sterke relatie met het bestaande Microsoft 365 omgeving. 

## TimeEdit

TimeEdit [@timeedit] is onderzocht omdat het academisch planning, studenten planning en registratie functionaliteit bevat. Hierbij kunnen ook acties als zelf-registratie, configureerbare groep capaciteit, registratie periodes, dit overlapt sterk met de behoeften voor de Sign-Up Tool.  
Echter, is TimeEdit voornamelijk gericht op modules, geplande activiteiten en studentengroepen. De workflow voor een sigh-up event lijkt niet aanwezig (FN-ETM-01, FN-ETM-03, FN-DRO-04). Hoewel Brightspace integratie wordt benoemt, lijkt deze meer gefocust rond de synchronisatie van courses en planningen en faciliteerd het niet een LTI 1.3 integratie voor de overdracht van authenticeerde gebruikers, course context en rollen (NF-INT-02, FN-CON-01).  
Een praktisch evalutatie was niet mogelijk door het ontbreken van een test omgeving of een video van de werking.  
TimeEdit blijft mogelijk relevant omdat de Hanze deze tool al gebruikt [@TimeEditAcademy] [@JaarverslagHanze23].

## Zoom LTI Pro / Easy Scheduler

Zoom LTI Pro [@zoom] is een relevante alternatief omdat het Easy Scheduler werkt binnen een LMS. Docenten kunne beschikbare tijdslots publiceren en studenten kunnen afspraken selecteren en annuleren vanuit de LTI interface. Hierbij wordt gebruik gemaakt van LTI 1.3 dat kan combineren met Brightspace.  
Easy Scheduler is primair geschikt voor een-op-een afspraken, in plaats van de gewenste multi-student assesments (FN-ETM-04) ook lijkt het overzichtg van studenten niet haalbaar (FN-DRO-05).

## Academy Attendance

Academy Attendance [@yournextconcepts] is specifiek ontworpen voor hoger onderwijs en heeft documentatie voor Brightspace integratie. Daarnaast is het gehost binnen Europa en biedt het documentatie t.a.v. AVG.  
Academy Attendance heeft een personlijk view voor studenten, docenten en administators. De eigenschapen hiervan komen dicht bij de requirements van de Sign-Up Tool, inclusief student registratie, capaciteit management en rol afhankelijke informatie.  


## RegisterBlast

Ook deze tool [@registerblast] is specifiek ontwikkelt voor het hoger onderwijs en bevat exam planning, evenement planning en materiaal planning. Evenementen registraties kunnen datums, deadline, herplanning en rappotering bevatten. Daarnaast ondersteunt RegisterBlast LTI 1.3 en SSO. De Brightspace integratie maken dit een interessante kandidaat, maar er blijven wat vraagtekens rond Europese hosting, AVG en of het model overweg kan met de assesment werkflow van de Hanze.  

## Microsoft Bookings



## Maatwerk

Een ander alternatief is het zelf binnen de hanze een Sign-Up Tool ontwikkelen. In tegenstelling tot een bestaand product kan deze oplossing vollidig worden aangepast op de eisen (uiteraard binnen de mogelijke technishe kaders). Het grootste voordeel is natuurlijk de controle die er is over het project. Het datamodel, gebruikerservaringen, privacy en security, en Brightspace integratie kunnen allemaal specifiek worden gemaakt, in plaats van het proces aan passen aan de beperkingen van een bestaand product.  
Hier tegenover staat natuurlijk de additionele technische verantwoordelijkheden. De applicatie dient veilig de LTI authenticatie flow te implementeren en de Brightspace gebruikers, role en context te mappen op het eigen model. Ook moet er oog blijven voor privacy, security, data minimalisatie en least-priviledge access en onderhouden worden.  
Een maatwerk implementatie geeft de best functionele oplossing, maar in de evalutatie dient naast het ontwikkel werk ook het onderhoud en de operationele kosten mee gewogen worden. 

## Conclusie