# Engineering Delivery Orchestrator

Connects requirements, backlog context, implementation evidence, delivery risks, and team follow-up across SharePoint, GitHub, and Microsoft Teams.

## Purpose: Connected Context

Information required for engineering delivery rarely lives in one place. Requirements and decisions may be stored in SharePoint, implementation details in GitHub, and current discussions or tasks in Microsoft Teams and Planner.

The Engineering Delivery Orchestrator connects these sources for a specific request. It brings together the relevant requirement, decision history, backlog context, code changes, delivery status, and team communication so that users and AI work with the right context instead of isolated fragments.

This connected context supports better decisions, exposes contradictions and missing evidence, and enables consistent follow-up across systems. The agent may prepare or perform changes only where the connected service permits them and only after the required user confirmation. SharePoint remains read-only.

## Team Deployment

The plugin is designed to be deployed once for an engineering or delivery team. A workspace administrator can make the same agent version, workflows, rules, and integrations available to all authorized members. This gives the team a consistent way to assess delivery readiness, connect requirements to implementation evidence, and coordinate follow-up.

## Personal Authentication

Each team member connects the plugin with their own Microsoft and GitHub accounts. Members can work with shared SharePoint sites, GitHub repositories, Teams, and Planner plans when their individual accounts already have access to those resources.

Shared service accounts are neither required nor recommended. Personal authentication keeps activity attributable to the person who requested it and preserves the access controls already maintained in Microsoft 365 and GitHub.

## Permission Model

The plugin does not grant access to team resources or expand a member's existing permissions. It can only use the resources available to the connected user.

- SharePoint is used as a read-only source.
- GitHub and Microsoft Teams writes are limited to resources available to the connected user.
- Every external write requires explicit user confirmation.
- The package contains no credentials or inherited permissions.

## Installation

Download and extract the [marketplace bundle](https://github.com/LiamCremering/ai-skill-marketplace/archive/refs/heads/main.zip), then register the extracted repository directory:

```bash
codex plugin marketplace add /path/to/ai-skill-marketplace-main
codex plugin add engineering-delivery-orchestrator@ai-skill-marketplace
```

Start a new Codex thread after installation and authorize SharePoint, GitHub, and Microsoft Teams with your own accounts.

## Package Contents

- [Plugin manifest](./.codex-plugin/plugin.json)
- [Connected app declarations](./.app.json)
- [Agent skill](./skills/engineering-delivery-orchestrator/SKILL.md)
