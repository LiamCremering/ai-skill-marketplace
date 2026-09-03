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

### Installation Option 1: Install as a Plugin

Download and extract the [marketplace bundle](https://github.com/LiamCremering/ai-skill-marketplace/archive/refs/heads/main.zip), then register the extracted repository directory:

```bash
codex plugin marketplace add /path/to/ai-skill-marketplace-main
codex plugin add engineering-delivery-orchestrator@ai-skill-marketplace
```

Start a new Codex thread after installation and authorize SharePoint, GitHub, and Microsoft Teams with your own accounts.

### Installation Option 2: Create a Personal Agent

Use this option when a workspace admin does not centrally provide the agent. It requires Agents, SharePoint, GitHub, and Microsoft Teams to already be enabled in the workspace.

#### 1. Create the agent

1. In ChatGPT, select the company workspace from the profile menu.
2. Select `Agents` in the left sidebar.
3. Select `Create → Start blank`.
4. If shown, select `Build this agent`.
5. Enter:

```text
Name:
Engineering Delivery Orchestrator

Description:
Connects requirements, decisions, tasks, communication, and implementation
evidence from SharePoint, GitHub, and Microsoft Teams.
```

6. Paste the contents of [`SKILL.md`](./skills/engineering-delivery-orchestrator/SKILL.md) into the `Instructions` field.

#### 2. Add the apps

Under `Tools → + Add tool`, add:

- SharePoint
- GitHub
- Microsoft Teams

Select `End-user account` for each app so the agent uses the personal account of the individual user.

#### 3. Configure security

- Allow only read actions for SharePoint.
- For GitHub and Teams, set `Write approvals` to `Always ask`.
- Optionally restrict GitHub access to specific repositories under `Safety → Add constraint`.

#### 4. Create the agent

1. Under `Channels → ChatGPT`, select `Private to me`.
2. Select `Preview` and run:

```text
Show me the available apps. Do not read or change any data yet.
```

3. Confirm that all three apps are displayed.
4. Select `Create` in the upper-right corner.

#### 5. Connect the accounts

When an app is used for the first time, ChatGPT asks the user to sign in:

- SharePoint: Sign in with the user's business Microsoft account.
- GitHub: Sign in with the user's GitHub account and allow only the required repositories.
- Teams: Sign in with the user's business Microsoft account.

Review the requested permissions, then select `Connect` or `Confirm`. The agent can only access content that the connected account is already permitted to access. Connections can be reviewed or disconnected later under `Settings → Apps`.

If `Agents` is missing or an app shows `Disabled by admin`, a workspace admin must enable that feature or app.

#### 6. Use the agent

Open the agent from `Agents` or mention it in a regular ChatGPT conversation:

```text
@Engineering Delivery Orchestrator
```

## Package Contents

- [Plugin manifest](./.codex-plugin/plugin.json)
- [Connected app declarations](./.app.json)
- [Agent skill](./skills/engineering-delivery-orchestrator/SKILL.md)
