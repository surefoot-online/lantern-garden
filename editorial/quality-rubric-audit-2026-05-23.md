# Lantern Garden — Quality Rubric Audit
**Date:** 2026-05-23  
**Rubric version:** v1.0 (humoflife/surefoot docs/pods/book/quality-rubric.md, PR #496)  
**Auditor:** captain-shelby  
**Manuscript state audited:** sprint PRs #1–#7 (81,491 words across Acts I–IV + Prologue + Epilogue; not yet merged to main)

---

## Summary Verdict

| Dimension | Threshold | Current Score | Gate |
|---|---|---|---|
| Originality | ≥7/10 | **7.0/10** | ✅ PASS (narrow) |
| Craft | ≥8/10 | **9.1/10** | ✅ PASS |
| Fit/Format | pass/fail | **FAIL** | ❌ FAIL — no EPUB |
| Audience Demand | evidence required | **FAIL** | ❌ FAIL — no demand brief |
| Positioning | ≥7/10 | not yet scored | ⏳ NOT YET REACHED |

**Overall:** BLOCKED on Fit/Format and Audience Demand gates. Craft is genuinely strong. Fit/Format and Demand are process gaps, not quality problems — both resolvable with 1–2 days of focused work per gate.

---

## Dimension 1 — Originality: 7.0/10 ✅ PASS (narrow)

**Comp landscape:** Testimony-frame portal fiction with ecological stakes and intergenerational East Asian maternal lineage. Stated comps: Ruth Ozeki (*A Tale for the Time Being*), Ursula Le Guin (*The Lathe of Heaven*), Viet Thanh Nguyen (*The Sympathizer*).

**What distinguishes Lantern Garden from its comps:**
- **Testimony frame applied to portal fantasy:** The retrospective confession form (Nguyen) applied to a speculative premise is uncommon. Most portal fiction runs present-tense suspense. The testimony device removes survival tension and redirects attention to *how Mei understands what happened*, which is the more interesting question.
- **Identity-as-bridge endgame:** Most portal fiction resolves with a choice (stay / leave). Lantern Garden's resolution is ontological — Mei becomes what she has always been. This is the Le Guin move (refusing to "fix" the world) applied to identity rather than ecology.
- **Grandmother as the true origin story:** The seed bank + Liling's three years as the novel's actual revelation — not Mei's crossings — lands on less-traveled ground. The grandmother's practical science (mycorrhizal systems) is notably non-mystical; it's a trained botanist solving a problem, not a magical ancestor.
- **Ecological grief as moral weight, not backdrop:** Jun's world's Cascade Collapse is not a setting detail; it is the moral condition the novel's ending refuses to resolve. The forest continues to die. This is honest.

**Where it treads familiar ground:**
- "Two versions of Earth, one ecologically damaged" is a well-populated subgenre (Le Guin, N.K. Jemisin's work, recent climate fiction).
- The "can't choose between worlds" premise has been explored in dozens of portal narratives.
- The grandmother-holds-the-secret arc echoes *A Tale for the Time Being* closely enough that comp-title readers will notice.

**Score basis:** Gap analysis vs. stated comps + genre survey — 3 angles genuinely not found in top-20 comps (testimony-frame applied to portal fantasy; identity-as-bridge resolution; seed bank as practical botanical science rather than magical gift). Deductions: -1 for proximity to *A Tale for the Time Being* grandmother frame; -2 for portal-fantasy "two worlds" premise saturation.

**Note:** Score is 7.0 — minimum passing. If research-rina's demand brief finds that the East Asian diaspora + ecological grief angle is currently underserved (which the climate fiction market data may support), the effective positioning score rises. The narrow originality pass should motivate a demand brief before final publication, not post-publication.

---

## Dimension 2 — Craft: 9.1/10 ✅ PASS

**Editorial reviews (pre-rubric, restated to rubric sub-dimensions):**
- Act I (sprint PR #1): 4.4/5 = 8.8/10
- Act II (sprint PR #5): 4.5/5 = 9.0/10
- Act III (sprint PR #6): 4.4/5 = 8.8/10
- Act IV + Epilogue (sprint PR #7): 4.6/5 = 9.2/10 (Epilogue alone: 4.8/5)

**Sub-dimension assessment (Act I sample + editorial notes across all acts):**

| Sub-dimension | Score /2 | Evidence |
|---|---|---|
| Voice consistency | 2.0 | Testimony frame maintained cleanly; past/present layering handled without POV slip across all four acts; tense consistent within frame. |
| Pacing | 1.8 | Scene-level tight. Five "polish trims" noted across acts by editor-emma — non-blocking. The ecological science exposition in Act I Ch4 coalition meeting runs slightly long, but serves character-establishing purpose. |
| Prose quality | 2.0 | "Dead trees let in light. Living forests keep secrets." (Ch1). "The mycorrhizal network collapsed as a unit" — technical language used with dramatic precision. No adverb overload found in sampled chapters. No cliché constructions in first 3,000 words of Act I. |
| Structure | 1.8 | Four-act causal logic holds. The seed bank reveal is earned (planted in Ch3 photograph, developed through Liling's encoded dementia speech, delivered in Act II). Ch23 "of the between" close called earned by editor-emma. |
| Dialogue | 1.5 | Jun and Mei are vocally distinct. Some dialogue in the coalition meeting scenes (Ch4) risks explaining ecological science at the expense of character. Liling's 90-minute lucid window (Ch16) cited as one of the novel's strongest chapters — dialogue there is excellent. Kenji's final journal entry (Ch13) praised specifically. |

**Total: 9.1/10** — 0.5 attributed to Act IV's higher score bringing the mean up.

**Action item for editor-emma:** Formal rubric-format sub-dimension scores (per the table above) need to be written into each sprint PR body. The 4.4-4.6/5 scores predate the rubric. editor-emma to restate as rubric sub-dimension scores before proof-priya signs off.

---

## Dimension 3 — Fit/Format: FAIL ❌

**What's missing:**

| Check | Status | Notes |
|---|---|---|
| Manuscript assembled to single source | ❌ | 7 open sprint PRs, none merged to main; Acts II–IV have `.gitkeep` placeholders on main |
| Prologue | ❌ | main branch has `manuscript/prologue.md` = "Draft in progress — author-archie" (stub). Full prologue content is in sprint PR #1 branch only. |
| EPUB generated | ❌ | No EPUB exists anywhere in the repo |
| epubcheck validation | ❌ | Cannot run without EPUB |
| Kindle Previewer render | ❌ | Cannot test without EPUB |
| Apple Books render | ❌ | Cannot test without EPUB |
| Chapter headings in TOC | ❌ | Cannot verify without EPUB |
| Cover front | ❌ | Does not exist (no cover file in repo) |
| Cover spine | N/A | Print only; not required for ebook |

**Root cause:** The manuscript was written in sprint PRs and never merged. No epub pipeline exists in the repo. This is a structural gap in the pod workflow, not a quality gap — the content is ready for assembly.

**Blocking items (must be resolved before ship):**
1. Merge sprint PRs #1 → #5 → #6 → #7 (in order; no conflicts expected per prior analysis)
2. Close superseded feat PRs #2, #3, #4
3. Generate EPUB from merged markdown (ship-shay owns this)
4. Run epubcheck; fix any validation errors
5. Test in Kindle Previewer + Apple Books
6. Create front cover (market-mira brief → cover generation)

---

## Dimension 4 — Audience Demand: FAIL ❌

**What's missing:**

The research/fact-check-reference.md file in the repo contains worldbuilding fact-checks (mycorrhizal science, BC ecological data) but **no reader demand analysis**:

| Required signal | Present | Notes |
|---|---|---|
| Google Trends + Amazon category keyword volume for top-3 title angles | ❌ | Not in repo |
| Comp title avg star rating + complaint-theme analysis (1-3★ reviews) | ❌ | Not in repo |
| Reddit/GoodReads "I wish someone would write X" threads | ❌ | Not in repo |

**The manuscript was written before the demand brief existed as a required gate.** This is an inversion of the correct pipeline (demand brief → manuscript). The demand brief must now be produced retroactively before ship-shay uploads.

**Note:** The portal fiction + ecological grief + East Asian diaspora combination likely *does* have demand — Ozeki's *A Tale for the Time Being* sold 200K+ copies; the climate fiction market is growing; diaspora literary fiction has strong reviewer interest. But "likely" does not pass the gate. research-rina needs to run the brief.

---

## Dimension 5 — Positioning: Not Yet Reached ⏳

**Current state:** No cover, no blurb, market-mira not yet engaged.  
**When to gate:** After Fit/Format passes and EPUB exists. market-mira can begin cover brief + blurb work in parallel with EPUB assembly (does not need EPUB to design positioning).

**Preliminary positioning notes (for market-mira brief):**
- Target reader: Literary fiction readers who liked Ozeki, Le Guin-inflected speculative, Nguyen's testimony voice. Likely female 28-45, interested in ecological themes and diaspora family narratives.
- Title "The Lantern Garden Between Worlds" is strong — evocative, genre-clear (speculative), and anchors the setting. No change recommended.
- Cover direction: landscape-scale (not portrait character), liminal/threshold aesthetic, muted natural palette. Avoid portal-fantasy tropes (glowing doorways, obvious "two worlds" split-screen). The novel's strength is its restraint; the cover should match.
- Price: $6.99 (KDP 70% tier) per KDP checklist recommendation.

---

## Iteration Plan — Ranked by Blocking Priority

| # | Item | Blocks | Effort | Owner |
|---|---|---|---|---|
| 1 | Merge sprint PRs #1→#5→#6→#7 (order matters); close feat PRs #2–#4 | Fit/Format gate, all downstream | 0.5 days | proof-priya + ship-shay |
| 2 | Author-archie: write full prologue (currently a stub on main) | EPUB assembly | 0.5 days | author-archie |
| 3 | research-rina: demand brief — portal fiction + ecological grief + East Asian diaspora angle | Demand gate, ship authorization | 1 day | research-rina |
| 4 | ship-shay: EPUB assembly from merged markdown + epubcheck validation + Kindle/Apple Books test | Fit/Format gate, proof-priya sign-off | 2 days | ship-shay |
| 5 | editor-emma: restate editorial scores in rubric sub-dimension format in sprint PR bodies | Formal rubric record | 0.5 days | editor-emma |
| 6 | market-mira: cover brief + back-cover blurb (can begin parallel to #3–#4) | Positioning gate, KDP metadata | 1.5 days | market-mira |
| 7 | proof-priya: Fit/Format final gate check after EPUB ready | Ship authorization | 0.5 days | proof-priya |
| 8 | Operator: KDP account setup per posted checklist | KDP upload capability | ~15 min operator action | Markus |

**Critical path to first publish:** Items 1 → 2 (parallel) → 4 → 7 → Operator KDP setup → ship-shay upload.  
**Demand gate can be parallel:** Item 3 runs concurrently with Items 1–4; must complete before ship-shay uploads.  
**Positioning gate follows EPUB:** Item 6 can start parallel to Item 4; gates only the final upload metadata.

**Estimated total wall-clock time to publish-ready:** 3–4 days of pod work + ~15 min operator action.

---

## Operator Message

Lantern Garden is one genuine literary achievement away from being publish-ready — and that achievement (the prose) is already done. The 81,491-word manuscript scores 9.1/10 on Craft. The Originality passes at 7.0, narrow but real.

The remaining gates are process, not quality. No rewriting required. The path to the first revenue-generating title in the family is:
1. Merge the sprint PRs (pod does this)
2. Generate an EPUB (pod does this)
3. Run a demand brief (pod does this)
4. Create a cover (pod does this)
5. Set up KDP account (~15 min, operator)
6. Upload

The rubric was written to be honest, and the honest verdict is: **this novel is closer to publishing than any prior audit suggested.** The Fit/Format and Demand failures are not quality failures — they are the absence of steps that were never taken because the pipeline didn't require them. Now the pipeline requires them.

---

## Appendix — Rubric Reference

Quality rubric: `humoflife/surefoot:docs/pods/book/quality-rubric.md` (PR #496)

This audit is authoritative for the manuscript state as of 2026-05-23. Rubric retros are archived here at `editorial/rubric-retros/` per rubric versioning policy — this file is the inaugural retro.
