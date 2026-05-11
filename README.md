# D4 Loot Filter Generator

A browser-based tool for generating Diablo IV loot filter import codes. No account, no server, no subscriptions — runs entirely in your browser.

**Live tool:** https://upsilon72.github.io/d4-filter-generator

## What it does

- Pick your class, select the stats that matter to your build
- Choose skill ranks to highlight
- Click **Generate** — get an import code ready to paste into D4 instantly

## Features

- ✅ 77 verified affix IDs (all confirmed via single-affix filter exports)
- ✅ Full offensive / defensive / resource / utility / mobility coverage
- ✅ Warlock skill ranks fully confirmed; other classes in progress
- ✅ Colour-coded tiers: Cyan (Greater Affix) → Green (Legendary) → Gold (2+ core stats) → Orange (any build affix)
- ✅ Preset builds (HF Warlock pre-loaded)
- ✅ Works entirely offline after first load

## How to import in-game

1. Open D4 → Character Menu → Loot Filter
2. Click **New Filter**
3. Click **Import**
4. Paste the generated code → Confirm

## How to deploy to GitHub Pages

1. Fork this repo (or create a new one named `d4-filter-generator`)
2. Push `index.html` and `README.md` to the `main` branch
3. Go to repo **Settings → Pages → Source → Deploy from branch → main / root**
4. Your tool will be live at `https://upsilon72.github.io/d4-filter-generator`

## Contributing

The biggest outstanding task is confirming skill rank IDs for non-Warlock classes. Each class needs ~15 minutes of in-game work (build a filter with one skill per rule, export, decode).

Classes needed: Barbarian, Druid, Necromancer, Rogue, Sorcerer, Spiritborn, Paladin.

See the [technical notes](https://github.com/Upsilon72/d4-filter-generator/wiki) for the export method.

## Technical notes

The filter format is Google Protocol Buffers binary, base64-encoded. All encoding runs client-side in ~80 lines of vanilla JS. No frameworks, no build step.

Format was reverse-engineered from live D4 exports. See the reference document for the full field spec.

## Credits

Research and reverse-engineering by **Upsilon72** with Claude (Anthropic).  
Season 13 — Lord of Hatred.
