---
title: "Mastra turns ACP coding agents into tools and subagents"
description: "Mastra's May 14 release adds @mastra/acp, letting ACP-compatible coding agents run as Mastra tools or lightweight subagents inside supervisors, workflows, and the Inngest adapter."
date: 2026-05-15T23:38:16Z
playerSlug: "mastra"
sourceName: "Mastra GitHub release"
sourceUrl: "https://github.com/mastra-ai/mastra/releases/tag/%40mastra/core%401.34.0"
category: "Release"
tags:
  - acp
  - coding-agents
  - subagents
  - workflows
  - orchestration
ogImage: "/images/news/mastra-1-34-acp-coding-agents.png"
draft: false
---

Mastra's May 14 release adds `@mastra/acp@0.1.0`, a new package for running ACP-compatible coding agents as Mastra tools or lightweight subagents. The release frames ACP agents as usable anywhere Mastra accepts a `SubAgent`, including supervisor delegation, workflow steps, and the Inngest workflow adapter.

![Editorial artwork showing ACP coding-agent modules flowing through a central orchestration graph into tools, subagents, workflows, and event streams](/images/news/mastra-1-34-acp-coding-agents.png)

The category signal is simple: coding agents are becoming composable runtime components. Instead of treating an ACP-compatible coding agent as a standalone CLI outside the application graph, Mastra can wrap it as `createACPTool(...)` or instantiate it as an `AcpAgent`. A supervisor can then delegate coding work to that subagent, and workflows can treat it as an agent-backed step.

That matters for Open Orchestrators readers because it narrows the gap between "agent framework" and "coding-agent control plane." ACP gives the coding agent side a protocol surface. Mastra is now giving that surface a place inside its TypeScript agent/workflow runtime.

The same release also adds agent metadata for filtering, cloning, and dynamic resolution; enterprise foundations for admin model policies and role-aware capabilities; better `workspace.read_file` handling for native media parts and safer binary behavior; lightweight observability trace listing; and improved retry visibility in workflow traces. Those are useful platform moves, but the ACP package is the orchestration headline.

The interesting next question is whether ACP-compatible coding agents become normal building blocks inside agent systems: one node in a supervisor graph, one step in a workflow, one tool behind a product agent, or one specialized worker among many. Mastra's release is a concrete step in that direction.

Source confidence: High for the release name, package, date, and highlighted capabilities. The source is the official Mastra GitHub release for `@mastra/core@1.34.0` and `@mastra/acp@0.1.0`. Medium for ecosystem implications because the release documents capability, not independent adoption or production reliability.

Evidence:

- [Mastra May 14, 2026 GitHub release](https://github.com/mastra-ai/mastra/releases/tag/%40mastra/core%401.34.0)
- [Mastra GitHub repository](https://github.com/mastra-ai/mastra)
- [Mastra documentation](https://mastra.ai/docs)

Explicit non-claims:

- This update does not claim ACP is universally adopted across coding agents.
- This update does not benchmark `@mastra/acp` against direct CLI orchestration or other agent runtimes.
- This update does not claim every ACP-compatible agent works in every Mastra deployment without adapter-specific configuration.
