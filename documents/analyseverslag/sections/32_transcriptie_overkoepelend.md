# Transcriptie interview – Technische Kaders

## Transcriptieproces

Voor het uitwerken van de interviews is gebruikgemaakt van de transcribe tool van teams dat automatisch spraak omzet naar tekst.

De gegenereerde tekst is daarna opgeslagen in een tekstbestand en handmatig gecontroleerd en waar nodig gecorrigeerd op fouten in interpunctie, naamgeving en herkenning van gesproken woorden. 

## Algemene Informatie

| | |
|---|---|
| Datum | 20 april 2026 |
| Tijd | 11.30u - 12.30u |
| Locatie | Teams / ZP11 |
| Doel gesprek | Stakeholdergesprek voor Sign-Up Tool |

| Aanwezigen | Rol |
|---|---|
| Arno de Boer | Business Architect | 
| Ronald Steenstra | Informatiemanager | 
| Nils van der Deen | Cloud Engineer | 
| Reijer van der Zande | Developer |

## Transcriptie

### ~ 0 Min

Ronald Steenstra 0:03  
Gebeurt er ja kijk.
Ja, heel goed, We gaan bij jou, Arno jij gaat straks het beleid delen.

Arno de Boer 0:15  
Ja ik deel straks even het beleid met jullie over dat architectuurkader, Maar de kern Nils voor jou even om te weten is dat we We hebben Natuurlijk bijvoorbeeld een in data, hè? Dat is zelf ontwikkeld en wij willen eigenlijk meer de ontwikkeling toespitsen. Niet zozeer op de bedrijfskritische applicaties, maar op juiste dingen waarbij we waar nou wat er al zeiden, we markten nog niet toereikend genoeg is of waarbij we juist wat. Uniek uniekheid willen. Hebben zo bijvoorbeeld bij portaalontwikkeling dat soort dingen. Je ziet dat dat vaak? Hoe zeg je dat weinig risico's over het algemeen met zich meebrengt, maar wel heel veel toegevoegde waarde hè? Dus zo'n onderwijsportaal bijvoorbeeld is een dingetje dat, hè? De onderliggende systemen blijven hem gewoon intact, maar je je biedt het dan wel aan op een manier wat bij gebruikers er wat meer aan hebben. Dat is een beetje de kern eigenlijk van de het architectuur kader. Ja dus meer richting, nou noem ik dan `high value, low risk` en en de dingen die uit de markt kunnen halen gewoon uit de markt halen. Dat is een beetje het idee en dat deed ik wel even ja.

### ~ 1 Min

Nils van der Deen 1:21  
Ja oh ja.

Ronald Steenstra 1:22  
Ja heel goed nou ja, Reijer kwam op een gegeven moment in de lucht van nou, Ik heb een aantal punten die ik graag willen bespreken. Wil je er zelf een aantal? 

Reijer van der Zande 1:39  
Ik heb inderdaad al deels Natuurlijk met arno en het architectuur kader, dus dat geeft in ieder geval een deel van de antwoorden zeker op hoogover. Maar ik zit eigenlijk nog een stukje dat ik denk van ja, We moeten op op die laag daaronder het technische stukje moeten denk ik ook even wat wat duidelijkheden komen wat er wenselijk in is en wat daarvan niet kan, wat er wel kan. Ik wil even kijken of we dat een beetje kunnen uitdiepen en dan heb ik, denk ik in eerste instantie voor dat eerste stukje. De requirements heb ik dan alles te pakken en daar kan ik dan een stukje in het in de diepgang en kijken wat de mogelijke oplossing is nu.

### ~ 2 Min

Arno de Boer 2:07  
Oh mooi ja.

Reijer van der Zande 2:10  
Dus Dat was eigenlijk het doel van het gesprek, eigenlijk een beetje uitdiepen na die van dat iets verder van het hoogover was, maar eventjes wat praktisch daar dan ook mogelijk is.

Ronald Steenstra 2:15  
Ja, Ik wil straks zo benieuwd voordat we er dan gelijk hier naartoe gaan of jij heb jij bijvoorbeeld ook contact gehad met de opleiding zelf hierover of OK, Ik heb mijn verpleegkunde, heb ik al althans eigenlijk al zelf een hele tijd terug heb ik al een gesprek gehad wat wat hun graag zouden willen wat hun nodig hebben om dat te doen. Ik heb vorige week even een gesprek gehad met een.


Reijer van der Zande 2:42  
Heer van... ik de naam even kwijt, maar dat weten jullie vast van security en van. Privacy maar ze schrijft twee kleurenburg, sterenburg, Sterenburg of security. 

Ronald Steenstra 2:50  
Een Wouter Knevelbaard misschien of ja, ja dus. 

Reijer van der Zande 2:55  
Daar hebben we even vorige week gesprek mee gehad en Ik heb met Arno een gesprek gehad over de architectuurkaders. Nou voor mij heb ik dan in ieder geval wat ik binnen de organisatie wil bepalen. Eerst alle informatie, want daar heb ik vaak ook een beetje. 

### ~ 3 Min

Ronald Steenstra 3:15  
Ik ben ook benieuwd of zijn zij op de hoogte, zeg maar voor de voortgang. Of bij bij de opleiding op de hoogte van de voortgang bij de opleiding worden zij af en toe geïnformeerd. Of willen meer iets wat Ik kan doen? Of nou ja, 

Reijer van der Zande 3:28  
Ik heb het inderdaad toentertijd met hun een gesprek gehad. Ik heb sindsdien nog niet heel veel contracten met ze gehad. Ik wou. Ik, helaas ben ik één dag In de week hier en de rest van de week ben ik gewoon aan het werk en ik merk dat die dagen heel snel vollopen natuurlijk is. Dus ik zit, ze bent nog een beetje zoekende. Ik wilde eigenlijk even uitwerken en dan wil ik naar de verschillende mensen. Ook de de samenvatting en de transcriptie eventjes terugsturen op het moment van even commentaar kunnen geven. En, Dat is eigenlijk het punt waarop ik denk, nou, Dat is een stukje terugkoppeling en ik zit zelf te denken om misschien even Quick en Dirty een mock up te maken voor een wat voor hun requirements om te kijken of ik ze begrepen heb.

### ~ 4 Min

Arno de Boer 4:09  
Ja.

Reijer van der Zande 4:09  
Ja niet met van dit gaat het exact worden, want anders kan ik niet beloven, maar wel van zijn dit jullie wensen? 

Ronald Steenstra 4:23  
Ja, nee, heel goed nee, Maar ik bedoel ook vooral van. Gebruik maar eventueel ook Als je dat wil van om dat dingen terug te koppelen of werkt wat, Maar dat hoeft allemaal niet hoor. Als je dat gewoon direct zelfs doet is dat komt wel prima. Dus Het is meer dat je weet van nou, dan kun je mij ook voor inzetten.

Reijer van der Zande 4:30  
Een, Ik denk dat dat direct wel gaat lukken. Ik zal wel binnenkort even proberen om daar even wat op te doen. Ja punt ja. Terugkoppeling, verpleegkundige. Even kijken? Ik had een aantal. Dingetjes. In de eerste instantie zit ik nog, We hebben dat deels al vroeg besproken, maar. De de de eigenaarschap van de app, en ook die gaat daar dan. Nou en wat concreter ook naar van waar de hosting, wie daar de verantwoording voor gaat nemen. Een stukje monitoring stukje onderhoud, stukje updates. En wat de kennis is binnen? Het stukje wat Het gaat doen? Ja, ja. Eigenlijk heb eigenlijk de vraag wie het functioneel beheer gaat, gaat oppakken. Straks is dat het of. Ja, dat denk ik wel, ja? Want.

### ~ 5 Min

Arno de Boer 5:44  
Reijer, Volgens mij even terug. Stel dus dat we stel dus dat we dat stukje functionaliteit gaan maken gaan bouwen. Dan heb je twee kanten, hè? Dan heb je ene kant hebben we een stukje functioneel beheer, hè? Dus van wie mag het gebruiken en hoe en je en we houden ook een stukje technisch weer en Ik denk dat dat nog een een vraagstuk is waar we dat beleggen binnen.

### ~ 6 Min

Ronald Steenstra 6:03  
Ja. Ja.

Arno de Boer 6:11  
De Hanze. Alleen wat ik wel kan zeggen is dat het team van Bart Leupen een team data aan applicaties. Dat zou het meest logische zijn om het daar te beleggen, dus ik laat even in het midden welke personen dat zijn, Maar dat is dan wel de plek waar waar het meeste aan development gebeurt. Kijk Nils ook ook even aan, want volgens mij is dat wel een beetje de de kern en, Dat is ook. Een beetje hoe we de natuurlijk werken, dus we willen eigenlijk wel zorgen dat. Dat er een soort van teampje binnen de Hanze en zelf ook verantwoordelijk is voor datgene wat misschien ooit geproduceerd wordt en wat we daadwerkelijk gaan gebruiken dat de continuïteit verborgd is hè, dus dat zie dus je hebt dus eigenlijk een van die straatjes.
Je hebt functioneel beheer. Die gaat echt de functionele kant van het verhaal doen een stukje. Nou ja, technisch applicatiebeheer, hoe moet ik dat noemen? Technisch applicatie ontwikkeling nou zo.

### ~ 7 Min

Arno de Boer 7:06  
Dat is tuig.

Reijer van der Zande 7:07  
Ik denk inderdaad dat mijn vraag naar wat meer gestoeld was op het technische stukje inderdaad. Dat was dat functionele weer. Had ik zoiets van? Dat zit waarschijnlijk bij nou een stukje verpleegkundige kunnen zelf. Of nou ja, Misschien nog wel een laag daartussen, Maar ik had het gevoel dat dat al redelijk gedekt was, Maar ik zocht inderdaad nog een beetje naar dit.

Arno de Boer 7:10  
Ja. Ja. Ja.

Reijer van der Zande 7:25  
Wat, wat zijn de? De technisch Als je Als we kijken, We gaan deze applicatie zometeen Natuurlijk in schrijven en Ik denk dat het dan ook heel fijn Als het Als het waarschijnlijk onder deze groep komt te hangen. Dat dat ook iets geschreven wordt en iets waar ze zich over hebt mee voelen en makkelijk kunnen oppakken.

Arno de Boer 7:38  
Ja.

Reijer van der Zande 7:44  
Dus zijn daar talen dingen die, want We hebben deels al gezegd van nou als er iets geschreven moet worden, dan moet het in ieder geval makkelijk toegankelijk zijn. Breed gedragen zijn en dat soort dingen. Maar ik zoek eigenlijk nog een stukje naar zijn er voorkeuren vanuit deze groep. Waarmee zeggen daarmee maken we het makkelijk.

### ~ 8 Min

Arno de Boer 8:03  
Die datantwoord, moet ik jou schuldig blijven, want Ik ben een de business architect, Maar ik denk dat het Misschien dat Nils daar iets over kan zeggen wat voor talen wat er nu gebruikt binnen hip en data team heb je daar zicht op.

Nils van der Deen 8:17  
Nee, ik, Ik heb dat wel eigenlijk niet zo heel veel zicht op, dus ik durf dat niet met zekerheid te zeggen van dat ik dan bijvoorbeeld zeg van ja, je maakt ze blij Als je met een Java applicatie komt. Volgens mij gebruik je ze wel wat Java, maar ik weet niet waar zij velen programmeren, dus misschien handig dat je daar Henk Hoekstra heeft. Misschien wij zelf kunnen betrekken als productowner denk ik. Dat hij daar een beter beeld bij heeft, en dan ook.

Arno de Boer 8:40  
Ja ja.

Nils van der Deen 8:43  
Laat je iets concreter ook naar je naar je juiste personen kan wijzen in dat opzicht? Nee, heel fijn.

Arno de Boer 8:49  
Bruno doet toch ook software development Bruno, ja.

Ronald Steenstra 8:51  
Ja ja ja, hij zit bij je HIP ja, OK.

Arno de Boer 8:54  
Ja en misschien rijden dan, want We hebben zeg maar een paar architectuur hebben we het onderverdeeld in iemand die zeg maar de mooie verhalen vertelde, ben ik dan en de en de en de harde techneus.

### ~ 9 Min

Ronald Steenstra 9:07  
De kletskousen van die.

Arno de Boer 9:08  
Ik ben een kletskous en de en de techneut is, is Raymond Dagret. En die heeft al ideeën over welke talen er ook gebruikt moet worden. Dus Ik denk dat Als je met Raymond en Henk gaat zitten, dat je dan wel een goede scoopbepaling kan krijgen van welke taal? En Dat was ook één van de. Openstaande acties nog uit het architectuur kader namelijk dat we ook gaan zeggen van dit zijn onze technische standaarden om applicatieontwikkeling mee te gaan doen, zeg maar, en dan hoor ik. Ik hoor vaak Json en weet ik veel. Nou ja, dat nou ja, ik hoor, ik hoor van allerlei talen, maar dus het is niet echt mijn cup of tea zeg maar. Maar dat zijn wel de namen om om, nou ja.

Ronald Steenstra 9:44  
En. Ja en arno je.

Arno de Boer 9:48  
En, er Reijer wat? Oh, sorry.

Ronald Steenstra 9:50  
Ja je noemde net al even een voor nou hebben we over technisch beheer beleggen dat dat onder Bart gaat vallen. Ik denk dat iemand van ons op een gegeven moment ook met hier met Bart al moet gaan hebben, denk ik of niet van dit. We gaan deze kant op. We zien dat we straks nou ja, waarschijnlijk meer software ontwikkeling binnen de Hanze gaan doen.

### ~ 10 Min

Arno de Boer 10:02  
Ja.

Ronald Steenstra 10:10  
Maar goed, dat betekent Natuurlijk ook dat er dan van die ontwikkelingen technisch beheer uit voortkomt. Hoe gaan we dat beleggen?

Arno de Boer 10:17  
Ja en Dat is één van de. Er zijn twee actiepunten overgebleven uit de architectuur kader softwareontwikkeling eentje was de technische standwaarde en de tweede was, hoe gaan we dat organisatorisch inbedden en die actiehouder is volgens mij Bart en oh ja, Er is nog een derde, dat is meer eigenlijk jouw rol Ronald is dat je zeg maar, softwareontwikkeling ook in je bagage meeneemt als een mogelijke oplossing.

Ronald Steenstra 10:44  
Zeker nou, dan is dit een mooi voorbeeld van volgens mij.

Arno de Boer 10:45  
Nou, precies daar is dit een mooi voorbeeld van en die actie had Rob. Die moet zorgen dat de orientatie naar beheerproces een plek krijgt. Das niet meer dan zeggen goh kijk daar es naar. 

Ronald Steenstra 11:0
Ja ja ja, dat doe ik. Maar ja, Ik weet niet, dat hoeft nu nog Misschien nog niet, maar op een gegeven moment moeten we ja ja, of ik dan Misschien kunnen Bart erover hebben of zo of?

### ~ 11 Min

Arno de Boer 11:08  
Ja, denk het wel Misschien met zijn tweeën even Dat is wel een leuke, want je hebt ook. Wij hebben het andere casus. We hebben dan een mooie uitgewerkt stuk. Ik denk dat dat een mooi moment is om ook meteen gaan kijken van OK, wat hebben we dan nodig aan capaciteit?

Ronald Steenstra 11:15  
Ja. Ja.

Arno de Boer 11:23  
Wat, wat is er al? Nou ja, zo dus.

Ronald Steenstra 11:25  
Maar dat is wel iets voor een later moment, dan denk ik.

Arno de Boer 11:28  
Ja ja.

Reijer van der Zande 11:32  
Ja, in her verlengende. Jullie gaan dan een de welk stukje gaan jullie dan nog uitbanen? Want ik moet even kijken of dat ook een heel relevant is voor mijn.

Arno de Boer 11:40  
Nee, het idee wat ik wat ik zelf heb, is een beetje van. Jij doet jouw onderzoek, hè? Dus je we hebben straks. Wij moeten uiteindelijk We hebben aan de hand van het architectuur kader softwareontwikkeling zijn het nog 3 openstaande acties voor voor zeg maar BSIT zelf eentje was de technische standaarden, dus heel veel kunnen we uit jouw onderzoek halen.

Ronald Steenstra 11:55  
Ja.

### ~ 12 Min

Arno de Boer 12:05  
Eentje was nog dat dat we het ergens moeten beleggen bij dat team van data en applicatie. Precies en daarna, daar is het MT lid zelf verantwoordelijk voor om dat te doen. Dus in dit geval is dat Bart Leupen en Er is. En, Er is nog een actie openstaand voor, zeg maar dat je dat we eigenlijk altijd software ontwikkeling ook als mogelijkheid meenemen. Als er een functionele vraag komt en Dat is meer het proces van oriëntatie naar beheer en voor jou is denk ik vooral belangrijk is dat jij met die standaarden bezig bent. En ongeveer een inschatting maakt van oké wat. Wat hebben we dan nodig aan kennis en kunde en wat zou?

Ronald Steenstra 12:48  
Ja ja ja precies.

Arno de Boer 12:49  
Dat is waar. En zelfs die benodigdheid aan kennis en kunnen daarvan, vraag ik me af of je datüberhaupt kan inschatten, want je weet niet hoe groot volume is en etc.

Ronald Steenstra 12:58  
Nee, nee, dat klopt, Maar ik moet Natuurlijk zometeen wel als ik ga natuurlijk verschillende opties overwegen en.

### ~ 13 Min

Arno de Boer 13:00  
Nee maar. Ja.

Reijer van der Zande 13:06  
Kijk naar een zo makkelijk mogelijke oplossing in eerste instantie, want niemand is gebaat bij een complexe oplossing en dat strikt noodzakelijk is. Maar één van de aspecten die ik Natuurlijk daarin mee moet nemen is wel inderdaad, hoe gaat het onderhoud plaatsvinden en is dat een optie binnen de hand of niet? En Dat is wel een  Meeweeg factor in of maatwerk geschikt is of deze oplossing.
Nou ja absoluut. Vandaar dat er een kleine.

Arno de Boer 13:30  
Het antwoord precies en hetantwoord daarop is wel, ja, zeg maar, wij gaan, Het is, Het is een ontwikkeling, Maar we willen wel daar naartoe werken, dus dat we echt even een een soort van, nou ja, altijd een.

Reijer van der Zande 13:37  
Ja. Maar dan kan ik dat In de primair als als antwoord meenemen, zijn er van nou de de de de optie tot maatwerk bestaat en niet alle kaders zijn daarvan bekend, maar processen lopen om dat verder in kaart te dringen en valt bijna verder buiten scope van deze opdracht. Maar dan moet ik het wel even afkaderen. Dat is wel iets wat ik nou, dat kan ik op deze manier even netjes doen dus.

Arno de Boer 13:42  
Die. Ja precies ja. Exact. Helemaal. Ja. Helemaal top, ja ja.

Ronald Steenstra 14:00  
Dat ja duidelijk.

### ~ 14 Min

Arno de Boer 14:03  
Ja.

Reijer van der Zande 14:05  
Even kijken hoor. Dat is al wel heel fijn. Ik zat u daar nog een stukje de technologie, Maar dat hebben we dus dat moet. Daar mag ik dan bij deze mensen uitvragen. Ik zal nog even een stukje. Integratie in systemen we hebben natuurlijk een een. Het is dol onder een planningstool te maken, Maar dat hangt aan Brightspace. Daar moet Natuurlijk dan eventueel een koppeling aankomen. Ik heb het met verpleegkunde erover gehaald. We gebruiken ook een planningstool webroom geloof ik, of Webboom is ja, ja, Er zijn met een nieuwe naam gekregen, geloof ik maar dat was een  Webroom Booking.

Arno de Boer 14:41  
Ja. Reserveringen.

Reijer van der Zande 14:48  
Ja, Maar dat is dus eventueel een mogelijke koppeling. En hetzelfde met bijvoorbeeld een Osiris, nou zijn er binnen de Hanze zijn daar apis beschikbaar. Is dat iets wat makkelijk open te stellen is, is dat juist iets wat heel moeilijk gaat. Is dat ik? Ik ben een beetje zoekende. Waar mag ik inhaken wat wat, waar zijn daar de kaders?

### ~ 15 Min

Arno de Boer 15:12  
Ja. Nou, Dat is we haken altijd in op hIP. En HIP is het Hanse Integratie Platform.

Ronald Steenstra 15:22  
En, Dat is eigenlijk wil je ook Henk Hoekstra is dat hè? Die daar wordt het dan dus.

Arno de Boer 15:22  
En. Ja dus we noemen gekscherend noem ik het ook wel Als het Henk Integratie Platform want het Henk Hoekstra is de productowner.

Ronald Steenstra 15:31  
Ja.

Arno de Boer 15:32  
Dus.

Ronald Steenstra 15:33  
Dat is dezelfde boek, zeg maar Als we net hadden, hè? Ja, kijk.

Arno de Boer 15:33  
Dus die ja, daar kun je daar wel bij mee terug. Ja, en volgens mij wordt er ook al informatie uit Brightspace ontsloten Als ik maar niet. Nou, kijk ik ook Ronald even aan.

Ronald Steenstra 15:45  
Ja, ja Dat is Natuurlijk nog wel een koppeling tussen Brightspace en Osiris voor het inschrijven van studenten In de brightspace course.

Arno de Boer 15:49  
Ja. Ja.

Ronald Steenstra 15:54  
De andere kant op resultaten van het Brightspace nou zie je dus daar wordt aan gewerkt, Maar dat ligt me eerder stil, geloof ik maar en en ze zijn nu ook met alles bezig met koppelingen volgens mij.

### ~ 16 Min

Reijer van der Zande 16:07  
Oh ja, ANS ze bestaat natuurlijk ook nog, ja, Maar ik denk dat ik ja nou, Dat is Misschien nog een, want ze willen het wel voor toetsmomenten gebruiken.

Arno de Boer 16:08  
Ja.

Reijer van der Zande 16:14  
Maar ik denk dat dat Misschien niet niet iets is wat direct zoals ik het zelf zal even anders gebruikt heb, denk ik niet dat er meteen een koppeling. 

Ronald Steenstra 16:25  
Nee, maar ja, dat wordt inderdaad duidelijk zijn van waar willen ze die tool Natuurlijk allemaal voor inzetten en wat voor informatie is daarvoor nodig? Dus waar moet het mee communiceren?

Arno de Boer 16:29  
Ja.

Reijer van der Zande 16:32  
Inderdaad welk systeem en daarvoor de security wel het verzoek om de dataminimalisatie van. Uiteraard Dat is, Dat is ook.

Arno de Boer 16:38  
Ja.

Reijer van der Zande 16:40  
Goed. Maar dus via hip is inderdaad dus het Er is een platform waarbinnen dat. OK.

Ronald Steenstra 16:45  
Ja en voor de rest zou Raymond er ook nog een rol in kunnen spelen. Arno, denk je of?

Arno de Boer 16:56  
Ja ja Raymond Dagelet. Die heeft er ook wel ideeën over, Alleen die die haar die die leidt ook wel weer erg op op Henk, maar zij zijn Samen, denk ik wel, voor de technische kaders en voor de nou ja.

### ~ 17 Min

Ronald Steenstra 17:11  
Ja, dat zou wel een beetje zeg maar de twee zwaargewichten binnenvrees die om het zo te noemen.

Arno de Boer 17:14  
Ja ja.

Ronald Steenstra 17:17  
Niet letterlijk, maar nou ja, 

Reijer van den Zande 17:20  
Iedereen specialisatie toch? Ja, ja, goed om daar ja. Jullie weten denk ik verder weinig van. Hoe heb zelf dan?

Arno de Boer 17:33  
Nou ik, Ik weet wel, Ik weet wel conceptueel hoe het werkt, wat wij wat eigenlijk gebeurt is dat. Nou ja, HIP is eigenlijk een laag die zorgt voor de interoperabiliteit tussen de systemen, dus die zorgt ervoor dat er een er een aantal bronsystemen die leveren dan Dat is de de waarde waar de bron informatie wordt vastgelegd, bijvoorbeeld als hier dus daar wordt de inschrijving van de student en de student zelf wordt er in vastgelegd. Dat gaat dan naar de HIP toe. En het HIP wordt het bij elkaar gebracht, dan wordt het gestructureerd en vervolgens kunnen doelapplicaties kunnen dan op HIP aansluiten om het om die data op te halen dan wel rechtstreeks dan wel. Of dus ik wou niet zeggen, rechtstreeks, maar real time ofwel gebatch en batch batchgewijs. Dus het dus Het is echt een. Het is echt een tussenlaag. Die bronnen ontsluit en die bronnen dan vervolgens naar doel applicaties. Dus Ik kan me voorstellen dat dit. Het kan zowel om bron zijn Als het doel. In principe is elke applicatie een bron. Als de rol ligt er maar net aan hoe je het bekijkt, maar.

### ~ 18 Min

Reijer van der Zande 18:39  
Ja. Als ik het goed begrijp, is HIP dan voornamelijk inderdaad een doorgeefluik?

Arno de Boer 18:47  
Ja ja.

Ronald Steenstra 18:48  
En het het registreert zelf niks, dus de eventuele data die vanuit de applicatie.

Arno de Boer 18:54  
Zeg niet dat het niet helemaal niks zelf registreert, Maar ik kan me voorstellen dat bepaalde als bepaalde informatie niet vastligt in bronsystemen.
Dat zowel bijvoorbeeld een stukje verrijking plaatsvindt om bepaalde koppelingen of om een bepaalde dingen mogelijk te maken. Maar het het zou niet moet. Je zou niet moeten willen, Maar ik kan me voorstellen dat in sommige gevallen dat dat wel eens plaatsvindt, Maar dat is Maar ik. Ik denk dat daar Henk ook het besteantwoord op kan geven.

### ~ 19 Min

Ronald Steenstra 19:13  
Ja.

Arno de Boer 19:26  
Omdat.

Reijer van der Zande 19:27  
Ik vraag het even, want ik krijg Natuurlijk het verzoek om data minimalisatie te doen en als het niet In de applicatie zelf belegd hoeft te liggen elders kan liggen, dan heb je natuurlijk niks aan extra informatie en applicatie zitten. Maar als ik het nu claimt is het inderdaad het bij één jaar en de de koppeling moet dan wel In de applicatie gebeuren en zal het ook ergens geregistreerd moeten worden. Maar het.

Arno de Boer 19:37  
Nee maar. Precies.

Reijer van der Zande 19:47  
Goed om dat nog eventjes bij Henk en Raymond even door te vragen. Ja. OK.

Arno de Boer 19:51  
En conceptueel ook wat ook in dat kader hebben gezegd, op het moment dat er een nieuwe applicatie of een nieuwe toepassing ontwikkeld, dan gaan we niet data platform om data op te slaan. Nee dan is dat gewoon een eigen dedicated database die daar onde moet gaan liggen. Nou dat we dan, want anders krijg je allemaal vermenging van. Hoe zeg je dat doelen en dat wil je gewoon niet. Je wilt niet dat dat op het moment dat je een nieuw data platform dat je dan nog moet rekening houden met een applicatie die er draait ofzo. Dat is natuurlijk, dat wil je dus niet, dus Dat is een.

### ~ 20 Min

Ronald Steenstra 20:19  
Ja. Ja Raymond heeft ook mee gewerkt, toch aan dat beleid van softwareontwikkeling.

Arno de Boer 20:30  
Ja ja zeker Ja ja.

Ronald Steenstra 20:31  
Ja precies, dus je weet gewoon vooral.

Arno de Boer 20:33  
Ja.

Reijer van der Zande 20:35  
OK, Dat is al, dan wordt het al een stuk Helder van In de zin in ieder geval. Waar ik verder mag doorvraag.

Nils van der Deen 20:40  
Een stukje SSO. Dat regelen wij vanuit cloud infra regelen wij op de manier daar precies weten.

Reijer van der Zande 20:45  
Nou, uiteindelijk zal dat waarschijnlijk ook bij. Zal ik daar op de applicatie meest wenselijk Misschien niet In de mVP, maar wel. Uiteindelijk moet hij Natuurlijk daarop aanhaken, dus dan moet dan wel ook eeb koppeling komen. Moet dan geregeld worden. Maar dat zou ik dus eventueel via. Informatie over kunnen krijgen. En ja, ook nou top.

### ~ 21 Min

Arno de Boer 21:09  
Ja. En wat ik nog bedenk rij je is dat wij een ook nog een kader hebben met eisen aan applicaties aan nieuwe applicaties? En, Het is niet zo dat die 100% ook moeten gelden voor ontwikkelde applicaties, Maar het geeft je ook. Daar staan bijvoorbeeld ook de SSO eisen in bijvoorbeeld dus die zal ik ook nog even met je delen, want dat bedacht ik mij laatst nog even van ja, Dit is best wel een rijk document. Er staan ook allemaal privacy en security aspecten in en wat we en dat document Dat is. Een leidraad, Maar het is nooit in beton gegooid. Gegoten hè dus? En, We hebben altijd wel een een soort van mogelijkheid van hè, Als het echt een eis is die nergens op slaat in in in relatie tot de doeleinden waarvoor je het inzet, ja, dan moet je dat niet doen. Maar het is wel een leidraad van OK, dit zijn wel een checklist van hier moet je wel aan voldoen om een applicatie van de binnen de handel te mogen neerzetten.

### ~ 22 Min

Ronald Steenstra 22:10  
Nou, Dat is heel fijn om dat mee te nemen, want dat betekent dat er hoe meer je daar aan kunt voldoen, hoe makkelijk Het is om dat draagvlak voor te krijgen.

Arno de Boer 22:12  
Ja. Ja, Ik ga. Ik ga even checken waar die staat en dan dan stuur ik jou zo wel even een linkje bij je ja.

Reijer van der Zande 22:41  
Zijn er van jullie uit? Het hoofdstuk architectuur kaders, dus dat heb ik deels met de Arno al doorgenomen in het. Dus in ieder geval. Volgens mij is het beleid om een gelaagde applicatie te maken. Jullie hebben een standaard 3 laag erin zetten data, Backend, Frontend. Maar zijn er ook nog andere eisen rondom nou stukje schaalbaarheid, voornamelijk ook met het aspect kijkend naar We gaan straks voor dit het nieuwe beter gaan doen, Maar het idee is dan wat Misschien wat blijven te trekken, want 

### ~ 23 Min

Ronald Steenstra 23:20  
Ik kan me voorstellen dat veel meer opleidingen hierin geïnteresseerd zijn, want Dit is inderdaad een functionaliteit die we voorheen een binnen Blackboard tool deels hadden, zeg maar ook een beetje op oneigenlijk manier. Manier werd het gebruikt, maar nou ja, het voldeed redelijk goed dan wat ze nodig hebben. Even leeg kunnen was niet de enige die dat op die manier deden dat we weten. Gewoon dat er meer opleidingen dat op die manier deden. Nou ja, dat dat lukt niet binnen Brightspace dus nou vandaar deze vraag, dus als hier straks iets voor is, dan denk ik. Nou ja, dat dat wel breder inzetbaar zou kunnen zijn. 

Reijer van der Zande 23:50  
Daar eisen onder. Al zijn geef dat additionele eisen haast nou precies ja, 

### ~ 24 Min

Ronald Steenstra 24:00  
nou, dat weet jij dus nog helemaal. Is dat gewoon voldoet binnen de Kaders af zoveel mogelijk voldoet aan de Kaders dus die we gewoon stellen. Inderdaad dan hoe de eisen die we stellen aan applicaties. Ja dan denk je dat dat niet echt per se het verschil zit, gezien de schaalbaarheid van? Nou ja, ja, Het is Natuurlijk behalve dan dit soort risico afweging maken soms, hè, Als je zegt Van ja, maar qua Prison security voldoet hij niet naar alle eisen, Maar we vinden het acceptabel, want het risico is klein, want Er zijn maar klein aantal gebruikers. Ja, dat zou Natuurlijk een rol kunnen spelen Als het op. Een veel breder aantal. Gebruikers zou worden ofzo dat het risico groter wordt dat zoiets zou ik voor hem kunnen zien, maar. Voor de rest.
Arno, heb jij daarna? Zie je het anders of.

Arno de Boer 24:43  
Ja, Ik heb, Ik vind het wel een goede vraag over überhaupt onderwerp schaalbaarheid. Dat is, denk ik. Dat staat nog niet dat dat zit een beetje op een technische vlak, maar ook wel op. Het idee is wel dat oplossingen die we ontwikkelen. Dat, Dat is zoveel mogelijk Hanze breed ingezet kunnen worden, hè? Dus dat er zal altijd het uitgangspunt. En toen zeiden het echt niet anders kan, maar dus wat Ronald ook zegt van het lijkt mij dat deze functionaliteit ook wel ergens anders In de of in ieder geval die wens ergens anders ook gaat leven. Dus dus qua schaalbaarheid moet in in principe Hanze breed inzetten zijn dat? Dat is eigenlijk wel het uitgangspunt.
Ja Dat is.

### ~ 25 Min

Ronald Steenstra 25:30  
Ja als er technische zin mogelijk is, zou dat heel mooi zijn, denk ik. En wat dat dan met zich meebrengt? Ja, dat Dat is ook een beetje wat we dan moeten zien.

Arno de Boer 25:36  
Ja.

Reijer van der Zande 25:38  
Maar dat betekent in ieder geval dat er bijvoorbeeld een scheiding van. Nou tussen moet vakken zal dus inderdaad een scheiding moeten zitten met wat van data Je kunt zien dus dat zijn allemaal primaire dingen die je nu al meteen mee kunt nemen dat daar dus een optie voor moet zijn. Of er een overkoepelend moet zijn om dat te kunnen regelen.

Arno de Boer 25:55  
Ja.

Ronald Steenstra 25:58  
Ik denk het wel, ja?

### ~ 26 Min

Arno de Boer 26:01  
Ik zal wat. Wat denk ik ook, belangrijk is om tweede. Ik kan wel bij software ontwikkeling ook voorstellen dat we niet in één keer helemaal. Een Hanse brede applicatie hebben die helemaal perfect werkt, Maar dat je juist in een groeisituatie ziet en dat schaalbaarheid meegroeit met die groeisituatie. Dus dat je hebt dan Agile team en je hebt dan bijvoorbeeld een versie één, noem ik dan maar de de de MVIP hè? Dus dat zal mooi heet. Nou, dan gaat bijvoorbeeld verpleegkunde, gaat ermee aan de slag en die gaat denken van nou, Dat is wel.

Ronald Steenstra 26:16  
Nee. Ja.

Arno de Boer 26:36  
Mooi en. Maar ik zie deze en deze deze dingetjes nog wel voordat we het echt echt in gebruik kunnen nemen. Nou, dat zijn dat soort dingetjes nou. Vervolgens komt er Misschien een tweede of derde opleiding die je ook die vraag heeft en dat we dan gaan kijken. OK, nu moeten we er een stukje schotting hè? Dus We moeten moet er een soort structuurtje in komen. Nou ja, zo dus het kan ook een.

Ronald Steenstra 26:57  
Ja ja.

Arno de Boer 26:57  
Groeimodel altijd zijn, hè, dus ik en Dat is het mooie ook van software ontwikkeling. Je hoeft dat niet. In één keer hoeft het eindproduct helemaal klaar te zijn. Je kunt het. Ik kan Misschien best wel een laagdrempelig trotische initiëel tool zijn, maar Je moet wel altijd rekening houden met een hanze brede inzet op het eind, dus dat je in je in je ontwerp altijd rekening houdt met OK.

### ~ 27 Min

Reijer van der Zande 27:13  
Ja dit doet inderdaad de de de.

Arno de Boer 27:20  
Ik moet schaalbaar zijn, dus zo dat dat je niet zoals Osiris model hebt, een datamodel wat niet meer aan te passen is.

Ronald Steenstra 27:31  
Ja, Dit is een pijnpunt.

Arno de Boer 27:35  
Daar lopen we tegen aan. Loopt Osiris zal ook tegen aan, Taki. Die heeft een bepaald model gekozen. Dat loop niet meer synchroon wat nu gevraagd wordt met de onderwijsmarkt. Die moet nu het verhaal hele maal op nieuw gaan doen. 

### ~ 28 Min

Reijer van der Zande 28:00  
En de applicatie hebben we dan helemaal gemaakt. Gaan we die dan als docker container deployen? Hebben jullie daar een idee of beeld bij?

Arno de Boer 28:06  
Dat moet je... das techniek he. Tenzij Ronald een oplossing heeft. 

Ronald Steenstra 28:10  
Ik hou me echt stil. Het is maar goed dat ik mijn achtergrond niet heb verteld, ik ben jurist, weet niets van techniek. Nee daar ben ik niet de aangewezen persoon voor, helaas. Dat zullen opnieuwe de namen zijn die we net genoemd hebben. 

Nils van der Deen 28:36  
Containers hebben we draaien, we hebben ook ander applicatie draaien, is maar net waar de voorkeur ligt van het HIP. Aangezien zij het waarschijnlijk in beheer krijgen dan. Ik denk dat dan het best is om even met henk te overleggen wat handig is. Kun iets heel moois opzetten maar als het voor hun niet handig werkt, dan wordt het erg lastig. 

Reijer van der Zande 28:59  
Is wel handig om die kader vooraf een beetje duidelijk te hebben, dat hoeft niet in steen gegoten te zijn. In het kiezen van een oplossing maakt het uit. 

### ~ 29 Min

Arno de Boer 29:15  
Heb trouwen de regeling gedeelt met je via de chat. Dus die staat erin. 

Reijer 29:29  
You do not have permission.

Arno de Boer 29:35  
oh Studenten mogen er niet bij

Reijer van der Zande 29:37  
Nee ik moet gemachtigd worden voor dit item. Ik mag toesgang vragen, weet niet waar die dan terecht komt....

Ronald Steenstra 29:42  
Vast bij Arno.

Arno de Boer 29:45  
Ik denk bij Marcella.

Ronald Steenstra 29:47  
Oh die geeft heel snel toegang.

Arno de Boer 29:51  
Anders ik, ik kijk wel even wat, nou ja.

Ronald Steenstra 29:54  
Ik heb hem Zonder bericht gestuurd, ja, dus, maar werkt dat wel? Ja, Het is wel een berichtje, denk ik. Even kijken hoor, want Ik heb 

### ~ 30 Min

Ronald Steenstra 30:17  
maar Als het niet lukt, dan laat het ons weten, dan gaan we dat op een andere manier met jou delen.

Arno de Boer 30:09  
Ja ja klopt ja.

Ronald Steenstra 30:17  
Wat voor een oplossing zouden jullie het liefst zien. Dat een losse applicatie brightspace plug in een ander bestaand systeem. Hebben jullie daar voorkeur in? Hebben jullie daar ideeën bij?

Arno de Boer 30:29  
Oh, dat snap ik. Heb jij daar ideeën bij Reijer?

Ronald Steenstra 30:39  
Wat goed.

Arno de Boer 30:39  
Ja, nee, even even even Zonder gekheid, hoor, want ik. Ik vind de plugin en idee. Dacht ik er even van. Oh, als dat als dat heel dicht tegen het Brightspace aan, hè? Dus, nou ja, hoe zie je dat zelf? Deze.

Reijer van der Zande 30:58  
Het is hier komt de persoonlijke voorkeur versus een een objectieve.

### ~ 31 Min

Arno de Boer 31:03  
Ja, nee, dat maakt niet, dat maakt niet uit hoor, in dit geval. Ik ben gewoon wel benieuwd inderdaad. Wat?

Reijer van der Zande 31:08  
Vind het zelf altijd leuk om een zelfcode te maken en daar iets mee te doen. Maar ik denk ook dat op het moment dat je als er inderdaad een bestaande plugging is, en dat moet ik nou even goed onderzoek willen doen. Cor altijd die pas over. Ja, dan moeten we niet iets heel complex gaan maken als er dan gewoon een bestaande oplossing is. Dat is gewoon zonde van Iedereen.

Arno de Boer 31:27  
Nee, klopt Maar dat Dat is ja precies. Ja.

Reijer van der Zande 31:30  
Dus. Dus Ik vind het heel leuk om iets te maken, Maar het moet wel toegevoegde waarde hebben, anders dan.

Arno de Boer 31:37  
Exact nee check.

Reijer van der Zande 31:39  
Doe ik liever wat anders met mijn tijd. Heel eerlijk.

Arno de Boer 31:44  
Één, zo ja.

Ronald Steenstra 31:46  
Maar ja, dat hangt er Misschien ook vanaf. Waar het met name gebruikt gaat worden, want. Dus, Ik weet niet of ik hier iets. En volgens mij zeg maar, Ik had het idee dat ze met name dat binnen Brightspace wilden gaan inzetten, in ieder geval met de studenten die ze in bepaalde courses in Brightspace zitten, dat ze daar inderdaad. Nou ja, een groep soms inschrijven willen hebben, of jullie iets om groepen Samen te stellen. Maar ja, Misschien is het ook wat breder dat. Dat weet ik even niet zo goed.

### ~ 32 Min

Reijer 32:15  
Nee voor mij wat ik begrepen heb vanuit verpleegkunde bestaat de vraag voornamelijk om het echt vanuit brightspace op te kunnen zetten.
Omdat dit ook de plek is waar de studenten In de met de course casseren. Dus dan heb je ook je je op één punt informatie liggen in plaats van dat je weer naar een externe tool moet. Of wat dan ook of iets dat dat dus volgens mij ligt juist de wens om het zo dicht, maar ook bij brightspace te hebben.

Ronald Steenstra 32:45  
Wat bepaalt dat dan deels het antwoord ook of niet? Heeft dat er niets mee te maken. 

Reijer van der Zande 32:49  
Ja, Ik denk uiteindelijk wel, Maar dat wil niet zeggen dat er vanuit andere elementen niet een voorkeur kan zijn en dan is het ook wel mijn taak om die ook te inventariseren mee te wegen en daar iets mee te doen. Dus vandaar dat ik daar even een open vraag over stel dat daar bij jullie leeft.

### ~ 33 Min

Ronald Steenstra 33:15  
Ja, maar is dat iets? Arno wat toch dan? Met name als input vanuit de opleiding moet komen, Omdat zij zeggen hoe zij dat voor zich zien of wat zij nodig hebben. Vooral dus of moeten wij vooral iets van vinden.

Arno de Boer 33:21  
Ja functioneel natuurlijk de opleiding, hè? Dus die degene die het.

Ronald Steenstra 33:25  
Ja.

Arno de Boer 33:29  
Maar de de technische kant denk ik toch dat we ook goed moeten gaan kijken van OK, is dat iets wat?
Ja vind Ik vind ik nogal lastiger. Ik denk dat dat nog even een beetje ook even met Raymond en Henk besproken moet worden ofzo, want.

Ronald Steenstra 33:42  
Ja ja. Ja, een idee over Niels of 

Nils van der Deen 33:45  
ja, Ik denk, Ik denk ook wel dat het beste met Henk. Ik kan hier nu allemaal dingen gaan zeggen en dat er dan een overleg met Henk en dat het dan de andere kant op wordt gedraaid.

Arno de Boer 33:57  
Ja.

Nils van der Deen 33:58  
Ja, Ik kan geen beslissingen maken, maar om even heel direct te zeggen, Dat was de.

### ~ 34 Min

Arno de Boer 34:05  
Kijk, als er als er echt een want er ging bijvoorbeeld ook over plugins hè, als die er echt zijn, die dus dit probleem helemaal omvatten. Ja, dan is het. We gaan niet zelf ontwikkelen, maar dan dan, dan geldt gewoon het kader weer weet je dus dan. We gaan niet zelf ontwikkelen, maar Als het echt zo is dat het zelf ontwikkelt, dan dan kom je eigenlijk wel op het wat we net al.

Ronald Steenstra 34:07  
Ja. Ja ja.

Arno de Boer 34:26  
Bespraken van je wil dan ook een aparte drielaags model. Je wil zorgen dat het nou ja, schaalbaar is. Nou ja. Dus. Ja.

Reijer van der Zande 34:37  
Duidelijk.

Arno de Boer 34:41  
Ik zoek ondertussen ook nog even door naar die kader die We hebben. Even kijken hoor.

Reijer van der Zande 34:52  
Nou voor mij, Ik had hierna nog een stukje over wat er.
De de vraag bestaat dus Er zijn er geen bestaande tools momenteel, maar zijn er al aanliggende tools binnen de Hanze die hier iets mee doen of is het echt een man op een pionier stukje of niet? 

### ~ 35 Min

Ronald Steenstra 35:14  
Ja, volgens mij dat laatste had ik het wel begrepen.

Arno de Boer 35:15  
Ja, dat weet ik ook.

Reijer van der Zande 35:16  
Ja ja. Doen we dat stukje verder verder, skippen. Zijn er van jullie als dingen die er minimaal in de applicatie zouden moeten zitten om het voor jullie werkbaar te krijgen.Ja dat wacht, ga je nog als eis als. 

Ronald Steenstra 35:50  
Nou ja, Ik denk dat Arno veel dingen verwezen heeft. Uit die die richtlijnen, kaders etcetera. Ja voor mezelf Ik ben, ik zie mezelf ook meer een soort doorgeefluik van opleidingen wat zij graag willen. Dus Als het voor hen werkt, nou, dan ben ik er helemaal blij. Maar goed, Dat is wel heel erg minimaal, maar ja.

### ~ 36 Min

Arno de Boer 36:08  
Ja echt, ja, en ik denk aanvullend. Het zou mooi zijn als we iets kunnen. Nou, dat dus Als we iets kunnen opleveren wat gewoon werkt en werkt ook In de zin van niet Alleen voor de opleiding, maar ook dat je kan zeggen van, We hebben een succesvol software development, trajectje doorlopen met een goede samenwerking met het met de Collab Space met een goede overdracht richting.

Ronald Steenstra 36:24  
Ja.

Arno de Boer 36:34  
Nou ja die plek van van team data aan applicaties.

Ronald Steenstra 36:39  
Ja ja.

Arno de Boer 36:39  
Conform die richtlijnen en ook al is het maar heel klein, hè? Wat gaat er even om dat wij die vinger oefening gedaan hebben met zijn allen en dat we weten van hé, Dit is Dit is een een werkwijze die We kunnen we In de toekomst verder Bart, Maar we hebben dus nou wat ik al zei Van We gaan met een onderwijsportaal zijn we met een aantal scenario's bezig en één van de.

Ronald Steenstra 36:42  
Ja ja.

Arno de Boer 36:58  
Scenario's is toch ook om een schil zelf te gaan ontwikkelen? En Dat is één van de scenario's. Nou, stel dat je daarop uitkomt en We hebben hier een goede werkwijze die loopt en die werkt. Dan kunnen we wellicht nou ja, daar ook een, nou ja, Daarom stappen zetten dus die dus vanuit die hè, dus dat we echt dat proces doorlopen van het ontwerp en ontwikkelen van de nieuwe applicatie dat het echt gebruik nemen en ook het beheren daarvan nou dat dat dat een succesvol trajectje is, zeg maar dus dat je ook al beginnen we met een kleine afgebaken stukje functionaliteit dat we zeggen van hé op.

### ~ 37 Min

Ronald Steenstra 37:28  
Ja.

Arno de Boer 37:35  
Deze manier kunnen we dit ook. Groter toepassen of iets iets meer iets meer body tay.

Ronald Steenstra 37:40  
Ja, het kan wel de deur openen voor de toekomst, zeker dan.

Arno de Boer 37:43  
Ja ja.

Ronald Steenstra 37:46  
Oké.

Arno de Boer 37:46  
En en en tegelijkertijd zie je ook en dat is een klein opmerking. Je ziet ook bijvoorbeeld dat sommige universiteiten hogescholen daarin helemaal doorslaan. En, dat willen we juist weer niets, dus dat je dan op een bepaald moment toch weer vandaar ja.

### ~ 38 Min

Ronald Steenstra 38:00  
Ja je weet hoe enthousiast we raken raken.

Arno de Boer 38:04  
Wat zei je?

Ronald Steenstra 38:04  
Wie weet hoe enthousiast we raken straks.

Arno de Boer 38:06  
Ja precies ja.

Ronald Steenstra 38:07  
Zou een eigen SIS bouwen.

Arno de Boer 38:09  
Ja, alles kan hè? Ja, Dat is het. Ja, Dat is het punt Ronald, het kan het kan en het kan ook nog wel redelijk binnen de kaders van onze portemonnee. Als ik het zo mag inschatten. Alleen de vraag is, wil je die, wil je dat Dat is? Dat is dan de tweede maar.

Ronald Steenstra 38:16  
Ja. Ja ja ja.

Arno de Boer 38:27  
Wel veel. Dus.

Reijer van der Zande 38:33  
We zijn er dat, bedenk ik me net zijn er nog. Kostenbeperkingen restricties aan deze applicatie waar ik rekening mee moet houden.

Arno de Boer 38:45  
Nou moet gratis zijn, ja?

Reijer van der Zande 38:47  
Ja, ja mijn voorkeur alles hè? Maar een man uren of in onderhoud of in want de de de kosten is Natuurlijk In de heel heel eenvoudig iets, Maar dat uit zich Natuurlijk op heel veel fronten.

Arno de Boer 38:49  
Ja. Ja kijk, Dat is een beetje lastig. Kijk, We hebben wel als idee altijd dat er een soort businesscase onderligt, hè? Dus dat het dat het waarde moet toevoegen en dat kan kwalitatief als kwantitatief kijk Als we in 1 keer 4 FTE nodig hebben aan personeel, dan gaan we zeggen van dat doen we niet, was de bij wijze van spreken de CollabSpace twee twee dagen werk heeft of zo om. Het te maken en het en Het is een uur beheer per. Maand ja. Ja prima, dat doen we het wel, maar snap je dus het zit een beetje in van.

### ~ 39 Min

Ronald Steenstra 39:31  
Ja.

Arno de Boer 39:32  
Wegen de baten op tegen de kosten, zeg maar, Dat is een beetje vooral de het heet hangijzer.

Reijer van der Zande 39:38  
Zeker waar we veel aspecten om even mee te nemen In de In de In de overwegingen je noemt inderdaad redelijk concreet wat wat nummers, maar daar heb je Niemand ballpark wat ik verwachtte Als ik heel eerlijk ben. Ik verwacht niet dat dit heel veel onderhoud gaat vergen, Maar het is wel iets wat meegenomen door.

Arno de Boer 39:40  
Ja ja.
Ja.
Nee precies.

Ronald Steenstra 39:56  
Ja, Dat is ook iets wat we TZT dan met Bart kunnen bespreken, denk ik van we verwachten dat dit zoveel tijd gaat kostenqua technische functioneel beheer, waarbij het functioneel beheerder Misschien inderdaad is bij verpleegkunde ligt maar.

### ~ 40 Min

Arno de Boer 40:00  
Ja ja zeker ja.

Reijer van der Zande 40:10  
Ja. OK. Ik ben volgens mij redelijk door mijn lijstje met dingen in die ik even wil aanstippen. Hebben jullie nog punten die jullie wilde toevoegen? Of dingen die ik gemist heb of je denkt, nou.

Arno de Boer 40:23  
Ik ben, ik benieuwd naar het resultaat, Dat is het enige wat ik.

Ronald Steenstra 40:27  
Nee, Ik was een beetje voorbarig met mijn vraag of we de opleiding inderdaad een beetje op de hoogte blijven en van het hebben we het over gehad. 

Reijer van der Zande 40:35  
Dus oh nee, op zich niet hoor, maar normaal kijk, Iedereen is nu Natuurlijk al twee maanden bezig, maar effectief heb ik nog maar één werkweek gehad. Ja klopt. Helaas gaat de doorlooptijd iets langer zijn. Als denk ik het het half jaartje wat er normaal voor staat. Maar ik ben. Weet je, dit soort gesprekken zijn heel leuk en heel interessant. Maar ik kan er maar elke week maar één of twee doen en dan je tijd loopt zo erg voordat je dat voorbereid hebt uitgewerkt hebt. Het is het, valt mij nog wel een beetje tegen. Beetje zwaar, Omdat dus. 

Ronald Steenstra 40:50  
Maar heb je het dan ook met Cor over qua planning en zo dat soort dingen? Als je merkt van hé er gaat wat met tijd kosten, Omdat dat dat valt toch wat tegen dat je.

### ~ 41 Min

Arno de Boer 41:00 
Ja. Ja begrijp ik ja. Ja ja.

Ronald Steenstra 41:16  
Dat met Cor over hebt.

Reijer van der Zande 41:20  
dat met Cor hier over zitten. En Ik had voor mezelf al wel besloten dat dat de doorlooptijd waarschijnlijk wel langer ging zijn als een half jaar, dus Dat is wel. Dat heb ik van tevoren ook wel aangegeven bij de verschillende personen. OK, maar wel goed om eventjes mee te nemen.

Ronald Steenstra 41:30  
Iemand anders nog vragen of aanvullingen. Nee, Als je je je wil in ieder geval 1 1 1 nou ja, in een korte klap een iets iets opzetten, zeg maar, had je plannen hoe je dat al wilde gaan doen?

Arno de Boer 41:39  
Nee hoor.

Nils van der Deen 41:44  
Je wil in inder geval in een korte klap iets opzetten, zeg maar. Had ja een plan hoe dat wil gaan doen. 

Ronald Steenstra 41:54  
Nog niet meteen, Maar ik denk, weet je, er hoeft heel weinig achter, dus Ik denk dat het een basically alleen vond en die heel snel met een een klein beetje data koppelt. Waarom? Je denk ik een heel eind en Het gaat voornamelijk erom. Kijk als er een paar Jason bestanden achter hebben staan die dat even wat. Dingen kunnen opvragen en dan wat willen we HTML een beetje geslaagd tot een klein beetje eruit ziet? Volgens mij kunnen we heel snel tot wat functionele eisen komen en kijken vanuit de goede vertaling van wat ik van jullie begrepen heb.

### ~ 42 Min

Arno de Boer 42:25  
Ja ja mooi man ja.

Reijer van der Zande 42:26  
Nou wel heel expliciet erbij dat dit niet op het eindproduct gaat lijken dat het puur om het functionele inhoud gaat.

Arno de Boer 42:31  
Nee, Maar dat vind ik heel mooi dat dan heb je in ieder geval een praatkader waar en dan kun je even checken van, is dit wat We willen? En nou ja, mooi.

Ronald Steenstra 42:36  
Ja.

Arno de Boer 42:40  
Gaaf.

Reijer van der Zande 42:41  
Ja zeker ja, dus Ik hoop dat ik dat even kan doen en dan is het even de vraag, in hoeverre dat? Kijk, je mooiste is als dat al in bruidspace zou kunnen doen, dan heb je een heel echte use case, Maar ik denk dat dat Misschien een brug te ver gaat. Dat moet je wel echt In de techniek zitten en Het gaat denim. Er zit ook een stapje daarvoor op. Het het functionele aspect zijn, zijn de jullie requirements gedekt? Nou nou ja.

### ~ 43 Min

Arno de Boer 43:09  
Ja.

Reijer van der Zande 43:11  
Maar dat was een idee waar ik mee speel.

Arno de Boer 43:11  
Maar Misschien zou dat bij ja dat. Dat zou een vervolgstapje kunnen zijn. Natuurlijk dat we even met Maurits of zo gaan zitten. Ja.

Ronald Steenstra 43:14  
Sorry. Ja stak ook naar het aan te denken aan de de functioneel beheerders van Brightspace team Icto. Het is zij om ook eens met met Er zijn één iemand die ze vooral of één iemand maar één iemand die is vooral daar met veel met techniek bemoeit Maurits Hoogerwerf.

Arno de Boer 43:23  
Ja.

Ronald Steenstra 43:35  
Die vind het denk ik ook heel interessant om nou, zo zou het hele team icto, dan vind ik het wel interessant om dit ook te horen. Maar dan kan ik eventueel ook een afspraak mee maken voor jou rechtstreeks maar.

Arno de Boer 43:40  
Ja.

Ronald Steenstra 43:46  
Kan ik je wel bij helpen? 

Reijer van der Zande 43:50  
Top. Dus dat ja dat in ieder geval het idee waar ik mee speel en wat volgens mij nou zeker Als ik er even een stukje AI tegen aan gooien, dan heb ik dat die boyer Playa zo voor mekaar. Ik bedoel dat, Dat is juist iets van de AI supergoed in is.

### ~ 44 Min

Arno de Boer 44:03  
Ja ja ja.

Reijer van der Zande 44:05  
En, Ik vind het leuk, mooi. Ja, ja, Dat is wel een stukje vibe coding, ja.

Arno de Boer 44:06  
Vibe coding toch? Ja vibe code.

Ronald Steenstra 44:12  
Ja.

Arno de Boer 44:13  
Ik moet trouwens zo richting de Hanze, dus ik zit nu thuis.

Ronald Steenstra 44:18  
Ja.

Arno de Boer 44:19  
Ja en dan dan ga ik zo. Ik heb verder niks meer namelijk. Ik weet niet of de rest nog ja, de bal.

Ronald Steenstra 44:23  
Hij stapt op de bus. OK. Nee, dan zijn we klaar, denk ik. Heel erg bedankt allemaal ik jij ook. Ik zal de opname stoppen.

Arno de Boer 44:32  
Jij ook Reijer Top? Goede vragen.
