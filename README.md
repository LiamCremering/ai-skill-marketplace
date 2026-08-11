# AI Skill Library

A curated library of AI agent skills, review tools, and productivity workflows for modern AI coding ecosystems.

This repository brings together practical capabilities across Claude Code, Codex, Cursor, GitHub Copilot, Greptile, Qodo, and related tooling. The goal is to provide a structured reference for understanding where a skill comes from, how it is installed, and what it is designed to help with in real-world development work.

## Repository structure

- `index.html` – static overview page for browsing the catalog in the browser
- `data/skills.json` – structured metadata for the skills and tools
- `README.md` – project overview and quick navigation

## Categories

### Context Shaping

- `grill-with-docs`
  - Purpose: Use this when you need to force the team to clarify scope, business goals, edge cases, and hidden assumptions before implementation begins. It helps reduce wrong building directions, vague specs, and rework caused by misunderstood intent.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `codebase-design`
  - Purpose: Use this to improve architecture quality before the codebase grows too much. It helps define module boundaries, interface contracts, seams for testing, and the right level of abstraction so the code stays maintainable.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `Architecture Designer`
  - Purpose: Use this when you are designing a new platform or service and need to think through trade-offs, dependencies, failure modes, and long-term maintainability. It helps structure system design discussions and document key architecture decisions.
  - Install: `/plugin marketplace add jeffallan/claude-skills`
  - Source: [jeffallan/claude-skills](https://jeffallan.github.io/claude-skills/skills/api-architecture/architecture-designer/)

- `/codex:adversarial-review`
  - Purpose: Use this as a critical reviewer to challenge assumptions, design choices, and implementation quality. It is especially useful when a plan looks good on paper but needs stress testing for hidden risks and weak trade-offs.
  - Install: `/plugin marketplace add openai/codex-plugin-cc`
  - Source: [openai/codex-plugin-cc](https://github.com/openai/codex-plugin-cc)

### Main Flow Shaping

- `/to-spec`
  - Purpose: Use this when a conversation or idea needs to be converted into a clear product or engineering specification. It reduces ambiguity and turns loose discussion into something that can be implemented and reviewed.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/to-tickets`
  - Purpose: Use this to break a large plan into small, actionable tickets with dependencies and blockers. It helps teams move from broad strategy into execution without losing context or sequencing.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/implement`
  - Purpose: Use this to move from a specification or ticket list to actual code changes. It is the execution-oriented workflow that transforms planning into delivery with a practical implementation loop.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/tdd`
  - Purpose: Use this when you want to drive implementation via tests first. It supports the red-green-refactor loop and helps keep features verifiable, smaller, and less error-prone.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `Qodo Code Review`
  - Purpose: Use this for repository-aware pull request review. It checks code quality, consistency, risk areas, and standards in the context of the actual codebase rather than only looking at a diff in isolation.
  - Install: create account and connect Git provider
  - Source: [Qodo docs](https://docs.qodo.ai/code-review)

- `GitHub Copilot Code Review`
  - Purpose: Use this when you want a quick review loop inside GitHub PRs. It gives code comments and repair suggestions while keeping the review process close to the actual pull request workflow.
  - Install: enable Copilot review in GitHub
  - Source: [GitHub docs](https://docs.github.com/en/copilot/concepts/agents/code-review)

### Upkeep

- `improve-codebase-architecture`
  - Purpose: Use this to spot structural pain points, duplicated logic, poor abstraction boundaries, or architectural drift. It helps keep a codebase healthy over time and reduces the risk of it becoming a hard-to-manage “ball of mud.”
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/security-review`
  - Purpose: Use this when you need a fast security-focused review of a code change or module. It is designed to catch common risks such as injection issues, unsafe handling of data, authentication and authorization weaknesses, and dependency problems.
  - Install: run `/security-review` in Claude Code
  - Source: [Claude Code docs](https://support.claude.com/en/articles/11932705-automated-security-reviews-in-claude-code)

- `Secure Code Guardian`
  - Purpose: Use this for design-time advice on secure coding patterns. It helps with authentication, authorization, validation, secret handling, OWASP concerns, and security headers before problems become production issues.
  - Install: `/plugin marketplace add jeffallan/claude-skills`
  - Source: [jeffallan/claude-skills](https://jeffallan.github.io/claude-skills/skills/security/secure-code-guardian/)

- `DeepSource`
  - Purpose: Use this as part of a quality and security pipeline. It provides ongoing static analysis, bug detection, vulnerability review, coverage insights, and compliance-oriented checks across the codebase.
  - Install: connect a Git provider in DeepSource
  - Source: [DeepSource docs](https://docs.deepsource.com/)

- `Trail of Bits Skills`
  - Purpose: Use this for deeper security research, vulnerability hunting, supply-chain risk analysis, and audit-style reviews. It is especially useful when you need a stronger, more focused security posture on critical parts of the system.
  - Install: `/plugin marketplace add trailofbits/skills`
  - Source: [trailofbits/skills](https://github.com/trailofbits/skills)

### Productivity

- `diagnosing-bugs`
  - Purpose: Use this when a bug is unclear or difficult to isolate. It guides a structured debugging loop: reproduce the issue, narrow it down, test a hypothesis, instrument the code, fix it, and confirm the regression is covered.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/codex:rescue`
  - Purpose: Use this when a task needs deeper investigation or a larger fix without losing momentum. It helps delegate complex debugging or recovery work to an AI agent while preserving a reviewable workflow.
  - Install: `/plugin marketplace add openai/codex-plugin-cc`
  - Source: [openai/codex-plugin-cc](https://github.com/openai/codex-plugin-cc)

- `Continue Agent Mode`
  - Purpose: Use this when you want an AI coding assistant that can work inside the IDE and operate with tool access. It is useful for change execution, debugging, and command-driven workflows in a more agentic development style.
  - Install: install Continue and switch to Agent mode
  - Source: [Continue docs](https://docs.continue.dev/ide-extensions/agent/quick-start)

- `check-pr`
  - Purpose: Use this to review pull requests for missing context, action items, incomplete descriptions, and failing checks before the merge is considered ready. It helps reduce review friction and avoid accidental low-quality merges.
  - Install: clone the Greptile skills repo and install the skill
  - Source: [greptileai/skills](https://github.com/greptileai/skills)

- `greploop`
  - Purpose: Use this when you want an iterative review loop: review, fix, re-review, and repeat until the issue is resolved or confidence is high. It is useful when you need a more systematic path to a clean result.
  - Install: clone the Greptile skills repo and install the skill
  - Source: [greptileai/skills](https://github.com/greptileai/skills)

- `Handoff`
  - Purpose: Use this to preserve context when a session needs to be resumed later by another agent or developer. It packages the current state into a concise transition artifact so work can continue without losing context.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `research`
  - Purpose: Use this when you need high-confidence answers grounded in trusted primary sources rather than assumptions. It is ideal for technical fact-finding, architecture decisions, or validating claims against current documentation.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

## Data file

The `data/skills.json` file contains structured metadata for each skill, including:

- category
- skill name
- ecosystem
- origin
- type (official vs community)
- installation instructions
- purpose

## Local preview

To view the HTML page locally:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Notes

This repository is intended as a practical shortlist and knowledge base for evaluating AI tooling, rather than a complete inventory of every available skill. It is designed to help teams and individuals quickly understand what a tool is for, where it comes from, and how it fits into a software engineering workflow.
