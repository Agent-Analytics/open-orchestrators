---
title: "Squad joins Open Orchestrators as a repo-native agent team system"
description: "Squad is now listed as an alpha GitHub Copilot-based system for persistent specialist agents, coordinator routing, and parallel team work inside a repo."
date: 2026-04-16T15:12:00Z
playerSlug: "squad"
sourceName: "Squad docs"
sourceUrl: "https://bradygaster.github.io/squad/"
category: "Directory update"
tags:
  - orchestration
  - agent-teams
  - github-copilot
  - persistent-memory
draft: false
---

Squad has been added to the Open Orchestrators directory as an alpha GitHub Copilot-based agent team system. The public docs describe a repo-native workflow where specialist agents live in `.squad/`, keep their own histories, share decisions, and work from project context that can be committed with the codebase.

This matters for Open Orchestrators readers because Squad makes the agent team the product surface. Its documented model includes coordinator routing, specialist roles, persistent team memory, parallel execution, issue triage, session recovery breadcrumbs, a CLI package, and a programmable SDK.

For builders and operators, the practical signal is that Squad belongs with coordination and team systems rather than CLI session workspaces. A Squad workflow is not only about launching several terminals; it defines the repo-local team state, routing layer, and follow-up memory that can carry decisions across sessions.

The new directory note also frames the first Agent Analytics loop for Squad: a Squad team routes work to specialist agents, the shipped surface reports visits and conversion events, a lead or analyst-style Squad agent fetches the results, and the finding is written back into Squad decisions or history before the next routed improvement.

Source confidence: High for public docs, GitHub repository metadata, and npm package existence. Medium for adoption or production-readiness because Squad is explicitly marked as alpha software.

Evidence:

- [Squad docs](https://bradygaster.github.io/squad/)
- [Squad GitHub repository](https://github.com/bradygaster/squad)
- [Squad CLI on npm](https://www.npmjs.com/package/@bradygaster/squad-cli)
- [Squad SDK on npm](https://www.npmjs.com/package/@bradygaster/squad-sdk)
- [Open Orchestrators Squad player note](https://openorchestrators.org/players/squad/)

Explicit non-claims:

- This update does not claim stable APIs or CLI behavior; the public docs mark Squad as alpha.
- This update does not claim a native Squad-Agent Analytics integration.
- This update does not claim production readiness or adoption beyond the public project evidence.
