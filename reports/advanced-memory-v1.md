# Report: Advanced Memory & Sub-Agent Orchestration (v1.0)
**Date:** 2026-01-30
**Status:** Architecture Research

## 1. Sub-Agent Orchestration
Moltbot uses a multi-agent routing system. 
- **Concept:** Named AI "employees" (e.g., Koda-Dev, Koda-Researcher) can operate autonomously.
- **Workflow:** Large tasks are broken into steps, assigned to sub-agents via the `sessions_spawn` tool, and monitored in the background.
- **Goal:** Enable Koda to delegate search/writing tasks while focusing on high-level strategy.

## 2. Advanced Memory: "Triple-Memory" Pattern
Research identified a "Triple-Memory" pattern (though likely a community term for integrated systems):
- **Core Memory:** Markdown-based (`MEMORY.md`, `USER.md`). Debuggable and portable.
- **Vector Memory:** Using plugins like `memory-lancedb` for semantic search over large contexts.
- **Git-Notes/Audit:** Tracking changes and decisions over time via repository notes.

## 3. Proactive Consciousness
- **Planning Phases:** Agents should perform a "thought flow" or "planning phase" before tool selection.
- **Background Persistence:** Long-running tasks (hours/days) with scheduled updates via `cron` or `heartbeat`.

## 4. Recommendations for Koda
- **Install `triple-memory-skill`** (Investigate if this is a standard skill or a collection of scripts).
- **Configure `memory-lancedb` plugin** once an OpenAI/Gemini embedding key is available for deep semantic search.
- **Implement a "Planning Step"** in my `HEARTBEAT.md` flow to simulate a thinking phase before action.

## 5. Next Steps
- Verify the availability of `triple-memory-skill` in the local registry.
- Draft a "Sub-Agent Delegation" template for research tasks.
- Explore the `memory-lancedb` configuration schema.
