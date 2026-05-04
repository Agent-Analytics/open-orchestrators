---
title: "Hermes adds a durable Kanban board for multi-agent profile work"
description: "A fresh Nous Research announcement and merged Hermes PRs show Hermes moving multi-agent coordination into a durable SQLite Kanban board where profile workers claim tasks, run in parallel, block for humans, and hand off with audit history."
date: 2026-05-03T17:55:00Z
playerSlug: "hermes"
sourceName: "Nous Research X announcement"
sourceUrl: "https://x.com/NousResearch/status/2050997692977844324"
category: "Announcement"
tags:
  - orchestration
  - multi-agent
  - kanban
  - agent-runtime
  - open-source
draft: false
---

Nous Research announced on May 3 that Hermes Agent now has "multi-agent via the Kanban" in v0.12.0: agents claim tasks from a board, work in parallel, hand off when blocked, and let the operator watch progress and unblock work from one view instead of juggling terminals.

The useful news is not that Hermes has another task list. It is that Hermes is moving profile-based agent coordination into a durable control plane. The official Kanban docs describe a shared `~/.hermes/kanban.db` board across Hermes profiles, with every task, handoff, comment, run, and event kept as rows that any profile or human can read and edit. The merged Kanban PR backs that up with a SQLite kernel, atomic task claiming, tenant namespacing, max-runtime timeouts, worker heartbeats, idempotency keys, crash detection, run history, and a gateway-embedded dispatcher that spawns assigned profiles as full Hermes worker processes.

That is a real Open Orchestrators category signal. Hermes already had subagent delegation for short-lived child-agent work. Kanban covers a different operating mode: persistent named profiles, durable task state, human-in-the-loop blocking and unblocking, retry history, scoped workspaces, and cross-agent handoffs that survive crashes or context compression. In orchestration terms, Hermes is separating quick in-process delegation from a longer-lived work queue that humans and agents can both operate.

There is also an important freshness caveat. The v0.12.0 release notes say an earlier Kanban implementation landed and was reverted while the design was reworked. The stronger signal came after that: PR #17805 merged the durable multi-profile board on Apr 30, and PR #19378 merged on May 3 to fix profile workers so they share the same board, workspaces, and worker logs as the dispatcher that spawned them. Nous then announced the capability publicly the same day.

For operators, the implication is practical. Hermes can now be organized more like a small agent team: one profile creates or decomposes work, specialist profiles claim ready tasks, a reviewer or writer profile waits on parent tasks, and a human can unblock the system from the board instead of reconstructing state from terminal scrollback. The docs explicitly position Kanban as the shape for research triage, scheduled ops, digital twins, engineering pipelines, and fleet work where simple `delegate_task` calls are too ephemeral.

For the Agent Analytics angle, this makes the measurement boundary cleaner. Hermes Kanban can coordinate the agent workforce that ships pages, docs, onboarding changes, and experiments. Agent Analytics should measure the user-facing outcomes after that work lands: visits, sources, install intent, signup, activation, retention, funnel movement, and experiment results. The Kanban board records agent operations; Agent Analytics records whether those operations changed product behavior.

Source confidence: High for the existence and current direction of the Kanban capability. The public Nous Research post announced it, the official Hermes docs describe the board and its distinction from subagent delegation, and merged repository PRs show the durable board and the May 3 profile-worker sharing fix.

Evidence:

- [Nous Research X announcement: Hermes Agent now has multi-agent via the Kanban](https://x.com/NousResearch/status/2050997692977844324)
- [Hermes Kanban documentation](https://hermes-agent.nousresearch.com/docs/user-guide/features/kanban)
- [Hermes Subagent Delegation documentation](https://hermes-agent.nousresearch.com/docs/user-guide/features/delegation)
- [Hermes PR #17805: durable multi-profile collaboration board](https://github.com/NousResearch/hermes-agent/pull/17805)
- [Hermes PR #19378: share board, workspaces, and worker logs across profiles](https://github.com/NousResearch/hermes-agent/pull/19378)
- [Hermes issue #18442: profile-scoped Kanban DB bug](https://github.com/NousResearch/hermes-agent/issues/18442)
- [Hermes Agent v0.12.0 GitHub release](https://github.com/NousResearch/hermes-agent/releases/tag/v2026.4.30)
- [Hermes Agent GitHub repository](https://github.com/NousResearch/hermes-agent)

Explicit non-claims:

- This update does not claim Kanban replaced Hermes subagent delegation; the docs describe them as different coordination surfaces.
- This update does not claim every Hermes profile or deployment already has a tuned multi-agent team configured.
- This update does not benchmark Hermes Kanban against other multi-agent boards or orchestration systems.
- This update does not claim Agent Analytics measures Hermes Kanban internals, worker logs, or conversation history.
