# Vision-Language Models (VLM)

> **Multimodal Document AI Learning Center**
>
> **Module:** Vision-Language Models (VLM)
>
> **Version:** v2.0
>
> **Last Updated:** July 2026
>
> 本文档介绍现代 **Vision-Language Models (VLM)** 的发展历程、代表性模型及最新研究进展，重点关注对 **Document AI、DocTags、多模态 Agent** 具有重要影响的开源模型。
>
> **Learning Objectives**
>
> * 理解 Vision-Language Model 的发展路线
> * 掌握现代多模态大模型的核心架构
> * 学习主流开源 VLM 的设计思想
> * 为 Qwen、DocTags、OmniDocBench 等研究奠定理论基础

---

# Learning Roadmap

建议按照下面的顺序学习。

```text
CLIP
 │
 ▼
BLIP-2
 │
 ▼
LLaVA
 │
 ▼
Florence-2
 │
 ▼
Qwen2.5-VL
 │
 ▼
InternVL
 │
 ▼
Modern Open VLM
 │
 ▼
Document AI
 │
 ▼
DocTags
```

---

# Reading Strategy

| Priority | Description      |
| -------- | ---------------- |
| ⭐⭐⭐⭐⭐    | 必须精读（Master）     |
| ⭐⭐⭐⭐     | 建议精读（Understand） |
| ⭐⭐⭐      | 拓展阅读（Reference）  |

---

# Part 1. What is a Vision-Language Model?

Vision-Language Model（VLM）是一类能够**联合理解图像、文本以及视觉语义**的大模型。

现代 VLM 已经不仅能够回答图片问题，还能够完成：

* OCR
* 表格理解
* 图表分析
* UI 理解
* 文档解析
* Visual Grounding
* Agent 操作
* 长视频理解
* 多图推理

对于 Document AI 而言，VLM 正逐渐成为统一的技术路线。

---

# Part 2. Evolution of Vision-Language Models

```text
CLIP
 │
 ▼
BLIP-2
 │
 ▼
LLaVA
 │
 ▼
Instruction Tuning
 │
 ▼
Native Vision Encoder
 │
 ▼
Modern Open VLM
 │
 ▼
Document Understanding
 │
 ▼
AI Agent
```

---

# Part 3. Foundation Vision-Language Models

## Paper 1

# CLIP

**Priority**

⭐⭐⭐⭐⭐

**Organization**

OpenAI

### Main Contributions

* Contrastive Learning
* Unified Vision-Text Embedding
* Zero-shot Recognition

### Why Read

现代几乎所有 VLM 都继承了 CLIP 的思想。

### Students Should Learn

* Contrastive Learning
* Dual Encoder
* Image Embedding
* Text Embedding

---

## Paper 2

# BLIP-2

**Priority**

⭐⭐⭐⭐⭐

**Conference**

ICML 2023

### Main Contributions

提出：

Q-Former

实现：

Frozen Vision Encoder

*

Frozen LLM

之间的高效连接。

### Why Read

现代大量开源 VLM 采用类似设计。

---

## Paper 3

# LLaVA

**Priority**

⭐⭐⭐⭐⭐

### Why Read

LLaVA 推动了 Instruction Tuning 在 VLM 中的普及。

首次让：

Image

*

Conversation

成为统一输入。

### Students Should Learn

* Instruction Tuning
* Visual Chat
* Multi-modal Alignment

---

# Part 4. Modern Open Vision-Language Models

---

## Paper 4

# Florence-2

**Priority**

⭐⭐⭐⭐⭐

**Organization**

Microsoft

### Main Contributions

提出：

Vision Foundation Model

支持：

* OCR
* Caption
* Detection
* Segmentation
* Region Understanding

统一到一个模型。

### Why Read

Florence-2 是目前最重要的 Vision Foundation Model 之一。

建议理解：

Prompt-based Vision Tasks。

---

## Paper 5

# Florence-VL

**Priority**

⭐⭐⭐⭐

**Conference**

CVPR 2025

### Main Contributions

利用 Florence-2 作为生成式视觉编码器，并提出 **Depth-Breadth Fusion（DBFusion）**，提升视觉表示质量，增强多模态推理能力。

### Why Read

代表了新一代 Vision Encoder 与 LLM 深度融合的发展方向。

---

## Paper 6

# Qwen2.5-VL Technical Report

**Priority**

⭐⭐⭐⭐⭐

**Year**

2025

### Main Contributions

Qwen2.5-VL 是目前最具代表性的开源 Vision-Language Model 之一。

主要创新包括：

* Native Dynamic Resolution Vision Transformer
* Window Attention
* Absolute Time Encoding
* 高质量 Document Parsing
* Visual Grounding
* Long Video Understanding
* Visual Agent

同时支持：

* OCR
* Chart
* Table
* Formula
* Layout
* UI
* Mobile Agent

等任务。

### Why Read

对于 **Document AI** 而言，

Qwen2.5-VL 是目前最值得深入研究的开源模型之一。

也是本课程后续实验的核心模型。

### Students Should Learn

* Native Resolution
* Dynamic Resolution
* Vision Encoder
* Window Attention
* Visual Grounding
* Document Parsing

---

## Paper 7

# InternVL

**Priority**

⭐⭐⭐⭐⭐

### Why Read

InternVL 是目前最重要的开源大型 Vision-Language Model 系列之一。

特点：

* Strong OCR
* Multi-image Reasoning
* Long Context
* Excellent Multilingual Ability

建议重点理解：

Visual Token Compression

以及：

Large-scale Multi-modal Training。

---

## Paper 8

# DeepSeek-VL2

**Priority**

⭐⭐⭐⭐⭐

### Why Read

DeepSeek-VL2 是近年来国产开源 VLM 的代表工作。

特点：

* 高性能 OCR
* 多图推理
* Document Understanding
* Agent 能力增强

适合作为：

Qwen

InternVL

之间的重要比较对象。

---

## Paper 9

# Molmo

**Priority**

⭐⭐⭐⭐⭐

**Conference**

CVPR 2025

### Main Contributions

Molmo 提供了开放权重与开放数据（PixMo），强调开放生态下的高性能 VLM。

### Why Read

理解：

开放数据

*

开放模型

对于未来 Vision-Language Research 的意义。

---

## Paper 10

# Pixtral

**Priority**

⭐⭐⭐⭐

### Why Read

Pixtral 是近年来开源 VLM 的重要代表。

建议关注：

* Large Context
* Multi-image
* Visual Reasoning

---

# Part 5. Lightweight Vision-Language Models

现代 VLM 不再只有：

70B

100B

而是开始出现：

```text
450M

↓

1B

↓

2B

↓

3B
```

适合：

* Edge AI
* Notebook
* Jetson
* Mobile

代表模型包括：

* Qwen 3B
* Qwen 7B
* SmolDocling
* MiniCPM-V
* LFM2.5-VL

轻量化模型正在成为产业部署的重要方向。

---

# Part 6. Vision-Language Models for Document AI

现代 VLM 已逐渐替代传统 OCR Pipeline。

典型能力包括：

| Capability       | Traditional OCR | Modern VLM |
| ---------------- | --------------- | ---------- |
| OCR              | ✓               | ✓          |
| Layout           | Limited         | ✓          |
| Table            | Partial         | ✓          |
| Formula          | Partial         | ✓          |
| Chart            | ✗               | ✓          |
| Reading Order    | ✗               | ✓          |
| Document QA      | ✗               | ✓          |
| Visual Grounding | ✗               | ✓          |
| Agent            | ✗               | ✓          |

因此：

现代 Document AI

=

Vision-Language Model

*

Structured Representation

---

# Part 7. Current Research Trends (2025–2026)

值得重点关注的发展方向：

## Native Resolution Vision Encoder

代表：

* Qwen2.5-VL

---

## Visual Grounding

模型能够直接输出：

* Bounding Box
* Point
* Region

---

## OCR-free Parsing

未来越来越多模型：

Image

↓

Markdown

直接生成。

---

## Long-context Vision

能够处理：

* 超长 PDF
* 长视频
* 多页文档

---

## Vision Agent

模型开始能够：

* 点击按钮
* 操作电脑
* 操作手机
* 调用工具

形成：

AI Agent。

---

# Part 8. Recommended Reading Order

| Week   | Papers                      |
| ------ | --------------------------- |
| Week 1 | CLIP                        |
| Week 1 | BLIP-2                      |
| Week 2 | LLaVA                       |
| Week 2 | Florence-2                  |
| Week 3 | Qwen2.5-VL Technical Report |
| Week 3 | InternVL                    |
| Week 4 | DeepSeek-VL2                |
| Week 4 | Molmo                       |
| Week 5 | Pixtral                     |

---

# Knowledge Checklist

完成本章节后，应能够回答：

## Vision Encoder

* 为什么 ViT 可以替代 CNN？
* 什么是 Native Resolution？

---

## Multi-modal Alignment

* 为什么需要 Alignment？
* 为什么需要 Instruction Tuning？

---

## Qwen2.5-VL

* Dynamic Resolution 有什么优势？
* Window Attention 如何降低计算量？
* 为什么 Qwen2.5-VL 在文档解析方面表现突出？

---

## Modern VLM

* 为什么越来越多模型支持 Visual Grounding？
* 为什么 VLM 可以替代传统 OCR Pipeline？

---

# Connection to Our Laboratory

实验室整体研究路线如下：

```text
Foundation Models
      │
      ▼
Vision-Language Models
      │
      ▼
Document AI
      │
      ▼
Structured Document Representation
      │
      ▼
DocTags
      │
      ▼
OmniDocBench
      │
      ▼
Multimodal AI Agent
```

其中：

**Vision-Language Model**

是整个研究体系的核心技术平台。

后续所有课程：

* Qwen3-VL
* SmolDocling
* OmniDocBench
* DocTags
* Document Agent

均建立在本章节知识基础之上。

---

# Recommended Next Reading

完成本章节后，请继续阅读：

> **doctags.md**

重点学习：

* Structured Document Representation
* Markdown
* DocTags
* Docling
* MinerU
* Semantic Rendering
* Reading Order

进入现代 **Document AI** 最重要的研究方向——**结构化文档表示（Structured Document Representation）**。
