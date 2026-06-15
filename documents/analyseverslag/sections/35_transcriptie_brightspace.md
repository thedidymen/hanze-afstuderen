# Transcriptie interview – Brightspace

## Transcriptieproces

Voor het uitwerken van de interviews is gebruikgemaakt van de transcribe tool van teams dat automatisch spraak omzet naar tekst.

De gegenereerde tekst is daarna opgeslagen in een tekstbestand en handmatig gecontroleerd en waar nodig gecorrigeerd op fouten in interpunctie, naamgeving en herkenning van gesproken woorden. 

## Algemene Informatie

| | |
|---|---|
| Datum | 1 juni 2026 |
| Tijd | 15.00u - 15.30u |
| Locatie | Hanze Hogeschool, Zernikeplein 11 |
| Doel gesprek | Stakeholdergesprek Brightspace voor Sign-Up Tool |

| Aanwezigen | Rol |
|---|---|
| Maurits Hoogerwerf | Brightspace | 
| Reijer van der Zande | Developer |

## Transcriptie


### ~ 0 Min

Maurits Hoogerwerf 0:15  
Daar ben ik weer.

Reijer van der Zande 0:15  
Top dankjewel voor dit gesprek.

Maurits Hoogerwerf 0:19  
Ja.

Reijer van der Zande 0:21  
Heb jij enig idee waar het over gaat of moet ik hem even?

Maurits Hoogerwerf 0:24  
Je je gaf iets aan van. Je hebt een project.

Reijer van der Zande 0:28  
Ja.

Maurits Hoogerwerf 0:30  
Ja, vertel maar.

Reijer van der Zande 0:31  
Ik mag binnen binnen een colleps Space bij Cor Blom ben ik aan het afstuderen momenteel het idee is om voor.In de In de eerste instantie vanuit verpleegkunde een sign off tool te maken. Die tool is bedoeld voor studenten, zodat ze zich kunnen inschrijven voor praktijkmomenten.Er gebeurt momenteel zo dat docenten krijgen een aantal uren toegewezen vanuit web room vanuit de organisatie. En daarin moeten ze een x aantal studenten. Moeten ze praktijkexamens in geven? Nou, dat gebeurt vaak in groepen soms individueel. Soms zitten twee. Gebruikers voor assessments nou verschillende dingetjes en ze hebben momenteel gebruiken ze bepaalde groepsfunctionaliteit binnen brightspace om dat voor zichzelf te kunnen faciliteren. En zij hadden zoiets van ja, vroeger hadden we een blackboard, hadden we een soort van rond tool, die werkte niet meer. Is het mogelijk om weer zoiets te krijgen? Mijn opdracht is om te kijken of dat kan. En als dat kan om daar iets voor te schrijven of om dat te maken.

### ~ 1 Min

Maurits Hoogerwerf 1:39  
Even even terug naar naar in blackboard hadden we een synd tool, zei je.

Reijer van der Zande 1:43  
Ja, Ik weet niet meer hoe het nou precies heette. Ze hadden een module vanuit de rug en die gebruikten ze om. Nou studenten over een tijdklok te kunnen verdelen met.

Maurits Hoogerwerf 1:56  
Ja de advancegroep tool.

Reijer van der Zande 1:58  
Nou, kijk.

### ~ 2 Min

Maurits Hoogerwerf 2:00  
Ja.

Reijer van der Zande 2:01  
Maar met de brightspace bestaat hij niet meer. En de normale brightspace functionaliteit zover Ik weet, biedt daar geen opties voor.

Maurits Hoogerwerf 2:12  
Ja, Dat is een goeie je, zei je bericht van jij weet alles van brightspace. Nou, brightspace hebben we Natuurlijk nu net vanaf september in in productie of in ieder geval. We hadden hem al eerder in productie, Alleen is ze hebben echt live gegaan daarmee. Dus Ik weet nog niet alles, Maar ik weet wel waar ik de informatie kan vinden.

Reijer van der Zande 2:30  
Ik, kijk nou, Ik was in ieder geval door Cor doorverwezen van. Nou, Je moet maar weer eens even hebben. Die weten in ieder geval binnen de Organisatie echt superveel van die kan je in ieder geval iets mee helpen kijken. Wat kan nou?

Maurits Hoogerwerf 2:31  
Dus ja.

Reijer van der Zande 2:42  
Ik denk ik schiet er mijn fan dus top dat dat zo even kon.

Maurits Hoogerwerf 2:44  
Ja. Helemaal goed.

### ~ 3 Min

Reijer van der Zande 2:50  
Ja, Ik heb dus eigenlijk de de de de. Het gaat voornamelijk om het vervangen van die tool.
Daarnaast lopen er een paar andere dingen als in. Ze willen graag kijken of ze studenten kunnen inzetten voor nou, het maken van dit soort niet primaire vast tools, maar secundaire tools die het leven een stuk makkelijker maken, maar niet mis je kritisch zijn. Ze willen kijken of ze daar onder andere ook studenten voor in kunnen zetten, dus Dat is eigenlijk deel twee van mijn opdracht. Nou dat van daaruit dat deze opdracht naar voren is gekomen. En vanuit verpleegkunde hebben ze een vrij generieke vraag en het idee is ook om te kijken of we dat eventueel voor alle instituten beschikbaar kunnen krijgen. Het is wel het doel om de tool ook generiek te maken als nou met de kanttekening dat het als er iets is, ja, dan gaan we niet iets schrijven zelf schrijven. Maar ze we neigen momenteel naar een maatwerk oplossing.

Maurits Hoogerwerf 3:51  
OK en Dat is ook, dat valt ook wel onder het nieuwe beleid, Omdat we mogen eigenlijk niet meer zelf ontwikkelen. En nou ja, dus dat willen ze zoveel mogelijk niet. Ja nou ja zo Maar dat ja nou ja, goed dan ja.

### ~ 4 Min

Reijer van der Zande 4:06  
Ja. Ik ben al bij Arno de Boer geweest, de business architect en die zit inderdaad nu met een met deze pilot te kijken of daar Misschien iets meer ruimte is om te kijken of daar wel wat kan en hoe dat dan zou moeten vormgeven. Een deel van de opdracht is ook om te kijken waar loop je tegenaan, wat zijn de hordes waar je doorheen moet? Kunnen we dat pareren of niet, dus het.

Maurits Hoogerwerf 4:11  
Ja ja.

Reijer van der Zande 4:29  
Is ook gewoon een experiment, een een use case om te kijken van nou, wat kan wel? Wat kan niet. Wat zijn de problemen? Dus daar wordt dit ook voor gebruikt.

Maurits Hoogerwerf 4:38  
Ja nou helemaal goed. Het is, We hadden vroeger naar blackboard. Natuurlijk hadden wij de mogelijkheid om een building blok te bouwen. Building block Dat was een bepaald bestand waarmee je rechtstreeks gebruik wil maken, eigenlijk van Van de API van Van van Blackboard. En dat zit in brightspace, zit dat niet? Brightspace heeft wel een API. En. Ik had een oud applicatie kan Ik kan ik aanmaken scope instellen waarmee je dus tot bepaalde. Nou ja, heb jij een punt of met bepaalde IM points kunt kunt communiceren of praten? Dat kan nou ja, jouw eerste vraag is Natuurlijk van, wat is er nu al mogelijk? Nu weet ik dat brightspace heel druk bezig is met het ontwikkelen of het doorontwikkelen van de Group Tool. Dus er zit een zit een tool in in brightspace waar waarschijnlijk dacht ik. Mensen wel via self applement zelf kunnen inschrijven in een in een groep. Alleen, Ik weet uiteindelijk nog niet. Eerste vraag. Is het de bedoeling dat ze er groepen komen, dus Als het 1 tweetje is, is dat dan met de begeleider en een en een student en is het dan de bedoeling dat ze? Nou ja. Dat ze met twee met zijn tweeën in een groep komen, dus met een met een examinator en en de studenten op. Is het de bedoeling dat nou ja, dat ze uitwijken naar een ander platform. En daar met elkaar in gesprek kunnen.

### ~ 6 Min

Reijer van der Zande 6:32  
Nee OK, Het is. Het idee is dat ze nou stel. Er is een praktijkexamen in een lokaal. We gaan dat bijvoorbeeld in drietallen doen. Ze willen graag een een inschrijfflijst op brightspace hebben waarin leerlingen zich op in kunnen schrijven als groepje zijnde.

Maurits Hoogerwerf 6:52  
Ja.

Reijer van der Zande 6:54  
En dan hebben ze een bepaald tijdslot en dan worden vervolgens binnen dat tijdslot wordt in dat lokaal de examens fysiek afgenomen.

### ~ 7 Min

Maurits Hoogerwerf 7:01  
OK.

Reijer van der Zande 7:03  
En waar ze nu tegenaan lopen, is dat ze dat niet helemaal netjes kunnen doen. Ze hebben daar een aantal dingen die ze er graag bij zouden willen hebben, zoals.
Ik wil graag een tijdslot vrij kunnen plannen zodat ik ook pauze heb Als ik 8 uur lang daar in het lokaal zit, moet ik ergens tussendoor een pauze kunnen inplannen. Daarnaast gaat het ook om bijvoorbeeld om herkansingen en ze zouden dus heel graag willen dat de een tijdslot wel beschikbaar is om op in te schrijven, Maar dat je niet kunt zien op welke tijdslotten andere Mensen hebben ingeschreven, zodat je een stukje privacy nou op het moment dat je daar bij een herkansing lijst staat, is het automatisch duidelijk dat je een herkansing moet doen. Nou, dat willen ze kijken of ze daar iets in kunnen betekenen. En daarnaast hoeft een docent. Volgens mij zit een docent primair dit op. De regisseur zet het momenteel klaar. Maar een docent, alle docenten, regisseurs zouden in principe. In ieder geval binnen het instituut of binnen die afdeling al de informatie mogen zien van alle leerlingen. Want dat mogen ze nu volgens mij ook Als het goed is. Maar het is dus wel het idee dat leerlingen inderdaad niet van elkaar kunnen zien wanneer ze zich hebben ingeschreven. Momenteel valt jouw audio weg?

### ~ 8 Min

Maurits Hoogerwerf 8:27  
Nu weer.

Reijer van der Zande 8:28  
Ja.

Maurits Hoogerwerf 8:28  
Ja OK top. Oké, en dus Het is eigenlijk een combinatie van webroom Booking roostering. En een systeem als ambts, bijvoorbeeld digitale toetsapplicatie of of niet.

Reijer van der Zande 8:44  
Nee ans hoeft in principe niet, want het examen zelf gebeurt in principe gewoon fysiek. En het het enige wat we, We hebben het wel even doorgehad van. Nou, weet je, het zou heel fijn zijn als bijvoorbeeld de tool wel een een eyedr kunnen maken van de lijst met Mensen. Dat zou, Maar dat zou een hele hele fijne Nice to have hebben, maar Er is niet randvoorwaardelijk.

Maurits Hoogerwerf 8:51  
Top. Ja. Nee dus nou ja, de tool wordt voor een beeldvorming wordt dan wordt er gebouwd, dus Het is een combinatie van roostering en webomboeking, dus een ruimte en rooster een gedeelte dus Dat is nou. Dat valt Natuurlijk buiten buiten brightspace. En dan wil je eigenlijk een i framme hebben in een course of zo waar, waarop de studenten of waardoor die studenten naar die tool kunnen kunnen gaan, dus daar zit ik al te. Denken aan een. LTI implementatie ofzo.

### ~ 9 Min

Reijer van der Zande 9:36  
Een LTI dat zegt bij dat zegt bij zijn niks.

Maurits Hoogerwerf 9:40  
Nee dus. OK, nee, Laten we daar niet naartoe gaan. Ja of toch wel, ik zal je even meenemen. Deel even mijn scherm.

Reijer van der Zande 9:55  
Ja.

Maurits Hoogerwerf 9:58  
We hebben hier brightspace. Nou ja, je kent brightspace, je werkt er zelf ook in.

### ~ 10 Min

Reijer van der Zande 10:02  
Ja, Ik heb inderdaad het een half jaar het genoegen gehad om daarin te mogen werken.

Maurits Hoogerwerf 10:07  
Ja OK. Nou, hoe kunnen wij applicaties? Naar binnen halen. We. Kunnen wat ik net zei, via LTA kunnen we een externe applicatie naar binnen halen. En wat houdt een LTI in eigenlijk? Dat is een een externe tool. Waarbij we aan de hand van een een IT target link URL en een keyset een een vertrouwde of een SSO creëren met met met de tool. Dus dan weet je van, hé, welke welke student, met welke student heb ik de heb ik te maken, dat zou je anoniem kunnen doen, dus Alleen maar met het Ordiffiend ID. Dus Dat is een idee. Die is Alleen bekend bij. De Hanze. Die gelinkt is aan een aan een student. Of door e mailadres, voornaam achternaam bijvoorbeeld op te halen. Dus dan kun je vanuit een cash de student die ingelogd is. Die kan een sessie starten met die eye frame via LTI naar die applicatie. En dan weet de applicatie met wie die te maken heeft, dus dan kun je je eigen dashboardje maken, bijvoorbeeld voor voor de student waarin die dus blokjes ziet. Zoals ik me dan voorziet van nou hé, dit dit tijdslot dus is avelable.

### ~ 11 Min

Reijer van der Zande 11:21  
Ja.

Maurits Hoogerwerf 11:33  
En oh, die is grijs, dus daar kan ik niet meer op op inboeken, Omdat daar een andere student op ingeschreven heeft. Dus Dat is LTILTI admantage en LT 1.3 is het protocol dan wat er wat er gebruikt wordt. En dan hebben wij bijvoorbeeld, Maar dat is meer Als je met de achterkant van Van brightspace wil praten. Brights base heeft een API en Dat is in D 6 dat niet belangrijk. Dan zou ik een off applicatie aan kunnen maken waarmee je dus toegang krijgt tot tot de achterkant van Van brightspace. Dus dan heb je API Endpoints waar je bijvoorbeeld cijfers op kunt halen of gegevens op kan. Van. Van de Van de studenten Alleen Ik denk dat het in bij deze casus minder aan de orde is. Wat jij wilt is echt dat een een docent na een koorts kan gaan, dus zij van mij zenbooks course. En. Onderaan ze een minuutje? Examen bijvoorbeeld toevoegt als als unit en dat hij dan kan zeggen van nou er ten existing plug in. Dat zou dan in deze zijn. Nou, ik zeg nu mentimeter. Maar dat zou dan exem schedule zijn of zoiets iets iets dergelijks dus die klikt daarop en dan wordt er gewoon een.

Reijer van der Zande 12:58  
Ja ja ja ja ja.

### ~ 13 Min

Maurits Hoogerwerf 13:04  
Nou, ik doe even mentimeter. Die doet niks Natuurlijk, of wel? Ja. Deze gaat dan naar mentimeter toe, dus Dat is een applicatie buiten buiten de Hanze en die zet hem erin. Als content. En dan krijg je een? H Fine. Klopt dat. Gaat u doen? Oh, daar zitten we nog niet in Sim capsure. Ik weet iets hebben wat echt? Een ISVMS. Als Misschien bij paspoort? Ja. Nu gaat hij, dus doet hij LTI authenticatie en dan heb dan heb je hier. Zo heb je dan de applicatie die gebouwd is, dus je bouwt een applicatie en wat je er eigenlijk omheen bouwt is 1 is 1 LTI schil waardoor je een een handshake doet en waardoor je een versleutelde sessie krijgt met met een met een keeper. Dat is denk ik de idee of.

Reijer van der Zande 13:53  
Ja, ik zag het.

### ~ 14 Min

Maurits Hoogerwerf 14:17  
Als je Als je dat echt in White Space wil, hebben de manier om het. Om het te implementeren in het in het LMS.

Reijer van der Zande 14:27  
Ja dit sluit heel erg aan bij wat inderdaad voor maatwerk een goede oplossing zou zijn volgens mij. Ja.

Maurits Hoogerwerf 14:35  
Ja.

Reijer van der Zande 14:37  
OK Wauw.

Maurits Hoogerwerf 14:41  
Waar vind je informatie over LTI? Het development. En daar heb je, hoe heet dat ook alweer? Ja ette? Nee, tuurlijk niet. Daar kon het niet zo 1 2 3 vinden, Maar het is een. Het is een standaard wat je gewoon online kunt vinden en Als je een development applicatie maakt, dan doe je dat in Flash FLASK. En Als je LTI applicatie in productie wilt draaien dan gebruik je unicorn.

### ~ 15 Min

Reijer van der Zande 15:37  
OK. Dus dat ligt ook al de dat die stack ligt alvast. Ja unicorn ken ik trouwens, dat gebruiken we ook beter ook.

Maurits Hoogerwerf 15:45  
Ja. Ja.

Reijer van der Zande 15:49  
Maar gebruiken we daar een variant van maar. OK. En In de def is het dan flask?

### ~ 16 Min

Maurits Hoogerwerf 16:02  
Kijken. Volgens mij geef ik verkeerde evaluatie. Ik zoek het nog even na. Ja blascus in ieder geval, dat klopt wel. Ja even kijken unicorn, heb je? In persbox is even niet aan de aan de orde. Ja flass is het en unicorn inderdaad. Als.

### ~ 17 Min

Reijer van der Zande 17:10  
OK.

Maurits Hoogerwerf 17:12  
Ja.

Reijer van der Zande 17:16  
Nou, Dat is al hele, heel veel de re informatie waar ik wat mee kan, dus Dat is al heel fijn.

Maurits Hoogerwerf 17:20  
OK. Ja.

Reijer van der Zande 17:24  
Jij weet toevallig niet wat die die doorontwikkeling van die Group Tool. Waar hoe dat eruit gaat zien?

Maurits Hoogerwerf 17:33  
Nou die die groep Tool. Dat was echt puur en Alleen voor groepen in blackboard, dus je had een. Het, het maakte de docent makkelijker om even snel 20 groepen aan te maken met met een bepaalde naam, dus groep één tot en met groep 20. En daarbij kon die dan aanvinken van mogen de studenten jezelf op inschrijven of wil je dat dat ik In de course zoek naar alle studenten en ze automatisch indeel? Dus kon je zelf een rooms aan aanzetten. Automatisch indelen kon je aanzetten en je kon. Achteraf kon je de groepsnamen nog aanpassen of in een groep de groep nog splitten in twee groepjes? Dat Dat was de Advance Goodwill en Ik denk niet dat dat dat de applicaties die jij bedoelde wat in wat in blackboard zat en Ik weet niet wat je wat je wel bedoelt.

### ~ 18 Min

Reijer van der Zande 18:18  
Nee.

Maurits Hoogerwerf 18:21  
Ja Misschien exem schedule Alleen ik. Daar gaat verder geen lampje branden bij mij van. Wat dat dan?

Reijer van der Zande 18:30  
Nee, Ik weet dat het een module was die ze op de rug ontwikkeld hebben en die de Hanze daarvoor ook gebruikte. Maar ook die tool was iets wat soort van werkte, maar ook niet volledig aansloot bij de wensen. Het was meer van OK, Dit is Dit is 1 1 1 manier waarop het gedaan kunnen krijgen, Maar dat ook Dat was niet ideaal wat ik begrepen had. Dus OK helemaal goe.

Maurits Hoogerwerf 18:30  
Pas. OK. Ja. Nee. OK.

Reijer van der Zande 18:58  
Even denken hoor ik vroeg me af. Want ik doe het momenteel dit Alleen op maandag. Nou valt ik zei vanwege mijn betaalde baan In de rest van de week.

### ~ 19 Min

Maurits Hoogerwerf 19:08  
Ja.

Reijer van der Zande 19:09  
En daarmee loop ik ook een stukje uit. Normaal gesproken zou ik vandaag klaar moeten zijn, Maar het gaat een stukje langer duren. Zou het mogelijk zijn om binnen brightspace een een dummy course te kunnen krijgen? Waarmee ik bijvoorbeeld over de zomer heen wat ontwikkelwerk kan doen om te kijken of dit in ieder geval proof of concept kan gaan werken. En dan kunnen we na de zomer Misschien wel kijken hoe dat dan echt overal moet gaan doen. Maar dan kan ik in ieder geval deze zomer doorwerken.

Maurits Hoogerwerf 19:41  
Ja OK. En, wil je dan, want de dummy course dat dat dat kan Alleen, hoe krijg je die applicatie er dan in? Want zo'n LTI configureren aan de achterkant? Dat mag Alleen een super Administration en and brightspace, dus dan zou je eigenlijk al een werkende applicatie moeten hebben die klaar is om te verbinden met een met een LMS via LTI.

Reijer van der Zande 19:57  
Ja. OK dan is dat niet zinnig om dat voor deze zomer te gaan doen, denk ik.

### ~ 20 Min

Maurits Hoogerwerf 20:09  
Nee.

Reijer van der Zande 20:11  
Heel goed. Oké. Jemig, Ik ben even zoekende of ik dan nog iets anders moet hebben of niet, of dat dat of dat ik eigenlijk al heel veel Ik heb. Ik heb al heel veel informatie gekregen, dat scheelt al, want Ik was inderdaad heel erg zoekende naar hoe ga ik dit in in brightspace iets mee kunnen doen?

Maurits Hoogerwerf 20:35  
Ja.

Reijer van der Zande 20:36  
En dit klinkt inderdaad als een hele valide oplossing.

Maurits Hoogerwerf 20:39  
Ja.

Reijer van der Zande 20:41  
Weet jij toevallig nog van andere plug ins mogelijkheden die. Brightspace zou hebben die hierbij aansluiten. Nee OK.

Maurits Hoogerwerf 20:52  
Nee, nee, nee, dus echt een. Ja, ik zag wel heel hard, nee, Maar ik neem de vraag even mee, dan ga ik er morgen nog even stellen en dan. Reageer ik daar nog wel even op, dus zijn. Andere. Scheduling plugin stand, hè?

### ~ 21 Min

Reijer van der Zande 21:14  
Ja, Ik denk dat dat inderdaad het dichtstbij komt bij het generieke doel.

Maurits Hoogerwerf 21:19  
Ja. Zo helemaal analoog met een pen. OK die vraag die stel ik morgen nog even binnen ons team en het antwoord blijf, blijf ik jou even verschuldigd.

Reijer van der Zande 21:32  
Top. Ja Assen heel fijn.

Maurits Hoogerwerf 21:41  
Ja.

Reijer van der Zande 21:43  
Ja ik, Ik denk dat ik in eerste instantie inderdaad de informatie hieruit heb. Wat ik wat ik verhogen had is heel fijn. Dankjewel.

Maurits Hoogerwerf 21:52  
Graag gedaan.

Reijer van der Zande 21:54  
Ik mocht ik zover zijn dat ik inderdaad iets heb wat er ingehaakt kan worden, kan ik weer contact opnemen. Mag ik weer contact opnemen?

### ~ 22 Min

Maurits Hoogerwerf 22:02  
Ja, dat kan Alleen. Er ligt aan hoe snel, want Ik heb één september. Heb ik een andere baan.

Reijer van der Zande 22:09  
Ah, wat leuk.

Maurits Hoogerwerf 22:10  
Ja dus.

Reijer van der Zande 22:12  
Tof wat ga je doen?

Maurits Hoogerwerf 22:14  
Ik ga ja, Ik ga voor de overheid werken binnen binnen Groningen. Ja, ja dus.

Reijer van der Zande 22:18  
Kijk leuk.
Nou gefeliciteerd en in ieder geval heel veel succes en plezier daarbij, want dat lijkt me inderdaad een hele andere omgeving nou een hele andere. Ja, Het is een andere omgeving als wij hier nu zit, denk ik dus cool.

Maurits Hoogerwerf 22:23  
Dankjewel. Dankjewel. Ja dat klopt ja. Dus, maar goed. Ons team Dat is team team icto die is bereikbaar. Dat hebben we een chat hier ja. En zitten knappe kop, hoor. HSBSBS at hoog.hans.nl.

Reijer van der Zande 22:58  
Kijk tof.

### ~ 23 Min

Maurits Hoogerwerf 23:01  
Die kun je benaderen op dit e mailadres.

Reijer van der Zande 23:03  
Ja, gaan we dat doen? Dan kun je wel vast in een documentje zetten zo. Top. Had jij nog iets toe te voegen of had jij zoiets van nou voorbij zijn we.

Maurits Hoogerwerf 23:18  
Volgens mij zijn we rond en als er iets in ieder geval het antwoord, krijg je nog van mij of of de eventueel nog andere plug ins zijn. En Als we er iets te binnen schiet dan dan schiet ik wel even een berichtje en op als reactie op jouw bericht van vanmorgen.

Reijer van der Zande 23:36  
Ja helemaal goed. Top nou dan heel erg bedankt. Heel veel succes en fijne vakantie.

Maurits Hoogerwerf 23:37  
Ja. Dankjewel jij ook? Jij ook? Joe Hoi.

Reijer van der Zande 23:44  
OK hé dankjewel hoi hoi.