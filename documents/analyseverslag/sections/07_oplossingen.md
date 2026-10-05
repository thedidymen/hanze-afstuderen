# Oplossingen

## Inleiding

Verschillende oplossingsrichtingen zijn onderzocht voor de Sign-Up Tool. De alternatieven variëren van bestaande Brightspace-functionaliteit (de huidige situatie) tot commerciële planningstools en een zelfbouwapplicatie. De requirements uit het vorige hoofdstuk zijn gebruikt als initiële selectiecriteria. Hierbij zijn vooral de must-criteria meegenomen, zoals tijdslots, capaciteit, privacy, overzicht, Brightspace-integratie en SSO. 

### Brightspace Groups

In de huidige situatie worden de zelfinschrijvingsgroepen van Brightspace gebruikt als tijdslots. Dit is in de huidige situatie uitgebreid besproken. Deze functionaliteit is vooral bedoeld om studenten in leergroepjes in te delen in plaats van voor assessmentregistratie. Dit vormt het uitgangspunt waaraan we nieuwe oplossingen toetsen. 

## Overwogen oplossingen

Mogelijke oplossingen zijn gevonden door verkennend te zoeken met Google en ChatGPT. Zoektermen waren gericht op combinaties van planningstool, zelfregistratie, assessmentplanning, Brightspace, D2L en LTI-integratie. Het doel hiervan was om een brede set mogelijke oplossingen te verzamelen. 

### Algemene planningstools

Verschillende algemene planningstools zijn overwogen, waaronder Calendly, SimpleBook.me en Cal.com. Deze producten voorzien in de basisfuncties die nodig zijn voor de Sign-Up Tool, zoals configureerbaarheid, tijdsduur en zelf boeken.  

Calendly [@calendly] is een volwassen commercieel planningsplatform dat individuele en groepsevenementen integreert met een kalender en identiteitsplatforms. Het is voornamelijk ontworpen voor afspraken tussen organisatoren en genodigden, en niet voor educatieve evenementen die gekoppeld zijn aan een LMS-cursus. Er is geen makkelijke koppeling met Brightspace gevonden. Calendly gebruikt een link en neemt dus niet de context van Brightspace mee (NF-INT-02, FN-CON-01, NF-AUT-02).  

SimplyBook.me [@simplybook] biedt een breder boekingssysteem met klassen en groepsboekingen, configureerbare capaciteit, wachtlijsten en administratieve functionaliteiten. Functioneel ligt dit dichter bij het vereiste registratieproces dan een basisafsprakenplanner. Het is echter meer een zelfstandig boekingsplatform voor een ondernemer. Er is geen Brightspace-integratie gevonden; dit zou dus via een apart synchronisatieproces moeten gebeuren. Dit conflicteert met de gewenste Brightspace-integratie en authenticatie (NF-INT-02, NF-AUT-01, FN-CON-01).  

Cal.com [@cal.com] is een open-sourcetool die zelf op een server gehost kan worden en geeft dus meer technische controle. Zelfhosting biedt ook voordelen ten aanzien van data-eigenaarschap en uitbreidbaarheid. Het ondersteunt individuele en teamplanningen. Primair is dit een planningsplatform en niet per se geschikt voor een LMS-integratie. Deze integratie zou zelf ontwikkeld moeten worden en is daarmee effectief een maatwerkoplossing (NF-INT-02, NF-AUT-02, FN-CON-01).  

Deze producten laten zien dat planningssoftware beschikbaar is. De grootste beperking zit niet in het maken van tijdslots, maar in de integratie met educatieve inhoud. Zonder de Brightspace-integratie is het lastig om gebruik te maken van de Brightspace-context.  
Daarom zijn algemene planningstools niet geselecteerd voor de shortlist. Hiervoor is gekeken naar producten met een duidelijke Brightspace-integratie. Microsoft Bookings is hierop een uitzondering vanwege de sterke relatie met de bestaande Microsoft 365-omgeving. 

### TimeEdit

TimeEdit [@timeedit] is onderzocht omdat het functionaliteit biedt voor academische planning, studentenplanning en registratie. Hierbij zijn ook functies als zelfregistratie, configureerbare groepscapaciteit en registratieperiodes beschikbaar. Dit overlapt sterk met de behoeften voor de Sign-Up Tool.  
TimeEdit is echter voornamelijk gericht op modules, geplande activiteiten en studentengroepen. De workflow voor een sign-upevenement lijkt niet aanwezig (FN-ETM-01, FN-ETM-03, FN-DRO-04). Hoewel Brightspace-integratie wordt benoemd, lijkt deze meer gericht op de synchronisatie van cursussen en planningen. De integratie faciliteert geen LTI 1.3-overdracht van geauthenticeerde gebruikers, cursuscontext en rollen (NF-INT-02, FN-CON-01).  
Een praktische evaluatie was niet mogelijk door het ontbreken van een testomgeving of een video van de werking.  
TimeEdit blijft mogelijk relevant omdat de Hanze deze tool al gebruikt [@TimeEditAcademy] [@JaarverslagHanze23].

### Zoom LTI Pro / Easy Scheduler

Zoom LTI Pro [@zoom] is een relevant alternatief, omdat Easy Scheduler binnen een LMS werkt. Docenten kunnen beschikbare tijdslots publiceren en studenten kunnen afspraken selecteren en annuleren vanuit de LTI-interface. Hierbij wordt gebruikgemaakt van LTI 1.3, dat kan worden gecombineerd met Brightspace.  
Easy Scheduler is primair geschikt voor een-op-eenafspraken in plaats van de gewenste assessments met meerdere studenten (FN-ETM-04). Ook lijkt een overzicht van studenten niet haalbaar (FN-DRO-05).  

### Microsoft Bookings

Microsoft Bookings [@bookings] is onderdeel van het Microsoft 365-ecosysteem. Dit wordt momenteel gebruikt door de Hanze en is daarmee interessant, omdat het niet speciaal onboarded hoeft te worden. Er wordt dus ook geen nieuw extern platform geïntroduceerd. 
Functioneel past de werking van Bookings bij de gewenste workflow. Het ondersteunt configureerbare services, beschikbaarheid en groepsafspraken met een maximumaantal deelnemers. De regisseurs en docenten beheren de services, afspraken en deelnemerinformatie, terwijl Bookings direct integreert met Outlook en Teams. 
Enkele kerneisen kunnen echter niet worden geborgd. Microsoft ondersteunt LTI 1.3-integratie tussen Microsoft 365 en Brightspace, maar Bookings is niet een van deze applicaties. Hierdoor kan niet automatisch gebruik worden gemaakt van de Brightspace-cursuscontext en -rollen (NF-INT-02, FN-CON-01, NF-AUT-02).
Ook lijken het tonen van de resterende capaciteit (FN-SR-06) en de beperking tot één registratie per student (FN-SR-09) binnen een evenement niet mogelijk. 
Bookings is een handige tool omdat het al onderdeel is van de bestaande Microsoft-omgeving, maar sluit niet goed aan op de kerneisen. 

### ConexED

ConexED [@connexed] is een platform dat is ontworpen voor het hoger onderwijs. Het ondersteunt het maken van afspraken en evenementen, capaciteitsmanagement, verslaglegging en verschillende gebruikersrollen. In de documentatie wordt gesproken over D2L Brightspace en ondersteuning voor SSO. Hiermee wordt voldaan aan een aantal belangrijke must-requirements van de Sign-Up Tool.  
In de beschikbare documentatie wordt echter niet verder ingegaan op de Brightspace-integratie met LTI 1.3 (NF-INT-02, FN-CON-01, NF-AUT-02). Ook is onvoldoende gedocumenteerd of de gewenste assessmentworkflow kan worden ondersteund (FN-ETM-01, FN-ETM-03, FN-DRO-04). Daarnaast worden de gebruikersgegevens gehost in de VS.  
Vanwege deze uitdagingen is ConexED niet op de shortlist gekomen. 

## Shortlist

Het initiële onderzoek is gebruikt om het aantal mogelijke opties terug te brengen tot een shortlist. Criteria hiervoor zijn dat er geen conflict is met een must-requirement en dat er voldoende aanleiding is om de beoogde workflow te ondersteunen.  
Selectie voor de shortlist is geen garantie dat de oplossing ook voldoet aan alle requirements. Hiervoor is verder onderzoek en vergelijking tussen de oplossingen nodig. Voor de initiële selectie zijn alle mogelijke oplossingen getoetst aan de must-requirements en de beoogde workflow op basis van de huidige situatie. 
 
Om de vergelijking leesbaar te houden, zijn de must-requirements samengevoegd in zeven groepen:  
- Tijdslots - Het creëren en configureren van Sign-Up-evenementen, metadata, tijdslots, capaciteit en slotstatus, en de mogelijkheid om een evenement op te zetten (FN-ETM-01, FN-ETM-02, FN-ETM-03, FN-ETM-04, FN-ETM-09, FN-DRO-04).  
- Registratie - De zelfregistratie voor een evenement, het bekijken van de eigen registratie, het zien van de beschikbaarheid en het voorkomen van dubbele registraties (FN-SR-01, FN-SR-05, FN-SR-06, FN-SR-09).  
- Docenten - Deelname- en tijdslotoverzicht en het genereren van een deelnamelijst (FN-DRO-01, FN-DRO-02, FN-DRO-05, FN-EXP-01).
- Context - Het koppelen van een evenement aan de educatieve context, RBAC via Brightspace, Brightspace-integratie en SSO (FN-CON-01, FN-CON-03, NF-INT-01, NF-INT-02, NF-AUT-01, NF-AUT-02).  
- Privacy & Security - Dataminimalisatie, inzicht in de eigen registratie, security-by-design, least-privilege-toegang en minimale data-exports (NF-PS-01, NF-PS-02, NF-PS-03, NF-PS-07, NF-PS-08, FN-EXP-04).  
- Onderhoudbaarheid - Het gebruik van onderhoudbare en ondersteunde technologie en de scheiding van presentatie, integratie en data (NF-MA-01, NF-MA-04).  
- Data - Simultaan gebruik zonder overplanning, dubbele registraties en partiële of inconsistente registraties (NF-BDI-01).  

In de onderstaande @tbl:initial-solution-screening geeft een + voldoende bewijs dat aan de must-requirements in de groep kan worden voldaan. Een ? geeft aan dat de oplossing de groep ondersteunt, maar dat een of meer requirements op basis van de documentatie niet of slechts gedeeltelijk kunnen worden gecontroleerd. Een - betekent dat ten minste één must-requirement conflicteert met de beoogde functionaliteit. 

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

\* De maatwerkoplossing heeft geen inherente productbeperkingen binnen de technische mogelijkheden. Dit betekent niet dat de functionaliteit al bestaat of dat er al aan de requirements wordt voldaan. 

Op basis van deze criteria blijven er drie alternatieven over voor verdere evaluatie:
- Academy Attendance
- RegisterBlast
- Maatwerk

### Academy Attendance

Academy Attendance [@yournextconcepts] is specifiek ontworpen voor het hoger onderwijs en heeft documentatie over Brightspace-integratie. Daarnaast wordt het gehost binnen Europa en biedt het documentatie over de AVG.  
Academy Attendance heeft een persoonlijk overzicht voor studenten, docenten en administrators. De eigenschappen hiervan sluiten aan bij de requirements van de Sign-Up Tool, waaronder studentenregistratie, capaciteitsmanagement en rolafhankelijke informatie.  


### RegisterBlast

Ook deze tool [@registerblast] is specifiek ontwikkeld voor het hoger onderwijs en bevat examenplanning, evenementenplanning en materiaalplanning. Evenementregistraties kunnen datums, deadlines, herplanning en rapportage bevatten. Daarnaast ondersteunt RegisterBlast LTI 1.3 en SSO. De Brightspace-integratie maakt dit een interessante kandidaat, maar er blijven vragen over Europese hosting, de AVG en de vraag of het model overweg kan met de assessmentworkflow van de Hanze.  

### Maatwerk

Een ander alternatief is om binnen de Hanze zelf een Sign-Up Tool te ontwikkelen. In tegenstelling tot een bestaand product kan deze oplossing volledig worden aangepast aan de eisen (uiteraard binnen de technische mogelijkheden). Het grootste voordeel is de controle over het project. Het datamodel, de gebruikerservaring, privacy en security, en de Brightspace-integratie kunnen allemaal specifiek worden vormgegeven, in plaats van het proces aan te passen aan de beperkingen van een bestaand product.  
Daartegenover staan natuurlijk de aanvullende technische verantwoordelijkheden. De applicatie dient de LTI-authenticatieflow veilig te implementeren en de Brightspace-gebruikers, rollen en context aan het eigen model te koppelen. Ook moet er aandacht blijven voor privacy, security, dataminimalisatie en least-privilege access, en moet de applicatie worden onderhouden.  
Een maatwerkoplossing kan direct rond de requirements worden ontworpen, maar bij de evaluatie moeten naast het ontwikkelwerk ook het onderhoud en de operationele kosten worden meegewogen. 

## Conclusie

Het initiële onderzoek levert nog geen voorkeursoplossing op, maar wel een gereduceerde set mogelijke oplossingen die in volgende hoofdstukken verder worden uitgewerkt. Academy Attendance en RegisterBlast vallen op omdat ze specifiek voor het hoger onderwijs registratiefunctionaliteit bieden met een gedocumenteerde Brightspace-integratie. Hiermee zijn dit realistische alternatieven voor een maatwerkoplossing. De maatwerkoplossing biedt de mogelijkheid om binnen de technische mogelijkheden aan alle eisen te voldoen. Daar staan wel technische en organisatorische verantwoordelijkheden tegenover. 
In de volgende stappen worden Academy Attendance, RegisterBlast en een maatwerkoplossing verder geëvalueerd aan de hand van alle requirements, de implementatie-inspanning, integratiemogelijkheden en het langetermijnonderhoud en -eigenaarschap.  