---
title: "Hermes v0.14.0 turns the agent runtime into easier infrastructure"
description: "Nous Research released Hermes Agent v0.14.0, the Foundation Release, with PyPI packaging, lighter installs, faster cold starts, an OpenAI-compatible local proxy for OAuth providers, SuperGrok OAuth, Teams, LINE, SimpleX Chat, x_search, and stronger tool/runtime surfaces."
date: 2026-05-16T09:59:15Z
playerSlug: "hermes"
sourceName: "Hermes Agent GitHub release"
sourceUrl: "https://github.com/NousResearch/hermes-agent/releases/tag/v2026.5.16"
category: "Release"
tags:
  - agent-runtime
  - orchestration
  - gateway
  - local-agents
  - open-source
draft: false
---

Nous Research released Hermes Agent `v0.14.0` on May 16 as "The Foundation Release." The release notes frame it as a broad infrastructure pass: Hermes installs more easily, starts faster, exposes more provider and gateway surfaces, and becomes easier to plug into other agent tools.

The biggest category signal is distribution. Hermes is now available as a PyPI package, so the install path can be as simple as `pip install hermes-agent && hermes`. The release also lazy-installs heavyweight backends on first use, trims the `[all]` extras, adds tiered install fallback when a wheel rejects on a platform, and includes a supply-chain advisory checker. For Open Orchestrators readers, that matters because an agent runtime becomes much more interesting when the install path stops being the hard part.

The second signal is interoperability. `hermes proxy` now exposes an OpenAI-compatible local endpoint backed by OAuth-authenticated providers such as Claude Pro, ChatGPT Pro, and SuperGrok. That lets tools like Codex CLI, Aider, Cline, Continue, and custom scripts point at Hermes as the provider bridge instead of each integration owning its own auth path. Hermes also adds SuperGrok OAuth with Grok 4.3 at a 1M-token context window, a Codex app-server runtime path for OpenAI/Codex models, NovitaAI, and an OpenRouter Pareto Code router knob.

The operating surface widened too. The release adds first-class `x_search`, Microsoft Teams end-to-end support, LINE, SimpleX Chat, Discord channel history backfill, native `clarify` buttons on Telegram and Discord, and a more resilient gateway that keeps running when platforms fail. Hermes now reaches 22 messaging platforms, which keeps pushing it toward a persistent agent layer that can live where teams already coordinate.

Performance and tool reliability are part of the same story. The release notes claim about 19 seconds cut from cold start, `hermes tools` All-Platforms dropping from 14 seconds to under 1.5 seconds, and `browser_console` evaluations becoming 180x faster by reusing a persistent Chrome DevTools connection. Hermes also adds per-turn file-mutation verifier summaries, LSP semantic diagnostics after writes, raw-pixel `vision_analyze` for vision-capable models, a unified pluggable `video_generate`, and a `computer_use` cua-driver backend that works beyond Anthropic-only paths.

For Open Orchestrators, the important reading is not "Hermes got many features." It is that Hermes is becoming more usable as agent infrastructure: installable from PyPI, lighter by default, faster to start, easier to call from other tools, present in more messaging systems, and better at catching file/tool mistakes during long agent work.

The release is also a useful counterpoint to v0.13.0's Tenacity Release. v0.13 focused on durability and finishing work. v0.14 focuses on foundation: packaging, providers, gateway reach, tool speed, plugin extension points, skills distribution, and platform support. Together they show Hermes moving from an autonomous terminal agent toward a broader orchestration substrate.

Source confidence: High for the release name, version, date, and highlighted changes. The source is the official GitHub release for `v2026.5.16` / `v0.14.0`. Medium for downstream category implications because the release notes describe capabilities, not independent adoption or reliability benchmarks.

Evidence:

- [Hermes Agent v0.14.0 GitHub release](https://github.com/NousResearch/hermes-agent/releases/tag/v2026.5.16)
- [Hermes Agent GitHub repository](https://github.com/NousResearch/hermes-agent)
- [Hermes Agent documentation](https://hermes-agent.nousresearch.com/docs/)

Explicit non-claims:

- This update does not benchmark Hermes v0.14.0 against other agent runtimes or local agent IDEs.
- This update does not claim every provider, gateway, tool, or platform path is enabled by default in every install.
- This update does not claim Agent Analytics measures Hermes internals, memory, gateway messages, tool traces, or terminal sessions.
