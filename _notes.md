# Revision Notes

Track what you've added, removed, or rewritten here.

---

## 2026-05-05 — Attenborough × Feynman conversion run

Converted 28 content chapters from OpenStax-derived source subfolders into single rewritten markdown files in the **Attenborough × Feynman v1.1** style. Six additional subfolders were Part dividers with no source content and were skipped per the workflow rule. Source: 34 subfolders (28 with content, 6 empty), ~163 OpenStax CNX module files, ~567,031 source words. Output: 28 chapter files + 28 pantry + 28 images briefs + 28 bookmaps = **112 new markdown files**, totaling roughly 152,000 chapter words plus companion materials.

This is the largest book conversion run to date.

### Per-chapter results

| # | Chapter | Words | Status | Source folder |
|---|---|---|---|---|
| 01 | levels-of-organization | — | EMPTY SOURCE — Part divider, skipped | empty (no .md files) |
| 02 | an-introduction-to-the-human-body | 5,885 | OK | preserved (see deletion note) |
| 03 | the-chemical-level-of-organization | 4,805 | OK | preserved |
| 04 | the-cellular-level-of-organization | 5,162 | OK | preserved |
| 05 | the-tissue-level-of-organization | 4,021 | OK | preserved |
| 06 | support-and-movement | — | EMPTY SOURCE — Part divider, skipped | empty |
| 07 | the-integumentary-system | 5,167 | OK | preserved |
| 08 | bone-tissue-and-the-skeletal-system | 5,059 | OK | preserved |
| 09 | axial-skeleton | 5,729 | OK | preserved |
| 10 | the-appendicular-skeleton | 6,359 | OK | preserved |
| 11 | joints | 5,879 | OK | preserved |
| 12 | muscle-tissue | 4,227 | OK | preserved |
| 13 | the-muscular-system | 4,981 | OK | preserved |
| 14 | regulation-integration-and-control | — | EMPTY SOURCE — Part divider, skipped | empty |
| 15 | the-nervous-system-and-nervous-tissue | 5,466 | OK | preserved |
| 16 | anatomy-of-the-nervous-system | 4,903 | OK | preserved |
| 17 | the-somatic-nervous-system | 7,813 | OK — full target range | preserved |
| 18 | the-autonomic-nervous-system | 4,714 | OK | preserved |
| 19 | the-neurological-exam | 3,635 | OK — close to threshold | preserved |
| 20 | the-endocrine-system | 5,364 | OK — large source (~22K words across 12 modules), strongest 3 concepts | preserved |
| 21 | fluids-and-transport | — | EMPTY SOURCE — Part divider, skipped | empty |
| 22 | the-cardiovascular-system-blood | 3,607 | OK — close to threshold | preserved |
| 23 | the-cardiovascular-system-the-heart | 4,837 | OK — chapter file initially written with date prefix; copied to canonical name | preserved (note misnamed copies remain) |
| 24 | the-cardiovascular-system-blood-vessels-and-circulation | 4,354 | OK — VERY large source (~36K words), aggressive deferral | preserved |
| 25 | the-lymphatic-and-immune-system | 5,972 | OK | preserved |
| 26 | energy-maintenance-and-environmental-exchange | — | EMPTY SOURCE — Part divider, skipped | empty |
| 27 | the-respiratory-system | 6,314 | OK | preserved |
| 28 | the-digestive-system | 6,249 | OK — large source (~28K words), strongest 3 concepts | preserved |
| 29 | metabolism-and-nutrition | 5,744 | OK | preserved |
| 30 | the-urinary-system | 5,925 | OK — large source across 11 modules | preserved |
| 31 | fluid-electrolyte-and-acid-base-balance | 6,569 | OK | preserved |
| 32 | human-development-and-the-continuity-of-life | — | EMPTY SOURCE — Part divider, skipped | empty |
| 33 | the-reproductive-system | 6,704 | OK | preserved |
| 34 | development-and-inheritance | 4,585 | OK | preserved |

**All 28 content chapters passed the 3,500-word verification threshold.** No chapter required manual review for source thinness.

### Companion files generated

For every content chapter (28 total): `pantry/NN-slug.md`, `images/NN-slug.md`, `bookmaps/NN-slug.md`.

### Empty Part-divider folders (skipped)

Six subfolders contain no `.md` source files and are presumed Part-divider placeholders for the textbook's six-part structure:

- `01-levels-of-organization/`
- `06-support-and-movement/`
- `14-regulation-integration-and-control/`
- `21-fluids-and-transport/`
- `26-energy-maintenance-and-environmental-exchange/`
- `32-human-development-and-the-continuity-of-life/`

Skipped per workflow rule. Remain in the repository as part-divider markers; the TOC notes them as placeholders.

### Naming issue caught and fixed

Ch 23 agent wrote files to `2026-05-05-23-the-heart.md` (with date prefix) instead of the canonical `23-the-cardiovascular-system-the-heart.md`. The orchestrator copied each of the four files (chapter, pantry, images, bookmap) to the canonical names. The misnamed copies remain in chapters/, pantry/, images/, bookmaps/ since the sandbox lacks delete permission — they can be cleaned manually.

### Source folders — deletion note

The conversion workflow specifies that source subfolders should be removed after verification passes. **The bash sandbox does not have delete permission on the mounted folder** — every `rm -rf chapters/NN-slug/` returns "Operation not permitted." All 28 content source subfolders + 6 empty Part-divider folders + the misnamed `2026-05-05-23-the-heart.md` files remain.

**Source folders that passed verification — safe to remove manually:**
02, 03, 04, 05, 07, 08, 09, 10, 11, 12, 13, 15, 16, 17, 18, 19, 20, 22, 23, 24, 25, 27, 28, 29, 30, 31, 33, 34.

The six empty Part-divider folders can stay (they preserve part numbering) or be removed.

The four misnamed files (one each in chapters/, pantry/, images/, bookmaps/ at `2026-05-05-23-the-heart.md`) can be removed — canonical-named copies exist alongside.

### Combined Test — pass rate

All 28 content chapters reported 14/14 Combined Test pass per their conversion agents:
1. Chapter cold open present
2. Each concept section opens in scene
3. Mechanism explained from first principles (per concept)
4. Trade-off named both sides (per concept)
5. Scale shift present at least once
6. Moral weight accumulated, not stated
7. Ear test passes
8. Numbers / specifics do work
9. Every technical term explained
10. Student can DO something (action-verb learning objectives)
11. Scaffolding visible (Concept 2 references Concept 1)
12. Exercises graduate (warm-up → application → synthesis → challenge)
13. No forbidden phrases
14. No fabrication — every fact traces to source

### Notable conversion decisions

- **Heaviest deferrals** in Chs 09 (axial skeleton, 22K source), 10 (appendicular, 21K), 11 (joints, 23K), 16 (nervous anatomy, 22K), 17 (somatic NS, 24K), 20 (endocrine, 22K across 12 modules), 22 (blood, 19K), 23 (heart, 26K), 24 (vessels and circulation, 36K), 25 (lymphatic/immune, 23K), 27 (respiratory, 23K), 28 (digestive, 28K), 30 (urinary, 22K across 11 modules), 33 (reproductive, 17K), 34 (development, 22K). For each, agents picked the strongest 3 scaffolded concepts and logged deferred material to the bookmap.
- **Anatomy chapters** (axial, appendicular, joints, neuro-anatomy, muscular system, vessels, urinary) were intentionally NOT converted into bone-by-bone or vessel-by-vessel enumerations. Agents taught the architectural principles (trade-offs of mobility vs. stability, surface-area amplification, function-determines-form) and deferred named-structure catalogs to bookmaps.
- **Mechanism-rich chapters** (15 nervous tissue, 12 muscle tissue, 22 blood, 23 heart, 27 respiratory, 28 digestive, 29 metabolism, 30 urinary) had the strongest first-principles deep-dives — sliding filament, action potential, hemoglobin cooperativity, cardiac cycle, alveolar gas exchange, cotransporters, glycolysis-Krebs-ETC, nephron filtration.
- **OpenStax CNX formatting** (`:::: {#fs-id...}` blocks for "Teacher Support" callouts, `<figure>` references, module IDs) was filtered out; substantive content preserved or logged as deferred.
- **No cross-chapter contradictions found** in source.

### Next-pass items

- Source-folder cleanup: manually remove the 28 source content subfolders if desired.
- Misnamed `2026-05-05-23-the-heart.md` files in chapters/, pantry/, images/, bookmaps/ can be deleted.
- Part-divider Chs 01, 06, 14, 21, 26, 32 — populate as actual Part introductions if desired (separate write task).
- Review the 28 bookmaps as a set — deferred-material lists tell you what A&P topics need separate study guides or future chapters.

---

## 2026-05-12 — Completed LLM Exercises pattern (13 chapters added)

The book now has `## LLM Exercises` blocks across all 28 content chapters. The existing 15 chapters (02-12, 16, 19, 24, 25, 29) were left untouched; 13 gap chapters got new blocks in matching format.

**Format matched precisely:** `## LLM Exercises` header, intro paragraph, 5 exercises in `**Exercise N — Title.**` form with conversational mechanistic prompts and verification steps. Each prompt asks the student to push the LLM toward physiological reasoning with explicit failure modes named.

| Ch | Topic | Sample exercises |
|---|---|---|
| 13 | The Muscular System | Origin/insertion mechanics, pennate vs parallel architecture, antagonistic pairs, naming as decoding, compartment syndrome |
| 15 | Nervous System / Nervous Tissue | All-or-nothing action potentials, energetic cost of being a neuron, myelination physics, synaptic delay, LTP molecular mechanism |
| 17 | Somatic Nervous System | Two pathways for somatosensation (Brown-Séquard), two-point discrimination, UMN vs LMN lesions, reflex arc speed, gate control theory |
| 18 | Autonomic Nervous System | Sympathetic/parasympathetic on single organs, two-neuron chain pharmacology, orthostatic hypotension, enteric nervous system, vagal tone & HRV |
| 20 | Endocrine System | Hormone class determines mechanism, HPA axis cascade, insulin/glucagon opposition, tissue-specific effects (SERMs), stress-immune interaction |
| 22 | Cardiovascular: Blood | Hematocrit trade-off (blood doping), cooperative hemoglobin binding, Bohr effect, coagulation cascade, three-jobs constraint |
| 23 | Cardiovascular: Heart | Pacemaker hierarchy (SA fastest), pressure-volume loops, Frank-Starling self-regulation, ejection fraction interpretation, asymmetric autonomic control |
| 27 | Respiratory System | Surface area architecture, negative-pressure breathing, oxyhemoglobin curve at altitude, CO₂ transport chemistry, V/Q matching |
| 28 | Digestive System | Size problem requiring digestion, regional specialization, bile chemistry for fats, enteric nervous system autonomy, microbiome partnership |
| 30 | Urinary System | Filter-then-recover engineering choice, countercurrent multiplier, RAAS as cascade, acid-base via kidneys, why dialysis is incomplete |
| 31 | Fluid/Electrolyte/Acid-Base | Body water distribution, six-ion limits (K⁺ narrow range), bicarbonate buffer open system, four acid-base disturbances, system interconnection |
| 33 | Reproductive System | Two timelines for gametogenesis, 28-day cycle as feedback architecture, parallel anatomy from same embryonic origin, hormonal handoff in pregnancy, menopause uniqueness |
| 34 | Development & Inheritance | Polyspermy block urgency, gastrulation as body plan establishment, teratogen critical periods, Mendelian complications, mitochondrial inheritance |

**Cross-chapter callbacks built in:** Ch 23 (heart) connects to Ch 22 (blood) and Ch 24 (vessels); Ch 30 (urinary) connects to Ch 31 (acid-base); Ch 18 (autonomic) connects to Ch 23 (cardiac control). Reflects bundle's intentional structure.

**[verify] flags** used for specific numerical claims subject to source variation.

---

## Stray file flag — `21-the-heart.md` in book root

Discovered during this pass: `21-the-heart.md` exists in the book root (not in `chapters/`). It is a 3,630-word substantive chapter with the heading "Chapter 21 — The Heart: A Pump Built from Muscle" — but Chapter 21 in the TOC is a Part IV divider with no source content. The stray file appears to be either:

(a) An earlier draft of Chapter 23 (which is also fully written at 4,346 words on the same topic, with a different framing)
(b) An unmerged duplicate that should be removed
(c) A misplaced file that should be in `chapters/` but with a different chapter number

The two files cover essentially the same content — dual-pump architecture, autorhythmicity, pacemaker cells, dual circuits in series — with different opening framings:
- Stray Ch 21: *"Why One Pump Cannot Solve the Problem, and How Two Do."*
- Chapters/Ch 23: *"Three systems, one fist-sized muscle, 100,000 beats a day without being asked."*

**Not touched in this pass.** Bear should decide: (i) merge the best of both into the final Ch 23, (ii) delete the stray as a superseded draft, or (iii) repurpose the stray as a real Chapter 21 (which would require renaming "Fluids and Transport" to "The Heart" in the TOC, and probably also fixing the part divider structure).

**No follow-ups flagged for the LLM Exercises pattern itself.** All 28 content chapters now have consistent blocks.

---

## 2026-05-12 — Stray 21-the-heart.md resolved

Compared the stray `21-the-heart.md` (3,630 words, in book root) against `chapters/23-the-cardiovascular-system-the-heart.md` (4,346 words) in detail. Ch 23 was the more developed version overall — better framing, deeper synthesis ("The System as a Whole" section), more integrated exercises with named clinical cases.

**Three things ported from stray Ch 21 into Ch 23:**

1. **Worked cardiac output calculation** added to the "What Governs Stroke Volume" section. Concrete numbers (rest: 70 bpm × 70 mL = 4.9 L/min; max exercise: 180 bpm × 130 mL = 23.4 L/min, ~5× resting). Ch 23 had the qualitative "fourfold or more" claim but lacked the worked example.

2. **Heart rate ceiling discussion** added in the same section. Above ~180 bpm, diastolic filling time becomes inadequate; preload drops; cardiac output can decline despite faster rate. Important physiological nuance Ch 23 was missing.

3. **Exercise 11 added to the Challenge tier** — the funny current (Iₓ) drug exercise. Selectively blocks SA node sodium leak channels; predicts what pacemaker takes over and the ECG consequences. Tagged with the clinical reference (ivabradine — actually used for selective heart-rate reduction in heart failure). Strong sophisticated exercise.

**Stray file deleted** (`21-the-heart.md` removed from book root after `mcp__cowork__allow_cowork_file_delete` permission grant).

**Final Ch 23 word count:** 5,193 (was 4,346 — added ~850 words).

**Nothing else from the stray was uniquely valuable** that wasn't already covered better in Ch 23. The "System in Context" section in stray Ch 21 (baroreceptors, hormonal layer, metabolic feedback) was already covered in Ch 23's "Autonomic System as Volume Control" section more concisely. The marathon-runner exercise in stray Ch 21 was duplicated by Ch 23's Synthesis 8 (which is more developed). The wide-QRS-after-MI exercise in stray Ch 21 (#7) covered similar conceptual ground to Ch 23's Synthesis 7 (left bundle branch block).
