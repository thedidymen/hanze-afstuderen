# Authoring Guide

Deze gids beschrijft de huidige authoringafspraken voor het Hanze verantwoordingsverslag in deze repository. De kern blijft: schrijf content-only Markdown en gebruik Docsmith-native structuurelementen waar die beschikbaar zijn.

Wie liever vanuit een klein, concreet voorbeeld start dan vanuit losse regels, kan nu ook kijken naar:

- `documents/hanze-starter-verantwoordingsverslag/`

Dat starterprofiel laat dezelfde afspraken zien in een minimale documentset met front matter, hoofdstukken, een figuur, een tabel, native cross-references en een appendix.

## Content-only Markdown

Voor deze repository geldt:

- geen raw LaTeX in authored Markdown
- geen lokale filters of workarounds voor cross-references
- geen `pandoc-crossref`
- figuren, tabellen en verwijzingen worden geschreven met de native Docsmith/Pandoc authoringvormen die de engine nu valideert en minimaal rendert

## Figures

Gebruik gewone Markdown image syntax, met een native figure-ID in Pandoc-attributen:

```md
![Demo-overzicht van student, evenement en beheerproces](assets/images/tech.jpg){#fig:demo-context width=80%}
```

Regels:

- gebruik IDs met prefix `fig:`
- zet de ID op de afbeelding zelf
- houd de caption in de alt-tekst kort en inhoudelijk
- gebruik bij voorkeur ook een `width=...` attribuut wanneer een expliciete breedte gewenst is

## Tables

Gebruik gewone Markdown-tabellen, met een captionregel direct onder de tabel:

```md
| ID | Type | Omschrijving |
| --- | --- | --- |
| R1 | Functioneel | Voorbeeld |

Table: Overzicht van demo-requirements. {#tbl:demo-requirements}
```

Regels:

- gebruik IDs met prefix `tbl:`
- zet de ID op de `Table:`-captionregel
- houd captions kort en zakelijk
- in de PDF horen tabelcaptions boven de tabel te verschijnen; figuurcaptions horen onder de figuur te verschijnen

## Text references

Verwijs in lopende tekst met native references:

```md
Zie @fig:demo-context voor de contextschets.
De requirements staan in @tbl:demo-requirements.
```

Gebruik:

- `@fig:...` voor figuren
- `@tbl:...` voor tabellen

Schrijf geen handmatige tekst zoals “Figuur 2” of “Tabel 1” wanneer een native reference mogelijk is.

## ID naming rules

Gebruik stabiele, eenvoudige IDs:

- alleen lowercase ASCII
- gebruik cijfers, `-` en `_` waar nodig
- begin met `fig:` of `tbl:`
- kies inhoudelijke namen die niet afhangen van handmatige nummering

Goede voorbeelden:

- `fig:demo-context`
- `fig:registratieproces`
- `tbl:demo-requirements`
- `tbl:validatiescenarios`

Vermijd:

- spaties
- hoofdletters
- losse numerieke IDs zoals `fig:1`
- captionspecifieke of tijdelijke namen die snel veranderen

## Mermaid diagrams

Mermaid-diagrammen blijven authored bronbestanden, maar worden via Docsmith-builds gerenderd tot gewone figuren.

Workflow:

1. schrijf de Mermaid-bron in `documents/verantwoordingsverslag/assets/diagrams/*.mmd`
2. declareer het diagram in `spec.yaml` onder `diagrams:`, inclusief `source` en `output`
3. verwijs in Markdown naar het gedeclareerde outputpad als gewone figuur:

```md
![Procesdiagram van het registratieproces](assets/generated/registratieproces.png){#fig:registratieproces width=80%}
```

Tijdens `docsmith build` rendert de engine het diagram via `mmdc` naar het gedeclareerde outputpad binnen de build. Daarna kan er in tekst normaal naar verwezen worden met `@fig:registratieproces`.

`mmdc` is hierbij een Docsmith build-environment dependency. Deze repository gebruikt die capability alleen aan de consumer-kant.

## What validation catches

De huidige Docsmith-validatie kan in elk geval authoringproblemen signaleren rond native figure/table cross-references, waaronder:

- duplicate IDs
- invalid IDs
- references naar ontbrekende targets

Gebruik daarom altijd eerst:

```bash
docsmith validate documents/verantwoordingsverslag
```

## Current limitations

- er zijn nog geen native references voor secties of appendices in deze demo-afspraak
- Mermaid-rendering is nu engine-managed, maar blijft afhankelijk van een buildomgeving waarin Docsmith `mmdc` op `PATH` kan vinden
- advanced image layout en cropping zijn nog niet opgelost
- de huidige cross-referenceflow is nog maar in een compacte demo-variant getest

## Practical rule of thumb

Als iets eruitziet als layoutlogica, hoort het niet in authored Markdown. Als iets een figuur, tabel of verwijzing is, gebruik dan de native `fig`/`tbl` authoringvormen en laat de engine/template de rest doen.
