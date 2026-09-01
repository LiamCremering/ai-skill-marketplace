# Engineering Delivery Orchestrator

Connects requirements, backlog context, implementation evidence, delivery risks, and team follow-up across SharePoint, GitHub, and Microsoft Teams.

## Installation

Download and extract the [marketplace bundle](https://github.com/LiamCremering/ai-skill-marketplace/archive/refs/heads/main.zip), then register the extracted repository directory:

```bash
codex plugin marketplace add /path/to/ai-skill-marketplace-main
codex plugin add engineering-delivery-orchestrator@ai-skill-marketplace
```

Start a new Codex thread after installation and authorize SharePoint, GitHub, and Microsoft Teams with your team's own accounts.

## Permissions

- SharePoint is used as a read-only source.
- GitHub and Microsoft Teams writes are limited to resources authorized by the installing team.
- Every external write requires explicit user confirmation.
- The package contains no credentials or inherited permissions.

## Package Contents

- [Plugin manifest](./.codex-plugin/plugin.json)
- [Connected app declarations](./.app.json)
- [Agent skill](./skills/engineering-delivery-orchestrator/SKILL.md)
