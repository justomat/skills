# Agent Skills by Geraldi (@justomat)

A curated collection of modular, production-tested [Agent Skills](https://agentskills.io) for AI coding assistants (Claude Code, Cursor, Antigravity, Codex, OpenCode, and any tool implementing the [Agent Skills Specification](https://agentskills.io/specification)).

Designed for high-autonomy agents, rigorous engineering standards, verified diffs, and low-slop communication.

---

## ⚡ Quick Installation

Install any or all skills using the open `skills` CLI:

```bash
# Install all skills globally
npx skills add justomat/skills -g

# Install into the current project only
npx skills add justomat/skills

# Install specific skills
npx skills add justomat/skills --skill poteto-mode technical-writing unslop

# List available skills without installing
npx skills add justomat/skills -l
```

### Supported Agents

Works out of the box with any tool compliant with the [Agent Skills specification](https://agentskills.io/specification), including:
- **Claude Code** (`~/.claude/skills/` or `~/.agents/skills/`)
- **Antigravity / agy** (`~/.gemini/antigravity-cli/skills/` or `~/.agents/skills/`)
- **Cursor** (`.cursor/skills/` or global)
- **Codex CLI / Copilot** (`~/.codex/skills/`, `~/.copilot/skills/`)
- **OpenCode** (`~/.config/opencode/skills/`)

---

## 📚 Skill Catalog

### 🧠 Principles & Software Craftsmanship
Universal principles that sharpen model decision-making before and during implementation.

| Skill | Description |
|---|---|
| [`principle-boundary-discipline`](skills/principle-boundary-discipline/SKILL.md) | Separate public contracts from internal mechanics; parse at boundaries. |
| [`principle-build-the-lever`](skills/principle-build-the-lever/SKILL.md) | Build the tool, codemod, or script that performs or proves non-trivial work instead of hand editing. |
| [`principle-encode-lessons-in-structure`](skills/principle-encode-lessons-in-structure/SKILL.md) | Turn recurring instructions or corrections into lints, types, or runtime checks. |
| [`principle-exhaust-the-design-space`](skills/principle-exhaust-the-design-space/SKILL.md) | Prototype competing options side-by-side for novel architecture or UI choices. |
| [`principle-experience-first`](skills/principle-experience-first/SKILL.md) | Prioritize end-user delight and polish over implementation convenience. |
| [`principle-fix-root-causes`](skills/principle-fix-root-causes/SKILL.md) | Trace symptoms to real roots; avoid nil-check guards that silence bugs. |
| [`principle-foundational-thinking`](skills/principle-foundational-thinking/SKILL.md) | Get core types, concurrent actor boundaries, and data structures right first. |
| [`principle-guard-the-context-window`](skills/principle-guard-the-context-window/SKILL.md) | Offload bulk payloads to subagents; keep summaries in main context. |
| [`principle-laziness-protocol`](skills/principle-laziness-protocol/SKILL.md) | Bias toward minimal diffs, zero dead weight, and deleting unnecessary abstractions. |
| [`principle-make-operations-idempotent`](skills/principle-make-operations-idempotent/SKILL.md) | Ensure lifecycle steps converge to the same state across crashes and retries. |
| [`principle-migrate-callers-then-delete-legacy-apis`](skills/principle-migrate-callers-then-delete-legacy-apis/SKILL.md) | Migrate callers and remove deprecated APIs in one atomic pass. |
| [`principle-minimize-reader-load`](skills/principle-minimize-reader-load/SKILL.md) | Reduce mental hops between questions and answers; collapse single-caller wrappers. |
| [`principle-model-the-domain`](skills/principle-model-the-domain/SKILL.md) | Encode business concepts as explicit types and structures rather than scattered conditionals. |
| [`principle-never-block-on-the-human`](skills/principle-never-block-on-the-human/SKILL.md) | Run reversible actions autonomously and present results for fast human feedback. |
| [`principle-outcome-oriented-execution`](skills/principle-outcome-oriented-execution/SKILL.md) | Drive directly toward the target architecture without throwaway transitional code. |
| [`principle-prove-it-works`](skills/principle-prove-it-works/SKILL.md) | Verify against actual artifacts, live outputs, and real runs—never assume "it compiles." |
| [`principle-redesign-from-first-principles`](skills/principle-redesign-from-first-principles/SKILL.md) | Integrate new requirements as if they were day-one requirements. |
| [`principle-separate-before-serializing-shared-state`](skills/principle-separate-before-serializing-shared-state/SKILL.md) | Eliminate shared state across concurrent actors before introducing locks or queues. |
| [`principle-sequence-verifiable-units`](skills/principle-sequence-verifiable-units/SKILL.md) | Break multi-step tasks into self-verifying, reviewable milestone commits and PRs. |
| [`principle-subtract-before-you-add`](skills/principle-subtract-before-you-add/SKILL.md) | Remove obsolete code and dead paths before building new capabilities. |
| [`principle-type-system-discipline`](skills/principle-type-system-discipline/SKILL.md) | Make invalid states unrepresentable using strict branded types and exhaustive guards. |

---

### 🚀 Autonomous Execution & Orchestration
High-leverage workflows for unattended or coordinated agent runs.

| Skill | Description |
|---|---|
| [`poteto-mode`](skills/poteto-mode/SKILL.md) | Complete agent operating style: deliberate subagents, playbooks, unslopped prose, verified work. |
| [`arena`](skills/arena/SKILL.md) | Run competitive solution branches and pick the optimal implementation. |
| [`automate-me`](skills/automate-me/SKILL.md) | Identify repetitive workflows and convert them into automated scripts or skills. |
| [`figure-it-out`](skills/figure-it-out/SKILL.md) | Autonomous problem-solving protocol when facing ambiguity or obscure errors. |
| [`recall`](skills/recall/SKILL.md) | Reconstruct recent working context, live state, and unresolved tasks before starting work. |
| [`reflect`](skills/reflect/SKILL.md) | Multi-perspective retrospective across transcripts to capture actionable learnings. |
| [`show-me-your-work`](skills/show-me-your-work/SKILL.md) | Generate a structured decision log (TSV) documenting every tradeoff and verification step. |
| [`swarm`](skills/swarm/SKILL.md) | Fan out N parallel worker agents to explore or test across large surfaces simultaneously. |

---

### 🔥 Grilling & Stress-Testing
Relentless plan grilling and domain modeling patterns (adapted from Matt Pocock).

| Skill | Description |
|---|---|
| [`grilling`](skills/grilling/SKILL.md) | Grill the user relentlessly about a plan, decision, or architecture tree until every branch is resolved. |
| [`grill-me`](skills/grill-me/SKILL.md) | Quick invocation for the grilling interview to stress-test your thinking. |
| [`grill-with-docs`](skills/grill-with-docs/SKILL.md) | Relentless interview that concurrently produces ADRs and domain glossaries. |
| [`domain-modeling`](skills/domain-modeling/SKILL.md) | Actively build and sharpen a project's domain glossary (`CONTEXT.md`) and ADRs. |

---

### 🏗 Architecture, Investigation & TypeScript
Tools for understanding systems, probing history, and crafting robust code.

| Skill | Description |
|---|---|
| [`architect`](skills/architect/SKILL.md) | Sketch types, interfaces, and module structure before writing implementation code. |
| [`how`](skills/how/SKILL.md) | Deep trace of runtime behavior, control flows, and state lifecycles. |
| [`why`](skills/why/SKILL.md) | Archeological deep-dive into git history, PRs, issues, and incident rationale. |
| [`interrogate`](skills/interrogate/SKILL.md) | Methodically cross-examine requirements and code boundaries to uncover hidden assumptions. |
| [`typescript-best-practices`](skills/typescript-best-practices/SKILL.md) | Production patterns, strict typing rules, and performance guidelines for TypeScript. |

---

### 🧪 Verification & Quality Control
Ensuring correctness and regression prevention.

| Skill | Description |
|---|---|
| [`pstack-tdd`](skills/pstack-tdd/SKILL.md) | Targeted test-driven development loop for regression tests and critical logic. |
| [`blast-radius`](skills/blast-radius/SKILL.md) | Calculate downstream impact and potential breakage across callers before refactoring. |
| [`create-verification-skill`](skills/create-verification-skill/SKILL.md) | Author reusable verification scripts and harnesses for complex feature checks. |
| [`maintain-verification-skill`](skills/maintain-verification-skill/SKILL.md) | Keep automated verification suites and checks up to date as systems evolve. |

---

### 🛠 Tools & Agent Managers
Direct agent harnesses and integrations.

| Skill | Description |
|---|---|
| [`antigravity-manager`](skills/antigravity-manager/SKILL.md) | Guide Claude Code to orchestrate the Antigravity CLI (`agy`) as an autonomous worker. |
| [`pi-manager`](skills/pi-manager/SKILL.md) | Direct the `pi` coding-agent harness with pinned model selection and execution flags. |
| [`biznetgio`](skills/biznetgio/SKILL.md) | Manage Biznet Gio cloud infrastructure (metal, VMs, storage, IPs) via CLI. |
| [`tiktok-business-messaging`](skills/tiktok-business-messaging/SKILL.md) | End-to-end integration with TikTok Business API (DMs, webhooks, auth, media). |
| [`plannotator-compound`](skills/plannotator-compound/SKILL.md) | Deep analysis of Plannotator plan archives to improve future prompt and planning accuracy. |
| [`make-bot-ui`](skills/make-bot-ui/SKILL.md) | Scaffold webhook-triggered web interfaces to wake bots with JSON payloads. |
| [`setup-pstack`](skills/setup-pstack/SKILL.md) | Configure model assignments per role and workload. |

---

### ✍ Writing & Communication
Ensuring clean, concise, and noise-free documentation and code.

| Skill | Description |
|---|---|
| [`technical-writing`](skills/technical-writing/SKILL.md) | Diátaxis structure, Google developer style, STE instruction rules, and Global English syntax. |
| [`unslop`](skills/unslop/SKILL.md) | Eliminate AI tropes, buzzwords, filler phrases, and unnecessary hedges. |
| [`teach`](skills/teach/SKILL.md) | Synthesize `how` and `why` into clear, intuitive explanations for humans. |
| [`no-comments`](skills/no-comments/SKILL.md) | Write self-explanatory code without noisy, obvious inline comments. |
| [`bro`](skills/bro/SKILL.md) | Direct, informal, high-signal peer programming tone. |

---

## 🔍 Validation

Every skill in this repository is 100% compliant with the [Agent Skills Specification](https://agentskills.io/specification). Validate locally with `skills-ref`:

```bash
# Validate a specific skill
npx skills-ref validate skills/poteto-mode

# Validate all skills
bun run validate
# or
npm run validate
```

---

## 📄 License

[MIT](LICENSE) © [Geraldi Sutanto](https://github.com/justomat)
