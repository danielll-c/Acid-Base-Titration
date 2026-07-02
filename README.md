# Acid-Base Titration

Interactive acid-base titration curve generator for classroom demonstration and chemistry teaching.


## Features

- pH titration curve and overlaid first-derivative curve
- Strong acid/base, weak acid/base, common salts, polyprotic systems, and custom reagents
- Two simultaneous acid-base indicators, with optional hidden indicators
- Manual readout by slider or numeric volume input
- Export curve as SVG or PNG
- Interface languages: Simplified Chinese, Traditional Chinese, English, and Japanese
- Built-in information panel with makers, sources, version, and expandable data tables

## Data

The structured data snapshot is stored in:

```text
database/acid-base-titration-database.json
```

It includes:

- acid/base conjugate families and pKa values
- supported acids, bases, and salts
- supported indicators, transition ranges, colors, and localized names
- model notes, data source notes, and last-updated metadata

The running app keeps the same data embedded inside `index.html` so it works as a single-file teaching artifact.

## Calculation Model

For each titration volume point, the app combines the analyte and titrant material amounts, then solves pH using:

- mass balance
- charge balance
- acid-base distribution fractions
- `Kw = 1.0e-14` at 25 °C
- numerical bisection

The first derivative curve is calculated from adjacent computed pH points.

## Sources

Data references include:

- CRC Handbook of Chemistry and Physics
- Lange's Handbook of Chemistry
- NIST Chemistry WebBook
- general analytical chemistry textbooks
- standard acid-base indicator tables

Values are intended for teaching visualization and may be rounded or simplified for classroom use.

## Makers

- Daniel@猫猫化学团队
- Codex
- ChatGPT

## Version

Version 1.0

Last updated: 2026-07-02

## Open Source Notice

This project may be used for teaching demonstrations, classroom modification, and non-commercial sharing. Please keep the maker and data source notes when redistributing.

## GitHub Pages Deployment

Recommended settings:

1. Repository name: `Acid-Base-Titration`
2. Branch: `main`
3. Pages source: `Deploy from a branch`
4. Folder: `/ (root)`
