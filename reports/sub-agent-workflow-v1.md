# Report: Sub-Agent Delegation Prototype (v1.0)
**Date:** 2026-01-30
**Status:** Workflow Design

## 1. Concept
To maximize efficiency, Koda will act as a **Supervisor Agent**, delegating specialized research tasks to temporary sub-agents using `sessions_spawn`.

## 2. Delegation Pattern
- **Trigger:** A complex research task (e.g., "Find the best local LLM for medical analysis").
- **Supervisor Action:** `sessions_spawn(task="Research [Topic] and provide a 3-paragraph summary", agentId="main")`.
- **Sub-Agent Workflow:**
    1.  Perform web searches using `web_search` or `perplexity-search`.
    2.  Summarize findings using a smaller, faster model (e.g., Gemini Flash).
    3.  Return the summary to the Supervisor chat.
- **Supervisor Role:** Review the summary, integrate it into the final report, and inform the user.

## 3. Benefits
- **Non-blocking:** The main chat remains responsive.
- **Parallelism:** Can spawn multiple sub-agents for different parts of a task.
- **Model Optimization:** Can use cheaper models for search and more powerful models for final reasoning.

## 4. Next Steps
- Create a reusable **Sub-Agent Prompt Template**.
- Test a parallel research run: Delegate "Tech News" and "Spain News" to two different sub-agents.
