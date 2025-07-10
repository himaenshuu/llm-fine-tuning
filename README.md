# 🚀 LLM Fine-Tuning with Unsloth + Hugging Face

> Fine-tune large language models (LLMs) like Mistral or LLaMA efficiently on custom instruction datasets using [Unsloth](https://github.com/unslothai/unsloth), [Hugging Face Transformers](https://huggingface.co/docs/transformers), and export to GGUF for fast inference via `llama.cpp`.

![Python](https://img.shields.io/badge/python-3.10+-blue)

![Status](https://img.shields.io/badge/status-active-success)

---

## 📌 Project Summary

This project demonstrates how to fine-tune an LLM on a custom instruction-based dataset using:

- 🧠 **Unsloth** for memory-efficient fine-tuning
- 🔧 **TRL’s `SFTTrainer`** from Hugging Face for supervised training
- 💾 **GGUF Export** for inference-ready deployment (supports `llama.cpp`, `llamafile`, etc.)
- 📊 Optional **W&B tracking** for experiment visualization

---

## 🧱 Tech Stack

| Component       | Tool/Library               |
|-----------------|----------------------------|
| Model           | Mistral / LLaMA            |
| Trainer         | TRL's `SFTTrainer`         |
| Optimization    | AdamW (8-bit), LR Schedulers |
| Quantization    | 8-bit / 4-bit via GGUF     |
| Logging         | Weights & Biases (optional) |
| Hardware Target | Colab / Kaggle GPU         |

---

## ✅ Features

- 🔧 Fine-tunes **Mistral** or **LLaMA** models with minimal VRAM requirements
- 🧠 Supports **instruction tuning** for domain-specific and structured tasks
- ⚡ Trains with **8-bit optimizer** using `bitsandbytes` for faster and lighter execution
- 📦 Exports the final model in **GGUF format** compatible with `llama.cpp`, `llamafile`, etc.
- 🎯 Runs on **Kaggle**, **Google Colab**, or custom local GPU environments
- 📊 Optional **Weights & Biases (W&B)** logging for real-time experiment tracking

---

## 🧪 Training Configuration

| Hyperparameter        | Value                |
|------------------------|----------------------|
| Epochs                | 2–3                  |
| Batch Size            | 2 (with accumulation = 8) |
| Max Steps             | 100                  |
| Learning Rate         | 2e-4                 |
| Optimizer             | AdamW (8-bit)        |
| Precision             | fp16 / bf16          |
| Quantization          | GGUF export (8-bit)  |

---

