# RoC Warband Generator

**Version 0.9.10** — Unofficial bilingual (English / Français) browser adaptation of Peter Acs (Phlyk)'s **RoC Warband Generator v1.2.8**, as published at [Lead Rising](https://www.lead-rising.com/p/roc-warband-generator.html).

## Use and deployment

Open [`index.html`](index.html) in any modern browser. No Excel, build step, registration or server backend is required. On GitHub Pages, publish from `main` → `/ (root)` via Settings → Pages. Intended live URL, when deployment is enabled: https://dreadaxe.github.io/roc-warband-generator/

## Features

- Original-English / French toggle and four skin variants (RoC pages, Slaves to Darkness, The Lost and the Damned, monochrome).
- One **Load / Charger** menu at the top. Its list includes **Local saves** first and **Original workbook examples** second; selecting an entry immediately loads it. JSON import remains available.
- A **generation seed** field in the Load menu. If a locally saved warband uses the entered seed, it loads that saved warband. Otherwise, it regenerates a warband using **the currently selected options** and the entered seed.
- Generate and edit warband and champion names with instant preview updates (no need to regenerate the roster). The champion name generator selects a race-aware pool after the champion's actual race has been rolled. Character followers get individual race-based names; grouped unit followers get one collective nickname (not a fictional name for each miniature). Every profile includes a dice button to reroll its displayed name only. Automatically generated names use an isolated PRNG derived from the warband seed, preserving all mechanical dice rolls. Names are included in JSON/TXT/Markdown/BBCode and survive loading.
- An icon next to the seed copies it; a miniature icon identifies the estimated model count.
- The header tagline is **Path to Glory** in both languages. Generated two-part personal names use canonical English spellings in saved files; the given name is retained while the compound surname is localized on screen and in TXT, Markdown and BBCode exports (e.g. `Goron Bloodreaper` ↔ `Goron Faucheur-de-sang`). Recognized French surnames can also be typed and switched back to English. Unknown or freely invented surnames are preserved unchanged. The estimated-miniatures symbol has been redrawn for better legibility.
- The **Save warband as JSON** and **Export & print** controls share a single horizontal action row. Preferences and advanced settings start collapsed. Results can be saved locally, imported/exported to JSON, or exported as TXT, Markdown (`.md`) and forum BBCode (`.bbcode`) with an optional dice-roll log. The export menu offers shared content controls for numeric profiles, attributes/gifts/items, model counts and the roll log; its copy action has a selectable TXT/Markdown/BBCode format. Printing remains a separate full visual render. JSON is always a full, lossless save and ignores presentation checkboxes.

## Naming sources and credit

The name generators are **independent reconstruction-inspired algorithms**, **not** copies of Zhu Bajiee's Google Sheets or exact historical name tables. They draw on the naming practices documented in four *The Realm of Zhu* essays: [Chaos Warriors (2016)](https://realmofzhu.blogspot.com/2016/10/the-chaos-deth-spiky-name-generator-of.html), [Orcs (2016)](https://realmofzhu.blogspot.com/2016/10/the-name-of-orc.html), [Elves (2017)](https://realmofzhu.blogspot.com/2017/06/ye-oldhammer-elf-name-generator.html), and [Dwarfs (2017)](https://realmofzhu.blogspot.com/2017/08/an-oldhammer-recounting-of-dwarves.html). The other races (Goblins, Skaven, Beastmen, Ogres, etc.) use original, deliberately separate themed vocabularies without claiming they come from Zhu. Warband names use a separate original algorithm. All links and author credit are present in the app's collapsed naming-sources panel.

## Logo and typography

The masthead first attempts to display the historic [Realm of Chaos logo reference provided by the project owner](https://eternalhunt.wordpress.com/wp-content/uploads/2013/05/roc_logo02.png). Because the original asset could not be reliably downloaded, it is **still external**. If it fails, the application now displays an **embedded monochrome SVG title artwork** (also available at [`assets/realm-of-chaos-monochrome.svg`](assets/realm-of-chaos-monochrome.svg)), so the title remains visible when offline. Both the loaded remote historic image and the local SVG are rendered in black-and-white for the RoC and monochrome skins; the historical image is recoloured for the other skins via CSS. The local SVG is a modern, independent typographic fallback **not a restoration or reproduction of the historical hand-drawn Games Workshop logo**. The default and photocopy skins use black and white; Slaves to Darkness and Lost and the Damned tint the title red and olive respectively. Original artwork, names and marks remain with their respective owners. For a fully local historical logo, a confirmed redistributable high-resolution source is still required.

## Seeded randomness

A seed is not a pre-selected warband. It initializes a repeatable pseudo-random process. **Same seed + same generation configuration + same algorithm version** reproduces the same dice results. A seed alone does not carry all the options required to recover the original warband. The JSON export preserves the full settings and roll log.

## Disclaimer

Independent, unofficial fan utility, neither affiliated with nor endorsed by Games Workshop. Some numerical effects of gifts, mutations and magical items are not automatically applied. The original macro-enabled spreadsheet is not included.