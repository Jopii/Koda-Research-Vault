# Report: Spanish TTS Benchmark - January 30, 2026 (v1.0)
**Date:** 2026-01-30
**Status:** Performance Research

## 1. Top Recommendation: Kokoro-TTS (82M)
Kokoro-TTS has established itself as the most efficient model for local deployment in early 2026.
- **Parameters:** ~82 million (extremely lightweight).
- **Speed:** ~96x real-time speed on mid-range GPUs (like your RTX 3060).
- **Quality:** Ranks #9 globally on Artificial Analysis (Open-Weight category).
- **Language Support:** Native Spanish variants included.
- **Why it fits:** It can easily run alongside your LLM without consuming significant VRAM.

## 2. Professional Multilingual: Fish Speech 1.5
- **Quality:** Industry-leading multilingual quality (ELO 1,339 in TTS Arena).
- **Architecture:** DualAR architecture trained on 300k+ hours of data.
- **Cons:** Higher resource requirements compared to Kokoro; Spanish performance is high quality but requires more VRAM.

## 3. Comparison
| Model | Size | Speed | Spanish Quality | Local API Ease |
|-------|------|-------|-----------------|----------------|
| **Kokoro** | 82M | Extreme | High (Efficient) | High (ONNX/Torch) |
| **Fish Speech** | Large | Moderate | Very High | Medium |
| **XTTS v2** | Medium | Good | Reference Level | High |

## 4. Koda's Implementation Recommendation
I recommend Jesus starts with **Kokoro-TTS (ONNX version)**. It provides the best "quality-to-VRAM" ratio for a background assistant like me.

## 5. Next Steps
- Download Kokoro-TTS Spanish weights.
- Prototype a local Python API for Kokoro.
