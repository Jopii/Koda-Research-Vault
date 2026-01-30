# Report: Desktop UI for Koda on Windows (v1.0)
**Date:** 2026-01-30
**Status:** UI/UX Research

## 1. Context: Moltbot on Windows
Moltbot primarily runs on Linux/macOS. For Windows users like Jesus, it typically operates via **WSL2** or **Docker**. 
- **Current UI:** Jesus uses Telegram/Discord.
- **Official Dashboard:** Moltbot has a built-in web dashboard (Gateway UI).

## 2. Framework Comparison for Custom UI
| Framework | Pros | Cons |
|-----------|------|------|
| **Streamlit** | Fast to build, Python-based, easy API integration. | Harder to package as a standalone `.exe`. Limited custom styling. |
| **Electron** | Native Windows feel, full styling control, "standard" for desktop apps. | Heavy resources, requires JS/TS. |
| **CustomTkinter** | Lightweight, modern look, Python-based. | Less flexible than web-based UIs. |
| **PWA / Web-UI** | Uses the existing browser, zero install. | Doesn't feel like a "separate" app. |

## 3. Recommended Approach for Koda
**Hybrid Python + Streamlit / NiceGUI:**
Since Jesus prefers Python and we need to talk to the local API, a **NiceGUI** or **Streamlit** app wrapped in a native window (using `pywebview`) is the fastest path to a functional local UI.

## 4. Next Steps
- Verify if the **Moltbot Gateway UI** can be extended or "skinned" for Koda.
- Create a simple **Python + NiceGUI** prototype that connects to the Moltbot API.
- Investigate **`pywebview`** to turn a web-UI into a dedicated Windows window.
