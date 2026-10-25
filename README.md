# Desire Coding

Source for [desirecoding.com](https://desirecoding.com), the page recording the term **desire coding**, coined by Shana Kayne Beach ([ORCID 0009-0009-7465-7447](https://orcid.org/0009-0009-7465-7447)) and first published 2 September 2026.

## Case studies

The site also hosts case studies of desire coding. Plain static HTML, no build step; Cloudflare Pages serves the repo as is.

```
index.html                      the definition page (keep unchanged and citable)
assets/case.css                 shared styles for case study pages
cases/index.html                list of cases
cases/<case>/index.html         case hub: about this case, field notes, lab notes
cases/<case>/field-notes/<post>/index.html
cases/<case>/lab-notes/<post>/index.html
themes/index.html               shared themes across cases, one section per theme slug
templates/                      starting points for new posts (not indexed by search engines)
_headers                        Cloudflare Pages headers
```

Two streams run through every case:

- **Field notes** tell the story for technical and non-technical readers alike.
- **Lab notes** are for AI industry and academic readers, and lean on open questions and cited related work.

Posts appear when a pattern emerges, grouped by theme. Theme slugs: `user-comms`, `oversight`, `platform`, `user-feedback`, `ai-errors`, `data-access`, `ownership`, `cost`, plus vignettes.

To add a post:

1. Copy `templates/field-note.html` or `templates/lab-note.html` to its folder, fill every `[bracket]`, and delete the robots line.
2. Add it to the case hub, newest first (unhide the list and remove the "on its way" line for the first post).
3. Add it under each of its themes in `themes/index.html`.
4. Pair a lab note with its field note by linking each to the other.
5. After publishing, log every edit in the post's changelog.

## License

Dual-licensed:

- **Prose** (the text content of `index.html`): [CC BY 4.0](LICENSE-text). Reuse freely with attribution to Shana Kayne Beach.
- **Code** (HTML, CSS, SVG, and everything else): [GNU GPL v3.0](LICENSE).
