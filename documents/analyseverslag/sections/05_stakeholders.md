# Stakeholders

## Inleiding

Dit hoofdstuk indentificeerd de stakeholders binnen het Sign-up Tool project en hun relevantie tot het onderzoek en ontwerp proces. De analyse is gebaseert op de opdracht, de huidige situatie en de stakeholder interviews (zie bijlages). Het doel is om tot een zo compleet mogelijk overzicht te komen van de stakeholders. 

De stakeholder analyse evalueert de stakeholders op basis van de invloede op het project en de interesse in uitkomst. Het doel is om niet aleen vast te stellen wie er betrokken zijn, maar ook hoe elke stakeholder kan bijdragen aan het succes van het project. 

De analyse is gebaseerd op de Mendelow's stakeholder matrix [@mendelow1981]. In deze analyse wordt gebruik gemaakt van de Invloed-Interesse matrix [@pmi2021]. Stakeholders met een hoge invloed en een hoge interesse worden contenu betrokken bij het proces, terwijl stakeholders met een lage invloed gebruikt worden voor domein kennis. 

De Sign-up tool raakt verschillende organisatorische lagen. Naast de directe eindgebruikes binnen Verpleegkunde, raakt de tool ook business architectuur, platform integratie informatie management, privacy, security, etc. Als gevolg hier van kunnen beslissingen niet alleen gebaseerd zijn op de functionele vereisten van de eindgebruikers. De oplossing zal ook moeten voldoen aan Hanze-brede archtectuur principes, technisch standarden en organisatorische verantwoordelijlheden. 

Het doel van deze analyse is drievoudig:  
- indentificatie van stakeholders  
- inzichtlijk krijgen van de verschillende interesses en verantwoordelijkheiden van de stakeholders  
- vaststellen hoe stakeholders betrokken moeten blijven bij de rest van het project.

Het resultaat van deze analyse vormt de basis voor de requirement analyse en voor de latere oplossings richting. 

## Overzicht Stakeholders 

De stakeholders zijn geindentificeerd op basis van 3 bronnen: de oorspronkelijke opdracht, de huidige situatie en de stakeholder interviews. De directe stakeholders zijn de gebruikers van de sign-up tool. Een tweede groep bestaat uit de organisatorische en technisch stakeholders. De laatste groep bestaat uit betroken/getroffen stakeholders die niet direct geinterviewd zijn. 

| Stakeholders | Rol | Geinterviewd | Relevantie |
|---|---|---|---|
| Regiseur | Bereid voor en coordineerd registratie momenten | Ja | Business stakeholder en proces eigenaar |
| Docenten | Gebruikers van registratie overzicht ter voorbereiding en uitvoering assesments | Gedeeltelijk | Directe gebruikers van Sign-Up Tool |
| Studenten | Gebruikers van de tool | Nee | Eindgebruikers van de Sign-Up Tool |
| IT instructeur | Begrip van huidige workaround | Ja | Kennis van technisch praktise beperkingen |
| Collabspace | Development | Ja/Nee | Project supervisie |
| BS&IT Business archtectuur | Stelt achtectuur kaders voor software development vast | Ja | Standaarden, eigenaarschap continuteit |
| Informatie management | Verbindt Verpleegkunde behoefte aan Hanze-breede informatie | Ja |  |
| Hanze Integratie Platform | integratie kennis, technisch standarden, onderhoud | Ja | Mogelijke landigsplaats applicatie |
| Privacy | Advies over persoonsdata | Ja | Essentieel omdat de tool persoonsgegeven verwerkt |
| Security | Advies over security en risk assesments | Ja | Essentieel voor access control, security design en operationele risico |
| Brightspace engineers | Advies over LMS mogelijkheden, beperkingen en mogelijke integratie zoals LTI | Ja | De tool wordt gebruikt vanuit Brightspace |
| Webroom | Geeft informatie over lokalen, datums, tijden en docenten | Nee | Informatie bron van basis data voor de applicatie |
| School Verpleegkunde | Huidig afnemer van de tool | Gedeeltelijk | Overkoeplende organisatie van initele gebruikers |
| Andere Schools | Toekomstige afnemers van de tool | Nee | Mogelijk toekomstige doelgroep |

: Stakeholder overview for the Sign-up Tool project {#tbl:stakeholder-overview}

## Geinterviewde stakeholders

### Regiseur Verpleegkunde / Mirjam Veenstra

De regiseur van verpleegkunde is de primare business stakeholder. Binnen het huidige process, vertaald de regiseur de beschikbare planning in registratie momenten en bereid deze voor in Brightspace. Vanuit het interview wordt duidelijk dat deze rol graag een gebruiksvriendelijker en meer herbruikbare proces wil, bijvoorkeur waar de regiseur niet of zo min mogelijk afhankelijke is van externe partijen. 

Deze stakeholder heeft veel praktische invloed op de de requirements, omdat de tool de manier van voorbereiden van de assesments ondersteunt. 

### Docenten Verpleegkunde / Mirjam Veenstra

De docenten zijn directe gebruikers van de tool. Ze moeten zien welke studenten geregistreerd zijn voor een assesment, ook is er behoefte aan een overview van alle assesments binnen vak/module. Docenten beijken momenteel de afzonderlijke groepen binnen Brightspace om tot een complete lijst te komen van de registreerde studenten. 

De docenten zijn niet als seperate groep geinterviewd. Mevr. Veenstra is naast haar rol als docent ook regiseur binnen verpleegkunde. 

### BS&IT / Arno de Boer

Vanuit de business archtectuur is het maken van de Sign-up tool een praktische usecase om te kijken hoe de Hanze zelf software kan gaan ontwikkelen. Wie is de eigenaar? Wie onderhoudt het? Welke standaarden zijn van toepassing?

Deze stakeholder heeft veel invloed op het project omdat architectuur principes, plaatsing binnen de organisatie en technnische standaarden een sterke invloed hebben op de richting van de oplossing. De interresse in het project is ook hoogl, omdat het project de input geeft voor richtlijnen voor bredere software ontwikkeling binnen de Hanze. 

### IT instructor / Jos Ensing

De IT instructor is de bron voor het begrijpen van de huidige werkwijze. Hoe de huidige groepstool oneigenlijk wordt gebruikt voor het oplossen van huidige probleem. Dit is een belangrijk perspectief omdat het functionele probleem wordt gekoppeld aan de beperking van de het huidige LMS. 

Deze stakeholder benoemt ook de privacy risicos van de huidige werkwijze, studenten kunnen van iedereen zien wie er geregistreerd hebben. 

### Brightspace / Maurits Hoogerwerf

De Sign-up tool moet beschikbaar zijn vanuit de LMS-context (Brightspace). Met de functioneel beheerder van Brightspace binnen de Hanze is er gekeken naar in hoeverre de huidige functionaliteit, plugins of integratie technieken de huidige usecase kunnen ondersteunen. 

Deze stakeholder heeft een grote invloed op de integratie mogelijkheden. De functioneel beheerders zijn niet de eigenaar van het bedrijfsproces, maar beheren wel de omgeving waar mee docenten en leerlingen toegang krijgen de applicatie. 

### HIP / Henk Hoekstra

Het Hanze Integratie Platform is binnen de Hanze een logische plek waar een mogelijke applicatie zou kunnen landen. Binnen dit interview is er gekeken naar integratie, onderhoudbaarheid en technisch eigenaarschap. 

Het HIP heeft een grote invloed op de integratie en onderhoudbaarheid van de applicatie, zeker als op langere termijn (voorbij de mvp) de applicatie binnen het HIP zou landen. 

### Informatie management / Ronald Steenstra

Informatie managemant is relevant voor de Sign-Up tool zodat het niet een oplossing wordt die past binnen Verpleegkunde, maar niet meer toepasbaar is binnen de andere Schools binnen de Hanze. Informatie management bewaakt de grens dat het een generieke tool wordt. 

Deze stakeholder heeft een grote interrese in de scope, herbruikbaarheid, procesuitlijning en implementatie. De invloed is groot, zeker zodra dit een Hanze-brede oplosing wordt ipv van een lokaal prototype. 

### Privacy / Wouter Knevelbaard

Privacy zijn van groot belang voor de Sign-Up tool, door dat de requirements de scope van oplossingen sterk kunnen beperken. Ook is er een groot belang omdat de huidige werkwijze privacy problemen met zich mee brengt, de nieuwe tool moet deze problemen voorkomen. 

### Security / Arjen Sterenborg

Voor security gelden vergelijkbare belangen, maar dan vooral gericht op de security aspecten. 

### CollabSpace / Cor Blom / Reijer van der Zande

Vanuit CollabSpace is het huidige project ontwikkelt. Het huidige project gelt als pilot project om te kijken hoe studenten aan de Hanze software kunnen ontwikkelen voor de Hanze. CollabSpace heeft hierbij dus een belandt voor haalbaarheid, educative waarde, goede documentatie en overdraagbaarheid. 

CollabSpace is niet een eindgebruiker van de Sign-Up tool, maar heeft een sterke invloed op hoe het project wordt uitgevoerd en gedocumenteerd. 

## Niet geinterviewde stakeholders

### Studenten

Studenten zijn niet direct geinterviewd binnen het huidige onderzoek. Dit is een beperking omdat studenten primare eindgebruikers zijn. Echter zijn er duidelijke beschrijvingen van docenten hoe studenten de applictatie gebruiken. 

Binnen de huidige fase, zijn de behoeften van de studenten vertegenwoordigt als afgeleide eisen rond duidelijkheid, minimale data oppervlak en simpele registratie mogelijkheden. Idealiter vindt er later in het proces nog een evalutatie plaats over de user interface. 

### Bredere groep docenten

Er is geen interview gedaan met een bredere groep docenten. Vanuit het verpleegkunde interview is al een duidelijk persectief van de regiseur en docenten verkregen. Op dit moment wordt er niet veel gewonnen door hier nog veel tijd in te steken. Net als bij de studenten kan het handig zijn deze groep te betreken bij een evaluatie van de user interface. 

### Andere schools

Momenteel wordt de Sign-up tool toe gespist op het gebruik door Verpleegkunde, waar mogelijk wordenn er gekeken om de requerement zo generiek mogelijk te houden. Hiermee wordt getracht om de wijzigingen die nodig zijn voor een generieke tool zo minimaal mogelijk te maken. Binnen deze opdracht wordt hier niet specifiek onderzoek naar gedaan. 

### Webroom

Dit is een operationele afhankelijkheid die gebruikt wordt door verpleegkunde. Vanuit webroom ontvangt verpleegkunde informatie zoals datum, tijd, lokaal en docent doormiddel van het bestaand plannings process. Dit onderzoek gebruikt de informatie vanuit het verpleegkunde interview. Mocht er in de toekomst een directe link komen tussen de plannings tool en de Sign-Up Tool kan hier verder naar gekeken worden. 

### Toekomstige technische eigenaar

Momenteel is het nog onduidelijk waar deze tool precies gaat landen. Hiervoor zijn verschillende opties. 

### Producent bestaande oplossing

Externe producenten zijn momenteel niet geinterviewd, omdat de huidige stakeholder analyse zich focussed op de interne behoefted en beperkingen. Mogelijk wordt deze partij relevant na de vergelijking tussen oplossingen, zeker als een bestaand SaaS oplossing of een LMS plugin worden overwogen. Op dit moment zijn dit niet primare stakeholders in deze analyse. 

## Stakeholder relaties

Hoewel elke stakeholder zijn eigen rol heeft, kan dit project alleen een succes worden door samenwerking tussen edicationele, organisatorisch en technische stakeholders. 

De School van verpleegkunde is verantwoordelijk voor de functionele vereisten. De regiseur, docenten, IT instructeur en studenten direct betroken bij het organiseren van de assesment en bepalen daar mee de functionaliteit van de applicatie. 

BS&IT vertalen deze requirements naar organisatorische en archtectuur vereisten. Ook evalueert of BS&IT of deze development strategy als basis kan dienen voor verdere ontwikkeling binnen de Hanze. 

Het HIP geeft de basis voor de technische integratie en koppelingen van systemen binnen de Hanze. 

Brightspace geeft de operationele omgeving waar binnen de applicatie moet draaien en gebruikt worden. De mogelijkheden en onmogelijkheden van Brightspace zijn van directe invloed op de oplossing. Bestaande API's, authenticatie mechanismes etc. bepalen of de functionaliteit als extensie of als standaalone applicatie geintegreerd kunnen worden. 

De Privacy en Security stakeholders bepalen de requirements van de organisatie t.a.v. personlijke data, toegankelijkheid en informatie beveiliging. Deze aanbevelingen bepalen sterk het functionele en technische ontwerp. 

## Stakeholderanalyse

De Mendelow matrix in @fig:mendelow_matrix groepeerd stakeholder naar hun invloed en interesse in het project. Deze classificatie is gebaseerd op de stakeholders interviews. In de onderstaande tabel (#tbl:mendelow-explanation) wordt een rationale en een communicatie strategy gegeven. 

![Mendelow matrix voor de  Sign-up Tool stakeholder](assets/generated/mendelow_matrix.png){#fig:mendelow_matrix width=90%}

| Quadrant | Stakeholders | Rationale | Communicatie |
|---|---|---|---|
| Manage | Regiseur, BS&IT Architectuur, Informatie Management, Privacy, Security, Brightspace, IT Instructeur, CollabSpace | Deze stakeholder hebben veel invloed op o.a.: haalbaarheid, privacy, security en integratie. Daarnaast hebben ze veel interesse en belang bij de uitkomst. | Frequente afstemming, toetsing van de requirements en ontwerp review. |
| Tevreden | Technisch Beheerder, HIP | Deze stakeholders hebben veel invloed op onderhoudbaarheid, zelfs zonder dat ze direct betroken zijn bij het dagelijks gebruik. | Betrekken bij overdrachts milestones. Bevestigen van verantwoordelijkheden voor productie besluiten. |
| Informeren | Docenten, Andere Schools | Dit zijn betrokken stakeholders met interesse in het eindproduct,  | Samenvatting, prototypes en validatie momenten. zonder direct zelf invloed te hebben hierop. |
| Monitor | Webroom, Studenten | Deze groep heeft een beprekt interesse en invloed op de tool | Volg afhankelijkheden en betrekken bij concrete veranderingen zoals integratie en operationele wijzigingen |

: Mendelow matrix {#tbl:mendelow-explanation}


## Governance en eigenaarschap

Een van de nog openstaande vragen na de interviews is waar de applicatie moet landen an voltooing. De School van verpleegkunde is eigenaar van het business proces en stelt daarmee de functionele requirements vast. BS&IT is verantwoordelijk voor de archtectuur standaarden, lifecycle management en de organisatorische continuiteit. Voor de directe technische onderhoud is echter niet meteen een aangewezen partij. Dit zou kunnen landen bij HIP, of mogelijk bij Collabspace. 

## Beperkingen van de stakeholder analyse

De stakeholder analyse geeft een breed overzicht van de omgeving van het project, echter zijn er ook beperking van de anaylse.

Ten eerst zijn niet alle stakeholders geinterviewd, sommige belangen zijn afgeleid van anders stakeholders die direct bij het proces betrokken zijn. 

Ten tweede focust het project zich momenteel allen op de implementatie van de tool binnen verpleegkunde. Hoewel de oplossing breed toepasbaar zou moeten zijn binnen de Hanze, zijn deze gebruikers niet mee genomen in de analyse. 

Het project is een pilot van de organisatie om te kijken of studenten in gezet kunnen worden voor de ontwikkeling van niet kritische software ontwikkeling. Discussies omtrent de eigenaarschap/onderhoud van de applicatie worden nog steeds gevoerd. Als gevolg hiervan zijn de analyses omtrent eigenaarschap not niet definitief, en zouden in de toekomst kunnen veranderen. 

Ondanks deze beperkingen zijn alle grote groepen belanghebbende voor dit project geinterviewd of meegenomen in de analyse. De verzamelde informatie geeft een goede basis voor de requirements en de evaluatie voor de oplossing. 

## Conclusie

De stakelholder analysse laat zien dat het Sign-Up Tool project verder gaat dan alleen de implementatie van de registratie tool. Het vereist samenwerking tussen verschillende lagen van de Hanze. 

De school van verpleegkunde stelt de functionele vereisten vast, terwijl BS&IT, HIP, BrightSpace, Privacy en Security geven organisatorisch en technische beperkingen waarbinnen de oplossing moet werken. Deze verschillende perspectieven moeten samen komen to een functioneel en langtermijn oplossing. 

Het resultaat van de analyse geeft de basis voor de verdere requirement analysse. 