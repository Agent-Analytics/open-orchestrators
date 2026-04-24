---
title: "Mastra adds browser support for agents and streams sessions into Studio"
description: "Mastra's Apr 24 launch lets agents browse and act on websites, starting with Stagehand and AgentBrowser, while the linked @mastra/core release adds CLI-driven browser automation and live screencasts."
date: 2026-04-24T21:40:00Z
playerSlug: "mastra"
sourceName: "Mastra Blog"
sourceUrl: "https://mastra.ai/blog/announcing-browser-support"
category: "Release"
tags:
  - orchestration
  - browser-automation
  - computer-use
  - agents
  - observability
draft: false
---

On Apr 24, Mastra announced browser support for agents. The launch says Mastra agents can now navigate pages, click through flows, fill forms, and extract structured data from sites that do not expose APIs. The announcement also says each interaction is streamed live into Mastra Studio, so operators can watch or step in while the run is happening.

This matters for Open Orchestrators readers because browser and computer-use expansion is a real capability-surface change, not just framework polish. Mastra is extending from TypeScript agents, workflows, memory, and observability into agent action on the live web. That broadens the kinds of end-to-end tasks a Mastra-based system can complete without waiting for a custom API integration.

For builders and operators, the practical signal is that Mastra is trying to close the loop between agent reasoning, tool execution, and visible web interaction. The blog says the first providers are Stagehand and AgentBrowser, with more providers coming, and that builders can run browsers locally or connect to managed services like Browserbase. The same-day `@mastra/core@1.27.0` release backs that up with release notes for CLI-driven browser automation, automatic CDP injection for browser CLIs, and a new `@mastra/browser-viewer` package for live screencasts in Studio.

Taken together, the launch pushes Mastra further toward an operator-facing platform rather than only a framework library. The category signal is not merely that Mastra can call another browser tool. It is that browser sessions, CLI-based agent workflows, and Studio visibility are being wired into the same product surface, which makes browser work easier to observe and manage as part of orchestration.

Source confidence: High for the existence and scope of the browser-support launch, the initial provider set, and the Studio screencast framing. Medium for downstream workflow implications because the announcement and release notes describe the capability surface, not a benchmark of task reliability across sites.

Evidence:

- [Mastra browser support announcement](https://mastra.ai/blog/announcing-browser-support)
- [Mastra `@mastra/core@1.27.0` release](https://github.com/mastra-ai/mastra/releases/tag/%40mastra/core%401.27.0)
- [Mastra official X post on browser support](https://x.com/mastra/status/2047718294040568140)
- [Mastra official X follow-up on Stagehand and AgentBrowser](https://x.com/mastra/status/2047718305709040090)
- [Mastra GitHub repository](https://github.com/mastra-ai/mastra)

Explicit non-claims:

- This update does not claim browser support is already available across every Mastra browser provider.
- This update does not claim a fully general computer-use agent with benchmarked reliability across arbitrary websites.
- This update does not compare Mastra's browser surface maturity against other Open Orchestrators players.
