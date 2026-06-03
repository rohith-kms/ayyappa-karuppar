# KARUPPAR — "The One Who Turns the War"

A cinematic ~2-minute trailer reel, built as a 4-stage production pipeline in one
shared Git repo. Everything flows from `Script.txt`.

## The pipeline

1. **Producer** writes prompts → `Sequences/Sequence_NN/*.txt`
   (open the Claude project, attach this repo, type **`Read Script.txt and RUN`**)
2. **Image team** generates images → `start.png` / `end.png` in each folder
3. **Video team** animates each clip → `animation.mp4` in each folder
4. **Editing team** stitches all 22 clips + sound → the final reel

## Repo layout

```
Karuppar-Reel/
├── README.md                  ← you are here
├── Script.txt                 ← the master creative (the whole reel in words)
├── CONFIG.txt                 ← global settings (aspect ratio, style) — CONFIRM first
├── CHARACTER_BIBLE.txt        ← locked character descriptions (visual consistency)
├── AUDIO_NOTES.txt            ← global sound / music / VO plan (editing team)
├── STATUS.md                  ← who's done what + the final assembly order
├── .gitattributes / .gitignore
├── Character-Sheets/          ← reference art (Karuppar supplied; others TODO)
├── Sequences/
│   ├── Generate-sequences.txt ← THE ENGINE (how "RUN" works)
│   ├── SEQUENCE_MAP.txt        ← fixed list of all 22 sequences + continuity flags
│   ├── generation.log          ← resume point (survives daily limits)
│   └── Sequence_01 … _22/       ← prompts + generated images + animation per beat
└── docs/
    ├── 00_START_HERE.txt
    ├── GITHUB_FOR_BEGINNERS.txt  ← non-technical, GitHub Desktop, click-by-click
    ├── IMAGE_TEAM_GUIDE.txt
    ├── VIDEO_TEAM_GUIDE.txt
    └── EDITING_TEAM_GUIDE.txt
```

## How the prompt generation resumes (daily limits)

`generation.log` records the first unfinished sequence. Each `RUN` continues from
there, processes a batch (default 5), and updates the log after **every** sequence
so a cutoff never loses progress. `Sequence_01` is supplied as a worked example;
the engine resumes at `Sequence_02`.

## The continuity rule

Only `Sequence_01` and `FRESH_START` sequences (hard cuts) get a **start** image.
`CONTINUES` sequences inherit the previous sequence's `end.png` as their start
frame — saving generation effort where the picture is truly continuous. Each
sequence's `Animation-prompt.txt` states its start source. See `SEQUENCE_MAP.txt`.

## Before anyone starts

Confirm the three `[CONFIRM]` values in `CONFIG.txt` (aspect ratio + which image /
video tools). Everything downstream uses them.

## Golden rule for all teams

In GitHub Desktop: **Pull before you start, Push when you finish.**
New here? Read `docs/GITHUB_FOR_BEGINNERS.txt` — no command line, just buttons.
