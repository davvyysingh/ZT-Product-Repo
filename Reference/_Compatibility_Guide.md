---
category: Reference
pin: true
brand: ZeroTech
last_updated: 2026-09-08
source: Aggregated from Footprint/Mount Type spec rows already in Red Dots/ and Prisms/ SKU files. Firearm-side table is a template — see "Firearm → footprint" below before relying on it.
---

# ZeroTech Optic Compatibility Guide

## How to use this
For a mounting/fit question: identify the ZeroTech optic's footprint below, then check what the customer's firearm/rail natively accepts. State fit only with the specific footprint or adapter plate named — never imply a bare slide or rail takes an optic without checking both sides.

## ZeroTech optic → footprint
Pulled directly from each SKU's own `Footprint` / `Mount Type` spec row — this table is only as current as those files; if a SKU here is missing, it hasn't shipped a documented footprint yet and should be checked against its own file, not guessed from this table.

### Aimpoint® Micro / T-2 footprint
Mounts directly to any Picatinny/Weaver rail via the included mount — no plate needed on a railed firearm.

| SKU | Model | Mount |
| --- | --- | --- |
| THRD22 | Thrive HD 1x22 2 MOA Digital Red Dot | Multiple (ships with high + low) |
| THRD25 | Thrive Reflex Sight 3 MOA | Low |
| TRRD125 | Trace R.A.S 1x25 2 MOA Digital Red Dot | Multiple (ships with high + low) |
| THDMP120 / THDMP120-FDE | Thrive HD 1x Micro Prism – Prism Dot Illuminated | Multiple |

### Trijicon RMR® footprint
Direct-mounts to any pistol slide with a factory or aftermarket RMR-pattern cut. Also rail-mountable via the included Picatinny mount.

| SKU | Model | Mount |
| --- | --- | --- |
| THDRS28H | Thrive HD Reflex Sight 3 MOA | High |
| THDRS28L | Thrive HD Reflex Sight 3 MOA | Low |
| THDRS28GH | Thrive HD Reflex Sight Green 3 MOA | High |
| THDRS28GL | Thrive HD Reflex Sight Green 3 MOA | Low |
| THDRS28MH | Thrive HD Reflex Sight Multi Reticle | High |
| THDRS28ML | Thrive HD Reflex Sight Multi Reticle | Low |
| THDRS28MGFL | Thrive HD Reflex Sight Green Multi Reticle (FDE) | Low |

### Shield RMSc footprint
Direct-mounts to compact/slimline pistol slides with an RMSc-pattern cut. Ultra-light, no rail mount included as standard — see the Terminology Glossary for the "Slimline" nickname mapping to this family.

| SKU | Model | Mount |
| --- | --- | --- |
| THDM21 | Thrive HD Micro Reflex Sight 3 MOA | None (direct-mount only) |
| THDM21G | Thrive HD Micro Reflex Sight Green 3 MOA | None (direct-mount only) |
| THDMM21 | Thrive HD Micro Reflex Sight Multi Reticle | None (direct-mount only) |

### Shield RMSc footprint + Picatinny rail mount included
Same RMSc slide footprint as above, but ships with an additional Picatinny adapter so it also mounts to rails.

| SKU | Model | Mount |
| --- | --- | --- |
| TRAE28 | Trace H.A.L.O Enclosed Reflex Sight 3 MOA | Low |
| TRAE28-FDE | Trace H.A.L.O Enclosed Reflex Sight 3 MOA (FDE) | Low |
| TRAE28G | Trace H.A.L.O Enclosed Reflex Sight Green 3 MOA | — |

### Mini ACOG footprint
| SKU | Model | Mount |
| --- | --- | --- |
| THDP1424 | Thrive HD 1-4x24 Variable Prism – RAP-R Illuminated | Neutral |

## Firearm / rail → footprint
**This section is intentionally a template, not filled in.** The mounting facts above come straight from ZeroTech's own spec sheets; which specific firearm models/generations accept which footprint natively is outside this repo's own data, varies by generation and sometimes by exact SKU (a factory optics-ready cut isn't guaranteed identical across every variant of a model line), and got flagged as an unverified/incorrect claim more than once in the Sep 2026 answer review when stated with confidence anyway. Rather than repeat that mistake here, add rows below only once confirmed — cite the manufacturer's own spec sheet, not general recollection:

| Firearm / rail | Native footprint | Adapter plate needed? | Source | Confirmed by |
| --- | --- | --- | --- | --- |
| *(add as confirmed — e.g. "Glock MOS, plate 08")* | | | | |

Enquiries already sitting on this exact gap, worth confirming first:
- Sig P320 (which generation/cut?) — factory optic-cut naming needs verification before it's stated as fact (flagged US-13705).
- Springfield Echelon VIS system — exact footprint list it accepts natively needs verification against Springfield's own spec sheet (flagged US-15810).
- CZ P10F, ZEV OZ9 — a customer-facing answer previously stated these as native RMR cuts; verify before restating.

## What this file is not
It doesn't cover reticle subtension/holdover — that's the PDF files in `Reticles/`, linked via `get_reticle_reference`, not summarized here. It doesn't cover pricing or stock.

---
*Last updated: 2026-09-08 · Source: ZeroTech ZT Product KB*
