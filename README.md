# Unsloth Fine-Tuning: Phi-3-mini

This project demonstrates how to fine-tune the **Phi-3-mini-4k-instruct** model using the **Unsloth** library. Unsloth provides highly optimized kernels that make LLM fine-tuning up to 2x faster with 70% less memory usage.

## 🚀 Overview

This project is optimized for **Google Colab (T4 GPU)** and provides a seamless walkthrough for fine-tuning LLMs. The notebook included in this repository (`unsloth_fine_tune.ipynb`) covers the entire pipeline of supervised fine-tuning (SFT):

1.  **Environment Setup**: Installing the necessary optimized libraries.
2.  **Model Loading**: Initializing the 4-bit quantized Phi-3 model.
3.  **Data Preparation**: Formatting a custom JSON dataset for instruction tuning.
4.  **LoRA Configuration**: Setting up Low-Rank Adaptation for efficient training.
5.  **Training**: Running the supervised fine-tuning loop.
6.  **Inference**: Testing the fine-tuned model's responses.
7.  **Export**: Converting the model to GGUF format for local deployment.
8.  **Local Testing**: Verifying the GGUF model using `llama-cpp-python`.

## 🛠️ Prerequisites

- **Google Colab** (Recommended: T4 GPU Runtime)
- NVIDIA GPU (T4, V100, A100, etc.)
- Python 3.10+
- PyTorch and CUDA installed

## 📥 Installation

The primary dependency is the Unsloth library. You can install it using:

```bash
pip install unsloth
```

For the local GGUF inference step, you will also need:

```bash
pip install -U llama-cpp-python
```

## 📊 Dataset

The training process expects a file named `people_data.json` containing pairs of prompts and responses. The notebook automatically formats these into the model's chat template.

## 💾 Exporting and Deployment

One of the highlights of this project is the seamless export to **GGUF format**. This allows you to run your fine-tuned model on local hardware with high performance using `llama.cpp`.

## ✨ Features

- **Fast Kernels**: Powered by Unsloth for rapid iterations.
- **4-bit Quantization**: Train on consumer-grade GPUs with minimal VRAM.
- **PEFT/LoRA**: Memory-efficient adaptation of large models.
- **GGUF Ready**: Export models directly for production or local use.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
