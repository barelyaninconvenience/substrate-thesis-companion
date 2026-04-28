# MCP Setup Guide — Architecture, Roster, and Hygiene for AI-Augmented Personal Workflows
## Publishable variant · v1 · 2026-04-24

**Status:** First publishable extraction from a private MCP Setup Guide v2 deployed in personal practice. Strips practitioner-specific paths, credentials, and machine-specific configuration; keeps the architectural reasoning, roster recommendations, hygiene patterns, and one representative loose-tuning example so readers can adapt to their own contexts.
**Disclosure pattern:** General defaults + reasons-to-change-dials + one concrete loose-tuning example as benchmark + ecosystem-state note (April 2026). Per-deployer specifics (exact paths, exact credentials, exact tier composition) are deliberately left to the deployer.
**License:** MIT (intended).

---

## §1 — Why this guide exists

Model Context Protocol (MCP) is the standard interface for connecting AI assistants (Claude Code, Claude Desktop, increasingly other tools) to external systems — file systems, web APIs, databases, knowledge bases, browser automation. The protocol itself is well-documented; what's underdocumented is **how to architect a personal MCP roster that delivers value without overwhelming the assistant's context budget or creating unmanageable credential surface**.

This guide is the publishable extraction of one practitioner's MCP architecture after roughly nine months of iteration through pre-1.0 → 1.0 → governance-transferred ecosystem evolution. It's not a prescription — every deployer's context produces different optimal rosters. It's an architectural framework + a worked example.

The guide reflects the ecosystem state as of April 2026 (Linux Foundation MCP governance complete; workspace-level cache isolation default; code-execution-with-MCP available; ~50+ first-party MCP servers in widespread use). Specific tools recommended in the roster section will date faster than the architectural framework; the architectural framework is the durable contribution.

---

## §2 — What's changed in the ecosystem (since early 2026)

For practitioners returning to MCP after a several-month gap, the major shifts:

- **Governance** — Linux Foundation hosts the MCP specification + reference implementations as of late 2025; client-server compatibility is more reliable than the pre-LF era
- **Workspace cache isolation** — clients now isolate MCP server caches by workspace by default, preventing cross-workspace credential bleed (was a 2025 hygiene concern; resolved at protocol level)
- **Cache TTL** — most clients default to 1-hour cache TTL on MCP server lists; manual invalidation rare
- **Code-execution-with-MCP** — clients can execute arbitrary code provided by MCP servers within the assistant's tool-use loop; substantially expands what MCP servers can do but introduces new sandboxing considerations
- **Custom-stdio-wrapping pattern** — common pattern of wrapping HTTP-based APIs as local stdio MCP servers for better latency + credential hygiene; supersedes earlier direct-HTTP integration patterns
- **DPAPI (Windows) / Keychain (macOS) / Secret Service (Linux) credential storage** — credential management has converged on OS-native secret stores rather than plaintext config files

If your last MCP setup was before late 2025, expect to refactor along these axes when you next touch your roster.

---

## §3 — Architectural framing — three deployment scopes

MCP servers fit into three deployment scopes; each has different cost / hygiene / value characteristics. The framework distinguishes them explicitly because over-deploying at the wrong scope is the most common architectural mistake.

### Scope A — Always-on global

Servers loaded into the assistant on every session, regardless of project. Reserved for capabilities used in 80%+ of sessions. Reasonable default count: **3-5 servers maximum.**

Why the cap: every loaded MCP server consumes context budget on every turn (typically 500-2000 tokens in tool schemas per server). Five servers loaded at all times is roughly 5-10K tokens of permanent overhead; ten servers is 10-20K; twenty servers is 20-40K of context tax before any work happens.

Examples that justify always-on for most deployers: a filesystem server, a web-search server, a credential manager, occasionally a calendar/email server if the deployer's work substantially depends on those interfaces.

### Scope B — Project-scoped

Servers loaded only when working in a specific project directory. The deployer's MCP configuration includes per-project overrides that augment or override the global roster.

Why this scope matters: some servers are valuable in one or two projects but irrelevant elsewhere. A research-paper-search server in a humanities project; a database-query server in a data engineering project; a specialized API integration in a single client project. Project-scoping these means the schema-tax is paid only when working in the relevant project.

Reasonable count per project: **2-5 additional project-scoped servers** beyond the global roster.

### Scope C — Session-only / on-demand

Servers loaded only for specific sessions, manually toggled. Useful for capabilities that are valuable but used rarely (a financial-data API for monthly market spot-checks; a legal-document API for quarterly review).

This scope is underused. Most deployers default to Scope A (global) when Scope C (session-only) would suffice. Re-evaluating your global roster against the "used in 80%+ of sessions?" test typically moves several servers to Scope C, reducing global schema tax substantially.

---

## §4 — Tier framework for roster decisions

Beyond deployment scope, MCP servers fall into capability tiers. The framework recognizes four tiers based on operational maturity + integration depth.

### Tier 1 — Production-grade

First-party servers from major providers (Anthropic, OpenAI, GitHub, Google, etc.) with documented stability commitments + active maintenance. Suitable for global deployment if usage justifies.

### Tier 2 — Community-maintained but stable

Open-source MCP servers from active maintainers with public test suites + reasonable update cadences. Suitable for project-scoped or session-only deployment; deploy with awareness that breaking changes may happen on the maintainer's schedule.

### Tier 3 — Custom wrappers (deployer-built)

Servers the deployer builds to wrap specific APIs not yet covered by Tier 1/2 options. Common pattern: wrap an HTTP API as a local stdio MCP server using the deployer's preferred language. Useful for credential hygiene (keeps the API key on local disk via OS-native secret store, never sent to the assistant) and for latency (local stdio is faster than HTTP roundtrips).

### Tier 4 — Experimental / pre-1.0

Servers in active development by the deployer or the community. Useful for capabilities not yet stable elsewhere; expect breakage; budget time for re-integration when the underlying API changes.

**Reasons to deploy at higher tier vs lower:** Tier 1 minimizes maintenance overhead; Tier 3 maximizes credential control. Most practitioners' rosters end up mostly Tier 1 (for ubiquitous capabilities) + a few Tier 3 (for capabilities specific to the deployer's work). Tier 4 should be intentional and time-bounded.

---

## §5 — Recommended roster pattern (general)

The following is a structural pattern, not a specific roster. Specific tools change faster than the pattern.

**Always-on global (3-5 servers):**
- A filesystem server for working with files on local disk
- A web-search server (one of several available; choose based on search quality + provider trust)
- A credential manager that interfaces with your OS-native secret store
- Optional: an always-on calendar/email server if your work substantially depends on those

**Project-scoped (2-5 servers per active project):**
- Project-specific APIs (research databases, specialized data sources, internal tooling)
- Project-specific knowledge bases (vector stores; documentation indexes)
- Browser automation if the project involves substantial web interaction

**Session-only (deployed as needed):**
- Financial / market data APIs (used periodically, not continuously)
- Legal / compliance APIs (used during specific review cycles)
- Specialized analysis tools used for narrow purposes
- Exploratory MCP servers being evaluated for promotion

**Custom wrappers (Tier 3) — deployer-specific:**
- Any API the deployer uses regularly enough that credential hygiene + latency justify the wrapping work
- Common examples: research-paper APIs, content-management systems, analytics platforms

The roster shape will reflect the deployer's actual work. Don't copy other deployers' rosters; build your own from your actual usage patterns.

---

## §6 — Token tax considerations

The most under-attended cost dimension in MCP setup. Every loaded server consumes context budget per session.

**Rough estimates (April 2026):**
- A simple server with 5-10 tools: ~500-1000 tokens of schemas
- A moderate server with 20-30 tools: ~2000-4000 tokens
- A large server with 50+ tools: ~5000-10000 tokens
- A complex server with deeply-nested schemas: 10000-20000+ tokens

**Worst-case scenarios:** a deployer with 8-12 always-on servers, several with large tool counts, can easily reach 50-100K tokens of MCP schema overhead per session. On context windows of 200K-1M, this is meaningful budget loss.

**Mitigation patterns:**
- **Selective loading via deferred tools** — some clients support loading only the schemas you need on-demand rather than all schemas upfront. Where supported, this dramatically reduces schema tax.
- **Roster pruning** — re-evaluate your global roster quarterly. If a server hasn't been used in 30+ sessions, demote it from always-on to session-only.
- **Custom-wrapper consolidation** — instead of three separate Tier 3 wrappers each exposing 10 tools, consolidate into one wrapper exposing 25 tools with shared credential / connection handling.

**Loose tuning example (one practitioner's calibration):** 4 always-on global servers (filesystem + web-search + credential-manager + calendar) totaling ~6K schema tokens; project-scoped additions per project averaging 3-5 servers totaling ~5-10K additional tokens; total typical session schema tax ~10-20K tokens (1-2% of 1M context window).

---

## §7 — Skills vs MCPs (when to choose which)

A common architectural decision in 2026 deployments: should this capability be an MCP server, or a Skill (reusable prompt/document the assistant invokes via slash command or natural-language reference)?

**Choose MCP server when:**
- The capability needs to call external APIs / make HTTP requests / access databases
- The capability needs to write to external systems (not just read)
- The capability has a clear stable interface that benefits from typed schemas
- Multiple deployers would benefit from the same capability with different configurations

**Choose Skill when:**
- The capability is primarily prompt logic (specialized analysis steps; structured output formats; recurring workflows)
- The capability is highly deployer-specific (your particular writing style; your particular research methodology)
- The capability doesn't need external API access
- The capability is being iterated rapidly (Skills are faster to update than MCP servers)

**Hybrid pattern:** a Skill that invokes an MCP server. The MCP server handles the external interaction; the Skill provides the prompt logic that calls the server. This pattern is increasingly common for specialized workflows.

---

## §8 — Security and credential hygiene

The single most-violated MCP best practice: **credentials in plaintext config files**.

**Anti-patterns:**
- API keys directly in `.mcp.json` or equivalent config files (if the config is committed to git, the credential leaks; even if uncommitted, the credential is exposed to anything that reads the file)
- Credentials passed via environment variables exported in shell profiles (visible to any process; persists across sessions even after revocation)
- OAuth tokens stored in client-specific config formats that aren't backed by OS secret store

**Best practices:**
- Use OS-native secret stores (Windows Data Protection API; macOS Keychain; Linux Secret Service)
- Custom Tier 3 wrappers should fetch credentials from the secret store at startup, not embed them
- For OAuth tokens, use refresh-token flows that store only the refresh token in the secret store; access tokens stay in memory only
- For API keys, use stdio-wrapper pattern: the wrapper holds the key; the MCP protocol never carries it to the assistant
- Audit existing config files quarterly for plaintext credentials; migrate any found

**Loose tuning example:** one practitioner runs a quarterly credential audit script that scans MCP configs + application config directories for API-key-shaped strings; flags anything matching common credential patterns; deployer reviews each flag and migrates to secret store. The audit takes ~15 minutes per quarter and has caught multiple plaintext-credential creep cases that would otherwise have persisted.

---

## §9 — Custom MCP wrapper pattern (when Tier 1/2 doesn't cover your need)

When you need a capability not covered by available servers, the custom-wrapper pattern is increasingly the right move. General architecture:

**Components:**
- A small program (Python, Node.js, etc.) that implements the MCP protocol on stdio
- The program imports your preferred language's SDK for the target API
- Credentials fetched from OS secret store at program startup
- Tool schemas defined to match the capabilities you want exposed
- The program handles request/response translation between the MCP protocol and the target API

**Benefits over direct API integration:**
- Credentials stay on local disk, encrypted by OS secret store
- Latency is local stdio rather than HTTP round-trip per call
- The wrapper can implement caching, rate-limiting, retry logic outside the assistant's view
- The wrapper can sanitize / filter / transform API responses before returning them to the assistant
- The wrapper can compose multiple API calls into single MCP tool calls when the deployer's workflow benefits

**Effort estimate:** for an experienced developer, a wrapper for a moderate API (REST, OAuth or API-key auth, ~10-20 endpoints exposed as tools) takes ~4-8 hours to build + debug + integrate. The investment pays back if the API is used regularly; doesn't pay back for one-off needs.

**Loose tuning example (one practitioner's deployment):** roster includes Tier 3 wrappers for ~6 external services (research-paper search, structured-data store, local LLM gateway, document-extraction service, workflow automation, content-generation tooling). Each wrapper required 4-12 hours upfront; collectively saves substantial time per week vs the direct-HTTP-from-assistant alternative; centralized credential handling means quarterly key rotation touches the wrappers' secret-store entries rather than dozens of config files.

---

## §10 — Migration patterns (v1 → v2 of your own MCP setup)

Practitioners revisiting their MCP setup after several months typically face a refactor. Recommended pattern:

**Phase 1 — Audit current state.** List all MCP servers currently configured (global + project-scoped + session-only). For each: when was it last actually used? How much schema tax does it carry? Where are its credentials stored?

**Phase 2 — Score against current best practices.** For each server, score: does it justify always-on deployment? Are credentials in OS secret store? Is the schema tax proportionate to value delivered?

**Phase 3 — Demote, decompose, deprecate.** Servers that fail the always-on test → demote to project-scoped or session-only. Servers with plaintext credentials → migrate to secret store. Servers no longer needed → deprecate (don't delete; archive in case you need them later).

**Phase 4 — Identify gaps for custom wrappers.** What capabilities do you currently route through ad-hoc tooling that would benefit from MCP integration? These are the candidates for new Tier 3 wrappers.

**Phase 5 — Documented end-state.** Write down the resulting roster + rationale per server. Future-you will thank present-you when next-quarter's audit fires.

**Loose tuning example:** one practitioner's pre-2026-Q2 roster had 7 servers in `~/.mcp.json` with three issues — a triple-duplicate server entry across three config files, one plaintext credential, and one server with substantially more schema tax than its usage frequency justified. The migration moved the duplicates to single canonical entry, migrated the plaintext credential to secret store, and demoted the high-tax server from global to session-only. Total migration time: ~3 hours including testing.

---

## §11 — Troubleshooting patterns

The most common failure modes practitioners hit:

**Server fails to start at session-open:** usually credential issue or path mismatch. Check secret-store contains required credential; check working directory matches what the server expects.

**Server starts but tools don't appear in assistant:** usually schema validation issue. Check server's response to the protocol's `tools/list` request; verify schemas conform to MCP spec.

**Server responses are slow:** usually upstream API latency (especially for HTTP-based servers without caching). Consider Tier 3 wrapper with caching layer, or session-only deployment for latency-sensitive sessions.

**Multiple clients see different MCP rosters:** usually configuration confusion across client-specific config files. Each client (Claude Code, Claude Desktop, IDE extensions) reads from its own config; consolidating onto a shared `~/.mcp.json` where supported reduces drift.

**OAuth tokens expire mid-session:** usually refresh-token logic missing in the server. Implement refresh-token flow in the server, or restart the server when tokens expire.

**Schema tax suddenly increases:** usually a server was added without considering its schema cost, or a server's underlying API added many new endpoints. Audit the largest schema-cost servers; demote or refactor.

---

## §12 — What this guide does NOT cover

For honest scope:

- **Specific tool recommendations.** Tools mentioned in the roster section are illustrative, not endorsements. The MCP ecosystem is evolving rapidly; consult current sources for specific tool selection.
- **Specific configuration syntax.** Different MCP clients (Claude Code, Claude Desktop, IDE extensions) use different config formats. The architectural patterns are client-independent; specific syntax is client-specific.
- **Multi-deployer / team configuration.** This guide addresses personal MCP setup. Team-scale deployments add coordination dimensions (shared credentials handling, role-based access, deployment cadences) not addressed here.
- **MCP protocol implementation details.** The MCP specification is the authoritative reference. This guide is about how to architect with MCP, not how MCP works internally.
- **Specific provider pricing.** API costs (Anthropic, OpenAI, Google, etc.) for the assistants consuming the MCP roster are out of scope. Budget per-provider separately.

---

## §13 — Summary

A well-architected personal MCP setup follows a small set of structural principles:

1. **Three deployment scopes** (always-on global / project-scoped / session-only); over-deployment at the wrong scope is the most common architectural mistake
2. **Four capability tiers** (production / community-stable / custom-wrapper / experimental); deploy at the appropriate tier for your use case
3. **Token tax discipline** — every loaded server consumes context budget on every session; quarterly roster pruning maintains efficiency
4. **OS-native credential storage** — never plaintext in config files; migrate any found at quarterly audit
5. **Custom-wrapper pattern** for capabilities specific to your work that don't yet have Tier 1/2 alternatives; saves credential and latency overhead vs direct HTTP
6. **Skills vs MCPs decision** — choose based on whether the capability needs external interaction (MCP) or is primarily prompt logic (Skill)
7. **Quarterly migration cycles** — the ecosystem evolves quickly; a roster that worked nine months ago may have better current alternatives

This document is the publishable extraction; the practitioner's private guide includes specific paths, credentials, and machine-specific configuration not appropriate for general distribution. Take what serves you. Adapt the rest.

---

*MCP Setup Guide publishable variant v1 · 2026-04-24 · Reflects ecosystem state April 2026 (Linux Foundation governance complete; workspace cache isolation default; code-execution-with-MCP available; ~50+ first-party servers in widespread use). Strips practitioner-specific paths/credentials/machine-specific configuration; keeps architectural framework + reasoning patterns + one representative loose-tuning example as benchmark. Subject to revision as ecosystem evolves. Companion to Substrate Thesis Companion repository (github.com/barelyaninconvenience/substrate-thesis-companion). MIT license intended.*
