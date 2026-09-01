# AI Engineering Resource Hub

A focused collection of three engineering deliverables. Each area is maintained separately so teams can use only what they need.

## Deliverables

### Best Practices

Practical guidance for designing and maintaining effective engineering workflows.

- [Browse Best Practices](./best-practices/)

### AI Skill Library

A curated catalog of AI agent skills, review tools, and productivity workflows, including a browsable web view.

- [Browse the Skill Library](./skill-library/)
- [Open the Skill Library documentation](./skill-library/README.md)

### Engineering Delivery Orchestrator

An installable Codex plugin that connects requirements, backlog context, implementation evidence, delivery risks, and team follow-up.

The plugin is designed as a centrally managed agent for engineering and delivery teams. All authorized members use the same workflows and rules while connecting their own Microsoft and GitHub accounts. The agent can work with shared SharePoint sites, GitHub repositories, Teams, and Planner plans only within each member's existing permissions. No shared credentials are required.

- [View installation and usage](./plugins/engineering-delivery-orchestrator/)
- [Open the plugin package](./plugins/engineering-delivery-orchestrator/)

## Repository Layout

```text
best-practices/                              Engineering workflow guidance
skill-library/                               Skill catalog, web view, and catalog data
plugins/engineering-delivery-orchestrator/   Installable Codex plugin
```

The hidden `.agents/plugins/marketplace.json` file is retained because Codex uses it for marketplace discovery and installation.
