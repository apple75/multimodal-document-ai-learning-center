# Qwen3.5-VL 后训练学习资源
> Learning Center · MV-AI-Lab

本资料整理了实验室目前采用的 **Qwen3.5-VL 后训练（Post-training）** 学习资源，包括 **MS-SWIFT、LoRA、SFT、GRPO** 以及 **Weights & Biases (W&B)** 等核心工具。

---

# 推荐学习路线

```text
Qwen3.5-VL
      │
      ▼
MS-SWIFT
      │
      ▼
LoRA / QLoRA
      │
      ▼
SFT
      │
      ▼
Weights & Biases
      │
      ▼
GRPO
      │
      ▼
Evaluation
```

建议严格按照上述顺序学习。

---

# 一、MS-SWIFT（★★★★★）

## 为什么学习 MS-SWIFT？

> **这是目前实验室统一采用的大模型微调框架，也是当前 Qwen 系列模型微调的主要框架。**

MS-SWIFT（ModelScope SWIFT）是 ModelScope 社区推出的大模型训练与部署框架，也是 **Qwen 官方推荐** 的训练框架。

支持：

- Qwen / Qwen2 / Qwen3 / Qwen3.5
- Vision-Language Model（VLM）
- LoRA / QLoRA / DoRA
- SFT
- GRPO
- DPO
- PPO
- RLHF
- DeepSpeed
- Megatron-SWIFT
- 多 GPU 分布式训练

---

## 官方学习资源

| 教程 | 推荐 | 官方链接 |
|------|:----:|----------|
| MS-SWIFT 官方文档（中文） | ⭐⭐⭐⭐⭐ | https://swift.readthedocs.io/zh-cn/latest/ |
| Qwen 官方 MS-SWIFT 教程 | ⭐⭐⭐⭐⭐ | https://qwen.readthedocs.io/zh-cn/stable/training/ms_swift.html |
| MS-SWIFT GitHub | ⭐⭐⭐⭐⭐ | https://github.com/modelscope/ms-swift |

---

## 实验室重点推荐（一）

### ⭐ Qwen3.5 Best Practice（必须阅读）

这是目前 **Qwen3.5 官方最佳实践**。

主要内容包括：

- 环境配置
- 推理
- SFT
- RL（GRPO）
- 数据格式
- 多模态训练
- Qwen3.5 推荐配置

官方文档：

https://swift.readthedocs.io/zh-cn/latest/BestPractices/Qwen3_5-Best-Practice.html

> ⭐⭐⭐⭐⭐ **建议所有成员首先阅读。**

---

## 实验室重点推荐（二）

### ⭐ LoRA Training（必须掌握）

目前实验室大多数科研训练均采用 **LoRA 微调**。

原因：

- GPU 显存需求低
- 收敛速度快
- 实验效率高
- 非常适合科研快速迭代

虽然 LoRA 在模型能力上存在一定瓶颈，但它仍然是目前**最高效、最实用的微调方法**，也是实验室当前的主力训练方式。

官方文档：

https://swift.readthedocs.io/zh-cn/latest/Megatron-SWIFT/LoRA-Training.html

建议重点学习：

- LoRA 原理
- LoRA 配置
- LoRA Rank
- LoRA Alpha
- LoRA Merge
- LoRA Export

---

## 建议重点掌握

- Environment
- Dataset Format
- Processor
- YAML Config
- LoRA
- SFT
- GRPO
- Model Export

---

# 二、Weights & Biases（W&B）

## 为什么学习 W&B？

Weights & Biases（简称 **W&B**）是目前国际上最流行的 AI 实验管理平台之一。

实验室建议：

> **所有模型训练默认开启 W&B。**

它最大的价值不是"加快训练速度"，而是：

> **帮助你更快发现问题、更科学调参、更容易复现实验。**

---

## W&B 可以做什么？

自动记录：

- Training Loss
- Validation Loss
- Learning Rate
- GPU Memory
- GPU Utilization
- Batch Size
- Epoch
- Step
- Checkpoint

自动生成：

- Loss 曲线
- 学习率曲线
- GPU 利用率
- 实验 Dashboard

无需人工记录。

---

## 重点关注

模型训练过程中，请重点观察：

- Loss
- Learning Rate
- Batch Size

分析三者之间的联动关系。

例如：

- Loss 是否震荡？
- Learning Rate 是否过大？
- Batch Size 是否影响收敛？
- 是否出现过拟合？

这些信息对于后续调参具有重要价值。

---

## 推荐学习资源

| 教程 | 推荐 | 官方链接 |
|------|:----:|----------|
| W&B 官网 | ⭐⭐⭐⭐⭐ | https://wandb.ai/site |
| W&B 官方文档 | ⭐⭐⭐⭐⭐ | https://docs.wandb.ai/ |
| Quick Start | ⭐⭐⭐⭐⭐ | https://docs.wandb.ai/get-started |
| Hyperparameter Sweeps | ⭐⭐⭐⭐☆ | https://docs.wandb.ai/models/sweeps/walkthrough |

---

## 推荐中文资源

| 平台 | 链接 |
|------|------|
| CSDN | https://blog.csdn.net/search?keyword=Weights%20%26%20Biases |
| 知乎 | https://www.zhihu.com/search?type=content&q=Weights%20%26%20Biases |
| Bilibili | https://search.bilibili.com/all?keyword=Weights%20%26%20Biases |

建议：

> **先阅读官方文档，再结合中文教程实践。**

---

# 三、推荐学习顺序

| 阶段 | 学习内容 |
|------|----------|
| 第一阶段 | MS-SWIFT 快速开始 |
| 第二阶段 | Qwen3.5 Best Practice（★★★★★） |
| 第三阶段 | LoRA 微调（★★★★★） |
| 第四阶段 | SFT 微调 |
| 第五阶段 | Weights & Biases |
| 第六阶段 | GRPO 后训练 |
| 第七阶段 | Benchmark 与 Evaluation |

---

# 四、实验室统一技术路线

```text
Qwen3.5-VL
      │
      ▼
MS-SWIFT
      │
      ▼
LoRA
      │
      ▼
SFT
      │
      ▼
Weights & Biases
      │
      ▼
GRPO
      │
      ▼
Evaluation
      │
      ▼
Paper
```

---

# 五、实验室建议

目前实验室统一采用：

| 模块 | 推荐方案 |
|------|----------|
| 基础模型 | Qwen3.5-VL-0.8B / 2B |
| 训练框架 | MS-SWIFT |
| 微调方法 | LoRA + SFT |
| 后训练 | GRPO |
| 实验管理 | Weights & Biases |
| 版本管理 | GitHub |
| 模型存储 | Hugging Face / ModelScope |
| 数据管理 | GitHub Metadata + 外部存储 |

---

# 12. 下一章（Next Chapter）

下一章学习：

> ** First Research Project **

主要内容包括：

* 第一个完整项目
* 数据准备
* 模型运行
* 实验记录
* Benchmark 测试
* 结果分析
* GitHub 项目管理

完成后，你将独立完成第一个 Multimodal Document AI 科研实践项目，并掌握实验室标准的项目开发流程。

[上一章](07_Doc_AI.md){ .md-button }    [下一章](../experiments/Experiment_01/README.md){ .md-button }


