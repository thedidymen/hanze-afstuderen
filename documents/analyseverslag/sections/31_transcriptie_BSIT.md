# Transcriptie interview – BS&IT

## Transcriptieproces

Voor het uitwerken van de interviews is gebruikgemaakt van een Python-script dat automatisch spraak omzet naar tekst. Hierbij is het audiobestand ingelezen met de Python-library `speech_recognition`. Vervolgens is via de Google Speech Recognition API een Nederlandse transcriptie (`nl-NL`) gegenereerd.

De gegenereerde tekst is daarna opgeslagen in een tekstbestand en handmatig gecontroleerd en waar nodig gecorrigeerd op fouten in interpunctie, naamgeving en herkenning van gesproken woorden. 

## Algemene Informatie

| | |
|---|---|
| Datum | 2 maart 2026 |
| Tijd | 13.30u - 14.00u |
| Locatie | Hanze Hogeschool, Zernikeplein 11 |
| Doel gesprek | Stakeholdergesprek BS&IT voor Sign-Up Tool |

| Aanwezigen | Rol |
|---|---|
| Arno de Boer | Business Architect |
| Cor Blom | Projectleider Collabspace |
| Reijer van der Zande | Developer |

## Transcriptie


### ~ 0 Min

Reijer van der Zande  
Ja, ik ga wat voor jullie doen. Is plan. Volgens mij was dit in ieder geval het stukje voor onderzoekskaders.

Arno de Boer  
De architectuurkade of de architectuurkade zat binnen dat onderzoek.

Cor Blom  
Ja, dat wordt hier zelf gebouwd. Dat doen we nog niet echt. Wat komt er dan bij kijken?

Arno de Boer  
Ik kan straks ook nog wel even de nieuwe architectuurkade software
ontwikkelen. Vanuit ons bedrijfsvoeringsperspectief. Die gaat morgen naar het MT. Dus die is ook wel even goed voor jullie om te weten. Die ga ik zo wel even toelichten. Dus misschien is dat goed. Als die vastgesteld is, wil ik hem wel met je delen. Want dan komt hij gewoon in het openbaar.

Reijer van der Zande  
Ja, dan mag ik hem ook inzien.

Arno de Boer  
Er zit nog één discussiepuntje denk ik in. Maar dat gaan we straks...

Cor Blom  
Collab space?

Arno de Boer  
Nee, dat niet zozeer. Maar wel hoe organiseren we het.

### ~ 1 Min

Cor Blom  
Ja, ja.

Arno de Boer  
Dat is de grootste discussie. Alle andere dingen komen wel uit. En dus alle inhoudelijke kant van: Wat doe je waar? Wanneer doe je het wel en wanneer niet? Dat is wel redelijk te overzien.Maar ik denk vooral van: Hoe ga je dat centraal beheren en organiseren? Dus dat is eigenlijk het.Ik vraag wel weer.

Reijer van der Zande  
Nee, dat is juist de bedoeling toch? Ja, ik probeer een beetje uit te zoeken wat dan inderdaad daarvoor nodig is.  is en wat van jullie daar ook de vraag voor is. Dus ik ben een beetje ook zelf nog zoekende.

Cor Blom  
Ja, voor de beeldformulier, de opdracht bestaat inderdaad uit twee dingen: de ontwikkeling van de sign-up booking tool voor verpleegkunde dan wel, voor een brightspace en dat is ook de focus. Dat is ook je hoofdonderzoek, je hoofdding waar je op bezig gaat. Maar daarnaast zijn we inderdaad vanuit BS&IT, wat komt er dan bij kijken?

### ~ 2 Min

Cor: Stel we ontwikkelen en dan vooral vanuit jou, vanuit het perspectief van de bouwer, waar loop je tegenaan met keuzes en met inrichting etcetera en waar soort van input als het ware wat weer gebruikt wordt door Arno en de andere architecten. Om te kijken van: hoe gaan we dan daadwerkelijk zelf ontwikkelcapaciteit hier realiseren en waar moeten we dan rekening mee houden?

Arno de Boer  
Ja, en met daarbij ook eigenlijk als een van mijn kaders is dat we samenwerken met...

Cor Blom  
Ja, met... De collabspace.

Arno de Boer  
Ja, met de collabspace.

Reijer van der Zande  
 Ja.
Arno Ik kan me voorstellen dat jij gaat bezig zijn met het Sign-Up Tool. En dan komen er vragenstukken op af. Oké, ik heb het straks klaar. Wie gaat het nou beheren?

Reijer van der Zande  
 Ja, dat is inderdaad een van de vragen die ik nu ook al heb. Hoe gaan we de overdracht doen? Hoe gaan we zorgen dat dingen geborgd gaan worden?

### ~ 3 Min

Arno de Boer  
Dat is precies ook een beetje het vraagstuk waar wij binnen de hand
tegenaan lopen. En ik zou me ook voor kunnen stellen dat jij, als je daarmee bezig bent,ook concreet ergens tegenaan loopt. En dat je dan zegt: Oké, nu heb ik een antwoord nodig op een vraag die ik niet krijg. En dat is precies, dan hebben wij namelijk ergens iets te regelen als
BSI.

Cor Blom  
Ja.

Arno de Boer  
En dat is eigenlijk ook een beetje de crux van deze casus. Dus we gaan aan de slag en we lopen ergens tegenaan. En waar lopen we dan tegenaan? En dat kan te maken hebben met continuïteit. Maar het kan ook te maken hebben met bijvoorbeeld hoe beleggen we het functioneel beheer van zo'n stukje of tooling.

Cor Blom  
Ja.

Arno de Boer  
Wie gaat dat beheren? Ja, want dit is dan voor verpleegkunde. Maar is dat dan alleen voor verpleegkunde of komt er misschien ook een andere opleidings...

Reijer van der Zande  
Het idee was wel om inderdaad het stukje software breed te schrijven. Ook vanuit het oogpunt dat dat vanuit de, nou, bezig, de hele Hanze inzetbaar kan worden.

### ~ 4 Min

Arno de Boer  
Dus eigenlijk wat, zoals ik het nu zie, is van draai hem om, ga ermee aan de slag en bedenk de vragen die je zou hebben als je dus dat, stel dat het operationeel draait. Wat komt er dan bij kijken? En waar moeten we dan rekening mee houden? En dat is een beetje de uitdaging die jij dan als student mag hebben van oké, oké nu draait het dan, wat kan er allemaal misgaan? Eigenlijk is dat een vraag, wat kan er allemaal misgaan? Dat kan zijn dat hij niet meer doet, maar het kan ook zijn dat hij bijvoorbeeld niet meer actueel genoeg is. Dus dat de functionaliteit doorontwikkeld moet worden omdat gewoon het proces is veranderd bijvoorbeeld. Of het kan zijn, nou ja zo, nou ja en dan kom je uiteindelijk dan bijvoorbeeld bij functioneel beheer uit. Nou functioneel beheer moet dan bepaalde dingen doen met dat tool, oké maar hoe zit, en wie is dan de leverancier waar de functioneel beheer op kan bouwen? Is dat de, is dat Reijer die inmiddels vertrokken is?
Dan gaan we naar Cor, Cor jij met jouw.
Cor zei nee, nee, nee.

Cor Blom  
Nee precies. Nee, precies. Nee, nee. Nee, inderdaad ja. Ja.

### ~ 5 Min

Arno de Boer  
Dus ik denk dat dat een beetje de kern zal zijn van, hè dus bedenk vooral van wat kan misgaan? En wat betekent dat dan? Wat wij hier intern moeten doen om, en dit Sign-Up Tool is ook, ook meteen een hele mooie omdat het ook best wel redelijk strategisch is. Dat wordt echt in het onderwijs ingezet. Dus als we het straks operationeel hebben...

Cor Blom  
Ja, je kan het er niet zomaar weer uittrekken.

Reijer van der Zande  
Nee, want mensen zijn er afhankelijk van. Er gaat een stukje een behoefte vervullen die niet zomaar weer... Er moet op een of andere manier opgelost worden als dat niet... Ja.

Arno de Boer  
En daar hebben we bewust van aan. Kijk, wat ik ook meteen zeg is van: Dit stukje, die Sign-Up Tool, daarvan kan ik me ook benenemen van: Ja, is er... En we hebben ook wel gezegd: Is daar niet iets voor in de markt bijvoorbeeld? Dus dat is ook meteen... Nou, dat soort vraagstukken ook. Dat zijn ook een van de architectuurkades. Die laat ik zo even zien. Het zijn er elf. Ik wilde er tien.

### ~ 6 Min

Cor Blom  
Jammer.

Arno de Boer  
Jammer. Het minst belangrijke. Organisatie en wat dan ook. Dus het is inderdaad... En nou ja, dus die opdracht die je hebt, hoe verder past die dan in de kaders? Of zou je adviseren? Dus wat dat betreft gaat het meer om van: Oké, wat kan er misgaan inderdaad? Hoe verhoudt zich dat tot die kaders die we nu stellen? Dus het is gewoon echt een proefpudding of zo. Proeven. Kijken waar we tegenaan lopen. En wat ik ook wel zie is standaarden. Van technische standaarden. Welke technische standaarden gaan we gebruiken. Stel dat je kiept het bij ons over de schutting en hier hebben jullie een prachtig tool. Ja, we hebben daar een Oracle database voor nodig, of weet ik veel wat,
voor de exotische apparatuur.

### ~ 7 Min

Reijer van der Zande  
Ik zit inderdaad wel met een vraagje van wat is het landschap waarbinnen jullie werken? Want ik denk dat het het makkelijkst wordt als het aansluit bij wat jullie al doen. Want anders moet je daar weer een nieuwe techstack kennis voor opbouwen. Dat lijkt mij niet handig.

Arno de Boer  
En dan kom je meteen naar de volgende discussie. Dus dan zeggen we van, oké, Meest Logo's is dan bijvoorbeeld een power platform. En daar aan geallieerde, ik weet niet welke ontwikkeltalen geallieerd zijn aan... Pas zijn alle ontwikkeltalen op Microsoft?

Cor Blom  
Nee, dat is echt low-code. Dat zou ik denk ik niet helemaal volstaan. Dat denk ik ook voor dit. Je hebt het zelf, voor de duidelijkheid, hij is een senior ontwikkelaar eigenlijk.

Reijer van der Zande  
Oh, nee, nee, nee, ik ben geen senior ontwikkelaar. Maar ik werk ook wel in het...

Cor Blom  
Het is geen student ontwikkelaar in die zin.

Arno de Boer  
Ik weet niet welke ontwikkeltalen... Wat ik me voor kan stellen is dat je een moderne ontwikkeltal hebt die redelijk platform onafhankelijk is.

### ~ 8 Min

Cor Blom  
Ja, een beetje universeel.

Arno de Boer  
Universeel, waarbij je ook zegt van... Dus dan mag je wat mij betreft... zelf ook al die redelijk platform onafhankelijk is. Dus daar mag je wat mij betreft zelf ook over nadenken. Wij adviseren, jullie hebben een Microsoft landschap, maar jullie hebben, wat bijvoorbeeld speelt, is die soevereiniteitsdiscussie.

Reijer van der Zande  
Mag je mij, ik denk dat ik weet waar het heen gaat. 

Arno de Boer  
Microsoft is Big Tech. En we zijn natuurlijk voor Microsoft een prachtig product, maar tegelijkertijd roept het ook veel afhankelijkheidsdiscussies op. Dus elke functionaliteit die we gaan bouwen in een Power Platform betekent een extra afhankelijkheid van Microsoft. Nou ja, hoe erg is dat? Zijn er alternatieven? Dus dat zijn ook van die dingetjes die je misschien tijdens het... En dan kan ik me voorstellen dat je dan zegt, dat je bijvoorbeeld een keuze krijgt, wordt het dan low-code, of wordt het dan juist full-code, met behulp van een AI-tool, waarbij je...

### ~ 9 Min

Cor Blom  
Ja, want het is denk ik wel handig om te weten dat het idee nu is, voor deze is in ieder geval om niet naar low-code te kijken, maar gewoon echt een ontwikkelde... 

Arno de Boer  
Full-code, ja, dan moet je dat Power Platform, dan is hij inderdaad... 

Cor Blom  
Ja, laat dat maar... Laat dat dan maar even achterwege.

Arno de Boer  
Dan zou ik inderdaad zeggen, kijk gewoon vooral naar, nou wat doen we hier bij HIP, daar heb jij denk ik het meeste kennis van.

Cor Blom  
Ik weet het ook niet allemaal, maar... Ja, daar komen we wel achter.
Ja, maar Bruno, heb je nou wel eens... Bruno weet dat best, dat is een beetje een developer, geloof ik.
Ja.

Cor Blom  
Ja, dat ben ik wel. - Ja, maar daar komen we wel achter. - Ja, maar

Arno de Boer  
Bruno, ben je dat best aan het dicen, met je developer-geloven? - Ja, Bruno kan dat wel. - Ja, dus ik denk dat je even met Bruno moet vragen: van God, welke talen gebruiken jullie? - Ja. - Of welkeontwikkeltalen? - Ja, voor input.

Cor Blom  
En daarnaast denk ik dat het ook wel belangrijk is: wat is nu actueel? - Ja. - Stel nou, we werken helemaal met COBOL en uiteindelijk willen wedaar helemaal niet mee verder. - Dan moeten we ook niet iets nieuws gaanmaken. - 

### ~ 10 Min

Arno de Boer  
Nee, maar kijk, ik ben dus... Ik sta los van de techniek. - Ja, ja, ja. - Ik heb vroeger wel nog een keer iets met SQL gedaan, Select * From, en dan......hele journaal passen heb ik eruit laten draaien. - O, ja. - Dat kon ik toen. Maar sindsdien doe ik niks meer met programmeren. Dus ik weet niet meer welke talen en wat is logisch. Dat weet ik allemaal niet. Maar wat ik wel weet, en daar ben ik altijd van, is dat je een taal moet kiezen. Die kennis breed in de markt verkrijgbaar moet zijn. Dat die taal ook makkelijk overdraagbaar is. Dus dat het ook niet abracadabra is en een continu ontwikkelaar. Maar goed, dat is bijna het eerste punt ook. Nou, het moet ook veilig zijn. Het moet voldoen aan bepaalde standaarden. Dus in die zin, daar zijn we echt nog wel op zoek. Er is een hoofdstukje in die architectuurkades, daarvan zeg ik ook, van de techniek. Of de technische standaarden die we willen hanteren, dat vind ik wel belangrijk. is een hoofdstukje in die architectuur kaders, daarvan zeg ik ook van de techniek, van de technische standaarden die we willen hanteren, dat vind ik nogal een vraagteken. Wat misschien ook wel goed is voor jou om te weten, 

### ~ 11 Min

Arno de Boer  
is dat ik wel een beetje een drielaags model probeer te hanteren, dus een presentatiekant, daar heb je bepaalde misschien wel ontwikkeltalen voor en dan heb je de integratiekant, API's en weet ik veel en waarschijnlijk ook de onderkant de datakant, dat heb je ook al, dus misschien dat je die gelagen ook in je achterhoofd mee kan nemen, presentatie, integratie, data, misschien zitten er nog vier de laag tegenwoordig tussen, of een tijde, ik weet het niet, software development, maar vaak zie je dat die drie lagen altijd wel terugkomen, integratie, data en... 

Reijer van der Zande  
Nee je hebt natuurlijk je datalaag maar je hebt nog veel meer. Ja, dat is wel een beetje een verandering, maar dat is wel een verandering, dat is wel je ook je, die zit nog database niveau en daarboven heb je natuurlijk nog een stukje bewerkingsniveau, dus dat is waar je programmeert al feitelijk leeft en je API's, hoe je communiceert naar de buitenwereld, dat grenst alweer bijna naar de presentatielaag toe.

### ~ 12 Min

Arno de Boer  
Nou maar dat is heel mooi input voor ons om te hebben van oké, wij moeten misschien wel niet naar een drielaags, maar naar een vierlaagse architectuur. En daarom zeg ik ook, wij zijn continu architectuur, running the business eigenlijk en wat jullie met zo'n software ontwikkelclub doen is changing Daarom zeg ik ook dat wij continu een running the business zijn. En wat jullie met zo'n software ontwikkelclub doen is changing businesses. Dus jullie maken nieuwe dingen. En wat mooi is, is dat jullie staan voorop in technologische ontwikkelingen. En die input kunnen wij mooi gebruiken om te zeggen: Wat zijn de mogelijkheden om de hand te helpen door te ontwikkelen? Dus ik probeer eigenlijk altijd... Jullie lopen voorop, we zijn de verkenners.

Reijer van der Zande  
Er komt nog een potje terug en daar moet wat mee.

Arno de Boer  
Daar zit het gammernei. Moet je daar maar een bommetje op gooien. Dat is een beetje het idee. Ga gewoon aan de slag. Maar bedenk dat soort vraagstukken. Want...

### ~ 13 Min

Arno de Boer  
Vanuit ons business perspectief, wat betekent dat voor ons? Als we het in gebruik nemen, welke risico's lopen we? Wat betekent dat voor hoe we misschien doorontwikkeling moeten vormgeven? Welke talen moeten we hanteren? Dus ook gelijk even naar breder kijken. 

Reijer van der Zande  
Ik denk dat als ik dit zo hoor, dat een levend gedeeld document misschien ook wel handig is. Want ik denk dat het ook heel belangrijk is om tijdig feedback te krijgen. En dat is ook heel belangrijk als jullie vragen niet beantwoord worden.

Arno de Boer  
Dat lijkt me heel goed. Neem het dadelijk mee. dat het ook heel belangrijk is om tijdig feedback te krijgen als jullie vragen niet beantwoord worden. Het klinkt misschien gek, maar ik vind het heel belangrijk voor de hand om dit goed voor elkaar te hebben.

Reijer van der Zande  
Ik kan ook een geitenpatje opslagen en denken: 'Nu kunnen we er niks meer mee.' Ik denk dat het belangrijk is om te zorgen dat we een gedeeld document hebben of iets waar we... We moeten even kijken hoe we dat het handigst kunnen vormgeven.

Arno de Boer  
Het maakt mij niet uit. Deel het met mij en zorg ook dat je maar achter de broek aan zit. Dat klinkt misschien gek, maar ik heb het heel druk.

### ~ 14 Min

Reijer van der Zande  
Ik zag het in de agenda inderdaad.
Ik vind het best wel een cruciaal stuk, omdat ik denk dat we met alle AI-ontwikkelingen en alles wat er gebeurt, dat wij... Daar heb ik het ook al met Cor over gehad. Wij ontkomen er niet aan om... Misschien wel van hip naar hoik heb ik het al genoemd. Hanze onderwikkel integratie platform. Ja, ja. een integratieklap. - Hoi! - Van hip naar hoip. Ja, dus ik zie wel dat we gewoon... we doen het nu al, alleen we doen het nu op zulke... heel gefragmenteerd, niet gesandaliseerd, en dat levert allemaal risico's op. En we zetten het niet in voor de doeleinden waarvoor je het misschien wel wilt inzetten. En dus dat is een beetje de kern. Zal ik jou meenemen in de... - Ja, doe nog even om... waarvoor je het misschien wel wilt inzetten. En dus dat is een beetje de kern. Zal ik jou meenemen in de...

Cor Blom  
Ja, doe nog even bijvoorbeeld concreet. We hebben het vanochtend over gehad over requirements.En dat was één van de dingen.  Dat was bijvoorbeeld integratie met Osiris. Dus optioneel. En hetzelfde met webroombooking.

### ~ 15 Min

Cor Blom  
Dat zijn wel allemaal afhankelijkheden. Die kun je nu wel regelen en bouwen. Maar hoe gaat dat dan in de toekomst? En is het dan wel handig om juist zo'n keuze te maken nu? Of juist niet? Dat kan je ook concreet doen.

Arno de Boer  
Ja, en zo'n integratie. Want bij webroombooking bijvoorbeeld. Op webloop in principe willen wij integraties via het integratieplatform laten lopen. Dus dat zijn echt van die dingen. Dat denk je als losse ontwikkelaar niet bijna. Dus nou ja, zo. 

Reijer van der Zande  
Maar ik neem aan dat het zometeen op basis van de andere documentatie ook duidelijker wordt.

Arno de Boer  
Ja, maar daarom is het wel goed dat je inderdaad gewoon aan de slag gaat. En afstemt van oké, hoe loopt het? En waar krijgen we... Nou ja, we lopen tegenaan. Wat voor vragen spelen we? En wat ik ook al meelees. Maar hier nemen jullie een afslag. Die willen wij helemaal niet. En dan gaan we in gesprek. Nou ja, dan gaan we in gesprek. Maar het is een vingeroefening. En niks is fout. Dus dat hebben we ook bij hebben gezegd.

### ~ 16 Min

Arno de Boer  
Niks is fout. Het kan in de prullenbak belanden. Het kan ook zijn dat we denken van nou, dit is eigenlijk zo goed. Dus gaan we eens kijken hoe het werkt. ja gaan we met de brede inzetten ja dan gaan we even de vrotvast erop leggen we gaan even kijken hoe rookt dit hebben we nou ja hebben we alle voorwaarden alles wat mis kan gaan hebben we daar iets voor ingeregeld zeg maar nou ja dat is op die manier daarnaar kijken 

Reijer van der Zande  
ja maar ik denk dat daar dan een kort lijntje is denk ik belangrijk want ik heb inderdaad tijdig op bij sturen wat nou ik zeg het is zonde om heel wat energie en tijd sturen in een oplossing die uiteindelijk voor niemand gaat werken.

Arno de Boer  
dat lijkt me niet nee dat dat sowieso jullie hebben wel afstemmingen onder verpleegkundig toch met de met de en en duurzaam 

Reijer van der Zande  
ja 

### ~ 17 min

Arno de Boer  
natuurlijk ook wel belangrijk is dat je Ronald Steenstra die heb je die moet je meenemen in de functionele kans om vraagstuk dus bijvoorbeeld
stel en dus hij moet dit gaat puur over verpleegkunde kunnen maar wie is die zegt mij dat verpleegkunde kunnen niet een lijst van wensen heeft ja die totaal botst met wat het conservatorium ik noem eens iets en hoe gaan we daarmee om dat zijn ook dingen die kunnen gebeuren dat jij kunt het echt maar wel anders zo is om zo wij gaan die met je linksaf en dan hebben we een hele stroom linksaf en zo komt conservatorium maar wij willen daar rechtsaf en we hebben er al ja hoe gaan we dat dan hoe gaan we daarmee om ja 

Cor Blom  
Ronald Steenstra is een informatie manager via hem komt de opdracht hier ook naar binnen. Maar ik heb hem inderdaad ook gevraagd om bij de sessie van vanochtend bij te zijn. Maar daar had hij dat voor wel prima. Maar ik denk dat het wel goed is om hem in de loop te houden inderdaad.

Arno de Boer  
Ja, want anders krijg je een hele gekleurde verpleegkundige oplossing. En dan krijg je eigenlijk een point oplossing.

Reijer van der Zande  
Ik heb hem wel vanochtend tegen verpleegkunde aangekaart. Dat het doel ook is om een generieke oplossing te maken. En dat die voor iedereen draagbaar moet zijn. En ja, dat zal in eerste instantie wel een beetje toegespitst zijn op wat hun willen.

### ~ 18 min

Arno de Boer  
Voorzichtig, ja. Voorzichtig zegt mijn ervaring op dit moment bij gebruik het niet in het deden. Maar ik merk wel dat zorg over het algemeen redelijk ook generiek toepasbaar is op veel plekken. Ik merk dat daar gewoon de processen, het is wel volwassener dan...
Nou, dat is goed.

Reijer van der Zande  
Dat is wel goed om mee te nemen. Want ik had ook inderdaad van mijn eigen perspectief uit, hoe ik er zelf over nadacht, had ik niet het idee dat er hele rare specifieke eisen waren vanuit verpleegkunde. Ik had het idee, nou, dit zou binnen elke opleiding, heb je hier de basisdingetjes wel te pakken.

Arno de Boer  
Ja.

Reijer van der Zande  
Dat was mijn eerste indruk in ieder geval.

Cor Blom  
Ja, en ik denk dat je er ook wel rekening mee moet houden dat je nooit een 100% match hebt voor alles.

Arno de Boer  
Nee, dat kan ook niet.

Cor Blom  
Want de comfortorium is echt wel een special in dit geval. En Minerva is nog een keer een special. met de Wilmer-Alexander Sportcomplex houdt dat je nooit een 100% match hebt voor alles. Dat zijn ook weer hele andere werelden dan wat wij zien.

### ~ 19 min

Arno de Boer  
Ja, en met een special, waar ik naartoe wil werken met een special, eigenlijk is dat een special een afslag is in een proces. En niet zozeer dat een special een nieuw proces is.

Reijer van der Zande  
Exact, ja.
Dus dat je eigenlijk zegt van, oké, we doen het generiek waar het kan en als het heel specifiek moet, dan doen we datgene wat specifiek is ook op een generieke manier. En ook zo generiek mogelijk. Dus je gaat pas, ik noem altijd de bol.com werkwijze. Dus je kunt daar allerlei input ingooien en er komt allerlei verschillende output in of uit. Maar wat ertussen gebeurt is best gestandardiseerd. En dat is natuurlijk omdat, echt, anders kan niet. Het komt nooit die catalogus aanbieden die die nu heeft. Zo geldt dat ook voor de Hanze. Als wij uniform werken, dan kan het best zijn dat er één keer hetproduct is een muziek, een compositie. En de andere keer een product is een, weet ik veel, een auto op zonnepanelen. Of zo.

Reijer van der Zande  
ja, jazeker. Oké.

### ~ 20 min

Arno de Boer  
Nou, dit is dus vers van de pers. Vorige week. - Waar zit uw plaat? - Ja, over plaat, misschien is het zo'n tekst. Hij is dus vers van de pers, vorige week tijdens jullie vakantie. - Oeh, ben jij ook weer even te zweten? 

Reijer van der Zande  
Ja. 

Cor Blom  
Immand moet men werken, hè.

Arno de Boer  
Mag ik jouw achtergrond even weten? 

Reijer van der Zande  
Ja, ik... Hoe ver wil je het weten? Ik ben ooit hier bij Hanze begonnen als chemiestudent. En ik ben intussen tijd gaan programmeren.  En daar ben ik nu een aantal jaren werkzaam. En ik werk sinds, nou, vorige oktober ergens voor CropX in Haren. Ik ben daar een Python Django developer. Ja, heel veel legacy code. Dat is een beetje mijn achtergrond. Dat is een beetje wat je zocht?

Arno de Boer  
Ja, precies. Je bent dus eigenlijk al werkende. 
Reijer Ja, ja. En ik heb inderdaad bij mijn vorige werkgever besloten dat ik dacht: ik wil toch wel een papiertje hebben. Ik wil die kennis wat verder dichten.

### ~ 21 min

Arno de Boer  
En dan doe je nu een master, is dat toch?

Reijer van der Zande  
Nee, dit is gewoon een hbo deeltijd. En ik moet nu nog een stukje afstuderen doen. Nou, daar valt dit project onder. 

Arno de Boer  
Nou, dit is een super project om in afstuderen dacht ik zelf. Even kijken. - Dank je. Oh ja, hier is... - 

Cor Blom  
Ja, en dit is ook om genoemd te weten: Reijer is in principe op de maandag aan de slag voor ons.

Arno de Boer  
Oké, dat is goed. Want maandag heb ik ook wel ruimte.

Cor Blom  
Ja, precies.

Arno de Boer  
En Jos en Mirjam zijn dan ook wel.
Dus bijna iedereen wel op maandag.

Reijer van der Zande  
Ja, ik werk dinsdag tot en met vrijdag voor mijn betalende baan. En dan probeer ik op maandag het werk te genereren dat ik in het weekend nog wat bij kan spijkeren als het moet. Dus die manier probeer ik daar uitvulling aan te geven.

Arno de Boer  
Ja. Het is nu een word document geworden, want het is voor een militaire. Ja, ja, inderdaad. Nou, kijk, slimme inzet. Blablabla. Even kijken hoor. Dus dit kun je allemaal vergeten. Dus ik deel het met je zodra het eind is gehoord. Officieel, ja.

Reijer van der Zande  
Helemaal goed.

### ~ 22 min

Arno de Boer  
Nou, we hebben eigenlijk even achtergrond. Wat jij ziet is dat we op verschillende plekken en op verschillende manieren software ontwikkelen. Dus we hebben de ene keer, nou, hebben we het kleinschalig. Inzet van NSBusinesscard, die kennen we natuurlijk wel.

Cor Blom  
Ja, zeker.

Arno de Boer  
En de andere keer hebben we ook gewoon betreidscritische systemen. De inzetplekken die we in de data zetten. Dus het gaat van rijk tot groen, klein tot heel groot. En we hebben allemaal kleine dingetjes. Dus we hebben softwareontwikkeling bij het functioneel beheerteam, ICTOis dat, dus ICT en onderwijs. Daar hebben we laatst iets gemaakt. Ook iets om de leraar te ondersteunen. Hartstikke goed idee. En daar zit één iemand, Maurits in dit geval, die heeft dat ontwikkeld. Die heeft dat ontwikkeld. En die geeft er kennis. Wat er gebeurt als hij straks er vandoor gaat. Nou, jullie heb ik er neergezet.

### ~ 23 min

Cor Blom  
De CollaSpace geef je aan elkaar trouwens.

Arno de Boer  
Oh ja, oké. Ga verder.Vastgoed en Facilitair, dat zit dus inderdaad ook. Webroombooking, digiroosten. Hanze Integratie Platform, dat is de dataplatform ook. Teams, cloud, infra en onze digitale werkplek. Daar wordt ook software ontwikkeld. CRM, dat is eigenlijk een power app, waar eigenlijk continu softwareontwikkeling is. En wat ik ook onder softwareontwikkeling vastgelegd heb, dat is eigenlijk, je noemt het al, low-code, no-code. Tegenwoordig, de aanvassingen van deze wereld, die zijn zo geavanceerd, dat je software kan ontwikkelen door dingen in elkaar te klikken.

### ~ 24 min

Reijer van der Zande  
Ik heb binnen de Duo de OTAP straat voor een low-code platform ingelegd. En binnen de opleiding hebben we met Pegasus gewerkt. Pega.

Arno de Boer  
Oh ja, oké. Dus je hebt heel veel van die workflow management tools, management tools, waarvan je eigenlijk kan afvragen: is dat nog wel functioneel beheer? of is het echt softwareontwikkeling? Want er gaat businesslogica in, er gaat heel veel analysewerk in, wat je eigenlijk ook nodig hebt voor softwareontwikkeling. Het enige verschil is: je schrijft geen code, maar je klikt het in elkaar. Ja, dat is eigenlijk het verschil. Nou, en dan de knelpunten, dus we hebben een risico, kwetsbaarheid, continuïteit en beschikbaarheid, beperkte kennis die bij slechts enkelemedewerkers aanwezig is. Dat zie je overal bij al die plekken, behalve dan bij de CollabSpace. 

Cor Blom  
Dank je.

Arno de Boer  
Is het allemaal gefragmenteerd, als ik het even vastgoedig faciliteer, is het één iemand die het doet. En die iemand is ook extern.

Cor Blom  
Ja, een risico. 

Arno de Boer  
Het is best een risico. 

Cor Blom  
dat is toch een mooi lijstje voor jou, denk ik ook, die van de hier gevoerd worden. Dat is een heel goed, gefragmenteerde aanpak, die klapjet. - Ja.

### ~ 25 min

Arno de Boer  
Nou, en een onvoldoende benutting van de aanwezige capaciteit en expertise, ik heb het op de Digital Site-cup genoemd, maar dat is niet het geval. Dus dat is één van de... Nou, en wat ik eigenlijk wil, is het doel softwareontwikkeling slim, beheersbewust en toekomstbestendig in te zetten. Nou, dat is... Nou, helft ze digitaal kompas, eigenlijk zou je daarmee willen beginnen. Maar ik had zoiets van: ja, dat is meer te hoger over dan het algemeen. We willen eigenlijk ook vanuit de strategie terugredeneren van: oké, wat betekent dat voor de manieren nu? Dus we gaan eigenlijk kijken van: hoe ziet de toekomst van de Hanse eruit? En wat moeten we nu daarvoor gaan organiseren? Dus dat is meer van: oké, welke richting gaan we op als informatiserings- of eigenlijk business support IT afdeling? En wat is softwareontwikkeling? Dat is een beetje de definitiekwestie. Ik heb gewoon die twee, dus de no-local platformen en de ontwikkeling met programmeertalen, die twee onderscheiden. Maar ik wil ze wel beide benoemd hebben, omdat wat je letterlijk ziet gebeuren, is dat bepaalde software tools die we al in huis hebben, dan

### ~ 26 min

Arno de Boer  
gaan die functioneel beheerteams, die gaan maar door. En tot zo op een bepaald moment iets maken wat groter is dan het proces waar de applicatie voor bedoeld is. Ja, en dan gaan ze te ver. Maar het kan allemaal. Dus ook daar wil je kaders in staan.

Cor Blom  
Is het al ingediend, dit document?

Arno de Boer  
Morgen wordt het geafgeleerd.

Cor Blom  
Maar je hebt nu de derde, dat is natuurlijk vibe-coding, dat jij als niet-programmeer iemand met een prompt kan vragen: maak een programma voor mij.

Arno de Boer  
Ja, dat heb ik ook genoemd bij kunstmatige intelligenties, dat betekent het genereren van de code.

Cor Blom  
Oh sorry, oké.

Arno de Boer  
Dus dan wordt die code al gegenereerd door...

Cor Blom  
Ja, vibe-coding inderdaad.

Arno de Boer  
Ja, dus meer vibe-code.

Cor Blom  
Ja, zo heet dat.

Arno de Boer  
Ja, dat zou ik bij de volgende versie ook willen.
Maar ja, vibe coding zie ik nog wel.

Reijer van der Zande  
Ja, vibe coding vind ik wel... dan... Ik vind het altijd een beetje... copy-paste. Letterlijk. Terwijl dan de... verantwoordelijkheid van de programmeur... neemt heel erg af. Terwijl als je juist daar als... verantwoordelijke programmeur tussen
zit... is het wel een andere orde.

### ~ 27 min

Arno de Boer  
Ja, zeker nog. Nee, de verantwoordelijkheid... van de programmeur neemt niet af. Die wordt juist gehouden.

Reijer van der Zande  
Ja, maar je bent geen programmeur.

Arno de Boer  
Je bent regisseur van de programmacode.

Reijer van der Zande  
Ja. Maar er zit dus een groot... gevaar tussen copy-pasten en... weten waar je mee bezig bent.

Arno de Boer  
En dat is een cruciale. Weet waar je mee bezig bent. Nou, prachtig hoe je dit zegt. Want ik heb letterlijk ook... een van de structuurprincipes die wij
hebben is... De Hanse weet welke... informatie ze waarom verwerkt. Alleen die uitspraak... als ik die neerlees en iedereen zegt: "Ja." Nou, oké, geef jij dan maar een... definitie van de term student. Nou, dan krijg je tien verschillende definities. Tien verschillende definities van student. Dus wij weten niet welke informatie wij verwerken.Want als je tien verschillende antwoorden krijgt... over die term, heb je... Hetzelfde geldt voor code. Als jij code laat maken door AI... dan moet je... blijven weten... wat die code doet, waarom die dat doet... en moet je die code ook kunnen volgen.

### ~ 28 min

Arno de Boer  
En als je het niet kan, dan ga je iets verliezen, waar je nooit, never nooit meer... blijven weten wat die code doet, waarom die dat doet, en moet je die code ook kunnen volgen. En als je het niet kan, dan ga je iets verliezen waar je nooit, never, nooit meer recht kan brengen. Dus dat is een hele mooie: weet waar je mee bezig bent.
En eigenlijk geldt dat voor de Hanze met processen. Wij moeten ook zeggen dat wij onze processen beheersen, net zoals Bol.com haar processen beheerst, moeten wij dat ook. Even strategische inzet van softwareontwikkeling. Ik wilde nog een term toevoegen, of een principe: 'high value, low risk'-principe, wilde ik introduceren. Alleen toen bedacht ik mij: misschien is die net niet helemaal, maar dat is wel een beetje waar ik naartoe wil. Als je kijkt naar een onderwijsportaal, dat is high value. Als je als student hier binnenkomt, moet je nu een studie doen voordat je alle systemen weet te werken, zonder dat je daar een portaal tussen hebt zitten en die brengt alles bij elkaar en die laat jou...

### ~ 29 min

Arno de Boer  
Je begeleidt jouw navigeer, je navigeert zo door de Hanze logisch op basis van je dagelijkse praktijk. Dat is een high value, maar tegelijkertijd ook low risk. Want als die uitvalt, heb je je primaire systemen nog gewoon.

Cor Blom  
Je hebt gewoon nog steeds die Brightspace.

Arno de Boer  
Je hebt nog steeds die Brightspace, maar dat is een beetje de dingwijze van 'high value, low risk'. Eigenlijk wil je niet die grote bedrijfscritische moeders, die die grote bedrijfscritische Maar dat is een beetje de dingwijze van high value, low risk. Eigenlijk wil je niet die grote bedrijfscritische software... Het moet gewoon doorgaan. Daarom hebben we ontwikkeling van intuïtieve betalen. Overbruggingsfunctioniteit, daar valt bijvoorbeeld deze denk ik ook onder. En dat is eigenlijk iets wat nog niet door de leverancier wordt gedaan, maar we willen het wel gebruiken. Mobiele apps. En wat mij betreft, die tweede kan er niet hard genoeg aan. Dat moet ook gewoon met vergrijzing en zo. We moeten zorgen dat wij onze ondersteunende processen zo veel mogen digitaliseren.

### ~ 30 min

Arno de Boer  
Maar dat betekent ook dat we moeten weten hoe we werken. Dat betekent ook dat, nou ja. Data en integratie. En die vierde, geloof ik, die vierde is nog wel een beetje disputabel. Want we weten niet hoe ver een surf iets gaat. Maar ik kan me voorstellen dat de voorkant van een AI tool, dat dat mooi moet integreren in ons onderwijsportaal of zoiets. Dus dat je een AI assistent iets kan vragen. Dat die gewoon door de data van Brightspace loopt. En dan komt die ook met een heel gericht antwoord. Nou, dat wil je misschien wel dat het een look and feel heeft. En een beetje... Dus daar, dat hebben we nu wel benoemd. Ik weet niet of het zeker was, maar dat is een beetje... Nou ja, prototyping. Voor validatie van ideeën. En of als basisformatie. en of als basis voor marktverkenningen.

### ~ 31 min

Arno de Boer  
Wat let ons om in plaats van hele uitgebreide Excel documenten met eisen en wensen te maken, gewoon een soort van proof of concept te maken van een product.Eigenlijk wil je dat het zou hebben, dan ga je daarmee de markt op. Waarom is dat niet zo? Waarom hebben jullie dat niet? Nou, daar hebben jullie wel een ander gesprek, ook in de marktverkenning. Dus daar kun je ook... Dus, nou ja, die hebben we ook. Nou, dan de principes. Ik ga niet alle teksten door, maar dan kun je later wat doen. Maar eigenlijk zeggen we 80% van de benodigde functionaliteit. Als het minder dan 80% is... Als het groter is dan 80% in de marktverkrijgbaarheid, dan gaan we niet zelf ontwikkelen. Zo simpel is dat. Dus als het...Is het de vraag natuurlijk...

Reijer van der Zande  
Hoe meet je dat?

Arno de Boer  
Hoe meet je dat? Nou, wat ik me kan voorstellen is...
Ik zie een Excel... Ken je aanbestedings criteria? Dan moet je dus een functionele eisen en wensen-lijst maken. En dan ga je met die lijst van eisen en wensen scoren in hoeverre iets dat heeft. Zo kun je dat weten. Wat dat al is gedaan is een tweede. 

### ~ 32 min

Arno de Boer  
En dit is natuurlijk ook niet... En dat... Ik bedoel dat het groter is, maar het is een kaart. Dus het kan best zijn dat die soms 79% is en dat je dan En wat een beton grote is, maar het is een kaart, een richtlijn. Het kan best zijn dat die soms 79% is en dat je dan zegt van nou, die 79% ik vind dat zo gebruiks-onvriendelijk, ik vind het toch echt, laat me zitten, dat wil ik niet. Dat kan ook, dat je zegt van 70%, maar het is totaal ongebruiksvriendelijk. We ontwikkelen alleen als er een sluitende business case is, ook daarin, dat je eigenlijk een beurskeuze maakt zodat die waarde toevoegt. En dat hoeft niet altijd quantificeerbaar te zijn in de zin van we moeten geld terugwinnen, want we gaan dan meteen 8 FTE ontslaan ofzo, dat is niet de bedoeling. Maar wel dat je erover nagedacht hebt van oké, wat is nou de strategische value die we hebben met dit leren, ik vind het een perfect voorbeeld. Er was niks in de markt, toch was er wel al een opleiding die iets deed. 

### ~ 33 min

Arno de Boer  
Nou, daar kun je van alles van vinden, maar dat is wel op dat moment een high value, een relatief lager risico. Want er was één opleiding die was daarmee bezig en die wist ook van de risico's. Nou ja, dat kan prima, want je doet het dan bewust. Nou ja, dat is een beetje het integratievraagstuk. integratie-vraagcirkel ontwikkelen wanneer... de benodigde functionaliteit, bestaande... want je doet het dan bewust. Nou ja, het is een beetje het integratie-vraagstuk: we ontwikkelen wanneer de benodigde functionaliteit in bestaande systemen overstijgt. Dus dat als je functionaliteit hebt, je hebt functionaliteit A uit systeem A en B uit systeem B, en samen worden ze met nog een klein beetje code functionaliteit C. Dat kan, en dat doe je vaak in zo'n portaal, dan zie je dus dat net niet die functionaliteit past in dat wat de eindgebruiker vraagt. Kun je dat mooi oplossen door die twee dingen met logica te combineren. En wat we ook doen, is we beschrijven wat we nooit in aanleiding hebben gekomen voor zelfbouw of maatwerk.

### ~ 34 min

Arno de Boer  
Wat de absolute no-go-areas zijn: we gaan geen leermanagementsysteem bouwen, we gaan geen OSIRIS bouwen, we gaan geen AFAS bouwen, we gaan geen INDATO bouwen, wat we wel hebben gedaan, want dat is eigenlijk van bedrijfs kritisch en dat is ook wel een hele inzetplanning van docenten gaat erin.

Reijer van der Zande  
INDATO?
INDATO is capaciteitsplanningssoftware. Maar die is zelf gebouwd. Dan denk ik, dan kun je gewoon uit de markt halen. Zou je verwachten, ik denk toen ook wel.Ik denk toen ook wel. Ik weet het niet, 2026. Ik kan me niet voorstellen dat tien jaar geleden er geen software was voor capaciteitsplanning.

Cor Blom  
Ja, geen idee.

Arno de Boer  
Ik kan me niet voorstellen dat er tien jaar geleden geen software was voor capaciteitsplanning.

Cor Blom  
Ja, geen idee.

Reijer van der Zande  
Ik denk dat ik dat met je eens ben.

Cor Blom  
Volgens mij komt het ook uit de hoek van Leo, dacht ik. Redacteuristisch en uiteindelijk wordt het veel te groot en dan heb je niet zo'n data.

### ~ 35 min

Arno de Boer  
Deze is een beetje een ingewikkelde, maar dat heeft te maken met die no-code en low-code softwareplatformen. Wij gaan per bedrijfsfunctie aangeven welke bedrijfsfunctie door welk systeem door ons neemt. Dus als je een bedrijfsfunctie hebt, ik pak de bedrijfsfunctielijst er even bij. Ik noem het wat inschrijving. Dat ga je niet automatiseren door bepaalde platformen. Maar dat laat je automatiseren door de functionaliteit die in Osiris zit. Stel dus dat Osiris die functionaliteit niet standaard heeft, maar die kun je wel bouwen door workflows. Dan is Osiris de plek om dat te bouwen. Hetzelfde geldt voor inkooporders, goedkeuren of zoiets. Het kan functionaliteit zijn waar wij gewoon al een standaard systeem voor hebben.

### ~ 36 min

Arno de Boer  
En waarbij al een workflow is. En waarbij ook een workflowachtige functionaliteit is. Topdesk is ook zo'n voorbeeld. Dat kun je ook zelf al formuleren bij een stukje business.Dus dat is eigenlijk de doelstelling. workflow-achtig functie. Topdesk is ook zo'n voorbeeld. Daar kun je ook zelf al formulieren bij al mijn succybusiness-logica. Dus dat is eigenlijk, dat wil je gewoon met je strategie zijn, maar je wil wel van tevoren weten dat bijvoorbeeld een AFAS niet in één keer zich met de inschrijving van studenten gaat bemoeien.

Cor Blom  
Nee, dat dat niet voor misbruik wordt inderdaad. Ja, zou het wel kunnen inderdaad. Nee, nee, nee, nee. Dat zou wel kunnen inderdaad.

Arno de Boer  
Ja, dat zou het wel kunnen. Nou, en deze is ook wel belangrijk, specifieke applicaties die veel specialistische kennis vereisen. Wat zie je vaak is dat je... Ik heb een prachtig voorbeeld, dat ging over casuïstiek voor verpleegkundigen, ook verpleegkundig was dat toevallig. En dat was eigenlijk ontwikkeld door iemand met verpleegkundige achtergrond. Op het moment dat je daar zelf kennis, op het moment dat je die software wil gaan bouwen, dan moet je dus eerst die kennis van die... Moet je bijna verpleegkundig verpleegkundige opleiding volgen om...

### ~ 37 min

Cor Blom  
Ja.

Arno de Boer  
Omdat... Dat wil je dus niet... Dat ga je dus niet zelf doen. Dus je ziet heel veel van die applicaties, dat hou je lekker buiten de deur. Dat is hele specifieke tooling gericht voor hele specifieke doeleinden. Dat ga je dus niet doen. En eigenlijk valt daar ook bijvoorbeeld onderzoeksoftware, valt daar misschien ook bij onder. En dus dat hele specifieke onderzoeken. Nou, en we eigenlijk zeggen we alle eisen die van toepassing zijn op onze gewone applicaties en ook van toepassing van de applicaties, van toepassing op onze ontwikkeld onderzoeken. En we zeggen eigenlijk alle eisen die van toepassing zijn op onze gewone applicaties zijn ook van toepassing op onze ontwikkelde applicaties. Eigenlijk moeten we daar dezelfde regels voor lanceren.

Cor Blom  
Dus zijn er andere eisen dan wat hierin staat?

Arno de Boer  
Dat zijn wat gedetailleerde eisen. Bijvoorbeeld SSO. Dat je met entera id daarmee inlogt. Dat je connect. Dat je bepaalde...

Cor Blom  
Ja, hebben we dat ergens staan? Dat we dat kunnen delen met Reijer?

### ~ 38 min

Arno de Boer  
Ja, dat kan wel rijden. Volgens mij is die ook net geüpdate. En ook dat is een richtlijn. Zeggen we ook niet altijd van, we voldoen daaraan tenzij. Dus nooit dat we...

Reijer van der Zande  
Maar dat moet dus een sluitende verklaring zijn waarom dat niet kan of waarom dat niet...

Arno de Boer  
Precies. Je kunt ook bijvoorbeeld... Wat we wel eens doen is die SSO-eis laten we soms wel eens vallen omdat er maar twee gebruikers gebruik van maken.

Reijer van der Zande  
Ja, logisch.

Arno de Boer  
Dan zeggen we bijvoorbeeld, gebruikers zorgen er in ieder geval voor dat je als je met je e-mailadres gaat dat je een ander wachtwoord hebt. Dat je twee factoren uit de kaart zet. Ja, zeker. Nou, security en privacy by design, geloof ik wel. Nou, dan heb je de organiseren van zoveel ontwikkeling centraal Dus we zeggen eigenlijk dat, Security en privacy by design, geloof ik wel. Dan heb je de organiseren van softwareontwikkeling centraal. Dus wij zeggen eigenlijk dat, dat is misschien voor jou ook wel goed om te weten, wij zeggen eigenlijk dat als een software, stel dat julliesoftware ontwikkelen voor onze informatiehuishouding, dan zijn wij eigenaar daarvan.

### ~ 39 min

Wij zorgen voor de doorontwikkeling, wij zorgen voor het beheer. En daar kunnen we wel van zeggen, wij besteden het uit aan een partij. Wij zijn de rechtsstuur en wij zijn eigenaar. Wat hier staat. Dus wij zeggen, dat valt binnen een aantal, centraal ingestuurd, ingericht en gefaciliteerd. En dus een verandering voor kaders, governance, ontwikkelstandaard, besluitvorming, afstemming met onderwijs, onderzoek en ondersteuning.Dus die is dus eigenlijk...

Cor Blom  
Ja, mooi.

Arno de Boer  
En daar heb ik nog een aantal. We organiseren samenwerkingen met een externe leverancier voor ondersteuning bij de ontwikkeling. Dus die willen we ook hebben. We maken hierbij gebruik van... De collabSpace, die is hier bij expliciet in genoemd.

Cor Blom  
Dankjewel.

Arno de Boer  
Ja. En softwareontwikkeling wordt ingebed in ons bedrijf, in IV-processen. Dus wat we doen, als er een verzoek binnenkomt, er komt geen verzoek aan software binnen. Er komt een functionele vraag binnen. En wij zijn informatiemanager om te zeggen van nou, dit lijkt me nou welecht iets...

Cor Blom  
Zelf bouwen.

### ~ 40 min

Arno de Boer  
Ja, zelf bouwen. En dat moeten we echt even gaan maken. Ja. Omdat wij ook de portalen gaan inzetten, kan ik me voorstellen dat er steeds meer vragen gaan binnenkomen. AI misschien ook. Volgens mij zijn dat ze. Dit zijn ze.

Cor Blom  
Netjes.

Arno de Boer  
Ja, dus.

Cor Blom  
Ja, verwacht je er wordt gebroken op?

Arno de Boer  
Ik verwacht bij 2.2.9 een verwachtingsdiscussie.

Cor Blom  
Ja. Maar ik denk dat het een hele goede insteek is. Dat je zegt, je ontwikkelt het inderdaad. Je kan het prima door een externe laten ontwikkelen. Maar informatie of BSI blijft verantwoordelijk. BSI.

Arno de Boer  
Ja, BSI. Check. Dus dat zijn de kaders. Ik ga die met je delen als die akkoord is.

Reijer van der Zande  
Heel graag.

Arno de Boer  
Heb jij hier, ik heb veel verteld.

Reijer van der Zande  
Ja, dat is heel fijn.

### ~ 41 min

Arno de Boer  
Als je vragen hebt, je weet wat je vindt. Gewoon benaderen. Zit me af en toe achter de broek aan als ik niet reageer. 

Reijer van der Zande  
Nou, voor mij ging het de laatste keer ook best goed toch? Ik had het eerst ingeschoten. Dit gaat niet werken. Ik draai de vraag even om. En dan krijg ik heel snel antwoord. Dus dat was heel fijn. Dus dat werkte prima wat mij betreft.

Arno de Boer  
Ja, nee mooi. Ik vind het mooi dat ze hebben een mooie casus. Concreet.

Cor Blom  
Ja. 

Arno de Boer  
Ik ben wel benieuwd.

Cor Blom  
Ja, mooi.

Arno de Boer  
We hebben een mooie casus, concreet, maar ik ben wel benieuwd. Eigenlijk zou je hem dus ook even moeten toetsen in deze casus.

Cor Blom  
Eigenlijk wel ja. 

Arno de Boer  
Maar dat mag Ronald doen. Dat is wel iets wat Ronald mag doen. Nou, dan leggen we het bij Ronald even af. Je mag dan meteen even die, want ik heb morgen volgens mij afstellingmet Ronald over het voorgeven van dit.

Cor Blom  
Ja, absoluut.

Arno de Boer  
Dan blijf ik wel even goed. Dus dan ga ik verder met mijn deadline. Je hebt genoeg in eerste instantie.

### ~ 42 min

Reijer van der Zande  
Ik denk in eerste instantie wel. Ik zeg, we gaan even loopend contact houden. Ik heb het contact.
