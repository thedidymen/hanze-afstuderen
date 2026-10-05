# Transcriptie interview – Verpleegkunde

## Transcriptieproces

Voor het uitwerken van de interviews is gebruikgemaakt van een Python-script dat automatisch spraak omzet naar tekst. Hierbij is het audiobestand ingelezen met de Python-library `speech_recognition`. Vervolgens is via de Google Speech Recognition API een Nederlandse transcriptie (`nl-NL`) gegenereerd.

De gegenereerde tekst is daarna opgeslagen in een tekstbestand en handmatig gecontroleerd en waar nodig gecorrigeerd op fouten in interpunctie, naamgeving en herkenning van gesproken woorden. 

## Algemene informatie


| | |
|---|---|
| Datum | 2 maart 2026 |
| Tijd | 11.00u - 12.00u |
| Locatie | Hanze Hogeschool, Eyssoniusplein 18, 9714 CA Groningen |
| Doel gesprek | Stakeholdergesprek Verpleegkunde voor Sign-Up Tool |


| Aanwezigen | Rol |
|---|---|
| Mirjam Veenstra | Regisseur Verpleegkunde |
| Jos Ensing | Instructeur IT |
| Cor Blom | Projectleider Collabspace |
| Reijer van der Zande | Developer |


## Transcriptie


### ~ 0 Min

Mirjam Veenstra  
Ik denk dat het het makkelijkste is om hem (de applicatie) ook even erbij te pakken. Wij werken met Brightspace. 

Reijer van der Zande  
Ja. 

Mirjam Veenstra  
En wij hebben hier ook onze toetsing op. En waar wij tegenaan lopen is bijvoorbeeld dat wij nu de inschrijvingen op deze manier hebben vormgegeven. Dat er een link is waar ze op moeten klikken, de studenten. En dan krijgen ze hier per moment een groep is aangemaakt. En dan kunnen zij zich op een moment inschrijven door deze aan te vinken. Nou, en dan zie je of die bezet is of niet. 

Jos Ensing  
Studenten zien het net iets anders. Die hebben de mogelijkheid om in te schrijven. En mochten ze het fout gedaan hebben, dan kunnen ze zich ook weer uitschrijven voor die groep. En ik denk, heel kort door de bocht gezegd, wat wij missen is een stukje flexibiliteit. Want je kunt hier niet variëren met bijvoorbeeld het aantal personen wat maximaal op een groep mag inschrijven. 

Mirjam Veenstra  
Ik denk dat dit wel een beetje een goede oplossing is. Ja, dat is wel een goede oplossing. Dit is hoe een student het ziet. 

### ~ 1 min

Mirjam Veenstra  
Ik heb hem even als learner erin gegeven. En dit is tijdrovend, want Jos moet elk moment de lozen ingooien. We moeten in Excel per tijdmoment moeten we dit aanmaken. En als toetsen moeten we ook elk moment aanklikken om te kijken welke student heeft zich ingeschreven. En studenten kunnen dus ook zien wie zich wanneer heeft ingeschreven. En wat we eigenlijk willen is dat we een mooie ingeschreven studenten hebben. Dus als ik een student heb, inschrijftool hebben waardoor we niet elke keer al die groepen hoeven aan te melden die ons gewoon meer gebruiksvriendelijk is waarin we ook makkelijker elk jaar terug kunnen laten komen. 

Reijer van der Zande  
Ja oké. 

Jos Ensing  
Je kunt het wel met een batchfile vanuit Excel doen hoor. Dit is dus de group tool en dat is eigenlijk puur om samen te werken binnen Brightspace dat je vroeger in Blackboard ook wel maar wij misbruiken hem om gewoon één persoon of twee personen in te schrijven op een bepaald moment

### ~ 2 min

Jos Ensing  
en wat wij de groepsnaam is dus eigenlijk de datum tijd en plaats. Zo misbruiken wij de groep tool. Zo misbruikt de hele Hanze de groep tool en wat hier een bijkomend dingetje is. Normaal gesproken is het om samen te werken dus dit is niet erg maar hier kom je ook een beetje met privacy in gedrang omdat iedereen kan zien die binnen die course zit van wie op welk tijdstip is ingeschreven. 

Mirjam Veenstra  
En dus ook wie een herkansing nodig is. 

Reijer van der Zande  
Ja precies. 

Jos Ensing  
Dat zijn eigenlijk gegevens die je eigenlijk liever niet wilt nemen. Nou is dat allemaal niet zo heel ernstig misschien maar nou ja als je als je dat kan uitsluiten zou dat gewoon heel mooi zijn. Kijk en wat wij nu doen is dus een groupset klaarzetten. Dus we hebben zeg maar herkansing nummer één en daar hebben we zoveel tijdslotjes voor. En daar zorgen we voor dat er één persoon op één groep en als een groep op de tijdslotjes zit dan is dat misschien twee personen op een groep in kunnen schrijven. Ja. Maar wij kunnen dus niet variëren binnen zo'n groepset dus dan is het of het is één persoon of meer personen. 

### ~ 3 min

Reijer van der Zande  
Dus je zou heel graag ook dynamisch die groepen willen kunnen maken. 

Jos Ensing  
Ja dat je zeg maar van 12 tot 1 hebben we een herkansing waar één op inschrijft maar van één tot twee waar twee op kunnen inschrijven. En dus dat het zomaar. 

Reijer van der Zande  
En nu moeten jullie dat dan volgens mij als ik het goed begrijp allemaal per groepje handmatig instellen?

Jos Ensing  
Dan moet je een nieuwe groep zetten eigenlijk. 

Reijer van der Zande  
En je zou dus eigenlijk bij voorkeur gewoon een excelletje of een bestandje willen uploaden waarin je dat even snel in elkaar klopt en dat die dat automatisch daar op basis daarvan gaat genereren. 

Mirjam Veenstra  
Ja en dat we als docent dus ook een andere inkijk hebben dan de student. De student hoeft alleen te weten hier heb ik me op ingeschreven en dit is vol. Daar kan ik me niet meer inschrijven. Maar als docent en ik ga de herkansingen doen dan wil ik kunnen zien hé welke studenten komen vandaag herkansen? Welke toets komen ze doen? Hebben ze een voldoende aan de eisen? Hebben ze de vaardighedenkaart ingeleverd? 

Reijer van der Zande  
En dan hebben we ja. 

### ~ 4 min

Mirjam Veenstra  
Ja dus dat en dat is nu moeten we elk moment aanklikken om te kijken wie er komt. En zij kunnen de student is dus ook niet in staat om even een opmerking erbij te zetten. 

Reijer van der Zande  
Ja oké. En we hebben dus nu een groepje studenten die hiermee moet kunnen werken. Er is een groepje docenten wat hier moet werken. Zijn er nog andere groepen die hier iets mee moeten doen? 

Jos Ensing  
Nou de ondersteuner. Ja maar dat is een groepje docenten dat is een medewerker student. Dat zijn de twee doelgroepen die je hebt. 

Mirjam Veenstra  
En als de tool dusdanig gemakkelijk is dan is het dus ook gewoon mogelijk dat de regisseur het klaar zet. En wat er nu vaak gebeurt is dat de ondersteuner de medewerker van de tool meekijkt en alles klaar zet. Dus dan heb je ook meerdere lijnen en het zou natuurlijk idealiter gewoon heel mooi zijn als het dusdanig gemakkelijk werkt. Dat ik gewoon het er in kan zetten en het staat open. 

Reijer van der Zande  
Ja en wie is de regisseur? 

### ~ 5 min

Mirjam Veenstra  
Dat ben ik in dit geval. Maar kijk voor deze ben ik dat. Maar mijn collega doet het voor jaar 2. En we hebben natuurlijk ook VCM heeft het eigenlijk ook nodig. 

Jos Ensing  
Communicatie ja. Dus er zijn een regisseur is eigenlijk iemand die een leerlijn de leiding heeft over een leerlijn zeg maar. Oké. Dus die staat voor de inhoud. Ja die zet het onderwijs klaar. 

Reijer van der Zande  
Nog net boven de docenten. 

Jos Ensing  
Het is een docent met een plus taak. Ja. Oké. 

Cor Blom  
Is dat dan hoofddocenten dat vormen? 

Jos Ensing  
Nee dat hoeft niet. Nee die zitten meer op beleid de lijnen meer uit te zetten. 

Mirjam Veenstra  
Ik sta gewoon gelijk als mijn collega's alleen ik ik ik bekijk van hey staat het allemaal goed kan de student overal bij en ik kijk dus ook vooruit hey dan hebben we een acteur nodig of dan moet de herkansing openstaan. Dus ik zet dat dan voor ze klaar. De studenten zodat niet alle docenten als we dat allemaal moeten doen is niet handig. En nu heb je gewoon een die het coördineert. Dus ook studenten weten heb ik een vraag over deze koers dan of naar mijn docent of ik mail de regisseur. 

Cor Blom  
Ja. Mooi. 

Jos Ensing  
Dat is vaak een urenkwestie. 

Mirjam Veenstra  
Ja ik heb hier meer uren voor gekregen om dit te doen. Ja. 

### ~ 6 min

Reijer van der Zande  
Dus dan zou jij dat klaarzetten en dan gaan de docenten hiermee verder aan de slag aan de leerlingen. Dus die gaan daar dan op inschrijven. 

Mirjam Veenstra  
Ja. Ik zet het open. De student schrijft het op. De student schrijft het op. Ja. De student schrijft erin en mijn collega die de herkansingen doet die bekijkt het blok want meestal hebben we vijf herkansingsmomenten in over één of twee weken en die gaat dan kijken hey welke studenten komen er naar langs. 

Reijer van der Zande  
Oké. En dan heb je de student mag dus eigenlijk alleen zijn eigen inschrijving zien en of de plek is. 

Jos Ensing  
Ja. 

Mirjam Veenstra  
Ja. 

Reijer van der Zande  
En docenten mag alles zien of alleen van zijn of haar leerlingen. 

Mirjam Veenstra  
Nee docent mag in principe gewoon zien wie kan ja want dat moet ook want ik kan ook studenten van mijn collega herkansen. Ja. En vice versa dus wij moeten gewoon ja. Oké. 

Jos Ensing  
En dan zou het wel makkelijk zijn dat je bijvoorbeeld op een makkelijke manier want het is niet iets wat je wat je in Brightspace gaat maken neem ik aan dat gaat er buiten om. Maar het zou wel mooi zijn dat je kunt ontsluiten bijvoorbeeld via een iframe dat je gewoon een formulier kan plaatsen op een makkelijke manier in een pagina in een course. 

### ~ 7 min

Reijer van der Zande  
Ja. Je wil het graag dus makkelijk integreren. Ja. 

Jos Ensing  
Maar dan zou je functioneel beheren. Ja dat is wel een goeie. Ik denk dat Maurits staat de meest geschikte persoon voor dit. Ja. 

Cor Blom  
Check. 

Reijer van der Zande  
Ja. Ik denk dat we even gaan kijken inderdaad. Een losse tool klinkt logisch maar we gaan even Ik moet even goed kijken wat alle opties zijn. 

Jos Ensing  
API kun je dat misschien koppelen of zo? Ik weet niet hoe ver dat dan wandelt. Er zijn wel mogelijkheden, zeg maar. 

Reijer van der Zande  
Maar laten we eerst even kijken naar jullie ideale situatie. En dan gaan we kijken van daaruit wat we daar realistisch kunnen neerzetten. Gaan we van daaruit verder. 

Mirjam Veenstra  
En kijk, dit is eigenlijk een terugkomende vraag die al 30 jaar wordt gesteld, als ik Jos moet te geloven. En hij komt nu weer actueel aan het licht, doordat we zijn geswitcht van Blackboard naar Brightspace. En voorheen, dan wist ik, dit zijn de momenten. 

### ~ 8 min

Mirjam Veenstra  
Dan stuurde ik de momenten door met de lokale, met wie de herkansing doet. En daarbij per wanneer ik een student wil zien en wanneer het een pauze is voor de docent. En dan ging mijn collega Janice, die werkt bij Tool, is een planner en die zit ook van het toetsbureau. Die zorgde er dan voor dat het op deze manier in Blackboard kwam. Maar omdat dit nu weer allemaal nieuw was, moesten we weer met z'n allen gaan kijken, hoe gaan we dit doen? Hoe werkt het nu in Brightspace? En dan kom je erachter dat iets simpels, tenminste het is niet, en voorheen zou ik nog wel een briefje op de deur plakken bewijzen van, best ingewikkeld is achter de schermen en tijdrovend. Waar wij tegenaan lopen, maar dus ook onze collega's bij Fysio, bij Ergo, bij alle opleidingen van de Hanze. Dus het is niet zo efficiënt. 

Jos Ensing  
En als je terug gaat in het verleden in Blackboard, daar had je nog, zeg maar, plug-ins, building blocks, noemden ze dat, en de rug had een advanced group tool building block gemaakt waar dit allemaal in zat. 

### ~ 9 min

Jos Ensing  
Maar toen is de rug overgegaan op Brightspace, toen is die tool, die ondersteunte ze niet meer, is ook bij ons eruit gegaan. En toen kregen we de platte tool van Blackboard, die al veel simpeler was, waar veel minder mee kon. En ja, dit is nog simpeler, wat nu in Brightspace zit. Dus die functionaliteit, die missen we eigenlijk al veel langer. Ja.

Cor Blom  
En heeft de RUG nu inmiddels ook iets anders in Brightspace? 

Jos Ensing  
Ja, die is in Brightspace gebouwd, dat is een goede vraag. 

Cor Blom  
Oké, ook een punt waar we eventjes naar kunnen kijken. 

Mirjam Veenstra  
Dus eigenlijk zijn we nu gewoon heel creatief met de middelen die we hebben, maar is dat gewoon heel arbeidsintensief en gaat daar gewoon heel veel tijd van ons in verloren, die wij gewoon veel nuttiger kunnen besteden.

Reijer van der Zande  
Hoe zouden jullie graag willen aanmerken, want ik neem, ik zoek een beetje naar van, hoe wil je graag de conversie veranderen? Hoe ga je van lokale tijden naar een planningstool doen? Want jullie gaan ergens zeggen, we hebben deze lokalen beschikbaar en voor deze momenten, is dat iets dat in het systeem wordt opgehaald, is dat gewoon iets wat, wat zouden jullie daar aan willen?

### ~ 10 min

Mirjam Veenstra  
Ik vraag het altijd op bij onze plannen, want er zijn herkansmomenten ingepland, wie, wanneer en wat, en dan krijg ik het in een Excel bestandje aan en daar staat gewoon in, ja, ik kan er één openen, maar. Deze activiteit, die docent, deze ruimte, die tijd, die datum, nou, dat staat er gewoon allemaal in.

Jos Ensing  
Ja, dat zijn dus de gegevens die in webroombooking zouden komen, denk ik. 

Reijer van der Zande  
Oké, en dat webroombooking, bedoel, als we dan toch bezig zijn, we moeten ook even kijken of het mogelijk is om daar misschien direct op in te haken, dat dat er gewoon meteen doorgepaast kan worden, als in, als heb je er weer een handeling tussen. Dus vandaar dat ik even benieuwd ben hoe dit... 

Mirjam Veenstra  
Als jij kunt aangeven, hè, we pakken die momenten vanuit webroom en dat ik dan kan aangeven, goh, ik wil de studenten per kwartier zien. Ja, maar het database op dingen plukt eigenlijk.

### ~ 11 min

Reijer van der Zande  
Maar ja, en anders zit er weer een handmatig handeling tussen, hè, het lijkt maar gewoon zonde, dus als dat niet hoeft, dan... 

Jos Ensing  
Ja, voor Leo, volgens mij. 

Cor Blom  
Ja, Leo is ook, maar die zit bij de paal. Ja, die is inmiddels niet meer, ja, volgens mij is daar nu ook een dingetje mee, dat er nu geen ontwikkelcapaciteit op zit, alleen visiobeheer, maar dat kunnen we ook wel even uitzoeken.

Reijer van der Zande  
Ja, oké. 

Mirjam Veenstra  
Nou, dat wordt best wel een grote klus, als ik het zo hoor, er komen er steeds meer van bij. Ik denk wel dat het een grote klus is, maar heel veel efficiëntie in de aarding. Ja, heel veel efficiëntie, ja. 

Jos Ensing  
Ja, en het is ook een Hanze vraag, het is niet echt specifiek, wij waren misschien de eerste nu, maar dit komt, ja, herkansing en dat soort dingen, ja, dat komt nog veel meer voor.

Cor Blom  
Ja, waar het er ook over gaat, het idee was dat we dit gebruiken als voorbeeld, hè, verpleegkunde, maar dat we dan de multitenant zouden kunnen opzetten, dat laten andere opleidingen hier ook... 

Reijer van der Zande  
Ja, dus dat is ook het idee en de scope om dat te proberen, om dat zo breed mogelijk te maken, dus misschien dat er inderdaad niet 100% op jullie wens inkomt, maar dan, dat is dat voornamelijk om hem zo breed mogelijk te trekken.

### ~ 12 min

Mirjam Veenstra  
Nou ja, en ik denk onze wens is, VCM heeft eigenlijk dezelfde, hè, voor sociale vaardigheden heb je dezelfde, heb je praktijkdoets met een acteur erbij, dus die heeft hetzelfde nodig. En ik denk eigenlijk, bij Ergo werken ze ook met acteurs, bij de toetsen, ik denk dat dit ook wel wel wordt, ja. Het is vooral herkansen, kijk, de toetsmomenten... 

Jos Ensing  
En die staan wel vast. 

Mirjam Veenstra  
Ja, maar dat doen wij natuurlijk ook handmatig, hè, dan maak ik als docent even een indeling, die maak ik als docent, en dat doe ik gewoon klassikaal tijdens de les, of ik zet studenten erin en dan deel ik hem zo van, hé, dit zijn mijn lessen, die deel ik in per half uur, en dan kunnen ze inschrijven, dat doe ik allemaal handmatig. Ja. Ja, misschien als deze tool er komt, dat dan ook nog wel, dat alle docenten dat op die manier kunnen doen, dan hoeven wij geen lijstjes... Ja. ... meer te maken en te doen. Nee. Maar dat is helemaal natuurlijk idealiter, eh...

Cor Blom  
Want nu de examens worden met examensschijfje er, of welke programma wordt daar nu voor gebruikt? 

### ~ 13 min
Nou, dat gebruiken wij nu, want ik doe een praktijktoets, kijk, als ik kijk naar mijn collega's van MK, die hebben gewoon een moment, en dan komen alle, weer mensen kennen, sorry, die hebben gewoon een blok, op het Zen, ik heb vooral verschillende lokalen met surreanten, en dan komen alle studenten in één keer.
Ja, ja. Maar kijk, onze toetsen... 

Jos Ensing  
Zo versnipperd. 

Cor Blom  
Ja, precies. Ja. 

Mirjam Veenstra  
Wij hebben geen, hè, en de andere collega's van de argumenteren verzorgd, die hebben weer een verslag wat ingeleverd wordt, maar wij hebben echt een praktijktoets, dus de student doet de skills na, en die beoordeel ik. Dus dan moet je echt gaan inplannen op tijd en op moment. 

Cor Blom  
Ja, precies. 

Mirjam Veenstra  
En meestal hebben wij drie lesblokken voor jaar twee, en in beide, in alle drie lessen, wordt dan getoetst, en die moet ik dan handmatig gaan indelen. En voor jaar één zijn dat twee lessen van drie uur, dus dan heb ik zes uur in totaal, die deel ik één. En daar schrijven ze zich op in. Ja. Maar ja, dat doet elke docent gewoon met een word. 

Jos Ensing  
Ja, dat is eigenlijk hetzelfde principe.

### ~ 14 min

Mirjam Veenstra  
Ja. Dat zou je ook... Het zou hier, hè, als dit een hele mooie tool is, die heel intuïtief werkt, dan zou elke docent dat gewoon kunnen gebruiken. Ja. 

Jos Ensing  
Gelijk lokaal reserveert en... Ja. Maar goed, dat is zeker...

Reijer van der Zande  
Maar dan zitten we wel even uit, want dan zitten we nog wel met een stukje... Want eerst ging het nu vanuit dat Map Manager was het, geloof ik, die we net noemden. Dus dat was specifiek voor deze casus. En deze is wat breder. Want dan moet je ook zelf iets kunnen opzetten, neem ik aan. 

Mirjam Veenstra  
Nou ja, in principe zou je gewoon in Webroom kunnen aangeven, hé, deze klas, dat moment dus, wil die inschrijvingsmomenten. En dan zouden de studenten zich van jouw klas... Maar dan zou je hem in een groep moeten zetten, in je klasgroep. 

Jos Ensing  
Dus je hebt gewoon een lokaal geblokt voor een aantal uren. En dat lokaal wil je dan eigenlijk onderverdelen in tien studenten die een inschrijvingsmoment hebben, zeg maar. Dus je reserveert een lokaal voor drie uur. En binnen die drie uur heb je die mogelijkheid van inschrijving. Ja, inderdaad, inderdaad. En dan moet je hem ook weer uitschrijven als je denkt van, ik ga toch bij de McDonald's werken vandaag.

### ~ 15 min

Mirjam Veenstra  
dat kan bij die niet, hè. Dan is het gewoon ingeschreven. Vast afvast. Ja, vast afvast. En bij de herkansingen is dat ook zo. Dus dat is ook nog wel eentje die bij je moet. Tot 24 uur van tevoren kunnen zij zich nog uitschrijven. Maar zijn ze later, dan is het een gemiste kans. Het is wel een handig om te weten. 

Reijer van der Zande  
Dat zijn wel belangrijke randvoorwaarden om eventjes... 

Mirjam Veenstra  
Dus eigenlijk moet hij gewoon open blijven staan. En moet er iets in dat je kunt zeggen, oké, dan is hij gesloten.

Cor Blom  
Ja, ja, ja. Gesloten van inschrijving. 

Reijer van der Zande  
Ja. En dat kan de docent dan bepalen waarschijnlijk. En dat is dan een triggermoment. Dus dat wil je van tevoren kunnen instellen. En dan gaat hij gewoon vanaf een x-moment gaat hij...

Mirjam Veenstra  
En eigenlijk zul je inschrijven tot aan dat moment. Want wij willen natuurlijk zo efficiënt alle momenten gevuld hebben. Maar uitschrijven mag maar tot 24 uur van tevoren. Dus daar ligt dan even een... 

### ~ 16 min

Jos Ensing  
Ja. Wat je ook nog kan doen is ook nog dat je een aantal plekken standaard beschikbaar hebt. En als die vol zijn, dat dan pas de volgende komen. 

Reijer van der Zande  
Ja, dat je een rolling... 

Jos Ensing  
Ja, want anders krijg je op een gegeven moment dat één heeft achteraan het blok en de ander vooraan. Dus je zou kunnen zeggen van we willen gewoon... Dit moment is nu vrij. Je kunt doorklikken en er komt steeds een moment bij. 

Reijer van der Zande  
Volgens mij is dat niet heel moeilijk. Maar het is wel... Ik denk in eerste instantie... Nice to have. 

Mirjam Veenstra  
Ja, zeker. 

Reijer van der Zande  
Als er wat tijd over is, dan plakken we die erbij aan. Maar ik denk dat dat wel... 

Mirjam Veenstra  
Misschien een doorontwikkeling is. 

Reijer van der Zande  
Ja, precies. Maar het is goed om mee te nemen. Die gaan we dan zeker even opschrijven. En wat moet de representatie zijn naar leerlingen toe? En wat wil je als representatie van het rooster hebben naar docenten toe? Want we hebben nu zometeen een inschrijftool. En dat staat dan zometeen ergens online. Daar kunnen we ergens waarschijnlijk bij. Dat kunnen we inzien. Dus leerlingen kunnen dan inderdaad inzien. Wil een docent bijvoorbeeld ook een pdfje kunnen uitdraaien?

### ~ 17 min

Mirjam Veenstra  
Oh, zo. Nou ja, dat zijn hele mooie opties. Want dan kun je hem gewoon afdrukken. En dan kan ik mijn cijfers erachter schrijven. En dan heb ik gelijk een overzicht deze studenten komen. Dus dan kan ik het meeste als ik dit heb, dan moet ik eerst nog even kijken. Volgen ze, mogen ze meedoen aan de toetsing. Dus dan kan ik er een vinger achter zetten. En vervolgens zet ik het cijfer erachter. Want die cijferlijst moet ik weer invullen. En dan heb je een mooi overzicht waarin het ook makkelijk kan.

Reijer van der Zande  
En zou je dat liever op papier doen? Zou je dat misschien zelfs in de tool willen doen? 

Mirjam Veenstra  
Ja, dat kan ook in de tool. Maar ja, dat maakt niet zoveel uit. In de tool met exportfunctie, zoiets. 

Reijer van der Zande  
Ja, nou ja, en ik weet niet wat allemaal kan. Maar ik probeer gewoon even zoveel informatie. Want wat voor jullie heel goed gaat werken, dat wil ik heel graag weten. Het is makkelijker om dit soort dingen vooraf in te bakken. Als dat je achteraf zegt van ja. Hadden we het maar even net anders vormgegeven, dan hadden we dit nog gekund.

Mirjam Veenstra  
Ja, nee, dat zou een hele mooie optie zijn. Want dan zou ik als herkanser gewoon zeggen, ik heb morgen herkansingen, inschrijftijden. Of ik heb pas om vier uur, morgenochtend print ik een lijst uit. 

### ~ 18 min

Mirjam Veenstra  
Check ik even iedereen en dan heb ik ook gelijk op papier wie wanneer komt. Wij doen tijdens een toetsmoment heel veel digitaal, de beoordelingen doen we digitaal. Dus dan is het heel fijn als je even op papier nog hebt. Oké, die komt hierna, die geef ik vast een casus. Dat is, dat is heel fijn. 

Reijer van der Zande  
Oké, ik kijk even, ik had wat aantekeningen gemaakt.

Mirjam Veenstra  
Kijk even door wat we... Ja, zeker, zeker en ik denk, ja, voor ons is het gewoon belangrijk dat die in ons LMS komt, in ons leersysteem. Dus dat die een plek krijgt in Brightspace en dat we daar makkelijk in kunnen afvragen.

Reijer van der Zande  
Ja, dat die makkelijk vanuit Brightspace te openen is en te gebruiken is. Ja, en je kunt natuurlijk in Brightspace ook een internetpagina zetten, hè. 

Jos Ensing  
Nou weet je, weet je, ik zit ook te denken. Kijk, je hebt binnen een koers, heb je een aantal van de studenten als gebruiker toegevoegd. Het zou mooi zijn dat je alleen die gebruikerslijst die in die cours zit, dat die toegang hebben tot de tool. Ja. Oké, ja. 

### ~ 19 min

Mirjam Veenstra  
Ja, dat zou inderdaad... In die gebruikerslijst staan ook alle docenten, maar die staan erin als een andere rol. Dus als die rolverdeling allemaal gelijk overgenomen kan worden, dan kun je ook gelijk zien... Nou, je vraagt me wel heel veel, dus... 

Reijer van der Zande  
Nee, nee, nee, maar dit is heel goed, hè, dit is juist wat ik, dit is de juiste informatie die ik nodig heb. 

Mirjam Veenstra  
Want je bent wel heel goed bekend met Brightspace, denk ik, en hoe het werkt? 

Reijer van der Zande  
Nou, net zo lang als dat jullie er mee gedaan hebben, en ik ben eigenlijk sinds dit jaar aan het afstuderen, dus ik heb er nog heel weinig mee gedaan. Dus ik heb er inderdaad een halfjaartje mee gewerkt, dus voor mij is het ook allemaal uitzoeken. En ik merkte in mijn persoonlijke ervaring met het eerste halfjaar dat het heel erg zoeken was, waar moet ik nu wat doen en hoe kan ik nou inzien wat ik ingeleverd heb. Ik vond het heel onduidelijk en vaag hoe het nou precies zat. 

Jos Ensing  
Ja, dat ligt ook een beetje aan... Welke instructies je hebt gehad bij de... Hoe mooi de docenten dit vormgegeven hebben, hè? 

Reijer van der Zande  
Niet, het was gewoon, dit is Brightspace, succes, dat was de instructie.

### ~ 20 min
Mirjam Veenstra   
Ja, en wij hebben op zich, kijk, dit is eigenlijk hoe het voor de studenten is opgebouwd. Dus ze hebben gewoon de cursusinformatie, waar we mee werken, wat voor leeractiviteiten we tijdens de lessen doen, en inleverpunt, dit is belangrijk voor bij de toetsing. En dit zijn gewoon voor ons ook de, waar ze kunnen vinden, hé, wat moet ik doen, hè, dit is gewoon de inlevering. En dat is de inlevering van de vaardighedenkaart, dus zij moeten wat aandragen, als dat voldoende is, dan mogen ze door naar de proeven, en bij de proeven kunnen ze zien wat is de rubrics, en bij het inschrijven, daar komt dus een stukje tekst met de link. Ja. En wat mooi zou zijn, is dat hier eventueel een pagina in komt, waarin gelijk ook het menu staat. Ja, oké. Kijk, deze link gaat nu door in Brightspace, naar de groepen, en dat zou gewoon, als het via een losse website is, zou het heel logisch zijn, als die... Ja. ...dat die gewoon erin opent, zeg maar. Ja. 

### 21 min

Jos Ensing  
Als Blackboard, of Brightspace Key User, is er ook een tooltje, zodat wij een nieuwe course kunnen aanvragen. Dat is door Maurits gebouwd. Ja. En die, daar is eigenlijk een aparte course, duikt daarvoor op, waarin dat tooltje zit. Dus, dus, er is wel een mogelijkheid om iets, want dat heeft hij wel buiten, ik weet niet waar hij het in ontwikkeld heeft. Ja. En dat is iets wat ik vroeger voor hun gemaakt heb in Formdesk. Ja, ja. En daar hebben we het voor gebruikt. Maar nu hebben ze daar, heeft Maurits daar een ander toeltje voor gebouwd. Dus, dus, op zo'n manier dat ontsluitend, ja, dat zijn wel mogelijkheden. Ja. En Maurits weet er wel meer van. 

Cor Blom  
Ja, want ik hoorde laatst ook dat er redelijk wat plugins al beschikbaar zijn, ook voor Brightspace.

Jos Ensing  
Het zou kunnen dat er iets bij zit, wat al werkt. Ja, of dat we in ieder geval kunnen gebruiken, als met koppeling, met andere dingen. 

Jos Ensing  
Ja, ik ben niet of er open source is, wat je kunt gebruiken en zelf kunt aanpassen nog. Maar je zou het zeker bij de rug kunnen informeren. Ja. 

Reijer van der Zande  
We hadden net even, even teruggrijpt op een klein stukje hiervoor. We noemden net dat leerlingen vanuit de course, die moeten toegang hebben. Zijn er ook situaties waarin dat niet het geval is, dat je dus als een publiek inschrijfmoment hebt. Dus dat dat voor buiten een course beschikbaar moet zijn. 

### ~ 22 min

Mirjam Veenstra  
Dat kan als je overstijgend, zoals nu met ons oud curriculum. Snap je waar ik heen wilde was? Nee. De course staat nu voor mijn huidige studenten. Dus ik heb SLO 2, heb ik nu net mee gestart. Maar ik heb ook studenten van vorig jaar, die SLO 2 nog niet hebben afgerond. En die zich willen inschrijven voor een herkansing. 

Jos Ensing  
Maar die zouden zich dus eigenlijk in die actuele course moeten inschrijven. Ja, nou ja, daar zijn we dus een beetje met stechelen.

Mirjam Veenstra  
Hoe gaan we dat doen? Moeten ze dan in de huidige course? En in Blackboard hadden we dan een course voor herkansingen. Een losse course voor herkansingen. En daar kwam iedereen die herkansen wilde daarin. Dat is ook niet heel efficiënt. Ik wil als docent ook niet alle courses terug moeten om herkansingen open te zetten. Dus dan zou het heel fijn zijn als de herkansingsmomenten ook openstaan voor studenten buiten een course. Maar ja, dat wil je wel weer.

### ~ 23 min

Reijer van der Zande  
En dan zou je misschien als docent zijn een approval op willen geven. Of je dat wel of niet wil laten doorgaan. 

Mirjam Veenstra  
Ja, dat is wel weer selectief. Want je wilt natuurlijk niet iedereen gewoon in zo'n course hebben. En mensen die denken. Oh, dat is leuk. Ik schrijf me gewoon in en dan hebben we straks.

Reijer van der Zande  
Nou, dat nemen we mee. Ik weet niet wat mogelijk is, maar het is goed om er even over na te denken. 

Mirjam Veenstra  
En ik weet ook niet wat mogelijk is, want ik denk Janice kan natuurlijk wel een overzicht vinden van. Hé, deze studenten moeten het nog doen en die automatisch ergens, die zou vanuit Osiris dus wel kunnen kijken. Oh, deze studenten hebben allemaal SLR 2 nog niet gehaald, dus die moeten in de aanmerking komen voor de herkansing. 

Reijer van der Zande  
Ja, dus dan zou je daarvan een filter. Precies. Ja, op basis van studenten, maar eh. Maar dan zou er inderdaad een koppeling naar eh, eh, Progress, eh, Osiris, ja. Ja, Progress, ja. Kom, wacht. Ja, vroeger ook de Hanse, maar dat was mijn tijd.

### ~ 24 min 

Mirjam Veenstra  
Ja, maar goed, dus in dat, in dat, dan zou het wel fijn zijn als ze dat ook uit andere courses kunnen inschrijven, ja. Ja, oké. Ja, maar ja, goed, dat is er misschien wel. Ik weet niet hoe dat dan werkt, want nu heb ik natuurlijk de studenten van vorig jaar, maar ja, volgend jaar heb ik misschien ook studenten. Ik heb ook nu bijvoorbeeld studenten, die zitten al in het vierde jaar, maar die moeten dan op een toets van het eerste jaar doen. Ja. Dus die schuiven wel steeds door, dus het is natuurlijk ook wel wat als je elk jaar vanuit Osiris die lijst moet opvragen en in moet voeren, maar goed, dat is misschien handmatig als dat in bulk gaat, makkelijker dan.

Reijer van der Zande  
Ik hoop, ik verwacht dat er gewoon een, eh, dat je binnen Osiris gewoon een lijst kunt doen met zo'n, voor wie staat ingeschreven voor deze studie en welke vakken staan open en dat je daar gewoon op een manier die informatie daaruit kunt trekken.

Mirjam Veenstra  
Importeren, exporteren. 

Reijer van der Zande  
Nou, bijvoorbeeld een CSV, en dat is inderdaad het makkelijkste voorbeeld, ehm, en dat je misschien als docent dan een lijst krijgt met van wil je deze leerlingen approven of niet. Ja. En dat je dat misschien, nou, dat mogen we dan zelf misschien kijken, maar dat is dan, eh.

### ~ 25 min

Jos Ensing  
Ja, dat jij er twee ingangen hebt. Eén, dus eigenlijk heb je, gebruik je de gebruikers uit, uit een course, maar dat je ook nog kunt uploaden van dit zijn de mensen buiten de course. 

Reijer van der Zande  
Ja, nou dat is inderdaad een optie. Ja. En een CSV export zou heel fijn zijn en dan moet je het alsnog wat later doen en misschien dat er ook wel een directe koppeling is dat dat. Met Osiris. Met Osiris kan. Maar dat is, ehm. Ik denk dat je dan wel een paar jaar verder bent als je dat dan nog in elkaar hebt.

Cor Blom  
Ja, nou ja, in theorie hebben wij wel, eh, we halen alle data van Osiris halen we al elke nacht eruit. Oké. Dus we hebben een, een, een hanze integratie platform, dus in theorie hebben we wel data, maar de vraag is denk ik van hoeverre wil je het automatiseren, want de, het werkt wel nog steeds met SLB'ers, de studenten, student loopbaan begeleider. Ja, ook. Waarmee je er eigenlijk ook bespreekt van hé, je hebt hier nog iets, je moet nog herkansen dit en dat. Hm, hm. Dat je zou kunnen kijken van misschien als je iets van een tool ontwikkelt waarin je dan inderdaad de lijst hebt met overgestaande herkansingen en dat dan die SLB'er of wie dan ook, zeg maar, dat linkje, eh, kan delen met diegene, met wie je dan in gesprek gaat van hé, hier kan je op inschrijven, schrijf je dan daar maar op in, zonder dat daar een check-up zit of wat dan ook.

### ~ 26 min

Mirjam Veenstra  
Ja, ja, dat zou ook mooi zijn, ja. 

Jos Ensing  
Maar is dat niet al onderdeel van een groter geheel, want ze zijn ook bezig met een studenten, bij studenten, eh, hoe noem je dat, eh, een soort. Een studentendossier achter. Ja. Ja, dat is waarom. Daar zijn ze ook met bezig om dat op te bouwen en ik denk dat dat ook een soort dashboard is waarin studenten en SOB'er. 

Cor Blom  
Oh, dat is waarvan Sjoerd, ja, ja, ja, ja, oh ja, ja, dat is, ja, maar dat is ook nog wel een paar jaar. Ja, precies. Ja, maar dat zou zeker, ja, maar dat zou ook wel weer. 

Jos Ensing  
Ja, volgens mij zijn ze net, net eigenlijk afgetrapt om daarmee te beginnen, zo'n studenten portal. 

Cor Blom  
Ja, dat hoor je straks ook wel over bij Armin, ja, ja, ja. Dus er speelt ook wel iets waar je misschien op in kan gaan. Ja, precies, ja, ja. Ja, want kijk, je kunt het wel helemaal automatiseren op basis van data uit andere dingen, maar je hebt altijd uitzonderingen, dus misschien zou je juist vanuit uitzonderingen al. Ja. En je hebt standaard die courses met degene die moet herkansen of die daar in aanmerking voor moeten komen en daarnaast heb je dan nog een examen van mensen die er op een bepaalde manier bij kunnen. 

### ~ 27 min 

Reijer van der Zande  
Ja, maar voor mij is het dus belangrijk dat je in ieder geval dus die leerlingen erin kunt krijgen die er gewoon standaard in horen en dat er in ieder geval een manier, een optie is om leerlingen daaraan toe te voegen. Ja. Eh, en dan is het even zoeken naar wat daar het ideaal in is. Of wat nu heel pragmatisch gewoon gaat werken. Ja, ja, ja, zeker, ja, ja. Dat eh, oké, neem je mee. Ik eh, ja, ik wil zeggen, er worden nu heel veel dingen bijgetrokken en dat is heel goed, maar het is ook even kijken wat dan inderdaad reëel is.

Mirjam Veenstra  
Ja, zeker. 

Jos Ensing  
En ik denk dat het handig is dat je met een flexibel platform begint, zeg maar. Ja, gewoon klein beginnen. 

Reijer van der Zande  
Ja, klein beginnen, sowieso. Ja. Dat is eerst de basis en dan van daaruit uit. Dat is een bloktelefoon, ja. Ik heb een iPhone, maar de bloktelefoon om met je dingetjes erbij te doen en zo. Ja, ja, ja, precies. 

Cor Blom  
Ja, want dat is inderdaad wel goed om te weten. Het idee is dus, daarom is het ook een onderdeel van mijn leergemeenschap, eh, als Reijer hiermee klaar is, eh, dan willen we bij informatisering of bij DS tegenwoordig, willen we het dan onderbrengen en in principe ook kunnen laten doorontwikkelen.

### ~ 28 min

Cor Blom  
Ja. Of vanuit daar, of weer vanuit ons en dat soort dingen. Dus, eh, we gaan inderdaad hier iets moois neerbouwen conform je opdracht en daarna gaan we ook ermee verder bouwen. 

Jos Ensing  
Ja, dat is wel een hele positieve verandering, want ik werk natuurlijk al honderd jaar bij de Hanze. Er is ooit iemand begonnen, Jan Suur, met een voedingsberekeningsprogramma. Ja. Nou, dat, eh, Jan Suur ging weg en daar, daar zit... Heel top. Ja, ja, ja, dus, eh, ik heb, ik heb nog meer van dat soort dingen. Dat zijn hele mooie initiatieven, ook om een EPD te bouwen. Ja, precies. En dan begint er ergens iemand en dan is de overdracht er niet en, en dan, dan stopt het ook weer. Ja, ja, ja. Dus dit is, eh, dit geeft naar de toekomst, eh, wat meer garantie. Ja. Dat is, eh... Dat is fijn. Ja. Dus, ja. 

Reijer van der Zande  
Eh... Ik denk dat we de belangrijkste stukken gehad hebben. Missen jullie nog iets? Hebben jullie nog een idee wat, nog andere wensen of... Nou, sowieso, als jullie nog dingen, tegen dingen aanlopen, mail mij vooral.

### ~ 29 min

Reijer van der Zande  
Ja. Eh, want ik ben daar, ik ga nu de komende weken, de eerste weken ga ik er nu mee bezig om dit op te zetten. Ja. En daar een eerst plan voor te maken. Het programmeren ligt nog een stukje verder. Ja. Dus mocht je nog tegen iets... ...aanlopen van, hé, dat zou echt fijn zijn of zou dit ook kunnen, vooral op de mail gooien, eh, of het naar mijn kant te slingeren, want dan kan ik het gewoon meenemen. 

Jos Ensing  
Weet je, ik werk van maandag tot en met donderdag, dus ik zit altijd in teams, dus als je een chatberichtje wil sturen en een korte vraag hebt, dan kun je dat altijd doen.

Mirjam Veenstra  
Ja. Dus dat is altijd snel. 

Jos Ensing  
Ja, ik probeer, ja. Ja, ja. 

Mirjam Veenstra  
Ja, en ik ben maandag, dinsdag en vrijdag. Ja. En, nou ja, Jos is echt the man of the tools. Ja. En alle ins en outs, en ik meer en meer van, ik geef het van... Meer de inhouds, ja.
Ik werk ermee en ik heb affiniteit met ICT, dus ik kom er wel eens heel eind in. 

### ~ 30 min

Reijer van der Zande  
Ja, leuk. Maar eh, ik ben eh, eh, in basis alleen maandag beschikbaar. Ik werk dinsdag tot en met donderdag werk ik voor mijn betalende baan. Ja, oké, oké. Eh, en ik probeer dan, eh, op die maandagen probeer ik genoeg werk te genereren dat ik in het weekend een klein beetje erbij kan doen. Ja. En dan hopelijk op die manier eraan te werken. Ja. Eh, dus dat is wel even handig om te weten. Ja. Eh, zou jij misschien nog, eh, want je zei dat je een Excel-tje kreeg vanuit de werkvoorbereider, met informatie die dan gebruikt wordt. Hm-hm. Eh, zou je me dat, eh, geanonymiseerd, mag, ik hoef niet, maar ik ben even benieuwd welke, in welke vorm het is en hoe, hoe het eruit ziet, eh, wat, wat daarin werkt. Eh, en heb ik straks eventueel toegang tot... Eh, en heb ik straks eventueel toegang tot... Nou, hoe het, hoe het nu werkt. Met Brightspace bedoel je? Nou, ja, of dat anders misschien daar een paar screenshots van kunnen komen, eh, want dan heb ik een beetje een idee van, van waaruit we vertrekken, eh, eh, met een beetje een visuele, eh, beeld 

Jos Ensing  
Jij, jij bent gewoon Hanse student? Ja. Zou die dan ook als student in de course kunnen of niet? Ja, ja, als die, ja, nee, je kan, ja, je zou, eh, gewoon kunnen toevoegen, dan kun je wel kijken. Ja. Ja. Ja, als die, ja, nee, je kan, ja, je zou, eh, gewoon kunnen toevoegen, dan kun je wel kijken. Ja. Ja. Moet je alleen niet aanmelden.

### ~ 31 min 

Reijer van der Zande  
Nee, dat is prima, maar dan heb ik een beetje een idee hoe het nu werkt, maar dan kan ik eventjes dat, eh, keertje controleren of een keertje kijken van, nou, maar gaat dit ook aan wat het nu doet ook helpen? Want als het niet beter wordt, dan moet ik wel een referentiekade voor hebben. Ja, dus doen we dat het beter wordt, hè? Ja, nou, precies, dat, dat is de insteek, eh... Ja, en ongetwijfeld als je het... Ja, en ongetwijfeld als je het gaat uitwerken in dit, eh, deze opnames, dan... Ik kom graag tegen je vragen, ja, ja. Ja. Ik denk dat we wel een paar keer contact gaan hebben ergens met, met vraagjes, maar dat, eh... 

### ~ 32 min

Mirjam Veenstra  
Ik heb alleen het overzicht wat jij nodig had voor, eh... Kijk, ik had deze, dit, dit is wat ik in eerste instantie had aangedragen, maar dit komt niet uit wat ik aangedragen krijg van de planner. Maar dit was nu omdat wij het even anders moesten doen, hè? Oké. Dus dan moet ik eigenlijk even zoeken naar Janice. 

Jos Ensing  
Ja, ik wou zelfs goed Janice even vragen of ze gewoon even een voorbeeldje kan, kan aanleggen. Ja, ja.

Reijer van der Zande  
En het mag heel willekeurig zijn. Het gaat er vooral om van hoe worden de, eh, als het, zeker als het automatisch gegenereerd is, hoe worden de kolommen genoemd? Want dat zijn de, de, als, als het een Excel-tje moet worden om die interactie te doen, zijn dat de, de, de, de keywords die ik moet gebruiken om erop in te haken. Ja. Ik kan heel makkelijk met een stukje Python zo'n Excel-tje... ...bewerken, eh, maar dan moet ik wel weten waar ik op in moet raken. 

Jos Ensing  
Precies. 

Mirjam Veenstra  
Dan moet je weten hoe het aankrijgt, geleverd. 

Reijer van der Zande  
En ik opteer toch voor de, de automatische integratie, dat is, dat is de a-technisch leuker en de tweede gewoon veel gebruiksvriendelijker. Dat zeker. Eh, maar dat is even, dat is een onderzoekje om te kijken of dat ook lukt. 

### ~ 33 min

Jos Ensing  
Het probleem daarvan is natuurlijk wel dat als er iets verandert in het basissysteem, dat, dat dat weer doorgrijpt op je, eh, wat eraan hangt.

Cor Blom  
Ja, een webroom, eh, vervangen wordt en dat zal er ook aan komen, denk ik. Ja. 

Jos Ensing  
Dat is ook een soort houtje-touwtje oplossing. Ja. Gegeven, eh, al met gifen en zo. Tegen de tijd, ja. Dat is al heel lang geleden ook al. Ja.

Cor Blom  
Ja, ja, zo, maar gelukkig worden al die dingen uiteindelijk wel omgebatterijd, maar goed. 

Jos Ensing  
Nou, de standaarden zijn ook beter, denk ik, nu waar je er gebruik van kan maken. Ja. Ja, ik denk dat er... Ik ben nooit nog begonnen met gewoon de oude, eh, oudwetse ASP's, eh...

Cor Blom  
Oh, echt? 

Jos Ensing  
Ja, spaghetti code. Oh, ja, ja. Haha, ja, ja. Oh, ja. Fantastisch. Dat is wel leuk, daar had ik online een vervanger gemaakt voor Indato. Konden ze bij het conservatorium niet meer uit de voeten. 

Cor Blom  
Nee. Haha, ja. Ja, grappig, ja.

### ~ 34 min

Mirjam Veenstra  
Is het ook een idee om Janice nog te vragen? Voor invloed, voor deze zijnde toe? 

Jos Ensing  
Ik denk, als je, zeg maar, een basisplannetje hebt, dan kun je het wel even langs een paar mensen houden. Ja, ik denk ook. Dan kun je dat wel, eh... Ja. Misschien met de roogstraat, of met de planners, eh... Ehm, 

Reijer van der Zande  
ja, ik denk wel dat het heel handig is. Zeker als, eh, want zij leveren natuurlijk informatie voor aan. Het is denk ik wel belangrijk om ook in de kaart te hebben wat voor hun gaat werken.

Jos Ensing  
Ja. Ja, kijk, en ik weet, kijk, het gaat nu een kant op, maar als je ook weer teruggaat naar de planners, dat zij dingen meenemen en zo, ja, dan... Dan moeten zij wel iets meer weten. Maar ja, we gaan kijken hoe ver we komen. Ja. 

Reijer van der Zande  
In basis gaat het om gereserveerde tijdslotten om op te delen onder studenten die ingeschreven zijn. Ja, heel plachtig. Ja, daar gaan we met beginnen en dan gaan we rustig van daaruit gaan we het onderhouden. Ja, dat is must have.

Reijer van der Zande  
Precies. 

### ~ 35 min

Cor Blom  
Ja, mooi. Nou, het schildert dat jij erop zit. Je merkt dat je geen starter bent, wat dat betreft. Dat is positief. 

Reijer van der Zande  
Nou, ik hoop het. 

Cor Blom  
Ja, dat is heel goed. 

Jos Ensing  
En je bent onderdeel van de leergemeenschap. Is dat vanuit, doe jij een aanvullende studie nu dan?

Reijer van der Zande  
Ik werk hier gewoon als programmeur. Ik ben recent weer echt naar programmeren teruggegaan. Ik heb een tijdje DevOps gedaan. Maar ik heb daarnaast, ben ik in de deeltijdopleiding. Ik heb nooit papiertje gehaald. Oké. Dus ik ben er wel in het werkveld gerold, heb er dingen gedaan, maar papiertje nooit gehaald. Ik had bepaald, ik wil het papiertje er gewoon bij hebben. Dus dat ben ik langzaamaan, de afgelopen vier jaar heb ik dat gedaan. En dit is dus het laatste stukje. Oké. En dat is ook heel erg leuk om te leren. Nou, dit project kwam daar om de hoek kijken.

Jos Ensing  
Ja, leuk man. Ja. Ja, dat is ook wel leuk dat je iets achter kan laten. Zeg maar. 

### ~ 36 min

Reijer van der Zande  
Ja, ja. Zeker. Nou, ik heb er met vrienden wel eens tijdens de opleiding over gehad. Daarom vind ik dit heel leuk. We hebben zoveel studenten rondlopen die kunnen programmeren, die iets kunnen. En dat wordt dan, dat wordt momenteel niet benut. En dat is deels een keuze vanuit de Hanze. Ze staan er nu voor mij iets opener in om daarnaar te kijken. En het lijkt me gewoon heel leuk om daar, om daar een basis voor te leggen. Kijken of we daarmee kunnen. Ja, zeker. Want je hebt daar best wel veel potentieel rondlopen. En dat wil niet zeggen dat het allemaal fantastisch is. Maar je moet er wel, je kunt er wel wat mee. 

Cor Blom  
Je zit er wel tussen, zeker.

Jos Ensing  
Ja. Ja, absoluut. Ja. Ja, Hanze heeft heel lang niets niet ontwikkeld, hè? Toch? Nee, nog steeds officieel. Officieel niet. Nee. Dus het is echt een pilot om te zeggen van oké, en dat gaan we dan ook met een flexibele capaciteit en in vorm van onze leergemeenschap doen. Ja. En dat is het idee. 

Jos Ensing  
En bij de rug. Ja. En dat hebben we altijd wel gedaan. Oké. 

Cor Blom  
Nou ja. Ja. Ja, maar dat is, ja, goed, wat Reijer ook zegt, dat is echt wel kennis wat je daar laat liggen. Want sommige studenten zijn zoveel verder dan, met alle respect natuurlijk aan onze medewerkers, maar goed, die zitten met een eigen, ja, een eigen scope, een eigen werkzaamheden. Ondertussen gebeurt er zoveel meer. En dan denk ik, ja, dat is toch iets waar we moeten gaan benutten. Ja. Dus ik ben blij dat ze inderdaad, dat we nu zover zijn van oké, we gaan nu zelf dingen ontwikkelen. En we gaan er niet zo van, oké, dat gedoofd beleid is, nee, we gaan er echt iets, iets voor neerzetten, hoe we er weer op gaan. Ja. En wanneer kunnen wij het ontwikkelen, wanneer moet de afdeling informatieën het ontwikkelen, wanneer moet er uitbesteed worden, etcetera. Nou, is dat een mooie stap, denk ik. Ja, zeker. Ja. 

### ~ 37 min

Mirjam Veenstra  
Ah, kijk, dit is 'm. Ik zat te kijken naar, ze heeft het me zo gestuurd. Dit komt zo uit Excel. Ja. Dus de dag, de datum, de tijd, de duur, de module, de locatie en de medewerker. Dat is wat ik aangeleverd krijg. 

Cor Blom  
Ja. Even kijken, dat is, een module is dan de code die ook uit Osiris komt, toch? Nee. Of niet? Hoe leg je de link met Osiris of wat dan in het gedaan? 

Mirjam Veenstra  
Ja, denk ik dan of niet, Jos? 

Jos Ensing  
Even kijken hoor, herken ik een Osiris code? Nee, dit is geen Osiris code. Dit is gewoon hoe wij het noemen.  

Reijer van der Zande  
Ja. Dat klinkt inderdaad als de...

Mirjam Veenstra  
Of SLO herkansing. 

Cor Blom  
Ja, dat is wel even een ding. Stel maar dat jullie dachten... Ik denk dat dit vanuit... 

Jos Ensing  
Dit is niet zo vanuit Osiris getrokken, nee. Nee, dit is vanuit Webroom getrokken. Oh, zo ja. Oké, dus dit is gewoon puur de lokaalplanning.

### ~ 38 min

Mirjam Veenstra  
Ja, dit is de lokaalplanning. Dit is gewoon vanuit het roostersysteem. Ja, dus niet wat het is. Nee. En... Hier staat dus ook de modulebenaming van hoe wij het noemen in ons rooster. 

Jos Ensing  
Ja, en ook het hele tijdslot. Dus uiteindelijk bepaal je als regisseur van de tijdslot van 9 uur 30 tot 12 uur 30, heb ik 20 studenten die daar iets kunnen doen.

Mirjam Veenstra  
Klopt. En kijk, dit is gewoon de volle 3 uur die hierop staat, maar een lesuur is 50 minuten. Dus eigenlijk zit er ook nog een half uur pauze tijd in voor de docent. Dus bij de herkansingen, als we het allemaal inplannen, ja dan moet je een nontstop door, dat is gewoon niet haalbaar. Dus ik plan dan vaak, blok ik een momentje in het midden, maar dan heb je even pauze. 

Reijer van der Zande  
Maar je wil dus als docent dus ook een tijdslot kunnen blokken? 

Mirjam Veenstra  
Ja, en eigenlijk... 

Reijer van der Zande  
Dat is dus toch wel een vraag die er... 

Mirjam Veenstra  
Ja, en eigenlijk doe ik dat als regisseur van tevoren. Dan geef ik dus aan, oké, dit is wat ik aangeleverd krijg, ik wil per  kwartier toetsen, 1 student. Of ik wil per half uur toetsen, 2 studenten. En dan kies ik 1 van die momenten, die haal ik er tussen uit. 

### 39 min

Reijer van der Zande  
Ja, kijk, heel fijn.

Mirjam Veenstra  
Dus dit is wat ik krijg. Dus deze kan ik wel doorsturen. Dus het is vrij basic.  Ja, nee, maar dat is goed. En uiteraard kan ik wel de OSIRIS-code erbij aanleveren. Ja, dat is geen probleem. Nou ja, dat is inderdaad een idee.

Cor Blom  
En als je daar dan ook iets van een naamgeving, een unieke naamgeving moet gaan hanteren, dan is het misschien wel verstandig om dan te gebruiken wat er al bestaat. 

Reijer van der Zande  
Ja. En ik ben inderdaad nog even, en dat is denk ik niet voor nu, maar de, ik ben nu ook Webroom?

Jos Ensing  
Webroom Booking. Webroom Booking. Ja, toen heette het Booking alleen, volgens mij. Maar het begon als Webroom Booking. Ja. 

Reijer van der Zande  
Maar die, hoe die daar inderdaad cursus benoemd, en hoe het binnen OSIRIS gaat, en hoe het binnen...

Cor Blom  
Nou, Webroom Booking zet er geen cursus in. 

### ~ 40 min

Reijer van der Zande  
Nee. Nee, precies. Dus dat is dus eventjes de key mapping van de verschillende... 

Cor Blom  
Ja, exact. 

Reijer van der Zande  
Dat is dat, maar dat is een heel technisch stukje, dus dat moet denk ik even ergens een keertje...
Ja. 

Mirjam Veenstra  
Ik weet niet, wat is de mail? 

Reijer van der Zande  
Eh, eh, r.c.van.der.Zande@st.hanze.nl. Eh, Reijer van der Zande  . Ja. R.c.van.der.Zande, student. Ja, ja. Er is ook een Renger, ook niet? Dat is een voetbaltrainer. Raaier. Nee. Raaier. Reijer van der Zande  .
Ja. 

Jos Ensing  
Ik vond deze ook wel. Renger van der Zander. Dat zou heel goed kunnen, ja. Ja. Renger is, eh, komt ook op de naam, mijn naam komt van de Veluwe. Eh, en die komt daar ook veel voor. Ja. Dus dat is een hele, allebei een hele oude naam.
Ik denk dat de vroegste referentie in mijn familie waar deze naam gebruikt is, is 1680. 

### ~ 41 min

Jos Ensing  
Oké. Weet je. Dat was net na de slag bij Nieuwpoort. Haha. Nee, dat is 1880 volgens mij. Of 1600. 

Reijer van der Zande  
1672 was het rampenjaar. Toen kwam Bomme Berend aan Groningen.
Oh ja, mooi. 

Mirjam Veenstra  
Je hebt hem op de mail. Ik heb jou meegenomen in de cc. Helemaal goed. Dus dan heb je ook gelijk onze mailadres. Ja, heel fijn. Ja, tof. Volgens mij kun je dan eerst uitvoeten zo, toch? Ja. 

Reijer van der Zande  
Ik kan in ieder geval aan gaan schrijven, dingen opzetten, plannetjes maken. Dan gaan we vast contact hebben voor additionele informatie, want daar komen vast nog wel vragen uit. Ja, en we kunnen ook altijd even een online meeting inplannen. Dan kun je het zo overleggen. Ja, dan kun je ook op maandag hier ergens gaan zitten als je wil. 

### ~ 42 min

Reijer van der Zande  
Ik woon hier letterlijk achter. In de Johannes Mulderstraat. Ik woon hier om de hoek. 

Cor Blom  
Ja, Bomme heeft geen hand, dat zie ik hier nooit. Nee, dat is prima. Dat is absoluut hoor. Kijk, als je hier een werkplek kan vinden en gewoon dicht bij Jos of wat dan ook.

Reijer van der Zande  
Nou, dat is niet altijd misschien, maar voor een middag of een keer kan dat heel handig zijn. Dat is even helemaal goed. Top. 
Mirjam Veenstra  
Ja, nou mooi. Best enthousiast. Doe je best. Ja, ik ga zeker mijn best doen. Ik hoop dat jij ook een beetje enthousiast wordt van deze opdracht. Ik dacht dat je dacht, yes, die kan ik wel neer. Help, dit wordt heel groot, maar... Beide. 

Reijer van der Zande  
Ja, het is concreet en het is klein. En aan de andere kant zit er ook legio en opties in om het heel groot en complex te maken. Nou, en de kunst is om klein te beginnen en het dan uit te kunnen bouwen.

Jos Ensing  
Je loopt natuurlijk wel tegen een bepaalde flexibiliteit van de organisatie aan. Ja. Waakrijk heeft wel toegang. Ja. 

Mirjam Veenstra  
Daar lopen wij ook wel eens tegenaan, hè? Ja, zeker. Ja. 

Cor Blom  
Ik hoop dat hij een medewerker kan krijgen, maar ik denk niet dat dat gaat lukken in feite.
