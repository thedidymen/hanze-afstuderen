# AGENTS.md

- Deze repository is een documentdemo en niet de Docsmith-engine.
- Hanze-specifieke inhoud en template-aanpassingen horen hier thuis, niet in de core-engine.
- Houd de scheiding tussen `templates/`, `documents/` en documentassets intact.
- Maak de demo realistisch genoeg voor validatie, maar niet onnodig uitgebreid of complex.

## Repository Role

- Deze repository is een consumer repository van de Docsmith-engine.
- Deze repository definieert:
  - templates
  - documentstructuren
  - real-world use cases, zoals een Hanze/HBO-ICT-verantwoordingsverslag
- Deze repository implementeert niet de Docsmith-engine.
- Deze repository mag niet leunen op ongedocumenteerd enginegedrag.

## Development Philosophy

- Docsmith ontwikkelt zich als document build system in een aparte repository.
- Deze repository drukt requirements voor dat systeem uit via templates, voorbeeldrapporten en validatiecases.
- Vermijd workarounds in deze repository voor problemen die eigenlijk in de engine horen te worden opgelost.
- Implementeer niet meerdere structurele aannames tegelijk als de engine daar nog geen stabiele support voor heeft.
- Wacht liever op expliciete engine support dan dat je structurele hacks in templates of documenten encodeert.
- Houd templates zo declaratief mogelijk.
