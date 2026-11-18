# Bundled fonts

Both families are self-hosted as WOFF2 under the SIL Open Font License 1.1.
The licence and author files are kept next to the binaries.

## Inter Tight (Latin)

- Source: https://github.com/rsms/inter-gf-tight (`fonts/webfonts/`)
- Files: `inter-tight/InterTight-{Regular,Medium,SemiBold,Bold}.woff2`
- Version: 3.262
- Licence: `inter-tight/OFL.txt` — Copyright 2022 The Inter Project Authors
- Authors: `inter-tight/AUTHORS.txt`
- Only the four weights the site uses are bundled. Italics are not used, so they
  are not included.

## Estedad (Persian / Arabic script)

- Source: https://github.com/aminabedi68/Estedad (`fonts/webfonts/`)
- File: `estedad/Estedad-wght.woff2` — variable, `wght` 200–900
- Licence: `estedad/OFL.txt` — Copyright 2022 The Estedad Project Authors
- Authors: `estedad/AUTHORS.txt`
- The `@font-face` declaration restricts this file to Arabic-script Unicode
  ranges, so Latin words inside Persian copy are drawn by Inter Tight.

## Adding or updating a font

1. Download the official WOFF2 build from the upstream repository (never a CDN
   or a font API).
2. Copy the upstream `OFL.txt` (and `AUTHORS.txt` when present) beside it.
3. Add a `@font-face` rule in `src/styles.css` with an explicit `font-display`
   and, for a script-specific family, a `unicode-range`.
4. Preload only the faces needed for first paint in `index.html`.
