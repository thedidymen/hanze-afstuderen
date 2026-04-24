# Post-Structure Review

Deze review kijkt naar de huidige staat van de Hanze demo-repository nadat metadata, document zones, appendices, bibliografieplaatsing en TOC-plaatsing zijn gemigreerd naar first-class Docsmith-concepten.

Bronnen voor deze review:

- de huidige repository-inhoud
- de huidige template in [template.tex](/Users/reijer/Repo/docsmith-demo/templates/hanze_thesis/template.tex)
- de huidige documentconfiguratie in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/spec.yaml)
- de recent geassembleerde output in [combined.md](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/build/combined.md)
- de succesvolle PDF-build

Opmerking:

- de lokale omgeving bevat geen `pdfinfo`, `pdftotext`, `mutool`, `qpdf` of `gs`, dus deze review gebruikt de build-output vooral via `combined.md` en de template, niet via directe tekstextractie uit de PDF

## Status update

Sinds deze review zijn de structurele cleanupstappen verder afgerond:

- de demo gebruikt de Docsmith-engine nu als schone consumer voor metadata, documentzones, appendices, bibliografieplaatsing en ordered TOC placement
- de oude Lua-gebaseerde TOC/document-structure-workaround geldt als verwijderd en obsoleet
- de front-matter-volgorde is nu structureel juist via `document.front_matter`, zonder lokale documentreordering
- rijkere titelpagina- en omslagmetadata worden nu ook echt gebruikt in de demo-template
- image handling heeft nu een baseline en Mermaid-rendering is nu engine-managed via gedeclareerde diagrammen
- ontbrekende tabelcaptions in de huidige demo zijn toegevoegd

De resterende aandachtspunten in dit document moeten daarom gelezen worden als template-, metadata- en workflowwerk, niet meer als fundamentele structurele blockers. De grootste open punten zitten nu in automatische cross-references, authoring guidance en verdere media-/templatepolish.

## 1. Remaining template/layout weaknesses

- De front-matter-volgorde is structureel correct in de geassembleerde output: `voorwoord -> samenvatting -> inhoudsopgave`. De resterende vraag is nu vooral visuele polish, niet plaatsing.
- De overgang van front matter naar hoofdtekst wordt template-side afgehandeld. In [template.tex](/Users/reijer/Repo/docsmith-demo/templates/hanze_thesis/template.tex) schakelt het eerste genummerde hoofdstuk naar Arabische paginanummering en start op pagina 1. Dat verdient hoogstens nog PDF-nacontrole, geen structurele herziening.
- De template gebruikt nog een vrij eenvoudige paginastijl. De running head toont nu alleen het actuele hoofdstuk en het paginanummer, maar verdere typografische verfijning kan nog wenselijk zijn.
- De titelpagina en omslag zijn duidelijk, maar nog vrij generiek. Ze ogen netjes, maar nog niet op het niveau van een echt afstudeerverslag met rijkere metadata, duidelijkere rolverdeling en sterkere informatiehiërarchie.
- De bibliografie wordt nu structureel geplaatst, maar de visuele opmaak blijft nog vrij basaal. Voor langere literatuurlijsten met URL’s, meerdere auteurs of verschillende bronsoorten is dat waarschijnlijk nog niet professioneel genoeg.
- De appendix werkt nu structureel goed, maar de visuele overgang naar de bijlagen is nog beperkt. Er is geen duidelijke appendix-intropagina of extra visuele scheiding tussen rapport en ondersteunend materiaal.
- Tabel- en figuurpresentatie is functioneel, maar nog niet overtuigend voor een langer rapport. Er zijn nog geen expliciete keuzes zichtbaar voor uitgebreidere captions, longtable-gedrag of lijsten van figuren/tabellen.

## 2. Remaining metadata/template issues

- De demo gebruikt nu een rijkere metadata-set in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/spec.yaml), maar die is nog maar op één compacte demo-variant beproefd. De vraag is nu vooral hoe breed en stabiel dat consumer-contract in de praktijk wordt.
- De template hard-codeert nog steeds waarden zoals `Hanzehogeschool Groningen`, `HBO-ICT` en `Verantwoordingsverslag` in [template.tex](/Users/reijer/Repo/docsmith-demo/templates/hanze_thesis/template.tex). Dat maakt de template minder flexibel dan de engine nu toelaat.
- Belangrijke verantwoordingsverslagvelden kunnen nu op de titelpagina verschijnen, maar de demo test nog niet breed genoeg of die metadataflow ook prettig authorable blijft in meerdere varianten.
- De demo oefent het engine-template contract voor rijkere metadata nu functioneel uit, maar nog niet onder zwaardere of alternatieve rapportprofielen.
- Er is nog geen onderscheid tussen een korte titel voor headers en de volledige titel voor omslag/titelpagina.

## 3. Remaining workflow/authoring issues

- Er is nog geen echte auteurservaring voor een student of begeleider. De demo is leesbaar als voorbeeld, maar nog geen sterk starterpakket voor een echt verantwoordingsverslag.
- De repo bevat nog maar één hoofdvoorbeeld. Daardoor is regressietesten op alternatieve rapportvormen of meerdere appendix-/bibliografievarianten beperkt.
- Er is nog geen reviewchecklist voor begeleiders of auteurs met punten als front-matter-volgorde, hoofdstuknamen, metadata-volledigheid en bijlagekwaliteit.
- Er is nog geen praktische guidance voor het invullen van rijkere metadata, ondanks dat de engine hier nu beter op voorbereid is.
- De demoinhoud is geloofwaardig, maar nog vrij compact. Voor echte afstudeergevoeligheid ontbreken nog lastiger cases zoals meerdere bijlagen, meer referenties en meer complexe tabellen.

## 4. Remaining documentation issues

- De README zegt terecht dat de grote structurele workarounds zijn gesloten. Wat nog ontbreekt is vooral bredere toetsing en aanscherping van de nu aanwezige auteurgerichte guidance voor rijkere metadata en realistischer vervolggebruik.
- De template-README noemt first-class support, maar zegt nog weinig over welke metadata de template idealiter zou gebruiken zodra deze repo die daadwerkelijk gaat invullen.
- Er is nu wel een authoring guide en compact starterprofiel, maar die instaproute is nog niet breed genoeg beproefd als echte auteursworkflow.
- De documentatie maakt nog niet scherp genoeg onderscheid tussen:
  - wat nu technisch ondersteund is
  - wat nu presentabel genoeg is
  - wat nog onvoldoende professioneel is voor echt thesis-gebruik

## 5. Things that are already good enough

- De scheiding tussen engine en consumer repository is nu helder in README, backlog en agent guidance.
- De demo gebruikt de nieuwe engineconcepten nu correct voor metadata-doorgifte, document zones, bibliografie, appendices en TOC-plaatsing.
- De documentstructuur voelt inhoudelijk als een geloofwaardig compact verantwoordingsverslag.
- De template heeft een duidelijke omslag en aparte titelpagina, wat al veel professioneler is dan een standaard Pandoc-output.
- De appendix wordt nu structureel correct als appendix behandeld in plaats van als willekeurige back-matter-sectie.
- De handmatige structurele workaround-lus is grotendeels gesloten. Dat is een grote verbetering ten opzichte van de eerdere staat.
- De repo is goed genoeg als validatieomgeving en real-world test case voor de Docsmith-engine.

## 6. Recommended next 5 improvements

### 1. Broaden and test the current automatic figure/table numbering and cross-references

- Why it matters: de basis is nu aanwezig, maar zonder bredere toetsing blijft onduidelijk hoe robuust de huidige nummering en verwijzingen zijn in rijkere rapportvarianten.
- Classification: template/workflow work
- Priority: high

### 2. Broaden and test the new authoring starter profile

- Why it matters: de repo heeft nu een starterprofiel en authoring guide, maar die instapworkflow is nog niet breed genoeg beproefd als echte auteursbasis.
- Classification: document/workflow work
- Priority: medium

### 3. Formalize the Mermaid workflow

- Why it matters: de engine-managed baseline werkt nu, maar bredere toetsing, dependencyduiding en later CI-/enginebeleid vragen nog vervolgwerk.
- Classification: document/workflow work
- Priority: medium

### 4. Expand image controls beyond the current baseline

- Why it matters: sizing werkt nu beter, maar cropping, complexere layout en rijkere plaatsingscontrole ontbreken nog.
- Classification: template work
- Priority: medium

### 5. Add a lightweight review checklist for structure conventions

- Why it matters: de structuur is nu grotendeels declaratief, maar reviewers hebben nog geen korte checklist voor punten als metadata-volledigheid, front matter en appendixkwaliteit.
- Classification: document/workflow work
- Priority: medium
