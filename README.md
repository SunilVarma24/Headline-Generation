# News Headline Generation

## Project Overview
This project focuses on **news headline generation** using **T5 (Text-To-Text Transfer Transformer)** fine-tuned with **Low-Rank Adaptation (LoRA)**. The goal is to generate short, accurate, and context-aware headlines for a wide variety of news articles. The model is optimized for the **METEOR metric**, and achieves a **47% improvement** over the baseline T5 model, demonstrating the effectiveness of parameter-efficient fine-tuning techniques.

## Introduction
Generating news headlines is a challenging **sequence-to-sequence (Seq2Seq)** task that requires understanding and summarizing lengthy article content into a single, concise sentence. This project leverages the **T5-base** architecture and applies **LoRA**, a parameter-efficient fine-tuning method, to train only a small subset of the model weights, significantly reducing memory usage and training time.

Instead of full fine-tuning or layer freezing, this method focuses on **FP16 precision + LoRA adapters**, allowing highly efficient and scalable headline generation across ~98K news samples.

## Key Highlights  
- 🧠 Fine-tuned a **T5-Base** model using **LoRA** on **98,400 news samples**  
- 💾 Used **FP16 precision** to reduce memory usage  
- 🔧 Only **1.56% of parameters** (3.5M / 226M) were trained using LoRA adapters  
- 🚀 Achieved **47% improvement in METEOR** score:
  - **Baseline T5**: 0.32  
  - **T5 + LoRA**: 0.47  
- 📈 Significantly improved generation quality through **parameter-efficient training**

## Dataset
The dataset used in this project consists of pairs of news articles and their corresponding headlines. The dataset includes diverse news categories such as politics, sports, technology, and entertainment, providing a comprehensive training set for the model.

## Evaluation Metrics  

The main evaluation metric used is **METEOR**, which is well-suited for summarization and generation tasks.

| Model        | METEOR Score |
|--------------|--------------|
| T5-Base (raw) | 0.32         |
| T5 + LoRA     | 0.47 ✅      |

This **47% improvement** reflects better alignment between generated and reference headlines in terms of **content, fluency, and structure**.

## Installation
To run this project, you need Python 3.x installed.

You can install the required packages using pip:
```bash
pip install requirements.txt
