# docsmith-hanze-demo

Deze repository is een zelfstandige demo/test-repository voor Docsmith. De inhoud bootst een Hanze/HBO-ICT-afstudeerworkflow na, maar is nadrukkelijk geen definitief verantwoordingsverslag of productierepository.

De repository is bedoeld om Docsmith te valideren op een realistische documentstructuur met:

- een lokale Hanze-specifieke template voor een verantwoordingsverslag
- geordende hoofdstukken en front matter
- metadata voor omslag en titelpagina
- citaties en bibliografie
- figuren en tabellen
- een bijlage
- versiegestuurde PDF-output

## Structuur

- `templates/hanze_thesis/`: lokale template voor deze demo
- `documents/verantwoordingsverslag/`: voorbeeld van een compact HBO-ICT-verantwoordingsverslag
- `documents/hanze-starter-verantwoordingsverslag/`: compacte startervariant voor nieuwe auteurs
- `notes/`: ruimte voor losse notities of testnotities

## Relationship with Docsmith

Deze repository gebruikt de Docsmith-engine, maar ontwikkelt die engine niet zelf. Engineontwikkeling gebeurt in een aparte repository. Deze repository fungeert als:

- validatieomgeving
- voorbeeldimplementatie
- real-world test case

De rol van deze repository is dus vooral om te laten zien wat de engine moet ondersteunen, niet om enginegedrag lokaal te simuleren.

## Waar deze demo op mikt

De lokale template en het voorbeeldrapport zijn niet neutraal. Ze proberen juist een geloofwaardige Hanze/HBO-ICT-opmaak en documentvolgorde te benaderen, met onder meer:

- een aparte omslag en titelpagina
- voorwoord en samenvatting vóór hoofdstuk 1
- een inhoudsopgave in de front matter
- `Hoofdstuk 1: Inleiding`
- kernhoofdstukken voor context, requirements, ontwerp, realisatie en validatie
- een literatuurlijst vóór de bijlagen
- duidelijk gelabelde bijlagen

De Docsmith-engine zelf blijft generiek. Hanze-specifieke keuzes zitten alleen in deze repository.

## Document Zones

Het demo-document gebruikt nu het minimale zone-model van de Docsmith-engine:

- `front_matter`
- `main_matter`
- `back_matter`
- `appendices`

Voor deze demo betekent dat:

- `front_matter`: voorwoord, samenvatting en daarna een engine-geplaatste inhoudsopgave als ordered generated item
- `main_matter`: inleiding en kernhoofdstukken
- `back_matter`: declaratief geplaatste literatuurlijst via `document.bibliography`
- `appendices`: bijlagen

De handmatige workaround-secties voor inhoudsopgave en literatuurlijst zijn hiermee uit de actieve documentstructuur verwijderd. TOC-plaatsing, bibliografieplaatsing en appendices gebruiken nu first-class engine support. De inhoudsopgavepositie wordt nu volledig engine-driven bepaald via de geordende `front_matter`-lijst; er draait geen lokale Lua-structuurfilter meer mee voor de documentvolgorde.

## Metadata Contract In This Demo

De Hanze-template gebruikt nu explicieter het engine-template contract door meer thesis-/rapportmetadata rechtstreeks uit `documents/verantwoordingsverslag/spec.yaml` te lezen.

Velden die in deze demo worden ingevuld:

- vereist in de praktijk voor een bruikbare titelpagina: `title`, `author`, `date`
- ondersteund en nu gebruikt in deze demo: `short_title`, `student_number`, `programme`, `institution`, `document_type`, `location`, `supervisor`, `second_reviewer`, `client`, `project_context`, `academic_year`, `cohort`
- optioneel voor logo’s: `logo_path`, `cover_logo_path`, `title_logo_path`

De template houdt veilige fallbacks:

- `programme` valt terug op `program`
- `student_number` valt terug op `student_id`
- `second_reviewer` valt terug op `second_reader`
- `institution`, `programme` en `document_type` hebben nog lokale standaardwaarden zodat minimale demo-documenten blijven builden

Hiermee valideert deze repository niet alleen documentstructuur, maar ook explicieter dat consumer-metadata netjes en declaratief doorloopt naar cover en titelpagina.

## Authoring Principles

Voor deze repository geldt voortaan expliciet:

- Markdown is voor inhoud, niet voor layout.
- Documentsecties horen geen LaTeX te bevatten voor titelpagina, front matter-layout of structurele rendering.
- Layout is verantwoordelijkheid van template + metadata.
- Front-matter-secties gebruiken gewone Markdown-headings met `.unnumbered`; de template verzorgt de ongenummerde rendering en running heads.
- Front matter gebruikt Romeinse paginanummers; hoofdstuk 1 start opnieuw op Arabische paginanummering.
- De TOC staat in `document.front_matter` als generated item met `numbered: false` en `listed: false`, zodat zij na de samenvatting staat, niet als hoofdstuk 1 telt en niet in zichzelf verschijnt.
- Deze repository vertrouwt daarmee volledig op ordered generated zone items uit Docsmith voor TOC-plaatsing; er is geen template-side structurele reordering meer.
- De resterende LaTeX in de build-pipeline zit in template- of engine-gegeneerde output, niet meer in authored Markdown-content.

## Image Conventions

Afbeeldingen worden in deze repo author-friendly gehouden:

- gebruik standaard Markdown-images: `![Beschrijving](assets/images/bestand.png)`
- gebruik Pandoc-attributen voor breedte wanneer een expliciete maat gewenst is: `![Beschrijving](assets/images/bestand.png){ width=80% }`
- gebruik bij voorkeur percentage-based breedtes voor gewone figuren in de lopende tekst

Aanbevolen patroon:

- `width=70%` tot `width=85%` voor normale illustraties of screenshots
- laat `width` weg als de natuurlijke afmeting al geschikt is; de template begrenst afbeeldingen automatisch op de beschikbare breedte
- houd captions kort en beschrijvend in de alt-tekst

Templategedrag:

- afbeeldingen kunnen niet buiten de beschikbare tekstbreedte renderen
- te hoge afbeeldingen worden ook in hoogte begrensd met behoud van aspect ratio
- figuren gebruiken captions onder de afbeelding, met consistente centrering
- tabellen gebruiken captions boven de tabel, met een compacte en leesbare stijl
- floats worden minder agressief naar aparte pagina’s geduwd en blijven niet over hoofdstukgrenzen heen hangen

Huidige beperking:

- cropping of complexe beeldcomposities worden nog niet ondersteund; stuur dat dus niet vanuit Markdown aan

## Table Conventions

Voor tabellen gebruikt deze repo gewone Pandoc Markdown-tabellen, met een caption direct onder de tabel:

```md
| Kolom | Waarde |
| --- | --- |
| R1 | Moet |

Table: Korte en professionele tabelcaption.
```

Afspraak:

- houd tabelcaptions kort en zakelijk
- gebruik de `Table:`-regel direct onder de tabel
- figuurcaptions horen in de alt-tekst van de afbeelding en renderen onder de figuur
- tabelcaptions renderen in de PDF boven de tabel; figuurcaptions renderen onder de figuur

## Mermaid Diagram Workflow

Voor diagrammen gebruikt deze repo nu de engine-managed Docsmith workflow:

- Mermaid-bronnen leven onder `documents/verantwoordingsverslag/assets/diagrams/`
- diagramoutputs worden gedeclareerd in `spec.yaml`
- Markdown blijft gewone afbeeldingspaden gebruiken, zoals `assets/generated/...`

De engine rendert gedeclareerde Mermaid-diagrammen tijdens `docsmith build` via `mmdc`.

`mmdc` hoort daarmee bij de Docsmith build-omgeving, net als `pandoc` en `xelatex`. Deze demo gebruikt die dependency alleen; zij beheert of installeert die niet zelf.

Opnemen in Markdown blijft ongewijzigd:

```md
![Procesdiagram van het registratieproces](assets/generated/registratieproces.png){ width=80% }
```

Afspraak in deze demo:

- Mermaid-bronnen worden als documentbron in de repository bewaard en moeten committed blijven
- gegenereerde PNG-assets zijn build-managed outputs en niet de source of truth
- diagrammen blijven gewone image assets in Markdown; er is geen lokale preprocessing of repo-side renderlogica meer nodig

Gewenste vervolgrichting:

- bredere engine-support voor diagramtypen en renderinginstellingen
- scherpere documentatie over wat engine-managed diagram rendering wel en niet dekt

## Bouwen met de sibling `../docsmith` engine

Voorwaarden:

- Python 3.11+
- `pandoc`
- `xelatex`
- `mmdc` op `PATH` wanneer het document gedeclareerde Mermaid-diagrammen gebruikt

Voorbeeld:

```bash
cd ../docsmith
python3 -m venv .venv
source .venv/bin/activate
pip install -e ".[dev]"
docsmith validate ../docsmith-demo/documents/verantwoordingsverslag
docsmith build ../docsmith-demo/documents/verantwoordingsverslag
```

## Valideren

Valideer de documentconfiguratie en invoerbestanden met:

```bash
cd ../docsmith
source .venv/bin/activate
docsmith validate ../docsmith-demo/documents/verantwoordingsverslag
```

## Wat deze demo wel en niet is

- Wel: een compacte maar geloofwaardige testset voor Docsmith
- Wel: Hanze-specifieke inhoud en opmaak, omdat dit een los documentrepo is
- Wel: een praktische benadering van verantwoordingsverslag-conventies voor validatie en demo-doeleinden
- Wel: een consumer-demo voor het minimale document-zone-model van Docsmith, inclusief first-class TOC-, bibliografie- en appendixsupport
- Niet: de Docsmith-engine zelf
- Niet: een definitieve afstudeerscriptie
- Niet: een claim dat DOCX al ondersteund wordt
