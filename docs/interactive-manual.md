# Interactive BMad Manual

Use this manual when you want fast, guided help from BMad agents. It focuses on high-level capabilities, the standard commands to activate them, and ready-to-run examples you can paste into your IDE chat. If you are new, start with the **Quick Start** and then try any example below.

---

## How to Use

1. **Open a fresh chat** with your IDE assistant (Claude Code, Cursor, Windsurf, or VS Code with web bundle).
2. **Load the BMad agent** for your task (most examples use the `BMM` agent). See the [IDE guides](./ide-info/) for loading instructions.
3. **Paste the example block** (including the triple backticks) to run the workflow.
4. **Review the generated plan** and follow prompts to iterate. Each example is scoped for <30 minutes of interactive time unless noted.

> Tip: Keep repos indexed so the agent can read your codebase. When in doubt, run `*workflow-init` first so BMad recommends the right track.

---

## What You Can Do (Top-Level Capabilities)

- **Bug fixes & quick features** — Rapid triage, minimal planning, code patching, and targeted tests.
- **Product & tech planning** — PRDs, technical specs, user stories, and architecture blueprints.
- **UX & game design** — Wireframe-quality flows, UI states, and gameplay loops with art direction notes.
- **Testing & QA** — Test plans, automated test generation, and gap analysis against requirements.
- **Brownfield modernization** — Dependency audits, refactors, dead code removal, and upgrade guides.
- **Creative ideation** — Story prompts, naming, copywriting, and brainstorming with the CIS module.
- **Custom agent building** — Craft bespoke agents and workflows via BMad Builder.
- **Web bundle usage** — Run BMad in ChatGPT, Claude Projects, or Gemini Gems without local install.

---

## Quick Start (One-Click)

Paste this to initialize a repo and get a tailored recommendation:

```
*workflow-init
```

---

## Guided Examples

Each example is copy-paste ready. Swap placeholders (like `<service>` or `<feature>`) with your details.

### 1) Lightning Bug Fix (<15 minutes)

```
*quick-fix
Goal: Resolve <bug> in <file/path> that <symptom>. Reproduce with: <command>. Add regression test and minimal docs.
```

- **When to use:** Small, localized bugs with a known repro path.
- **Outcome:** Patch, test, and brief changelog-ready summary.

### 2) Small Feature Ship (Tech Spec + Code)

```
*quick-spec-flow
Goal: Implement <feature> for <user persona>. Must touch <areas>. Provide a short spec, then produce code + tests.
Constraints: ship in one PR; prefer incremental commits.
```

- **When to use:** Minor features needing just enough planning to stay safe.
- **Outcome:** Lightweight spec, implementation plan, code, and tests.

### 3) Architecture Spike (Level 2)

```
*bmm-architecture
Context: We need an MVP design for <system/service>. Priorities: <scalability/perf/security>. Show 2 options with trade-offs and a recommended path. Produce component diagram + interface contracts.
```

- **When to use:** Exploring designs before committing to a build.
- **Outcome:** Comparative design note, diagrams, and interface stubs.

### 4) UX Flow + Wireframe Notes

```
*ux-designer
Product: <app/product> targeting <audience>. Screen set: <list screens>. Deliver user flows, state matrix, and wireframe notes with accessibility checks.
```

- **When to use:** Early UI/UX alignment without high-fidelity mockups.
- **Outcome:** Flow narrative, interaction states, and annotated layout guidance.

### 5) Test Coverage Rescue

```
*testarch-gap-analysis
Scope: <package/module>. Inputs: key requirements and current test files. Deliver missing test cases, risk ranking, and concrete test stubs (unit + integration) with fixtures.
```

- **When to use:** Raising confidence before refactors or releases.
- **Outcome:** Prioritized test backlog and starter code.

### 6) Brownfield Hardening (Dependencies + Refactor)

```
*brownfield-audit
Repo: <repo focus>. Goals: remove deprecated deps, modernize <framework/lib>, and cut dead code. Provide migration steps, risk callouts, and a staged refactor plan with checkpoints.
```

- **When to use:** Modernizing legacy sections without breaking production.
- **Outcome:** Audit summary, ordered refactor plan, and safety rails (tests + rollout steps).

---

## Tips for Faster Runs

- **Stay scoped:** One goal per chat keeps context tight and responses fast.
- **Confirm assumptions early:** Ask the agent to restate constraints before coding.
- **Prefer iterative commits:** Use small diffs; BMad workflows are tuned for incremental delivery.
- **Add repro commands:** The more precise the repro, the better the fix quality.
- **Ask for diffs:** Use `git diff --stat` or `git diff` prompts to keep changes reviewable.

---

## Where to Go Next

- **Workflow catalog:** Explore more commands in the [BMM workflows guide](../src/modules/bmm/workflows/README.md).
- **Customization:** Tune personalities and prompts via the [agent customization guide](./agent-customization-guide.md).
- **Web bundles:** Run BMad without local install using the [web bundler usage guide](./installers-bundlers/web-bundler-usage.md).
