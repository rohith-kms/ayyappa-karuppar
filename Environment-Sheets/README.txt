ENVIRONMENT SHEETS
==================
Reference plates for the four locations in the reel. Each location folder
contains:
  Reference-prompt.txt          — paste-ready generation prompt for the plate
  README.txt                    — short workflow note
  <Place>_master_plate.png      — the approved plate (once generated)

The text LOCKED BLOCKS that every later sequence prompt embeds live in
/ENVIRONMENT_BIBLE.txt. The plate is the visual companion.

------------------------------------------------------------------------------
LOCATIONS
------------------------------------------------------------------------------
Battlefield/      The cursed plain — appears in Movements I, III, IV (most sequences)
Kailash/          Shiva's abode — Movement II only (sequences 06–08)
Mahishi-Hill/     The spawning hill — sequence 04 and 21
Ridgeline/        Karuppar's arrival — sequence 11 only (the iconic frame)

------------------------------------------------------------------------------
WORKFLOW  (Stage 0)
------------------------------------------------------------------------------
1. Open a location folder, read Reference-prompt.txt
2. Paste the prompt into Midjourney/Flux/SDXL
3. Run /Character-Sheets/QA-CHECKLIST.txt against the output
4. Save approved image as <Place>_master_plate.png in that folder
5. Run reconciliation (see /Character-Sheets/RECONCILIATION_GUIDE.txt) against
   /ENVIRONMENT_BIBLE.txt
6. Update /STATUS.md Stage 0
