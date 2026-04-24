# Hanze Verantwoordingsverslag Backlog

Deze backlog is afgeleid van [hanze-gap-analysis.md](/Users/reijer/Repo/docsmith-demo/docs/hanze-gap-analysis.md) en gebruikt die analyse als bron van waarheid.

Doel van deze backlog:

- duidelijk maken wat de Docsmith-engine nog moet kunnen
- duidelijk maken welke template- en workflowaanpassingen in deze repository thuishoren
- voorkomen dat deze repository enginegedrag gaat simuleren met tijdelijke workarounds

Deze repository beschrijft dus vooral requirements en afhankelijkheden. Engine-implementatie gebeurt in de sibling `../docsmith` repository.

## Completed structural milestones

De volgende structurele stappen zijn voor deze demo nu functioneel afgerond:

- DONE: uitbreidbare metadata in de engine consumer-flow
- DONE: minimale documentzones
- DONE: first-class appendices
- DONE: first-class bibliography placement
- DONE: first-class TOC placement
- DONE: template cleanup voor dubbele structurele elementen

Deze backlog verschuift daardoor van structurele workarounds naar engine-template contract, rijkere metadata-invulling, authoring workflow, beeldverwerking en verdere professionalisering.

## 1. Docsmith engine backlog

Dit zijn required engine capabilities. Ze beschrijven wat deze repository van de engine nodig heeft, niet hoe de engine dat intern moet bouwen.

### 1. Uitbreidbare documentmetadata

- Problem it solves: `spec.yaml` moest eerst basisdocumentmetadata declaratief naar templates kunnen doorgeven.
- Why it matters: een verantwoordingsverslag heeft meer nodig dan alleen titel, subtitel, auteur en datum, bijvoorbeeld studentnummer, opleiding, begeleiders, opdrachtgever en documenttype.
- Priority: high
- Estimated scope: medium
- Dependency: none
- Recommendation: done

### 2. Minimale documentzones: front matter, main matter, back matter

- Problem it solves: de engine moest onderscheid kunnen maken tussen front matter, hoofdtekst en afsluitende delen.
- Why it matters: deze use case vereist ten minste een betrouwbare scheiding tussen ongenummerde front matter en genummerde hoofdtekst, plus een nette plaats voor afsluitende onderdelen.
- Priority: high
- Estimated scope: large
- Dependency: none
- Recommendation: done

### 3. Engine ↔ template contract

- Problem it solves: de verwachtingen tussen engine en template zijn nu te impliciet.
- Why it matters: deze repository heeft een stabiel contract nodig over welke metadata beschikbaar is, welke documentzones bestaan, hoe appendices worden aangegeven en hoe bibliografie en inhoudsopgave gepositioneerd kunnen worden. Impliciet gedrag maakt templates fragiel en maakt validatie onbetrouwbaar.
- Priority: high
- Estimated scope: medium
- Dependency: items 1 and 2
- Recommendation: implement now

### 4. Appendix support

- Problem it solves: appendices moesten first-class worden in plaats van op incidenteel marker- of templategedrag te leunen.
- Why it matters: bijlagen horen bij dit type verslag en moeten betrouwbaar achterin kunnen verschijnen met consistente appendixstatus en labeling.
- Priority: high
- Estimated scope: medium
- Dependency: item 2 and item 3
- Recommendation: done

### 5. Bibliography placement

- Problem it solves: de literatuurlijst moest zonder handmatige documenttrucs op de juiste plek kunnen landen.
- Why it matters: deze repository verwacht dat de engine de literatuurlijst op een gecontroleerde plek in de documentstructuur kan laten landen, zonder raw LaTeX of handmatige `refs`-workarounds.
- Priority: high
- Estimated scope: medium
- Dependency: item 2 and item 3
- Recommendation: done

### 6. Table of contents placement

- Problem it solved: de inhoudsopgave stond eerder alleen correct doordat de demo een apart handmatig TOC-bestand gebruikte.
- Why it matters: voor een verantwoordingsverslag is de plek van de inhoudsopgave een vaste conventie en geen ad-hoc templatekeuze.
- Priority: high
- Estimated scope: medium
- Dependency: item 2 and item 3
- Recommendation: done

### 7. Template metadata and partial support in the render contract

- Problem it solves: templatebestanden zoals `metadata.yaml` en eventuele partials zijn nog geen duidelijk ondersteund contract tussen engine en template.
- Why it matters: zonder dit blijft deze repository meer enginekennis in templates stoppen dan wenselijk is.
- Priority: medium
- Estimated scope: large
- Dependency: item 1 and item 3
- Recommendation: implement soon

### 8. Profielgebaseerde structuurvalidatie

- Problem it solves: `docsmith validate` controleert nu vooral technische aanwezigheid en niet of een document logisch aan een verantwoordingsverslagprofiel voldoet.
- Why it matters: in deze use case is structuurdiscipline minstens zo belangrijk als buildbaarheid.
- Priority: medium
- Estimated scope: medium
- Dependency: items 2, 4, 5, and 6
- Recommendation: implement later

### 9. Schema evolution / compatibility notes

- Problem it solves: `spec.yaml` en het documentmodel zullen evolueren, maar die veranderingen zijn nog niet expliciet gekaderd.
- Why it matters: breaking changes zijn in `0.x` acceptabel, maar ze moeten expliciet worden gedocumenteerd zodat consumer repositories zoals deze weten wanneer ze mee moeten bewegen.
- Priority: medium
- Estimated scope: small
- Dependency: none
- Recommendation: implement soon

### 10. End-to-end rendering tests met echte toolchain

- Problem it solves: regressies in metadata, documentzones, appendices en bibliografie kunnen nu te laat aan het licht komen.
- Why it matters: zodra deze repository serieuzere real-world use cases gaat valideren, wordt enginebetrouwbaarheid belangrijker.
- Priority: medium
- Estimated scope: medium
- Dependency: items 1 through 7
- Recommendation: implement later

### 11. Machine-readable build manifest or JSON CLI output

- Problem it solves: buildresultaten zijn nu vooral mensleesbaar en lastig verder te automatiseren.
- Why it matters: nuttig voor CI en reviewflows, maar geen eerste blocker voor deze use case.
- Priority: low
- Estimated scope: small
- Dependency: none
- Recommendation: implement later

### 12. Real multi-format and DOCX support

- Problem it solves: de config suggereert bredere outputmogelijkheden dan de engine nu daadwerkelijk levert.
- Why it matters: nuttig op termijn, maar geen voorwaarde om dit verantwoordingsverslagprofiel geloofwaardig te maken.
- Priority: low
- Estimated scope: large
- Dependency: none
- Recommendation: implement later

## 2. Hanze template backlog

Dit zijn templatewijzigingen in deze repository. Ze blijven afhankelijk van enginecapaciteiten en horen pas te gebeuren zodra de benodigde enginecontracten beschikbaar zijn.

### 1. Declaratieve titelpagina en omslagmetadata integreren

- Problem it solves: de huidige template leest al meer metadata dan de demo invult, waardoor titelpagina en omslag nog te weinig echte documentgegevens tonen.
- Why it matters: zonder dit blijft de template een demo-layout en geen herbruikbare verantwoordingsverslag-template.
- Priority: high
- Estimated scope: medium
- Dependency: engine item 3
- Recommendation: baseline done, expand test coverage

### 2. Hard-coded Hanze- en documentwaarden terugbrengen

- Problem it solves: opleiding, instelling en documenttype zitten nu nog te direct in de templatecode.
- Why it matters: deze repository moet realistische use cases kunnen modelleren zonder templatecode telkens te herschrijven.
- Priority: medium
- Estimated scope: small
- Dependency: engine item 1 and engine item 3
- Recommendation: implement soon

### 3. Appendix-opmaak integreren op basis van engine support

- Problem it solves: appendixpresentatie is nu deels incidenteel en niet volledig declaratief.
- Why it matters: zodra de engine appendices first-class ondersteunt, moet de template dat duidelijk en professioneel zichtbaar maken.
- Priority: medium
- Estimated scope: small
- Dependency: engine item 4
- Recommendation: implement soon

### 4. Literatuurlijst-opmaak integreren op basis van engine placement

- Problem it solves: de literatuurlijst is structureel correct geplaatst, maar de visuele presentatie is nog te basic voor langere rapporten.
- Why it matters: deze repository wil een realistische rapportpresentatie die ook bij langere bronlijsten overeind blijft.
- Priority: medium
- Estimated scope: medium
- Dependency: engine item 5
- Recommendation: implement soon

### 5. Beeldplaatsing en afbeeldingscontrole verder uitwerken

- Problem it solves: de baseline voor afbeeldingsplaatsing is aanwezig, maar geavanceerdere controle voor cropping, positionering en consistente layout ontbreekt nog.
- Why it matters: voor een realistische thesis-workflow moet beeldmateriaal voorspelbaar en presentabel geplaatst kunnen worden zonder incidenteel handwerk.
- Priority: medium
- Estimated scope: medium
- Dependency: none
- Recommendation: implement soon

### 6. Figuur- en tabelpresentatie verder uitwerken

- Problem it solves: de basis voor figuur-/tabelcaptions en floatpresentatie werkt nu, maar complexere rapporten vragen nog explicietere keuzes voor nummering, referenties en eventueel lijsten van figuren/tabellen.
- Why it matters: dit verhoogt de professionele bruikbaarheid van de template, maar is geen eerste blocker.
- Priority: medium
- Estimated scope: medium
- Dependency: none
- Recommendation: implement later

### 9. Automatic figure/table numbering and cross-references

- Problem it solves: de basisroute voor figuur-/tabelcross-references is nu aanwezig in de demo, maar moet nog breder beproefd worden in rijkere rapportvarianten en complexere referentiepatronen.
- Why it matters: voor een verantwoordingsverslag is dat een duidelijke stap van demo-opmaak naar echt bruikbare rapportworkflow.
- Priority: high
- Estimated scope: medium
- Dependency: none
- Recommendation: implement soon

### 7. Running heads en page style verfijnen

- Problem it solves: lange titels en langere rapporten kunnen met de huidige paginastijl onrustig ogen.
- Why it matters: nuttig voor polish, maar ondergeschikt aan structurele engineafhankelijkheden.
- Priority: low
- Estimated scope: small
- Dependency: none
- Recommendation: implement later

### 8. Template robuust houden op minimale TeX-omgevingen

- Problem it solves: templatewijzigingen kunnen ongemerkt weer extra lokale LaTeX-aannames introduceren.
- Why it matters: deze repository is een validatieomgeving en moet daarom niet onnodig gevoelig worden voor lokale TeX-varianten.
- Priority: medium
- Estimated scope: small
- Dependency: none
- Recommendation: implement soon

## Authoring model cleanup

Dit is de volgende grote fase voor deze repository. De structuur is nu expliciet genoeg; de resterende cleanup gaat vooral over het uit de Markdown halen van layoutverantwoordelijkheid.

### 1. LaTeX uit Markdown-secties verwijderen

- Problem it solved: authored content bevatte eerder nog LaTeX voor layout- en structuurdoeleinden, maar dat cleanupwerk is voor de huidige demo afgerond.
- Why it matters: dit is de basis voor een content-only authoring model.
- Priority: high
- Estimated scope: medium
- Dependency: engine-template contract moest stabiel genoeg zijn om front matter en overige structuur zonder handmatige LaTeX te renderen
- Recommendation: done

### 2. Front matter layout volledig naar template + metadata verplaatsen

- Problem it solved: front matter is nu structureel engine-driven en authored content stuurt de layout niet meer via lokale LaTeX-workarounds.
- Why it matters: de volgende stap is niet meer structurele cleanup, maar verdere templatepolish.
- Priority: high
- Estimated scope: medium
- Dependency: cleanup item 1
- Recommendation: done

### 3. Title-page and report metadata vollediger invullen via metadata in plaats van content

- Problem it solves: de repo gebruikt nog maar een beperkt deel van de beschikbare metadataflow en compenseert dat deels met template-hardcoding.
- Why it matters: een professioneel verantwoordingsverslag moet uit metadata opgebouwd kunnen worden, niet uit handmatige layout in de hoofdstukbestanden.
- Priority: medium
- Estimated scope: medium
- Dependency: cleanup item 2
- Recommendation: baseline done, broaden usage

### 4. Markdown authoring rules expliciet vastleggen

- Problem it solves: zonder duidelijke authoringregels sluipen LaTeX-fragmenten of templateafhankelijke workarounds later opnieuw de documenten in.
- Why it matters: deze repo wil een realistische, herhaalbare auteursworkflow laten zien.
- Priority: medium
- Estimated scope: small
- Dependency: none
- Recommendation: implement now

## 3. Demo/documentation/workflow backlog

Dit zijn repositorytaken die deze repo helpen functioneren als specification layer, validatieomgeving en real-world voorbeeld.

### 1. Authoring guide zonder engineworkarounds voor normale gebruikers

- Problem it solves: auteurs zouden nu te snel workarounds overnemen die eigenlijk in de engine thuishoren.
- Why it matters: deze repository moet uiteindelijk een realistische auteursworkflow beschrijven, niet een verzameling tijdelijke hacks.
- Priority: high
- Estimated scope: medium
- Dependency: engine items 2 through 6
- Recommendation: baseline guide and starter profile done, expand coverage

### 2. Hanze starterpakket voor een echt verantwoordingsverslag

- Problem it solves: de huidige demo is nog geen bruikbaar startpunt voor een echte auteur.
- Why it matters: deze repository wil ook een real-world use case tonen, niet alleen een validatiesample.
- Priority: high
- Estimated scope: medium
- Dependency: engine item 3 and template item 1
- Recommendation: compact baseline done, expand carefully

### 3. Afbeeldingsworkflow en beeldrichtlijnen

- Problem it solves: de basisworkflow voor images is er nu, maar rijkere richtlijnen voor cropping, bestandskeuze en geavanceerder layoutgedrag ontbreken nog.
- Why it matters: deze demo moet realistisch genoeg zijn voor validatie van visuele documentopbouw, niet alleen tekststructuur.
- Priority: high
- Estimated scope: medium
- Dependency: template items 5 and 6
- Recommendation: implement soon

### 4. Mermaid- en diagramworkflow

- Problem it solves: de demo gebruikt nu engine-managed Mermaid-rendering, maar bredere toetsing, regressiedekking en scherpere grenzen van het diagramcontract ontbreken nog.
- Why it matters: echte verantwoordingsverslagen bevatten vaak proces-, architectuur- en contextdiagrammen.
- Priority: high
- Estimated scope: medium
- Dependency: none
- Recommendation: broaden and formalize next

### 4b. Table caption cleanup

- Problem it solved: de huidige demo-tabellen misten nog captions, waardoor de templateverbeteringen niet overal zichtbaar waren.
- Why it matters: consistente tabelcaptions zijn onderdeel van een nette authoringconventie.
- Priority: medium
- Estimated scope: small
- Dependency: none
- Recommendation: done

### 5. Documentatie van huidige enginegrenzen en tijdelijke afhankelijkheden

- Problem it solves: zonder expliciete duiding is onduidelijk welke beperkingen uit de engine komen en welke keuzes lokaal zijn.
- Why it matters: dat helpt deze repository scherp te positioneren als consumer en requirementdrager.
- Priority: medium
- Estimated scope: small
- Dependency: none
- Recommendation: implement now

### 6. Reviewchecklist voor verantwoordingsverslag-structuur

- Problem it solves: er ontbreekt een lichte kwaliteitslaag voor structuurconventies naast technische validatie.
- Why it matters: begeleiders en reviewers kijken juist naar deze conventies.
- Priority: medium
- Estimated scope: small
- Dependency: engine items 2 through 6
- Recommendation: implement soon

### 7. Template-regressieworkflow voor meerdere demo-varianten

- Problem it solves: templateaanpassingen kunnen regressies veroorzaken zonder vaste validatieset binnen deze repository.
- Why it matters: als deze repo meerdere real-world use cases gaat dragen, wordt regressiebeheer belangrijker.
- Priority: medium
- Estimated scope: medium
- Dependency: engine item 10
- Recommendation: implement later

### 8. README’s verder expliciteren als consumer documentation

- Problem it solves: gebruikers kunnen deze repository nog te makkelijk zien als engine-roadmap of engine-implementatielaag.
- Why it matters: deze repo moet vooral duidelijk maken wat hij van de engine verwacht en wat hij lokaal valideert.
- Priority: medium
- Estimated scope: small
- Dependency: none
- Recommendation: implement now

## Recommended implementation order

1. Engine-template contract in the engine.
2. Automatic figure/table numbering and cross-references breder toetsen.
3. Authoring guide en Hanze starterprofiel breder toetsen.
4. Verdere beeldplaatsing en afbeeldingsworkflow.
5. Mermaid- en diagramworkflow formaliseren.
6. Verdere templatepolish en regressiechecks.

## Why this order is best

De structurele basis is nu aanwezig, dus de kritieke vraag is niet meer of de engine zones, TOC of bibliografie kan plaatsen, maar of engine en template een stabiel en authorable contract vormen. De metadata-, image- en engine-managed Mermaid-baselines maken die consumerkant al zichtbaar, maar automatische nummering en cross-references zijn nu de duidelijkste vervolgstap richting een volwassener rapportworkflow.

Daarna is het logisch om de auteursworkflow expliciet te maken, zodat nieuwe demo’s en echte use cases niet terugvallen op oude workarounds. Beeld- en diagramworkflow komen vervolgens omdat juist daar in realistische rapporten snel nieuwe incidentele handelingen insluipen. Templatepolish en regressiechecks blijven belangrijk, maar renderen pas echt goed als authoring, mediaworkflow en referentiegedrag eerst duidelijk zijn.
