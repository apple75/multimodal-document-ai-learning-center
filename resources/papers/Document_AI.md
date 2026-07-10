# Document AI

> **Multimodal Document AI Learning Center**
>
> **Module:** Document AI
>
> **Version:** v2.0
>
> **Last Updated:** July 2026
>
> 本文档介绍现代 **Document AI（文档智能）** 的发展历程、代表性论文以及最新研究进展。
>
> **学习目标**
>
> * 理解现代 Document AI 的发展脉络
> * 掌握文档理解的核心技术
> * 学习主流 Document Foundation Models
> * 为学习 Qwen-VL、DocTags、OmniDocBench 奠定理论基础

---

# Learning Roadmap

建议按照下面的路线学习。

```text
OCR
 │
 ▼
Document Layout Analysis
 │
 ▼
Document Foundation Models
 │
 ▼
Document Parsing
 │
 ▼
Structured Document Representation
 │
 ▼
Vision-Language Document Models
```

---

# Reading Strategy

| Priority | Description      |
| -------- | ---------------- |
| ⭐⭐⭐⭐⭐    | 必须精读（Master）     |
| ⭐⭐⭐⭐     | 建议精读（Understand） |
| ⭐⭐⭐      | 拓展阅读（Reference）  |

---

# Part 1. Introduction

## What is Document AI?

Document AI（文档智能）是人工智能的重要研究方向，其目标是让计算机能够像人一样理解复杂文档。

典型文档包括：

* PDF
* Word
* 扫描件
* 论文
* 合同
* 财务报表
* 发票
* 司法文书
* 病历
* 科技论文

现代 Document AI 不再局限于 OCR，而是关注：

* 文本理解（Text Understanding）
* 页面布局理解（Layout Understanding）
* 阅读顺序（Reading Order）
* 表格解析（Table Parsing）
* 公式识别（Formula Recognition）
* 图文关系（Vision-Language Understanding）
* 语义结构表示（Structured Document Representation）

---

# Part 2. Evolution of Document AI

```text
OCR
 │
 ▼
Layout Analysis
 │
 ▼
LayoutLM
 │
 ▼
LayoutLMv2
 │
 ▼
LayoutLMv3
 │
 ▼
Document Foundation Models
 │
 ▼
Vision-Language Models
 │
 ▼
DocTags
```

---

# Part 3. Classic Papers

---

## Paper 1

# LayoutLM

**Priority**

⭐⭐⭐⭐⭐

**Year**

2019

**Conference**

ACL

---

### Why It Matters

第一篇真正意义上的 **Document Pre-training Model**。

建立了：

Text + Layout

联合建模思想。

现代几乎所有 Document AI 都受到 LayoutLM 的影响。

---

### Main Contributions

* Layout Embedding
* BERT + Bounding Box
* Document Pre-training

---

### Students Should Learn

* Layout Embedding
* 2D Position Encoding
* OCR Token Representation

---

### Keywords

Layout

Bounding Box

Document Representation

---

## Paper 2

# LayoutLMv2

**Priority**

⭐⭐⭐⭐⭐

**Year**

2020

**Conference**

ACL Findings

---

### Main Contributions

首次统一：

* Text
* Image
* Layout

三种信息。

---

### Why Read

真正进入：

Multi-modal Document Understanding

时代。

---

### Students Should Learn

* Cross-modal Attention
* Visual Backbone
* Multi-modal Pre-training

---

## Paper 3

# LayoutLMv3

**Priority**

⭐⭐⭐⭐⭐

**Year**

2022

**Conference**

ACM MM

---

### Main Contributions

统一：

* Text Masking
* Image Masking
* Word-Patch Alignment

采用统一 Transformer。

---

### Why Read

目前仍然是：

Document AI Baseline

之一。

---

### Students Should Learn

* Unified Pre-training
* Patch Embedding
* Joint Learning

---

# Part 4. Document Foundation Models

---

## Paper 4

# DocFormer

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

提出：

End-to-End Multi-modal Transformer

适合理解：

Text + Vision

联合学习。

---

### Main Contributions

* Shared Transformer
* Multi-modal Encoder
* End-to-End Learning

---

## Paper 5

# DiT

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

Document Image Transformer。

首次证明：

Document Image

可以进行：

Self-supervised Learning。

---

### Students Should Learn

* Image-only Representation
* Self-supervised Learning
* Document Vision Backbone

---

## Paper 6

# DocLLM

**Priority**

⭐⭐⭐⭐

---

### Why Read

提出：

面向文档理解的大语言模型。

开始进入：

LLM + Document

时代。

---

### Students Should Learn

* Instruction Tuning
* Document QA
* Layout-aware LLM

---

# Part 5. OCR Foundation

---

## Paper 7

# PaddleOCR

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

目前工业界应用最广泛的 OCR 框架之一。

---

### Students Should Learn

* Detection
* Recognition
* PP-OCR Pipeline

---

## Paper 8

# PaddleOCR-VL

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

代表 OCR 从传统 Pipeline 向 Vision-Language Model 演进的重要方向。

特点：

* End-to-End
* 多元素识别
* 表格
* 公式
* 图表
* 多语言

对于理解新一代 OCR 系统具有重要价值。

---

## Paper 9

# TrOCR

**Priority**

⭐⭐⭐⭐

---

### Why Read

Transformer OCR。

OCR End-to-End

经典工作。

---

# Part 6. Scientific Document Parsing

---

## Paper 10

# Nougat

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

Meta 提出：

PDF

↓

Markdown

直接生成。

影响：

整个 Scientific Document Parsing

方向。

---

### Students Should Learn

* Sequence Generation
* OCR-free Parsing
* Markdown Generation

---

## Paper 11

# MinerU

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

目前开源社区影响力最大的 PDF Parsing 工具之一。

特点：

* 高质量 Markdown
* Table
* Formula
* Reading Order

建议结合官方技术报告和 GitHub 一起学习。

---

## Paper 12

# Docling

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

IBM 开源文档处理框架。

支持：

* PDF
* DOCX
* PPT
* HTML

统一转换为：

* Markdown
* JSON
* HTML

是现代 Agent 与 RAG 文档预处理的重要工具。

---

## Paper 13

# SmolDocling

**Priority**

⭐⭐⭐⭐⭐

---

### Why Read

轻量级 Document AI 模型。

特点：

* 小模型
* 快速推理
* Markdown Generation

非常适合作为：

教学

科研

部署

实验平台。

---

# Part 7. Modern Trends (2024–2026)

近年来，Document AI 的研究重点已经发生变化。

传统研究重点：

```text
OCR
```

↓

现代研究重点：

```text
Structured Document Representation
```

↓

未来研究重点：

```text
Document Foundation Model

↓

Document Agent

↓

Document Reasoning
```

目前值得重点关注的方向包括：

* OCR-free Document Parsing
* End-to-End Document Understanding
* Vision-Language Foundation Models
* Structured Document Representation（DocTags）
* Document Agent
* Long Context Document Understanding

---

# Part 8. Reading Order

建议按照下面顺序阅读。

| Week   | Papers       |
| ------ | ------------ |
| Week 1 | LayoutLM     |
| Week 1 | LayoutLMv2   |
| Week 2 | LayoutLMv3   |
| Week 2 | DocFormer    |
| Week 3 | DiT          |
| Week 3 | PaddleOCR    |
| Week 4 | PaddleOCR-VL |
| Week 4 | TrOCR        |
| Week 5 | Nougat       |
| Week 5 | MinerU       |
| Week 6 | Docling      |
| Week 6 | SmolDocling  |

---

# Knowledge Checklist

完成本章节后，应能够回答：

## Layout

* 什么是 Layout Embedding？
* 为什么需要 Bounding Box？
* 为什么 Document AI 不能只使用 OCR？

---

## Multi-modal

* Text 与 Image 如何联合建模？
* 为什么需要 Cross-modal Attention？

---

## Document Foundation Models

* 什么是统一预训练？
* 什么是 OCR-free？
* 为什么越来越多模型直接生成 Markdown？

---

## Modern OCR

* PaddleOCR 与 PaddleOCR-VL 有什么区别？
* TrOCR 与传统 OCR 有什么不同？

---

## Scientific Documents

* Nougat 为什么重要？
* MinerU 与 Docling 有什么区别？
* SmolDocling 为什么适合轻量级部署？

---

# Connection to Our Laboratory

本实验室研究方向如下：

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
Multimodal Document Agent
```

因此，本章节是整个课程体系的核心基础之一。

完成本章节后，应能够理解：

* 为什么现代 Document AI 正从 OCR 转向结构化表示；
* 为什么 Markdown、JSON、DocTags 等语义表示越来越重要；
* 为什么 Vision-Language Model 正逐渐成为统一的文档理解框架。

---

# Recommended Next Reading

完成本章节后，请继续阅读：

> **vlm.md**

重点学习：

* Qwen 系列 Vision-Language Models
* Florence-2
* InternVL
* DeepSeek-VL2
* Molmo
* Pixtral
* Modern Multimodal Foundation Models

进一步理解现代多模态大模型如何推动新一代 Document AI 的发展。
