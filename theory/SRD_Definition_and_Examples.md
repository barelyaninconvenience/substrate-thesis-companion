# SRD — Stable Recursive Decomposition
## Definition + Empirical Examples from Clay's Personal-OS

**Status:** First seed draft 2026-04-24 (overnight autonomous). Substantive elaboration pending future sessions.

---

## Definition

A **Stable Recursive Decomposition (SRD)** is a structural pattern with these properties:

1. **Same structural shape at multiple scales** — the pattern repeats identically at different time horizons, different problem sizes, or different domains.
2. **Same correctness guarantees at every scale** — what holds at the smallest instance also holds at the largest.
3. **Same failure modes at every scale** — what breaks the small instance also breaks the large one (predictably).
4. **Per-scale autonomous operation** — each scale's instance can operate without coordination with other scales.
5. **Cross-scale informativeness** — observing the pattern at one scale teaches you about other scales' behavior.

SRDs are the most powerful Substrate Thesis pattern because they enable **cross-scale prediction**: if you know how the pattern behaves at the weekly scale, you know how it behaves at the annual scale. If you know how it behaves on a small project, you know how it behaves on a large one.

---

## Worked Examples

### 1. The ENDEAVOR Loop W/M/Q/A Cadence (Canonical SRD)

The audit cadence framework is the cleanest SRD instance Clay has built:

| Scale | Source | Output | Stop condition |
|---|---|---|---|
| **Weekly** | Past 7 days of sessions/oversights/snapshots | Weekly_Audit_<YYYY-WW>.md | After Section 6 populated |
| **Monthly** | Past 4 weekly audits | Monthly_Audit_<YYYY-MM>.md | After all weekly inputs integrated |
| **Quarterly** | Past 3 monthly audits | Quarterly_Audit_<YYYY-Q>.md + Master Log delta | After Master Log delta committed |
| **Annual** | Past 4 quarterly audits | Annual_Audit_<YYYY>.md + regenerated Master Log | After Master Log regeneration |

**Same shape at every scale:**
- Read prior layer's outputs (only)
- Catalog new + completed undertakings
- Surface backlog deltas
- Note drift / calibration observations
- Stop at defined boundary (no inline investigation)

**Same correctness guarantees:** at every scale, the audit is "correct" if it captures the prior layer's content without inventing new information or skipping documented findings.

**Same failure modes:** any scale can fail by recursing into prior-prior layer (the "single layer deep" violation). Same anti-pattern at all scales.

This is the canonical SRD because it's been *deliberately designed* to exhibit the pattern.

### 2. Job-Crawler Architecture

`scripts/job-crawler/` exhibits SRD across multiple dimensions:

```
At the source-module level:
    scrape → normalize → score → store
At the per-source level:
    fetch → parse → emit NormalizedJob
At the rubric level:
    score per dimension → weighted sum → multiplier → recommendation
At the corpus level:
    score → dedupe → shortlist → cover-letter
```

Same structural shape (transform + emit, with explicit interface) at each scale. Same failure mode (interface violation breaks downstream).

This SRD is what makes the architecture **domain-portable**: per Clay's 2026-04-24 directive, the same pattern can serve job listings, Canvas pages, GitHub repos. The crawler isn't job-specific; it's an SRD instance applied to "structured data extraction with LLM-based scoring."

### 3. The Reinvigoration Template

The pattern observed in:
- Caddell_Descriptive_Insights_Memo v1 (Apr 5) → v2 (Apr 24)
- Caddell_Individual_Segmentation_Memo v1 (Apr 14) → v2 (Apr 24)
- Operating_Stack v1 → v1.3.1
- KLEM/OS v1 → v2 → v3
- IS7036 deck v1 → v2 → v3

Every reinvigoration has the same structural shape:
1. Identify v1's vintage + acknowledge what's changed since
2. Apply numeric corrections from intervening audit findings
3. Add new sections capturing post-v1 discoveries
4. Add forward-pointing section connecting to subsequent work
5. Preserve v1 in Deprecated/

Same shape. Same failure modes (skipping audit findings, omitting forward-pointing). Cross-scale: applies to memos, decks, scripts, frameworks.

The reinvigoration template is an SRD that compounds: each application adds an evidence point that the pattern works.

### 4. SOK Directory Structure

`Projects/SOK/Logs/<script>/<RunId>/` decomposes the same way at every script + every run:

```
SOK/Logs/SOK-Backup/20260424-013000/
SOK/Logs/SOK-Comparator/20260424-014500/
SOK/Logs/SOK-WeeklyAudit/20260427-180000/
```

Same structural shape (script_name × run_id timestamp) at every script. Same failure modes (missing log directory, conflicting run IDs). Discovery is uniform: any tool that knows the pattern can read any script's logs.

### 5. Memory Directory Structure

`memory/{user_, project_, feedback_, protocol_, reference_}*.md` decomposes by file-type prefix:

- `user_*` → facts about Clay
- `project_*` → state of named projects
- `feedback_*` → policies Clay has stated
- `protocol_*` → recurring decision patterns
- `reference_*` → external system pointers

Same shape (prefix + topic) for every file. Same failure modes (mis-categorized file, missing prefix). Cross-domain: applies to user identity, projects, feedback, protocols, references — same scaffolding everywhere.

---

## When SRD Pattern Fails

- **Pseudo-recursion** — pattern looks the same at different scales but actually differs in correctness guarantees. Example: per-session audit vs annual audit aren't true SRD if they apply different rules; calling them "the same" then misleads about behavior.
- **Forced uniformity** — applying the SRD pattern where it doesn't naturally fit, distorting the underlying problem to maintain pattern. Example: jamming an audit cadence into a domain that doesn't have meaningful periodicity.
- **Cross-scale leak** — patterns that need to coordinate across scales (e.g., the weekly audit reading directly from monthly to "save time") break the SRD.
- **Hidden state** — SRD instances that maintain hidden global state across instances (e.g., "the script remembers prior runs") violate per-scale autonomous operation.

---

## SRD vs FKS vs SCC

- **FKS** is *static structural* (layered dependencies)
- **SCC** is *temporal stability* (containers that change deliberately)
- **SRD** is *recursive replication* (same shape at multiple scales)

A well-formed substrate exhibits all three:
- FKS layering (clear dependency order)
- Each FKS layer is also an SCC (stable enough to depend on)
- The whole exhibits SRD (pattern repeats at scales)

The Substrate Thesis is the framework that surfaces all three simultaneously. Most personal-OS work surfaces only one or two at a time; the thesis claims all three are necessary for sustainable cognitive labor.

---

## Cross-domain SRD recognition

The most powerful SRDs cross domains:

- **The reinvigoration template** applies to memos, decks, scripts, frameworks — different artifact types, same shape
- **The audit cadence** applies to weekly / monthly / quarterly / annual — different time scales, same shape
- **The crawler architecture** applies to jobs / Canvas / GitHub — different domains, same shape
- **The SOK directory structure** applies to backup logs / archive logs / monitor logs — different scripts, same shape

Recognizing cross-domain SRDs is what makes Clay's personal-OS *compound* over time: each new instance reuses prior pattern recognition.

---

## TODO for elaboration

- Add formal mathematical notation (functor / monad analogies?)
- Compare/contrast with: fractals, scale-invariant systems, design patterns
- Document the "domain portability test" formally
- Add real failure cases from Clay's history (where SRD was attempted but didn't generalize)

---

*SRD first seed draft 2026-04-24. Anchored to `Writings/Master_Log_Audit_Cadence_20260424.md` (canonical SRD) + `scripts/job-crawler/` architecture + reinvigoration cycles + `Projects/SOK/Logs/` structure + `memory/` prefix scheme.*
