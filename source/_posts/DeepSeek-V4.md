---
title: DeepSeek V4
date: 2026-04-25 17:17:00
categories:
  - 基模
tags:
---

昨天 (2026.4.24) DeepSeek 发布了 V4 版本，包括专业版 Pro 和轻量版 Flash、都支持 1M 上下文和深度思考，在 Agent 能力、知识和推理方面有显著提升。

## 基本信息

| 模型  | 上下文长度 | 深度思考 | 参数 | 激活参数 | 预训练数据 |
| ----- | ---------- | -------- | ---- | -------- | ---------- |
| pro   | 1M         | 支持     | 1.6T | 49B      | 33T        |
| flash | 1M         | 支持     | 284B | 13B      | 32T        |

## 模型评测

- 评测领域：Agent 能力、知识、推理
- pro 模型：
  - 三个领域都领先或持平开源模型、持平或落后闭源模型
- flash 模型：
  - Agent 能力：简单任务持平 pro、复杂任务有差距
  - 知识：稍落后 pro
  - 推理：接近 pro

![](/images/bench.webp)

## DSA 稀疏注意力

V4 开创了一种新的注意力机制：DSA 稀疏注意力 (DeepSeek Sparse Attention)，用于实现 1M 长上下文、相比传统方法降低了对计算和显存的要求。

![](/images/dsa.webp)

## 使用方式

- Web/App：免费使用，快速模式对应 flash、专家模式对应 pro，都支持设置深度思考
- API 接口：
  - 支持 Anthropic 和 OpenAI 格式
  - 模型名：`deepseek-v4-flash`，`deepseek-v4-pro`
  - `reasoning_effort` 参数设置思考强度 high/max

## 更多资料

- 公众号：https://mp.weixin.qq.com/s/8bxXqS2R8Fx5-1TLDBiEDg
- 技术报告：https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro/blob/main/DeepSeek_V4.pdf
