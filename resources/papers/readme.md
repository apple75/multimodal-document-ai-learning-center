
# Paper Library

> **Multimodal Document AI Learning Center**
>
> This page provides a curated reading roadmap for graduate students and researchers working on **Multimodal Document AI**, **Vision-Language Models (VLMs)**, **Document Parsing**, **DocTags**, and **Document Benchmarks**.
>
> **Last Updated:** July 2026

---

# Reading Roadmap

建议所有实验室成员按照下面的顺序阅读论文。

```text
Foundation Models
        │
        ▼
Document AI
        │
        ▼
Vision-Language Models
        │
        ▼
Structured Document Representation (DocTags)
        │
        ▼
Benchmarks & Evaluation
        │
        ▼
Research Papers
```

---

# Top 20 Recommended Papers

| Priority | Paper                       | Category                | Difficulty |
| -------- | --------------------------- | ----------------------- | ---------- |
| ⭐⭐⭐⭐⭐    | Attention Is All You Need   | Foundation              | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | BERT                        | Foundation              | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | CLIP                        | Vision-Language         | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | LayoutLM                    | Document AI             | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | LayoutLMv2                  | Document AI             | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | LayoutLMv3                  | Document AI             | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | DocFormer                   | Document AI             | ⭐⭐⭐        |
| ⭐⭐⭐⭐⭐    | DiT                         | Document AI             | ⭐⭐⭐        |
| ⭐⭐⭐⭐⭐    | PaddleOCR                   | OCR                     | ⭐          |
| ⭐⭐⭐⭐⭐    | TrOCR                       | OCR                     | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | Florence-2                  | Vision Foundation Model | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | InternVL                    | Vision-Language Model   | ⭐⭐⭐        |
| ⭐⭐⭐⭐⭐    | Qwen2.5-VL Technical Report | Vision-Language Model   | ⭐⭐⭐        |
| ⭐⭐⭐⭐⭐    | DeepSeek-VL2                | Vision-Language Model   | ⭐⭐⭐        |
| ⭐⭐⭐⭐⭐    | Docling Technical Report    | Structured Documents    | ⭐⭐         |
| ⭐⭐⭐⭐⭐    | OmniDocBench                | Benchmark               | ⭐⭐         |
| ⭐⭐⭐⭐     | PubTabNet                   | Benchmark               | ⭐⭐         |
| ⭐⭐⭐⭐     | DocVQA                      | Benchmark               | ⭐⭐         |
| ⭐⭐⭐⭐     | FUNSD                       | Benchmark               | ⭐          |
| ⭐⭐⭐⭐     | BLIP-2                      | Vision-Language Model   | ⭐⭐⭐        |

---

# Reading Categories

## 1. Foundation Models

学习现代大模型的基础理论。

建议阅读：

* Attention Is All You Need
* BERT
* CLIP
* BLIP-2

📄 Foundation Papers

👉 foundation.md

---

## 2. Document AI

学习现代 Document AI 的核心模型。

建议阅读：

* LayoutLM
* LayoutLMv2
* LayoutLMv3
* DocFormer
* DiT

📄 Document AI Papers

👉 document_ai.md

---

## 3. Vision-Language Models (VLM)

学习当前主流多模态模型。

建议阅读：

* Qwen3.5-VL Technical Report
* Florence-2
* InternVL
* DeepSeek-VL2
* SmolDocling（Model Card）

📄 Vision-Language Papers

👉 vlm.md

---

## 4. Structured Document Representation (DocTags)

这是实验室当前重点研究方向。

重点关注：

* Semantic Document Representation
* Markdown Generation
* Structured Parsing
* Reading Order
* Table Parsing
* Formula Parsing
* DocTags

推荐资料：

* Docling Technical Report
* Docling GitHub
* MinerU
* MarkItDown
* SmolDocling
* OmniDocBench

📄 DocTags Papers

👉 doctags.md

---

## 5. Benchmarks

Document AI Benchmark 是实验室科研工作的基础。

建议阅读：

* OmniDocBench（CVPR 2025）
* DocVQA
* PubTabNet
* FUNSD
* OCRBench
* CC-OCR

📄 Benchmark Papers

👉 benchmarks.md

---

# Papers Closely Related to Our Research

以下论文与实验室研究方向高度相关，建议优先阅读。

| Paper                       | Importance |
| --------------------------- | ---------- |
| Qwen3.5-VL Technical Report | ⭐⭐⭐⭐⭐      |
| LayoutLMv3                  | ⭐⭐⭐⭐⭐      |
| Docling Technical Report    | ⭐⭐⭐⭐⭐      |
| OmniDocBench                | ⭐⭐⭐⭐⭐      |
| Florence-2                  | ⭐⭐⭐⭐       |
| InternVL                    | ⭐⭐⭐⭐       |
| DeepSeek-VL2                | ⭐⭐⭐⭐       |
| PaddleOCR                   | ⭐⭐⭐⭐       |
| MinerU                      | ⭐⭐⭐⭐       |
| SmolDocling                 | ⭐⭐⭐⭐       |

---

# Suggested Reading Plan

## Week 1

Foundation

* Attention Is All You Need
* BERT
* CLIP

---

## Week 2

Document AI

* LayoutLM
* LayoutLMv2
* LayoutLMv3

---

## Week 3

Vision-Language Models

* Florence-2
* InternVL
* Qwen2.5-VL Technical Report

---

## Week 4

Structured Document Representation

* Docling Technical Report
* MinerU
* SmolDocling
* MarkItDown

---

## Week 5

Benchmarks

* OmniDocBench
* DocVQA
* PubTabNet

---

# Reading Requirements

实验室建议采用统一论文阅读规范。

对于每篇论文，至少完成以下内容：

* Research Background
* Problem Statement
* Main Contributions
* Model Architecture
* Dataset
* Experimental Results
* Advantages
* Limitations
* Future Work
* Personal Notes

建议每篇论文整理为一份 Markdown 阅读笔记，并提交到实验室 GitHub。

---

# Related Learning Chapters

本课程建议结合以下章节一起学习：

| Chapter       | Topic                   |
| ------------- | ----------------------- |
| Chapter 06    | Qwen3.5-VL              |
| Chapter 07    | SmolDocling             |
| Chapter 08    | Document AI             |
| Chapter 09    | DocTags                 |
| Experiment 01 | First Inference         |
| Experiment 02 | OmniDocBench Evaluation |

---

# Paper Library Structure

```text
papers/

README.md

foundation.md

document_ai.md

vlm.md

doctags.md

benchmarks.md

surveys.md
```

每个专题文档均持续更新，与实验室研究方向保持同步。
