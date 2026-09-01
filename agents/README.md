# Agents

This area contains the user-facing documentation and downloads for reusable agents. Technical plugin files remain in the repository paths required by Codex and GitHub.

## Engineering Delivery Orchestrator

Connects requirements, backlog context, implementation evidence, delivery risks, and team follow-up across SharePoint, GitHub, and Microsoft Teams.

**[Download the installable marketplace bundle (ZIP)](https://github.com/LiamCremering/ai-skill-marketplace/archive/refs/heads/main.zip)**

### Installation

Extract the downloaded ZIP and register the extracted repository directory:

```bash
codex plugin marketplace add /path/to/ai-skill-marketplace-main
codex plugin add engineering-delivery-orchestrator@ai-skill-marketplace
```

Start a new Codex thread after installation and authorize SharePoint, GitHub, and Microsoft Teams with your team's own accounts.

### Permissions

- SharePoint is used as a read-only source.
- GitHub and Microsoft Teams writes are limited to resources authorized by the installing team.
- Every external write requires explicit user confirmation.
- The package contains no credentials or inherited permissions.

### Plugin Source

- [Plugin manifest](../plugins/engineering-delivery-orchestrator/.codex-plugin/plugin.json)
- [Connected app declarations](../plugins/engineering-delivery-orchestrator/.app.json)
- [Agent skill](../plugins/engineering-delivery-orchestrator/skills/engineering-delivery-orchestrator/SKILL.md)

## Code Writer

The repository also contains a GitHub custom agent for focused code changes and testing.

- [View the Code Writer agent](../.github/agents/code-writer.agent.md)
