# Westmeath Arts & Creative Network

A static map of people, organisations, venues, events and skills across Westmeath. GitHub Pages serves `index.html`. The graph, search, directory and poster export all read from `data/network.js`.

## Updating the data

Edit `data/network.js`. It sets `window.CREATIVE_LINKS_DATA` to an array. Each entry has four fields:

- **name** — the person, organisation, venue or event as it should appear on the map
- **about** — comma-separated tags, for example `painting, festivals, heritage`
- **contact** — a public contact name, or `""` when there is none
- **kind** — one of `person`, `organisation`, `venue`, `event`

Only these fields are published. Do not add phone numbers, email addresses, biographies or social links.

Keep the file as a script (`window.CREATIVE_LINKS_DATA = [ ... ];`) rather than JSON loaded with `fetch`, so the page still opens from `file://`.

Reload `index.html` after saving. The page normalises tags, merges near-duplicates, and leaves out the generic tags listed in `SKIP_TAGS`.
