Noto Serif Bengali (Regular, Bold) — Google Noto Fonts project.

Licensed under the SIL Open Font License 1.1: https://scripts.sil.org/OFL

Used by `theme/pdf/progit-bn-theme.yml` so the generated PDF actually
has Bengali glyphs embedded — Asciidoctor PDF's default theme fonts
don't cover the Bengali script, so without this the PDF renders
Bangla text as blank/missing glyphs regardless of fonts installed on
the reader's machine (PDF text uses embedded font glyphs, not the
viewer's system fonts).
