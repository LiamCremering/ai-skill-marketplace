# AI Skill Library

A curated library of AI agent skills, review tools, and productivity workflows for modern AI coding ecosystems.

## Download the Engineering Delivery Orchestrator

**[Download the installable marketplace bundle (ZIP)](https://github.com/LiamCremering/ai-skill-marketplace/archive/refs/heads/main.zip)**

After downloading, extract the ZIP and register the extracted directory in Codex:

```bash
codex plugin marketplace add /path/to/ai-skill-marketplace-main
codex plugin add engineering-delivery-orchestrator@ai-skill-marketplace
```

Start a new Codex thread and authorize SharePoint, GitHub, and Microsoft Teams with your team's own accounts. The download contains no credentials or inherited permissions.


This repository brings together practical capabilities across Claude Code, Codex, Cursor, GitHub Copilot, Greptile, Qodo, and related tooling. The goal is to provide a structured reference for understanding where a skill comes from, how it is installed, and what it is designed to help with in real-world development work.

Each entry includes a practical example so you can quickly decide whether it fits the task in front of you.

## Categories

### Context Shaping

- `grill-with-docs`
  - Use when: The request sounds clear but key decisions are still missing.
  - Example: Before building a patient portal, use it to clarify user roles, data access, success criteria, and what happens when records are unavailable.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `codebase-design`
  - Use when: A feature is growing and you need clear module boundaries before coding.
  - Example: Use it to decide whether notifications, user preferences, and email delivery belong in one service or separate modules.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `Architecture Designer`
  - Use when: You are choosing a technical shape for a new system or major service.
  - Example: Compare a single API with a queue-based architecture for an import process that may handle thousands of files.
  - Install: `/plugin marketplace add jeffallan/claude-skills`
  - Source: [jeffallan/claude-skills](https://jeffallan.github.io/claude-skills/skills/api-architecture/architecture-designer/)

- `/codex:adversarial-review`
  - Use when: A design or plan looks convincing and you want someone to actively look for what could break.
  - Example: Ask it to challenge a proposal to store customer documents in one shared bucket and identify privacy or access-control gaps.
  - Install: `/plugin marketplace add openai/codex-plugin-cc`
  - Source: [openai/codex-plugin-cc](https://github.com/openai/codex-plugin-cc)

### Main Flow Shaping

- `/to-spec`
  - Use when: You have meeting notes, a chat, or an idea but no implementable specification.
  - Example: Turn “users should be able to find their invoices faster” into acceptance criteria, screens, edge cases, and non-functional requirements.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/to-tickets`
  - Use when: A specification is ready but the work is still too large to assign or estimate.
  - Example: Split a new login flow into UI, API, migration, test, and rollout tickets with dependencies between them.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/implement`
  - Use when: A ticket is understood and you want to move from plan to a focused code change.
  - Example: Implement the “export CSV” ticket, including the endpoint, download button, validation, and tests.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/tdd`
  - Use when: A behavior is important enough that you want to define it through tests before writing implementation code.
  - Example: Write tests for discount eligibility first, then implement the calculation until those tests pass.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `Qodo Code Review`
  - Use when: You want a pull request reviewed against the conventions and surrounding code of the repository.
  - Example: Before merging a new API endpoint, let it check whether error handling and validation match the existing endpoints.
  - Install: create account and connect Git provider
  - Source: [Qodo docs](https://docs.qodo.ai/code-review)

- `GitHub Copilot Code Review`
  - Use when: You want fast first-pass feedback directly on a GitHub pull request.
  - Example: Open a PR, request a Copilot review, and address its comments before asking a teammate for final approval.
  - Install: enable Copilot review in GitHub
  - Source: [GitHub docs](https://docs.github.com/en/copilot/concepts/agents/code-review)

### Upkeep

- `improve-codebase-architecture`
  - Use when: The code works, but changes keep taking longer because logic is duplicated or tangled.
  - Example: Use it to find why the same permission checks appear in five controllers and propose one reusable policy layer.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/security-review`
  - Use when: A change handles authentication, user input, sensitive data, or an external API.
  - Example: Review a file-upload feature for unsafe file types, missing authorization, and unvalidated filenames before release.
  - Install: run `/security-review` in Claude Code
  - Source: [Claude Code docs](https://support.claude.com/en/articles/11932705-automated-security-reviews-in-claude-code)

- `Secure Code Guardian`
  - Use when: You need security guidance while designing or implementing a feature, not only after it is done.
  - Example: Before adding a webhook, use it to choose signature validation, replay protection, and safe secret storage.
  - Install: `/plugin marketplace add jeffallan/claude-skills`
  - Source: [jeffallan/claude-skills](https://jeffallan.github.io/claude-skills/skills/security/secure-code-guardian/)

- `DeepSource`
  - Use when: You want automated quality and security checks on every change.
  - Example: Connect it to the repository so a pull request is flagged when it introduces duplicated code, a vulnerability, or lower test coverage.
  - Install: connect a Git provider in DeepSource
  - Source: [DeepSource docs](https://docs.deepsource.com/)

- `Trail of Bits Skills`
  - Use when: A high-risk component needs deeper security analysis than a normal code review.
  - Example: Use it to examine a dependency update for supply-chain risk or audit a smart contract before it holds real funds.
  - Install: `/plugin marketplace add trailofbits/skills`
  - Source: [trailofbits/skills](https://github.com/trailofbits/skills)

### Productivity

- `diagnosing-bugs`
  - Use when: You know something is broken but cannot yet explain why or reproduce it reliably.
  - Example: A page is slow only for some customers; use it to capture timings, narrow down the data pattern, test a hypothesis, and prevent recurrence.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `/codex:rescue`
  - Use when: A task is stuck, spans several files, or needs sustained investigation.
  - Example: Use it when a production error has no obvious cause and the agent needs to trace logs, configuration, and recent changes before proposing a fix.
  - Install: `/plugin marketplace add openai/codex-plugin-cc`
  - Source: [openai/codex-plugin-cc](https://github.com/openai/codex-plugin-cc)

- `Continue Agent Mode`
  - Use when: You want an assistant inside the IDE that can inspect files, make a change, and run commands as part of one task.
  - Example: Ask it to add a form field, update validation, run the test suite, and explain the changed files without leaving your editor.
  - Install: install Continue and switch to Agent mode
  - Source: [Continue docs](https://docs.continue.dev/ide-extensions/agent/quick-start)

- `check-pr`
  - Use when: A pull request may be technically correct but is not yet ready for a smooth human review.
  - Example: Run it before requesting review to catch a missing description, unchecked test failure, or undocumented configuration change.
  - Install: clone the Greptile skills repo and install the skill
  - Source: [greptileai/skills](https://github.com/greptileai/skills)

- `greploop`
  - Use when: You want to keep reviewing and improving a change until no important issues remain.
  - Example: Let it review a PR, apply the suggested fixes, then review the revised diff again before merging.
  - Install: clone the Greptile skills repo and install the skill
  - Source: [greptileai/skills](https://github.com/greptileai/skills)

- `Handoff`
  - Use when: Work must pause and someone else needs to continue without rediscovering the whole situation.
  - Example: At the end of a debugging session, create a handoff with the reproduced error, failed hypotheses, changed files, and next recommended test.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

- `research`
  - Use when: A decision depends on facts that should be verified in official documentation or primary sources.
  - Example: Before choosing an authentication flow, research the provider’s current OAuth requirements and capture the links and constraints.
  - Install: `npx skills add mattpocock/skills`
  - Source: [mattpocock/skills](https://github.com/mattpocock/skills)

## Notes

This repository is intended as a practical shortlist and knowledge base for evaluating AI tooling, rather than a complete inventory of every available skill. It is designed to help teams and individuals quickly understand what a tool is for, where it comes from, and how it fits into a software engineering workflow.

## Engineering Delivery Orchestrator

This repository also contains an installable Codex team plugin for delivery analysis across SharePoint, GitHub, and Microsoft Teams.

### Installation

Clone or download this repository, then register its marketplace from the repository root:

```bash
git clone https://github.com/LiamCremering/ai-skill-marketplace.git
codex plugin marketplace add /path/to/ai-skill-marketplace
codex plugin add engineering-delivery-orchestrator@ai-skill-marketplace
```

Start a new Codex thread after installation so the plugin and its connected apps are loaded.

### Authorization and permissions

Each team authorizes SharePoint, GitHub, and Microsoft Teams with its own accounts and organizational policies. No credentials or permissions from the plugin publisher are distributed with the plugin.

SharePoint is used as a read-only source. GitHub and Microsoft Teams write actions are limited to resources granted by the installing team's authorization and require explicit user confirmation before execution.
