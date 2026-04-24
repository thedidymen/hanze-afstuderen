# Hanze Starter Profile

Dit starterprofiel is een extra startpunt voor nieuwe auteurs. Het vervangt **niet** het uitgebreidere voorbeeld in `documents/verantwoordingsverslag/`.

Gebruik dit profiel wanneer je:

- snel wilt beginnen met een compact verantwoordingsverslag
- de aanbevolen content-only workflow wilt volgen zonder eerst een grotere demo door te nemen
- een kleine, overzichtelijke basis wilt met front matter, hoofdstukken, een figuur, een tabel, native cross-references en een appendix

Gebruik het volledige demo-profiel wanneer je:

- een rijker voorbeeld met meer hoofdstukken wilt zien
- meer metadata, meer inhoud en meer validatiecases nodig hebt
- template- of workflowgedrag in een realistischer rapportvorm wilt beoordelen

## Safe metadata changes

Pas metadata in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/hanze-starter-verantwoordingsverslag/spec.yaml) veilig aan door:

- `title`, `subtitle`, `author` en `date` te vervangen door je eigen gegevens
- velden zoals `student_number`, `supervisor`, `second_reviewer` en `client` inhoudelijk aan te passen, maar de sleutelnaam gelijk te houden
- `project.template` en de documentzones ongemoeid te laten
- IDs voor figuren en tabellen niet te hergebruiken voor iets anders

Wijzig liever geen:

- `project.template`
- `document.front_matter`, `document.main_matter` en `document.appendices` structuur zonder duidelijke reden
- bestandsnamen van secties zonder tegelijk `spec.yaml` mee te werken

## Add a chapter

Een extra hoofdstuk toevoegen:

1. maak een nieuw Markdown-bestand in `sections/`, bijvoorbeeld `06_resultaten.md`
2. voeg een top-level heading toe, bijvoorbeeld `# Resultaten`
3. zet het nieuwe bestand in de juiste volgorde onder `document.main_matter` in `spec.yaml`
4. houd de inhoud content-only: geen raw LaTeX, geen lokale renderinghacks

## Add a figure or table

Voor een figuur:

```md
Zie @fig:mijn-overzicht voor het overzicht.

![Overzicht van de voorbeeldsituatie](assets/images/mijn_overzicht.png){#fig:mijn-overzicht width=80%}
```

Voor een tabel:

```md
De kernpunten staan in @tbl:mijn-overzicht.

| Onderdeel | Status |
| --- | --- |
| R1 | Gereed |

Table: Overzicht van de kernpunten. {#tbl:mijn-overzicht}
```

Afspraak:

- figuren gebruiken `#fig:...`
- tabellen gebruiken `#tbl:...`
- tekstverwijzingen gebruiken `@fig:...` en `@tbl:...`
- gebruik stabiele lowercase IDs

## Mermaid reminder

Als je een Mermaid-diagram toevoegt:

1. zet de bron in `assets/diagrams/*.mmd`
2. voeg het diagram toe aan `diagrams:` in [spec.yaml](/Users/reijer/Repo/docsmith-demo/documents/hanze-starter-verantwoordingsverslag/spec.yaml)
3. verwijs daarna naar het gedeclareerde outputpad als gewone figuur

## Checklist before commit

1. metadata gecontroleerd in `spec.yaml`
2. eventuele Mermaid-diagrammen gedeclareerd onder `diagrams:` in `spec.yaml`
3. document gevalideerd met:

```bash
docsmith validate documents/hanze-starter-verantwoordingsverslag
```

4. PDF gebouwd met:

```bash
docsmith build documents/hanze-starter-verantwoordingsverslag
```

## Rule of thumb

Gebruik de starter voor een schone eerste opzet. Gebruik `documents/verantwoordingsverslag/` als referentie wanneer je wilt zien hoe dezelfde workflow eruitziet in een rijkere, verder uitgewerkte demo.
