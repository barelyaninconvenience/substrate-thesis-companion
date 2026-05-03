# Bibliography — Substrate Thesis Companion
## IEEE-style references, consolidated 2026-04-25

**Status:** First unified artifact. Replaces scattered citations across `prior_art_survey.md` (Citations section) + `academic_paper_outline.md` §4 References + each `differentiation_vs_*_20260425.md` memo footnote + `Mempalace_NeedSingularity_CommunityContext_20260425.md` §6 + `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md` inline URLs. **Canonical source for all citations going forward.**

**Style:** IEEE author-list format, "Title," *Venue*, Year. Cross-references show every artifact citing each entry.

**Verified:** All star counts + version numbers + release dates verified via direct GitHub WebFetch on 2026-04-25 (after audit-finding flagged the OSSInsight-trending-vs-absolute confusion). Star counts represent absolute totals as of access date, not monthly deltas.

**Access date convention:** [Accessed: 2026-04-25] applies to all URLs unless otherwise noted.

---

## §A — Academic peer-reviewed / preprint

### A.1 Operating-instructions-at-repository-root convention (Category 4)

[A1] T. Gloaguen, N. Mündler, M. Müller, V. Raychev, and M. Vechev, "Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents?," arXiv:2602.11988 [cs.SE], Feb. 12 2026. [Online]. Available: https://arxiv.org/abs/2602.11988
- *Cited in:* `differentiation_vs_gloaguen_2602_11988_20260425.md` (full memo); `prior_art_survey.md` §2.5 Category 4 (line 385); `academic_paper_outline.md` §2.5 + §4 References
- *Disambiguation:* Previously cited as "Liu et al." in this corpus; corrected 2026-04-25 via arXiv WebFetch verification

[A2] R. Robbes, T. Matricon, T. Degueule, A. Hora, and S. Zacchiroli, "Agentic Much? Adoption of Coding Agents on GitHub," arXiv:2601.18341 [cs.SE], Jan. 26 2026 (v2 Apr. 8 2026). [Online]. Available: https://arxiv.org/abs/2601.18341
- *Cited in:* `differentiation_vs_konrad_2601_18341_20260425.md` (filename retained for git-history continuity, but title-author cross-reference must be updated to Robbes et al.); `prior_art_survey.md` §2.5 (line 387)
- *Cite as:* **Robbes et al. (2026)**
- *Audit catch 2026-04-30:* prior bibliography draft incorrectly attributed authorship to "P. M. Konrad et al." — that author list belongs to [A3], not [A2]. arXiv direct WebFetch confirmed the actual authors are Robbes / Matricon / Degueule / Hora / Zacchiroli. Differentiation memo filename retained for git-history; memo content + cross-references in `prior_art_survey.md` and `academic_paper_outline.md` must be updated to reflect the correct author attribution.

[A3] P. M. Konrad, T. L. Adam, R. Terrenzi, and S. Ayvaz, "Architecture Without Architects: How AI Coding Agents Shape Software Architecture," arXiv:2604.04990 [cs.SE], Apr. 5 2026. [Online]. Available: https://arxiv.org/abs/2604.04990
- *Cited in:* `differentiation_vs_konrad_arch_2604_04990_20260425.md`; `prior_art_survey.md` §2.5; `academic_paper_outline.md` §2.5
- *Cite as:* **Konrad et al. (2026)**. Position paper introducing "vibe architecting." (Disambiguation handle "(2026b)" dropped 2026-04-30 after [A2] author-list correction; no longer same-first-author conflict.)

[A4] M. Galster, S. Mohsenimofidi, J. L. Lulla, M. A. Abubakar, C. Treude, and S. Baltes, "Configuring Agentic AI Coding Tools: An Exploratory Study," arXiv:2602.14690 [cs.SE], Feb. 16 2026 (v3 Apr. 9 2026). [Online]. Available: https://arxiv.org/abs/2602.14690
- *Cited in:* `differentiation_vs_galster_2602_14690_20260425.md`; `prior_art_survey.md` §2.5; `academic_paper_outline.md` §2.5
- *Note:* Filename uses "galster" but first-author surname requires arXiv re-verification (audit flagged potential anomaly with Mohsenimofidi)

[A5] G. Bakal, "Knowledge Activation: AI Skills as the Institutional Knowledge Primitive for Agentic Software Development," arXiv:2603.14805 [cs.SE], Mar. 16 2026. [Online]. Available: https://arxiv.org/abs/2603.14805
- *Cited in:* `differentiation_vs_bakal_2603_14805_20260425.md`; `prior_art_survey.md` §2.5; `academic_paper_outline.md` §2.5 + §2.6 (Category 5 framework-level candidate)

[A6] Y. Zhang, Z. Pan, I. N. B. Yusuf, H. Ruan, R. Shariffdeen, and A. Roychoudhury, "Code Review Agent Benchmark," arXiv:2603.23448 [cs.SE], Mar. 24 2026 (v3 Apr. 7 2026). [Online]. Available: https://arxiv.org/abs/2603.23448
- *Cited in:* `differentiation_vs_zhang_crab_2603_23448_20260425.md`; `prior_art_survey.md` §2.5
- *Classification:* Tangential; peripheral §1 Introduction citation only

[A7] H. He, C. Miller, S. Agarwal, C. Kästner, and B. Vasilescu, "Speed at the Cost of Quality: How Cursor AI Increases Short-Term Velocity and Long-Term Complexity in Open-Source Projects," in *Proc. 23rd Int. Conf. Mining Software Repositories (MSR '26)*, Rio de Janeiro, Brazil, Apr. 13-14 2026; arXiv mirror 2511.04427. [Online]. Available: https://arxiv.org/abs/2511.04427 ; https://cmustrudel.github.io/papers/msr2026he.pdf
- *Cited in:* `differentiation_vs_he_msr2026_20260425.md`; `prior_art_survey.md` §2.5
- *Critical:* Mediation finding empirically substantiates Substrate Thesis structural-pattern-violation-compounds claim
- *Audit refinement 2026-04-30:* prior framing "CMU MSR 2026" implied CMU was the venue. MSR 2026 is Rio de Janeiro; the CMU connection is via the authors (Kästner, Vasilescu, et al. are at CMU's STRUDEL group, hence the cmustrudel.github.io paper-mirror URL). First-author full name verified as Hao He.

[A8] M. Schreiber and P. Tippe, "Security Vulnerabilities in AI-Generated Code: A Large-Scale Analysis of Public GitHub Repositories," arXiv:2510.26103, Oct. 30 2025. [Online]. Available: https://arxiv.org/abs/2510.26103
- *Cited in:* `prior_art_survey.md` §2.5 (cited 3× — flagged for consolidation by audit)
- *Classification:* ADJACENT (security topic, not operating-instructions convention)
- *Audit catch 2026-04-30:* prior bibliography draft used incorrect first-name initials "J. Schreiber and N. Tippe"; arXiv direct WebFetch confirmed actual authors are Maximilian Schreiber and Pascal Tippe (M. and P. initials). Corrected.

### A.2 Personal informatics + HCI

[A9] I. Li, A. Dey, and J. Forlizzi, "A stage-based model of personal informatics systems," in *Proc. CHI 2010*, Atlanta, GA, USA, 2010.
- *Cited in:* `prior_art_survey.md` Category 3; `academic_paper_outline.md` §2.2 + §4

[A10] G. Wolf and K. Kelly, "The Quantified Self movement," *Wired Magazine*, 2007.
- *Cited in:* `prior_art_survey.md` Category 3; `academic_paper_outline.md` §2.2

### A.3 PKM frameworks (books)

[A11] T. Forte, *Building a Second Brain: A Proven Method to Organize Your Digital Life and Unlock Your Creative Potential*. New York, NY, USA: Atria Books, 2022.
- *Cited in:* `prior_art_survey.md` Category 1; `academic_paper_outline.md` §2.1 + §4
- *Differentiation focus:* CODE workflow + PARA organization

[A12] D. Allen, *Getting Things Done: The Art of Stress-Free Productivity*, rev. ed. New York, NY, USA: Penguin, 2015.
- *Cited in:* `prior_art_survey.md` Category 1; `academic_paper_outline.md` §2.1 + §4

[A13] A. Matuschak, "Evergreen Notes," 2019. [Online]. Available: https://notes.andymatuschak.org/
- *Cited in:* `prior_art_survey.md` Category 1; `academic_paper_outline.md` §2.1 + §4

[A14] J. F. K. Schmidt, "Niklas Luhmann's card index: The fabrication of serendipity," 2018.
- *Cited in:* `academic_paper_outline.md` §4 (Luhmann secondary-literature)

### A.4 System-design pattern canon

[A15] F. Buschmann, R. Meunier, H. Rohnert, P. Sommerlad, and M. Stal, *Pattern-Oriented Software Architecture: A System of Patterns* (POSA1). Chichester, UK: Wiley, 1996.
- *Cited in:* `prior_art_survey.md` Category 2; `academic_paper_outline.md` §2.3 + §3.1 (FKS predecessor)

[A16] E. Gamma, R. Helm, R. Johnson, and J. Vlissides, *Design Patterns: Elements of Reusable Object-Oriented Software*. Reading, MA, USA: Addison-Wesley, 1994.
- *Cited in:* `prior_art_survey.md` Category 2; `academic_paper_outline.md` §2.3 + §3.3 (SRD comparison)

[A17] S. Newman, *Building Microservices: Designing Fine-Grained Systems*. Sebastopol, CA, USA: O'Reilly, 2015.
- *Cited in:* `prior_art_survey.md` Category 2 (microservices as SRD instance)

[A18] E. Evans, *Domain-Driven Design: Tackling Complexity in the Heart of Software*. Reading, MA, USA: Addison-Wesley, 2003.
- *Cited in:* `prior_art_survey.md` Category 2

[A19] B. Mandelbrot, *The Fractal Geometry of Nature*. New York, NY, USA: W.H. Freeman, 1982.
- *Cited in:* `academic_paper_outline.md` §2.3 + §3.3 (fractal/SRD comparison)

[A20] C. Alexander, S. Ishikawa, and M. Silverstein, *A Pattern Language: Towns, Buildings, Construction*. New York, NY, USA: Oxford Univ. Press, 1977.
- *Cited in:* PKM literature survey scoping (deferred dedicated session); referenced as predecessor to Gamma et al. [A16]

### A.5 Distributed cognition + external cognition

[A21] E. Hutchins, *Cognition in the Wild*. Cambridge, MA, USA: MIT Press, 1995.
- *Cited in:* `prior_art_survey.md` Citations seed; `academic_paper_outline.md` §4

[A22] D. Norman, *Things That Make Us Smart: Defending Human Attributes in the Age of the Machine*. Reading, MA, USA: Addison-Wesley, 1993.
- *Cited in:* `prior_art_survey.md` Citations seed; `academic_paper_outline.md` §4

### A.6 AI-augmented knowledge work (emerging)

[A23] F. Dell'Acqua et al., "Navigating the jagged technological frontier: Field experimental evidence of the effects of AI on knowledge worker productivity and quality," Working paper, 2024.
- *Cited in:* `academic_paper_outline.md` §2.4 + §4

[A24] W. Liang et al., "Mapping the increasing use of LLMs in scientific papers," Working paper, 2024.
- *Cited in:* `academic_paper_outline.md` §2.4 + §4

### A.7 Personal AI memory + cognitive-architecture convergence anchors (Cat-5 academic-paper cluster — added 2026-05-01)

Verified through WebFetch verification cycle 2026-05-01 against an external literature-search haul. Each citation below was checked along four axes (paper-existence / architecture-claim accuracy / cited-references accuracy / quoted-material accuracy) before inclusion; entries with axis failures were demoted to §A.8 with explicit fabrication callouts (the Substrate Thesis project applies a search-result tier-verification discipline whereby tier-1+2 Exa output is reliable, tier-3+4 require WebFetch confirmation before propagation).

[A25] M. Roynard, "The Missing Knowledge Layer in Cognitive Architectures for AI Agents," arXiv:2604.11364, Apr. 13 2026. [Online]. Available: https://arxiv.org/abs/2604.11364
- *Affiliation:* LAAS-OASIS
- *Cited in:* `prior_art_survey.md` §5.10.1 Cat-5 cluster; `academic_paper_outline.md` §2.6
- *Substrate-relevance:* **Strongest external academic anchor for the Substrate Thesis convergent-design claim.** Four-layer decomposition (Knowledge / Memory / Wisdom / Intelligence) with "fundamentally different persistence semantics" instantiates SCC axiom directly. "Eight convergence points" framing is independent identification of the convergence pattern this paper's framework names. Cites Karpathy's LLM Knowledge Base + BEAM benchmark + Tulving's trichotomy.

[A26] S. S. Tanguturi, "The Continuity Layer: Why Intelligence Needs an Architecture for What It Carries Forward," arXiv:2604.17273, 2026. [Online]. Available: https://arxiv.org/abs/2604.17273
- *Cited in:* `prior_art_survey.md` §5.10.2 Cat-5 case-study (NOT-adoption tier)
- *Substrate-relevance:* Cat-5 case-study. Continuity Layer + DTCM (Decomposed Trace Convergence Memory) storage primitive + four-layer development arc (SDK → hardware node → long-horizon human infrastructure) all verified. **Citation caveat:** kenosis/Alpha-Omega theological mapping framing makes this NOT-adoption tier; cite four-layer arc + DTCM selectively, avoid theological framing in cited material.

[A27] Z. Li, "Memory as Ontology: A Constitutional Memory Architecture for Persistent Digital Citizens" (Animesis), arXiv:2603.04740, Mar. 5 2026. [Online]. Available: https://arxiv.org/abs/2603.04740
- *Cited in:* `prior_art_survey.md` §5.10.3 Cat-5
- *Substrate-relevance:* Three-axiom shape (Identity Persistence + Governance Prioritization + Identity Continuity) directly mirrors FKS+SCC+SRD triple structure. Constitutional Memory Architecture as four-layer governance hierarchy + multi-layer semantic storage. "no prior AI memory system architecture places governance before functionality" parallels Substrate Thesis's structural-precedes-content stance.

[A28] G. Servedio, P. Aghilar, A. Mattiace, G. Carmosino, F. Musicco, G. Conte, V. W. Anelli, T. Di Noia, and F. M. Donini, "The EpisTwin: A Knowledge Graph-Grounded Neuro-Symbolic Architecture for Personal AI," arXiv:2603.06290, Mar. 6 2026. [Online]. Available: https://arxiv.org/abs/2603.06290
- *Cited in:* `prior_art_survey.md` §5.10.4 Cat-5
- *Substrate-relevance:* Personal Knowledge Graph as verifiable user-centric semantic-triple substrate (SCC instantiation at personal-AI scale); decoupled storage (multimodal lifting → semantic triples) and reasoning (agentic coordinator with Graph RAG + Online Deep Visual Refinement). Multi-author paper from Italian research consortium (Politecnico di Bari + Università del Salento implied).

[A29] Y. Wang and Y. Lu, "Interaction, Process, Infrastructure: A Unified Framework for Human-Agent Collaboration," arXiv:2506.11718, Jun. 13 2025 (v1); Dec. 24 2025 (v2). [Online]. Available: https://arxiv.org/abs/2506.11718
- *Cited in:* `prior_art_survey.md` §5.10.5 Cat-5
- *Substrate-relevance:* Three-layer framework (Interaction / Process / Infrastructure) with Process elevated to first-class concern as "explicit, inspectable structural representation of activities." Five-module Process Model. **NOTE: 2025 paper, not 2026** — predates much of the rest of this cluster; suggests the convergence pattern was already detectable in 2025 academic literature.

[A30] D. B. Piskala, "MAPLE: A Sub-Agent Architecture for Memory, Learning, and Personalization in Agentic AI Systems," arXiv:2602.13258, Feb. 3 2026. [Online]. Available: https://arxiv.org/abs/2602.13258
- *Cited in:* `prior_art_survey.md` §5.10.6 Cat-5
- *Substrate-relevance:* Three-mechanism decomposition (Memory / Learning / Personalization) with separation-of-concerns + asynchronous operation + explicit user models. Each component is a "dedicated sub-agent with specialized tooling and well-defined interfaces"; 14.6% personalization improvement. Same-axiom-recurring-across-distinct-components shape at the sub-agent layer.

[A31] S. Liu, S. Tian, K. Hu, Y. Dong, Z. Yang, B. Li, J. Yang, C. C. Loy, and Z. Liu, "FileGram: Grounding Agent Personalization in File-System Behavioral Traces," arXiv:2604.04901, Apr. 6 2026. [Online]. Available: https://arxiv.org/abs/2604.04901
- *Cited in:* `prior_art_survey.md` §5.10.7 Cat-5 candidate
- *Substrate-relevance:* FileGramOS bottom-up memory architecture builds user profiles directly from atomic actions and content deltas; three-channel memory routing (procedural / semantic / episodic) with query-time abstraction. Multi-author paper from NTU/MMLab Singapore implied. Code/project resources referenced as available.

### A.8 Cat-4 supporting refs (related-work breadth, not axiom-convergent)

[A32] A. Bering, "ZenBrain: A Neuroscience-Inspired 7-Layer Memory Architecture for Autonomous AI Systems," arXiv:2604.23878, 2026. [Online]. Available: https://arxiv.org/abs/2604.23878
- *Cited in:* `prior_art_survey.md` §5.10 Cat-4 supporting (DEMOTED from initial Cat-5/6 candidate)
- *Substrate-relevance:* Real 7-layer memory architecture (working / short-term / episodic / semantic / procedural / core / cross-context). **DEMOTED 2026-05-01 from initial Cat-5/6 candidate** because Exa-attributed citations of mempalace + Mastra + Claude Code Auto Dream + Karpathy were verified FABRICATED (not in actual paper). The "Practitioners and industry are converging on the same thesis" quote is also FABRICATED. Cite for the 7-layer architecture only as Cat-4 operating-instructions instance. Real comparators in paper: letta / a-mem / mem0 (LongMemEval-500 evaluation).

[A33] L. Obiuwevwi, K. J. Rechowicz, V. Ashok, S. Shetty, and S. Jayarathna, "Cognitive Prosthetic: An AI-Enabled Multimodal System for Episodic Recall in Knowledge Work," arXiv:2603.02072, 2026. [Online]. Available: https://arxiv.org/abs/2603.02072
- *Cited in:* `prior_art_survey.md` §5.10 Cat-4 supporting
- *Substrate-relevance:* Cognitive Prosthetic Multimodal System (CPMS) combines speech transcripts + physiological signals + gaze behavior into temporally aligned episodic records; structured episodic capture; natural-language querying of past experiences; privacy safeguards. Cite for episodic-recall + multimodal-knowledge-work breadth at Related-Work scope. **Caveat:** Exa-attributed "Self-Organizing Personal Knowledge Assistants" framing was verified FABRICATED (not in actual paper).

---

## §B — Industry analyses (non-peer-reviewed but load-bearing)

[B1] GitHub, "How to write a great agents.md: Lessons from over 2,500 repositories," GitHub Blog, 2026. [Online]. Available: https://github.blog/ai-and-ml/github-copilot/how-to-write-a-great-agents-md-lessons-from-over-2500-repositories
- *Cited in:* `prior_art_survey.md` §2.5 industry analyses

[B2] GitHub, "Accelerate developer productivity with these 9 open source AI and MCP projects," GitHub Blog, 2026. [Online]. Available: https://github.blog/open-source/accelerate-developer-productivity-with-these-9-open-source-ai-and-mcp-projects/
- *Cited in:* `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md`; this bibliography (informs §C MCP server roster)

[B3] M. Danilchenko, "MemPalace Review: The 100% Score Was Fake. 96.6% Is Real.," danilchenko.dev, Apr. 10 2026. [Online]. Available: https://www.danilchenko.dev/posts/2026-04-10-mempalace-review-ai-memory-system-milla-jovovich/ [URL verified live via WebFetch 2026-04-30]
- *Cited in:* `Mempalace_NeedSingularity_CommunityContext_20260425.md` §3.4 (credibility audit) + §6; Essay 6 (`06_anti_patterns_first_draft.md` Documentation Drift section)
- *Audit catch 2026-04-30:* prior bibliography draft listed title as "...That Broke GitHub in a Weekend" — that framing came from a paraphrase of the post's content, not the actual headline. WebFetch-verified title corrected. URL slug retains the original `milla-jovovich` reference (the MemPalace creator's GitHub handle). Substantive claims (contradiction-detection absent from source code; AAAK accuracy 84.2% vs 96.6% raw mode; benchmark-gaming acknowledgment) all confirmed in re-WebFetch.

[B4] Väinämöinen / Pulsed Media, "Väinämöinen vs MemPalace vs claude-mem: A Source-Code-Level Comparison of AI Agent Memory Systems," dev.to, Apr. 15 2026. [Online]. Available: https://dev.to/vainamoinen/vainamoinen-vs-mempalace-vs-claude-mem-a-source-code-level-comparison-of-ai-agent-memory-systems-4bk4 [URL verified live via WebFetch 2026-04-30]
- *Cited in:* `Mempalace_NeedSingularity_CommunityContext_20260425.md` §3.2 + §6
- *Verified content:* compares the three systems across 18 dimensions; claims Väinämöinen wins 15/18; promotional tone for the author's own system; source-code-grounded critique of MemPalace's claimed-but-unimplemented features.

[B5] OSSInsight, "Public API," 2026. [Online]. Available: https://api.ossinsight.io/
- *Cited in:* This bibliography (used to validate trending/star data)
- *Note:* Trending-list star counts represent monthly delta, NOT absolute total — verified via direct GitHub fetch on 2026-04-25

---

## §C — Open-source projects (verified 2026-04-25 via GitHub)

### C.1 Personal-AI-memory layer (Category 5 candidates)

[C1] Milla Jovovich (handle), "MemPalace: Local-first AI memory," GitHub repository, 2026. [Online]. Available: https://github.com/MemPalace/mempalace
- *Verified 2026-04-30:* **50.5k stars** / 6.6k forks / Python 91.7% / MIT / v3.3.3 (released Apr. 24 2026, "restore install integrity")
- *Verification history:* 49.6k stars at 2026-04-25 audit; 50.5k stars at 2026-04-30 re-verification (+0.9k drift in 5 days, consistent with continued community growth)
- *Cited in:* `prior_art_survey.md` §5.1; `Mempalace_NeedSingularity_CommunityContext_20260425.md`; Essays 02/03/04/05/06/07; `academic_paper_outline.md` §2.6 + §4.3 case study C; `Personal_Temporal_Journal_Hierarchy_20260425.md` (Category 5.6 ancestor)

[C2] doobidoo, "MCP Memory Service: Persistent Shared Memory for AI Agent Pipelines," GitHub repository, 2026. [Online]. Available: https://github.com/doobidoo/mcp-memory-service
- *Verified 2026-04-25:* **1.7k stars**, v10.40.3 (released Apr. 24 2026), Apache 2.0
- *Cited in:* `prior_art_survey.md` §5.2; `academic_paper_outline.md` §2.6 + §4.3 (Triple-Layer Test DB Safety attribution as cross-practitioner SRD instance)

### C.2 LM-programming layer

[C3] StanfordNLP, "DSPy: Declarative framework for building modular AI software," GitHub repository, 2022 - present. [Online]. Available: https://github.com/stanfordnlp/dspy
- *Verified 2026-04-25:* **34k stars**, v3.2.0 (released Apr. 21 2026), MIT licensed, Python
- *Cited in:* this bibliography (Category 5 candidate; deferred under an incorporate-first sequencing pivot)
- *Operational status 2026-04-25:* installed v3.2.0; ANTHROPIC_API_KEY in DPAPI but credit balance too low for actual model calls

### C.3 LLM observability layer

[C4] Langfuse, "Open Source LLM Engineering Platform," GitHub repository, 2023 - present. [Online]. Available: https://github.com/langfuse/langfuse
- *Verified 2026-04-25:* **26.1k stars**, v3.170.0 (released Apr. 23 2026), MIT (with enterprise edition exceptions), TypeScript 98.8%, Y Combinator W23
- *Cited in:* `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md` §2
- *Operational status 2026-04-25:* langfuse Python SDK 4.5.1 installed; Docker self-host setup pending

### C.4 Workflow orchestration

[C5] n8n.io, "n8n: Free and source-available fair-code licensed workflow automation tool," GitHub repository. [Online]. Available: https://github.com/n8n-io/n8n
- *Star count via Awesome-integration secondary source:* ~184k stars (not directly verified 2026-04-25 — flagged)
- *Cited in:* KLEM/OS v3 Part F roster; `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md`; this bibliography (operational candidate)

### C.5 MCP server ecosystem

[C6] Anthropic, "Claude Code," GitHub repository, 2025 - present. [Online]. Available: https://github.com/anthropics/claude-code [Accessed 2026-04-25]
- *Star count:* 118k stars (verified directly via WebFetch 2026-04-25)
- *Repository scale:* 603+ commits on main; ~5,000 issues; 511 pull requests; primary languages Shell 47.1% / Python 29.2% / TypeScript 17.7%
- *Cited in:* throughout corpus; foundational tool

[C6a] Anthropic, "Claude Code Action," GitHub repository, 2025 - present. [Online]. Available: https://github.com/anthropics/claude-code-action [Accessed 2026-04-25]
- *Star count:* 7.3k stars (verified directly via WebFetch 2026-04-25)
- *Notable:* CLAUDE.md exists at repository root (treated as vendor-canonical example in `case_studies/07_appendix_prevalence_study_preliminary_20260425.md`)
- *Cited in:* Case Study 07 prevalence appendix as vendor-canonical CLAUDE.md exemplar

[C7] Anthropic, "Public Agent Skills repository," GitHub repository, 2025 - present. [Online]. Available: https://github.com/anthropics/skills [Accessed 2026-05-01]
- *Star count:* 124k stars (verified directly via WebFetch 2026-04-25)
- *Cited in:* **`prior_art_survey.md` §6.3 Category 6 (PROMOTED 2026-05-01 from Cat-4 to Cat-6 following code-level audit at `Writings/Source_Repos_Audit_20260501.md`)**; academic_paper_outline.md §1 + §2.7; `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md`
- *Substrate-relevance:* **HEADLINE Cat-6 case study for CHI 2027** — Anthropic's Skills system instantiates all three Substrate Thesis axioms (FKS via SKILL.md → scripts → references → agents → assets layering; SCC via name-stable frontmatter + plugin-marketplace versioning; SRD via skill-creator as canonical meta-recursive skill-for-creating-skills signature). The most-credentialed possible convergence anchor: the AI lab building the foundational AI independently converges on the same architecture this paper's framework predicts. Spec at agentskills.io/specification.

[C7a] Anthropic, "Claude Cookbooks: 76 production-quality Jupyter notebooks for building with Claude," GitHub repository, 2024-present. [Online]. Available: https://github.com/anthropics/anthropic-cookbook [Accessed 2026-05-01]
- *Star count:* 41k+ stars (per April 2026 documentation)
- *Cited in:* **`prior_art_survey.md` §5.9 Category 5 (added 2026-05-01 following code-level audit at `Writings/Source_Repos_Audit_20260501.md`)**; academic_paper_outline.md §1 + §2.6
- *License:* MIT
- *Substrate-relevance:* **Cat-5 multi-axiom convergence at the pedagogical-infrastructure scale.** FKS via helper-modules + nested CLAUDE.md per subdirectory (operating-instructions inheritance pattern); SCC via registry.yaml schema-validated 76-notebook catalog + naming conventions (CMA_* prefix, etc.) + pre-commit validation; SRD via uniform notebook structural shape across all 76 entries. Combined with [C7] Skills, Anthropic now has TWO Cat-5+ artifacts in prior_art_survey demonstrating the framework's axioms across BOTH pedagogical infrastructure AND production capability infrastructure.

[C7b] Park, M.W. / need-singularity org, "Independent research organization with multi-axiom convergence across 14+ repos," GitHub organization, 2025-present. [Online]. Available: https://github.com/need-singularity [Accessed 2026-04-30]
- *Cited in:* **`prior_art_survey.md` §6.2 Category 6 (added 2026-04-30; per-repo entries at §5.4 nexus / §5.5 papers / §5.6 n6-architecture / §5.7 anima / §5.8 hexa-lang)**; academic_paper_outline.md §2.6 + §2.7
- *Author:* Park Min Woo (Independent Research)
- *Substrate-relevance:* **Cat-6 whole-ecosystem convergence (secondary entry alongside Miessler [C17a-f] primary case and Anthropic Skills [C7] tertiary case).** Five distinct Cat-5 components within one stack (nexus FKS in OUROBOROS cycle; papers SCC in DOI-anchored Zenodo+OSF dual-archive; n6-architecture SRD in cross-domain pattern-recurrence; anima SRD in cross-substrate consciousness implementation; hexa-lang SRD in multi-target single-source compilation). Per-repo adoption-tier varies per `prior_art_survey.md §5.4-5.8` per-repo summary table.

[C7c] Park, M.W. / need-singularity, "papers: Complete paper collection with DOI-anchored Zenodo+OSF dual-archive," GitHub repository, 2025-present. [Online]. Available: https://github.com/need-singularity/papers [Accessed 2026-05-01]
- *Cited in:* `prior_art_survey.md` §5.5 (verified 2026-05-01 via Source_Repos audit)
- *Umbrella DOI:* 10.5281/zenodo.19271599 (CC BY 4.0)
- *Substrate-relevance:* **Cat-5 single-axiom convergence (SCC) at research-publication-layer.** 120 papers / 92 published; schema-validated manifest.json; per-paper Zenodo DOIs; name-stable IDs (P-001, PA-01-..., etc.). Most-direct example of SCC discipline at corpus scale in any prior-art surveyed.

[C8] tadata-org, "fastapi_mcp: Expose secure FastAPI endpoints as MCP tools," GitHub repository. [Online]. Available: https://github.com/tadata-org/fastapi_mcp
- *Cited in:* `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md` §6 candidates from GitHub blog [B2]

[C9] Upstash, "context7: Pulls version-specific documentation into AI prompts," GitHub repository. [Online]. Available: https://github.com/upstash/context7
- *Cited in:* GitHub blog [B2]; this bibliography (operational candidate under an incorporate-all-candidates sequencing decision, 2026-04-25)
- *Substrate-relevance:* partial (context retrieval similar to Exa search patterns)

[C10] oraios, "serena: Semantic code editing and retrieval for agent-driven coding," GitHub repository. [Online]. Available: https://github.com/oraios/serena
- *Cited in:* GitHub blog [B2]; this bibliography (operational candidate)
- *Substrate-relevance:* partial (semantic retrieval overlaps with DSPy retrieval patterns)

[C11] czlonkowski, "n8n-mcp: AI integration for n8n workflow automation," GitHub repository. [Online]. Available: https://github.com/czlonkowski/n8n-mcp
- *Cited in:* GitHub blog [B2]; this bibliography (operational candidate complementing [C5])

[C12] CoplayDev, "unity-mcp: Unity game engine MCP integration," GitHub repository. [Online]. Available: https://github.com/CoplayDev/unity-mcp
- *Cited in:* GitHub blog [B2]; out-of-scope for current Substrate work

[C13] antfu, "nuxt-mcp: Nuxt developer tools MCP," GitHub repository. [Online]. Available: https://github.com/antfu/nuxt-mcp
- *Cited in:* GitHub blog [B2]; out-of-scope for current Substrate work

[C14] steipete, "Peekaboo: Swift screen-content code analysis," GitHub repository. [Online]. Available: https://github.com/steipete/Peekaboo
- *Cited in:* GitHub blog [B2]; out-of-scope (Apple ecosystem)

[C15] instavm, "coderunner: Sandbox code execution for LLMs," GitHub repository. [Online]. Available: https://github.com/instavm/coderunner
- *Cited in:* GitHub blog [B2]; potential operational candidate (sandboxed execution)

[C16] MCPJam, "inspector: MCP server testing and debugging tool," GitHub repository. [Online]. Available: https://github.com/MCPJam/inspector
- *Cited in:* GitHub blog [B2]; operational candidate for Path B Exa MCP debugging

### C.6 Vocabulary-collision references (Category 0)

[C17] D. Miessler, "Substrate: Open-source framework for human understanding, meaning, and progress," GitHub repository, 2024-present. [Online]. Available: https://github.com/danielmiessler/Substrate [Accessed 2026-04-26]
- *Repository scale:* 800 stars, 111 forks (verified via dossier 2026-04-26); MIT licensed, TypeScript+Bun stack; 17+ structured object types (Problems / Solutions / Claims / Arguments / Plans / Ideas / People / Organizations / Projects / Data / Frames / Funding-Sources / Models / Outcomes / Questions / Results / Risks / Threats / Values)
- *Created:* 2024-07-12; *Last push:* 2025-12-10
- *Cited in:* `prior_art_survey.md` Category 0 (vocabulary-collision differentiated by scope) AND Category 6 §6.1 (Parallel Engineering Discovery primary entry)

### C.6a Daniel Miessler ecosystem — Category 6 Parallel Engineering Discovery primary entries

The following Miessler repos collectively form the strongest cross-practitioner architectural-axiom evidence in this survey. All cited together in `prior_art_survey.md` Category 6 §6.1.

[C17a] D. Miessler, "fabric: AI prompt framework for human augmentation," GitHub repository, 2024-present. [Online]. Available: https://github.com/danielmiessler/Fabric [Accessed 2026-04-26]
- *Repository scale:* 41,072 stars, 4,091 forks (verified 2026-04-26); MIT licensed; Go (originally Python, rewritten)
- *Created:* 2024-01-03; *Last push:* 2026-04-23 (actively maintained)
- *Architectural concept:* Pattern (named, composable system prompt; SCC instance #1 in triple-instantiation argument)
- *Verbatim mission:* "human_flourishing_via_AI_augmentation"
- *Verbatim philosophy:* "AI doesn't have a capabilities problem - it has an integration problem"
- *Cited in:* `prior_art_survey.md` Category 6 §6.1; SCC empirical evidence

[C17b] D. Miessler, "Personal AI Infrastructure (PAI): Agentic AI infrastructure for magnifying human capabilities," GitHub repository, 2025-present. [Online]. Available: https://github.com/danielmiessler/Personal_AI_Infrastructure [Accessed 2026-04-30]
- *Repository scale (2026-04-30 re-verify):* **11.9k stars, 1.6k forks**; **latest release v5.0.0 ("Life Operating System")** — major version bump from v4.0.3 since the 2026-04-25 audit; 45 integrated skills with 171 workflows; Algorithm v6.3.0 (seven-phase problem-solving loop); ISA (Ideal State Artifact) primitive; structural privacy via containment zones; Bun runtime for the Pulse daemon
- *Created:* 2025-09-08; *Last activity:* Mar 2 2026 v4.0.3 patch + v5.0.0 release subsequent
- *Architectural concept:* 16 numbered architectural Principles; 9 Core Primitives; 3-tier AI maturity model (Chatbots / Agentic Platforms / PAI); Skills system as SCC instance #2
- *Notable principle:* #4 "Scaffolding > Model selection" (direct mapping to Substrate Thesis central architecture-over-content axiom)
- *v5.0.0 framing implication:* "Life Operating System" naming connects directly to the Substrate Thesis personal-OS framing; bibliography entry at next prior_art_survey refresh should treat this version-bump as a strong convergence-evidence datapoint (cross-practitioner SCC plus operating-system-as-personal-substrate framing)
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (primary load-bearing entry); 14-of-16 principles mapping table

[C17c] D. Miessler, "TELOS: Deep Context framework for entities," GitHub repository, 2024-present. [Online]. Available: https://github.com/danielmiessler/Telos [Accessed 2026-04-26]
- *Repository scale:* 1,334 stars, 205 forks
- *Created:* 2024-10-04; *Last push:* 2026-01-09
- *Architectural concept:* 10-file structure (MISSION / GOALS / PROJECTS / BELIEFS / MODELS / STRATEGIES / NARRATIVES / LEARNED / CHALLENGES / IDEAS); SCC instance #3 in triple-instantiation argument
- *Relationship to PAI:* PAI's goal-documentation primitive
- *Verbatim positioning vs Substrate (Miessler's):* "Substrate provides evidence. TELOS provides intention."
- *Cited in:* `prior_art_survey.md` Category 6 §6.1; FKS analog discussion (teleological where the Substrate Thesis FKS is epistemic)

[C17d] D. Miessler, "TheAlgorithm: Universal problem-solving algorithm," GitHub repository, 2026-present. [Online]. Available: https://github.com/danielmiessler/TheAlgorithm [Accessed 2026-04-26]
- *Repository scale:* 107 stars, 12 forks (early-stage adoption; rapid development)
- *Created:* 2026-01-24; *Last push:* 2026-04-25 (one day before this survey access)
- *Architectural concept:* Seven-phase loop (OBSERVE > THINK > PLAN > BUILD > EXECUTE > VERIFY > LEARN); ISC typing system (Functional / Structural / Behavioral / Negative / Edge / Antecedent); Effort Tiers E1-E5; PRD audit (Coverage / Tightness / Uniqueness)
- *Theoretical grounding:* David Deutsch's "hard-to-vary explanation" criterion (cite [P1] below)
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (most explicit SRD instance in Miessler's work)

[C17e] D. Miessler, "Ladder: Autonomous creation and optimization system," GitHub repository, 2026-present. [Online]. Available: https://github.com/danielmiessler/Ladder [Accessed 2026-04-26]
- *Repository scale:* 203 stars, 29 forks
- *Created:* 2026-03-22; *Last push:* 2026-03-22
- *Architectural concept:* Six-collection pipeline (Sources SR- > Ideas ID- > Hypotheses HY- > Experiments EX- > Algorithms AL- > Results RE-) with feedback loop; Cognitive Phases (CONSUME / DREAM / DAYDREAM / CONTEMPLATE / STEAL / MATE / TEST / EVOLVE / META-LEARN)
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (SRD evidence at creative-optimization scale)

[C17f] D. Miessler, "SecLists: Security testing wordlists and resources," GitHub repository, 2012-present. [Online]. Available: https://github.com/danielmiessler/SecLists [Accessed 2026-04-26]
- *Repository scale:* 70,515 stars, 24,978 forks (highest-starred Miessler repo; among top 50 most-starred GitHub repos period)
- *Created:* 2012-02-19; *Last push:* 2026-04-26
- *Adjacent relevance:* establishes Miessler's community-resource-library methodology that he later applied to fabric (crowdsourced patterns) and Substrate (collaborative knowledge); not direct Substrate Thesis evidence but background context

[C17g] D. Miessler, "Unsupervised Learning Newsletter," 1996/97-present. [Online]. Available: https://newsletter.danielmiessler.com [Accessed 2026-04-26]
- *Subscriber count:* 110,000+ as of April 2026
- *Publication volume:* 3,057 essays over 29.5 years (~103 essays/year, ~2/week)
- *Audience:* CISOs, security professionals, hackers, technologists from OpenAI, Google, Apple, Global 1000 companies
- *Relevance:* venue for Miessler's framework-development-in-public; weekly stress-testing of architectural claims against real events
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (publication-pattern evidence)

[C17h] D. Miessler, "A Conversation With Claude on Deutsch, Knowledge, and the PAI Algorithm," blog post, 2026-04-24. [Online]. Available: https://danielmiessler.com/blog/conversation-with-claude-on-deutsch-and-the-pai-algorithm [Accessed 2026-04-26]
- *Relevance:* explicit theoretical grounding of TheAlgorithm in Deutsch's epistemology; foundational essay for ISC architecture; "knowledge as hard-to-vary explanation" thesis
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (Deutsch citation pathway); academic_paper_outline.md (joint theoretical scaffolding)

[C17i] D. Miessler, "We're All Building a Single Digital Assistant," blog post, 2026-04-15. [Online]. Available: https://danielmiessler.com/blog/we-are-all-building-single-digital-assistant [Accessed 2026-04-26]
- *Relevance:* convergence thesis ("DA prime directive"); current/desired/ideal state framing; maturity arc Chatbots > Agents > Assistance
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (convergence-thesis support)

[C17j] D. Miessler, "Good and Bad Harness Engineering," blog post, 2026-04-14. [Online]. Available: https://danielmiessler.com/blog/good-and-bad-harness-engineering [Accessed 2026-04-26]
- *Relevance:* context-over-instructions axiom ("the smarter AI gets, the more antiquated your prescriptive instructions will become"); scaffold design principles
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (PAI Principle #4 "Scaffolding > Model" theoretical foundation)

### P. Philosophical foundations referenced in framework grounding

[P1] D. Deutsch, *The Beginning of Infinity: Explanations That Transform the World.* Allen Lane, 2011. ISBN 978-0-71-399275-7.
- *Relevance:* "hard-to-vary explanation" criterion as foundational epistemology; Miessler's TheAlgorithm grounds ISC architecture in this concept; recommended joint theoretical scaffolding for Substrate Thesis bibliography
- *Cited in:* `prior_art_survey.md` Category 6 §6.1 (Deutsch citation pathway)

[C18] paritytech, "Substrate: Polkadot blockchain framework," GitHub repository. [Online]. Available: https://github.com/paritytech/substrate
- *Cited count:* ~8.4k stars (at time of survey)
- *Cited in:* `prior_art_survey.md` Category 0 dominant-vocabulary finding

### C.7 Other tooling cited in corpus

[C19] tensorchord, "Awesome-LLMOps: Curated list of LLMOps tools," GitHub repository. [Online]. Available: https://github.com/tensorchord/Awesome-LLMOps
- *Cited in:* operational tooling-roster notes (internal); ingested 2026-04-25 as a candidate resource for the framework's operational toolchain

[C20] stn1slv, "awesome-integration: Curated system integration software list," GitHub repository. [Online]. Available: https://github.com/stn1slv/awesome-integration
- *Cited in:* `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md`; ingested 2026-04-25

[C21] eltociear, "awesome-AI-driven-development: 542 AI-powered development tools," GitHub repository. [Online]. Available: https://github.com/eltociear/awesome-AI-driven-development
- *Cited in:* `Tool_Integration_Plan_DSPy_Langfuse_StackAI_ElevenLabs_HeyGen_20260425.md`; ingested 2026-04-25

---

## §D — Vendor documentation (cite as venue + version)

[D1] Anthropic, "Claude Code memory documentation," 2026. [Online]. Available: https://code.claude.com/docs/en/memory
- *Cited in:* `prior_art_survey.md` §2.5 industry-authoritative; foundational for CLAUDE.md convention

[D2] GitHub, "Adding custom instructions for GitHub Copilot," documentation, 2026. [Online]. Available: https://docs.github.com/copilot/customizing-copilot/adding-custom-instructions-for-github-copilot
- *Cited in:* `prior_art_survey.md` §2.5

[D3] AGENTS.md spec maintainers, "AGENTS.md canonical specification," 2026. [Online]. Available: https://agents.md
- *Cited in:* `prior_art_survey.md` §2.5

[D4] Aider, "Configuration documentation (.aider.conf.yml)," 2026. [Online]. Available: https://aider.chat/docs/config/aider_conf.html
- *Cited in:* `prior_art_survey.md` §2.5

[D5] OSSInsight, "Public API beta documentation," 2026. [Online]. Available: https://ossinsight.io/docs/api
- *Cited in:* this bibliography (used 2026-04-25 to validate trending/star data)
- *Rate limit note:* 600 req/hr per IP; 1000 req/min global; no auth

---

## §E — Practitioner / community references

[E1] Reddit r/ClaudeCode community, "We analyzed 12,356 repos with claude.md files," 2026. [Online]. Available: https://www.reddit.com/r/ClaudeCode/comments/1srm2vv/we_analyzed_12356_repos_with_claudemd_files
- *Cited in:* `prior_art_survey.md` §2.5 community-authoritative

[E2] 0xdevalias, "Some notes on AI Agent Rule / Instruction / Context files / etc," GitHub Gist, 2026. [Online]. Available: https://gist.github.com/0xdevalias/f40bc5a6f84c4c5ad862e314894b2fa6
- *Cited in:* `prior_art_survey.md` §2.5

---

## §F — Datasets / benchmarks

[F1] LongMemEval benchmark (referenced via mempalace BENCHMARKS.md). Used by [C1] for the 96.6% R@5 raw-mode performance claim. Direct citation deferred until verified against original paper.

[F2] c-CRAB Code Review Agent Benchmark dataset, introduced by [A6]. Used for evaluating PR-agent, Devin, Claude Code, and Codex code review agents.

[F3] LoCoMo benchmark (referenced via mempalace and Penfield Labs critique). Direct citation deferred.

---

## §G — Internal Substrate Thesis Companion artifacts (cross-referenced for self-citation hygiene)

[G1] S. C. Caddell, "Substrate Thesis Companion repository," GitHub, 2026. [Online]. Available: https://github.com/barelyaninconvenience/substrate-thesis-companion

[G2] S. C. Caddell, "Prompt Engineering Field Guide," GitHub repository, Feb. 26 2026. [Online]. Available: https://github.com/barelyaninconvenience/Prompt_Engineering
- *Cited in:* `prior_art_survey.md` Category 0 (predecessor to Substrate Thesis SRD pattern naming)

[G3] S. C. Caddell, "structured-data-crawler-substrate," GitHub repository, 2026. [Online]. Available: https://github.com/barelyaninconvenience/structured-data-crawler-substrate
- *Cited in:* substrate-thesis-companion case_studies/04 (job crawler architecture as SRD instance)

---

## §H — Audit + provenance metadata

**Authored 2026-04-25** under an audit-style directive: prefer formal IEEE-style citation hygiene over implicit "trust the source" references throughout the corpus.

**Bibliography-hygiene status (post 2026-04-30 audit pass):**
- ✅ Gloaguen vs Liu disambiguation resolved (was [A1])
- ✅ ~~Konrad disambiguation strategy applied (2026a/2026b for [A2]/[A3])~~ → **superseded 2026-04-30**: [A2] "Agentic Much?" was incorrectly attributed to Konrad et al. in earlier draft; arXiv direct WebFetch confirmed actual authors are Robbes / Matricon / Degueule / Hora / Zacchiroli. [A2] handle is now "Robbes et al. (2026)"; [A3] handle simplified to "Konrad et al. (2026)" since same-first-author conflict no longer applies.
- ✅ [A8] Schreiber & Tippe initials corrected 2026-04-30 from "J./N." to "M./P." (Maximilian Schreiber, Pascal Tippe per arXiv direct verification)
- ✅ [A7] He et al. venue framing refined 2026-04-30: "CMU MSR 2026" → "MSR 2026, Rio de Janeiro" with note that authors are at CMU's STRUDEL group; first-author confirmed Hao He
- ✅ [B3] Danilchenko + [B4] Väinämöinen URLs verified live via WebFetch 2026-04-30
- ✅ [B3] title corrected 2026-04-30 from paraphrase ("...Broke GitHub in a Weekend") to actual headline ("MemPalace Review: The 100% Score Was Fake. 96.6% Is Real.")
- ✅ [C1] MemPalace star count refreshed 2026-04-30: 49.6k → 50.5k (5-day drift)
- ✅ [C17b] PAI version refreshed 2026-04-30: v4.0.3 → v5.0.0 ("Life Operating System") — major version bump worth dedicated cross-pollination treatment in `prior_art_survey.md` Category 6 §6.1
- ✅ [C17] / [C17a] / [C17c] minor star+fork drifts captured 2026-04-30 (Substrate 800→803; Fabric 41.1k→41.2k; TELOS forks 205→206)
- ⚠️ Star counts verified for [C1]/[C2]/[C3]/[C4]/[C17]/[C17a]/[C17b]/[C17c] via direct GitHub WebFetch (2026-04-25 + 2026-04-30 re-verify)
- ⚠️ Schreiber & Tippe [A8] cited 3× in `prior_art_survey.md`; consolidation queued
- ⚠️ [C5] n8n star count via secondary source only; direct verification queued
- ⚠️ [C17d] TheAlgorithm + [C17e] Ladder + [C17f] SecLists + [C17g] Newsletter star counts not re-verified 2026-04-30 (carrying forward 2026-04-26 dossier values)
- ⚠️ [F1]/[F3] benchmarks cited indirectly; original papers should be located

**Audit cycle takeaway 2026-04-30:** of 8 academic citations [A1-A8], 3 had truth-discipline violations (37.5%): [A2] entire author list wrong (cross-contamination from [A3]), [A8] author initials wrong, [B3] post title wrong (paraphrase substituted for actual headline). All three corrected. The pattern matches the Module 8/9/11 truth-discipline catches in IT 7021C work — confidently-stated specifics that were drafted without re-verification at authoring time. Going forward: every citation entry must reach this file with at-the-time WebFetch verification of authors, title, version/date, and URL liveness; prior_art_survey + academic_paper_outline cross-references must propagate corrections via mini-ENDEAVOR pass.

**Cross-reference index status:** complete for all entries citing within the substrate-thesis-companion repository as of 2026-04-25. Future citations should add reverse-references back to this file.

**Update protocol:** when adding a new citation in any artifact, also add the entry here with cross-reference. When verifying a previously-unverified claim, update the verification status here. This file is the canonical source.

---

*Bibliography first unified version 2026-04-25. IEEE author-list style; access dates default to 2026-04-25 unless noted. Cross-references go both ways: each entry lists every artifact citing it. Audit + provenance metadata in §H makes verification gaps visible. Companion: `Audit_Findings_Bibliography_and_Fabrication_20260425.md` (the audit reports that drove this consolidation).*
