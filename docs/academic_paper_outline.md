# Substrate Thesis — Academic Paper Outline (v1)
## Parallel track to the Substack series, per Publication+IP Strategic Audit decision #6

**Status:** First outline. Subject to substantial revision once venue is committed.
**Track decision:** PARALLEL TRACK, not conditional on Substack reception. The academic track is pursued for its own merits — bolstering department opportunities regardless of Substack visibility.
**Companion to:** Substack series Essays 1-7 (substantively complete in `docs/essays/`); theory trio v2.1 in `theory/` — FKS, SCC, SRD definitions each with formal diagnostic test, 8 anti-patterns, practitioner-framework comparison, and compliance metrics (proposed Health Indices); 7 case studies (`case_studies/01-07`).

---

## §1 — Working titles (3 candidates; choose at venue commitment)

1. **"The Substrate Thesis: Structural Patterns in Personal Cognitive Infrastructure with AI-Augmented Workflows"** — most direct; emphasizes the framework + the AI-augmented context that distinguishes from pre-LLM personal informatics literature
2. **"Foundational Knowledge Stacks, Stable Cognitive Containers, and Stable Recursive Decompositions: An Empirical Framework for Personal Cognitive Infrastructure"** — most academic; emphasizes the three components by name
3. **"Personal Cognitive Infrastructure That Compounds: A Practitioner-Theorist Framework for AI-Augmented Knowledge Work"** — most narrative; emphasizes the practitioner-theorist position

**Recommendation:** Title #1 for HCI / CSCW venues; Title #2 for Personal Informatics / Software Engineering venues; Title #3 for design-research / autoethnographic venues.

---

## §2 — Venue decision matrix

The right paper depends substantially on venue. Three candidate paths with substantially different framings.

| Venue category | Candidate venues | Audience | Paper length | Tone | Effort |
|---|---|---|---|---|---|
| **HCI / CSCW** | CHI, CSCW, Ubicomp Personal Informatics workshop | HCI researchers + practitioners | 8-15 pages | Empirical, design-research framing | 100-150 hrs |
| **Software Engineering / Personal Informatics** | ICSE, Onward!, Personal Informatics workshops at Ubicomp | SE researchers + tools-builders | 8-12 pages | Architectural, pattern-language framing | 100-150 hrs |
| **Design Research / Autoethnography** | DIS, RTD (Research Through Design), Design Studies journal | Design researchers | 12-20 pages | Reflective practitioner-theorist framing | 80-120 hrs |

**Recommendation pending venue commitment:** **CHI 2027** (submission window: Sep 2026; notification: Dec 2026; conference: spring 2027) is the highest-impact realistic target. Companion submission to Personal Informatics workshop at Ubicomp 2026 (workshop deadline typically May for fall conference) for early feedback before main CHI cycle.

This outline structures for the **HCI / CSCW path**. Adaptable to other paths with reorganization.

---

## §3 — Paper structure (HCI/CSCW path; ~10-12 pages, 6,000-8,000 words)

### Section 1 — Introduction (1-1.5 pages)

**Draft hook (expanded from the Essay 1 recognition moment; CHI-submission-quality narrative):**

*[Draft ¶1]* There's a specific kind of moment that happens to practitioners who build cognitive infrastructure over time without naming what they're building. You're doing routine work — synthesizing months of session notes into a master log, revising a memo, propagating a correction through downstream documents. Somewhere mid-task, you notice the work has a shape. The same five elements keep appearing in each revision. The same layering keeps producing the same bounded-blast-radius property. The same recursive structure keeps applying across artifact types you previously thought were unrelated. The recognition is retrospective, but it's generative: once you can name the patterns, you can deploy them deliberately rather than stumble into them by luck.

*[Draft ¶2 — revised 2026-05-01 to reflect expanded cross-practitioner evidence base]* This paper argues that well-formed personal cognitive infrastructure for AI-augmented knowledge work exhibits three interacting structural patterns: layered knowledge stacks with bounded blast radius (Foundational Knowledge Stacks), versioned reference structures that update via deltas and full regenerations (Stable Cognitive Containers), and the same structural pattern operating at multiple scales (Stable Recursive Decompositions). The patterns are not novel individually — layered architecture [Buschmann et al. 1996], immutable data structures [functional programming canon], and design patterns [Gamma et al. 1994] are well-established in software systems. The contribution is three-fold: (1) demonstrating that these structural patterns recur in *personal cognitive infrastructure* rather than just software systems, (2) articulating their interaction as necessary for compounding rather than decaying infrastructure, and (3) providing empirical grounding through documented case studies plus cross-practitioner convergence evidence drawn from independent practitioner work spanning individual researchers, research organizations, and Anthropic's own production AI infrastructure (Skills system + Cookbooks corpus). The convergence base is meaningfully over-determined: six or more independent practitioners — including the AI lab building the foundational AI itself — have built systems instantiating the same architectural axioms without articulating the meta-framework, indicating the patterns are constraint-imposed by the problem structure rather than diffused stylistic conventions.

*[Draft ¶3]* The practical stakes are increasing. AI-augmented knowledge work makes the *cost* of building personal cognitive infrastructure nearly free (automation lowers the marginal cost of each additional artifact) while making the *cost of building it poorly* nearly fatal (infrastructure that decays instead of compounds consumes attention as it grows). Within months, an undisciplined substrate becomes harder to operate than starting from scratch. Within a year, it's abandoned or forked. The practitioner's effort grows linearly while their leverage stays flat — or inverts, as maintenance exceeds payoff.

*[Draft ¶4 — revised 2026-05-01 with expanded convergence anchors]* The framework we present treats this as a structural problem with a structural solution. We articulate the three patterns formally (§3), demonstrate them via six case studies spanning artifact reinvigoration, framework evolution, audit cadence design, cross-domain architecture reuse, and longitudinal personal-OS evolution (§4), catalog named anti-patterns with documented failure modes and mitigations (§5), and present cross-practitioner convergence evidence where independent practitioners — including individual researchers (Miessler's six-layer personal-OS ecosystem; need-singularity's 14+ repo research stack), distributed open-source communities (mempalace, mcp-memory-service), and the AI lab building the foundational AI itself (Anthropic's Skills production system and Cookbooks pedagogical corpus) — have arrived at structurally-identical conventions through what we argue is convergent design rather than social diffusion (§4 case C + §6 discussion). The presence of this convergence pattern in Anthropic's own production infrastructure is particularly load-bearing for the structural-not-stylistic claim: the practitioners constructing the foundational AI substrate independently converge on the same architectural axioms, suggesting the patterns are imposed by the problem of building durable AI-augmented infrastructure rather than transmitted through any community or vocabulary lineage. We close with implications for HCI design, AI-augmented workflow tooling, and personal informatics research (§6), and honest acknowledgment of limitations (§7).

**Claim statement (concise version for abstract):** Three structural patterns recur in well-formed personal cognitive infrastructure for AI-augmented knowledge work:

1. **Foundational Knowledge Stack (FKS)** — layered structures where each layer reads only its immediate predecessor, producing bounded blast radius
2. **Stable Cognitive Container (SCC)** — versioned reference structures that update via deltas + regenerations rather than continuous mutation, producing bounded cognitive load
3. **Stable Recursive Decomposition (SRD)** — the same structural pattern operating identically at multiple scales and domains, producing cross-scale prediction and pattern-compounding

The patterns are not novel individually. They correspond to layered architecture, immutable data structures, and design patterns respectively in established software-systems literature. The contribution is naming them as a triple specifically for *personal cognitive infrastructure*, demonstrating their interaction empirically, characterizing their failure modes, and providing cross-practitioner convergence evidence that the patterns are structural rather than stylistic.

**Contribution outline:**
- Empirical framework derived from six months of documented practitioner work (single-practitioner longitudinal evidence)
- Six worked case studies plus one cross-practitioner convergence case demonstrating pattern recurrence at multiple scales
- Anti-pattern catalog with 24 named failure modes (eight per pattern) and mitigations
- Quantitative compliance metrics proposed for each pattern (FKS Health Index / SCC Health Index / SRD Health Index) — scaffolded, not validated
- Practical guidance for building minimal viable substrate exhibiting the patterns (30-60-90-365 day progression)
- Cross-practitioner evidence of pattern emergence in independent practitioners (N=6+ confirmed across two Cat-6 ecosystems and four Cat-5 single-axiom convergences per `prior_art_survey.md §5.1-5.9` and `§6.1-6.3`; prevalence study in progress with N=10 academic-paper candidates pending per-paper validation; §7.2 future work)

**Roadmap:** §2 surveys related work across personal knowledge management, personal informatics, system-design pattern literature, and emerging AI-augmented knowledge work research. §3 defines the three patterns formally including graph-notation diagnostic tests and Health Index composition. §4 presents three case studies demonstrating the patterns individually and interacting, plus the cross-practitioner convergence case. §5 catalogs anti-patterns. §6 discusses implications for HCI design, AI-augmented workflow tooling, and personal informatics research. §7 acknowledges limitations and directions for future work.

---

### Section 2 — Related Work (1-1.5 pages)

Three categories of related work. Each addressed in compressed form (1-2 paragraphs each); citations to representative works.

**§2.1 Personal Knowledge Management (PKM) frameworks.** Building a Second Brain (Forte 2022), Getting Things Done (Allen 2001), Evergreen Notes (Matuschak 2019), Zettelkasten (Luhmann via Schmidt 2018). The PKM literature is largely practitioner-prescriptive — describing what to do — with limited treatment of *why* certain practices work or fail. Substrate Thesis complements PKM by providing the structural grammar for what makes PKM practices succeed or decay. PKM tells you *what to do*; Substrate Thesis tells you *why those things work + when they fail*.

**§2.2 Personal Informatics + Lifelogging literature.** The stage-based model of personal informatics systems (Li, Dey, Forlizzi 2010) explicitly studies preparation → collection → integration → reflection → action workflows. Quantified Self literature (Wolf & Kelly 2007 onward). CSCW collaboration patterns (multiple). The personal informatics literature focuses primarily on data-collection-and-reflection workflows; Substrate Thesis extends to the broader personal cognitive infrastructure that surrounds and supports such workflows.

**§2.3 System-design pattern literature.** Layered architecture (Buschmann et al. 1996). Immutable data structures (functional programming canon). Design patterns (Gamma et al. 1994). Microservices (Newman 2015). Domain-driven design (Evans 2003). Substrate Thesis explicitly draws on this literature — the three patterns are personal-infrastructure analogs of patterns established in software systems literature. The contribution is demonstrating that the same patterns appear in personal cognitive infrastructure work, enabling cross-disciplinary recognition.

**§2.4 AI-augmented knowledge work (emerging).** Recent literature on LLM-augmented workflows (Liang et al. 2024; Dell'Acqua et al. 2024; etc.). Substrate Thesis sits in this emerging area but extends beyond LLM-specific patterns to the broader cognitive infrastructure that AI-augmented workflows operate within.

**§2.5 Operating-instructions-at-repository-root convention (CRITICAL prior-art; updated 2026-04-25 with second batch of differentiation memos).** Multiple recent academic and industry analyses establish empirical prevalence of the convention this paper's Case Study C examines:

- **Gloaguen et al. (Feb 2026, arXiv 2602.11988) — "Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents"** evaluates effectiveness on 138 Python tasks; finds context files REDUCE task success (LLM-generated −3%; dev-written +4% only) and INCREASE inference cost 20%+. Recommends minimal context files. Full differentiation analysis at `docs/differentiation_vs_gloaguen_2602_11988_20260425.md`.
- **Robbes et al. (Jan 26 2026, v2 Apr 8 2026; arXiv 2601.18341) — "Agentic Much? Adoption of Coding Agents on GitHub"** N=128,018 projects (v2; was 129,134 in v1); 22.20%-28.66% adoption rate (v2 figures); broad across maturity/languages/orgs. Empirical scale-study without structural taxonomy. Authors: Romain Robbes, Théo Matricon, Thomas Degueule, André Hora, Stefano Zacchiroli. Full differentiation analysis at `docs/differentiation_vs_konrad_2601_18341_20260425.md` (filename retained for git-history continuity; content corrected 2026-04-30 to attribute to Robbes et al.). **Audit note 2026-04-30:** earlier outline drafts attributed this paper to "Konrad et al. (2026a)" — that was cross-contamination from arXiv 2604.04990 (which IS by Konrad et al.). Direct arXiv WebFetch verification 2026-04-30 confirmed authorship; this entry corrected.
- **Konrad et al. (April 5 2026, arXiv 2604.04990) — "Architecture Without Architects: How AI Coding Agents Shape Software Architecture"** position paper introducing **"vibe architecting"** — architecture shaped by prompts rather than deliberate design. Five mechanisms by which agents make implicit architectural choices; six prompt-architecture coupling patterns spanning contingent (may weaken as models improve) to fundamental (persists regardless of capability). Authors: Phongsakon Mark Konrad, Tim Lukas Adam, Riccardo Terrenzi, Serkan Ayvaz. Cite simply as **Konrad et al. (2026)**; no 2026a/2026b disambiguation needed (no longer same-first-author conflict, per audit correction immediately above). Full differentiation analysis at `docs/differentiation_vs_konrad_arch_2604_04990_20260425.md`. **Names the failure mode the Substrate Thesis structural framework prevents.**
- **Galster et al. (Feb 2026 / Apr 9 2026 v3, arXiv 2602.14690) — "Configuring Agentic AI Coding Tools: An Exploratory Study"** N=2,923 GitHub repositories across Claude Code / GitHub Copilot / Cursor / Gemini / Codex; identifies **eight configuration mechanisms** spanning a spectrum from static context to executable workflows; AGENTS.md emerging as cross-tool standard; Skills/Subagents shallowly adopted. Full differentiation analysis at `docs/differentiation_vs_galster_2602_14690_20260425.md`. **Most-citable empirical mechanism inventory; load-bearing for Case Study C prevalence appendix.** Provisional mapping of their 8 mechanisms to FKS/SCC/SRD pattern instances available in companion memo.
- **Bakal (Mar 2026, arXiv 2603.14805) — "Knowledge Activation: AI Skills as the Institutional Knowledge Primitive for Agentic Software Development"** position/framework paper introducing **Atomic Knowledge Units (AKUs)** at enterprise scale. **Convergent meta-claim** ("knowledge architecture > model capability") at different scale and abstraction from Substrate Thesis (enterprise vs personal; content-unit primitive vs structural-pattern framework). Composable rather than competitive. Full differentiation analysis at `docs/differentiation_vs_bakal_2603_14805_20260425.md`. **Framework-level Category 5 candidate** (parallel to mempalace's tool-level convergence; see §2.6).
- **Zhang et al. (Mar 2026 / Apr 7 2026 v3, arXiv 2603.23448) — "Code Review Agent Benchmark"** c-CRAB benchmark + agent evaluation; ~40% solve rate. TANGENTIAL not Category 4. Peripheral §1 Introduction citation only. Full differentiation analysis at `docs/differentiation_vs_zhang_crab_2603_23448_20260425.md`.
- **He et al. (CMU MSR 2026, arXiv 2511.04427) — "Speed at the Cost of Quality"** N=806 Cursor adopters via staggered DiD + matched controls + GMM mediation. **Transient velocity gains + persistent quality degradation; quality mediates long-term slowdown.** Full differentiation analysis at `docs/differentiation_vs_he_msr2026_20260425.md`. **Their mediation finding empirically substantiates the Substrate Thesis's structural-pattern-violation-compounds-into-maintenance-cost claim.**
- **GitHub (2026 blog) — "Lessons from over 2,500 AGENTS.md repositories"** — industry analysis of adoption patterns.
- **Schreiber & Tippe (Oct 30, 2025, arXiv 2510.26103) — "Security Vulnerabilities in AI-Generated Code"** N=7,703 files; 4,241 CWE instances. ADJACENT, not competitive — security topic, not structural-pattern. Cite as supporting evidence for security implications.

These works establish prevalence + adoption + outcome-correlation. They do not articulate the **structural framework explaining why the convention recurs** or the **convergence-vs-diffusion analytical taxonomy**. This paper's contribution is the structural-pattern lens (FKS/SCC/SRD as theoretical framework) + the 8-dimension a priori taxonomy + the convergence-vs-diffusion hypothesis-testing methodology.

**§2.6 Independent-practitioner axiom convergence (Category 5 prior-art; new section added 2026-04-25).** Distinct from §2.5's empirical-on-the-convention prior-art, two independently-developed open-source projects exhibit axiomatic convergence with the Substrate Thesis at the personal-AI-memory-infrastructure layer:

- **`MemPalace/mempalace` (49.6k★ as of 2026-04-25; up from 45.8k 11 days prior)** — Python verbatim-memory project with Wings → Rooms → Drawers Zettelkasten-inspired taxonomy. **Six of seven non-negotiable principles** (verbatim storage / append-only ingestion / entity-first / local-first-zero-API / privacy-by-architecture / background-operations) **map directly to the principles in this author's stack's operating-instructions and memory layer.** Founding need (per maintainer's MISSION.md): "AI agent waking blank between sessions" — same continuity-failure-mode the Substrate Thesis hexad addresses manually. Full case study at `docs/prior_art_survey.md` Category 5.1. **Strongest-available existence proof for the cross-practitioner SRD recurrence claim** at the tool/infrastructure scale.
- **`doobidoo/mcp-memory-service` (1.7k★ steady-state)** — Python production-grade structured memory with knowledge-graph layer (typed asymmetric edges: causes / fixes / supports / follows; symmetric: related / contradicts). Apache 2.0; v10.40.3 as of 2026-04-24. **Most-direct cross-practitioner rule transfer documentable in this author's stack:** the operating-instructions Triple-Layer Test Database Safety rule was inherited DIRECTLY from doobidoo's Feb 8 2026 incident response (8,663 production memories destroyed by test-mode-DB-cleanup-against-prod-paths). This is direct cross-practitioner operational-discipline rule transfer with documented chronology — stronger than convention-adoption alone. Full case study at `docs/prior_art_survey.md` Category 5.2.

These two projects strengthen Case Study C (cross-practitioner convergence) substantially: alongside Daniel Miessler's Substrate framework (Category 0 vocabulary-collision documented in `docs/prior_art_survey.md` Category 0), the mempalace + doobidoo entries provide **two independent existence proofs of axiomatic (not just lexical) convergence**.

**Updated 2026-05-01 — Category 5 expansion to include need-singularity research-publication SCC + Anthropic Cookbooks pedagogical infrastructure:**

- **`need-singularity/papers` (Park Min Woo)** — DOI-anchored research-corpus with Zenodo+OSF dual-archive discipline, schema-validated manifest, hash-verifiable provenance. SCC axiom instantiated at the research-publication-layer: name-stable IDs (P-001, PA-01-... etc.), versioned reference structure, durable-cognitive-container at corpus scale. The need-singularity org has five Cat-5 entries (`prior_art_survey.md §5.4-5.8`) covering nexus, papers, n6-architecture, anima, and hexa-lang — five distinct components within one research stack each independently instantiating one or more axioms.
- **`anthropics/claude-cookbooks` (Anthropic engineering team)** — 76-notebook pedagogical infrastructure with multi-axiom convergence: FKS via helper-modules + nested CLAUDE.md per subdirectory (operating-instructions inheritance pattern); SCC via registry.yaml schema-validated catalog + naming conventions + pre-commit validation; SRD via uniform notebook structural shape across all 76 entries. Production-deployed as Anthropic's official developer-education vehicle. Full case study at `prior_art_survey.md §5.9`.

Case Study C's N is now N=6+ confirmed instances spanning individual researchers (mempalace, doobidoo, Park Min Woo's need-singularity stack), distributed open-source community work (the same projects via their contributors), and **Anthropic's own pedagogical infrastructure** as an independent practitioner-organization. The N=2 limitation acknowledged in the original outline is more than addressed; the prevalence study (§7.2 item 1) remains the path to formal-N quantification but qualitative-evidence is now substantial. Additionally, ten arxiv-indexed academic papers (April-May 2026 literature comb) provide candidate-tier convergence anchors pending per-paper code-level audit; the seven that passed WebFetch verification are catalogued at `bibliography.md §A.7` and `prior_art_survey.md §5.10`.

**§2.7 Parallel engineering discovery — whole-ecosystem axiom convergence (Category 6 prior-art; new section added 2026-04-26).** Distinct from §2.5's empirical-on-the-convention prior-art and §2.6's single-axiom convergence at the tool/infrastructure scale, one independently-developed practitioner ecosystem exhibits **whole-ecosystem axiomatic convergence** — multiple distinct components, each instantiating the same architectural patterns, built without articulating the meta-framework:

**Daniel Miessler's six-component personal-OS ecosystem:** SecLists (70.5k★ since 2012, security wordlist library demonstrating community-resource methodology) → fabric (41.1k★ since Jan 2024, AI prompt augmentation framework) → Substrate (800★ since July 2024, public collaborative knowledge platform) → TELOS (1.3k★ since Oct 2024, "Deep Context" 10-file framework) → PAI (Personal AI Infrastructure, 11.8k★ since Sept 2025, full personal AI operating system) → TheAlgorithm (107★ since Jan 2026, universal problem-solving algorithm grounded in Deutsch's epistemology) → Ladder (203★ since Mar 2026, autonomous optimization loop). Plus Unsupervised Learning newsletter (110k+ subscribers, 3,057 essays over 29.5 years).

**Triple-instantiation of the SCC pattern in Miessler's work** is the strongest single piece of empirical evidence in this prior-art survey: Fabric Patterns (named composable system-prompt files), PAI Skills (CODE > CLI > PROMPT hierarchy in upgrade-safe `USER/` directory), and TELOS document files (10 named bounded categorical containers) are three independent re-discoveries of the same architectural insight in three different problem domains, without Miessler naming any of them as instances of a single underlying pattern. This converges on the SCC axiom from three independent paths.

**14-of-16 PAI Principles map directly to Substrate Thesis axioms:** Miessler's Principle #4 "Scaffolding > Model selection" is the central architecture-over-content claim; Principle #11 "Goal > Code > CLI > Prompts > Agents" is a five-level recursive decomposition of execution abstraction directly homologous to FKS L0-L5; Principle #5 "Deterministic Infrastructure" is SCC discipline articulated; Principle #15 "Science as Meta-Loop" maps to W/M/Q/A audit cadence. Of 16 principles, 14 map cleanly to specific Substrate Thesis axioms or operational disciplines documented in this paper's first author's stack.

**Theoretical grounding:** Miessler's TheAlgorithm and his April 2026 essay "A Conversation With Claude on Deutsch, Knowledge, and the PAI Algorithm" ground the framework in David Deutsch's *Beginning of Infinity* (2011) epistemology — specifically the "hard-to-vary explanation" criterion. This provides a natural theoretical scaffolding for the Substrate Thesis bibliography: Deutsch's criterion is a respected formal claim about what distinguishes structural from accidental claims.

**Critical positioning for this paper:** PAI's first commit (Sept 8, 2025) predates this paper's first author's Substrate Thesis articulation (2026-02-16) by approximately five months. This is publication-strategically advantageous, not problematic — Miessler's contribution is empirical-architectural (specific working systems), this paper's contribution is theoretical-structural (the framework that explains why Miessler's pattern recurs). The two contributions are complementary at different levels of abstraction. The right framing: *"Miessler is a practitioner who built the thing without articulating the theory; this paper provides the theory that explains what he built."*

**Critical divergence between Miessler and the Substrate Thesis:** Miessler's framework is **teleological** — organized around a destination (the DA endpoint, human flourishing, "Euphoric Surprise"). This paper's framework is **structural** — organized around identifying what is necessarily true about the architecture, regardless of destination. Miessler is an engineer building toward a goal; this paper is a theoretical articulation of constraints that hold regardless of goal. The two layers are complementary; this paper's structural layer sits one level below Miessler's teleological layer. Full case study at `docs/prior_art_survey.md` Category 6 §6.1.

**Updated 2026-05-01 — Category 6 expansion to include need-singularity org + Anthropic Skills:**

Two additional whole-ecosystem axiom-convergence cases supplement the Miessler primary case:

- **`need-singularity` org as a whole** — 14+ active repos with multi-axiom convergence: FKS in nexus's OUROBOROS cycle, SCC across papers + hash-chained laws, SRD in three-loop nexus + cross-domain n6-architecture + cross-substrate anima. Author Park Min Woo. Differentiation from Miessler: vocabulary grounded in number-theory-as-meta-substrate; load-bearing application is autonomous-discovery + consciousness research; per-repo adoption tier varies (nexus + papers + n6-architecture are sound for technical citation + adoption; anima + hexa-lang are case-study / metaphor-only). Full case study at `prior_art_survey.md §6.2`.

- **`anthropics/skills` (Anthropic engineering team)** — 17 production skills + template + spec + plugin marketplace + Claude Code/Claude.ai/API integration. All three axioms instantiated with canonical strength: FKS via layered SKILL.md → scripts → references → agents → assets architecture; SCC via name-stable frontmatter and plugin-marketplace versioning; SRD via `skill-creator` as canonical meta-recursive skill-for-creating-skills signature plus identical structural shape across all 17 skills regardless of complexity. Production-deployed at scale through claude.ai + Claude Code + API. **The most-credentialed possible convergence anchor:** Anthropic itself — the AI lab building the foundational AI — independently converges on the same architecture this paper's framework predicts. Full case study at `prior_art_survey.md §6.3`.

Combined with Miessler's primary case, the Cat-6 evidence base is now N=3 whole-ecosystem convergences across distinct practitioner-classes: individual practitioner-thinker (Miessler), independent research organization (need-singularity), and AI lab building foundational AI (Anthropic). The recurrence of FKS+SCC+SRD axioms across these three distinct classes — none of whom share vocabulary or community, all of whom independently solve the same problem — is the paper's strongest empirical claim that the patterns are constraint-imposed by the problem of building durable AI-augmented infrastructure rather than diffused through any community lineage.

**Gap statement (revised 2026-05-01):** Existing literature addresses (a) individual pieces of personal cognitive infrastructure (PKM, personal informatics) or analogous patterns in software systems (layered architecture, immutable data, design patterns), (b) empirical prevalence + outcomes of operating-instructions-at-repository-root files specifically (Gloaguen et al. 2026; Konrad et al. 2026; He et al. CMU MSR 2026), (c) single-axiom convergence at the tool/infrastructure scale (mempalace, doobidoo, need-singularity research-corpus, Anthropic Cookbooks - §2.6), and (d) whole-ecosystem axiom convergence in working multi-component implementations at scale across distinct practitioner-classes (Miessler stack, need-singularity org, Anthropic Skills - §2.7). What no prior work provides is the **structural framework explaining the recurrence** + the **3-pattern integration** showing operating-instructions files as one instance of a broader SRD pattern that also encompasses reinvigoration templates, audit cadences, and cross-domain architectures. This integrated framework is the paper's contribution. The convergence evidence base — N=6+ confirmed across two Cat-6 ecosystems and four Cat-5 single-axiom convergences with N=10 candidate academic-paper anchors pending per-paper validation — substantiates the structural-not-stylistic claim with unusual empirical strength for a personal-informatics-adjacent contribution.

---

### Section 3 — The Three Patterns (2-2.5 pages)

Compress Substack Essays 2-4 into formal pattern definitions. Each pattern: 5-7 paragraphs.

**§3.1 Foundational Knowledge Stack (FKS).** Five properties: explicit dependency order; no cross-layer reaching; stable interfaces; independent evolution within a layer; per-layer correctness checkable. The pattern produces three measurable benefits: bounded blast radius from changes; modular debugging; independent evolution. Compare to Buschmann's Layered Architecture with reference to personal-cognitive-infrastructure adaptation.

**§3.2 Stable Cognitive Container (SCC).** Five properties: frozen between updates; delta-or-regeneration update mode; versioned; independently consumable; per-purpose scoped. The pattern produces three measurable benefits: bounded cognitive load from references; citable, auditable decisions; stable foundation for FKS layering. Compare to immutable data structures in functional programming + content-addressed storage in Git, with reference to personal-cognitive-infrastructure adaptation.

**§3.3 Stable Recursive Decomposition (SRD).** Five properties: same structural shape at multiple scales; same correctness guarantees; same failure modes; per-scale autonomous operation; cross-scale informativeness. The pattern produces three measurable benefits: cross-scale prediction; pattern-recognition compounding; domain portability. Compare to fractal / scale-invariant systems + design patterns + functor pattern from category theory, with reference to personal-cognitive-infrastructure adaptation.

**§3.4 Pattern interaction.** Brief subsection (4-5 paragraphs) summarizing how the three patterns reinforce each other. Forward-reference to Section 4 case study for detailed demonstration.

**§3.5 Formalization + Health Indices (~0.75 page; new in v2.1-aware outline).** Each pattern admits a compact formal statement — FKS as a strict layer assignment on a dependency graph with blast-radius bounded by layer-fanout; SCC as a version graph with delta + regeneration transitions and quantifiable freshness gap; SRD as a structure-preserving map satisfying correctness-and-failure-mode preservation across scales. For each pattern, the companion theory documents (v2.1 expanded 2026-04-24) define compliance metrics that compose into a proposed Health Index: FKS Health (layer-span score × blast-radius compliance × interface stability × modularity fraction); SCC Health (version coverage × freshness compliance × delta discipline × citation specificity); SRD Health (scale coverage × structural fidelity × failure-mode transfer rate × compound recognition value). The paper presents the formalization for clarity but frames Health Indices as *proposed, not validated* — the framework's core empirical support is the case studies, not quantitative scoring across practitioners. Cross-practitioner validation is identified in §7.2 as future work.

---

### Section 4 — Case Studies (3-3.5 pages)

Three case studies presented in compressed form. Each: ~1 page.

**§4.1 Case study A: Reinvigoration template across artifact types (drawn from Substack Essay 5 + case_studies/01).** A descriptive insights memo undergoes v1 → v2 reinvigoration four hours of practitioner work. The same five-element template subsequently applies identically to seven additional artifacts (memos, frameworks, decks, code, letters) over six weeks. Demonstrates SRD at the artifact-type scale + FKS-enabled access to corrected inputs + SCC-enabled citable changes operating together.

**§4.2 Case study B: Audit cadence framework (drawn from case_studies/03).** A weekly/monthly/quarterly/annual audit cadence is deliberately designed to exhibit SRD. Each scale's instance reads only its immediate prior layer's outputs and follows the same five structural elements. Demonstrates the proof-of-design SRD complement to case study A's proof-of-discovery SRD. Includes anti-pattern observation: cross-scale leak attempted once, corrected, discipline reasserted.

**§4.3 Case study C: Cross-practitioner convergence (drawn from case_studies/07; expanded 2026-04-26 with Category 5 + Category 6 evidence).** The convention of placing operating-instructions files at repository roots (CLAUDE.md / AGENTS.md / similar) recurs independently across multiple practitioners' substrates. Updated through April 2026, the case study now spans four distinct levels of cross-practitioner convergence:

- **Convention level (Category 0):** Daniel Miessler's `Substrate` repo uses CLAUDE.md at root; same convention as this paper's first author. Vocabulary-collision concern documented separately.
- **Axiom level (Category 5.1):** `MemPalace/mempalace` (49.6k★) exhibits 6-of-7 axiom mirroring with this paper's first author's CLAUDE.md memory/protocol layer despite different problem origin and vocabulary — strongest single-axiom convergence existence proof at the tool scale.
- **Operational-discipline level (Category 5.2):** `doobidoo/mcp-memory-service` provides documented direct cross-practitioner rule transfer — the Triple-Layer Test Database Safety rule was inherited DIRECTLY from doobidoo's published Feb 8 2026 incident response (8,663 production memories destroyed) into the first author's CLAUDE.md §2. Most-direct documentable cross-practitioner rule transfer in the corpus.
- **Whole-ecosystem level (Category 6.1; new 2026-04-26):** Daniel Miessler's six-component personal-OS stack (fabric 41.1k★ / PAI 11.8k★ / TELOS 1.3k★ / Substrate 800★ / TheAlgorithm / Ladder, plus Unsupervised Learning newsletter 110k+ subscribers) exhibits **triple instantiation of the SCC pattern** (Fabric Patterns + PAI Skills + TELOS files) and **14-of-16 PAI principles mapping** directly to Substrate Thesis axioms. Miessler is a practitioner who built the thing without articulating the theory; this paper provides the theory that explains what he built. Strongest available whole-ecosystem cross-practitioner convergence evidence; Deutsch-grounded epistemology provides additional theoretical scaffolding.

Demonstrates that SRD pattern recurrence extends beyond single-practitioner work to cross-practitioner emergence at four distinct levels: convention, axiom, operational-discipline, and whole-ecosystem. **N is now N=4+ confirmed instances** of independent axiom convergence in adjacent problem domains; quality of evidence ranges from vocabulary-only (Miessler/Substrate) through operational-rule-transfer (doobidoo) to whole-ecosystem axiom mapping (Miessler stack at large). The N=2 limitation in the original case study is fully addressed at the qualitative level; the prevalence study (§7.2 item 1) remains the path to formal-N quantification at scale. The paper's claim that the Substrate Thesis predicts cross-practitioner convergence is now empirically testable against four distinct convergence-quality levels.

---

### Section 5 — Anti-Patterns and Failure Modes (1-1.5 pages)

Compress the v2.1 expanded anti-pattern catalog (8 per pattern, 24 total) into a page-length structured catalog. The paper includes the 2-3 most operationally-important anti-patterns per pattern; the theory documents carry the full 8-per-pattern catalog with mitigations for readers wanting depth.

**§5.1 FKS failure modes.** Operational selection (from 8 total in theory/FKS v2.1): cross-layer leaks (downstream reaches for upstream implementation rather than contract); missing layer separation (concerns at different change-rates collapsed into one layer); versioning mismatch (interface contract changes without coordinated updates). Additional anti-patterns (lateral leak, shortcut reach, temporal drift, collapsed layering under time pressure, implicit dependencies) cataloged in companion theory document.

**§5.2 SCC failure modes.** Operational selection (from 8 total in theory/SCC v2.1): stale containers (regeneration cadence breaks; downstream acts on stale state); container fragmentation (authoritative version unclear across multiple files); missing deltas (incremental changes not captured between regenerations). Additional anti-patterns (premature regeneration, freshness-gap blindness, container bleed, unversioned reach-through, ghost delta) cataloged in companion theory document.

**Contemporary exemplar (added 2026-04-27):** the IT 7021C Spring 2026 anomaly-detection paper bug — a Boolean K-Means anomaly column compared to integer -1 in consensus-intersection logic, producing zero overlap values where actual values are 22/12/11 — instantiates the *missing deltas* failure mode at the code-cell scale. The team's notebook contained a corrective cell (cell 32) that converted the Boolean to -1/+1 integer, but a typo in the column name (`kmenans_anomaly`) prevented the fix from being referenced downstream. The corrective delta existed but was never wired in; the original broken comparison persisted and propagated into the published Table II + the §V.A interpretation built upon it. Independent reproducibility scaffold + bug diagnosis at `github.com/barelyaninconvenience/it7021-anomaly-detection-replication`. The pattern — "fix authored, typo prevents wiring, original failure preserved" — is recognizable and distinct from the better-known stale-container anti-pattern; flagged as candidate for inclusion in the prevalence study (§7.2 item 1) once the SCC anti-pattern catalog is extended for empirical sampling.

**§5.3 SRD failure modes.** Operational selection (from 8 total in theory/SRD v2.1): pseudo-recursion (pattern looks the same but correctness guarantees differ); forced uniformity (pattern applied where it doesn't fit); cross-scale leak (per-scale autonomy violated by coordination shortcuts). Additional anti-patterns (hidden state, over-abstraction, premature generalization, failure-mode non-preservation, taxonomic drift) cataloged in companion theory document. Theory document also includes four anti-case studies of failed SRD portability attempts — pipeline over-abstraction, reinvigoration-template-on-transcripts, audit-cadence-on-creative-writing, crawler-on-streaming-data — with what each teaches about SRD portability prerequisites.

**§5.4 Diagnostic value.** Brief discussion: the framework's contribution is diagnostic vocabulary as much as structural prescription. Naming the failure modes makes them recognizable + repairable; without the vocabulary, failures feel like generalized bad luck. This subsection explicitly frames the paper's contribution as enabling recognition rather than guaranteeing prevention.

---

### Section 6 — Discussion + Implications (1-1.5 pages)

**§6.1 Implications for HCI design.** The framework predicts that tools supporting personal cognitive infrastructure should make FKS dependencies + SCC versioning + SRD recurrence first-class. Specific design implications: tools that surface layer boundaries explicitly; tools that version artifacts at the file level (not just behind-the-scenes via git); tools that recognize pattern recurrence and offer template application across artifact types.

**§6.2 Implications for AI-augmented knowledge work.** Operating-instructions documents (CLAUDE.md / AGENTS.md / similar) are the foundational SCC of AI-augmented personal cognitive infrastructure. The convergent emergence of this convention across independent practitioners (case study C) suggests the convention is structural rather than stylistic. Tooling for AI assistants should recognize this and support it as a primitive rather than treating it as user-defined custom configuration.

**§6.3 Implications for personal informatics research.** The framework offers the personal informatics literature a structural grammar for distinguishing personal-informatics-systems-that-compound from those-that-decay. Future personal informatics research could test framework predictions empirically (do systems exhibiting FKS / SCC / SRD discipline outperform those lacking the patterns?).

**§6.4 Implications for practitioner education.** Substack series Essay 7 articulates a Minimum Viable Substrate buildable in a weekend. The framework as an educational vocabulary may lower the bar for practitioners to build cognitive infrastructure that compounds; future work could study adoption + outcomes empirically.

---

### Section 7 — Limitations and Future Work (0.5-1 page)

**§7.1 Limitations.** Six months of single-practitioner observation is preliminary; longitudinal studies are needed. Selection bias (the framework's author is the framework's chief beneficiary). N=2 cross-practitioner evidence is preliminary; prevalence study is needed. The framework's domain is specifically AI-augmented personal cognitive infrastructure; generalizability to other contexts (institutional, real-time, purely creative) is bounded.

**§7.2 Future work.** Seven concrete directions:
1. Cross-practitioner prevalence study of operating-instructions convention (formalizing case study C's TODO)
2. Longitudinal study of practitioners adopting MVS framework (do measurable outcomes follow?)
3. Empirical study of pattern interaction quantitatively (can the multiplicative cost claim from Substack Essay 5 be measured?)
4. Tooling implications: prototype tools that surface FKS / SCC / SRD as first-class objects; including static analyzers that compute the proposed Health Indices (§3.5) from a personal-OS corpus's dependency graph + version history + citation network
5. Cross-domain extension: do the patterns appear in collective cognitive infrastructure (teams, organizations, fields)?
6. Adversarial study: failure modes in adversarial contexts (substrates under attack; manipulated artifacts; etc.)
7. Empirical validation of the Health Indices proposed in v2.1 theory documents — correlating Health scores against self-reported substrate outcomes (maintenance cost, perceived reliability, compounding perception) across a practitioner cohort. Would convert the proposed metrics from scaffold to validated instrument.
8. **Anti-pattern prevalence study at the code-cell scale (added 2026-04-27).** The IT 7021C dtype-comparison bug exemplar (§5.2) suggests SCC failure modes are observable in published academic notebooks — typically Jupyter or Colab — at sufficient scale to enable empirical sampling. A study could static-analyze a corpus of published academic data-science notebooks (e.g., from supplementary materials of recent IEEE/ACM proceedings) for the specific anti-pattern signatures (Boolean-vs-int comparison, typo'd column references that break corrective wiring, untested cell-execution-order dependencies) and report base-rate prevalence. Would establish whether the IT 7021C bug is one-off accident or recurring pattern at field scale.

---

### Section 8 — Conclusion (0.25-0.5 page)

Brief restatement of contribution. Three sentences:
1. Three structural patterns recur in well-formed personal cognitive infrastructure for AI-augmented knowledge work.
2. The patterns are not novel individually but their integration is, and their explicit naming enables practitioners to build deliberately rather than accidentally.
3. The framework offers diagnostic vocabulary for recognizing failure modes + structural prescription for building substrates that compound rather than decay.

Closing call: the framework is articulated; the empirical evidence is in the companion repository (URL); the practical guidance for adoption is in the Substack series (URL); future work is the cross-practitioner prevalence study + longitudinal adoption study + tooling implications. Counter-examples and refinements welcome.

---

## §4 — References (initial seed; needs formal expansion)

The companion `docs/prior_art_survey.md` enumerates ~30 references. The paper's bibliography would draw from that. Initial seed:

**PKM and personal informatics:**
- Forte, T. (2022). *Building a Second Brain*. Atria Books.
- Allen, D. (2001/2015). *Getting Things Done*. Penguin.
- Matuschak, A. (2019). *Evergreen Notes*. https://notes.andymatuschak.org/
- Schmidt, J. F. K. (2018). Niklas Luhmann's card index: The fabrication of serendipity.
- Li, I., Dey, A., & Forlizzi, J. (2010). A stage-based model of personal informatics systems. *CHI '10*.

**System-design patterns:**
- Buschmann, F., Meunier, R., Rohnert, H., et al. (1996). *Pattern-Oriented Software Architecture*. Wiley.
- Gamma, E., Helm, R., Johnson, R., Vlissides, J. (1994). *Design Patterns*. Addison-Wesley.
- Newman, S. (2015). *Building Microservices*. O'Reilly.
- Evans, E. (2003). *Domain-Driven Design*. Addison-Wesley.
- Mandelbrot, B. (1982). *The Fractal Geometry of Nature*. W.H. Freeman.

**Distributed cognition + external cognition:**
- Hutchins, E. (1995). *Cognition in the Wild*. MIT Press.
- Norman, D. (1993). *Things That Make Us Smart*. Addison-Wesley.

**AI-augmented knowledge work (emerging):**
- Dell'Acqua, F., et al. (2024). Navigating the jagged technological frontier of AI capabilities. *Working paper.*
- Liang, W., et al. (2024). Mapping the increasing use of LLMs in scientific papers.

**Convergent operating-instructions convention (Category 0 vocabulary collision):**
- Anthropic Claude Code documentation (2025-2026)
- Miessler, D. (2026). *Substrate*. github.com/danielmiessler/Substrate

**Independent-practitioner axiom convergence (Category 5 — added 2026-04-25):**
- mempalace project (Milla Jovovich handle). 2026. *MemPalace: Local-first AI memory.* github.com/MemPalace/mempalace
- doobidoo. 2026. *MCP Memory Service: Persistent shared memory for AI agent pipelines.* github.com/doobidoo/mcp-memory-service
- Danilchenko, M. 2026. *MemPalace Review: The AI Memory System That Broke GitHub in a Weekend.* danilchenko.dev. (Third-party credibility audit cited in mempalace Category 5.1 entry.)

**Cluster-4 batch academic prior-art (added 2026-04-25 batch differentiation memos):**
- Konrad, P. M., Adam, T. L., Terrenzi, R., & Ayvaz, S. 2026. *Architecture Without Architects: How AI Coding Agents Shape Software Architecture.* arXiv 2604.04990.
- Robbes, R., Matricon, T., Degueule, T., Hora, A., & Zacchiroli, S. 2026. *Agentic Much? Adoption of Coding Agents on GitHub.* arXiv 2601.18341.
- Galster, M., Mohsenimofidi, S., Lulla, J. L., Abubakar, M. A., Treude, C., & Baltes, S. 2026. *Configuring Agentic AI Coding Tools: An Exploratory Study.* arXiv 2602.14690 (v3 Apr 9 2026).
- Bakal, G. 2026. *Knowledge Activation: AI Skills as the Institutional Knowledge Primitive for Agentic Software Development.* arXiv 2603.14805.
- Zhang, Y., Pan, Z., Yusuf, I. N. B., Ruan, H., Shariffdeen, R., & Roychoudhury, A. 2026. *Code Review Agent Benchmark.* arXiv 2603.23448 (v3 Apr 7 2026).

---

## §5 — Pre-submission checklist

Before submitting to a venue:

- [x] ~~Substantively elaborate theory documents in companion repository~~ **DONE 2026-04-24: theory trio v2 → v2.1 (FKS 549 / SCC 501 / SRD 601 lines; formal diagnostic + 8 anti-patterns + practitioner-framework comparison + Health Indices each)**
- [ ] Run formal prevalence study for case study C (cross-practitioner convergence) — converts N=2 to documented N
- [ ] Add formal experimental validation of at least one framework prediction (e.g., reinvigoration cycle time decreases with substrate maturity; can be demonstrated quantitatively across the seven documented v1 → v2 instances)
- [ ] Pre-readers identified — at least 2 HCI researchers + 2 personal informatics researchers + 2 senior practitioners
- [ ] IRB consideration: the personal-substrate observations use the author as the subject; minimal IRB requirements but worth verifying institutional policy
- [ ] Companion repository's commit history is clean and citable for paper's empirical-evidence references
- [ ] Anonymization review: any client / employer / collaborator identifiers in the case studies are scrubbed appropriately for anonymous review
- [ ] Diagrams authored (§3 dependency-graph figure; §3 version-graph figure; §3.5 Health Index composition figure; §4 case-study timeline figure; §5 anti-pattern taxonomy figure) — typical HCI paper has 3-5 figures

---

## §6 — Adaptation notes for non-CHI venues

### Software Engineering / Personal Informatics venues
- Increase Section 3 (formal pattern definitions) to 3-4 pages with more explicit comparison to system-design pattern literature
- Decrease Section 4 (case studies) to 2-2.5 pages with more emphasis on the architectural patterns
- Add a §3.5 explicit pattern-language framing (Alexander; Gamma et al.)

### Design Research / Autoethnography venues
- Expand Section 1 (introduction) to 2 pages with deeper practitioner-positionality treatment
- Frame case studies as autoethnographic accounts rather than empirical case studies
- Add explicit reflexivity section discussing the practitioner-theorist position
- Increase paper length to 12-15 pages reflecting the genre conventions

### Personal Informatics workshop at Ubicomp (early-feedback target)
- Compress to 4-6 page workshop position paper
- Lead with case study C (cross-practitioner convergence) as the most differentiated empirical contribution
- Use as feedback-gathering venue to inform main CHI submission

---

## §7 — Timeline (assuming CHI 2027 main submission)

| Date | Action |
|---|---|
| 2026-05-01 | Venue commitment finalized (CHI 2027 main + Ubicomp 2026 PI workshop) |
| 2026-06-01 | Substantive theory document elaboration complete |
| 2026-07-01 | Cross-practitioner prevalence study complete (case study C upgrade) |
| 2026-08-01 | First full draft (matched to Ubicomp 2026 workshop deadline) |
| 2026-09-01 | Pre-reader feedback complete; revisions in flight |
| 2026-09-XX | CHI 2027 submission deadline (TBD; typically mid-September) |
| 2026-10-01 | Ubicomp 2026 PI workshop presentation (if accepted) |
| 2026-12-XX | CHI 2027 notifications |
| 2027-04-XX | CHI 2027 conference (if accepted) |

Parallel to the Substack series cadence:
- Substack Essays 1-7 publish bi-weekly Aug 2026 through Nov 2026
- Academic paper submission Sep 2026 (after Substack Essays 1-2 published; before Substack Essays 5-7 published)
- The Substack series and academic paper compound each other: Substack establishes practitioner audience; paper establishes academic legitimacy; both reinforce Substrate Thesis Companion repository's credibility

---

## §8 — What this outline does NOT yet contain

For honest scope:

- **Specific quantitative claims with empirical numbers.** The framework predicts compounding payoffs (e.g., reinvigoration cycle time decreases with substrate maturity); quantification requires structured measurement that hasn't been instrumented yet. The v2.1 theory documents propose Health Indices as quantification scaffolding, but empirical validation of those indices across a practitioner cohort is future work (§7.2 item 7).
- **Cross-practitioner prevalence data** for case study C (convergent CLAUDE.md). Currently N=2 (this author + Miessler). The paper would be substantially strengthened by formal prevalence study via GitHub search or equivalent; §7.2 item 1 identifies this as future work, but it could also be in-scope if the study is completed before submission.
- **Specific tool prototypes** for the §6.1 design implications. Prototype tools would substantially strengthen the paper but require additional development time. The §3.5 Health Index formulations are tooling-ready (well-defined metrics computable from standard personal-OS artifacts) but no implementation exists yet.
- **Author bio and acknowledgments.** Standard academic-paper boilerplate added at submission time.
- **Diagrams.** A typical HCI paper has 3-5 figures (FKS dependency graph; SCC version graph with deltas + regenerations; SRD structure-preserving-map diagram; Health Index composition; case-study timeline). Diagrams designed at draft stage.
- **Anonymization for double-blind review.** Currently mentions the first author's identity throughout; anonymization is a final-pass edit before submission.

**Closed gaps from prior version of this outline (now addressed in theory v2.1):**

- ~~Substantive theory-document elaboration~~ → FKS 307→549 lines (1.79x); SCC 279→501 (1.80x); SRD 357→601 (1.68x); total 943→1651 (1.75x) on 2026-04-24
- ~~Formal notation for each pattern~~ → graph-based formalization for each (FKS layer assignment + edge constraints; SCC version graph + freshness gap; SRD structure-preserving maps + domain portability test)
- ~~Diagnostic tests~~ → 5-step diagnostic per pattern, implementable against real personal-OS corpora
- ~~Comparison with established frameworks~~ → Forte BASB, Matuschak Evergreen, Allen GTD, Luhmann Zettelkasten, Miessler Substrate explicitly assessed in theory docs with summary tables
- ~~Extended anti-pattern catalogs~~ → 8 anti-patterns per pattern (24 total); SRD additionally includes 4 anti-case studies of failed portability attempts

---

## §9 — Alternative formulation (if HCI/CSCW path is wrong fit)

If venue commitment lands on Software Engineering or Design Research instead of HCI/CSCW, the paper restructures substantially. This outline assumes HCI/CSCW because it's the highest-impact realistic target and the framework's empirical-grounding-in-practitioner-experience fits HCI's epistemic conventions well.

If venue is Software Engineering: lead with Section 3 (formal patterns) as the main contribution; relegate practitioner narrative to a "motivation" section. If venue is Design Research: lead with Section 1 (recognition + autoethnography) as the main contribution; relegate formal patterns to "framework articulation" section.

The companion repository's deeper material (theory documents + case studies + prior art survey) supports any of the three framings without restructuring.

---

*Academic paper outline first draft 2026-04-24. Parallel track to the Substack series under the publication strategy. Subject to substantial revision once venue is committed (deadline 2026-05-15). Companion to Substack Essays 1-7 (drafted in `docs/essays/`) + theory trio v2 (`theory/`) + case studies 01-07 (`case_studies/`).*
