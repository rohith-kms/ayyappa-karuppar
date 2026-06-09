CHARACTER SHEETS — VISUAL GROUND TRUTH
======================================
Reference plates for every subject in the reel. The text LOCKED BLOCKS that
must be embedded in every sequence prompt live in /CHARACTER_BIBLE.txt
(organized into 5 sections). Each plate here is the visual companion attached
as image reference (--cref / image prompt / IP-Adapter).

------------------------------------------------------------------------------
ACTIVE FOLDERS
------------------------------------------------------------------------------
§1 HEROES
  Karuppar/         — Karuppaswamy turnaround sheet (with cigar) + pose libs
  Ayyappa/          — Character sheet + master portrait
  Mahishi/          — Character sheet + hero portrait
  Shiva/            — Shiva_meditative.png + Shiva_thigh-strike.png (two states)

§2 DIVINE CREATURES
  Bengal-Tiger/     — Ayyappa's mount (NEW)
  War-Horse/        — Karuppar's mount
  Black-Dog/        — Karuppar's hound

§3 ARMY OF DHARMA
  Dharma-Army/      — 4 archetypes (Infantry / Veteran / Commander / Divine General)

§4 ARMY OF THE ASURAS
  Asura-Army/       — 5 archetypes (Infantry / Beast-Blooded / Giant Breaker /
                      Chieftain / Mahishi Elite Guard)

§5 WEAPONS
  Weapons-Catalog/  — Named weapon and standard reference

------------------------------------------------------------------------------
SUPPORT FILES
------------------------------------------------------------------------------
QA-CHECKLIST.txt         — tick every box before approving a new plate
RECONCILIATION_GUIDE.txt — sync LOCKED BLOCK to plate after generation

------------------------------------------------------------------------------
DEPRECATED FOLDERS (kept for archive)
------------------------------------------------------------------------------
Ganas/    — superseded by Dharma-Army/
Asuras/   — superseded by Asura-Army/ (5 archetypes instead of 3)

------------------------------------------------------------------------------
WORKFLOW
------------------------------------------------------------------------------
Most Stage 0 work is DONE — plates are sourced from the team's Final-images
folder and staged into the active subfolders above. The remaining work is:

1. Reconcile LOCKED BLOCKS in CHARACTER_BIBLE.txt against the staged plates
   (see RECONCILIATION_GUIDE.txt → automated via /RECONCILIATION_SPEC.txt)
2. Generate the 4 environment plates (Environment-Sheets/)
3. Begin sequence generation (uses /Sequences/Generate-sequences.txt)
