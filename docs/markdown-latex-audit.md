# Markdown LaTeX Audit

Deze audit kijkt alleen naar raw LaTeX in Markdown-bestanden onder `documents/`. Het doel is te bepalen of authored content nog structurele of layoutgerichte LaTeX-workarounds bevat die niet meer nodig zouden moeten zijn.

Scope-opmerking:

- De primaire focus is authored content in `documents/verantwoordingsverslag/sections/`.
- [combined.md](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/build/combined.md) is gegenereerde build-output, geen authoring source.

## Current state

### Authored Markdown sources

- In de huidige sectiebestanden staat geen authored raw LaTeX meer voor front matter, inhoudsopgave, bibliografie of appendices.
- [00_voorwoord.md](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/sections/00_voorwoord.md#L1) en [01_samenvatting.md](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/sections/01_samenvatting.md#L1) gebruiken gewone Markdown-headings met `.unnumbered`.
- Er is geen los authored TOC-bestand of authored bibliografiehoofdstuk meer aanwezig in `sections/`.

### Generated Markdown build output

- [combined.md](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/build/combined.md#L25) bevat `\tableofcontents` binnen de gegenereerde TOC-sectie in `front_matter`.
- [combined.md](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/build/combined.md#L160) bevat de bibliografie in `back_matter`.
- [combined.md](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/build/combined.md#L167) bevat `\appendix` vóór de appendixsecties.

Deze LaTeX-fragmenten zijn build-output van engine- of templategedrag en geen authored workaround meer.

## Assessment

- De structurele LaTeX-workarounds zijn uit authored Markdown verdwenen.
- TOC-plaatsing is nu engine-driven via ordered generated `front_matter` items in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/spec.yaml#L13).
- Bibliografieplaatsing komt uit `document.bibliography` in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/spec.yaml#L27).
- Appendix-omschakeling komt uit `document.appendices` in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/verantwoordingsverslag/spec.yaml#L25).

## Conclusion

De authored documentbron is nu content-only voor de onderdelen die eerder door raw LaTeX werden gestuurd. De resterende LaTeX zit in gegenereerde output en hoort daar functioneel thuis.

Er is vanuit deze audit geen extra cleanup nodig voor de Hanze demo rond de oude Lua- of front-matter-workarounds.
