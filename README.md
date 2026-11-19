# Nikke Tier List and Team Builder

A single self-contained HTML page for **Goddess of Victory: Nikke** — rank
Nikkes into tiers S–D and build teams of 5. No server, no external images or
APIs; everything is inline in one file.

Live at: https://homebrew.franxx.net/nikke-tier-list.html

## Use it

Just open `nikke-tier-list.html` in a browser — double-click it, or serve it
with any static file server. Your tier placements and saved teams are stored
in your browser's `localStorage`; use **Export** on the page to back them up
as JSON (or move them to another device), and **Import** to restore them.

## Features

- All 75 Nikkes from the roster in `roster.md`, starting in the Unranked pool
- Drag-and-drop with click-to-move fallback, search and filters (element,
  rarity, Burst)
- Team builder: 3 named teams of 5 slots, live Burst I/II/III counts with a
  warning if a Burst step is missing, element breakdown, average level
- Ranked vs unranked counts, Reset, Export/Import JSON

## Update the roster

The Nikke data lives in a table inside `nikke-tier-list.html` (name, level,
Burst, element, rarity, limit break). Edit the table, keep the format, and
update `roster.md` to match so the source of truth stays in one place.

## Deploy

The live copy is hosted on a static file server (Caddy) at
`homebrew.franxx.net`. To update it, copy `nikke-tier-list.html` to the web
root. Note: the site's Content-Security-Policy must allow inline scripts
(`script-src 'self' 'unsafe-inline'`) or the page will render without any
interactivity.
