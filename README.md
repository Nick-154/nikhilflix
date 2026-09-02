# Nikhilflix

A portfolio laid out like a streaming service. Projects, experience and research
are title cards in horizontal rows; each one opens a detail sheet with the real
numbers, the stack, and links out to the source.

**Live:** https://nick-154.github.io/nikhilflix/

## Why it looks like this

A list of bullet points is the same document every candidate sends. A row of
title cards is scannable in the way a résumé is not: the metric sits on the card
face, so "12.6M rows", "30+ FPS" and "97% acc" read before any prose does.

The cover art is drawn rather than sourced. Every card carries a procedural SVG
built from what the project actually does: an oscilloscope trace for the SCPI
work, bronze/silver/gold partition bands for the lakehouse, bounding boxes with
corner brackets for the detector, skip-connection arcs over layer blocks for the
ResNet, a URL rendered as glyph ticks with one segment flagged for the phishing
classifier. No stock gradients.

The palette holds to two hues. Red marks my own work. Gold is reserved for the
GitHub row, because stars are gold and the colour tells you at a glance that
those repositories are not mine.

## The GenAI row

That row is a snapshot of the GitHub search API for `topic:llm` repositories
created since March 2026, taken on 1 September 2026. **Those are other people's
repositories.** Each card says so in the artwork itself, the row is labelled as
a snapshot with its date, and the footer repeats it. They are there for context
on what the field is building, not as a claim of authorship.

The numbers are frozen because the page makes no outbound requests at runtime.

## Build

One self-contained file. No framework, no build step, no bundler. The photo is
embedded as a data URI and the only external request is Google Fonts.

- `index.html` — the deployed page, a complete standalone document
- `nikhilflix.html` — the same page in Claude Artifact form, which supplies its
  own `<head>`; kept in sync with `index.html`

Type is Archivo, using its width axis to separate display from body, with
JetBrains Mono for every number and tech chip so metrics read in a different
voice than prose.

Committed dark on purpose. Netflix has no light mode, so rather than invert
badly the page paints every colour explicitly from a token and holds on any
host background.

## Accessibility

Cards are buttons, the detail sheet traps focus and closes on Escape, the rail
arrows are reachable by keyboard, and `prefers-reduced-motion` disables the
scale and reveal transitions. Text contrast was measured rather than eyeballed:
every foreground/background pair used for real content clears 4.5:1.
