---
title: "Mastra joins the Open Orchestrators watchlist as a TypeScript agent workflow platform"
description: "Mastra is an open-source TypeScript framework for building agents, graph-based workflows, MCP servers, evals, observability, and production AI applications."
date: 2026-04-13T20:09:00Z
playerSlug: "mastra"
sourceName: "Mastra GitHub repository"
sourceUrl: "https://github.com/mastra-ai/mastra"
category: "Directory"
tags:
  - orchestration
  - agents
  - workflows
  - typescript
  - open-source
  - agent-analytics
draft: false
---

Mastra has been added to the Open Orchestrators directory after verification from its official website, documentation, public GitHub repository, GitHub release channel, and npm package metadata. Mastra describes itself as a framework for building AI-powered applications and agents with a modern TypeScript stack.

This matters for Open Orchestrators readers because Mastra's public surface is directly about orchestrating agentic applications. The repository highlights agents, graph-based workflows, human-in-the-loop suspension and resume, context management, MCP servers, evals, observability, and production deployment patterns.

For operators and builders, the practical signal is that Mastra has several watch surfaces: the official site, docs, `mastra-ai/mastra` repository, GitHub releases, the `@mastra/core` npm package, and the official social handle `@mastra`. The npm package `@mastra/core` was observed at `1.24.1` during the 2026-04-13 verification pass, and the GitHub release stream showed the `@mastra/core@1.24.0` release from 2026-04-08.

## Where Mastra Fits

Mastra belongs in the Open Orchestrators frame because it gives TypeScript teams a structured way to build agent systems, not only chat completions. Agents handle open-ended tasks with tools and goals. Workflows provide explicit control over multi-step processes. The docs position workflows around clear steps, data movement, execution order, suspension, resumption, streaming results, and managed runners.

That makes Mastra a strong fit for teams already building in React, Next.js, Node.js, or TypeScript-heavy backend stacks. It can sit close to the application code, expose agents and workflows through familiar runtime surfaces, and give builders a typed framework for explicit orchestration.

The workflow layer is the category signal. Mastra workflows can call functions, external APIs, agents, or tools, and they can be composed with control-flow primitives such as sequential steps, branching, and parallel execution. That gives teams a way to make agent work inspectable and repeatable, instead of leaving everything to a single model loop.

## Where Builder Web Analytics Fits

Agent Analytics does not need a player-specific plugin to be useful here. It is web analytics for builders: instrument the TypeScript app, docs site, demo, onboarding flow, support surface, or internal web app that a Mastra-backed project affects, then let the builder or workflow read the results.

That surface might be a Next.js app, a product onboarding flow, a docs site, a demo, a support experience, or an internal tool with deliberate product events. Mastra can coordinate the agent or workflow logic. Agent Analytics measures the project surface those builders ship, not Mastra logs or traces.

A useful Mastra task can stay short:

```text
Set up Agent Analytics for this Mastra-backed project. Track the first value path, verify that events arrive, and add a scheduled workflow that reviews activation, drop-off, and source quality after each shipped change.
```

The first event set should stay small. For a developer-facing product, start with docs visit, install command copy, signup, project creation, provider connection, first workflow run, or first successful deployment. For an internal web app, start with task created, task completed, approval submitted, report viewed, or escalation avoided.

The editorial point is that Mastra gives TypeScript builders an orchestration layer inside the app stack, while Agent Analytics gives those builders project usage data their agent workflow can act on.

## The First Loop To Measure

For most Mastra operators, the first Agent Analytics loop should connect builder output to the user journey:

1. A Mastra-backed builder changes a page, docs flow, onboarding path, app surface, demo, or support surface.
2. Users encounter the changed surface through search, GitHub, social, docs, product navigation, or an internal web app.
3. Agent Analytics tracks visits, sources, signup, install intent, setup start, first workflow run, report viewed, task completed, or the product's equivalent activation events.
4. A Mastra workflow reviews the project event data and identifies the largest drop-off or best-performing source.
5. The workflow creates the next improvement task with the relevant context attached.

Example recurring task:

```text
Every weekday morning, query Agent Analytics for the last 24 hours. Report visits, sources, signup, project creation, first workflow run, report viewed, task completed, and the largest drop-off. Create one follow-up issue for the project surface most likely to improve activation.
```

This is the operating loop that matters: build the change, measure the project outcome, and route the next task based on evidence.

## What To Watch Next

Mastra should stay on the Open Orchestrators watchlist for TypeScript workflow, agent, and production-app movement. The most useful future signals are:

- GitHub releases for workflow engine, agents, human-in-the-loop, MCP, evals, observability, storage, deployment, and server-adapter changes.
- npm releases for `@mastra/core`.
- Documentation changes around workflows, workflow state, suspend/resume, human-in-the-loop, observability, evals, and MCP.
- Official `@mastra` announcements for launch, release, or ecosystem updates.
- Official examples or setup paths that show Mastra workflows querying Agent Analytics project data directly.

## Source Confidence

High for the directory addition and source surfaces. The official site, repository, docs, GitHub release stream, and npm package all support Mastra as an open-source TypeScript agent workflow platform. The Agent Analytics framing is builder-facing web analytics: it applies when the measured object is a project surface with deliberate web or product events.

## Evidence

- [Mastra official website](https://mastra.ai/)
- [Mastra GitHub repository](https://github.com/mastra-ai/mastra)
- [Mastra GitHub releases](https://github.com/mastra-ai/mastra/releases)
- [Mastra workflows documentation](https://mastra.ai/docs/workflows/overview)
- [Mastra agents documentation](https://mastra.ai/docs/agents/overview)
- [Mastra observability documentation](https://mastra.ai/docs/observability/overview)
- [npm package `@mastra/core`](https://www.npmjs.com/package/@mastra/core)
- [Agent Analytics CLI package](https://www.npmjs.com/package/@agent-analytics/cli)
- [Agent Analytics installation guides](https://docs.agentanalytics.sh/installation/)

## Explicit Non-Claims

- This update does not claim Agent Analytics measures Mastra logs, traces, or workflow-engine execution.
- This update does not compare Mastra's quality, adoption, or maturity against other Open Orchestrators players.
- This update does not claim all Mastra repository code is under the same license; the repository documents a dual-license model with Apache-2.0 for the core framework and a separate enterprise license for `ee/` directories.
