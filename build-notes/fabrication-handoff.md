# Chessboard Coffee Table - Fabrication Handoff (Scaffold)

> **Status: REVIEW SCAFFOLD - NOT SHOP-READY.**
> This packet indexes the existing CAD archive and lists the fields a shop
> reviewer must fill before any cut is made. No dimension, tolerance, or
> material call-out below is authoritative until each gate is signed off by
> the reviewer.
>
> Refs `tonykoop/chessboard-table#1`.

## 0. CAD / source inventory gate

The repo contains rich CAD inherited from the 2015 build, but it has not been
re-reviewed for current shop fabrication. **Do not treat any of these files as
authoritative** until the gate below is signed off.

| Status | Item |
| --- | --- |
| [ ] | All `cad/*.SLDPRT` parts opened in current SolidWorks and saved without conversion warnings. |
| [ ] | All `cad/*.SLDDRW` drawings opened, title block reviewed, dimensions sanity-checked against parts. |
| [ ] | `cad/*.SLDASM` assemblies open without missing-reference errors and mate cleanly. |
| [ ] | Vector layouts (`Chessboard Layout.ai`, `Chessboard Layout V2.ai/pdf`, `Wedges Laser.AI`, `Corner Shelf.AI`, `New Corner Shelf.AI`, `Little Wedges Laser.AI`) reviewed for scale, units, and registration marks. |
| [ ] | `cad/legacy-archive-2018/coffee-table/` flagged as historical-only; not a primary build source. |
| [ ] | Decision recorded: which CAD files are the *primary build sources* for this packet vs. retained for history. |

Observed CAD components (top-level `cad/`, 2026-05-18 snapshot - **inventory
only, not authority**):

- Top surface: `Checkerboard.SLDASM`, `Checkerboard Tile.SLDPRT`, `Cherry Mitered Border.SLDPRT`, `Chessboard Layout.ai`, `Chessboard Layout V2.ai`, `Chessboard Layout V2.pdf`.
- Edge bands: `Coffee Table Edge Band.SLDPRT`, `Coffee Table Edge Band.SLDDRW`, `Coffee Table Edge Band - Short Side.SLDPRT`.
- Panels / slabs: `Long Panel.sldprt`, `Long Panel.SLDDRW`, `Short Panel Bubinga.sldprt`, `Short Panel Bubinga.SLDDRW`, `Long Slab.sldprt`, `Short Slab.sldprt`.
- Base / legs: `Table Leg.SLDPRT`, `MirrorTable Leg.SLDPRT`, `MirrorMirrorTable Leg.SLDPRT`, `Cross Beam.sldprt`, `Cross Beam Drawing.SLDDRW`.
- Shelving: `Corner Shelf.sldprt`, `Corner Shelf.SLDDRW`, `Corner Shelf.AI`, `Corner Shelf.pdf`, `New Corner Shelf.AI`, `New Corner Shelf.SLDDRW`.
- Wedges (assembly + laser jig): `Wedge.SLDPRT`, `Wedge Drawing.SLDDRW`, `Little Wedge.SLDPRT`, `Little Wedge.SLDDRW`, `Little Wedges Laser.SLDASM`, `Little Wedges Laser.AI`, `Wedges Laser Assembly.SLDASM`, `Wedges Laser Assembly.SLDDRW`, `Wedges Laser.AI`.
- Stock / utility: `quarter inch plywood.sldprt`, `Part2.sldprt`.

## 1. Bill of materials - to be filled by reviewer

Every cell marked `?` must be filled from reviewed CAD before this packet is
treated as shop-ready. Quantities, dimensions, and species are placeholders.

### 1a. Top assembly (chessboard inlay + field + border)

| Component | Source CAD | Qty | Rough size (?) | Finish size (?) | Species (?) | Grain orientation (?) | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Checkerboard tile - light | `Checkerboard Tile.SLDPRT` | 32 | ? | ? | ? | ? | Confirm pair-species with dark tile. |
| Checkerboard tile - dark | `Checkerboard Tile.SLDPRT` | 32 | ? | ? | ? | ? | Two-color alternation; verify cumulative-error budget (see gate 4). |
| Mitered border | `Cherry Mitered Border.SLDPRT` | 4 | ? | ? | cherry (per part name) | ? | Miter angle and corner key (if any) TBD. |
| Field panel - long | `Long Panel.sldprt` / `Long Panel.SLDDRW` | ? | ? | ? | ? | ? | Confirm whether this is solid stock or veneered substrate. |
| Field panel - short | `Short Panel Bubinga.sldprt` / `Short Panel Bubinga.SLDDRW` | ? | ? | ? | bubinga (per part name) | ? | Confirm CITES / movement notes for bubinga (see gate 3). |
| Long slab | `Long Slab.sldprt` | ? | ? | ? | ? | ? | Substrate vs. show surface - clarify. |
| Short slab | `Short Slab.sldprt` | ? | ? | ? | ? | ? | Same as above. |
| Edge band - long side | `Coffee Table Edge Band.SLDPRT` | ? | ? | ? | ? | ? | Confirm whether mitered or butt at corners. |
| Edge band - short side | `Coffee Table Edge Band - Short Side.SLDPRT` | ? | ? | ? | ? | ? | Same. |

### 1b. Base / legs / apron / structure

| Component | Source CAD | Qty | Rough size (?) | Finish size (?) | Species (?) | Joinery (?) | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Table leg | `Table Leg.SLDPRT` | ? | ? | ? | ? | ? | Confirm whether mortise-and-tenon, dowel, floating tenon, or other. |
| Mirrored leg | `MirrorTable Leg.SLDPRT` | ? | ? | ? | ? | ? | Mirror-pair geometry; check orientation in assembly. |
| Double-mirror leg | `MirrorMirrorTable Leg.SLDPRT` | ? | ? | ? | ? | ? | Confirm intent - is this a third unique geometry or a redundant mirror? |
| Cross beam | `Cross Beam.sldprt` / `Cross Beam Drawing.SLDDRW` | ? | ? | ? | ? | ? | Joinery to legs TBD. |
| Apron (if any) | *not found in CAD root* | ? | ? | ? | ? | ? | If table relies on cross beams only, document the no-apron decision. |
| Corner shelf | `Corner Shelf.sldprt` / `Corner Shelf.SLDDRW` / `Corner Shelf.AI` / `Corner Shelf.pdf` | ? | ? | ? | ? | ? | Identify whether current or superseded by `New Corner Shelf.*`. |
| Corner shelf (new) | `New Corner Shelf.AI` / `New Corner Shelf.SLDDRW` | ? | ? | ? | ? | ? | Mark old version as superseded if so. |

### 1c. Wedges / jigs / laser-cut consumables

| Component | Source CAD | Qty | Material (?) | Use (?) | Notes |
| --- | --- | --- | --- | --- | --- |
| Wedge | `Wedge.SLDPRT` / `Wedge Drawing.SLDDRW` | ? | ? | jig / assembly aid? | Confirm whether shipped as part of final piece or jig only. |
| Little wedge | `Little Wedge.SLDPRT` / `Little Wedge.SLDDRW` | ? | ? | ? | Same. |
| Little wedges laser jig | `Little Wedges Laser.SLDASM` / `Little Wedges Laser.AI` | ? | laser-cut sheet | jig | Material thickness TBD (see `quarter inch plywood.sldprt`). |
| Wedges laser assembly | `Wedges Laser Assembly.SLDASM` / `Wedges Laser Assembly.SLDDRW` / `Wedges Laser.AI` | ? | laser-cut sheet | jig | Same. |
| Stock plywood | `quarter inch plywood.sldprt` | ? | 1/4" plywood (per file name - verify) | jig stock | Confirm species/grade. |
| Misc part | `Part2.sldprt` | ? | ? | ? | Identify or remove. |

## 2. Joinery review checklist

- [ ] Top-to-base joinery method documented (e.g., figure-8 fasteners, Z-clips, slotted screw holes) so the **wide solid top can move seasonally** without splitting.
- [ ] Leg-to-cross-beam joinery method documented (mortise & tenon, drawbore, floating tenon, dowel, etc.) with shoulder and cheek tolerances.
- [ ] Border-to-field joinery documented (spline, tongue & groove, glued miter only?) with stress / racking note.
- [ ] Checkerboard tile-to-tile joinery: glue-up sequence, slip-sheet usage, cawl/clamping plan.
- [ ] Each joinery decision tagged "primary load path", "alignment only", or "decorative".

## 3. Material / movement / finish safety gates

- [ ] Species list finalized and cross-checked against CAD part-name hints (`Cherry Mitered Border`, `Short Panel Bubinga`).
- [ ] **Wood movement budget** computed per species pair: tangential vs. radial shrinkage at expected indoor RH swing. Two contrasting species in the checkerboard inlay **will not move at the same rate**; substrate strategy must absorb this.
- [ ] **Cumulative dimensional error** budget for the 64-square grid documented (per-square tolerance × 8 must remain under the border reveal).
- [ ] Bubinga / exotic species: confirm sourcing, CITES status, and any dust-toxicity / sensitization PPE notes (respirator, skin protection).
- [ ] Glue selection documented (open time vs. panel size; PVA vs. hide vs. epoxy for the inlay vs. structural joints).
- [ ] Finish schedule documented end-to-end: surface prep grit progression, raise-grain step, stain or dye (if any), seal coat, build coats, rub-out. Note whether finish is film-forming or penetrating and how it interacts with the two-species color contrast.
- [ ] Finish safety: solvent ventilation, rag-disposal (oil-based finishes are spontaneous-combustion hazards), respirator selection, skin contact.
- [ ] Shop-floor safety for glue-up: clamp pinch points, glue squeeze-out cleanup before cure, slip hazards.

## 4. Assembly / tolerance review checklist

- [ ] Glue-up sequence documented: tile strips first, then strips to panel, then panel into border, then top to base. Each step has a defined flat reference.
- [ ] Per-square tolerance and per-strip tolerance defined; cumulative budget across 8 squares stays under border reveal.
- [ ] Flatness reference: which face is the show face, when is hand-planing vs. drum-sanding vs. scraping used. (Hand-planing across the 64-segment seams is shown in `images/2015-09-20 18.18.27.jpg`; document why and when.)
- [ ] Square (90°) check at each border miter; corner key plan if miters alone are insufficient.
- [ ] Leg-to-top alignment jig or layout method documented.
- [ ] Final flatness / wobble check on assembled table; shim or trim plan if a leg is proud.
- [ ] Photo / measurement record kept of any deviation from CAD so the next iteration learns.

## 5. README / authority statement

The repo README states wood notes, glue-up, and finish schedule are
"forthcoming". Until each gate above is signed off, this packet is the
forthcoming-status placeholder, **not** an authoritative shop document.

Reviewer (sign on completion):

- Name: _______________
- Date: _______________
- Sign-off scope: (CAD only / CAD + BOM / full shop packet)

Until signed, downstream consumers (other repos, future builds, public
documentation) must not cite this packet as fabrication authority.
