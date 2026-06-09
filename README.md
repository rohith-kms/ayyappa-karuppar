# KARUPPAR — "The One Who Turns the War"

A cinematic ~2-minute trailer reel (2:04 with the Tiger beat insert), built as a 5-stage production pipeline in
one shared Git repo. Everything flows from `Script.txt`.

## The pipeline

0. **Reference library (Stage 0)** — generate and lock master reference plates
   for every character, army archetype, weapon, and environment. These are
   the visual ground truth every later stage anchors to. The character/army
   plates are DONE (sourced from the team's Final-images and staged into
   `Character-Sheets/`). Environment plates remain TODO.
1. **Producer** writes prompts → `Sequences/Sequence_NN/*.txt`
   (Trigger: **`Read Script.txt and RUN`**)
2. **Image team** generates images → `start.png` / `end.png` in each folder
3. **Video team** animates each clip → `animation.mp4` in each folder
4. **Editing team** stitches all 22 clips + sound → the final reel

## Repo layout

```
Karuppar-Reel/
├── README.md                       ← you are here
├── Script.txt                      ← master creative
├── CONFIG.txt                      ← global settings: aspect ratio, CULTURAL
│                                     anchor, ANTI-CLONING token, style, negatives
├── CHARACTER_BIBLE.txt             ← 5 sections: Heroes, Divine Creatures,
│                                     Dharma Army (4 archetypes), Asura Army
│                                     (5 archetypes), Weapons Catalog
├── ENVIRONMENT_BIBLE.txt           ← locked location descriptions
├── AUDIO_NOTES.txt                 ← global sound / music / VO plan
├── STATUS.md                       ← Stage 0 + sequence tracker
├── SEQUENCE_BACKPATCH_SPEC.txt     ← retrofit existing prompts (cheap-model spec)
├── RECONCILIATION_SPEC.txt         ← sync BIBLE to plates (cheap-model spec)
├── Character-Sheets/               ← visual ground truth (mostly DONE)
│   ├── Karuppar/  Ayyappa/  Mahishi/  Shiva/
│   ├── Bengal-Tiger/  (NEW — Ayyappa's mount)
│   ├── War-Horse/  Black-Dog/
│   ├── Dharma-Army/   (4 archetypes; replaces /Ganas)
│   ├── Asura-Army/    (5 archetypes; replaces /Asuras)
│   ├── Weapons-Catalog/
│   ├── QA-CHECKLIST.txt
│   └── RECONCILIATION_GUIDE.txt
├── Environment-Sheets/             ← location plates (TODO)
│   ├── Battlefield/  Kailash/  Mahishi-Hill/  Ridgeline/
├── Final-images/                   ← team's source plates (read-only canon)
│   ├── 00_WORLD_BIBLE/             (army taxonomies + weapons)
│   ├── 02_HERO_MASTERS/            (hero character bibles)
│   └── 03_PATCH_IMAGES/            (Karuppar+cigar, Shiva states)
├── Sequences/
│   ├── Generate-sequences.txt      ← THE ENGINE (Trigger: "Read Script.txt and RUN")
│   ├── SEQUENCE_MAP.txt
│   ├── generation.log
│   └── Sequence_01 … _22/ + Sequence_20.5 (Tiger beat insert)
└── docs/                           ← team guides
```

## The three producer commands

| Goal | Spec to attach | Trigger |
|---|---|---|
| Generate NEW sequence prompts | `Sequences/Generate-sequences.txt` | `Read Script.txt and RUN` |
| Retrofit EXISTING sequence prompts | `SEQUENCE_BACKPATCH_SPEC.txt` | `Read SEQUENCE_BACKPATCH_SPEC.txt and RUN` |
| Sync BIBLE to plates | `RECONCILIATION_SPEC.txt` | `Read RECONCILIATION_SPEC.txt and RUN` |

## The three visual-failure guardrails

1. **Cultural drift** — image models default to Vikings/knights/D&D demons.
   The mandatory `GLOBAL_CULTURAL_TOKEN` in `CONFIG.txt` anchors everything
   to Tamil-Hindu / Sanatan-Dharma iconography.
2. **Clone armies** — image models repeat identical figures in crowd shots.
   The mandatory `GLOBAL_ANTI_CLONING_TOKEN` (new) forces faces, builds, ages,
   weapons, and ornaments to vary within each archetype.
3. **Identity drift** — characters look like different people across shots.
   Identity-Lock lists in each LOCKED BLOCK + reference plates attached as
   image references keep faces consistent.

## How the prompt generation resumes (daily limits)

`generation.log` records the first unfinished sequence. Each `RUN` continues from
there, processes a batch (default 5), and updates the log after **every** sequence
so a cutoff never loses progress.

## The continuity rule

Only `Sequence_01` and `FRESH_START` sequences (hard cuts) get a **start** image.
`CONTINUES` sequences inherit the previous sequence's `end.png` as their start
frame. See `SEQUENCE_MAP.txt`.

## Golden rule for all teams

In GitHub Desktop: **Pull before you start, Push when you finish.**
New here? Read `docs/GITHUB_FOR_BEGINNERS.txt`.
