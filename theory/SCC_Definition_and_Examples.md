# SCC — Stable Cognitive Container
## Definition + Empirical Examples from Clay's Personal-OS

**Status:** First seed draft 2026-04-24 (overnight autonomous). Substantive elaboration pending future sessions.

---

## Definition

A **Stable Cognitive Container (SCC)** is a reference structure with these properties:

1. **Frozen between updates** — the container's contents are stable for some defined period (an SCC is not a streaming buffer or live view).
2. **Updates via deltas or full regeneration** — incremental changes accumulate in deltas; the container itself regenerates only at periodic intervals.
3. **Versioned** — each SCC state has a known version / date; downstream consumers cite versions.
4. **Independently consumable** — readers can use the SCC without needing to track all changes since its last regeneration.
5. **Per-purpose scoped** — each SCC serves a specific cognitive function; not a general-purpose dump.

SCCs work because they trade real-time accuracy for **bounded cognitive load**: rather than tracking continuous change, the reader can rely on a stable reference point that updates on a known cadence.

---

## Worked Examples

### 1. The 5 Protocol Files (`memory/protocol_*.md`)

Each protocol file is an SCC for a specific recurring decision pattern:
- `protocol_endeavor.md` — daily-recursive review pattern
- `protocol_session_close.md` — five-pillar quintet at session close
- `protocol_cold_start.md` — state-first → policy-after → queue-third
- `protocol_operating_stack.md` — per-task cost / pacing / verbosity
- `protocol_master_plan.md` — strategic direction

Each is read-mostly; updates are deliberate (versioned commits with rationale); readers consume the protocol assuming it's correct without re-deriving it from first principles.

### 2. The State_Snapshot_Current.md

The State_Snapshot is an SCC for "what is true RIGHT NOW about the personal-OS state." It updates via **Addenda** (deltas) and **Deprecated/ snapshots** (versioning). Each new session's cold-start reads the current State_Snapshot as authoritative; doesn't re-derive state from session logs.

29+ Addenda accumulated since April 16 demonstrate the SCC pattern in operation: the document is stable enough to be read top-down, yet evolves continuously through bounded deltas.

### 3. The Master Log

`Writings/Master_Log_20260424.md` is an SCC for the Projects/-wide undertaking catalog. It updates via:
- **Quarterly deltas** (`Master_Log_Deltas/*_delta.md`) for incremental changes
- **Annual full regeneration** for major refresh

Between regenerations, the Master Log is the authoritative reference for what undertakings exist and where they sit in the priority queue.

### 4. The 10 Methodology Decisions in Apex Analytics

`apex-analytics-submission/docs/METHODOLOGY_JUSTIFICATION.md` documents 10 methodology decisions made during the Apex Analytics work. Each decision is an SCC: once made + documented, it's stable for the project's duration. Future questions about "why K=4?" or "why MNAR-aware regression?" cite the SCC, not the live discussion that produced it.

### 5. CLAUDE.md Itself

The root operating instructions document is the foundational SCC of the personal-OS. Updates are deliberate, versioned (the date footer changes), and rare. All downstream protocols + memory + workflows assume CLAUDE.md is correct.

---

## When SCC Pattern Fails

- **Stale containers** — SCC isn't updated when underlying reality changes; readers act on incorrect cached state. Example: pre-correction State_Snapshot listing "PhotoRec PID 14092 running" when it had stopped.
- **Container fragmentation** — what should be one SCC gets split across multiple files; readers can't determine the authoritative version. Example: scattered "what's our latest segmentation methodology" across team memo + individual draft + audit doc + corrected analysis.
- **Premature regeneration** — full container rewrite when only a delta was needed; loses the version history.
- **Missing deltas** — incremental changes not captured between regenerations; readers don't know what changed.

---

## Relationship to FKS + SRD

- **FKS** describes the static structural relationships
- **SCC** describes the temporal stability properties
- **SRD** describes the recursive replication

A well-formed substrate has FKS layering where each layer IS an SCC, AND the whole structure exhibits SRD.

---

## TODO for elaboration

- Add formal versioning notation
- Compare/contrast with: snapshots in distributed systems, immutable data structures, content-addressed storage
- Document the "regeneration cadence vs delta cadence" trade-off mathematically
- Add anti-pattern examples (stale State_Snapshot, fragmented memo versions)

---

*SCC first seed draft 2026-04-24. Anchored to `memory/protocol_*.md` files + `Writings/State_Snapshot_Current.md` + `Writings/Master_Log_20260424.md` + `apex-analytics-submission/docs/METHODOLOGY_JUSTIFICATION.md`.*
