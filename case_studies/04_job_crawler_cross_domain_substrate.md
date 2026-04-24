# Case Study 04 — Job-Crawler as Cross-Domain Substrate
## SRD applied to "structured data extraction with LLM-based scoring"

**Status:** Tight seed 2026-04-24.

---

## Why this case demonstrates cross-domain SRD

Cases 01-03 demonstrated SRD within personal-OS work (memo reinvigoration, framework versioning, audit cadence). Case 04 demonstrates **cross-domain** SRD: the same architectural pattern applied to fundamentally different domains (jobs vs Canvas vs GitHub).

This is the most powerful SRD pattern because it predicts portability: if the same shape works for one domain, the framework predicts it will work for adjacent domains with bounded adaptation cost.

---

## The architecture as SRD instance

```
Source-specific fetch → normalize (NormalizedJob) → LLM rubric score → store → shortlist → cover-letter
```

Same five-stage pipeline at every level of decomposition:
- **Per-source level:** RemoteOK fetch → normalize → emit NormalizedJob; same shape as Jobicy fetch → normalize → emit
- **Per-rubric level:** Score per dimension → weighted sum → multiplier → recommendation; same shape as v1 (6-dim) and v2.1 (8-dim)
- **Per-corpus level:** Score → dedupe → shortlist → cover-letter; same shape regardless of source diversity

---

## Cross-domain extensibility (per Clay's 2026-04-24 strategic note)

Per the State_Snapshot Addendum 28 strategic-direction note: *"you can use our crawler for all intents and purposes — job listing websites, canvas, github pages."*

This is the cross-domain SRD claim made explicit. The framework's structure:

| Domain | Source modules | Normalized item | LLM rubric | Output |
|---|---|---|---|---|
| **Jobs** (current) | RemoteOK / WWR / Handshake / Indeed / Wellfound / ZipRecruiter / Crawl4AI / Kaggle + 5 new Tier-A (Remotive / Jobicy / Working Nomads / Remote.co / SkipTheDrive) | `NormalizedJob` dataclass | overemployment rubric v1 + v2.1 | shortlist + cover letters |
| **Canvas** (proposed) | recursive course-page crawler | `NormalizedCanvasItem` (assignment / module / page / file) | "what's new since last crawl" rubric | daily Canvas digest |
| **GitHub** (proposed) | repo discovery crawler | `NormalizedRepo` (Substrate-Thesis-relevant signals) | competitive-intelligence rubric | weekly research-horizon digest |
| **General** (existing) | `crawl4ai_generic.py` fallback | `NormalizedWebItem` | per-domain LLM rubric | per-domain digest |

Same architecture. Same correctness guarantees. Different domains.

**The substrate isn't job-specific** — it's "structured data extraction with LLM-based scoring" applied wherever that pattern fits.

---

## What the cross-domain SRD predicts

The pattern predicts:
- Adaptation cost per new domain ≈ source-module template (1-2 hrs) + per-domain rubric + storage schema (1-2 hrs)
- Same failure modes apply (interface violation, schema drift, rate-limiting)
- Same operational discipline (smoke-test before live, dedupe across sources, version rubrics)
- Same evolution arc (v1 broad rubric → v2 tuned per stack-goal parameters)

This is testable: when the Canvas crawler is built (currently backburner per Clay 2026-04-24), the predicted adaptation cost should hold within 50% of the prediction. If it does, the SRD claim is empirically validated.

---

## Substrate Thesis recognition

- **FKS:** scrape → normalize → score → store → shortlist is an explicit dependency layering; each layer reads only its immediate prior
- **SCC:** the rubric (v1 and v2.1) is an SCC frozen between updates; cited per version
- **SRD:** the architecture itself; same shape across sources, rubrics, domains

The job-crawler is the most concrete substrate Clay has built that demonstrates all three patterns AND demonstrates cross-domain portability.

---

## TODO for elaboration

- Build the Canvas crawler (gated on Clay's go-ahead from backburner status); validate the SRD prediction empirically
- Document the GitHub crawler as a third domain test
- Compare adaptation cost across the three domains
- Add the substrate's failure modes documented (e.g., the wage-cap audit catalyst as a per-domain calibration drift)

---

*Case Study 04 tight seed 2026-04-24. Anchored to `scripts/job-crawler/` (full architecture) + `Writings/Top33_Boards_Scopeout_20260424.md` (Phase 1+2 expansion) + State_Snapshot Addendum 28 (Clay's cross-domain directive).*
