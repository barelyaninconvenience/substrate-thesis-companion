# Operating Stack — A Framework for Per-Task Cost-and-Configuration Reasoning in AI-Augmented Knowledge Work
## Publishable variant · v1 · 2026-04-24

**Status:** First publishable extraction from a private Operating Stack v1.3.1 deployed in personal practice. Strips practitioner-specific paths, credentials, and dollar amounts; keeps the structural framework, reasoning patterns, and a representative loose-tuning example so readers can adapt to their own contexts.
**Disclosure pattern:** General defaults + reasons-to-change-dials + one concrete loose-tuning example as benchmark + multiplicative cost framework. Per-deployer specifics (exact thresholds, exact budgets, exact tool integrations) are deliberately left to the deployer.
**License:** MIT (intended).

---

## §1 — Why an Operating Stack exists

Knowledge work mediated by AI assistants — coding agents, research assistants, writing collaborators — has variable cost per task. The same prompt to the same model can cost two-orders-of-magnitude more or less depending on configuration: how much reasoning effort is invoked, how verbose the output, how many tool calls allowed, whether agents are dispatched in parallel, how the agents are briefed, and a half-dozen additional dimensions practitioners rarely think about explicitly.

Most practitioners learn this implicitly through bills + frustration. They calibrate by accident: a session blew the budget; they tighten next time. A session under-delivered; they loosen.

The Operating Stack is the explicit alternative. It names the dimensions that drive cost; it provides a default configuration per task class; it specifies when (and why) to deviate from the default; it makes the cost reasoning legible.

This document is the publishable extraction of one practitioner's Operating Stack after roughly six weeks of deliberate calibration. It's not a prescription — every deployer's context produces different optimal calibrations. It's a structural framework + a worked example.

---

## §2 — Task classification taxonomy

The first decision before configuring anything is: what kind of task is this? The framework recognizes six classes, each with substantially different optimal configurations:

| Class | Description | Typical configuration tendency |
|---|---|---|
| **Reasoning-heavy** | Deep analysis, decision-making under uncertainty, novel problem-solving | High effort, structured-verbose, fewer tool calls per turn |
| **Mechanical** | Refactors, format conversions, deterministic transforms | Low-medium effort, terse output, more tool calls allowed |
| **Retrieval** | Finding specific facts, locating files, citation gathering | Medium effort, terse output, many tool calls allowed |
| **Measurement** | Verifying claims, running tests, collecting metrics | Medium effort, terse output, agent-dispatch favored for parallelism |
| **Creative** | Writing, design, ideation | Medium-high effort, verbose output, fewer tool calls |
| **Adversarial** | Red-teaming, finding failure modes, falsification attempts | High effort, structured-verbose, role-cast agent often favored |

The taxonomy is descriptive, not prescriptive. The point is to *name* the task class explicitly before configuring. Misclassification (treating a reasoning-heavy task as mechanical, treating a creative task as retrieval) is the most common source of cost surprise.

**Reason to change dials per class:** if the default configuration for a class isn't producing the expected output quality, the framework predicts the misfit is configurational, not skill-based. Re-tune the dials before changing models or escalating effort.

---

## §3 — Effort × Verbosity matrix

Two dials drive most cost variance. Effort governs how much reasoning the model invokes per response; verbosity governs how much output it produces.

| | Terse | Structured-verbose | Open-verbose |
|---|---|---|---|
| **Low effort** | Cheapest. Mechanical refactors. | Mismatched (output overhead without reasoning depth). | Wasteful. |
| **Medium effort** | Retrieval, simple measurement. | Most working configurations. | Creative drafting where exploration matters. |
| **High effort** | Compressed reasoning artifacts (rare). | Reasoning-heavy analysis, decision-making. | Adversarial sweep, novel problem-solving. |
| **Extra-high effort** | Almost never useful. | Pre-decision adversarial sweeps. | Supermax (earned, not default). |

**Reasons to change dials:** every notch up on either dial multiplies cost. The default working configuration for most knowledge work is **medium effort + structured-verbose**. Move to high effort when the task class requires it (reasoning-heavy, adversarial). Move to terse when the output is for code/automation rather than human consumption.

**Concrete loose tuning example (one practitioner's calibration):** Default configuration for routine sessions = medium effort + structured-verbose. Reserve high effort for explicit decision points or novel problem-solving. Reserve extra-high (supermax) for pre-irreversibility-commit adversarial sweeps. Most days never trigger the higher tiers; budgets remain well within sustainable ranges.

---

## §4 — Per-agent tier policy

When dispatching subagents (specialized agents handling discrete tasks within a larger workflow), each agent inherits a tier that bounds its configuration. A reasonable starting policy:

| Tier | Use case | Typical effort × verbosity |
|---|---|---|
| **Critical** | Decisions touching irreversibility, security, or financial commitment | High × structured-verbose |
| **Standard** | Routine analytical work, code review, content drafting | Medium × structured-verbose |
| **Light** | Mechanical lookups, format conversions, status checks | Low × terse |

**Reasons to change tiers per agent:** the tier represents the *minimum* configuration the agent needs to produce useful output. Under-tiering (assigning standard work to a light agent) produces shallow output that requires re-work. Over-tiering (assigning light work to a critical agent) wastes budget and produces output more elaborate than the work warrants.

**Concrete loose tuning example:** A practitioner-deployed agent fleet of ~26 specialized agents settled into roughly 7 critical / 16 standard / 3 light after iteration. The ratio reflects the deployer's actual work distribution; other deployers should expect different ratios.

---

## §5 — Parallelism cost profiles

Multi-agent dispatch changes cost in non-linear ways. The framework tracks parallelism as one of several cost dimensions because it interacts with brief-permissiveness in particular.

**Decision-support framing (not caps):**
- 1 agent: baseline cost; full briefing usable
- 2-3 agents: ~2-3× baseline; briefs should be tightened to bounded scope
- 4-6 agents: ~4-6× baseline; briefs should be substantially bounded; coordination overhead emerges
- 7+ agents: ~7+× baseline plus substantial coordination overhead; reserve for pre-decision adversarial sweeps where breadth justifies the cost

**Reasons to change dials on parallelism:** parallelism is most useful when the work decomposes cleanly into independent sub-tasks. If the sub-tasks coordinate (one agent's output feeds another), parallelism breaks; serialize. If the sub-tasks are genuinely independent (multiple files to audit; multiple sources to query), parallelism compounds value.

**Anti-pattern to avoid:** high parallelism + open-ended briefs. The combination produces sprawling agent work that exceeds budget without producing focused output. The framework calls this the "runaway regime" — most cost surprises come from this combination.

---

## §6 — Topic complexity gradient

A discovered cost dimension: tasks that span more topical scope cost more per response than narrowly-scoped tasks at the same effort × verbosity. Multiple topics in one task force the model to maintain more context per response.

**Loose tuning:** when a task spans 3+ distinct topics, the configurational default should shift toward bounded briefs (give each topic explicit scope) and serialized execution (one topic per agent, then synthesize) rather than parallel multi-topic agents.

**Anti-pattern:** asking one agent to "look at all the issues" across multiple unrelated areas. The agent's context budget gets distributed thinly; output quality degrades; cost increases.

---

## §7 — Role-composition rules (when dispatching multiple agents on the same problem)

When dispatching multiple agents on the same problem, role composition matters. The framework recognizes a particular role-cast pattern as load-bearing for adversarial work:

**Default for routine multi-agent dispatch:** roles are differentiated by domain (one agent for security review, one for documentation review, one for test coverage). Each agent has clear non-overlapping scope.

**For adversarial / pre-decision sweeps:** include an explicit "skeptic" role whose job is to attack the proposed direction, not to support it. Without an adversarial role, multi-agent sweeps produce convergent agreement that may reflect coordination rather than analytical merit.

**Reasons to change role composition:** if a multi-agent sweep produces unanimous agreement and the decision is reversible, the unanimous agreement is probably fine. If the decision is irreversible, the unanimous agreement is suspicious — there should have been at least one credible objection raised + addressed.

---

## §8 — Cost annotation discipline

Whatever framework you adopt, annotate cost reasoning where decisions are made. Future-you (or other readers) will need to understand why specific configurations were chosen.

**Practical convention:** at the point of dispatching an agent or invoking a higher-effort configuration, leave a brief comment noting the task class, the configuration chosen, and the cost-reasoning. Format suggestion: `[L-01 medium / L-02 structured-verbose / L-05 1 agent / L-06 bounded brief / cost ~Xk tokens — reason: <one sentence>]`.

**Why this matters:** without annotation, configuration choices look arbitrary in retrospect. With annotation, patterns emerge: which configurations consistently work; which configurations consistently waste; what task classes have been mis-classified. The annotation discipline is the data layer that enables calibration.

---

## §9 — Brief-writing discipline

The brief (the agent's task description) is the most under-attended cost dimension. Briefs that are too open invite sprawling work. Briefs that are too narrow produce mechanical output without judgment.

**Default:** structured + bounded. Specify what's in scope, what's out of scope, what success looks like, what to do if the agent encounters something unexpected.

**Reasons to change brief shape:** for genuinely exploratory tasks (you don't know what you're looking for), open briefs are appropriate. For known-shape tasks (you know what kind of output you need), bounded briefs are appropriate. Misuse in either direction wastes cost.

**Anti-pattern:** "look at this and tell me what you think" with no scope. Predictably produces sprawling output that touches multiple unrelated topics shallowly.

---

## §10 — Multiplicative cost framework

The Operating Stack's quantitative core. Cost per task is multiplicative across dimensions, not additive. Small increases on multiple dimensions compound.

**Cost = effort × verbosity × parallelism × tool-use × topic-complexity × brief-permissiveness × role-cost × output-volume**

Roughly speaking:
- Each "effort" notch ≈ 1.5× to 3× cost
- Each "verbosity" notch ≈ 1.15× to 1.5× cost
- Each additional agent ≈ +1× cost (roughly linear) plus coordination overhead
- Open-ended brief vs bounded brief ≈ 1.4× cost
- Open-ended topic vs single-topic ≈ 1.3× cost

**Why multiplicative matters:** moving two dials from "default" to "elevated" doesn't add the costs; it multiplies them. A reasoning-heavy task at high effort × structured-verbose × 2 agents × bounded brief is roughly 6-8× a baseline task. A reasoning-heavy task at extra-high effort × open-verbose × 4 agents × open brief is roughly 50-100× a baseline task.

**Practical calibration:** track per-task token spend across a few weeks; back-fit the multipliers to your observed cost. The exact numbers will differ per deployer; the multiplicative structure holds.

---

## §11 — Plank-by-plank viability math

Beyond per-task cost, the framework includes a session-level viability check: at any moment in the session, what's the running total cost relative to the session budget?

**The check:** at the point of considering a new dispatch or higher-effort invocation, compute the projected cost; verify the session can absorb it; verify the work justifies the spend.

**Three viability questions per dispatch:**
1. **Affordability:** does the session budget have headroom for this dispatch's projected cost?
2. **Earned cost:** does the dispatch's information value justify the spend, given alternatives at lower configurations?
3. **Coupling:** would this dispatch combined with already-pending work push the session into the runaway regime (high parallelism × open briefs simultaneously)?

If any answer is no, configure differently. The plank-by-plank discipline prevents single-decision cost surprises from compounding into session-level budget breaks.

---

## §12 — Decision reasoning flow

When configuring a new task, the framework recommends a structured reasoning flow:

1. **Classify** the task (Section 2)
2. **Assess irreversibility** (reversible / near-reversible / irreversible / multi-year-shadow)
3. **Assess information posture** (do I have priors? are the priors directional? are they suspect?)
4. **Assess time posture** (this-session / 72hr / 2-4wk / 6mo+)
5. **Assess budget posture** (window-available / cap-proximate / lockout)
6. **Compose configuration** (effort × verbosity × parallelism × tool-use × brief-permissiveness from the dimensions above)
7. **Estimate cost** (multiplicative framework, Section 10)
8. **Verify viability** (plank-by-plank check, Section 11)

**Why the flow matters:** without structured reasoning, configurations get chosen by recent-experience heuristics. With it, each task gets an explicit reasoning trail that's auditable in retrospect.

---

## §13 — Lessons learned catalog

The framework develops by encoding what's been learned through cost surprises. A representative catalog of lessons (from one practitioner's six-week calibration):

- **L-1 — Wall-clock time is not session cost.** A long session with low-throughput work costs less than a short session with multi-agent dispatch. Calibrate by token spend, not minutes elapsed.
- **L-2 — Re-using prior context is cheap; loading new context is expensive.** Sessions that build on prior session's artifacts cost less than sessions that orient from scratch.
- **L-3 — Verbosity floors are real.** Below a verbosity threshold, output quality collapses; the model can't fit the necessary structure into the available output budget.
- **L-4 — Effort ceilings are also real.** Above an effort threshold, marginal improvements don't justify cost; sometimes the model just doesn't have additional reasoning to deliver on a question.
- **L-5 — Parallelism without bounded briefs is the canonical cost surprise.** Almost every "session blew the budget" event traces to high parallelism + open briefs.
- **L-6 — Adversarial roles are load-bearing for irreversible decisions.** Multi-agent sweeps without adversarial roles produce false confidence.
- **L-7 — Mechanical work doesn't need reasoning effort.** Wasting high-effort configurations on mechanical tasks is the second-most-common cost surprise.
- **L-8 — Brief-writing time pays itself back.** Five minutes spent writing a tight brief saves 20 minutes of agent re-work.
- **L-9 — Cost annotation enables calibration.** Without per-decision annotation, calibration is folk wisdom; with it, calibration is empirical.
- **L-10 — The runaway regime is asymptotic.** Once you're in it, escalating doesn't help; the cost-to-value ratio collapses. Best to abort, reconfigure, restart.

The catalog grows with experience. Encode lessons as they're discovered.

---

## §14 — Anti-patterns

The most common mistakes the framework helps avoid:

- **Default-effort drift:** the deployer's "default" creeps higher over time without explicit decision; budgets grow accordingly.
- **Parallelism-as-default:** dispatching multiple agents because parallelism feels productive, not because the work decomposes cleanly.
- **Open-brief habituation:** the deployer stops writing tight briefs because the model usually figures it out; eventually the model doesn't, and the cost surprise lands.
- **Tool-use inflation:** allowing more tool calls per turn than the task warrants; the agent does extra work without producing better output.
- **Convergent role composition:** dispatching multiple agents that all share supportive frames; missing the adversarial perspective.
- **Multi-topic single-agent:** asking one agent to handle several topics; output quality degrades thin.
- **Annotation skipping:** running configurations without leaving cost-reasoning notes; foreclosing future calibration.

Each anti-pattern has a name. Each has a specific mitigation. The framework's diagnostic value comes from being able to recognize the pattern when it surfaces.

---

## §15 — Adoption path

How to start using this framework if you're new to it:

**Week 1:** annotate cost reasoning at every dispatch. You don't need to change any configurations yet; just leave the notes. Pattern-matching emerges naturally.

**Week 2:** classify task type at every dispatch (Section 2). Notice when the classification is hard; those are the tasks worth thinking about.

**Week 3:** introduce the explicit decision reasoning flow (Section 12). Walk through it before higher-cost dispatches.

**Week 4:** check plank-by-plank viability (Section 11) before any dispatch above your routine cost band.

**Months 2-3:** back-fit the multiplicative cost framework (Section 10) to your observed token spend. Your specific multipliers will be different from anyone else's; calibrate to your context.

**Months 4-6:** develop your own lessons-learned catalog (Section 13). Encode what costs surprised you and why; encode what configurations consistently delivered.

**Months 6+:** the framework becomes habitual. Cost reasoning happens implicitly; explicit annotation becomes the exception (for unusual configurations) rather than the rule.

---

## §16 — What this document does NOT cover

For honest scope:

- **Specific dollar costs.** Per-token costs vary substantially by model and provider; the framework's structure is provider-independent. Apply your own provider's pricing to get dollar estimates.
- **Specific tool/agent integrations.** The framework treats agents as a generic capability; specific integration with Claude Code / Cursor / specialized tooling requires deployer-specific configuration not included here.
- **Specific calibrated thresholds.** This document gives ranges + reasons-to-change-dials; specific thresholds (effort cutoffs, verbosity ceilings, parallelism caps) are deployer-specific. The framework helps you find your own thresholds; it doesn't impose mine.
- **Multi-deployer coordination.** This is a personal Operating Stack. Team-scale cost-and-configuration reasoning has additional dimensions (shared budget allocation, role coordination across team members) not addressed here.

---

## §17 — Summary

The Operating Stack is a structural framework for reasoning about per-task cost and configuration in AI-augmented knowledge work. Its core claims:

1. **Cost is multiplicative across dimensions** (effort, verbosity, parallelism, tool-use, brief-permissiveness, role-cost, topic-complexity, output-volume); naive escalation on multiple dimensions compounds quickly.
2. **Most cost surprises come from a small set of named anti-patterns** (parallelism + open briefs being the most common); recognizing the patterns enables avoidance.
3. **Per-task structured reasoning is cheap; cost surprises are expensive**; the upfront investment in classification + configuration + viability check pays back.
4. **Calibration is empirical**, not a priori; deployer-specific thresholds emerge from per-decision annotation across weeks of practice.
5. **The framework's diagnostic value matters more than its prescriptive value**; recognizing what configuration mistake produced a bad outcome is what enables fixing it.

This document is the publishable extraction; the framework's deeper material lives in the practitioner's private Operating Stack v1.3.1 and continues to evolve with practice. Take what serves you. Adapt the rest.

---

*Operating Stack publishable variant v1 · 2026-04-24 · Strips practitioner-specific paths/credentials/dollar-amounts; keeps structural framework + reasoning patterns + one representative loose-tuning example as benchmark. Subject to revision based on reader feedback. Companion to Substrate Thesis Companion repository (github.com/barelyaninconvenience/substrate-thesis-companion). MIT license intended.*
