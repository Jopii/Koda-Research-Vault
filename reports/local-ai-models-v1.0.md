# Report: Local AI & TTS for Windows / iPhone (v1.0)
**Date:** 2026-01-30
**Status:** Hardware/Model Research

## 1. Local LLM Strategy (PC - RTX 3060 12GB)
The **RTX 3060** is a powerhouse for local inference due to its 12GB VRAM.
- **Top Choice:** **Qwen3 8B Instruct** (via Ollama or LM Studio). It fits the VRAM perfectly and offers state-of-the-art performance for its size.
- **Safe Choice:** **Qwen3 4B Instruct**. Fast, leaves plenty of VRAM for other tasks (like TTS).
- **Optimization:** Use **LM Studio** with NVIDIA TensorRT for 50% faster inference.

## 2. Best Spanish TTS (Local)
- **Primary:** **Coqui XTTS v2**. This is the gold standard for local high-fidelity Spanish TTS. It supports voice cloning and runs smoothly on the RTX 3060.
- **Lightweight:** **Kokoro-ONNX**. Extremely fast, though Spanish support is evolving.
- **Workflow:** Set up an **XTTS API server** locally that Koda can call via a custom tool.

## 3. iPhone Local AI (MLX / CoreML)
- **Concept:** Run small quantized models directly on the iPhone's Neural Engine.
- **Model:** **Qwen3 4B** quantized to 4-bit. 
- **Tools:** Use the **MLX-Swift** library or **LLM Farm** / **Private LLM** apps to load GGUF/MLX models locally.

## 4. Recommendations
- Install **Ollama** on Windows to serve Qwen3 models.
- Prototype an **XTTS-Spanish** wrapper tool for Koda.
- Investigate **MLX-Swift** for a dedicated iPhone local "brain".
