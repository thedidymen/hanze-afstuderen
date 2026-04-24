# Project Status

## Current Phase

Template and authoring workflow stabilization.

Deze repository zit nu primair in de fase waarin de Hanze/HBO-ICT-demo als schone consumer van Docsmith-structuurfeatures verder wordt gestabiliseerd voor realistisch authoring- en templategebruik.

## Current Focus

- de demo gebruiken als schone consumer van Docsmith support voor metadata, zones, appendices, bibliografie en ordered TOC placement
- het engine-template contract scherper maken waar dat nog impliciet is
- native figure/table cross-references in authored Markdown toetsen als consumer-contract
- richer metadata, media-baselines en captionconventies verder toetsen als consumer-contract
- authoring guidance en compact starterprofiel verder toetsen als consumer-workflow
- de demo blijven gebruiken als validatieomgeving en real-world test case

## Next Milestone

Stabiele thesis-achtige authoring workflow met rijkere metadata, media-richtlijnen en verdere templatepolish.

Concreet betekent dit dat deze repository nu kan doorpakken op:

- bredere toetsing van automatische figuur-/tabelnummering en cross-references
- verdere uitbouw van het starterprofiel naast de nu aanwezige authoring guide
- rijkere beeldplaatsing, sizing, cropping en layoutcontrole voor afbeeldingen
- bredere toetsing van engine-managed diagram rendering in meerdere demo- en profielvarianten
- verdere professionele afwerking van paginastijlen, tabellen en bibliografie

## Current Known Issues

- titelpagina-metadata wordt nu rijker benut, maar nog niet volledig breed genoeg getest over meerdere demo-varianten
- image handling heeft nu een baseline, maar geavanceerde cropping- en layoutcontrols ontbreken nog
- Mermaid-rendering is nu engine-managed via `spec.yaml`, maar nog niet breed genoeg getest buiten de huidige demo- en startervariant
- native figuur-/tabelcross-references zijn nu in deze demo in gebruik, maar nog niet breed getest in complexere documenten
- de authoring guide en het starterprofiel zijn er nu, maar nog niet breed genoeg getest als echte instapworkflow
- templatepolish is nog gaande voor echte thesis-readiness

## Note on Stability

Enginewijzigingen in de sibling `../docsmith` repository mogen deze repository tijdelijk breken zolang die wijzigingen expliciet worden gedocumenteerd en deze repository daardoor scherper als consumer/specification layer kan meebewegen.
