# Differentiation Analysis — Substrate Thesis vs. Galster et al. arXiv 2602.14690
## "Configuring Agentic AI Coding Tools: An Exploratory Study"

**Status:** Authored 2026-04-25 from WebFetch extraction (free; no Exa burn). **Re-verified 2026-04-26 overnight** via second WebFetch pass — Galster confirmed as first author (full author list: Galster, Mohsenimofidi, Lulla, Abubakar, Treude, Baltes); latest revision v3 dated 2026-04-09; abstract verbatim confirmed; eight mechanisms NOT enumerated in abstract (Context Files / Skills / Subagents are the three highlighted exemplars). Full-paper read still needed for the explicit eight-mechanism enumeration. Companion to `prior_art_survey.md` Category 4.1 + `differentiation_vs_konrad_2601_18341_20260425.md` (adjacent empirical work — Konrad: 129K repos / adoption; Galster: 2,923 repos / mechanism inventory).

---

## TL;DR for the CHI submission

Galster et al. (Mohsenimofidi, Lulla, Abubakar, Treude, Baltes; arXiv 2602.14690, first submitted Feb 16 2026, latest revision Apr 9 2026 v3) is **the closest empirical-mechanism-inventory work to the Substrate Thesis Case Study 07 prevalence appendix**. They examine **2,923 GitHub repositories** across Claude Code, GitHub Copilot, Cursor, Gemini, and Codex, and identify **eight configuration mechanisms** spanning a spectrum from static context to executable workflows.

Their key empirical findings directly support the Substrate Thesis's prevalence claim:

1. **Context Files (CLAUDE.md / AGENTS.md / .cursorrules / etc.) dominate** the configuration landscape and are often the sole mechanism used in a repository
2. **AGENTS.md is emerging as an interoperable cross-tool standard**
3. **Advanced mechanisms (Skills, Subagents) show shallow adoption** — most repos define one or two artifacts
4. **Distinct configuration cultures forming around different tools** — Claude Code users employ the broadest range of mechanisms
5. **Skills predominantly rely on static instructions** rather than executable workflows

**Strategic relevance:** Galster et al. is the **single most-citable empirical work for the Substrate Thesis prevalence claim** because their mechanism inventory directly maps to FKS/SCC/SRD pattern instances and their adoption-distribution data establishes the convention's empirical weight. Cite as foundation; differentiate by providing the structural framework that explains the eight mechanisms' coexistence.

---

## Their key claims

1. **Eight configuration mechanisms** for agentic AI coding tools span a spectrum from static context to executable and external integrations
2. **Context Files dominate** the landscape and are often the sole configuration mechanism in a repository
3. **AGENTS.md is emerging as an interoperable standard** across tools
4. **Skills and Subagents are only shallowly adopted** — most repositories define only one or two artifacts
5. **Skills predominantly rely on static instructions** rather than executable workflows
6. **Distinct configuration cultures** are forming around different tools, with Claude Code users employing the broadest mechanism range
7. **AGENTS.md serves as a natural starting point** for new adopters; longitudinal study warranted

## Their methodology

- **Type:** empirical exploratory study
- **Sample:** N = 2,923 GitHub repositories
- **Tools surveyed:** Claude Code, GitHub Copilot, Cursor, Gemini, Codex
- **Analytical lens:** mechanism-inventory + adoption-pattern + tool-specific-culture
- **Detailed analysis depth:** Context Files, Skills, Subagents (the three most distinctive mechanism categories)

## Their gap (Substrate Thesis fills it)

1. **No structural framework explaining the mechanism inventory** — their eight mechanisms are described as observed categories; they don't articulate why these particular eight emerge or which structural patterns each mechanism instantiates
2. **No multi-pattern integration** — Skills + Subagents + Context Files are presented as parallel mechanism types; Substrate Thesis treats them as SRD instances at different scales (Context Files = root layer; Skills = recursive decomposition of capability; Subagents = recursive decomposition of agent specialization)
3. **No diagnostic framework for well-formed vs malformed configuration** — they observe what's adopted; they don't theorize what makes a configuration well-formed (FKS layer separation, SCC versioning discipline, SRD pattern reuse)
4. **No PKM / personal informatics / system-design canonical engagement** — same notable absence as Konrad et al. and Gloaguen et al.; the SE-and-AI-systems-only related-work pattern continues
5. **Adoption-pattern framing without structural-prescription** — their "AGENTS.md is a natural starting point" recommendation is descriptive (most adopters start there); they don't articulate the structural reasoning (AGENTS.md as Layer 0 in an FKS hierarchy)

## Strategic positioning

Galster et al. is the **highest-leverage existing empirical work for the Substrate Thesis Case Study 07 prevalence appendix** because:

- Their N = 2,923 is large enough to be authoritative without being unwieldy
- Their five-tool comparison (Claude Code, Copilot, Cursor, Gemini, Codex) is comprehensive and Claude-Code-prominent
- Their AGENTS.md interoperability finding directly supports the cross-tool SRD claim
- Their Skills/Subagents shallow-adoption finding is consistent with the Substrate Thesis prediction that advanced patterns require deliberate framework discipline beyond what default adoption produces

**Citation strategy:**
- Case Study 07 §3 Prevalence: Galster et al. as primary empirical citation alongside Gloaguen et al. 2602.11988 and Konrad et al. 2601.18341
- CHI §2 Related Work: Galster et al. is the most directly comparable empirical work; honest framing is "they describe the mechanism landscape, we provide the structural framework"
- CHI §3 Framework: explicitly map their eight mechanisms onto FKS/SCC/SRD pattern instances (mapping table below)

## Mapping Galster et al.'s eight mechanisms onto Substrate Thesis patterns

**Status update 2026-04-26 overnight:** the abstract verifies Context Files / Skills / Subagents as three of the eight; the remaining five are inferred from the abstract's framing ("spectrum from static context to executable and external integrations") and from observed configuration practice in the Anthropic + GitHub Copilot + Cursor + Gemini + Codex ecosystems. Each row below carries a **falsifier** — the empirical observation that would invalidate the mapping if the full paper's mechanism enumeration differs from the inferred set.

| # | Galster Mechanism (verified or inferred) | Substrate Thesis Pattern Instance | Concrete example | Falsifier |
|---|---|---|---|---|
| 1 | **Context Files** (AGENTS.md / CLAUDE.md / .cursorrules / etc.) — *abstract-verified* | Layer 0 of an FKS hierarchy; the most-superficial-but-most-canonical operating-instructions scale | Repo-root CLAUDE.md / AGENTS.md | Galster classifies as multi-layer rather than Layer 0 |
| 2 | **Path-scoped instructions** (.github/copilot-instructions.md / .instructions.md) — *inferred* | Layer 1 FKS instance; SCC at per-directory scope; same FKS pattern instantiated one scale deeper | `.github/copilot-instructions.md` for repo-scoped Copilot rules | Galster does not include path-scoped instructions in the eight (rolls into Context Files as one mechanism) |
| 3 | **Skills** (`anthropics/skills` directory pattern; per-capability instruction packages) — *abstract-verified* | SRD instance — same recursive shape (instructions + scripts + resources) applied at the per-capability scale | `.claude/skills/<name>/SKILL.md` + supporting files | Galster classifies Skills as Context-File-extension rather than its own mechanism |
| 4 | **Subagents** (Claude Code subagent definitions; per-agent-specialization) — *abstract-verified* | SRD instance — same recursive shape applied at the per-agent-specialization scale | `.claude/agents/<name>.md` defining a specialized agent | Galster classifies Subagents as orchestration-only, distinct from configuration |
| 5 | **Memory files / directives** (CLAUDE.md memory blocks; auto-memory systems) — *inferred* | SCC at the durable-policy scale; persistent state-of-practitioner-and-collaboration | a memory index file plus per-topic memory files | Galster does not surface memory as a configuration mechanism (treats as agent-internal) |
| 6 | **MCP server registrations** (`mcp.json` / `.claude.json` mcpServers) — *inferred* | FKS Layer N — external-integration boundary; the seam between agent-side configuration and external tool ecosystems | `~/.claude.json` mcpServers block; `~/.mcp.json` | Galster does not include MCP as a configuration mechanism (treats as outside-scope external infrastructure) |
| 7 | **Hooks** (pre-commit / pre-compact / post-write / stop hooks) — *inferred* | Operational-trigger instances; cross-cutting governance that wraps the FKS at execution time | `.claude/settings.json` hooks block | Galster does not include hooks (treats as platform-specific extension) |
| 8 | **Configuration JSON** (settings.json / settings.local.json / per-tool config) — *inferred* | SCC at the runtime-configuration scale; the per-installation versioned policy | `~/.claude/settings.json` permissions / env / model | Galster collapses runtime config into Context Files |

**The structural argument:** the contribution Substrate Thesis adds to Galster et al.'s empirical work is the recognition that each of their eight mechanisms is **one of three patterns (FKS / SCC / SRD) operating at a different scale**, and that the mechanisms coexist because the framework *predicts* them to coexist. The framework also predicts which mechanisms should appear together (Context Files + Memory files + Configuration JSON form an FKS-coherent set; Skills and Subagents are SRD instances at adjacent scales) and which would be redundant (two parallel mechanisms at the same scale targeting the same pattern would indicate framework misalignment, not richness).

**Empirical falsification opportunity:** if the full Galster paper enumerates a mechanism that does NOT map onto FKS / SCC / SRD, that's an honest discontinuation point for the framework — surface and address it openly. Conversely, if the eight mechanisms ALL map cleanly, this is a strong positive control for the framework's explanatory adequacy at the configuration-mechanism scale.

**Pending action:** full-paper read on next dedicated CHI prep session to (1) replace the inferred rows with verified rows, (2) document any non-mappable mechanisms as honest framework boundary, and (3) verify the framework's predicted co-occurrence patterns against Galster's adoption distribution.

## Recommended treatment in CHI §2 Related Work

Approximately 250-350 words. Suggested paragraph:

> Galster et al. (2026) provide the most comprehensive empirical mechanism inventory to date, examining 2,923 GitHub repositories across five agentic AI coding tools (Claude Code, GitHub Copilot, Cursor, Gemini, Codex) and identifying eight distinct configuration mechanisms ranging from static Context Files to executable Skills to runtime Subagents. Their findings establish three load-bearing facts for our work: Context Files dominate the configuration landscape (often as the sole mechanism in a repository); AGENTS.md is emerging as an interoperable cross-tool standard; and advanced mechanisms — Skills and Subagents in particular — show shallow adoption, with most repositories defining only one or two artifacts. We build directly on Galster et al.'s empirical baseline and complement it with structural theory: where they observe that eight mechanisms coexist, we articulate why these particular eight (and not others) emerge from the underlying FKS/SCC/SRD pattern interactions. Section 3 maps each Galster mechanism to a specific Substrate Thesis pattern instance, demonstrating that the apparent diversity of configuration approaches reduces to three patterns operating at different scales.

## Recommended treatment in Case Study 07 §3 Prevalence

Galster et al. should appear alongside Liu et al. (2602.11988) and Konrad et al. (2601.18341) as the empirical-prevalence-citation triad. Their N=2,923 anchors the medium-scale evidence (between Gloaguen's >60,000 and the qualitative case studies). Their AGENTS.md interoperability finding directly supports the Case Study 07 claim that the convention is converging on a cross-practitioner standard (cross-practitioner SRD).

## Open questions for full-paper read (when CHI submission prep advances)

- The full eight-mechanism list with definitions (only abstract-level summary extracted via WebFetch)
- Specific adoption percentages per mechanism per tool (the "Claude Code users employ broader mechanism range" claim deserves quantification)
- Which mechanisms are co-occurring vs mutually exclusive (informs the FKS layer-separation argument)
- Their detection methodology + error rates (informs prevalence-claim defensibility)
- Their related-work section's full citation list (gap analysis for the PKM/SE-canon engagement absence)

---

*Galster et al. arXiv 2602.14690 differentiation memo authored 2026-04-25 from WebFetch extraction (zero Exa cost). Status: ready for CHI §2 Related Work + Case Study 07 §3 Prevalence integration; needs full-paper read for mechanism-list detail and adoption percentages before final manuscript. Companion files: prior_art_survey.md Category 4.1 + differentiation_vs_konrad_2601_18341 + differentiation_vs_he_msr2026 + Case Study 07 prevalence appendix.*
