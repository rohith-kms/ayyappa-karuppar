# KARUPPAR — "The One Who Turns the War"

A cinematic ~2-minute trailer reel, built as a 5-stage production pipeline in
one shared Git repo. Everything flows from `Script.txt`.

## The pipeline

0. **Reference library (Stage 0)** — generate and lock the master reference
   plates for every character, asura variant, and environment first. These
   become the visual ground truth every later stage anchors to.
   See `Character-Sheets/`, `Environment-Sheets/`, and the `Reference-prompt.txt`
   inside each subject folder.
1. **Producer** writes prompts → `Sequences/Sequence_NN/*.txt`
   (open the Claude project, attach this repo, type **`Read Script.txt and RUN`**)
2. **Image team** generates images → `start.png` / `end.png` in each folder
3. **Video team** animates each clip → `animation.mp4` in each folder
4. **Editing team** stitches all 22 clips + sound → the final reel

## Repo layout

```
Karuppar-Reel/
├── README.md                       ← you are here
├── Script.txt                      ← the master creative (the whole reel in words)
├── CONFIG.txt                      ← global settings (aspect ratio, cultural
│                                     anchor, style, negatives) — CONFIRM first
├── CHARACTER_BIBLE.txt             ← locked character descriptions
├── ENVIRONMENT_BIBLE.txt           ← locked location descriptions
├── AUDIO_NOTES.txt                 ← global sound / music / VO plan
├── STATUS.md                       ← reference library + sequence tracker
├── SEQUENCE_BACKPATCH_SPEC.txt     ← mechanical spec for retrofitting old
│                                     sequence prompts with the new globals
├── .gitattributes / .gitignore
├── Character-Sheets/               ← character reference plates + prompts
│   ├── README.txt
│   ├── QA-CHECKLIST.txt
│   ├── RECONCILIATION_GUIDE.txt
│   ├── Karuppar/                   (sheets supplied)
│   ├── Shiva/                      Reference-prompt.txt
│   ├── Ayyappa/                    Reference-prompt.txt
│   ├── Mahishi/                    Reference-prompt.txt
│   ├── War-Horse/                  Reference-prompt.txt
│   ├── Black-Dog/                  Reference-prompt.txt
│   ├── Ganas/                      Reference-prompt.txt
│   └── Asuras/
│       ├── README.txt              (router)
│       ├── Asura_Foot-Soldier/     Reference-prompt.txt
│       ├── Asura_Brute/            Reference-prompt.txt
│       └── Asura_Commander/        Reference-prompt.txt
├── Environment-Sheets/             ← location reference plates + prompts
│   ├── README.txt
│   ├── Battlefield/                Reference-prompt.txt
│   ├── Kailash/                    Reference-prompt.txt
│   ├── Mahishi-Hill/               Reference-prompt.txt
│   └── Ridgeline/                  Reference-prompt.txt
├── Sequences/
│   ├── Generate-sequences.txt      ← THE ENGINE (how "RUN" works)
│   ├── SEQUENCE_MAP.txt            ← fixed list of all 22 sequences
│   ├── generation.log              ← resume point (survives daily limits)
│   └── Sequence_01 … _22/          ← prompts + generated images + animation
└── docs/
    ├── 00_START_HERE.txt
    ├── GITHUB_FOR_BEGINNERS.txt    ← GitHub Desktop, click-by-click
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

## The cultural anchor (why this project's prompts look different)

Image models default to Western martial imagery (Vikings, knights, generic
D&D demons) because their training data skews Western. This project's prompts
include a mandatory **GLOBAL_CULTURAL_TOKEN** anchoring every generation to
Tamil-Hindu / Sanatan-Dharma iconography, plus an expanded negative-prompt
list that explicitly rules out Western fantasy tropes. See `CONFIG.txt`.

## Before anyone starts

Confirm the three `[CONFIRM]` values in `CONFIG.txt` (aspect ratio + which image /
video tools). Everything downstream uses them.

## Golden rule for all teams

In GitHub Desktop: **Pull before you start, Push when you finish.**
New here? Read `docs/GITHUB_FOR_BEGINNERS.txt` — no command line, just buttons.
