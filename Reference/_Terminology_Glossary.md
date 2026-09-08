---
category: Reference
pin: true
brand: ZeroTech
last_updated: 2026-09-08
source: ZeroTech Widget Answer Review (Sep 2026) findings + product Tags/spec vocabulary already used across this repo
---

# ZeroTech Terminology Glossary

## Purpose
Maps what a customer actually types to the spec field, product family, or SKU it means. Every SKU file already carries its own informal `## Tags` — this file is the reverse index: customer language first, ZeroTech term second. `pin: true` above means this file's chunks are always included in chat context, not subject to similarity-search ranking (see AgentSourceChunk.pinned in the backend) — keep it lean; this is a lookup table, not a spec reference.

Add to this file whenever a support ticket or contact-form question uses a term that isn't here. It's meant to grow.

## Product nicknames → official SKU family
Confirmed customer usage, not present anywhere else in this repo before this file:

| Customer says | Means | SKUs |
| --- | --- | --- |
| "Slimline" / "carry optic" / "carry red dot" | Thrive HD Micro Reflex | THDM21 (red), THDM21G (green), THDMM21 (multi-reticle) — 19g, Shield RMSc footprint, built for concealed-carry pistols |

*(Flagged in the Sep 2026 answer review, US-13321: a customer asked about the "ZT Thrive HD Slimline" and the widget denied any such product existed instead of recognizing the nickname. Add further nicknames here as they turn up in real enquiries — don't invent ones nobody has actually used.)*

## Family / tier names
Confirmed from front matter across all categories — `family` and `series` values actually in use:

| Term | Tier | Notes |
| --- | --- | --- |
| Thrive | Accessible / value | `family: Thrive`. Some product lines add a `Thrive HD` series step above base Thrive. |
| Trace | Mid / dedicated red dot & prism systems | `family: Trace`. `Trace Advanced` series is a step up within Trace for scopes/spotting scopes. |
| Vengeance | Premium | `family: Vengeance`. **Has three tiers, not two**: base **Vengeance** (`series: Vengeance`, no suffix — e.g. VG1042, "Vengeance 10x42"), **Vengeance ED** (ED glass, e.g. VG1042ED), and **Vengeance HD** (HD glass, e.g. VG1042HD). A customer asking about "the base Vengeance" or "Vengeance without ED or HD" is asking about a real, existing tier — don't deny it. |

## General customer-language → spec-field mapping

| Customer says | Maps to | Notes |
| --- | --- | --- |
| zoom / zoom range | `Magnification` | e.g. "3-9x" |
| how bright / brightness of the glass / low-light performance | `Light Transmission` (%) | Higher % = brighter image. Distinct from a red dot/prism's illumination brightness *settings* (a count, e.g. "10 brightness settings") — those are reticle intensity steps, not light transmission. |
| clear picture / sharpness / clarity / edge distortion | `Lens Type` (ED/HD/Standard), `Lens Coating`, `Light Transmission` | ED = extra-low dispersion, reduces colour fringing at edges. HD = high-definition glass, brighter. |
| waterproof / can it get wet / water rating | `Waterproof` (Yes/No) | IPX rating (`ipx6`/`ipx7` tags) given where the source spec sheet states one — don't state an IPX number if the SKU's own spec table doesn't have it. |
| red dot / dot sight / reflex sight | Category: **Red Dots** | |
| prism scope / prism sight | Category: **Prisms** | |
| rifle scope / hunting scope / long gun scope | Category: **Riflescopes** | |
| spotter / spotting scope | Category: **Spotting Scopes** | |
| binos | Category: **Binoculars** | |
| FFP / front focal / first focal plane | `Focal Plane: First` | Reticle subtensions are accurate at any magnification. |
| SFP / second focal plane | `Focal Plane: Second` | Reticle subtensions are only accurate at the calibrated power (usually max magnification) — see spec row `Reticle calibrated magnification power (SFP only)`. |
| clicks / MOA clicks / mil clicks | `Turret Index Value` | e.g. "0.25 MOA" or "0.1 MRAD" per click. |
| locking turrets / lockable turrets | Turret spec row + `locking-turret` tag | ZeroTech's lockable turret system is branded **Pop-Lok** — lift-to-adjust, push-to-lock. |
| zero stop | `Zero Stop` (Yes/No) | |
| eye box | `Eye Relief` + `Exit Pupil Diameter` together | Not a single spec field — both contribute to how forgiving the sight picture is. |
| parallax-free / parallax adjustment | `Parallax Adjustment Range` | "Fixed" means no adjustment; a distance range means adjustable. |
| illuminated reticle / lit reticle | `Illumination: Yes` + reticle type | Glass-etched reticles remain visible with illumination off or the battery dead — only the illuminated dot/lines disappear. |
| shake-awake / auto on-off / motion sensor | `shake-awake` / `motion-sensor` tag | Red dot/prism auto-sleep after inactivity, wakes on movement. |
| QD mount / quick-detach | `Mount Type` field, `picatinny-qd` tag | |
| co-witness | Red-dot mount height terminology | Dot sits at the same height as the iron sights so both are visible together. "Low mount" and "high mount" SKU variants exist specifically to set this. |
| footprint / optic cut | `Footprint` spec field (red dots/prisms only) | See `_Compatibility_Guide.md` in this folder for footprint ↔ SKU ↔ firearm mapping. |
| MOS / optics-ready slide | Firearm-side term, not a ZeroTech spec field | See `_Compatibility_Guide.md` — confirm the *specific* footprint the firearm's cut accepts before recommending an optic. |
| thermal scope / thermal imaging / night vision scope | Not carried | ZeroTech does not currently sell thermal imaging optics — say so plainly rather than searching for a near-match; several red dots/prisms are *night-vision-compatible* (a low brightness setting usable with NV devices), which is a different thing from a thermal imager. |

## What this file is not
It doesn't carry prices, URLs, or stock — those stay in their own exact-lookup tables (`get_product_details`). It doesn't carry firearm mounting facts either — that's `_Compatibility_Guide.md`. This file only translates vocabulary.

---
*Last updated: 2026-09-08 · Source: ZeroTech ZT Product KB*
