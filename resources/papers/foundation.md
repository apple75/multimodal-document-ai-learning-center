# Foundation Models

> **Multimodal Document AI Learning Center**
>
> **Module:** Foundation Models
>
> **Version:** v2.0
>
> **Last Updated:** July 2026
>
> 本文档介绍现代人工智能发展的基础模型（Foundation Models），重点关注对 **Document AI、Vision-Language Model（VLM）、DocTags、多模态大模型** 具有深远影响的经典论文与代表性工作。
>
> **阅读目标：**
>
> * 理解 Transformer 的发展脉络
> * 掌握现代 Foundation Model 的核心思想
> * 建立后续学习 VLM 与 Document AI 的理论基础

---

# Learning Roadmap

建议按照下面的顺序阅读。

```text
Transformer
      │
      ▼
BERT
      │
      ▼
Vision Transformer (ViT)
      │
      ▼
CLIP
      │
      ▼
BLIP-2
      │
      ▼
SigLIP / SigLIP 2
      │
      ▼
Modern Vision-Language Foundation Models
```

---

# Reading Strategy

建议采用以下原则：

| Priority | Description                          |
| -------- | ------------------------------------ |
| ⭐⭐⭐⭐⭐    | 必读（Every graduate student must read） |
| ⭐⭐⭐⭐     | 建议精读                                 |
| ⭐⭐⭐      | 根据研究方向阅读                             |

---

# Part 1. Transformer Era

---

## Paper 1

### Attention Is All You Need

**Priority**

⭐⭐⭐⭐⭐

**Year**

2017

**Conference**

NeurIPS

**Keywords**

Transformer

Self-Attention

Encoder-Decoder

---

### Why It Matters

这是现代人工智能最重要的论文之一。

几乎所有现代基础模型均建立在 Transformer 架构之上，包括：

* GPT
* BERT
* ViT
* CLIP
* Qwen
* Llama
* DeepSeek
* InternVL

---

### Main Contributions

* 提出 Self-Attention
* 完全去除 RNN
* 完全并行训练
* 建立现代 Transformer 架构

---

### Must Understand

学生必须理解：

* Self-Attention
* Multi-Head Attention
* Positional Encoding
* Encoder
* Decoder

---

### Recommended Reading Time

Week 1

---

# Part 2. Language Foundation Models

---

## Paper 2

### BERT

**Priority**

⭐⭐⭐⭐⭐

**Year**

2018

**Conference**

NAACL

---

### Main Contributions

* Bidirectional Pre-training
* Masked Language Model
* Next Sentence Prediction

---

### Why Read

几乎所有现代 NLP 模型都受到 BERT 的影响。

很多 Document AI 模型（例如 LayoutLM）直接继承了 BERT 的思想。

---

### Students Should Learn

* MLM
* Fine-tuning
* Pre-training
* Encoder-only Architecture

---

## Paper 3

### RoBERTa

**Priority**

⭐⭐⭐⭐

---

### Why Read

告诉大家：

模型并不是因为结构更好，而是：

训练得更充分。

RoBERTa 是理解：

"Scaling Matters"

最好的论文之一。

---

# Part 3. Vision Foundation Models

---

## Paper 4

### An Image is Worth 16×16 Words (Vision Transformer)

**Priority**

⭐⭐⭐⭐⭐

**Conference**

ICLR 2021

---

### Main Contributions

首次证明：

Transformer 可以完全替代 CNN。

---

### Why Read

所有现代 VLM：

* Qwen-VL
* Florence
* InternVL
* SmolDocling

都采用 ViT 或其变体作为视觉编码器。

---

### Students Should Learn

* Patch Embedding
* CLS Token
* Vision Encoder

---

# Part 4. Vision-Language Foundation Models

---

## Paper 5

### CLIP

**Priority**

⭐⭐⭐⭐⭐

**Organization**

OpenAI

---

### Main Contributions

首次提出：

Image + Text Contrastive Learning

建立统一视觉语义空间。

---

### Why Read

CLIP 对整个多模态领域影响巨大。

现代：

* Retrieval
* VLM
* OCR
* Agent

均受到 CLIP 思想影响。

---

### Students Should Learn

* Contrastive Learning
* Image Encoder
* Text Encoder
* Zero-shot Learning

---

## Paper 6

### BLIP-2

**Priority**

⭐⭐⭐⭐⭐

**Conference**

ICML 2023

---

### Main Contributions

提出：

Q-Former

连接：

Frozen Vision Encoder

*

Frozen LLM

成为现代多模态模型的重要设计路线。

---

### Why Read

理解：

为什么现代 VLM 不再端到端训练全部参数。

---

### Students Should Learn

* Frozen Encoder
* Frozen LLM
* Q-Former

---

## Paper 7

### SigLIP

**Priority**

⭐⭐⭐⭐

---

### Why Read

Google 提出的新一代 Image-Text Alignment 方法。

采用 Sigmoid Loss 替代传统 CLIP Loss。

提高训练稳定性。

---

## Paper 8

### SigLIP 2

**Priority**

⭐⭐⭐⭐⭐

**Year**

2025

---

### Main Contributions

* 多语言 Vision-Language Encoder
* 更好的语义理解
* 更强 Localization
* 更好的 Dense Features
* 更适合作为现代 VLM 的视觉基础模型。

---

### Why Read

代表 Vision Encoder 最新的发展方向。

---

# Part 5. Efficient Foundation Models

---

## Paper 9

### FlashAttention

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

现代 Transformer 加速的重要基础。

几乎所有大模型推理框架：

* vLLM
* TensorRT-LLM
* SGLang

均采用类似思想。

---

## Paper 10

### FlashAttention-2

**Priority**

⭐⭐⭐⭐⭐

---

### Main Contributions

进一步提高：

* Training Speed
* Inference Speed
* GPU Utilization

---

### Why Read

理解现代高性能推理框架。

---

# Part 6. Modern Trends (2024–2026)

下面几篇论文建议了解，不要求第一次阅读全部掌握。

| Paper       | Why Read                      |
| ----------- | ----------------------------- |
| MetaCLIP 2  | 全球多语言 CLIP 扩展，代表最新视觉-语言预训练趋势。 |
| SigLIP 2    | 最新 Vision Encoder。            |
| MobileCLIP2 | 轻量化 Vision Foundation Model。  |

---

# Reading Order

建议按照下面顺序阅读。

| Week   | Papers                    |
| ------ | ------------------------- |
| Week 1 | Attention Is All You Need |
| Week 1 | BERT                      |
| Week 2 | Vision Transformer        |
| Week 2 | CLIP                      |
| Week 3 | BLIP-2                    |
| Week 3 | SigLIP                    |
| Week 4 | SigLIP 2                  |
| Week 4 | FlashAttention            |

---

# Knowledge Checklist

完成本章节后，应能够回答以下问题。

## Transformer

* 什么是 Self-Attention？
* 为什么不用 RNN？
* 为什么可以并行训练？

---

## BERT

* 什么是 MLM？
* 为什么是双向编码？

---

## ViT

* 为什么图片可以切成 Patch？
* Patch Embedding 是什么？

---

## CLIP

* 为什么 Image 和 Text 可以放到同一个空间？
* 什么是 Contrastive Learning？

---

## BLIP-2

* 为什么需要 Q-Former？
* Frozen LLM 有什么优势？

---

## Foundation Models 与实验室研究

完成本章节后，应能够理解：

```text
Transformer
      │
      ▼
BERT
      │
      ▼
ViT
      │
      ▼
CLIP
      │
      ▼
BLIP-2
      │
      ▼
Qwen / InternVL / Florence
      │
      ▼
Document AI
      │
      ▼
DocTags
      │
      ▼
Multimodal AI Agent
```

这也是 **Multimodal Document AI Laboratory** 后续所有课程、实验和科研项目的理论基础。

---

# Recommended Next Reading

完成本章节后，继续阅读：

> **document_ai.md**

重点学习：

* LayoutLM
* LayoutLMv2
* LayoutLMv3
* DocFormer
* DiT
* Document Foundation Models

为后续 **Qwen3-VL、DocTags、OmniDocBench** 的学习建立完整理论基础。
