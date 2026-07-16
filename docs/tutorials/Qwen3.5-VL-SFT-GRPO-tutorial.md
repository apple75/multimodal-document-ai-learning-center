# Qwen3.5-VL 后训练学习路线（SFT · GRPO）

> **Learning Center · MV-AI-Lab**

本文档整理了 Qwen3.5-VL 后训练（Post-training）相关的官方文档、开源框架及推荐学习路线，供实验室成员自学参考。

---

# 学习目标

完成本模块学习后，应能够：

* 理解 Vision-Language Model（VLM）微调流程；
* 掌握 LoRA / QLoRA 微调方法；
* 使用 SFT 完成领域模型微调；
* 理解 GRPO 强化学习微调流程；
* 能够完成 Qwen3.5-VL 的基础训练与评测。

---

# 推荐学习路线

```text
Qwen3.5-VL
        │
        ▼
LoRA / QLoRA
        │
        ▼
SFT
        │
        ▼
Evaluation
        │
        ▼
GRPO
```

建议先完成 SFT，再学习 GRPO。

---

# 一、Qwen 官方资源

| 资源                                                                             | 说明                 |
| ------------------------------------------------------------------------------ | ------------------ |
| [Qwen 官方 GitHub](https://github.com/QwenLM?utm_source=chatgpt.com)             | Qwen 系列模型官方代码仓库    |
| [Qwen Hugging Face Models](https://huggingface.co/Qwen?utm_source=chatgpt.com) | 官方模型下载与 Model Card |
| [Qwen 官方文档](https://qwen.readthedocs.io/?utm_source=chatgpt.com)               | 官方使用文档（持续更新）       |

---

# 二、SFT 微调（推荐优先学习）

## 推荐框架：LLaMA-Factory

推荐理由：

* 配置简单
* 支持 LoRA / QLoRA
* 支持 Qwen 系列模型
* 社区活跃
* 适合科研实验

学习资料：

* [LLaMA-Factory 官方 GitHub](https://github.com/hiyouga/LLaMA-Factory?utm_source=chatgpt.com)
* [LLaMA-Factory 中文 SFT 文档](https://llamafactory.readthedocs.io/zh-cn/latest/getting_started/sft.html?utm_source=chatgpt.com)
* [LLaMA-Factory 英文文档](https://llamafactory.readthedocs.io/en/latest/getting_started/sft.html?utm_source=chatgpt.com)

建议重点学习：

* LoRA
* QLoRA
* Dataset 配置
* YAML 配置文件
* 模型导出

---

# 三、GRPO 强化学习微调

GRPO（Group Relative Policy Optimization）是当前主流的大模型强化学习算法之一，适用于推理能力优化及后训练。

推荐框架：

## Hugging Face TRL

官方文档：

* [TRL GRPO Trainer](https://huggingface.co/docs/trl/grpo_trainer?utm_source=chatgpt.com)

重点学习：

* GRPOTrainer
* Reward Function
* VLM GRPO
* LoRA + GRPO

---

## OpenRLHF

推荐用于科研实验和大规模训练。

官方文档：

* [OpenRLHF 官方文档](https://openrlhf.readthedocs.io/en/latest/?utm_source=chatgpt.com)
* [OpenRLHF SFT / DPO 文档](https://openrlhf.readthedocs.io/en/latest/non_rl.html?utm_source=chatgpt.com)
* [OpenRLHF RL Training Guide](https://openrlhf.readthedocs.io/en/latest/agent_training.html?utm_source=chatgpt.com)

建议重点学习：

* Ray + vLLM
* GRPO
* PPO
* 多 GPU 训练

---

# 四、建议掌握的知识点

## SFT

* Instruction Dataset
* LoRA
* QLoRA
* Tokenizer
* Processor
* YAML 配置
* Checkpoint

---

## GRPO

* Reward Function
* Sampling
* Rollout
* Policy Optimization
* Reference Model
* Reward Model
* vLLM

---

# 五、实验室推荐学习顺序

| 阶段   | 学习内容                   |
| ---- | ---------------------- |
| 第一阶段 | Qwen3.5-VL 基础使用        |
| 第二阶段 | LoRA / QLoRA 微调        |
| 第三阶段 | SFT 实践                 |
| 第四阶段 | Benchmark 与 Evaluation |
| 第五阶段 | GRPO 后训练               |
| 第六阶段 | 阅读最新论文并开展科研实验          |

---

# 六、推荐实践项目

建议完成以下实验：

* 使用 OmniDocBench 对 Qwen3.5-VL-0.8B 进行 SFT；
* 使用 Qwen3.5-VL-2B 完成 SFT 基线实验；
* 构建 Document AI Benchmark；
* 基于 Reward Function 开展 GRPO 微调；
* 对比 SFT 与 GRPO 的性能差异。

---

# 七、参考框架

| 框架               | 推荐用途            |
| ---------------- | --------------- |
| Qwen             | 基础模型            |
| LLaMA-Factory    | SFT 微调          |
| Hugging Face TRL | GRPO 与 RL       |
| OpenRLHF         | 大规模 RLHF / GRPO |

---

> **Learning First · Practice Second · Research Finally**
