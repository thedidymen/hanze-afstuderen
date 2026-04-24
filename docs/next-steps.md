# Next Steps

De grote structurele migratie is afgerond: metadata-doorgifte, documentzones, appendices, bibliografieplaatsing en ordered TOC placement gebruiken nu first-class Docsmith support. De Hanze demo hoeft die structuur niet langer lokaal met Lua- of document-structure-workarounds te simuleren.

De volgende fase draait daarom niet meer om basisstructuur, maar om stabieler templategebruik, betere auteursworkflow en realistischer mediahandling.

## Top priorities

### 1. Verbreed de toetsing van native figure/table numbering en cross-references

De basis voor captions en native `@fig:`/`@tbl:`-verwijzingen is nu aanwezig in de demo. De volgende stap is om dit in rijkere of complexere documenten breder te beproeven, inclusief meer figuren, tabellen en combinaties van verwijzingen.

### 2. Toets de authoring guide en het starterprofiel breder

De content-only authoring guide en een compact Hanze starterprofiel zijn nu aanwezig. De volgende stap is om die instapworkflow verder te toetsen en gericht uit te breiden met rijkere voorbeelden, zonder het onnodig zwaar te maken.

### 3. Verbeter image sizing, cropping en layoutcontrole

Afbeeldingen hebben nu een basisconventie met Markdown + Pandoc breedte-attributen, betere floatplaatsing en nette figuur-/tabelcaptions. Wat nog ontbreekt zijn rijkere opties voor cropping, positionering en complexere beeldlayout.

### 4. Formaliseer de Mermaid- en diagramworkflow

De demo gebruikt nu engine-managed Mermaid-rendering via `diagrams:` declaraties in `spec.yaml`. Wat nog ontbreekt zijn bredere richtlijnen voor meerdere diagramvarianten, mogelijke CI-dekking en verdere toetsing van deze workflow buiten de huidige compacte demo’s.

### 5. Werk de template verder af richting thesis-readiness

Nu de structuur stabiel is, wordt templatepolish waardevoller. Denk aan betere titelpagina-informatiehiërarchie, rustiger paginastijlen, sterkere bibliografiepresentatie en betere appendix- en figuurpresentatie.

## Already implemented baselines

- rijkere metadata voor omslag en titelpagina werken nu in deze demo, maar zijn nog maar op één demo-variant beproefd
- image handling heeft nu een bruikbare baseline met Pandoc breedte-attributen, overflowbescherming en nette figuur-/tabelcaptions
- Mermaid heeft nu een engine-managed baseline met `.mmd` bronbestanden, `diagrams:` declaraties en build-managed image outputs
- tabelcaptions zijn nu aanwezig in de huidige demo-tabellen
- native `fig`/`tbl` IDs en `@fig:`/`@tbl:`-verwijzingen zijn nu in de demo-authoring opgenomen
- er is nu een authoring guide voor native figure/table cross-references
- er is nu een compact starterprofiel voor een Hanze verantwoordingsverslag

## Current known issues

- image sizing is nu consistenter, maar cropping en geavanceerde beeldlayout ontbreken nog
- Mermaid-diagrammen worden nu engine-managed gerenderd, maar de workflow is nog niet breed genoeg beproefd in rijkere documentvarianten of CI
- rijkere metadata werkt nu, maar is nog niet breed genoeg getest over meerdere demo- of profielvarianten
- native cross-references zijn nu aanwezig, maar nog niet breed genoeg getest in zwaardere of complexere rapportvarianten
- templatepolish is nog gaande en nog niet op thesis-niveau

## Working principle

Deze repository blijft een consumer van Docsmith. Nieuwe verbeteringen horen daarom declaratief en repo-lokaal te blijven: geen nieuwe structurele workarounds, geen simulatie van enginegedrag in templates, en geen afhankelijkheid van ongedocumenteerd gedrag.
