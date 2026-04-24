# Workflow

## Purpose of this document

Dit document is een high-level workflowgids voor `docsmith-demo`. Het geeft het mentale model en de belangrijkste entry points, maar is **geen volledige specificatie**.

Gedetailleerd gedrag leeft elders:

- in `docsmith` voor enginegedrag, build/validate-routes en renderorkestratie
- in de specifieke docs en voorbeeldprofielen in deze repository voor authoring- en consumerafspraken

Gebruik dit document dus als navigatie en overzicht, niet als bron van volledige implementatiedetails.

## Repository roles

### `docsmith`

- generieke engine
- verantwoordelijk voor build, validatie en renderorkestratie
- hoort geen Hanze-specifieke template- of documentlogica te bevatten

Voor engine-interne details: zie de `docsmith` repository en diens README/docs.

### `docsmith-demo`

- consumer repository
- verantwoordelijk voor templates, content, authoringworkflow en voorbeeldprofielen
- laat zien hoe de engine in een realistische Hanze/HBO-ICT-context gebruikt kan worden

## Entry points for users

### Starter profile

- [documents/hanze-starter-verantwoordingsverslag/README.md](/Users/reijer/Repo/docsmith-demo/documents/hanze-starter-verantwoordingsverslag/README.md)
- doel: snelle start, minimaal voorbeeld, compacte authoringcase

Gebruik dit profiel wanneer je een klein en overzichtelijk startpunt zoekt.

### Full demo

- `documents/verantwoordingsverslag`
- doel: realistischer validatieprofiel, rijkere voorbeeldcase

Gebruik dit profiel wanneer je de workflow wilt zien in een uitgebreider verantwoordingsverslag of template-/workflowgedrag onder realistischer belasting wilt beoordelen.

## Authoring model

De authoringafspraken worden bewust niet hier volledig herhaald. Zie:

- [docs/authoring-guide.md](/Users/reijer/Repo/docsmith-demo/docs/authoring-guide.md)

Kort samengevat:

- content-only Markdown
- figuren en tabellen gebruiken native `fig`/`tbl` IDs en `@fig:` / `@tbl:` references
- Mermaid-diagrammen worden in `spec.yaml` gedeclareerd en tijdens de build als gewone afbeeldingen gerenderd

## Build workflow

Het conceptuele pad is:

1. declareer diagrammen waar nodig in `spec.yaml`
2. valideer het documentprofiel met `docsmith validate ...`
3. bouw de PDF met `docsmith build ...`, waarbij gedeclareerde diagrammen tijdens de build worden gerenderd

Dit document beschrijft bewust niet alle CLI-details; daarvoor hoort de engine-documentatie leidend te zijn.

Belangrijk: `mmdc` is hierbij een build-environment dependency van Docsmith voor documenten die Mermaid-diagrammen declareren. Het hoort niet bij de demo-repository zelf.

Diagram policy in deze repo:

- `.mmd`-bestanden zijn authored bronbestanden en horen committed te blijven
- gegenereerde diagram-PNG’s onder `build/` zijn build-output en horen niet committed te worden
- eerder gecommitte gegenereerde PNG’s zijn niet langer de source of truth

## What the engine guarantees

Op hoofdlijnen levert de engine in deze workflow:

- validatie van native figure/table cross-reference authoring
- deterministische documentbuilds binnen het gekozen profiel
- template-driven rendering op basis van consumer-side metadata en documentstructuur

Voor de exacte grenzen van die garanties: zie de `docsmith` repository/documentatie.

## What is intentionally NOT handled

Deze workflow dekt op dit moment expliciet **niet**:

- section references
- appendix references
- DOCX cross-reference parity
- advanced image layout/cropping
- rijkere diagramfeatures buiten de huidige engine-managed Mermaid-rendering

Dit voorkomt dat deze repository per ongeluk meer belooft dan de huidige workflow werkelijk ondersteunt.

## Keeping this document up to date

### When should this document be updated?

Werk dit document bij:

- wanneer er een nieuwe entry point bijkomt, zoals een extra documentprofiel
- wanneer het authoringmodel wezenlijk verandert
- wanneer de buildstappen conceptueel veranderen
- wanneer de verantwoordelijkheidsverdeling tussen engine en consumer verschuift

### What should NOT trigger updates?

Werk dit document **niet** bij voor:

- template styling tweaks
- kleine contentwijzigingen in voorbeeldrapporten
- kleine herformuleringen in andere docs

Als een wijziging de mentale workflow niet verandert, hoort dit document meestal ongemoeid te blijven.

## Links

- [docs/authoring-guide.md](/Users/reijer/Repo/docsmith-demo/docs/authoring-guide.md)
- [documents/hanze-starter-verantwoordingsverslag/README.md](/Users/reijer/Repo/docsmith-demo/documents/hanze-starter-verantwoordingsverslag/README.md)
- [docs/project-status.md](/Users/reijer/Repo/docsmith-demo/docs/project-status.md)
- `docsmith` engine repository: `../docsmith`
