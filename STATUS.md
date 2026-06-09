# KARUPPAR REEL — PIPELINE STATUS BOARD

Single source of truth for every stage of the production. Each team updates its
own column when done, then commits + pushes.

============================================================================
STAGE 0 — REFERENCE LIBRARY  (the visual ground truth)
============================================================================
Stage 0 is now in TWO halves: the 18 character/army plates (all DONE — staged
from Final-images by the team) and the 4 environment plates (TODO).

For each plate: tick `Plate` once the file is in its folder. Tick `Reconciled`
once the matching LOCKED BLOCK in CHARACTER_BIBLE.txt / ENVIRONMENT_BIBLE.txt
has been updated to describe what the plate actually shows
(see /Character-Sheets/RECONCILIATION_GUIDE.txt + /RECONCILIATION_SPEC.txt).

| §  | Subject                                       | Folder                                                  | Plate | Reconciled | WHO |
|----|-----------------------------------------------|---------------------------------------------------------|-------|------------|-----|
| 1  | Karuppar (with cigar — patch)                 | Character-Sheets/Karuppar/                              | DONE  |            |     |
| 1  | Ayyappa                                       | Character-Sheets/Ayyappa/                               | DONE  |            |     |
| 1  | Mahishi                                       | Character-Sheets/Mahishi/                               | DONE  |            |     |
| 1  | Shiva — MEDITATIVE state                      | Character-Sheets/Shiva/Shiva_meditative.png             | DONE  |            |     |
| 1  | Shiva — WRATHFUL THIGH-STRIKE state           | Character-Sheets/Shiva/Shiva_thigh-strike.png           | DONE  |            |     |
| 2  | Bengal Tiger (Ayyappa's mount — NEW)          | Character-Sheets/Bengal-Tiger/                          | DONE  |            |     |
| 2  | White Horse (Karuppar's mount)                | Character-Sheets/War-Horse/                             | DONE  |            |     |
| 2  | Black Dog (Karuppar's hound)                  | Character-Sheets/Black-Dog/                             | DONE  |            |     |
| 3  | Dharma Army — Archetype A (Infantry)          | Character-Sheets/Dharma-Army/                           | DONE  |            |     |
| 3  | Dharma Army — Archetype B (Veteran)           | Character-Sheets/Dharma-Army/                           | DONE  |            |     |
| 3  | Dharma Army — Archetype C (Commander)         | Character-Sheets/Dharma-Army/                           | DONE  |            |     |
| 3  | Dharma Army — Archetype D (Divine General)    | Character-Sheets/Dharma-Army/                           | DONE  |            |     |
| 4  | Asura Army — Archetype A (Infantry)           | Character-Sheets/Asura-Army/                            | DONE  |            |     |
| 4  | Asura Army — Archetype B (Beast-Blooded)      | Character-Sheets/Asura-Army/                            | DONE  |            |     |
| 4  | Asura Army — Archetype C (Giant Breaker)      | Character-Sheets/Asura-Army/                            | DONE  |            |     |
| 4  | Asura Army — Archetype D (Chieftain)          | Character-Sheets/Asura-Army/                            | DONE  |            |     |
| 4  | Asura Army — Archetype E (Mahishi Elite Guard) | Character-Sheets/Asura-Army/                           | DONE  |            |     |
| 5  | Weapons & Standards Catalog                   | Character-Sheets/Weapons-Catalog/                       | DONE  |            |     |
| Env| Battlefield                                   | Environment-Sheets/Battlefield/                         | DONE  |            |     |
| Env| Kailash                                       | Environment-Sheets/Kailash/                             | DONE  |            |     |
| Env| Mahishi's Hill                                | Environment-Sheets/Mahishi-Hill/                        | DONE  |            |     |
| Env| Ridgeline                                     | Environment-Sheets/Ridgeline/                           | DONE  |            |     |

Legend: blank = not started · DONE = plate saved in folder · Reconciled =
LOCKED BLOCK in BIBLE has been updated to match the plate.

DEPRECATED FOLDERS (kept for archive, do not generate new plates here):
  Character-Sheets/Ganas/     → superseded by Character-Sheets/Dharma-Army/
  Character-Sheets/Asuras/    → superseded by Character-Sheets/Asura-Army/
                                (with 5 archetypes instead of 3)

============================================================================
STAGES 1-4 — SEQUENCES  (assembly order top to bottom)
============================================================================
Stage flow: Prompts (producer) → Start/End images (image team) → Animation
(video team) → Approved (producer) → Stitch (editing team).

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
| 20.5 | Ayyappa Unleashed — Tiger Rides | | | | | | |
| 21 | Mahishi's Fear | | | | | | |
| 22 | Final Frame — Verdict | | | | | | |

**Legend:** blank = not done · DONE = finished & pushed · N/A = not needed
(sequence continues from the previous end image).
