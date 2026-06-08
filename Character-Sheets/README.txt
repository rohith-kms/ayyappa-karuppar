CHARACTER SHEETS
================
Reference plates for every character (and asura variant). Each subject folder
contains:
  Reference-prompt.txt   — paste-ready generation prompt for the master plate
  README.txt             — short workflow note
  <Subject>_master_sheet.png — the approved plate (once generated)

The text LOCKED BLOCKS that must go into every later sequence prompt live in
/CHARACTER_BIBLE.txt. The plate is the visual companion attached as a reference
(--cref / image prompt / IP-Adapter).

Files at this level:
  QA-CHECKLIST.txt         — tick every box before approving a plate
  RECONCILIATION_GUIDE.txt — after approval, sync the locked block to the plate

------------------------------------------------------------------------------
STATUS  (also tracked in /STATUS.md Stage 0)
------------------------------------------------------------------------------
Karuppar/                       DONE — 4 master sheets supplied
Karuppar/War-Horse panel        DONE (also: standalone in War-Horse/)
Karuppar/Black-Dog panel        DONE (also: standalone in Black-Dog/)
Shiva/                          TODO — Reference-prompt.txt ready
Ayyappa/                        TODO — Reference-prompt.txt ready (partial art exists)
Mahishi/                        TODO — Reference-prompt.txt ready (partial art exists)
Ganas/                          TODO — Reference-prompt.txt ready
Asuras/                         TODO — 3 variants (Foot-Soldier, Brute, Commander)

------------------------------------------------------------------------------
WORKFLOW  (Stage 0 — must complete before sequence generation)
------------------------------------------------------------------------------
1. Open a subject's folder, read Reference-prompt.txt
2. Paste the prompt into your image tool (Midjourney/Flux/SDXL)
3. Run QA-CHECKLIST.txt against the output
4. Save approved image as <Subject>_master_sheet.png in that folder
5. Run RECONCILIATION_GUIDE.txt — update the LOCKED BLOCK to match the plate
6. Update STATUS.md, commit + push
