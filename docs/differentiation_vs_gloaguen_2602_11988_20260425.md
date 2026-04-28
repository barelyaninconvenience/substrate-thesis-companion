# Differentiation Analysis — Substrate Thesis vs. Gloaguen et al. arXiv 2602.11988
## "Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents?"

**Status:** Authored 2026-04-25 from deep-research extraction (research ID `r_01kq297qyv8htt9bs8wkw59765`, $0.41 cost). Companion to `prior_art_survey.md` Category 4.1 + `academic_paper_outline.md` §2.5.

---

## TL;DR for the CHI submission

Gloaguen et al. (ETH Zurich, Feb 2026) is the closest-competing academic work to the Substrate Thesis. Their contribution is **empirical: they show context files at the repository root do NOT reliably improve coding-agent task success** (LLM-generated: −3%; developer-written: only +4% average) **and DO reliably increase inference cost** (20%+). They recommend minimal context files focused on tooling specifics.

**Their gap (Substrate Thesis fills it):**
1. **No structural framework** — they describe content categories functionally; no formal multi-dimensional taxonomy
2. **No convergence-vs-diffusion analytical lens** — they observe behavioral effects (broader exploration, more testing) but don't theorize when/why these are productive vs harmful
3. **No cross-pattern integration** — they treat context files as isolated phenomena, not as one instance of a broader SRD pattern across personal-OS / cognitive-infrastructure substrates
4. **No PKM / personal-informatics framing** — they cite only coding-agent benchmarks + agent industry guidance; don't engage with the broader knowledge-management literature
5. **Single-language scope** (Python) + **outcome-centered** (task success only) — they explicitly limit to repository-issue-resolution outcomes; substrate-thesis-level structural questions (compounding personal cognitive infrastructure) are out-of-scope for their study

The Substrate Thesis can cite Gloaguen et al. as **supporting empirical evidence** for the convention's prevalence (>60,000 repos) AND as the **operational-effectiveness baseline** that the structural framework explains. The Gloaguen finding that "more context can hurt" is consistent with the SCC anti-pattern catalogued in this framework as "container-bleed" — adding content beyond scope-purpose is exactly what would degrade performance.

---

## Key extracted findings (verbatim where possible)

### Abstract verbatim
> "A widespread practice in software development is to tailor coding agents to repositories using context files, such as AGENTS.md, by either manually or automatically generating them. Although this practice is strongly encouraged by agent developers, there is currently no rigorous investigation into whether such context files are actually effective for real-world tasks. In this work, we study this question and evaluate coding agents' task completion performance in two complementary settings: established SWE-bench tasks from popular repositories, with LLM-generated context files following agent-developer recommendations, and a novel collection of issues from repositories containing developer-committed context files. **Across multiple coding agents and LLMs, we find that context files tend to reduce task success rates compared to providing no repository context, while also increasing inference cost by over 20%.** Behaviorally, both LLM-generated and developer-provided context files encourage broader exploration (e.g., more thorough testing and file traversal), and coding agents tend to respect their instructions. Ultimately, we conclude that **unnecessary requirements from context files make tasks harder, and human-written context files should describe only minimal requirements.**"

### Methodology summary
- **AGENTBENCH:** new benchmark, 138 Python tasks, 12 niche repositories with developer-committed context files
- **Complementary set:** SWE-BENCH LITE for LLM-generated context evaluation on popular repos
- **3-arm design:** (a) no context, (b) developer-provided context, (c) LLM-generated context
- **Outcome metrics:** task success rate (primary), inference cost, agent behavioral traces (file traversal, tests run, reasoning steps), instruction adherence

### Headline quantitative results
| Condition | Effect on task success | Effect on cost |
|---|---|---|
| Developer-provided context | +4% average | +20%+ |
| LLM-generated context | −3% average | +20%+ |
| No context | baseline | baseline |

### Their stated contributions
1. AGENTBENCH benchmark
2. Empirical evaluation showing LLM-generated context files reduce performance
3. Trace-based behavioral analysis showing context files increase exploration + testing

### Their explicit limitations
- **Python-only** (Section 6.3, p.11)
- **Single context-file form-factor** (AGENTS.md / repo-root)
- **Outcome-focused** (no semantic-quality analysis of file content)
- **Snapshot in time** (rapidly-evolving agent landscape)

### Their related work
- Coding-agent benchmarks (SWE-bench, etc.)
- Agent industry guidance (AGENTS.md spec, Anthropic, OpenAI)
- Prior descriptive context-file studies (Chatlatanagulchai, Mohsenimofidi, Nigh)
- **NOT cited:** PKM literature, personal informatics, system-design patterns, knowledge-management theory

---

## Differentiation matrix

| Dimension | Gloaguen et al. (arXiv 2602.11988) | Substrate Thesis (Caddell, in prep for CHI 2027) |
|---|---|---|
| **Scope** | Coding agents ↔ repository context files | Personal cognitive infrastructure across artifacts (memory, protocols, writings, code, scripts, audit cadences) |
| **Unit of analysis** | Single context file per repository | Multi-artifact substrate with FKS / SCC / SRD relationships |
| **Domain** | Software engineering (Python only) | Cross-domain (PKM-adjacent, personal informatics, systems work) |
| **Outcome measure** | Task success rate; inference cost | Compounding vs decay over multi-month horizons; cross-practitioner pattern recurrence |
| **Methodology** | Benchmark-driven (AGENTBENCH; 138 tasks) | Practitioner-theorist autoethnography + cross-practitioner prevalence study (planned) |
| **Theoretical framework** | None articulated; functional content categorization | FKS/SCC/SRD triple + 8-dimension a priori taxonomy + convergence-vs-diffusion lens |
| **Time horizon** | Single-task within single agent session | Multi-month / multi-year personal-OS evolution |
| **Prescriptive guidance** | "Minimal context files focused on tooling" | Structural diagnostic framework + 24 named anti-patterns + Health Indices |
| **Empirical base** | 138 task evaluations | 6 case studies + 24-instance preliminary prevalence sample + N≥100 stratified study (planned) |

The two works are **complementary, not redundant.** Gloaguen et al. answers "do context files improve agent task success?" Substrate Thesis answers "what structural patterns make personal cognitive infrastructure compound across multi-month horizons in AI-augmented knowledge work?"

---

## Anticipated critiques + pre-emptive responses

### Critique 1: "Richer structure does not imply better outcomes" (citing Gloaguen's negative results)
**Response:** Acknowledged. The Substrate Thesis's 8-dimension taxonomy is **diagnostic and analytical, not prescriptive-for-richness.** Gloaguen et al.'s finding that "unnecessary requirements... make tasks harder" is consistent with the SCC anti-pattern "container bleed" (adding content beyond scope-purpose) catalogued in `theory/SCC_Definition_and_Examples.md`. The framework provides the structural language to *predict* when context files will help vs hurt — minimal-tooling files exhibit FKS-aligned scope discipline; bloated files violate SCC purpose-scoping. The Substrate Thesis framework explains *why* Gloaguen's finding holds.

### Critique 2: "Added complexity increases cost" (citing 20% inference cost increase)
**Response:** The Substrate Thesis taxonomy explicitly includes operational-cost dimensions. The structural framework predicts that context files exhibiting *poor* FKS / SCC / SRD discipline (e.g., scope creep, lateral leak between sections, cross-layer reach) will produce exactly the increased-exploration / increased-testing / increased-cost behavior Gloaguen observes. Disciplined context files (the framework's reinvigoration template, with explicit scope-acknowledgment + delta-driven updates + forward-pointing) should not exhibit the same cost penalty.

### Critique 3: "Generalizability across languages and agents" (citing Python-only limitation)
**Response:** Substrate Thesis empirical base is multi-domain (PowerShell scripts, markdown writings, Python data-science notebooks, infrastructure configurations, prose). Cross-language / cross-agent generalizability is the framework's claim, not Gloaguen's; we extend rather than challenge their Python-bounded findings.

### Critique 4: "Operationalization of dimensions" (challenging measurement reliability)
**Response:** The 8-dimension taxonomy operationalizes via concrete observables — filename, location, size, content-category presence, last-modified date, integration with adjacent artifacts, practitioner-context. Each dimension can be coded from public-repository inspection alone (no agent traces required). The formal N≥100 prevalence study protocol (in `case_studies/07_convergent_claude_md_cross_practitioner_SRD.md`) specifies inter-coder reliability methodology.

### Critique 5: "Empirical-base size" (138 vs. our N=24 preliminary)
**Response:** Gloaguen's 138-task base evaluates a different question (agent task success). Our N≥100 prevalence study evaluates a different question (structural pattern recurrence). The two empirical bases serve non-overlapping research questions.

---

## Recommended CHI §2 Related Work paragraph (revised draft)

> Gloaguen et al. [arXiv 2602.11988, Feb 2026] provide the closest existing empirical engagement with the operating-instructions-at-repository-root convention. Their AGENTBENCH benchmark across 138 Python software-engineering tasks finds that LLM-generated context files reduce task success rates (−3% average) while developer-written files marginally improve them (+4%), and both modalities increase inference cost over 20%. They conclude that human-written context files should "describe only minimal requirements." Their contribution is the empirical evaluation of context-file effectiveness for coding-agent task completion. Our work is complementary in scope and method: where Gloaguen et al. examine single-file effectiveness for short-horizon software-engineering tasks, we articulate the structural framework explaining why such files recur as one instance of a broader pattern (Stable Recursive Decomposition; see §3.3) across the multi-artifact substrate of personal cognitive infrastructure that AI-augmented knowledge work operates within. Their finding that excess content harms agent performance is consistent with our SCC anti-pattern "container bleed" (Section 5.2); the structural framework provides the diagnostic language for predicting when context files will help versus hurt that their empirical study identifies but doesn't theorize.

---

## Citations to incorporate into prior_art_survey.md

**Primary:**
- Gloaguen, F., et al. (Feb 2026). "Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents?" arXiv:2602.11988. https://arxiv.org/pdf/2602.11988

**Adjacent commentary (for awareness):**
- Eberhardt, C. LinkedIn analysis of Gloaguen et al. https://www.linkedin.com/posts/colin-eberhardt-1464b4a_evaluating-agentsmd-are-repository-level-activity-7430220332390572032-RN_p
- Hacker News discussion (Item 47280099) — community engagement
- Reliable Data Engineering (Medium): "Claude.md Don't Work: ETH Zurich Study Shows Context Files Reduce Success Rates by 3%"
- Upsun developer blog: "The research is in: your AGENTS.md is probably too long"
- Martin Fowler: "Context Engineering for Coding Agents"
- Dortort, F. E. "Don't Ditch AGENTS.md — Fix What's In It"

**Authors' affiliation (per third-party commentary):** ETH Zurich (research group affiliation; primary-source affiliation page not yet verified).

---

## Strategic recommendation

This is the **single most important academic citation** to incorporate into the CHI submission's §2 Related Work. The paragraph above + 1-2 sentences in the Introduction acknowledging that "recent empirical work (Gloaguen et al. 2026) shows the convention's effectiveness for short-horizon coding tasks is mixed" + a Section 5 (Anti-Patterns) tie-in to "container bleed" producing the cost penalty Gloaguen observes — together these positions the Substrate Thesis as **complementary structural/theoretical contribution** rather than a competing empirical claim.

Pursue full read of arXiv 2510.26103 + 2601.18341 + CMU MSR He et al. 2026 next; each likely requires similar differentiation analysis.

---

*Differentiation Analysis — Substrate Thesis vs. Gloaguen et al. arXiv 2602.11988, authored 2026-04-25 from Exa deep-research extraction. Cost: $0.41 (67 pages, 14 searches, 1,344 reasoning tokens). Companion to `prior_art_survey.md` Category 4.1 + `academic_paper_outline.md` §2.5 + `case_studies/07_appendix_prevalence_study_preliminary_20260425.md`. Subsequent differentiation memos to be authored for arXiv 2601.18341, CMU MSR 2026 He et al., arXiv 2510.26103.*
