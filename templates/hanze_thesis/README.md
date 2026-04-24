# hanze_thesis

Lokale Hanze/HBO-ICT-template voor deze demo-repository. Deze template is nadrukkelijk niet generiek: hij ondersteunt de look-and-feel en documentvolgorde van een compact verantwoordingsverslag zoals je dat in een Hanze-context zou verwachten.

De template richt zich vooral op:

- een duidelijk verschil tussen `omslag` en `titelpagina`
- front matter vóór hoofdstuk 1, met voorwoord, samenvatting en inhoudsopgave
- hoofdstukopbouw die past bij een jaar-4 verantwoordingsverslag
- nette presentatie van literatuurlijst en bijlagen
- een professionele, rustige PDF-opmaak voor demo- en validatiedoeleinden

De implementatie blijft bewust pragmatisch. Er is geen Hanze-logica in de Docsmith-engine toegevoegd; alle Hanze-specifieke keuzes zitten lokaal in deze repository.

Deze template wordt nu gebruikt in combinatie met het minimale document-zone-model van de engine:

- `front_matter`
- `main_matter`
- `back_matter`
- `appendices`

In deze demo/workflowcombinatie gebruiken inhoudsopgave, bibliografie en appendices nu first-class engine support. Daarmee is de hoofdloop van handmatige structurele workarounds voor dit verantwoordingsverslagprofiel gesloten.

Deze template hoort uiteindelijk verantwoordelijk te zijn voor:

- titelpagina
- front matter-layout
- structurele rendering van de door de engine aangeleverde documentstructuur
- running heads voor front matter
- pagineringsovergang tussen front matter en hoofdtekst

Documenten in `documents/` horen die layout niet zelf via LaTeX te sturen. Markdown-secties moeten dus naar een content-only model bewegen.

Huidige front-matterconventie:

- authored front-matterbestanden gebruiken een normale top-level Markdown-heading met `.unnumbered`
- Pandoc vertaalt dat naar een ongenummerde hoofdstukkop met TOC-opname
- de template zet voor zulke ongenummerde hoofdstukken zelf de running head, zodat `\markboth` niet meer in content nodig is
- de inhoudsopgave komt nu als first-class generated item uit de engine in de juiste volgorde van `document.front_matter`
- de TOC gebruikt in deze demo `numbered: false` en `listed: false`, zodat `Inleiding` hoofdstuk 1 blijft en de inhoudsopgave niet in zichzelf wordt opgenomen
- front matter gebruikt `plain` paginastijl met Romeinse nummering; de template schakelt bij het eerste genummerde hoofdstuk over naar Arabische nummering voor de hoofdtekst

Overige templateconventies:

- running heads tonen alleen het actuele hoofdstuk en het paginanummer, zodat lange documenttitels niet botsen in de header
- cover en titelpagina gebruiken optioneel een logo via metadata of bekende assetpaden, maar running headers blijven logovrij
- cover en titelpagina ondersteunen nu expliciet rijkere metadata zoals `student_number`, `programme`, `institution`, `document_type`, `location`, `supervisor`, `second_reviewer`, `client`, `project_context`, `academic_year`, `cohort` en optioneel `short_title`
- afbeeldingen worden template-side automatisch begrensd op de beschikbare breedte en op een veilige maximale hoogte, met behoud van aspect ratio
- figuurcaptions staan onder figuren en worden klein, leesbaar en consistent gecentreerd gezet
- tabelcaptions staan boven tabellen en blijven compact en goed scanbaar
- floatgedrag is getuned om onnodige floatpagina’s te verminderen en hoofdstukgrenzen beter te respecteren
- er is geen lokale Pandoc-structuurfilter of andere template-side structurele reordering meer nodig voor TOC-volgorde of documentzone-reordering

Daarmee bevatten de authored Markdown-secties in deze demo geen raw LaTeX meer voor front matter.

## Metadata support

De template verwacht minimaal:

- `title`
- `author`
- `date`

Daarnaast kan de template, wanneer beschikbaar, deze velden op cover en titelpagina tonen:

- `short_title`
- `student_number`
- `programme`
- `institution`
- `document_type`
- `location`
- `supervisor`
- `second_reviewer`
- `client`
- `project_context`
- `academic_year`
- `cohort`

Compatibiliteitsfouten worden waar mogelijk vermeden met fallbacks:

- `programme` of `program`
- `student_number` of `student_id`
- `second_reviewer` of `second_reader`

Deze uitbreiding is bewust consumer-side: de repository laat hiermee zien hoe een lokale thesis-template rijkere engine-metadata benut zonder enginecode te wijzigen of authored Markdown met LaTeX te vervuilen.

## Image handling

Aanbevolen authoringpatroon:

- basisvorm: `![Beschrijving](assets/images/bestand.png)`
- met expliciete breedte: `![Beschrijving](assets/images/bestand.png){ width=80% }`

Richtlijnen:

- gebruik gewone Markdown image syntax
- gebruik Pandoc-attributen voor sizing, niet raw LaTeX
- gebruik bij voorkeur percentage-based breedtes voor gewone figuren in lopende tekst
- laat `width` weg als de natuurlijke maat al passend is; de template voorkomt overflow automatisch

Beperkingen:

- cropping wordt nog niet ondersteund
- er is nog geen geavanceerde beeldlayout voor meerdere afbeeldingen naast elkaar
- Mermaid-diagrammen worden in deze repo niet template-side verwerkt; ze moeten eerst naar gewone image assets zoals `.png` worden gerenderd

## Table handling

Aanbevolen authoringpatroon:

```md
| Kolom | Waarde |
| --- | --- |
| R1 | Moet |

Table: Korte en professionele tabelcaption.
```

Conventie in deze template:

- tabelcaptions worden via Pandoc Markdown aangeleverd met een `Table:`-regel
- tabelcaptions renderen boven de tabel
- figuurcaptions renderen onder de figuur

## Mermaid workflow status

In deze repository geldt momenteel:

- `.mmd` Mermaid-bestanden zijn authored documentbron en horen committed te blijven
- gegenereerde `.png` diagrammen zijn conceptueel build artifacts van die bronbestanden
- voor deze demo mogen die gegenereerde assets nog steeds committed blijven, zodat review en PDF-builds niet afhankelijk zijn van een lokale Mermaid-installatie

Gewenste latere richting:

- een engine-supported diagramworkflow in Docsmith
- of een formeel gedocumenteerde pre-build stap in de Docsmith-workflow

Bestanden:

- `defaults.yaml`: Pandoc-defaults voor hoofdstukindeling, marges en bibliografie
- `template.tex`: lokale LaTeX-opmaak met omslag, titelpagina en hoofdstukstyling
- `metadata.yaml`: aanvullende vaste metadata zoals documenttaal
