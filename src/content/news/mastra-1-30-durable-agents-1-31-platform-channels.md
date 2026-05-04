---
title: "Mastra ships Durable Agents, remote filesystems, and platform channels"
description: "Mastra's late-April and early-May releases move the TypeScript agent framework toward production orchestration with crash-resilient Durable Agents, resumable streams, workflow-backed execution, remote filesystems for S3, GCS, and Azure, channel providers, Slack integration, NestJS support, and Google Drive workspaces."
date: 2026-05-04T15:21:40Z
playerSlug: "mastra"
sourceName: "Mastra GitHub releases"
sourceUrl: "https://github.com/mastra-ai/mastra/releases/tag/%40mastra/core%401.31.0"
category: "Release"
tags:
  - orchestration
  - durable-agents
  - channels
  - streaming
  - agents
  - workspaces
draft: false
---

Mastra published remote filesystem support for workspaces on April 29, then released `@mastra/core@1.30.0` on May 1 and `@mastra/core@1.31.0` on May 4. Together, the updates turn last week's browser-support story into a broader production-orchestration push: remote filesystems for S3, Google Cloud Storage, and Azure; Durable Agents; resumable streams; workflow-backed execution; platform channels; Slack integration; NestJS support; Google Drive workspaces; and a real-time AWS Nova Sonic voice provider.

Before the durability release, Mastra also announced remote filesystem support for workspaces. Agents can attach providers for S3, Google Cloud Storage, and Azure, then read, write, and manage remote files from the workspace layer. Mastra positioned this alongside sandboxes, so an agent can use remote storage while also running scripts, installing packages, and executing commands in a safer runtime boundary.

The most important operator-facing change is the new Durable Agent support in `@mastra/core@1.30.0`. Mastra says agent streams can now resume after client disconnects and continue through server crashes or restarts by caching stream events and reconnecting with `observe(runId, { offset })`. That addresses a real orchestration failure mode: long-running agent loops should not disappear just because a browser refreshes, a mobile client backgrounds, or an HTTP connection drops.

Mastra also adds workflow-backed durable execution through `createEventedAgent` and `createInngestAgent`, so agent loops can run outside the original HTTP request while clients subscribe to progress. The release notes describe a pluggable PubSub and cache layer, with Redis-backed production configurations recommended for replay and reconnect behavior across instances.

The May 4 release expands the surrounding platform layer. The new platform channels framework adds `ChannelProvider`, `ChannelsStorage`, connection flows for OAuth, deep links, and immediate integrations, plus Mastra-level connect, disconnect, and list APIs. The first concrete provider is `@mastra/slack`, which connects agents to Slack workspaces with OAuth-based app provisioning, encrypted credential storage, slash commands, and threaded conversation support.

This matters for Open Orchestrators readers because Mastra is not only adding model wrappers or another workflow helper. It is wiring workspace storage, sandboxed execution, durability, channel integrations, server adapters, streaming, and observability into the same agent platform. That is the shape of an orchestrator moving from "run an agent" toward "operate agents across real work surfaces without losing state."

Source confidence: High for the release and blog contents because the primary evidence is Mastra's official GitHub releases and Mastra's own remote-filesystems announcement. Medium for category implications because the sources describe capabilities and APIs, not independent reliability benchmarks in production deployments.

Evidence:

- [Mastra remote filesystems announcement](https://mastra.ai/blog/announcing-remote-filesystems)
- [Mastra X thread on remote filesystems and sandboxes](https://x.com/mastra/status/2049522309460062216)
- [Mastra `@mastra/core@1.31.0` release](https://github.com/mastra-ai/mastra/releases/tag/%40mastra/core%401.31.0)
- [Mastra `@mastra/core@1.30.0` release](https://github.com/mastra-ai/mastra/releases/tag/%40mastra/core%401.30.0)
- [Mastra `@mastra/core@1.29.0` release](https://github.com/mastra-ai/mastra/releases/tag/%40mastra/core%401.29.0)
- [Mastra GitHub repository](https://github.com/mastra-ai/mastra)
- [Mastra official website](https://mastra.ai/)

Explicit non-claims:

- This update does not claim Durable Agents eliminate every failure mode in long-running agent execution.
- This update does not benchmark Mastra's durability against other Open Orchestrators players.
- This update does not claim every platform channel provider exists today; the release names the framework and Slack provider specifically.
