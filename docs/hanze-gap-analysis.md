# Hanze Verantwoordingsverslag Gap Analysis

Deze analyse vergelijkt:

1. de huidige Docsmith-engine in `../docsmith`
2. de huidige lokale Hanze-template en demo in deze repository
3. de verwachtingen die in deze demo-opdracht al zijn samengevat voor een jaar-4 verantwoordingsverslag

Beoordelingsbasis:

- de huidige engine is een werkende MVP voor versiegestuurde PDF-builds uit geordende Markdown
- de lokale `hanze_thesis` template maakt de PDF visueel bruikbaarder
- de Hanze-/HBO-ICT-expectaties die hier relevant zijn, zijn vooral structureel en workflowgericht:
  omslag, titelpagina, front matter, hoofdstuk 1 als inleiding, nette literatuurlijst, duidelijke bijlagen en een professionele rapportagevorm

Deze analyse gebruikt dus de nu bekende verwachtingen uit de demo-context. Het is geen letterlijke toetsing tegen een volledige Hanze-handleidingtekst.

## 1. Already well supported

- Expliciete documentvolgorde is goed ondersteund via het zone-model in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/spec.yaml). Voor een verantwoordingsverslag is vaste hoofdstukvolgorde belangrijk; Docsmith kan die nu betrouwbaar afdwingen via `front_matter`, `main_matter`, `back_matter` en `appendices`.
- Lokale template-separatie is goed ondersteund via `project.template`. Dat past goed bij deze use case, omdat Hanze-specifieke opmaak in de documentrepo hoort en niet in de engine.
- PDF-builds met citaties, bibliografie-assets en lokale afbeeldingen werken. Voor een verantwoordingsverslag is dat de minimale productieketen; die is aanwezig.
- Basisvalidatie is al bruikbaar. `docsmith validate` controleert of `spec.yaml`, bronbestanden, templatepad, CSL/bibliografie en outputlocatie kloppen.
- Appendix-omschakeling en appendixplaatsing worden nu structureel uit de engine aangestuurd via `document.appendices`.
- Versiegestuurde outputnamen en build-artifacts zijn al aanwezig. Voor reviewrondes in een afstudeercontext is dat praktisch bruikbaar.
- De huidige demo-structuur is inhoudelijk al geloofwaardig genoeg als compacte testset: voorwoord, samenvatting, inleiding, kernhoofdstukken, conclusie/aanbevelingen, literatuurlijst en bijlage zijn aanwezig.
- TOC-plaatsing en bibliografieplaatsing zijn nu first-class ondersteund in deze repo/workflow: de inhoudsopgave staat als generated item in `document.front_matter` en de literatuurlijst via `document.bibliography` in `back_matter`.

## 2. Partially supported but fragile

- Front matter is nu content-only authored met gewone Markdown-headings en `.unnumbered`, maar de uiteindelijke presentatie blijft nog sterk afhankelijk van templategedrag. Dat is beter dan authored LaTeX, maar nog niet volledig uitontwikkeld als generieke thesis-workflow.
- De inhoudsopgave staat nu structureel correct via ordered generated `front_matter`, maar de template houdt `toc: false` in de Pandoc-defaults om dubbele automatische insertie te voorkomen. Die combinatie is functioneel correct, maar vraagt discipline in template en enginecontract.
- De literatuurlijst wordt nu declaratief geplaatst via `document.bibliography`, maar de visuele uitwerking blijft nog vrij basic voor langere of complexere bronlijsten.
- Appendixpresentatie is nog steeds deels templateafhankelijk. De structuur is first-class, maar zaken als visuele scheiding, appendix-intropagina of uitgebreidere appendixstyling zijn nog niet uitgewerkt.
- Omslag en titelpagina zijn visueel gescheiden, maar de inhoud daarop is deels hard-coded in de template in plaats van gestuurd door documentmetadata. Daardoor werkt deze demo, maar niet als herbruikbare workflow voor echte studenten.
- De template buildt nu, maar eerdere iteraties liepen vast op ontbrekende LaTeX-pakketten en fontconfiguratie. Dat laat zien dat de template nog gevoelig is voor lokale TeX-omgevingen.
- Bibliografie-output is acceptabel, maar nog niet aantoonbaar robuust voor langere literatuurlijsten, veel auteurs, URL’s en typische afstudeerrapport-bronnen.

## 3. Missing features in Docsmith

### 3.1 Uitbreidbare metadata voor templates

- Wat ontbreekt: de engine accepteert in `metadata` alleen `title`, `subtitle`, `author` en `date` in [config.py](/Users/reijer/Repo/docsmith-demo/../docsmith/src/docsmith/config.py). Velden zoals studentnummer, opleiding, opdrachtgever, begeleider, tweede beoordelaar of logo-pad kunnen niet declaratief worden meegegeven.
- Waarom dit belangrijk is: een verantwoordingsverslag heeft bijna altijd rijkere titelpagina- en covermetadata dan alleen titel en auteur.
- Hoort thuis in: Docsmith engine.
- Prioriteit: high.

### 3.2 First-class appendix sections

- Wat ontbreekt: appendices zijn nu alleen een tekstmarker die naar `\appendix` wordt vervangen in [assembler.py](/Users/reijer/Repo/docsmith-demo/../docsmith/src/docsmith/core/assembler.py). Er is geen concept van meerdere bijlagen, appendixlabels of appendix-validatie.
- Waarom dit belangrijk is: een verantwoordingsverslag gebruikt bijlagen vaak intensief. Dan moet het systeem duidelijk kunnen omgaan met meerdere bijlagen en consistente labeling.
- Hoort thuis in: Docsmith engine.
- Prioriteit: high.

### 3.3 Template metadata and partial support are not really wired into rendering

- Wat ontbreekt: templatebestanden zoals `metadata.yaml` en scaffolded partials bestaan, maar de engine gebruikt ze niet als formeel mechanisme. De renderflow schrijft alleen runtime metadata uit [metadata.py](/Users/reijer/Repo/docsmith-demo/../docsmith/src/docsmith/renderer/metadata.py).
- Waarom dit belangrijk is: voor echte thesis-workflows wil je templatepacks declaratief kunnen voeden zonder sectiebestanden vol LaTeX-hacks.
- Hoort thuis in: Docsmith engine.
- Prioriteit: high.

### 3.4 Validatie van documentstructuur op profielniveau

- Wat ontbreekt: `docsmith validate` controleert vooral technische aanwezigheid, niet of hoofdstuk 1 de inleiding is, of front matter echt voorin staat, of de literatuurlijst vóór bijlagen komt.
- Waarom dit belangrijk is: een verantwoordingsverslag faalt in de praktijk vaker op structuurdiscipline dan op ontbrekende bestanden.
- Hoort thuis in: Docsmith engine.
- Prioriteit: medium.

### 3.5 Betere machine-readable build output / manifest

- Wat ontbreekt: de CLI print statusregels, maar er is geen manifest van buildresultaten, gebruikte metadata, outputbestand en versie.
- Waarom dit belangrijk is: voor begeleidings- of reviewworkflows is het nuttig om builds geautomatiseerd te kunnen controleren of publiceren.
- Hoort thuis in: Docsmith engine.
- Prioriteit: medium.

### 3.6 Real DOCX and multi-format support

- Wat ontbreekt: de config laat `docx` toe, maar de buildflow produceert alleen PDF. Dat staat ook expliciet als beperking in de engine-README.
- Waarom dit belangrijk is: voor echte afstudeertrajecten is PDF meestal genoeg voor beoordeling, maar DOCX of extra exportvormen kunnen later alsnog relevant worden voor feedback of aanlevering.
- Hoort thuis in: Docsmith engine.
- Prioriteit: low.

### 3.7 Echte end-to-end rendering tests met Pandoc/LaTeX

- Wat ontbreekt: de engine heeft veel logische tests, maar geen sterke end-to-end garantie dat echte templates op een realistische toolchain blijven renderen.
- Waarom dit belangrijk is: juist thesis-templates zijn gevoelig voor regressies in citeproc, LaTeX-pakketten en template-aanpassingen.
- Hoort thuis in: Docsmith engine.
- Prioriteit: medium.

## 4. Missing features in the local Hanze template

### 4.1 Declaratieve titelpagina-invulling

- Wat ontbreekt: de template in [template.tex](/Users/reijer/Repo/docsmith-demo/templates/hanze_thesis/template.tex) kan al velden zoals studentnummer, begeleider, opdrachtgever, tweede beoordelaar en locatie lezen, maar de demo vult die metadata nog nauwelijks in en oefent het contract daardoor beperkt.
- Waarom dit belangrijk is: dat zijn typische verantwoordingsverslag-gegevens en ze horen niet hard-coded of handmatig in LaTeX te staan.
- Hoort thuis in: lokale Hanze template en demo-configuratie.
- Prioriteit: high.

### 4.2 Minder hard-coded Hanze-context

- Wat ontbreekt: waarden als `Hanzehogeschool Groningen`, `HBO-ICT` en `Verantwoordingsverslag` staan nu letterlijk in de template.
- Waarom dit belangrijk is: voor deze repo is Hanze-specificiteit prima, maar zelfs binnen deze repo wil je nog kunnen variëren tussen opleidingen, documenttypen of toekomstige demo’s zonder templatecode te herschrijven.
- Hoort thuis in: lokale Hanze template.
- Prioriteit: medium.

### 4.3 Sterkere appendix-opmaak

- Wat ontbreekt: appendices zijn duidelijker dan eerder, maar er is nog geen extra appendix-intropagina, appendix-specifieke kopstijl of visuele scheiding tussen hoofdtekst en bijlagen.
- Waarom dit belangrijk is: in een verantwoordingsverslag moeten bijlagen direct herkenbaar zijn als ondersteunend materiaal en niet als doorlopend hoofdstuk.
- Hoort thuis in: lokale Hanze template.
- Prioriteit: medium.

### 4.4 Professionelere literatuurlijst-opmaak

- Wat ontbreekt: de bibliografie gebruikt nu de generieke CSL/Pandoc-output zonder extra templatepolish zoals consequente hanging indent-afstemming, compacte spacing-tuning of betere lange-URL-afhandeling.
- Waarom dit belangrijk is: de literatuurlijst is in een afstudeerrapport een opvallend kwaliteitskenmerk.
- Hoort thuis in: lokale Hanze template.
- Prioriteit: medium.

### 4.5 Betere figuur- en tabelpresentatie voor langere rapporten

- Wat ontbreekt: de basis werkt, maar de template heeft nog geen expliciete keuzes voor caption spacing, doorlopende longtables, tabeluitlijning of lijst van figuren/tabellen.
- Waarom dit belangrijk is: in een echte thesis groeien figuren en tabellen snel uit tot terugkerende structuurelementen.
- Hoort thuis in: lokale Hanze template.
- Prioriteit: medium.

### 4.6 Header/footer tuning voor langere titels en meerdere hoofdstukken

- Wat ontbreekt: de huidige header gebruikt rechts de volledige documenttitel. Dat kan bij lange rapporttitels snel onrustig worden.
- Waarom dit belangrijk is: professionele thesis-PDF’s hebben meestal rustige running heads die ook bij lange documenten prettig leesbaar blijven.
- Hoort thuis in: lokale Hanze template.
- Prioriteit: low.

## 5. Missing authoring/documentation/workflow support

### 5.1 Schrijfrichtlijnen voor auteurs zonder LaTeX in Markdown

- Wat ontbreekt: er is nog geen repo-documentatie die de huidige content-only Markdownworkflow kort en auteurgericht uitlegt.
- Waarom dit belangrijk is: een werkbare verantwoordingsverslagflow moet haalbaar zijn voor studenten die vooral Markdown schrijven, niet voor templatebouwers.
- Hoort thuis in: document repo/workflow.
- Prioriteit: high.

### 5.2 Een expliciet Hanze authoring-profiel of starterdocument

- Wat ontbreekt: de repo heeft een demo, maar nog geen "zo start je een echt verantwoordingsverslag" pakket met aanbevolen hoofdstukvolgorde, naamgeving, placeholders en minimale invulinstructies.
- Waarom dit belangrijk is: een demo is nog geen bruikbare auteursworkflow.
- Hoort thuis in: document repo/workflow.
- Prioriteit: high.

### 5.3 Duidelijke scheiding tussen demo-inhoud en real-thesis-gebruik

- Wat ontbreekt: de README beschrijft de demo goed, maar nog niet concreet genoeg welke delen productieachtig zijn en welke vooral demonstratief of nog layout-light zijn.
- Waarom dit belangrijk is: anders lijkt de workflow volwassener dan hij nu feitelijk is.
- Hoort thuis in: document repo/workflow.
- Prioriteit: medium.

### 5.4 Reviewchecklist voor structuurconventies

- Wat ontbreekt: er is geen praktische checklist voor reviewers of auteurs met punten als "staat de inhoudsopgave op de juiste plek", "begint hoofdstuk 1 met Inleiding", "staan bijlagen na de literatuurlijst".
- Waarom dit belangrijk is: dit soort rapporten worden vaak op conventies beoordeeld die buiten pure build-validatie vallen.
- Hoort thuis in: document repo/workflow.
- Prioriteit: medium.

### 5.5 Workflow voor herbruikbare Hanze-template-updates

- Wat ontbreekt: er is geen afgesproken manier om wijzigingen in de Hanze-template te testen tegen meerdere voorbeeldrapporten of meerdere varianten van dezelfde structuur.
- Waarom dit belangrijk is: zodra de template realistischer wordt, groeit de kans op regressies in front matter, bibliografie en appendices.
- Hoort thuis in: document repo/workflow.
- Prioriteit: medium.

### 5.6 Documentatie over huidige enginebeperkingen

- Wat ontbreekt: er is nog geen korte expliciete lijst in deze repo van de resterende echte beperkingen, zoals beperkte profielvalidatie, beperkte metadata-invulling en nog vrij basic templatepolish.
- Waarom dit belangrijk is: dat voorkomt verkeerde verwachtingen en helpt prioriteren wat naar de engine terug moet.
- Hoort thuis in: document repo/workflow.
- Prioriteit: medium.

## 6. Nice-to-have improvements that are not required yet

- Meerdere templateprofielen binnen dezelfde Hanze-demo, bijvoorbeeld `compact_verantwoordingsverslag` en `volledig_verantwoordingsverslag`. Dit is nuttig, maar nog niet nodig zolang de basisworkflow niet first-class is.
- Automatische lijst van figuren en lijst van tabellen. Voor langere scripties nuttig, maar niet essentieel voor deze MVP-use case.
- Structured cross-references voor figuren, tabellen en bijlagen. Praktisch voor grote rapporten, maar niet de eerste blocker.
- Meer semantische versioning-logica dan alleen patch-bumps bij elke inhoudswijziging. Handig, maar geen kernvereiste voor thesis-authoring.
- JSON-output van `docsmith validate` en `docsmith build`. Handig voor CI, niet nodig om deze use case eerst geloofwaardig te maken.
- Template inheritance/composition. Dat zou templatebeheer eleganter maken, maar is niet nodig voor een eerste realistische Hanze-workflow.

## Minimum remaining work before this is realistic enough for real thesis use

De minimale resterende set is kleiner dan een volledige engine-herbouw, maar groter dan alleen "nog wat templatepolish".

### Absoluut nodig

- Docsmith moet uitbreidbare template-metadata ondersteunen.
- De Hanze-demo moet rijkere metadata daadwerkelijk invullen en zichtbaar testen op titelpagina en omslag.
- De repo moet een auteursworkflow documenteren die de huidige content-only Markdownaanpak expliciet maakt.

### Sterk aanbevolen voordat echte studenten ermee gaan werken

- `docsmith validate` moet ten minste optioneel structuurregels kunnen controleren voor dit documentprofiel.
- De Hanze-template moet sterker worden getest op bibliografie, meerdere bijlagen en langere figuur-/tabelrijke documenten.
- De repo moet een expliciet starterprofiel of voorbeeldpakket bevatten voor een echt verantwoordingsverslag, niet alleen een demo.

### Conclusie

De huidige situatie is goed genoeg als demonstrator van haalbaarheid en laat nu ook first-class ondersteuning zien voor front matter, inhoudsopgaveplaatsing en bibliografieplaatsing. Ze is nog niet goed genoeg als volledig geloofwaardige, herhaalbare thesis-workflow voor echte studenten. De grootste resterende gaten zitten nu vooral in metadata-invulling, profielvalidatie, appendixverfijning en verdere templatepolish.
