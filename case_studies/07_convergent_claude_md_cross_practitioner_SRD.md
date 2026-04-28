# Case Study 07 — The Convergent CLAUDE.md Pattern as Cross-Practitioner SRD
## A Substrate Thesis instance crossing the practitioner boundary

**Status:** First draft 2026-04-24. Preliminary prevalence reconnaissance executed 2026-04-25 (see `07_appendix_prevalence_study_preliminary_20260425.md`). Formal N≥100 stratified study protocol in this document remains execution-ready.

**Prevalence reframing (2026-04-25):** the deep research reconnaissance documented in the appendix establishes that the operating-instructions-at-repository-root convention is empirically prevalent in the **tens of thousands** of public GitHub repositories (per arXiv 2602.11988 Feb 2026 reporting >60,000 instances). The N=2 framing in the main text below documented the author and Daniel Miessler as the original two confirmed independent-emergence instances; the appendix updates the empirical context to reflect that the convention is far more widespread than that initial framing implied. The structural argument in the main text remains valid; the prevalence claim is now empirically grounded at scale.
**Companion to:** `theory/SRD_Definition_and_Examples.md` v2 + `docs/prior_art_survey.md` Category 0 + cases 01-06.
**Distinguishing feature:** the only case study in the corpus where the SRD instance crosses the practitioner boundary. Cases 01-06 demonstrate patterns within a single practitioner's substrate; case 07 demonstrates the pattern recurring across independent practitioners' substrates.

---

## Why this case is canonical

The first six case studies in this corpus all share a feature: the SRD instances they document exist within a single practitioner's cognitive infrastructure. The reinvigoration template (case 01) was applied repeatedly by one person. The Operating Stack evolution (case 02) was a single practitioner's framework iteration. The audit cadence (case 03), the crawler architecture (case 04), and the year-over-year personal-OS evolution (case 06) all illustrate the Substrate Thesis patterns *within* a substrate.

Case 07 demonstrates something different and stronger: **the same structural pattern appearing independently across practitioners' substrates**. Not by coordination. Not by derivation. By convergent design — the kind of parallel emergence that happens when independent practitioners arrive at the same convention because the underlying pattern is real.

Specifically: the convention of placing an operating-instructions document at the root of a project repository — typically named `CLAUDE.md` or `AGENTS.md` or similar — has emerged independently across multiple practitioners building cognitive substrates with AI-augmented development tools. Each practitioner discovered the convention through their own work; the pattern recurs because it solves a real problem the same way every time it's encountered.

This is significant for the Substrate Thesis claim. The first six case studies establish that the FKS / SCC / SRD patterns are recognizable in personal substrate work. Case 07 establishes that the patterns are *not idiosyncratic to one practitioner* — they're structural features of well-formed cognitive infrastructure that emerge wherever practitioners build seriously with AI assistants over time.

---

## What the convention looks like

The convergent pattern: a single root-level document at the top of a project or personal-OS repository that contains operating instructions — vocabulary, rules, conventions, and standards — that AI assistants and human collaborators both read at the start of every working session.

The document has consistent structural properties wherever it appears:

- **Single file at repository root.** Not buried in a subdirectory. Discoverable on first inspection of the repo.
- **Plaintext markdown.** Readable without specialized tooling. Diff-friendly. Version-controllable in git.
- **Authoritative for the scope it covers.** When the document and other sources conflict, the document wins. Downstream consumers don't have to weigh competing instructions.
- **Globally loaded.** Read at the start of every session. Not consulted only when a specific question arises; consulted as default context.
- **Per-scope tunable.** A repository may have a project-specific operating-instructions file in addition to a global one. The local file extends or overrides the global.

The naming varies. The community has converged on `CLAUDE.md` for Claude Code installations, `AGENTS.md` as a more provider-neutral proposal, `.cursorrules` in some Cursor IDE contexts, and other variations. The naming is convention; the structural pattern is the substance.

---

## Two confirmed instances

This case study documents two confirmed practitioners whose substrates include the operating-instructions-at-repo-root pattern, where the instances were developed independently.

### Instance 1: Daniel Miessler — Substrate (`github.com/danielmiessler/Substrate`)

A public framework for collective knowledge organization. 799 stars at time of writing (late April 2026). MIT-licensed. TypeScript-and-Bun stack. Last updated 2026-04-22.

The repository contains a `CLAUDE.md` at its root. The file specifies vocabulary the framework uses (Problems, Solutions, Arguments, Claims, Plans, etc.), defines the relationships between knowledge components, and articulates the conventions humans and AI assistants follow when contributing to the framework's content.

The convention serves the same function in Miessler's substrate that it serves elsewhere: a single authoritative source of operating instructions, loaded by default, reducing the need for repetitive calibration of context across sessions or across collaborators.

### Instance 2: Clay Caddell (the author) — personal cognitive infrastructure with global + per-project operating-instructions files

A personal cognitive infrastructure spanning multiple analytical datasets, tens of thousands of words of personal writing, a multi-source structured-data crawler, dozens of PowerShell automation scripts, and the audit cadences that keep all of it coherent.

The substrate includes a global operating-instructions file at the home-directory level (a `CLAUDE.md` under `~/.claude/`) plus per-project variants at the root of specific repositories. The global file specifies machine context, engineering standards (a DryRun mandate, deprecate-never-delete discipline, exhaustive-reads-before-modifications), communication conventions, protocol references, and the universal rules that apply across all projects. Per-project files extend the global with project-specific vocabulary, conventions, and constraints.

The convention serves the same function in this substrate that it serves in Miessler's: a single authoritative source of operating instructions, loaded by default, reducing the need for repetitive calibration across sessions.

---

## Independence of the two instances

The two practitioners reached the convention independently. The intellectual lineages are traceable.

Miessler's Substrate framework predates its `CLAUDE.md` by some period — the repository's earlier commits don't reference the convention; later commits adopt it as the framework matured. Miessler's broader public work in cybersecurity and knowledge organization predates Anthropic's Claude Code release entirely.

The author's adoption of the convention emerged through personal-OS work in late 2025 and early 2026. The earliest CLAUDE.md in the author's substrate dates to the period when Claude Code was first deployed for personal use. The author's intellectual lineage is documented elsewhere (Tool Inventory Framework November 2025, Substrate Thesis genesis February 2026, Prompt-Engineering Field Guide February 2026, Substrate Thesis Companion April 2026); the lineage doesn't reference Miessler's Substrate as an influence because the author didn't discover Miessler's work until April 24, 2026, well after the convention had become structurally embedded in the author's substrate.

The instances are independent. The convergence is therefore evidence of a structural pattern, not of cross-pollination.

---

## Why the SRD claim holds

For this to be a Stable Recursive Decomposition rather than a coincidence, the five SRD properties need to hold at the cross-practitioner scale.

### 1. Same structural shape at multiple scales

Both instances exhibit the same shape. The shape is: single-file, root-level, markdown, authoritative, globally loaded, per-scope tunable. The variations between Miessler's and the author's instances (specific contents, specific vocabulary, specific scope) are within-pattern variations; the structural shape is preserved.

The pattern also recurs at multiple scales within each practitioner's substrate. Miessler's framework has the convention at the framework level. The author's substrate has it at the global level (for cross-project rules) and at the per-project level (for project-specific extensions). Two scales within one practitioner's work; the convention applies identically at both scales.

### 2. Same correctness guarantees at every scale

Both instances treat the operating-instructions file as authoritative within its scope. When the file says something, downstream consumers (AI assistants, human collaborators, future-self) follow it. The criterion for "the file is being used correctly" is the same: is it being read at session-open, is it being treated as authoritative, is it being updated deliberately rather than silently mutated.

This holds across instances and across scales. Miessler's `CLAUDE.md` and the author's `CLAUDE.md` have the same correctness criteria. The author's global `CLAUDE.md` and the author's per-project `CLAUDE.md` have the same correctness criteria.

### 3. Same failure modes at every scale

The known failure modes of the convention are the same wherever it appears. The file gets too long and people stop reading it. The file gets stale because nobody updates it. The file conflicts with other sources of operating instructions and the conflict isn't resolved cleanly. The file's scope gets ambiguous and people don't know whether to put a new rule in the global file or a per-project file.

Each failure mode is documented in practice. Mitigations developed for one practitioner's substrate apply to the other's. The failure-mode catalog is portable.

### 4. Per-scale autonomous operation

Each instance operates autonomously within its scope. Miessler's `CLAUDE.md` doesn't depend on the author's; the author's doesn't depend on Miessler's. Within the author's substrate, the global `CLAUDE.md` and the per-project variants operate autonomously — a per-project variant doesn't break if the global file is updated, as long as the project-specific extensions are still valid.

The autonomy is structural. Each instance is a self-contained operating-instructions file for its scope.

### 5. Cross-scale informativeness

This is the property that's hardest to demonstrate at the cross-practitioner scale, because a strong demonstration would require studying many practitioners' instances and showing that lessons learned at one practitioner's scale propagate to others. With only two confirmed instances, the demonstration is preliminary.

But the preliminary evidence is consistent. The fact that Miessler and the author independently arrived at structurally-similar conventions is itself evidence that the pattern is real — that the underlying problem (authoritative operating instructions for AI-augmented work) has the same structural solution wherever it's encountered. Lessons Miessler has learned about how to keep his `CLAUDE.md` useful (presumably documented in his framework's evolution) would apply to the author's substrate. Lessons the author has learned (codified in this substrate's protocol files and case studies) would apply to Miessler's framework.

A more rigorous demonstration would require a prevalence study (see TODO at end of this case).

---

## What the convergence reveals about the Substrate Thesis

If the convention had been invented by one practitioner and adopted by others through imitation, the convergence would tell us something about social diffusion. It would not tell us much about whether the pattern is structurally necessary.

Independent emergence is different. When two practitioners — with different backgrounds, different domains of expertise, different bodies of work, no documented mutual awareness during the relevant development window — arrive at structurally-identical conventions, the most parsimonious explanation is that they're both responding to the same structural pressure. The pattern emerges because the problem it solves has the same structural solution wherever the problem is encountered.



This is the Substrate Thesis's strongest claim in microcosm. The framework asserts that FKS, SCC, and SRD patterns appear in well-formed personal cognitive infrastructure not because they're a methodology somebody invented, but because they're the structural shape that cognitive infrastructure takes when it holds together over time. The convergent CLAUDE.md pattern is empirical evidence for the same claim at one specific scale: the operating-instructions convention is what cognitive substrates converge to when they're built seriously enough to need authoritative cross-session context.

The pattern is, in this sense, *discovered rather than invented*. Practitioners who try to build serious cognitive substrates without it run into the problems it solves and eventually rediscover it. Practitioners who start with it benefit from the convention without having to learn its necessity through failure.

---

## What this case adds to the broader corpus

Cases 01-06 establish that the FKS / SCC / SRD patterns are recognizable in well-formed personal substrate work. They establish that the patterns compound across artifact types and time scales. They establish that the patterns can be made deliberate rather than implicit.

Case 07 adds that the patterns *aren't idiosyncratic*. They aren't features of one practitioner's working style or one personality's preferences. They're structural features of cognitive infrastructure that emerge wherever the infrastructure is built seriously enough to need them. The SRD claim — that the patterns recur across instances with the same structural guarantees — extends not just across artifact types within one substrate, but across substrates built independently by different practitioners.

This is the strongest form of the Substrate Thesis claim. The framework isn't describing one practitioner's idiosyncratic methodology. It's describing the structural shape that personal cognitive infrastructure takes when it's built to last. The shape is recognizable, repeatable, and predictable — and it's recognizable across practitioners, not just within one.

---

## Acknowledged limitations

This case study has clear gaps that should be addressed in future revisions.

**Sample size of two.** Two confirmed instances is not a prevalence study. A more rigorous demonstration would identify many practitioners who use the convention, characterize the variation in their implementations, and verify the SRD properties hold across the full sample.

**Selection bias.** Both confirmed instances are from practitioners who deliberately publish their work in public repositories. Practitioners who use the convention privately (which may be the majority) are invisible to a public-repository search. The visible sample may not be representative.

**Self-reporting risk.** The author of this case study is one of the two confirmed instances. There's a structural risk that the case study over-fits the pattern to the author's own practice. A rigorous version of this case would be written by an independent observer, ideally one who has not adopted the convention themselves.

**Lack of formal prevalence study.** The strongest version of this case would include a quantitative survey: how many public repositories on GitHub have a `CLAUDE.md` (or `AGENTS.md`, or similar) at root? How does that number compare to repositories that use AI-augmented development tools but don't have such a file? What predicts adoption? A formal prevalence study would convert this case from "two confirmed instances + structural argument" to "N confirmed instances + statistical evidence."

**Time horizon.** Both confirmed instances are recent (within the past year). Whether the convention is durable — whether it persists in practitioners' substrates over multi-year horizons — can't be evaluated yet because the convention itself is too new. Longitudinal study is needed.

These limitations don't undermine the case; they constrain its strength. The case as written is sufficient to establish that *the pattern recurs across at least two independent practitioners*. Stronger claims require the broader study acknowledged in the TODO below.

---

## A priori variation taxonomy (for use during prevalence study)

Before running a prevalence study, defining the classification dimensions in advance prevents post-hoc interpretation bias. The following taxonomy is proposed as the classification scheme for any future data collection. It was derived from analyzing the two confirmed instances + the structural properties listed earlier in this case.

### Dimension A — Filename convention

The convention appears under multiple filenames:
- `CLAUDE.md` — most common in Anthropic-ecosystem repositories
- `AGENTS.md` — provider-neutral proposal; emerging
- `.cursorrules` — Cursor IDE-specific
- `.aider.conf.yml` — Aider-specific
- `.github/copilot-instructions.md` — GitHub Copilot-specific
- `SYSTEM.md`, `INSTRUCTIONS.md`, `CONTEXT.md` — generic variants
- Multiple-file combinations (e.g., `CLAUDE.md` + `AGENTS.md` coexisting)

**Concrete example of variation:** Miessler's `Substrate` repo uses `CLAUDE.md`; the same-day-examined Anthropic official repos (e.g., `anthropics/claude-code`) also use `CLAUDE.md` as the canonical filename but with different content structure. The filename is convergent; the content is not. This is exactly what the SRD claim predicts — structural invariance on Dimension A with within-pattern variance on Dimension D.

### Dimension B — Location

The convention's structural claim is *root-level*. Variations:
- Repository root (canonical)
- `.claude/` subdirectory (common for per-scope variants)
- `docs/` subdirectory (less canonical; suggests weaker authority claim)
- Home directory globals (`~/.claude/CLAUDE.md`) — applies across repositories

**Concrete example of variation:** most public instances place the file at repository root (canonical); a minority place it in `.claude/` (secondary scope); very few place it in `docs/` (suggests the author views it more as documentation than as operating instructions). The root-level placement is load-bearing for the "authoritative-by-default" property; non-root placements often correlate with weaker authority-treatment downstream.

### Dimension C — Scope declaration

What the file's authority covers:
- Global / machine-level (e.g., a practitioner's `~/.claude/CLAUDE.md`)
- Project-level (most common; per-repository)
- Team-level (shared operating instructions across collaborators)
- Framework-level (e.g., Miessler's `Substrate/CLAUDE.md` governing contributions to that specific framework)

**Concrete example of variation:** single-practitioner substrates commonly have a global `~/.claude/CLAUDE.md` plus per-project variants that extend the global. Team substrates typically lack the global layer (no shared home directory) but may have more extensive project-level files. Framework-level files (Miessler's case) govern contributions to a specific framework and sit at the intersection of project-level and team-level — scoped to the framework, shared across contributors.

### Dimension D — Content categories present

Common content patterns (present in one or both confirmed instances):
- Vocabulary definitions (domain-specific terms)
- Engineering standards (code conventions, test requirements, documentation standards)
- Communication conventions (tone, verbosity, response format)
- Protocol references (pointers to specific procedural documents)
- Machine / environment context (hardware, OS, tool versions)
- Security / credential rules (never-in-chat, always-DPAPI, etc.)
- Destructive-operation gating (confirmation required for certain actions)
- Named failure modes + mitigations

**Concrete example of variation:** Miessler's `CLAUDE.md` focuses heavily on vocabulary (the 17+ noun-typed knowledge components) because his framework IS a vocabulary. A single-practitioner personal-OS file focuses heavily on engineering standards + security + destructive-operation gating because those rules are what keep individual infrastructure coherent under AI assistance. Both files exhibit the operating-instructions convention; the specific content categories emphasized reflect the author's use case.

### Dimension E — Length + structure

Observable structural variation:
- Short (<1KB) — minimal rules; essentially a preamble
- Medium (1-5KB) — full convention with categories
- Long (5-20KB) — comprehensive with sub-protocols inline
- Sectioned vs. flowing prose
- Numbered rules vs. narrative convention

**Concrete example of variation:** starter templates in the wild (AGENTS.md examples, Anthropic's boilerplate) are typically <1KB — just enough to establish vocabulary. Mature single-practitioner personal-OS files grow to 5-15KB as the practitioner discovers and encodes rules over months. Framework-contribution files (Miessler's case) sit in the medium range because their scope is bounded by what framework-contributors need to know, not everything the framework author knows about AI-augmented work.

### Dimension F — Update cadence indicator

When the file was last modified + commit-history density:
- Static (created once; rarely touched)
- Gradually evolving (monthly-to-quarterly updates)
- Active (weekly updates or faster)
- Abandoned (initial creation then silent for months)

**Concrete example of variation:** static files typically indicate the convention was adopted as scaffolding and never subsequently iterated (common in starter-template cases). Active files typically indicate a practitioner treating the file as load-bearing infrastructure (the author's is in this category; commit history shows weekly-to-monthly updates). Abandoned files indicate adoption-by-imitation followed by disuse — a useful signal for the "adoption via social diffusion vs structural necessity" hypothesis test (H0 in the formal prevalence study).

### Dimension G — Integration with other operating-instructions layers

Whether the file is:
- Standalone authoritative
- One of multiple coordinated files (e.g., `CLAUDE.md` + `AGENTS.md` + `.cursorrules` all present)
- Paired with a `memory/` or `.claude/memory/` directory for per-topic content
- Cross-referenced from other documents

**Concrete example of variation:** the author's substrate pairs `CLAUDE.md` with a `memory/` directory containing several dozen per-topic files — Dimension G shows a strong "paired with memory/" integration pattern. Miessler's substrate uses a more standalone-authoritative pattern; his framework content lives outside the `CLAUDE.md`. Multi-file coordinated patterns (`CLAUDE.md` + `AGENTS.md` + `.cursorrules` simultaneously) typically indicate practitioners supporting multiple AI tooling providers — a heterogeneity signal rather than a substrate-maturity signal.

### Dimension H — Practitioner context (where observable)

What can be inferred from public profile:
- Solo practitioner vs. team
- Domain (web dev, infra, data, research, personal-OS, etc.)
- Years using AI-augmented development
- Public contribution to AI-tooling discourse (Twitter/X, Substack, blog posts about AI workflow)

**Concrete example of variation:** practitioners with public AI-workflow discourse (bloggers, Substack authors, Twitter/X presence) typically have longer and more-active operating-instructions files — their substrate work IS part of their public output. Practitioners without such public discourse tend toward shorter, more-project-specific files — their substrate is operational rather than rhetorical. This correlation tests the H0 "social-diffusion" hypothesis: if most mature files belong to high-visibility practitioners, diffusion is plausible. If mature files are evenly distributed across visibility tiers, convergent design is more plausible.

### How to use the taxonomy

During the prevalence study, each sampled repository's operating-instructions convention (if present) should be coded along all 8 dimensions. The resulting data matrix permits:

- **Descriptive statistics** per dimension (e.g., what fraction of instances use each filename convention)
- **Cross-dimensional correlation** (e.g., does filename choice predict content category composition?)
- **Invariant identification** (which dimensions show low variance — these are the SRD's structural shape)
- **Variant characterization** (which dimensions show high variance — these are within-pattern variation)

The SRD claim is empirically supported if: dimensions A-C exhibit structural invariance (same shape across instances), while dimensions D-H exhibit within-pattern variance (individual practitioners vary in specifics but all instances share the structural shape).

---

## Formal prevalence study protocol (executable runbook)

A formal prevalence study would substantially strengthen this case. The following protocol is ready-to-execute; the data collection requires either GitHub API access (with rate-limit budget) or an exa.ai search budget. Analysis is offline-feasible once data is collected.

### §1 — Research hypotheses

**Primary hypothesis (H1):** The convergent operating-instructions-at-repo-root convention exhibits Stable Recursive Decomposition properties across independent practitioners' substrates — specifically, dimensions A-C (filename convention / location / scope declaration) exhibit low variance across sampled instances.

**Secondary hypothesis (H2):** Dimensions D-H exhibit higher variance than A-C, supporting the within-pattern variance claim. This establishes that the convention is structurally recognizable (A-C invariance) while accommodating practitioner-specific customization (D-H variance).

**Null hypothesis (H0):** The convention is socially-diffused rather than structurally-convergent. If H0 is true, we would expect: (a) adoption predicted primarily by proximity to high-profile instances rather than by independent discovery, and (b) uniform copying of content patterns rather than convergent structural shape with divergent specifics.

### §2 — Sampling methodology

**Target sample size:** N ≥ 100 repositories with the convention (statistical significance threshold; pilot study at N=30 first for power-analysis calibration).

**Sampling frame:** all public GitHub repositories with a root-level file matching any of the filenames in Dimension A (CLAUDE.md, AGENTS.md, .cursorrules, .aider.conf.yml, .github/copilot-instructions.md, SYSTEM.md, INSTRUCTIONS.md, CONTEXT.md), or any combination thereof.

**Sampling procedure:** stratified random sample with strata on (a) filename convention (Dimension A), (b) project activity level (repos with commits in past 6 months vs. inactive), (c) approximate project size (stars/forks bins). Within each stratum, simple random sample to target proportion.

**Inclusion criteria:**
- Public GitHub repository
- File is present at root (or recognized location per Dimension B)
- File is ≥200 bytes (exclude placeholder / empty files)
- Repository has at least one commit in past 12 months (exclude abandoned)

**Exclusion criteria:**
- Forks of other repositories (avoid double-counting via inheritance)
- Template repositories (avoid systematic bias from single-author templates adopted by many)
- Repositories whose convention file consists only of references to another file (content is elsewhere)

### §3 — Data collection instrument

For each sampled repository, code the following into a structured record (JSON schema provided in `docs/research_instruments/prevalence_study_schema.json` — to be authored if study is executed):

```json
{
  "repo_url": "...",
  "sampled_at": "ISO-8601 timestamp",
  "filename": "...",              // Dimension A
  "location": "...",              // Dimension B
  "scope": "...",                 // Dimension C
  "content_categories": [...],    // Dimension D (multi-select)
  "length_bytes": N,              // Dimension E
  "structure": "sectioned|prose", // Dimension E
  "last_modified": "ISO-8601",    // Dimension F
  "commit_count": N,              // Dimension F
  "paired_files": [...],          // Dimension G
  "practitioner_context": {...}   // Dimension H
}
```

### §4 — Analysis plan

**Descriptive analysis:**
- Frequency distribution for each of Dimensions A-H
- Cross-tabulation of filename × content categories, filename × length, location × scope
- Visual: heatmap of dimension co-occurrence

**Variance analysis:**
- For categorical dimensions: entropy / Gini coefficient (lower = more invariant)
- For continuous dimensions: coefficient of variation
- Compare variance across A-C (hypothesized low) vs. D-H (hypothesized higher)

**Primary hypothesis test (H1):**
- Operationalize "low variance on A-C" as: A entropy ≤ log(3) (≤ 3 effective filename categories despite many possible), B entropy ≤ log(2), C entropy ≤ log(3)
- If observed entropies meet thresholds: fail to reject H1
- If not: reject H1; the pattern is more variable than the SRD claim allows

**Secondary hypothesis test (H2):**
- Test whether mean entropy across A-C is significantly lower than mean entropy across D-H
- Two-sample permutation test on entropy values
- If p < 0.05: support H2

**Null hypothesis assessment (H0):**
- Regress adoption on proxies for social proximity (practitioner follows Miessler / Anthropic / other visible CLAUDE.md authors on GitHub or Twitter)
- If social-proximity predicts >50% of adoption variance: H0 supported
- If social-proximity predicts <20%: H0 rejected; independent convergence is the better explanation
- If 20-50%: mixed; both mechanisms at play

### §5 — Reporting template

The prevalence study results should be reported as an appendix to this case study (case_studies/07_appendix_prevalence_study.md) with the following structure:

1. **Abstract** — 150 words on methodology, sample, key findings, implications for SRD claim
2. **Methods** — sampling frame, inclusion/exclusion, data collection period, ethical considerations
3. **Descriptive results** — frequency distributions, cross-tabulations
4. **Hypothesis tests** — H1, H2, H0 assessments with statistics
5. **Qualitative observations** — notable instances, unexpected patterns, outliers
6. **Limitations** — sampling bias, self-selection (only public repos visible), temporal snapshot vs. longitudinal
7. **Implications** — what the results mean for the Substrate Thesis and for practitioner education
8. **Raw data availability** — JSON records (anonymized if needed) in supplementary materials

### §6 — Resource requirements

**Data collection:** ~8-16 hours with GitHub API (subject to rate limits); ~4-8 hours with exa.ai search credits if available. Target 100 repositories.

**Analysis:** ~4-8 hours once data collected. Python + pandas sufficient; no specialized statistical software needed.

**Writing:** ~4-6 hours for appendix-style writeup.

**Total estimated effort:** 16-30 hours across data collection + analysis + writing. Executable as a single tool-budgeted assistant session, or as an author-pen focused-session block.

### §7 — Execution readiness

The protocol is execution-ready — all methodology decisions, hypothesis formulations, analysis plans, and reporting formats are specified in advance. Future execution needs only: (a) GitHub API access or exa.ai budget for data collection, (b) an analysis session, (c) the writeup time.

The a priori taxonomy (preceding section) provides the classification dimensions. The protocol (this section) provides the research design. Together they convert the case 07 TODO from "run a prevalence study someday" to "execute this specific protocol when budget permits."

---

## TODO for future revisions (updated)

~~Six-item TODO list superseded 2026-04-24 by the formal prevalence-study protocol above.~~ The protocol is execution-ready; what remains is resource availability (exa budget or GitHub API time) plus an execution session.

Remaining work beyond the prevalence study:

- **Longitudinal tracking.** Once the prevalence study establishes cross-sectional prevalence, repeating the study at 12-month intervals establishes longitudinal durability. Is the convention stable over time, or does it churn?
- **Practitioner interview study.** Complement the repository-level data with practitioner-level data via interviews. Ask practitioners how they discovered the convention, how they maintain it, what failure modes they've observed. Qualitative data complements the quantitative prevalence data.
- **Cross-language / cross-tooling study.** Does the convention appear in AI-augmented workflows outside the Claude / Anthropic ecosystem? Cursor, Aider, GitHub Copilot, local-LLM workflows — do they exhibit the convention? If yes, the SRD claim generalizes beyond Anthropic-specific tooling.
- **Structural-similarity metric.** Develop a quantitative measure of how similar two instances are (Jaccard on content categories; normalized edit distance on content; etc.). Apply to sampled pairs and verify that the structural-invariance claim holds at the pairwise level, not just aggregated.

---

## Connection to other case studies

| Case | Relationship to case 07 |
|---|---|
| Case 01 (Descriptive Insights v1 → v2) | Within-substrate SRD instance; case 07 extends to cross-substrate |
| Case 02 (Operating Stack v1 → v1.3.1) | Within-substrate SRD; case 07 demonstrates the convention case 02 evolves IS itself an SRD pattern |
| Case 03 (Master Log Audit Cadence) | Canonical within-substrate SRD; case 07 is the cross-substrate analog |
| Case 04 (Job-Crawler Cross-Domain) | Cross-domain SRD within one substrate; case 07 is cross-practitioner SRD |
| Case 06 (Personal-OS Year-Over-Year) | Longitudinal within-substrate evolution; case 07 cross-sectional across substrates |

The case studies progressively widen the scope of the SRD claim. Cases 01-02 demonstrate the pattern at the artifact-type level. Cases 03-04 demonstrate it at the framework-and-architecture level. Case 06 demonstrates it crossing the time-horizon boundary. Case 07 demonstrates it crossing the practitioner boundary.

Each case adds a degree of generality to the framework's empirical grounding. Case 07 is the most ambitious; with the prevalence study added, it would also be the most rigorously supported.

---

## What this case study does NOT claim

For honest positioning:

- Does NOT claim Miessler's Substrate framework is structurally similar to the Substrate Thesis itself. The frameworks operate at different scales (collective vs. personal) and serve different purposes. The convergence documented here is at the operating-instructions convention level, not at the framework level.
- Does NOT claim the author's adoption of the convention preceded Miessler's or vice versa. Both adoptions are recent; precedence is not the relevant question.
- Does NOT claim the convention is universally beneficial. Some practitioners may have substrates where the convention isn't load-bearing. The claim is that *where the convention appears*, it has consistent structural properties — not that it should be everywhere.
- Does NOT claim adoption-by-imitation isn't also occurring. Some practitioners undoubtedly adopt the convention because they've seen others use it. The independent-emergence claim applies specifically to the documented Miessler + author instances; broader adoption may have different dynamics.

---

*Case Study 07 first draft 2026-04-24. Companion to theory/SRD_Definition_and_Examples.md v2 + docs/prior_art_survey.md Category 0 + cases 01-06. Subject to revision when formal prevalence study is conducted (TODO above). Distinguishing contribution: extends SRD claim from within-substrate to cross-practitioner scope.*
