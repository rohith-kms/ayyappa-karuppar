# KARUPPAR REEL — PIPELINE STATUS BOARD

Single source of truth for every stage of the production. Each team updates its
own column when done, then commits + pushes.

============================================================================
STAGE 0 — REFERENCE LIBRARY  (must be done before sequence generation begins)
============================================================================
Generate the master reference plate for each subject. Workflow per subject:
  1. Open the subject's folder, read `Reference-prompt.txt`.
  2. Paste the prompt into Midjourney/Flux/SDXL.
  3. Run the `Character-Sheets/QA-CHECKLIST.txt` against the output.
  4. Save the approved image into that folder as `<Subject>_master_sheet.png`
     (or `_master_plate.png` for environments).
  5. Reconcile the LOCKED BLOCK in the BIBLE to match what was actually drawn —
     see `Character-Sheets/RECONCILIATION_GUIDE.txt`.
  6. Mark DONE in the table below, commit + push.

| Subject                 | Type        | Folder                                     | Plate | Reconciled | WHO |
|-------------------------|-------------|--------------------------------------------|-------|------------|-----|
| Karuppar                | Character   | Character-Sheets/Karuppar/                 | DONE  | DONE       |     |
| War-Horse (standalone)  | Character   | Character-Sheets/War-Horse/                | DONE  |            |     |
| Black-Dog (standalone)  | Character   | Character-Sheets/Black-Dog/                | DONE  |            |     |
| Shiva                   | Character   | Character-Sheets/Shiva/                    |       |            |     |
| Ayyappa                 | Character   | Character-Sheets/Ayyappa/                  | partial |          |     |
| Mahishi                 | Character   | Character-Sheets/Mahishi/                  | partial |          |     |
| Ganas                   | Character   | Character-Sheets/Ganas/                    |       |            |     |
| Asura — Foot-Soldier    | Character   | Character-Sheets/Asuras/Asura_Foot-Soldier/|       |            |     |
| Asura — Brute           | Character   | Character-Sheets/Asuras/Asura_Brute/       |       |            |     |
| Asura — Commander       | Character   | Character-Sheets/Asuras/Asura_Commander/   |       |            |     |
| Battlefield             | Environment | Environment-Sheets/Battlefield/            |       |            |     |
| Kailash                 | Environment | Environment-Sheets/Kailash/                |       |            |     |
| Mahishi's Hill          | Environment | Environment-Sheets/Mahishi-Hill/           |       |            |     |
| Ridgeline               | Environment | Environment-Sheets/Ridgeline/              |       |            |     |

Legend: blank = not started · partial = some artwork exists, not a clean
master plate · DONE = approved master plate saved in the folder · Reconciled
= LOCKED BLOCK in the relevant BIBLE file has been updated to match the plate.

============================================================================
STAGES 1-4 — SEQUENCES  (assembly order top to bottom)
============================================================================
Stage flow: Prompts (producer) → Start/End images (image team) → Animation
(video team) → Approved (producer) → Stitch (editing team).

Mark a cell `DONE` (or `N/A` where a start image isn't needed). "Claim" a
sequence by putting your name in WHO before you start, to avoid two people doing
the same one.

| Seq | Beat | Prompts | Start img | End img | Animation | Approved | WHO |
|-----|------|---------|-----------|---------|-----------|----------|-----|
| 01 | Cold Open | DONE | DONE-when-gen | DONE-when-gen | | | |
| 02 | Battlefield descending | | | | | | |
| 03 | Soldier POV → aerial | | | | | | |
| 04 | Mahishi spawns asuras | | | | | | |
| 05 | Ayyappa eyes close → black | | | | | | |
| 06 | Kailash stillness | | | | | | |
| 07 | Shiva — thigh-strike | | N/A (continues) | | | | |
| 08 | The forging (vortex) | | N/A (continues) | | | | |
| 09 | Back to hell | | | | | | |
| 10 | The silence, freeze | | N/A (continues) | | | | |
| 11 | Ridgeline silhouette | | | | | | |
| 12 | The face — full reveal | | | | | | |
| 13 | First strike | | N/A (continues) | | | | |
| 14 | The Plow | | | | | | |
| 15 | The Spear Ride | | N/A (continues) | | | | |
| 16 | Dismount — bare-handed | | | | | | |
| 17 | The Ashing (close-up) | | | | | | |
| 18 | Chain Storm — AERIAL | | | | | | |
| 19 | The Drag & Beheading | | | | | | |
| 20 | The Rally | | | | | | |
| 21 | Mahishi's Fear | | | | | | |
| 22 | Final Frame — Verdict | | | | | | |

**Legend:** blank = not done · DONE = finished & pushed · N/A = not needed
(sequence continues from the previous end image, so no separate start frame).
