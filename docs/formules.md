# Formules in Docsmith

Docsmith verwerkt Markdown met Pandoc en bouwt de PDF met XeLaTeX. Gebruik daarom
de Pandoc-syntax voor wiskundige formules.

## Inline formule

Zet een korte formule tussen enkele dollartekens:

```md
De prioriteit is $P(r) = I(r) \times N(r)$.
```

## Formule als blok

Zet een formule die gecentreerd en op een eigen regel moet staan tussen dubbele
dollartekens:

```md
$$
P(r) = I(r) \times N(r)
$$
```

Ook uitgebreidere LaTeX-constructies, zoals `cases`, horen binnen deze
`$$...$$`-blokken:

```md
$$
Priority(r)=
\begin{cases}
\infty, & \text{if } r \text{ is a Must Have}\\
Importance(r)\times Necessity(r), & \text{otherwise}
\end{cases}
$$
```

Gebruik voor displayformules in authored Markdown dus `$$...$$`. De alternatieve
LaTeX-notatie `\[...\]` wordt in deze documentworkflow niet als betrouwbare
display-math-syntax behandeld en kan als letterlijke tekst in de output
verschijnen.

## Praktische afspraken

- Gebruik alleen ASCII-tekens in de LaTeX-opmaak zelf wanneer dat kan.
- Gebruik `\text{...}` voor gewone woorden binnen een formule.
- Gebruik `\\` voor een nieuwe regel in omgevingen zoals `cases`.
- Houd complexe formules in een apart blok; gebruik inline math alleen voor korte
  uitdrukkingen in een zin.