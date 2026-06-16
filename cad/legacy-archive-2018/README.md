# Legacy archive 2018 — recovery status

> *Status note for the #43 archive-recovery attempt on the original "Coffee Table" CAD folder. Honest partial/status recovery — not a full asset import.*

## The #43 recovery attempt

Story #43 wanted the full archive **"Coffee Table"** CAD folder copied off the `D:\` external drive into this repo's `cad/` tree.

When I went looking on 2026-06-15, the original archive **"Coffee Table"** folder was **found degraded** — the complete folder is no longer intact on the `D:\` drive. The recovery did not pull in a fresh full copy of that original folder.

## What this repo already has

The good news: this repo's `cad/` tree already carries a substantive 2015-era chessboard / coffee-table SolidWorks set — it predates and does not depend on the degraded `D:\` archive folder. That set lives both at the top of `cad/` and mirrored here under `cad/legacy-archive-2018/coffee-table/`, and includes:

- **Assemblies:** `Checkerboard.SLDASM`, `Wedges Laser Assembly.SLDASM`, `Little Wedges Laser.SLDASM`
- **Top / panels:** `Long Slab.sldprt`, `Short Slab.sldprt`, `Long Panel.sldprt`, `Short Panel Bubinga.sldprt`, `Cherry Mitered Border.SLDPRT`, `quarter inch plywood.sldprt`
- **Chessboard surface:** `Checkerboard Tile.SLDPRT`, `Chessboard Layout.ai`, `Chessboard Layout V2.ai` / `.pdf`
- **Edge band:** `Coffee Table Edge Band.SLDPRT` / `.SLDDRW`, `Coffee Table Edge Band - Short Side.SLDPRT`
- **Structure / legs:** `Cross Beam.sldprt` (+ drawing), `Table Leg.SLDPRT`, `MirrorTable Leg.SLDPRT`, `MirrorMirrorTable Leg.SLDPRT`, `Corner Shelf` / `New Corner Shelf` (`.sldprt`/`.SLDDRW`/`.AI`/`.pdf`)
- **Wedges:** `Wedge.SLDPRT` (+ drawing), `Little Wedge.SLDPRT` (+ drawing), `Wedges Laser.AI`, `Little Wedges Laser.AI`

So the coffee-table CAD is **not** lost — the working set is here and committed. What's missing is specifically the *original full archive "Coffee Table" folder* as it sat on `D:\`, which #43 intended to capture verbatim.

> Note on the sub-manager's finding: #43 was scoped on a report that *only* `Coffee Table Edge Band.PDF` had survived loose at `D:\`. In this worktree I could not find any loose `Coffee Table Edge Band.PDF`, and the repo already holds the full SLDPRT/SLDDRW/.ai set above — richer than that report assumed. The degradation finding applies to the original `D:\` source folder, not to this repo's CAD.

## OPEN — escalate to Tony

- [ ] **Locate the original full "Coffee Table" CAD folder** on another backup or drive (other external HDDs, old laptop, cloud). The `D:\` copy is degraded; confirm whether a clean original exists anywhere before treating the in-repo set as canonical.
- [ ] If no clean original surfaces, decide whether the in-repo `cad/` set is declared canonical and #43 is closed as "recovered from repo working set, source archive degraded."

## Provenance

- Original source: `D:\` external hard drive, archive **"Coffee Table"** folder — found degraded as of 2026-06-15.
- In-repo CAD set: 2015-era SolidWorks files already committed to this repo (see `build-notes/fabrication-handoff.md` — these are historical reference, not yet re-reviewed for current fabrication).

---

*Recovery-status note only — no raw assets added or moved. Refs #43, #212 (tracked in [tonykoop/claude-skills](https://github.com/tonykoop/claude-skills/issues/43)).*
