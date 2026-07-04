---
title: ZeroTech Product Knowledge Base — README
brand: ZeroTech
owner: mj@tsaoutdoors.com.au (TSA Outdoors)
last_updated: 2026-06-26
---

# ZeroTech Product Knowledge Base (ZT Product Repo)

A structured, per-SKU product knowledge base for the ZeroTech Optics range. It exists to be a **single source of truth** that (a) can be read by AI assistants (e.g. Claude) for accurate product answers, and (b) is easy for the TSA team to browse, search, and reuse.

Every product (SKU) has its own Markdown (`.md`) file. Shared operating instructions are factored out into per-model-line **manual reference** files so the SKU files stay lean. Reticle subtension/holdover references live as PDFs in the **Reticles** folder.

> This repository grows over time. New products are added as new `.md` files inside the relevant category folder, and new product categories are added as new folders that follow the same layout described below. Adding products or categories does **not** require changes to this README — revisit it only if the conventions themselves change (the schema, taxonomy rules, or how manuals/reticles are handled).

## Folder structure

The repo is organised into one folder per product category. Each category folder contains one `.md` file per SKU, plus any shared `_*_manual.md` reference files for that category's model lines. Current category folders include:

- `Riflescopes/`
- `Red Dots/`
- `Prisms/`
- `Binoculars/`
- `Spotting Scopes/`
- `Reticles/` — not a product category; a shared library of reticle reference PDFs (see below)

Additional category folders may appear over time; each follows the same per-SKU + shared-manual pattern.

## How each SKU file is structured

Every SKU `.md` opens with a YAML front-matter block, then a fixed body. Front-matter keys:

`sku, model_name, category, family, series, brand, color, manual_ref, has_video, last_updated`

Body sections, in order:
1. `# <Title> (<SKU>)`
2. `## Summary` — one-line positioning
3. `## Specifications` — the full spec table, reproduced **verbatim** from the source spec sheet
4. `## Key features` — from the product Data
5. `## What's in the box` — from the source "In the box" list
6. `## Video insights` — substantive notes from a review transcript, or "No video available"
7. `## Manual` — a lean pointer to the shared manual reference plus a few model-specific bullets
8. `## Tags` — search keywords
9. Footer: `*Last updated: <date> · Source: ZeroTech ZT Product KB*`

## Conventions and rules of the road

- **Specs are authoritative and verbatim.** Spec values, units, and formatting are copied exactly from the source spec sheet — never converted, expanded, or restyled. Where a source is genuinely blank it is shown as-is (e.g. `–`, `NA`, `Blank`). Where a sheet looks internally inconsistent, the discrepancy is **flagged** rather than silently "fixed" (see Known flags).
- **Conflict priority:** Spec sheet → Manual → Data → Video. If two sources disagree, the spec sheet wins in the table and the difference is noted.
- **Taxonomy:** `Category > Family > Series`. Variant tiers (HD / ED / Marine / etc.) are captured in `model_name` and a `Variant` spec row rather than as separate series, except where a tier has historically been its own line (e.g. Thrive HD).
- **Shared manuals:** files prefixed with `_` and ending `_manual.md` are not products — they hold the warranty, setup, care, and safety content shared by a model line. SKU files reference them via `manual_ref` and their `## Manual` section.
- **Customer-review text is excluded**; only structured Data, Specs, and video-transcript-derived insights are used.

## The Reticles folder

`Reticles/` contains ZeroTech's reticle reference PDFs — the source of truth for reticle subtensions, holdovers, and ranging. For most reticles there is a **Reticle Manual** (diagram + usage) and a **Range Chart** (subtension/holdover values), with separate **Illuminated** variants where they exist.

Reticle families covered include: **RMG** (plus RMG MOA, RMG 2, RMG-L, RMG-H), **PHR** (PHR, PHR 2, PHR 3, PHR 4), **R3**, **RAR**, **LR Hunter**, **TREMOR3**, **Mildot**, and **THLR**. The Trace Advanced spotting scope's **OSR** first-focal-plane reticle chart ships with that product and is referenced from its SKU file. Further reticle PDFs may be added here over time.

To find which reticle a given scope uses, check that SKU's file (spec table / manual section), then open the matching PDF here for the subtension detail.

## Known flags (for reconciliation on the source sheets)

Surfaced while building the KB; worth a check by the product team, none blocking:
- **Spotting scopes:** TH206085 & THD206085ED video reviewers say "IPX5" vs spec "IPX6"; TR206080F spec leaves Prism Type and Tripod Compatibility blank (`–`) despite the Data detailing M-LOK/ARCA/Picatinny mounting.
- **Binoculars:** VG1042-M Data markets "dielectric-coated" prisms vs spec "Silver"; VG1042 & VG1042-M show `Variant: Classic` with `Lens Type: ED`; TH1032 Eyepiece Diameter is `Blank`.
- **Red dots:** TRRD125 turret index spec "1 MOA" vs manual/video "0.5 MOA"; THDRS28MGFL reticle spec "3 MOA Green Dot" vs actual multi-reticle; THDP1424 brightness spec "10" vs manual "11" / video "13".
- **Series naming:** Trace red dots use `series: Trace`; the Trace Advanced spotting scope uses `series: Trace Advanced` — align if a single convention is preferred.

## Pending / not yet built
- **Red dots:** THDRS26 and THDRS26-FDE (new; source currently has transcript only) — to be added when spec/Data are available. Series: Thrive HD; will share the Thrive HD RS28 manual reference.

## Maintenance notes
- One file per SKU. Editing is done by replacing the file (there is no in-place edit step); remove superseded duplicates when replacing.
- Keep `last_updated` and the footer current when a file changes.
- Save Markdown directly to the relevant category folder; keep new reticle PDFs in `Reticles/`.
- New products/categories slot into the existing structure and don't require editing this README.

---
*Last updated: 2026-06-26 · Source: ZeroTech ZT Product KB*
