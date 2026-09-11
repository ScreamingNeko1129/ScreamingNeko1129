# Third-party notice

The two SVG files in `templates/` are copied from
[jstrieb/github-stats](https://github.com/jstrieb/github-stats) (release 2.0.1)
and modified only to change colours so the generated cards match the palette
used in the profile README.

That project is licensed under the **GNU General Public License v3.0**. Its full
licence text is at
<https://github.com/jstrieb/github-stats/blob/master/LICENSE>, and these two
modified template files are covered by it.

## What was changed

Colour declarations only — 29 of them across the two files. No markup, layout,
template placeholders or animation was touched, so the files still work with the
upstream binary unmodified.

| | Upstream | Here |
|---|---|---|
| Card background | `white` / `#0d1117` | `#FDF1E3` / `#1B1B1D` |
| Card border | `rgb(225, 228, 232)` | `#EFE4D6` / `#3A2E24` |
| Heading | `rgb(3, 102, 214)` / `#58a6ff` | `#C96C12` / `#F7A63C` |
| Body text | `rgb(88, 96, 105)` / `#c9d1d9` | `#1B1B1D` / `#FDF1E3` |
| Icons | `rgb(88, 96, 105)` / `#8b949e` | `#C96C12` / `#F7A63C` |
| Progress track | `rgb(225, 228, 232)` | `#EFE4D6` / `#3A2E24` |

The coloured segments of the language bar are **not** themed here. Those colours
are written into the SVG by the generator using GitHub Linguist's per-language
palette, so they are not part of the template.

## Upgrading

The generator itself is not vendored — the workflow downloads a pinned, checksum
verified release binary. To move to a newer release, bump `VERSION` and `SHA256`
in `.github/workflows/github-stats.yml`, then re-check these templates against
the upstream ones in `src/templates/` for any structural change.
