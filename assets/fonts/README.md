# Fonts

IBM Plex, SIL Open Font License 1.1. See `OFL.txt`.

Upload this whole folder to `assets/fonts/` in `dinith-heshan/learn`.

## Files

| File | Size | What it is |
|---|---|---|
| `plex-sans-latin-wght-normal.woff2` | 44.6 KB | IBM Plex Sans **variable**, weight axis 100–700, upright |
| `plex-sans-latin-wght-italic.woff2` | 49.0 KB | IBM Plex Sans **variable**, weight axis 100–700, true italic |
| `plex-mono-latin-400.woff2` | 14.4 KB | IBM Plex Mono Regular, static |
| `plex-mono-latin-600.woff2` | 15.3 KB | IBM Plex Mono SemiBold, static |

Total: ~123 KB.

## Provenance

Extracted from npm, both at version 5.3.0:

- `@fontsource-variable/ibm-plex-sans` → IBM Plex Sans 3.201
- `@fontsource/ibm-plex-mono` → IBM Plex Mono 2.3

Subset: **latin only**. No latin-ext, cyrillic, greek or vietnamese.
Characters outside latin fall back to a system font rather than failing.

The sans is the **weight-axis-only** build, not the `standard` build.
The standard build adds a width axis and costs 64 KB instead of 44.6 KB,
for an axis this site does not use.

The italic files are genuine italics with their own letterform drawings,
not sheared uprights.

## Verified

`fvar` table on both sans files reports a single `wght` axis, 100 to 700,
default 400. Mono files report OS/2 weight class 400 and 600.

## Why there is no variable mono

IBM does publish a variable Plex Mono, but it is not distributed through
Fontsource or Google Fonts — only as a manual download from IBM's GitHub
releases. Static mono weights are ~15 KB each, and mono is used here for
code and labels where only two weights are ever wanted, so the axis would
buy flexibility that never gets spent.

## No mono italic

Deliberate. Slanted code is almost never wanted. If a page needs it later,
add `plex-mono-latin-400-italic.woff2` from the same npm package.
