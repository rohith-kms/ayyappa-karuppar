Dharma Army — Ayyappa's Forces  (replaces former /Ganas folder)
===============================================================
Four archetypes, all visually distinct, all sharing the same Tamil-Hindu
warrior aesthetic:

  Archetype A — Dharma Infantry         (5'8"-6'0", frontline)
  Archetype B — Veteran Warrior         (6'1"-6'5", battle-hardened)
  Archetype C — Commander               (6'4"-6'10", unit leader, standard)
  Archetype D — Divine General          (6'10"-7'4", supreme rank)

Each archetype has its own LOCKED BLOCK in /CHARACTER_BIBLE.txt §3.

Master plates in this folder:
  Dharma-Army_full_formation.png       — the full army arrayed (visual sense
                                          of the rank pyramid)
  Dharma-Army_character_system.png     — the four archetypes side-by-side,
                                          labeled, with their stats — THIS
                                          is the canonical reference
  Dharma-Army_character_system_v2.png  — alternate cleaner version with same
                                          archetypes

PER-PROMPT WORKFLOW:
1. Check SEQUENCE_BACKPATCH_SPEC.txt for the per-beat archetype mix.
2. Embed the LOCKED BLOCK from CHARACTER_BIBLE.txt §3 for each archetype
   present in the beat.
3. Attach Dharma-Army_character_system.png as the reference plate (pointing
   to the relevant archetype panel in IMAGE REFERENCES).
4. If ≥3 figures of the same archetype, inject the ANTI_CLONING_TOKEN from
   CONFIG.txt.

ANTI-CLONING (CRITICAL): the four archetypes already define the rank-level
variation. WITHIN each archetype, the model must still vary faces, builds,
ages, hair, beards, and ornament. The anti-cloning token handles this.
