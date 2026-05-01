# Differentiation Analysis — Substrate Thesis vs. Robbes et al. arXiv 2601.18341
## "Agentic Much? Adoption of Coding Agents on GitHub"

**Status:** Authored 2026-04-25 from deep-research extraction (research ID `r_01kq29zy9df70sm8h3xpnk466s`, $0.30 cost). Companion to `differentiation_vs_gloaguen_2602_11988_20260425.md` + `prior_art_survey.md` Category 4.1 + `academic_paper_outline.md` §2.5.

> **Audit correction 2026-04-30:** This memo originally attributed the paper to "P. M. Konrad et al." That attribution was wrong (cross-contamination from arXiv 2604.04990 *Architecture Without Architects*, which IS by Konrad et al.). Direct arXiv WebFetch verification on 2026-04-30 confirmed the actual authors of arXiv 2601.18341 are **Romain Robbes, Théo Matricon, Thomas Degueule, André Hora, Stefano Zacchiroli**. All "Konrad et al." references in this memo are corrected to "Robbes et al."; cite as **Robbes et al. (2026)**. The filename retains `konrad` for git-history continuity (per `bibliography.md` §H audit metadata note); content attribution is the authoritative source. The intellectual analysis below (architectural critique, complementarity argument, etc.) stands unchanged — it concerns the paper's findings (which are real) and the Substrate Thesis's positioning (which is independent of authorship attribution).
>
> Adoption-rate numbers in the memo body (`15.85%–22.60%` on `129,134 projects`) are from the v1 paper at memo-authoring time (Jan 26 2026); the v2 paper (Apr 8 2026 revision) reports `22.20%–28.66%` on `128,018 projects`. The numbers in this memo correspond to the v1 figures the deep-research-extraction was based on; for any publication-bound use, refresh against the v2 numbers via direct arXiv read.

---

## TL;DR for the CHI submission

Robbes et al. ("Agentic Much?" arXiv 2601.18341, early 2026) is the second-most-competing academic prior-art for the Substrate Thesis. They present **the largest empirical study of coding-agent adoption on GitHub to date** — 129,134 projects analyzed, finding **15.85%–22.60% adoption rate**, broad across project maturity / languages / organizations. Their contribution is empirical-descriptive (how prevalent is agent use; what observable traces; what commit-level patterns).

**Their gap (Substrate Thesis fills it — same pattern as Gloaguen):**
1. **No multi-dimensional structural taxonomy** — they articulate the "agentic loop" mechanism and distinguish detection signals (file-level traces vs commit-level metadata) but don't provide the kind of repeatable framework for classifying agentic artifacts that the 8-dimension a priori taxonomy provides
2. **No convergence-vs-diffusion analytical lens** — they document adoption distribution but don't theorize when/why architectures converge vs diffuse
3. **No PKM / personal-informatics / system-design pattern engagement** — their related work is exclusively SE/ML systems literature + technical-debt literature + qualitative human-agent studies; doesn't engage with structural-pattern academic canon
4. **Detection-method-bound rather than theory-driven** — explicitly heuristic, with acknowledged under/over-counting risks; they treat this as a methodological limitation rather than as evidence that a theory-grounded operationalization is needed
5. **Adoption framing rather than substrate framing** — they treat coding-agent adoption as a discrete event ("does this project have agent traces?") rather than as one instance of a broader cognitive-infrastructure pattern (FKS / SCC / SRD across artifacts)

**Strategic positioning:** Robbes et al.'s adoption figures (15.85%–22.60% across 129K projects) are **strong supporting evidence** for the Substrate Thesis's prevalence claim. Cite as foundation for the "convention is real and widespread" empirical baseline; differentiate by providing the structural framework that explains the adoption pattern rather than just measuring it.

---

## Key extracted findings

### Abstract verbatim
> "In the first half of 2025, coding agents have emerged as a category of development tools that have very quickly transitioned to the practice. Unlike 'traditional' code completion LLMs such as Copilot, agents like Cursor, Claude Code, or Codex operate with high degrees of autonomy, up to generating complete pull requests starting from a developer-provided task description. This new mode of operation is poised to change the landscape in an even larger way than code completion LLMs did, making the need to study their impact critical. Also, unlike traditional LLMs, coding agents tend to leave more explicit traces in software engineering artifacts, such as co-authoring commits or pull requests. We leverage these traces to present **the first large-scale study (129,134 projects) of the adoption of coding agents on GitHub**, finding an estimated **adoption rate of 15.85%–22.60%**, which is very high for a technology only a few months old—and increasing. We carry out an in-depth study of the adopters we identified, finding that adoption is broad: it spans the entire spectrum of project maturity; it includes established organizations; and it concerns diverse programming languages or project topics. At the commit level, we find that commits assisted by coding agents are larger than commits only authored by human developers, and have a large proportion of features and bug fixes. These findings highlight the need for further investigation into the practical use of coding agents."

### Methodology summary
- **Sample:** 129,134 projects (Abstract); 128,018 projects in some sub-analyses
- **Detection method:** repository-level heuristics — agent-specific configuration files (.cursorrules class) + commit/PR metadata (co-authorship; commit messages)
- **Time window:** dataset snapshots through **February 21, 2026**
- **Sampling intent:** broad across project maturity, languages, organization types
- **Limitation acknowledged:** heuristic with both under/over-counting risk; can't capture private-repo or in-IDE-only usage

### Headline quantitative findings
| Metric | Value |
|---|---|
| Project-level adoption rate | **15.85% – 22.60%** |
| Project-level file-trace evidence | ~7.89% (sub-analysis) |
| Commit-level metadata evidence | ~8.64% (sub-analysis) |
| Total sample | 129,134 GitHub projects |
| Time-series start | March 2025 (rapid growth begins) |
| Growth pattern | "Ballooning"; concentrated in small number of agent providers |

### Their conceptual framing
- **Coding agent definition:** "a LLM running in a loop with tool access that aims to complete a given goal" (Section 2.1)
- **Distinguishing feature from completion-only LLMs:** scale + autonomy
- **Trace types:** configuration files, knowledge summaries, commit/PR metadata
- **Filename variants:** acknowledged but not exhaustively catalogued; .cursorrules used as illustrative example

### Their gap statement / contribution claim
> "The paucity of work studying coding agents motivates us to study this from another angle. While completion-based coding assistance embedded in the IDE is hard to track in the wild, since it leaves no explicit traces, coding agents leave abundant traces in software repositories... This paves the way to study the adoption of coding agents in the real world at a very large scale, **a point of view that is highly complementary to the existing qualitative studies**."

Their explicit framing: their study is *complementary to* existing qualitative work, not competitive. They claim the empirical-scale niche.

### Their related work — what they cite + notable absences
**Cited:**
- Code completion / Copilot empirical studies
- Earlier qualitative AI-assisted programming studies
- SE / repo-mining methodology precedents (commit/PR metadata analysis)
- Technical-debt literature (classic ML / system debt discussions)

**NOT cited:**
- PKM literature
- Personal informatics
- System-design pattern academic canon
- Knowledge-management theory

(Same notable absence as Gloaguen et al. — both empirical-SE papers don't engage with the structural-pattern / cognitive-infrastructure literature the Substrate Thesis draws from.)

### Their explicit limitations
- Heuristic detection with under/over-count risk
- Public-repo-only scope; misses in-IDE completion, private/enterprise telemetry
- No deep qualitative usage insights (manual commit labeling but not extensive user-study)
- Snapshot-in-time; rapidly-evolving landscape may shift findings

### Their future-work
- Further investigation into practical use of coding agents
- Agent impact on workflows + quality
- Human-agent interaction dynamics
- Supervision/autonomy spectrum
- Security implications

---

## Differentiation matrix

| Dimension | Robbes et al. (arXiv 2601.18341) | Substrate Thesis (Caddell, in prep for CHI 2027) |
|---|---|---|
| **Question type** | Descriptive-empirical: how widespread is coding-agent adoption? | Theoretical-structural: what patterns make personal cognitive infrastructure compound? |
| **Unit of analysis** | Project (does it show agent traces?) | Multi-artifact substrate with FKS/SCC/SRD relationships |
| **Sample size** | 129,134 GitHub projects | 6 case studies + 24-instance preliminary + N≥100 stratified study (planned) |
| **Method** | Heuristic trace-detection + commit metadata analysis | Practitioner-theorist autoethnography + cross-practitioner prevalence study |
| **Empirical target** | Adoption rate; commit-level effects | Compounding vs decay over multi-month horizons; cross-practitioner convergence |
| **Theoretical framework** | None articulated; "agentic loop" as descriptive mechanism only | FKS/SCC/SRD triple + 8-dimension a priori taxonomy + convergence-vs-diffusion lens |
| **Time horizon** | Cross-sectional snapshot (project-level adoption events) | Multi-month / multi-year personal-OS evolution |
| **Domain** | All public GitHub (broad) | Personal cognitive infrastructure for AI-augmented knowledge work |
| **Output type** | Empirical findings + future-work pointers | Diagnostic framework + 24 named anti-patterns + Health Indices + structural prescriptions |

The two works are **complementary, not competing.** Robbes et al. measure adoption at scale; Substrate Thesis explains the structural pattern producing the adoption.

---

## Anticipated critiques + pre-emptive responses

### Critique 1: "Your taxonomy is theoretical/overly prescriptive compared to our empirical evidence-driven, large-scale analysis"
**Response:** Acknowledged. The 8-dimension taxonomy is *operationalized via measurable repo-level + commit-level indicators* that map directly to the trace types Robbes et al. use (file-level traces → Dimensions A/B; commit metadata → Dimensions F/G; content categories → Dimension D). The Substrate Thesis CHI submission can explicitly demonstrate per-dimension operationalization using their detection heuristics as the empirical foundation.

### Critique 2: "You underestimate adoption heterogeneity and the pragmatic constraints of detecting agentic activity"
**Response:** Robbes et al. themselves acknowledge heuristic limits + under/over-counting risk. The Substrate Thesis prevalence-study protocol (Case Study 07) explicitly addresses this with multi-signal triangulation (file-level + commit metadata + practitioner-context) and reports conservative-vs-aggressive measurement variants per dimension. We adopt their methodological discipline.

### Critique 3: "You ignore socio-technical/qualitative realities of human-agent supervision"
**Response:** Robbes et al. cite qualitative studies as complementary. The Substrate Thesis incorporates targeted practitioner-theorist case studies (Case Studies 01-07 in the companion repo) plus the formal cross-practitioner prevalence study. We complement rather than displace human-centered qualitative findings.

### Critique 4: "Your sample is microscopic compared to ours"
**Response:** N=129,134 projects vs N=24 preliminary + N≥100 planned reflects different research questions. Robbes et al. measure *adoption* (a binary or ordinal trace-presence question — well-suited to massive heuristic scaling). Substrate Thesis measures *structural patterns within the adopting population* (an 8-dimensional coding question requiring per-instance qualitative analysis — better-suited to focused stratified samples). The two empirical bases serve non-overlapping research questions.

### Critique 5: "Why theory at all when the empirical work is sufficient?"
**Response:** Robbes et al.'s own finding — that coding-agent adoption "spans the entire spectrum of project maturity... includes established organizations... concerns diverse programming languages or project topics" — establishes the *phenomenon* but doesn't *explain* it. The Substrate Thesis provides the structural-pattern theory (FKS / SCC / SRD) that predicts *why* the convention recurs across diverse contexts and *what taxonomic dimensions* distinguish productive from unproductive instances.

---

## Recommended CHI §2 Related Work paragraph (to combine with Gloaguen paragraph)

> Recent empirical work has begun documenting both the prevalence and effectiveness of repository-level operating-instructions conventions for AI coding agents. Robbes et al. [arXiv 2601.18341] present the largest study to date (N=129,134 projects), reporting **15.85%–22.60% adoption rates** detectable via repository traces (configuration files, commit metadata) across diverse project maturities, languages, and organization types. Gloaguen et al. [arXiv 2602.11988] complement this with effectiveness analysis on 138 Python tasks, finding LLM-generated context files reduce task success rates and developer-written files only marginally improve them. **Together these studies establish the convention as widespread but with mixed empirical effectiveness.** Our work provides the structural framework explaining *why* the convention recurs (Stable Recursive Decomposition; §3.3) and *which dimensions* distinguish productive from unproductive instances (8-dimension a priori taxonomy; §3.5), addressing the gap both empirical studies acknowledge but neither operationalizes.

---

## Citations to incorporate into prior-art survey

**Primary:**
- Robbes et al. (early 2026). "Agentic Much? Adoption of Coding Agents on GitHub." arXiv:2601.18341. https://arxiv.org/pdf/2601.18341.pdf

**Adjacent works (each now has dedicated differentiation memo as of 2026-04-25; cross-references added per bibliography-hygiene audit):**
- Konrad et al. 2026 (arXiv 2604.04990) — "Architecture Without Architects: How AI Coding Agents Shape Software Architecture" — see `differentiation_vs_konrad_arch_2604_04990_20260425.md`. *Audit-correction note:* the prior bibliography draft cross-contaminated authors between this paper and arXiv 2601.18341 ("Agentic Much?"), incorrectly tagging the latter as also by Konrad et al. Direct arXiv verification (2026-04-30) shows arXiv 2601.18341 is by Robbes et al. and arXiv 2604.04990 is by Konrad et al. — they're different first authors entirely.
- Galster et al. (arXiv 2602.14690) — "Configuring Agentic AI Coding Tools: An Exploratory Study" — see `differentiation_vs_galster_2602_14690_20260425.md`
- Bakal (arXiv 2603.14805) — "Knowledge Activation: AI Skills as the Institutional Knowledge Primitive for Agentic Software Development" — see `differentiation_vs_bakal_2603_14805_20260425.md`
- Zhang et al. (arXiv 2603.23448) — "Code Review Agent Benchmark" — see `differentiation_vs_zhang_crab_2603_23448_20260425.md`
- Drexel research portal: "Where Do AI Coding Agents Fail" (preprint by drexel.edu) — uninspected; deferred

The "awesome-agentic-coding-papers" GitHub list (archersama/awesome-agentic-coding-papers) is a literature-aggregation source worth periodic monitoring.

---

## Strategic recommendation

After three deep-research passes (initial Case 07 prevalence + Gloaguen differentiation + Konrad differentiation), the **prior-art landscape is becoming legibly mapped:**

| Paper | Question type | Method | Key finding |
|---|---|---|---|
| Gloaguen 2602.11988 | Effectiveness | Benchmark (138 Python tasks; 3-arm) | Context files reduce task success; recommend minimal |
| Konrad 2601.18341 | Adoption | Large-scale heuristic detection (129K projects) | 15.85%-22.60% adoption rate; broad spread |
| **Substrate Thesis** | **Structural** | **Theoretical framework + autoethnography + cross-practitioner study** | **FKS/SCC/SRD pattern triple explains the convention's recurrence + structural variation** |

The Substrate Thesis occupies a distinct contribution position. **The empirical landscape is being documented by others; we contribute the explanatory framework.**

Pursue full read of CMU MSR He et al. 2026 + arXiv 2510.26103 next; each likely fits the same descriptive-empirical-without-structural-theory pattern. After that, the prior-art differentiation work for the CHI submission's §2 Related Work is approximately complete.

---

*Differentiation Analysis — Substrate Thesis vs. Robbes et al. arXiv 2601.18341, authored 2026-04-25 from Exa deep-research extraction. Cost: $0.30 (54 pages, 5 searches, 1,344 reasoning tokens). Companion to `differentiation_vs_gloaguen_2602_11988_20260425.md` + `prior_art_survey.md` Category 4.1 + `academic_paper_outline.md` §2.5. Subsequent differentiation memos to be authored for CMU MSR 2026 He et al. + arXiv 2510.26103.*
