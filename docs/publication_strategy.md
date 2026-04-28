# Publication Strategy
## Substrate Thesis — venue + format + cadence decisions

**Status:** First seed 2026-04-24. Decision artifact for the author (per `docs/thesis_v1_outline.md` decision deadline 2026-05-15).

---

## The strategic question

You've built a coherent framework with 6 case studies + 3 theory seed docs + a paper outline. The Substrate Thesis is publication-ready in scaffold form. The only blocker is **venue + format + cadence commitment**.

This document structures that decision.

---

## Three candidate paths (recap from `thesis_v1_outline.md`)

| Path | Audience | Effort | Compounding payoff | Risk |
|---|---|---|---|---|
| **Substack series** (7 essays bi-weekly) | Technical-but-non-academic; PKM community; professional network | 40-80 hrs over 14 weeks | Audience that informs whether academic/book is worth it; iterative validation | Low — abandonable mid-series |
| **Academic paper** (workshop/journal) | CS/HCI/personal-informatics researchers | 100-200 hrs incl. citations + peer-review cycle | Citation impact; PhD-application leverage | Medium — peer review can reject; cycle long |
| **Book** (self/trade publish) | Crossover technical-narrative readers | 300-600 hrs over 6-18 months | Definitive artifact; consulting/positioning leverage | High — significant commitment; no validation until publication |

---

## Recommendation: hybrid path with sequencing

**Phase 1 (May 2026 → November 2026):** Substack series Essays 1-7
**Phase 2 (December 2026 → March 2027):** Convert top 1-2 essays into academic paper for workshop submission
**Phase 3 (post-PhD-acceptance, 2027+):** If validation positive, book proposal

This sequencing:
- **Validates iteratively** — each essay's reception informs whether to continue
- **Compounds across paths** — academic paper draws from already-written Substack content; book draws from already-validated essays
- **Minimizes commitment risk** — Substack abandonable; academic effort only after Substack validates; book only after academic publishes
- **Aligns with PhD application timeline** — Substack series gives faculty browsable evidence pre-application (Sept 2026 deadline)

---

## Phase 1 detailed plan — Substack Series

**Recommended platform:** Substack (free tier; technical-audience-friendly; built-in subscription; minimal config)
**Alternative:** Medium (broader reach but algorithm-dependent; less owner-controlled)

**Essays per `thesis_v1_outline.md`:**
1. Recognition (May 2026)
2. FKS — When Layers Hold (June 2026)
3. SCC — Power of Frozen References (June 2026)
4. SRD — Same Pattern, Every Scale (July 2026)
5. When the Three Patterns Interact — Case Study (July 2026)
6. Anti-Patterns and How They Surface (August 2026)
7. Building Your Own Substrate (September 2026)

**Cadence:** Bi-weekly. Allows ~2 weeks per essay for writing + 1 week for reader feedback before next.

**Pre-publication preparation (April 25 → May 15):**
- [ ] Substack/Medium account setup
- [ ] Substrate Thesis Companion repo made public on GitHub (so essays can link)
- [ ] Pre-readers identified (3-5 from the author's professional network)
- [ ] Theory seed docs substantively elaborated (current versions are seeds; need 2x expansion)
- [ ] Voice consistency check across 2-3 draft essays
- [ ] Visual style decision (diagrams? code snippets? minimal text?)

**Mid-series checkpoint (after Essay 3 — late June 2026):**
- Subscriber count > 50 and growing? → continue series + start Phase 2 prep
- Subscriber count < 50 or flat? → reduce to 4-essay series + skip Phase 2

**End-of-series retrospective (December 2026):**
- Total readership + engagement metrics
- Most-cited / most-shared essay
- Decision on Phase 2 academic paper effort

---

## Phase 2 detailed plan — Academic Paper

**Format:** 8-12 page workshop or short-conference paper (NOT a 30-page journal article — entry barrier too high for first publication)

**Venue candidates (ranked):**
1. **CHI Workshop on Personal Informatics** — best fit for the practitioner-narrative + framework structure
2. **CSCW Workshop on Personal Knowledge Management** — alternative with more PKM-specific audience
3. **HotOS Workshop** — if framing is "personal computing systems" rather than "personal informatics"
4. **Late-stage stretch:** SIGCHI / CSCW main conference (high prestige, harder acceptance)

**Adapting Substack essays to paper:**
- Compress 7 essays into 1 paper (~10-12 pages):
  - §1 Introduction (Essay 1's recognition + framework overview)
  - §2 Related Work (PKM literature, system design literature)
  - §3 The Three Patterns (Essays 2-4 compressed)
  - §4 Case Study (Essay 5)
  - §5 Anti-Patterns (Essay 6)
  - §6 Practical Implications (Essay 7's MVS + templates)
  - §7 Limitations + Future Work
  - §8 Conclusion

**Submission window:** workshop deadlines typically September-November for spring conferences; March-April for fall. Aim for late-2026 / early-2027 submission cycle.

---

## Phase 3 detailed plan — Book (only if Phase 1+2 validate)

**Conditional:** pursue ONLY if Phase 1 reaches 1000+ subscribers OR Phase 2 paper accepted at top-tier venue.

**Format options:**
- **Self-published technical book** (Leanpub / Amazon KDP) — 50-80K words; no advance, full royalties
- **Trade publisher** (O'Reilly / Pragmatic / Apress) — 60-100K words; advance + royalty; longer cycle
- **Hybrid academic-trade** (MIT Press / Princeton) — most prestigious but hardest acceptance

**Adapting Substack + paper to book:**
- Expand 7 essays into 8-10 chapters (per `thesis_v1_outline.md` Book option)
- Add chapters: Long-term reflections (year-over-year evolution); Case studies expanded with more empirical data
- Add appendices: Templates Library; Repository Tour; Glossary; Bibliography

**Timeline:** 2027-2028 if pursued. Year-2 personal-OS evolution data (per case 06 prediction) provides strong material for the long-term-reflection chapter.

---

## Cross-cutting decisions

### Repository visibility (gates Phase 1)

- **Public GitHub** required for Substack essays to link verifiably
- **Private + selective access** acceptable for academic paper if essays are private
- **Recommendation:** public by 2026-05-15 to align with Phase 1 essay 1 launch

### Authorship + attribution

- Sole author OR co-author with collaborators?
- For Substack: sole authorship simplifies cadence
- For academic paper: sole or with PhD advisor (if PhD admits by then)
- For book: sole authorship maintains creative control; co-authoring with established figure adds credibility

### Voice + tone

- Substack: first-person practitioner; analytically rigorous voice; concrete examples over abstract arguments
- Academic paper: third-person formal; cited literature; methodology section
- Book: hybrid — first-person narrative arc with rigorous technical depth

The Substack voice (already established in case studies + theory seeds) is the natural anchor; academic + book derive from it with appropriate register shift.

### Funding model

- Substack: optional paid tier (start free; add paid for premium content if subscribers warrant); Patreon alternative
- Academic paper: no direct revenue; indirect (citation + PhD acceleration + consulting opportunities)
- Book: advance + royalty (trade) OR direct sales (self-published)

---

## Risk mitigations per phase

| Phase | Risk | Mitigation |
|---|---|---|
| Phase 1 | Series doesn't gain audience | Mid-series checkpoint; reduce to 4-essay series; abandon if <50 subscribers |
| Phase 1 | Voice inconsistency across essays | Pre-readers; style guide based on first 2 essays; consistent vocabulary check |
| Phase 1 | Reveal too much personal-OS detail | Selective disclosure; redact specific names/dates where appropriate; private companion repo for full evidence |
| Phase 2 | Paper rejected | Submit to next-tier venue; academic peer review is iterative |
| Phase 2 | Methodology criticism (selection bias, survivorship bias) | Address explicitly in §7 Limitations; acknowledge gaps documented in case 06 |
| Phase 3 | Book commitment exceeds bandwidth | Sequenced — only commit after Phase 1+2 validate; Year 2 retrospective provides natural pause point |

---

## Decision deadlines

| Date | Decision | Status |
|---|---|---|
| **2026-05-01** | Substrate Thesis Companion repo strategy (public GitHub vs private) | Open |
| **2026-05-15** | Publication path commitment (Substack / Academic / Book / Hybrid) | Open |
| **2026-05-31** | Substack/Medium account setup (if Phase 1 chosen) | Open |
| **2026-06-15** | Theory seed docs substantively elaborated (2x expansion) | Open |
| **2026-07-15** | Essay 1 draft + pre-reader feedback complete | Open |
| **2026-08-15** | Essay 1 published | Open |
| **2026-12-15** | Phase 1 retrospective + Phase 2 commitment decision | Open |

---

## Recommendation summary

**Commit to Phase 1 (Substack series) by 2026-05-15.** Lowest commitment cost; highest validation value; aligns with PhD application timeline; provides faculty-browsable evidence for application essays.

Defer Phase 2 + 3 commitments to mid-series + end-of-series retrospectives. Don't pre-commit to academic paper or book before Phase 1 validates.

---

*Publication Strategy first seed 2026-04-24. Decision artifact for the 2026-05-15 commitment milestone. Companion to `docs/thesis_v1_outline.md` + `docs/prior_art_survey.md` (next).*
