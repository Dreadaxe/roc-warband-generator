# RoC Warband Generator

**Version 0.9.7** — Unofficial bilingual (English / Français) browser adaptation of Peter Acs (Phlyk)'s **RoC Warband Generator v1.2.8**, as published at [Lead Rising](https://www.lead-rising.com/p/roc-warband-generator.html).

## Use and deployment

Open [`index.html`](index.html) in any modern browser. No Excel, build step, registration or server backend is required. On GitHub Pages, publish from `main` → `/ (root)` via Settings → Pages. Intended live URL, when deployment is enabled: https://dreadaxe.github.io/roc-warband-generator/

## Features

- Original-English / French toggle and four skin variants (RoC pages, Slaves to Darkness, The Lost and the Damned, monochrome).
- One **Load / Charger** menu at the top. Its list includes **Local saves** first and **Original workbook examples** second; selecting an entry immediately loads it. JSON import remains available.
- A **generation seed** field in the Load menu. If a locally saved warband uses the entered seed, it loads that saved warband. Otherwise, it regenerates a warband using **the currently selected options** and the entered seed.
- Generate warband names and champion names using adjacent dice buttons. A name can always be edited manually. Champion names are stored with the roster, included in exports, and survive loading.
- An icon next to the seed copies it; a miniature icon identifies the estimated model count.
- The **Save warband as JSON** and **Export & print** controls share a single horizontal action row. Preferences and advanced settings start collapsed. Results can be saved locally, imported/exported to JSON, exported to text, or printed.

## Naming sources and credit

The warrior naming tool is **an independent algorithm**, inspired by the early 1980s Citadel Chaos Warrior names documented by **Zhu Bajiee** in [The Chaos Deth Spiky Name Generator of Chaos](https://realmofzhu.blogspot.com/2016/10/the-chaos-deth-spiky-name-generator-of.html), published 23 October 2016 on *The Realm of Zhu*. It is **not** a reproduction of Zhu's embedded generator or full original tables. Warband names use an independent selection of evocative Oldhammer-style constructions; they are not sourced from Zhu's article.

## Logo and typography

The masthead first attempts to display the historic [Realm of Chaos logo reference provided by the project owner](https://eternalhunt.wordpress.com/wp-content/uploads/2013/05/roc_logo02.png). Because the original asset could not be reliably downloaded, it is **still external**. If it fails, the application now displays an **embedded monochrome SVG title artwork** (also available at [`assets/realm-of-chaos-monochrome.svg`](assets/realm-of-chaos-monochrome.svg)), so the title remains visible when offline. The local SVG is a modern, independent typographic fallback **not a restoration or reproduction of the historical hand-drawn Games Workshop logo**. The default and photocopy skins use black and white; Slaves to Darkness and Lost and the Damned tint the title red and olive respectively. Original artwork, names and marks remain with their respective owners. For a fully local historical logo, a confirmed redistributable high-resolution source is still required.

## Seeded randomness

A seed is not a pre-selected warband. It initializes a repeatable pseudo-random process. **Same seed + same generation configuration + same algorithm version** reproduces the same dice results. A seed alone does not carry all the options required to recover the original warband. The JSON export preserves the full settings and roll log.

## Disclaimer

Independent, unofficial fan utility, neither affiliated with nor endorsed by Games Workshop. Some numerical effects of gifts, mutations and magical items are not automatically applied. The original macro-enabled spreadsheet is not included.