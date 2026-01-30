# Report: Research Roundup & Digital Presence
**Date:** 2026-01-30
**Status:** Completed Night Shift Tasks

## 1. User Profile: Jesús Jódar Piernas (@jesujopi / @jesujopi3D)
- **Identity:** Novice 3D artist and student of Video Game Design and Development from Spain.
- **Interests:** 3D assets, concept art, and phone development.
- **GitHub Highlights:** 22 repositories under user `Jopii`. Pinned personal site: `jopii.github.io`.
- **Note for Koda:** Assist with 3D modeling workflows (Blender/Maya), game design logic, and mobile development research.

## 2. Advanced Memory & Sub-Agents
- **Orchestration:** Moltbot manages sub-agents through the Gateway control plane. Proactive behavior is driven by `heartbeats` and `cron`.
- **Memory Optimization:** Use `MEMORY.md` and `USER.md` for persistent context. Syncing the workspace repo (`~/clawd`) is critical for cross-session continuity.
- **Architecture:** Sub-agents can be orchestrated via WebSocket interfaces for long-running background tasks.

## 3. Local AI & TTS (PC/iPhone)
- **Frameworks:** Use **WSL2** or **Docker** for running Moltbot on Windows.
- **TTS:** Spanish support is best achieved via models like **Coqui XTTS v2** or **Kokoro-TTS** (efficient, lightweight).
- **iPhone:** Focus on quantized models (Gemma/Qwen) that can run on-device via CoreML or MLX.

## 4. Identity Expansion
- **Email:** Services like **AgentMail** provide dedicated API-based inboxes for AI agents.
- **Socials:** Automation tools can bridge Moltbot to Instagram Graph APIs for account management.
- **Images:** **Cloudflare Workers AI** offers a generous free tier for generating images via SDXL APIs.

---
*End of Night Shift Report. Ready for morning briefing.* 🐾🚀🐱
