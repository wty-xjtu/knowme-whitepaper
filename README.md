# Knowme: 以人为中心的 Personal Agent 综述

> **理解人 · 恰当回应人 · 主动关心人**
>
> 📋 完整大纲见 [knowme白皮书版本2.md](./knowme白皮书版本2.md) · 综述撰写中，论文列表持续更新

一篇关于 **Personal Agent（个人智能体）** 的综述论文之配套仓库。我们以"**理解人 → 恰当回应人 → 主动关心人**"为主线，将长期记忆、用户建模、个性化回应与主动介入等研究整合进同一能力框架。

**核心系统闭环：** 个人证据 → 用户模型 → 互动决策 → 用户反馈 → 持续更新

---

## 📑 目录

- [第一章 引言](#第一章-引言)
- [第二章 定义与能力框架](#第二章-定义与能力框架)
- [第三章 理解人](#第三章-理解人)
  - [3.1 记忆表示与存储](#31-记忆表示与存储结构)
  - [3.2 记忆写入与更新](#32-记忆写入与更新机制)
  - [3.3 记忆检索策略](#33-记忆检索策略)
  - [3.4 用户模型与人物推断](#34-用户模型与人物推断)
- [第四章 恰当回应人](#第四章-恰当回应人)
  - [4.1 信息选择与上下文构建](#41-个性化信息选择与上下文构建)
  - [4.2 回应动作与交互策略](#42-回应动作与交互策略选择)
  - [4.3 回应生成与个性化表达](#43-回应生成与个性化表达)
  - [4.4 评估、边界控制与反馈校准](#44-回应评估边界控制与反馈校准)
- [第五章 主动关心人](#第五章-主动关心人)
  - [5.1 情境监测与需求检测](#51-持续情境监测与潜在需求检测)
  - [5.2 帮助目标与内容规划](#52-主动帮助目标与内容规划)
  - [5.3 介入时机与沉默决策](#53-介入时机与沉默决策)
  - [5.4 反馈与主动策略更新](#54-用户反馈与主动策略更新)
- [第六章 应用场景](#第六章-应用场景)
- [第七章 未来方向](#第七章-综合讨论与未来方向)

---

## 第一章 引言

Personal Agent 正从单次任务工具，走向长期服务具体用户的智能体。现有研究中长期记忆、用户画像、个性化生成与主动交互仍分散在不同研究线索中，本综述用统一能力框架重新组织。

**相关综述：**

- [2024/04] A Survey on the Memory Mechanism of Large Language Model based Agents. [paper](https://arxiv.org/abs/2404.13501)
- [2025/12] Memory in the Age of AI Agents. [paper](https://arxiv.org/abs/2512.13564)
- [2024/11] Personalization of Large Language Models: A Survey. [paper](https://arxiv.org/abs/2411.00027)
- [2023/05] A Survey on Proactive Dialogue Systems: Problems, Methods, and Prospects. [paper](https://arxiv.org/abs/2305.02750)
- Proactive Conversational AI: A Comprehensive Survey. [paper](https://doi.org/10.1145/3715097)

## 第二章 定义与能力框架

界定 Personal Agent 与一般 Agent 的根本区别（任务完成 · 长期连续性 · 用户特定性），从用户授权、跨时间个人证据、动态用户模型、个性化行动、适度主动和用户控制六个方面给出操作性定义。

- [2023/04] Generative Agents: Interactive Simulacra of Human Behavior. [paper](https://arxiv.org/abs/2304.03442)
- [2023/09] Cognitive Architectures for Language Agents. [paper](https://arxiv.org/abs/2309.02427)

## 第三章 理解人

### 3.1 记忆表示与存储结构

比较树、事件图、主题图、时间层级和多模态记忆图，重点看抽象结论能否回溯到原始个人经历。

- [2024/10] From Isolated Conversations to Hierarchical Schemas: Dynamic Tree Memory Representation for LLMs. [paper](https://arxiv.org/abs/2410.14052)
- [2026/04] GAM: Hierarchical Graph-based Agentic Memory for LLM Agents. [paper](https://arxiv.org/abs/2604.12285)
- [2025/08] Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory. [paper](https://arxiv.org/abs/2508.09736)
- [2026/02] M2A: Multimodal Memory Agent with Dual-Layer Hybrid Memory for Long-Term Personalized Interactions. [paper](https://arxiv.org/abs/2602.07624)
- [2023/10] MemGPT: Towards LLMs as Operating Systems. [paper](https://arxiv.org/abs/2310.08560)
- [2023/05] Memorybank: Enhancing Large Language Models with Long-Term Memory. [paper](https://arxiv.org/abs/2305.10250)
- [2025/04] Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory. [paper](https://arxiv.org/abs/2504.19413)
- [2025/01] Zep: A Temporal Knowledge Graph Architecture for Agent Memory. [paper](https://arxiv.org/abs/2501.13956)
- [2025/02] A-MEM: Agentic Memory for LLM Agents. [paper](https://arxiv.org/abs/2502.12110)
- [2025/06] Memory OS of AI Agent. [paper](https://arxiv.org/abs/2506.06326)
- [2025/07] MemOS: A Memory OS for AI System. [paper](https://arxiv.org/abs/2507.03724)
- [2024/07] Memory³: Language Modeling with Explicit Memory. [paper](https://arxiv.org/abs/2407.01178)
- [2024/02] MEMORYLLM: Towards Self-Updatable Large Language Models. [paper](https://arxiv.org/abs/2402.04624)
- [2025/02] M+: Extending MemoryLLM with Scalable Long-Term Memory. [paper](https://arxiv.org/abs/2502.00592)
- [2024/04] From Local to Global: A Graph RAG Approach to Query-Focused Summarization. [paper](https://arxiv.org/abs/2404.16130)
- [2023/05] Voyager: An Open-Ended Embodied Agent with Large Language Models. [paper](https://arxiv.org/abs/2305.16291)
- [2024/06] Enhancing Long-Term Memory using Hierarchical Aggregate Tree for Retrieval Augmented Generation. [paper](https://arxiv.org/abs/2406.06124)
- [2025/06] G-Memory: Tracing Hierarchical Memory for Multi-Agent Systems. [paper](https://arxiv.org/abs/2506.07398)
- [2025/08] Memory Decoder: A Pretrained, Plug-and-Play Memory for Large Language Models. [paper](https://arxiv.org/abs/2508.09874)
- [2025/11] O-Mem: Omni Memory System for Personalized, Long Horizon, Self-Evolving Agents. [paper](https://arxiv.org/abs/2511.13593)
- [2025/12] MMAG: Mixed Memory-Augmented Generation for Large Language Models Applications. [paper](https://arxiv.org/abs/2512.01710)
- [2025/12] MemVerse: Multimodal Memory for Lifelong Learning Agents. [paper](https://arxiv.org/abs/2512.03627)
- [2025/12] Memoria: A Scalable Agentic Memory Framework for Personalized Conversational AI. [paper](https://arxiv.org/abs/2512.12686)
- [2025/12] Hindsight is 20/20: Building Agent Memory that Retains, Recalls, and Reflects. [paper](https://arxiv.org/abs/2512.12818)

### 3.2 记忆写入与更新机制

新证据写入、重复信息合并、冲突保留以及旧结论的修改、删除与隐式失效判断。

- [2026/01] Inside Out: Evolving User-Centric Core Memory Trees for Long-Term Personalized Dialogue Systems. [paper](https://arxiv.org/abs/2601.05171)
- [2025/03] MemInsight: Autonomous Memory Augmentation for LLM Agents. [paper](https://arxiv.org/abs/2503.21760)
- [2026/05] STALE: Can LLM Agents Know When Their Memories Are No Longer Valid? [paper](https://arxiv.org/abs/2605.06527)
- [2023/03] Reflexion: Language Agents with Verbal Reinforcement Learning. [paper](https://arxiv.org/abs/2303.11366)
- [2024/06] Towards Lifelong Dialogue Agents via Timeline-based Memory Management. [paper](https://arxiv.org/abs/2406.10996)
- [2025/02] R³Mem: Bridging Memory Retention and Retrieval via Reversible Compression. [paper](https://arxiv.org/abs/2502.15957)
- [2025/08] Memory-R1: Enhancing Large Language Model Agents to Manage and Utilize Memories via Reinforcement Learning. [paper](https://arxiv.org/abs/2508.19828)
- [2025/08] Building Self-Evolving Agents via Experience-Driven Lifelong Learning: A Framework and Benchmark. [paper](https://arxiv.org/abs/2508.19005)

### 3.3 记忆检索策略

比较层级、向量、图回溯、实体约束和多路检索，讨论相关性、时效性、可信度与检索成本的平衡。

- [2024/10] From Isolated Conversations to Hierarchical Schemas: Dynamic Tree Memory Representation for LLMs. [paper](https://arxiv.org/abs/2410.14052)
- [2026/04] GAM: Hierarchical Graph-based Agentic Memory for LLM Agents. [paper](https://arxiv.org/abs/2604.12285)
- [2025/08] Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory. [paper](https://arxiv.org/abs/2508.09736)
- [2024/01] RAPTOR: Recursive Abstractive Processing for Tree-Organized Retrieval. [paper](https://arxiv.org/abs/2401.18059)
- [2024/05] HippoRAG: Neurobiologically Inspired Long-Term Memory for Large Language Models. [paper](https://arxiv.org/abs/2405.14831)
- [2024/09] MemoRAG: Boosting Long Context Processing with Global Memory-Enhanced Retrieval Augmentation. [paper](https://arxiv.org/abs/2409.05591)
- [2025/05] MemGuide: Intent-Driven Memory Selection for Goal-Oriented Multi-Session LLM Agents. [paper](https://arxiv.org/abs/2505.20231)

### 3.4 用户模型与人物推断

个人证据怎样转化为状态、画像、动机与未来选择；重点看深层结论能否由历史证据支持并允许用户修正。

- [2026/01] TiMem: Temporal-Hierarchical Memory Consolidation for Long-Horizon Conversational Agents. [paper](https://arxiv.org/abs/2601.02845)
- [2026/04] PersonaVLM: Long-Term Personalized Multimodal LLMs. [paper](https://arxiv.org/abs/2604.13074)
- [2026/04] EgoSelf: From Memory to Personalized Egocentric Assistant. [paper](https://arxiv.org/abs/2604.19564)
- [2026/01] HumanLLM: Towards Personalized Understanding and Simulation of Human Nature. [paper](https://arxiv.org/abs/2601.15793)
- [2025/10] Enabling Personalized Long-term Interactions in LLM-based Agents through Persistent Memory and User Profiles. [paper](https://arxiv.org/abs/2510.07925)
- [2025/10] RGMem: Renormalization Group-inspired Memory Evolution for Language Agents. [paper](https://arxiv.org/abs/2510.16392)
- [2025/12] Sophia: A Persistent Agent Framework of Artificial Life. [paper](https://arxiv.org/abs/2512.18202)

**记忆评测基准：**

- [2024/02] LoCoMo: Evaluating Long-Term Conversational Memory in Multi-Session Dialogue. [paper](https://arxiv.org/abs/2402.17753)
- [2024/10] LongMemEval: Benchmarking Chat Assistants on Long-Term Interactive Memory. [paper](https://arxiv.org/abs/2410.10813)
- [2026/01] KnowMe-Bench: Benchmarking Person Understanding for Lifelong Digital Companions. [paper](https://arxiv.org/abs/2601.04745)
- [2026/05] STALE: Can LLM Agents Know When Their Memories Are No Longer Valid? [paper](https://arxiv.org/abs/2605.06527)

## 第四章 恰当回应人

### 4.1 个性化信息选择与上下文构建

当前回应应该调用哪些用户历史；讨论信息不足与信息过度使用两类问题。

- [2023/04] LaMP: When Large Language Models Meet Personalization. [paper](https://arxiv.org/abs/2304.11406)
- [2025/07] PRIME: Large Language Model Personalization with Cognitive Dual-Memory and Personalized Thought Process. [paper](https://arxiv.org/abs/2507.04607)
- [2025/03] Measuring What Makes You Unique: Difference-Aware User Modeling for Enhancing LLM Personalization. [paper](https://arxiv.org/abs/2503.02450)

### 4.2 回应动作与交互策略选择

把回应视为动作选择问题：直接回答、澄清、询问、建议还是提供支持。

- [2026/06] From Empathy to Personalized Empathy: Adapting Empathetic Strategies to Individual Users. [paper](https://arxiv.org/abs/2606.00728)
- [2024/06] Learning to Clarify: Multi-turn Conversations with Action-Based Contrastive Self-Training. [paper](https://arxiv.org/abs/2406.00222)
- [2022/12] CLAM: Selective Clarification for Ambiguous Questions with Generative Language Models. [paper](https://arxiv.org/abs/2212.07769)

### 4.3 回应生成与个性化表达

用户经历、长期信念、语言习惯和情绪背景如何影响信息内容、措辞、语气与支持方式。

- [2024/06] Personalized Pieces: Efficient Personalized Large Language Models through Collaborative Efforts. [paper](https://arxiv.org/abs/2406.10471)
- [2024/06] Personalized Steering of Large Language Models: Versatile Steering Vectors Through Bi-directional Preference Optimization. [paper](https://arxiv.org/abs/2406.00045)
- [2025/05] Steerable Chatbots: Exploring Personalization Control Interfaces via LLM Activation Steering. [paper](https://arxiv.org/abs/2505.04260)

### 4.4 回应评估、边界控制与反馈校准

什么时候应该克制、停止追问或承认信息不足；把用户纠正用于后续策略更新。

- [2026/01] OP-Bench: Benchmarking Over-Personalization for Memory-Augmented Personalized Conversational Agents. [paper](https://arxiv.org/abs/2601.13722)
- [2025/05] Personalized Safety in LLMs: A Benchmark and A Planning-Based Agent Approach. [paper](https://arxiv.org/abs/2505.18882)
- [2026/02] Learning Personalized Agents from Human Feedback. [paper](https://arxiv.org/abs/2602.16173)
- [2025/09] SPECTRA: Revealing the Full Spectrum of User Preferences via Distributional LLM Inference. [paper](https://arxiv.org/abs/2509.24189)
- [2025/02] Unveiling Privacy Risks in LLM Agent Memory. [paper](https://arxiv.org/abs/2502.13172)

## 第五章 主动关心人

### 5.1 持续情境监测与潜在需求检测

区分"观察到事件"和"用户可能需要帮助"；讨论需求推断的证据基础和误判风险。

- [2026/04] PASK: Toward Intent-Aware Proactive Agents with Long-Term Memory. [paper](https://arxiv.org/abs/2604.08000)
- [2026/07] Vinci2: Providing Proactive Assistance in Continuous Egocentric Videos. [paper](https://arxiv.org/abs/2607.11523)
- [2024/10] Proactive Agent: Shifting LLM Agents from Reactive Responses to Active Assistance. [paper](https://arxiv.org/abs/2410.12361)

### 5.2 主动帮助目标与内容规划

比较主动话题、推荐、提醒、任务指导、安全警告和错误恢复等帮助目标。

- [2025/03] Interpersonal Memory Matters: A New Task for Proactive Dialogue Utilizing Conversational History. [paper](https://arxiv.org/abs/2503.05150)
- [2025/09] ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation. [paper](https://arxiv.org/abs/2509.21730)
- [2025/09] PRINCIPLES: Synthetic Strategy Memory for Proactive Dialogue Agents. [paper](https://arxiv.org/abs/2509.17459)

### 5.3 介入时机与沉默决策

结合时间偏好、活动阶段、任务进展和历史反馈，在立即介入、延迟介入与保持沉默之间选择。

- [2026/08] Preference-Driven Online Adaptation for Personalized Interaction Initiation in Proactive AI Assistants. [paper](https://arxiv.org/abs/2608.04416)
- [2025/09] ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation. [paper](https://arxiv.org/abs/2509.21730)
- [2026/07] Vinci2: Providing Proactive Assistance in Continuous Egocentric Videos. [paper](https://arxiv.org/abs/2607.11523)

### 5.4 用户反馈与主动策略更新

利用真实反馈调整主动内容、频率与时机；讨论模拟反馈与长期真实反馈的差距。

- [2025/09] ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation. [paper](https://arxiv.org/abs/2509.21730)
- [2026/08] Preference-Driven Online Adaptation for Personalized Interaction Initiation in Proactive AI Assistants. [paper](https://arxiv.org/abs/2608.04416)

## 第六章 应用场景

三类能力在不同环境下的组合方式与安全边界（论文待补充）：

- **教育与学习支持：** 过度帮助 · 错误标签 · 学生自主性 · 未成年人隐私
- **车载与驾驶辅助：** 实时性 · 误报 · 驾驶干扰 · 安全责任
- **可穿戴设备与个人健康：** 持续监测隐私 · 敏感授权 · 健康焦虑 · 功耗

## 第七章 综合讨论与未来方向

1. **从分散组件走向闭环 Personal Agent：** 建立"个人证据—用户模型—互动决策—用户反馈—模型更新"长期闭环
2. **多模态、动态且可追溯的用户模型：** 动态更新 · 证据追溯 · 不确定性表达
3. **回应内容与主动时机的联合决策：** 说什么与什么时候说联合建模
4. **真实反馈与长期在线适应：** 避免偶然反馈固化为稳定偏好
5. **用户授权、控制与安全边界：** 查看 · 修正 · 授权 · 降级 · 撤销
6. **面向完整能力链的评测：** 更准 · 更合适 · 更可控 · 更持续有效

---

## 🤝 贡献

欢迎提交 Issue 或 PR 补充遗漏论文、修正链接或调整分类。

## 📝 引用

综述论文撰写中，敬请期待。