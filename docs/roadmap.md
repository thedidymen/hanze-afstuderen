# Roadmap

Deze roadmap houdt de Hanze demo compact en consumer-side. Het doel is niet om enginegedrag lokaal te simuleren, maar om scherp te maken wat al werkt, waar de demo nu op focust en welke vragen nog openstaan.

## Done

- first-class gebruik van metadata, documentzones, appendices, bibliografieplaatsing en ordered TOC placement
- content-only front matter zonder authored LaTeX-workarounds
- rijkere titelpagina- en omslagmetadata in `spec.yaml` en de lokale template
- basisconventies voor afbeeldingen met Markdown + Pandoc breedte-attributen
- Mermaid-bronbestanden als `.mmd` plus engine-managed rendering via `diagrams:` declaraties
- tabelcaptions toegevoegd aan de huidige demo-tabellen
- native `fig`/`tbl` IDs en `@fig:`/`@tbl:` cross-references in de huidige demo
- authoring guide voor native figure/table cross-references
- compact Hanze starterprofiel als tweede, kleine authoringcase
- lokale templatepolish voor figuur- en tabelcaptions

## Current focus

- nette authoringconventies voor tabellen, figuren en diagrammen
- native cross-references breder toetsen in realistischer documentvarianten
- stabiel gebruik van engine-managed Mermaid-rendering in meerdere documentvarianten
- verdere verbetering van figuur-, tabel- en floatpresentatie in de lokale template
- starterprofiel verder toetsen en eventueel licht uitbreiden naast de nu aanwezige authoring guide
- documentatie die duidelijk onderscheid maakt tussen huidige demo-afspraken en gewenste engine/workflowrichting

## Next

- bredere toetsing van de huidige automatische figuur- en tabelnummering plus cross-references
- bredere toetsing en documentatie van engine-managed diagramrendering voor meerdere diagramtypen
- bredere toetsing en lichte uitbreiding van de authoring guide en het starterprofiel
- verdere image sizing-, cropping- en layoutcontrols zonder authored LaTeX
- extra demo-inhoud om tabellen, figuren en bijlagen onder iets zwaardere belasting te valideren

## Later

- rijkere engine-side diagramfeatures of bredere Docsmith-dekking voorbij de huidige Mermaid-baseline
- regressie- of CI-dekking voor diagramrendering buiten deze losse demo
- rijkere beeldlayout zoals meerdere afbeeldingen naast elkaar of gestuurde placementprofielen
- verdere thesis-polish voor headers, bibliografie, appendixovergangen en grotere tabellen
- bredere regressiechecks over meerdere demo- of profielvarianten

## Open design questions

- hoe breed moet de huidige engine-side figuur-/tabelreferentie worden buiten de bestaande PDF-baseline?
- hoe breed moet engine-managed diagramrendering worden voordat extra diagramtypen of theming nodig zijn?
- wanneer zijn build-managed diagramoutputs nog zinvol om lokaal te inspecteren, en wanneer moeten ze puur ephemeral blijven?
- hoeveel image control is wenselijk in authored Markdown voordat de workflow te technisch wordt?
- welke minimale set aan authoringregels maakt de demo bruikbaar als starterprofiel zonder de repo onnodig complex te maken?
