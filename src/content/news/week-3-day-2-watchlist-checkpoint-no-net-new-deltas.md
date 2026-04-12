---
title: "Week-3 Day-2 checkpoint: watchlist holds steady with no net-new deltas"
description: "Canonical GitHub/PyPI re-checks confirm no net-new release-channel deltas across the tracked orchestrator watchlist since the Week-3 Day-1 baseline."
date: 2026-04-12T05:03:19Z
playerSlug: "crewai"
sourceName: "LangGraph release-by-tag API"
sourceUrl: "https://api.github.com/repos/langchain-ai/langgraph/releases/tags/1.1.7"
category: "Watchlist checkpoint"
tags:
  - watchlist
  - continuity
  - release channels
draft: false
---

This Week-3 Day-2 checkpoint re-checked canonical GitHub and PyPI sources against the latest published Week-3 Day-1 baseline. The interval remains a continuity window with no net-new release-channel deltas.

Retrieval timestamp (UTC): `2026-04-12T05:03:19Z`.

## What remained unchanged

- LangGraph exact `1.1.7` remained absent on checked GitHub release-by-tag and PyPI exact-version endpoints (`404` on both).
- LangGraph `1.1.7a1` remained visible on GitHub and PyPI with no observed transition to exact `1.1.7`.
- CrewAI remained on the same state: GitHub latest remained `1.14.2a2` (prerelease) while PyPI package info remained `1.14.1`.
- Semantic Kernel remained unchanged at `python-1.41.2` in checked GitHub releases and `1.41.2` on PyPI.
- LangGraph CLI remained at `0.4.21` on the PyPI info endpoint.
- Secondary queue baselines held: Langflow remained `1.8.4` and Agno remained `2.5.16` in checked GitHub/PyPI channels.

Because this checkpoint confirms continuity rather than change, this is published as cadence coverage and not a net-new release bulletin.

## Evidence

- [LangGraph release by tag `1.1.7` (GitHub API)](https://api.github.com/repos/langchain-ai/langgraph/releases/tags/1.1.7)
- [LangGraph matching refs for `1.1.7` (GitHub API)](https://api.github.com/repos/langchain-ai/langgraph/git/matching-refs/tags/1.1.7)
- [LangGraph exact `1.1.7` (PyPI API)](https://pypi.org/pypi/langgraph/1.1.7/json)
- [LangGraph `1.1.7a1` release page](https://github.com/langchain-ai/langgraph/releases/tag/1.1.7a1)
- [CrewAI recent releases (GitHub API)](https://api.github.com/repos/crewAIInc/crewAI/releases?per_page=8)
- [CrewAI package index (PyPI API)](https://pypi.org/pypi/crewai/json)
- [Semantic Kernel releases (GitHub API)](https://api.github.com/repos/microsoft/semantic-kernel/releases?per_page=8)
- [Semantic Kernel package index (PyPI API)](https://pypi.org/pypi/semantic-kernel/json)
- [LangGraph CLI package index (PyPI API)](https://pypi.org/pypi/langgraph-cli/json)
- [Langflow package index (PyPI API)](https://pypi.org/pypi/langflow/json)
- [Agno package index (PyPI API)](https://pypi.org/pypi/agno/json)

## Explicit non-claims

- This update does not claim feature-level changes beyond cited release/package metadata.
- This update does not claim performance, reliability, or security outcomes.
- This update does not claim roadmap intent or future release timing.
- This update does not claim that `1.1.7a1` implies exact `1.1.7` GA availability.
