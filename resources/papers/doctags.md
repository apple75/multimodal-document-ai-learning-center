# Structured Document Representation (DocTags)

> **Multimodal Document AI Learning Center**
>
> **Module:** Structured Document Representation (DocTags)
>
> **Version:** v2.0
>
> **Last Updated:** July 2026
>
> 本文档介绍现代 **Structured Document Representation（结构化文档表示）** 的发展趋势，重点关注 **DocTags、Markdown、Docling、MinerU、Semantic Rendering、Reading Order** 等关键技术。
>
> **说明：**
>
> 目前国际学术界尚未形成统一的 **DocTags** 国际标准，因此本章节以 **Structured Document Representation** 为主线，在此基础上介绍 DocTags 思想及相关研究方向。

---

# Learning Objectives

完成本章节后，应能够理解：

* 为什么 OCR 已不能满足现代 AI 的需求
* 为什么 Document AI 正从 **OCR** 转向 **Structured Representation**
* Markdown、HTML、JSON、DocTags 的区别
* 为什么 Reading Order 是 Document AI 的核心问题
* 为什么 Structured Document 是 RAG 与 AI Agent 的基础

---

# Learning Roadmap

```text
OCR
 │
 ▼
Layout Analysis
 │
 ▼
Markdown Generation
 │
 ▼
Structured Document Representation
 │
 ▼
Semantic Rendering
 │
 ▼
DocTags
 │
 ▼
Document Agent
```

---

# Part 1. Why Structured Document Representation?

传统 OCR 输出通常如下：

```text
Title

Paragraph 1

Paragraph 2

Table

Figure

Equation
```

虽然文本被识别出来，但大量语义信息已经丢失：

* 标题层级
* 阅读顺序
* 图表引用关系
* 表格结构
* 数学公式
* 页眉页脚
* 图文对应关系
* Caption
* Footnote

因此：

**OCR ≠ Document Understanding**

现代大模型真正需要的是：

> **Semantic Document Representation（语义化文档表示）**

---

# Part 2. Evolution of Document Representation

```text
Plain Text
      │
      ▼
OCR
      │
      ▼
Layout-aware OCR
      │
      ▼
Markdown
      │
      ▼
Structured JSON
      │
      ▼
DocTags
      │
      ▼
Knowledge Graph
      │
      ▼
Document Agent
```

---

# Part 3. Representation Formats

| Format     | Structure | LLM Friendly | Editable | Semantic |
| ---------- | --------- | ------------ | -------- | -------- |
| Plain Text | ✗         | ✓            | ✓        | ✗        |
| HTML       | ✓         | ✓            | ✗        | ✓        |
| XML        | ✓         | ✓            | ✗        | ✓        |
| Markdown   | ✓         | ✓            | ✓        | ✓        |
| JSON       | ✓         | ✓            | ✗        | ✓        |
| DocTags    | ✓✓        | ✓✓           | ✓        | ✓✓       |

---

# Part 4. What is DocTags?

DocTags 并不是简单的 Markdown。

DocTags 更强调：

* Document Semantics
* Layout Semantics
* Reading Order
* Structural Relationships
* Element Types

例如：

```text
<Document>

<Title>

<Abstract>

<Section>

<Paragraph>

<Table>

<Figure>

<Equation>

<Caption>

<Reference>

<Footnote>

...
```

相比 OCR，

DocTags 保存的是：

> **Document Structure**

而不仅仅是：

> **Recognized Text**

---

# Part 5. Core Research Topics

现代 Structured Document Representation 主要关注：

## Document Layout

理解：

* Heading
* Paragraph
* Figure
* Table
* Formula

---

## Reading Order

决定：

文档真正阅读顺序。

目前：

Reading Order

已经成为：

Document Parsing

最困难的问题之一。OmniDocBench 将 Reading Order 作为核心评测维度之一。

---

## Semantic Hierarchy

例如：

```text
Book

Chapter

Section

Subsection

Paragraph
```

而不是：

OCR Text。

---

## Cross-reference

例如：

Figure 3

↓

Caption

↓

正文引用

↓

图片

保持完整关联。

---

## Table Semantics

现代 Table 不仅仅识别：

Cell

更需要理解：

* Header
* Row
* Column
* Merge
* Caption
* Footnote

---

# Part 6. Recommended Papers

---

## Paper 1

# Docling: An Efficient Open-Source Toolkit for AI-driven Document Conversion

**Priority**

⭐⭐⭐⭐⭐

**Year**

2025

### Why Read

Docling 是目前最具代表性的开源文档转换框架之一。

支持：

* PDF
* DOCX
* PPTX
* HTML

统一转换为：

* Markdown
* HTML
* Rich JSON

采用模块化架构，集成版面分析（DocLayNet）、表格识别（TableFormer）等模型，并已集成到 LangChain、LlamaIndex 等生态。

### Main Contributions

* Unified Document Representation
* Modular Architecture
* Rich Structured Output
* AI-native Document Pipeline

### Students Should Learn

* Document Object Model
* Structured JSON
* Markdown Generation
* Pipeline Design

---

## Paper 2

# OmniDocBench

**Priority**

⭐⭐⭐⭐⭐

**Conference**

CVPR 2025

### Why Read

OmniDocBench 不仅是 Benchmark。

更重要的是：

它定义了：

Document Parsing

应该输出什么。

提供：

* Reading Order
* Layout
* Table
* Formula
* Attribute

等丰富标注，是目前最全面的文档解析评测基准之一。

### Students Should Learn

* Reading Order
* Semantic Evaluation
* Multi-granularity Evaluation
* Markdown Evaluation

---

## Paper 3

# Docling Technical Report

**Priority**

⭐⭐⭐⭐⭐

### Why Read

理解：

为什么现代 Document Parsing

越来越强调：

Structured Representation

而不是：

OCR。

Docling 的核心理念就是：

**One Unified Representation**

统一管理不同来源文档。

---

## Paper 4

# Evidence Units: Ontology-Grounded Document Organization

**Priority**

⭐⭐⭐⭐⭐

**Year**

2026

### Why Read

提出 **Evidence Units (EU)**，通过本体（Ontology）将不同解析器（如 Docling、MinerU）的输出统一到语义层，并将图像、表格、公式与相关文本组织成完整证据单元，大幅提升 RAG 检索效果。

### Main Contributions

* Ontology-based Semantic Normalization
* Parser-independent Representation
* Graph-based Document Organization
* RAG-oriented Structured Chunking

### Why It Matters

代表研究重点已经从：

> PDF → Markdown

转向：

> **Semantic Document Organization**

---

# Part 7. Important Open-source Projects

---

## Docling

推荐指数：

⭐⭐⭐⭐⭐

特点：

* MIT License
* Rich JSON
* Markdown
* HTML
* LangChain
* LlamaIndex

适合作为：

Document AI

基础平台。

---

## MinerU

推荐指数：

⭐⭐⭐⭐⭐

特点：

* 高质量 PDF Parsing
* Reading Order
* Formula
* Table
* Markdown

目前是学术界与工业界广泛使用的 PDF 解析方案之一，并持续出现在 OmniDocBench 官方评测中。

---

## MarkItDown

推荐指数：

⭐⭐⭐⭐

Microsoft 开源工具。

适合：

Office

↓

Markdown

转换。

适合作为：

LLM 数据预处理。

---

## SmolDocling

推荐指数：

⭐⭐⭐⭐⭐

特点：

* Lightweight
* Fast
* Markdown Generation
* Local Deployment

非常适合：

实验室教学。

---

# Part 8. Modern Trends (2025–2026)

现代研究已经从：

```text
OCR
```

转向：

```text
Structured Representation
```

再进一步发展到：

```text
Semantic Representation
```

最终目标：

```text
Document Knowledge Representation
```

目前重点研究方向包括：

* OCR-free Parsing
* Semantic Chunking
* Reading Order
* Document Graph
* Ontology
* AI-ready Documents
* Agent-ready Documents

---

# Part 9. Why DocTags?

实验室提出 DocTags 的目标不是：

重新设计一种标签语言。

而是：

建立：

**LLM Native Document Representation**

特点：

* Better than Markdown
* Better than OCR
* Better than HTML

同时支持：

* RAG
* Agent
* Document QA
* Knowledge Graph
* Workflow Automation

---

# Part 10. Connection to Our Laboratory

实验室总体研究路线：

```text
Vision-Language Models
         │
         ▼
Document AI
         │
         ▼
Structured Representation
         │
         ▼
DocTags
         │
         ▼
OmniDocBench
         │
         ▼
Document Agent
         │
         ▼
Autonomous Scientific Assistant
```

未来重点研究方向：

* DocTags Schema Design
* Semantic Rendering
* Document Foundation Dataset
* Reading Order Learning
* Structured RAG
* Document Agent

---

# Knowledge Checklist

完成本章节后，应能够回答：

## Representation

* 为什么 Markdown 比 OCR 更适合 LLM？
* JSON 与 Markdown 的区别？
* 为什么需要 Rich Structured Document？

---

## Reading Order

* Reading Order 为什么重要？
* 为什么 Reading Order 会影响 RAG？
* OmniDocBench 如何评测 Reading Order？

---

## Semantic Representation

* 什么是 Semantic Rendering？
* 什么是 Document Object Model？
* 为什么未来需要 DocTags？

---

## Research Thinking

思考以下问题：

1. DocTags 是否可以成为一种统一的文档表示标准？
2. 如何设计适用于大模型训练的 DocTags Schema？
3. DocTags 如何支持 Agent 自动推理与工具调用？
4. 如何利用 Vision-Language Model 直接生成高质量 DocTags？

---

# Recommended Next Reading

完成本章节后，请继续阅读：

> **benchmarks.md**

重点学习：

* OmniDocBench
* DocLayNet
* DocVQA
* PubTabNet
* FUNSD
* OCRBench

理解现代 **Document AI** 如何进行科学、系统、可复现的评测，为后续模型训练与论文实验打下基础。
