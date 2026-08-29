# 🧠 Knowme: 以人为中心的 Personal Agent 论文精选

<div align="center">

![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)
[![commit](https://img.shields.io/github/last-commit/wty-xjtu/knowme-whitepaper?color=blue)](https://github.com/wty-xjtu/knowme-whitepaper/commits/master)
[![PR](https://img.shields.io/badge/PRs-Welcome-red)](https://github.com/wty-xjtu/knowme-whitepaper/pulls)

</div>

## 🌟 Overview

本仓库是一篇 **Personal Agent（个人智能体）综述** 的配套论文清单，围绕「**理解人 → 恰当回应人 → 主动关心人**」这一能力主线，把长期记忆、用户建模、个性化回应与主动介入等原本分散在不同研究线索里的工作组织进同一框架。

我们从「个人证据 → 用户模型 → 互动决策 → 用户反馈 → 持续更新」的闭环出发，按组件（存储 · 更新 · 检索 · 推断 · 决策 · 生成 · 反馈）对论文分类，重点收录 2024–2026 年 Agent Memory 与个性化智能体方向的高影响力工作——优先选择顶会顶刊录用（ACL / NAACL / EMNLP / NeurIPS / ICLR / ICML / AAAI / UIST / WWW 等）或高引用开源框架（MemGPT、Mem0、Zep、A-MEM 等）论文。

📄 **[查看综述完整大纲](./knowme白皮书版本2.md)** · 综述撰写中，论文列表持续更新

## 📑 目录

- [🌟 Overview](#-overview)
- [🔍 Key Categories](#-key-categories)
- [📚 Resource List](#-resource-list)
  - [第一章 引言：相关综述](#第一章-引言相关综述)
  - [第二章 定义与能力框架](#第二章-定义与能力框架)
  - [第三章 理解人](#第三章-理解人)
  - [第四章 恰当回应人](#第四章-恰当回应人)
  - [第五章 主动关心人](#第五章-主动关心人)
- [🤝 Contributing](#-contributing)
- [📝 Citing](#-citing)

## 🔍 Key Categories

- **🧩 理解人（第三章）**：记忆表示与存储 → 记忆写入与更新 → 记忆检索策略 → 用户模型与人物推断
- **💬 恰当回应人（第四章）**：个性化信息选择 → 回应动作策略 → 回应生成表达 → 评估、边界与反馈校准
- **🔔 主动关心人（第五章）**：持续情境监测 → 帮助目标规划 → 介入时机与沉默决策 → 反馈与主动策略更新

## 📚 Resource List

### 第一章 引言：相关综述

- **[A Survey on the Memory Mechanism of Large Language Model based Agents](https://arxiv.org/abs/2404.13501)** (*2024*) `Arxiv`
  > 系统梳理 LLM 智能体记忆机制的代表性综述，覆盖记忆来源、形式、操作与使用。
- **[Memory in the Age of AI Agents](https://arxiv.org/abs/2512.13564)** (*2025*) `Arxiv`
  > 面向 AI Agent 时代记忆研究的最新综述，按记忆生命周期组织方法、评测与开放问题。
- **[Personalization of Large Language Models: A Survey](https://arxiv.org/abs/2411.00027)** (*2024*) `Arxiv`
  > LLM 个性化方向的综述，界定个性化任务、数据与方法谱系。
- **[Toward Personalized LLM-Powered Agents: Foundations, Evaluation, and Future Directions](https://arxiv.org/abs/2602.22680)** (*2026*) `CSUR`
  > 以能力为视角综述个性化 LLM 智能体，围绕画像建模、记忆、规划与动作执行组织文献。
- **[A Survey on Proactive Dialogue Systems: Problems, Methods, and Prospects](https://arxiv.org/abs/2305.02750)** (*2023*) `Arxiv`
  > 主动对话系统的早期综述，梳理目标规划、时机判断与策略生成等核心问题。
- **[Proactive Conversational AI: A Comprehensive Survey](https://doi.org/10.1145/3715097)** (*2025*) `CSUR`
  > 主动式对话 AI 的综合综述，覆盖何时介入、提供什么与如何表达。

### 第二章 定义与能力框架

- **[Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442)** (*2023*) `UIST`
  > 以「记忆流—反思—规划」确立智能体长期行为范式，是本领域基石。
- **[Cognitive Architectures for Language Agents](https://arxiv.org/abs/2309.02427)** (*2024*) `TMLR`
  > 提出 CoALA，划分工作/情景/语义/程序性记忆，成为后续 Agent 记忆工作的默认认知架构。

### 第三章 理解人

#### 3.1 记忆表示与存储结构

- **[From Isolated Conversations to Hierarchical Schemas: Dynamic Tree Memory Representation for LLMs](https://arxiv.org/abs/2410.14052)** (*2024*) `Arxiv`
  > 提出 MemTree，用动态树状记忆结构组织多会话对话，支持层级化信息回溯。
- **[GAM: Hierarchical Graph-based Agentic Memory for LLM Agents](https://arxiv.org/abs/2604.12285)** (*2026*) `Arxiv`
  > 基于层级图的 Agent 记忆表示，组织跨任务经验与关系。
- **[Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory](https://arxiv.org/abs/2508.09736)** (*2025*) `Arxiv`
  > 多模态智能体长期记忆，融合视觉与听觉信息支持推理。
- **[M2A: Multimodal Memory Agent with Dual-Layer Hybrid Memory for Long-Term Personalized Interactions](https://arxiv.org/abs/2602.07624)** (*2026*) `Arxiv`
  > 双层混合记忆的多模态记忆智能体，面向长期个性化交互。
- **[MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560)** (*2023*) `Arxiv`
  > 以操作系统的虚拟内存理念管理 LLM 上下文，实现分层存储与跨会话记忆。
- **[Memorybank: Enhancing Large Language Models with Long-Term Memory](https://arxiv.org/abs/2305.10250)** (*2023*) `AAAI`
  > 借鉴遗忘曲线的记忆更新机制，让 LLM 随交互理解并适应用户性格。
- **[Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory](https://arxiv.org/abs/2504.19413)** (*2025*) `Arxiv`
  > 面向生产环境的可扩展长期记忆层，高 Star 开源框架代表。
- **[Zep: A Temporal Knowledge Graph Architecture for Agent Memory](https://arxiv.org/abs/2501.13956)** (*2025*) `Arxiv`
  > 用时序知识图谱组织 Agent 记忆，支持时间感知的事实与关系检索。
- **[A-MEM: Agentic Memory for LLM Agents](https://arxiv.org/abs/2502.12110)** (*2025*) `Arxiv`
  > 借鉴 Zettelkasten 笔记思想的自组织智能体记忆，支持动态更新与自适应管理。
- **[Memory OS of AI Agent](https://arxiv.org/abs/2506.06326)** (*2025*) `Arxiv`
  > 提出 Agent 记忆操作系统，统一记忆的存储、调度与生命周期。
- **[MemOS: A Memory OS for AI System](https://arxiv.org/abs/2507.03724)** (*2025*) `Arxiv`
  > 面向 AI 系统的记忆操作系统，提供可感知、可组合、可追溯的记忆服务。
- **[Memory³: Language Modeling with Explicit Memory](https://arxiv.org/abs/2407.01178)** (*2024*) `Arxiv`
  > 用显式「稀疏键值」记忆外部化具体知识，降低训练与推理成本。
- **[MEMORYLLM: Towards Self-Updatable Large Language Models](https://arxiv.org/abs/2402.04624)** (*2024*) `NeurIPS`
  > 让 LLM 通过自更新方式把新知识写入自身参数，形成长期记忆。
- **[M+: Extending MemoryLLM with Scalable Long-Term Memory](https://arxiv.org/abs/2502.00592)** (*2025*) `Arxiv`
  > 在 MemoryLLM 基础上引入可扩展外部记忆，缓解模型参数更新的容量瓶颈。
- **[From Local to Global: A Graph RAG Approach to Query-Focused Summarization](https://arxiv.org/abs/2404.16130)** (*2024*) `Arxiv`
  > 微软 GraphRAG，用社区层级与全局摘要增强查询聚焦式问答。
- **[Voyager: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291)** (*2023*) `Arxiv`
  > 开放世界具身智能体，以技能库与程序式记忆持续探索与学习。
- **[Enhancing Long-Term Memory using Hierarchical Aggregate Tree for Retrieval Augmented Generation](https://arxiv.org/abs/2406.06124)** (*2024*) `Arxiv`
  > 层次聚合树记忆结构，用于增强检索增强生成的长程记忆。
- **[G-Memory: Tracing Hierarchical Memory for Multi-Agent Systems](https://arxiv.org/abs/2506.07398)** (*2025*) `Arxiv`
  > 面向多智能体系统的层级记忆追踪，组织共享历史与个体经验。
- **[Memory Decoder: A Pretrained, Plug-and-Play Memory for Large Language Models](https://arxiv.org/abs/2508.09874)** (*2025*) `Arxiv`
  > 预训练即插即用的记忆解码器，为 LLM 提供外部可读记忆。
- **[O-Mem: Omni Memory System for Personalized, Long Horizon, Self-Evolving Agents](https://arxiv.org/abs/2511.13593)** (*2025*) `Arxiv`
  > 面向个性化、长程、自进化智能体的全域记忆系统。
- **[MMAG: Mixed Memory-Augmented Generation for Large Language Models Applications](https://arxiv.org/abs/2512.01710)** (*2025*) `Arxiv`
  > 混合多种记忆形式增强生成，平衡事实性与推理能力。
- **[MemVerse: Multimodal Memory for Lifelong Learning Agents](https://arxiv.org/abs/2512.03627)** (*2025*) `Arxiv`
  > 面向终身学习智能体的多模态记忆，支持跨模态经历存储与调用。
- **[Memoria: A Scalable Agentic Memory Framework for Personalized Conversational AI](https://arxiv.org/abs/2512.12686)** (*2025*) `Arxiv`
  > 面向个性化对话 AI 的可扩展智能体记忆框架。
- **[Hindsight is 20/20: Building Agent Memory that Retains, Recalls, and Reflects](https://arxiv.org/abs/2512.12818)** (*2025*) `Arxiv`
  > 强调记忆的保留、回忆与反思三环节，构建更完整的 Agent 记忆。

#### 3.2 记忆写入与更新机制

- **[Inside Out: Evolving User-Centric Core Memory Trees for Long-Term Personalized Dialogue Systems](https://arxiv.org/abs/2601.05171)** (*2026*) `Arxiv`
  > 以用户为中心演化的核心记忆树，动态维护长期个性化对话中的稳定结论。
- **[MemInsight: Autonomous Memory Augmentation for LLM Agents](https://arxiv.org/abs/2503.21760)** (*2025*) `Arxiv`
  > 自主记忆增强，让 LLM 智能体自动决定写入什么、如何组织新增信息。
- **[STALE: Can LLM Agents Know When Their Memories Are No Longer Valid?](https://arxiv.org/abs/2605.06527)** (*2026*) `Arxiv`
  > 研究 LLM 智能体识别记忆失效的能力，处理旧结论的隐式过期判断。
- **[Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366)** (*2023*) `NeurIPS`
  > 以语言化自我反思更新经验，让智能体从失败中改进后续决策。
- **[Towards Lifelong Dialogue Agents via Timeline-based Memory Management](https://arxiv.org/abs/2406.10996)** (*2024*) `Arxiv`
  > 基于时间线的记忆管理，支撑终身对话智能体的持续更新。
- **[R³Mem: Bridging Memory Retention and Retrieval via Reversible Compression](https://arxiv.org/abs/2502.15957)** (*2025*) `Arxiv`
  > 通过可逆压缩在记忆保留与检索之间取得平衡。
- **[Memory-R1: Enhancing Large Language Model Agents to Manage and Utilize Memories via Reinforcement Learning](https://arxiv.org/abs/2508.19828)** (*2025*) `Arxiv`
  > 用强化学习训练智能体主动管理并利用外部记忆。
- **[Building Self-Evolving Agents via Experience-Driven Lifelong Learning: A Framework and Benchmark](https://arxiv.org/abs/2508.19005)** (*2025*) `Arxiv`
  > 经验驱动的终身学习框架与基准，支撑智能体持续自进化。
- **[In Prospect and Retrospect: Reflective Memory Management for Long-term Personalized Dialogue Agents](https://arxiv.org/abs/2503.08026)** (*2025*) `ACL`
  > 提出 RMM，以前瞻/回顾式反思分别优化记忆组织与检索排序。

#### 3.3 记忆检索策略

- **[From Isolated Conversations to Hierarchical Schemas: Dynamic Tree Memory Representation for LLMs](https://arxiv.org/abs/2410.14052)** (*2024*) `Arxiv`
  > 树状结构支持从原始对话到抽象结论的层级检索。
- **[GAM: Hierarchical Graph-based Agentic Memory for LLM Agents](https://arxiv.org/abs/2604.12285)** (*2026*) `Arxiv`
  > 层级图记忆支持沿关系的回溯式检索。
- **[Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory](https://arxiv.org/abs/2508.09736)** (*2025*) `Arxiv`
  > 多模态记忆的跨通道检索与推理调用。
- **[RAPTOR: Recursive Abstractive Processing for Tree-Organized Retrieval](https://arxiv.org/abs/2401.18059)** (*2024*) `ICLR`
  > 递归抽象式树状检索，在多粒度摘要上做兼顾全局与局部的问题回答。
- **[HippoRAG: Neurobiologically Inspired Long-Term Memory for Large Language Models](https://arxiv.org/abs/2405.14831)** (*2024*) `NeurIPS`
  > 受海马体启发的个性化知识图谱检索，实现单步多跳回忆。
- **[MemoRAG: Boosting Long Context Processing with Global Memory-Enhanced Retrieval Augmentation](https://arxiv.org/abs/2409.05591)** (*2024*) `WWW`
  > 用全局记忆生成草案线索，再据此检索长上下文中的关键信息。
- **[MemGuide: Intent-Driven Memory Selection for Goal-Oriented Multi-Session LLM Agents](https://arxiv.org/abs/2505.20231)** (*2025*) `Arxiv`
  > 意图驱动的记忆选择，面向目标导向的多会话 LLM 智能体。
- **[On Memory Construction and Retrieval for Personalized Conversational Agents](https://arxiv.org/abs/2502.05589)** (*2025*) `Arxiv`
  > 提出 SeCom，从记忆粒度与检索角度优化个性化对话智能体。

#### 3.4 用户模型与人物推断

- **[TiMem: Temporal-Hierarchical Memory Consolidation for Long-Horizon Conversational Agents](https://arxiv.org/abs/2601.02845)** (*2026*) `Arxiv`
  > 时间层级式记忆整合，支撑长跨度对话中稳定用户结论的沉淀。
- **[PersonaVLM: Long-Term Personalized Multimodal LLMs](https://arxiv.org/abs/2604.13074)** (*2026*) `Arxiv`
  > 长期个性化多模态大模型，融合跨模态个人历史形成用户画像。
- **[EgoSelf: From Memory to Personalized Egocentric Assistant](https://arxiv.org/abs/2604.19564)** (*2026*) `Arxiv`
  > 从自记忆到个性化第一视角助手，利用自我经历理解用户。
- **[HumanLLM: Towards Personalized Understanding and Simulation of Human Nature](https://arxiv.org/abs/2601.15793)** (*2026*) `Arxiv`
  > 面向个性化理解与人性模拟的大模型，建模个体深层特征。
- **[Enabling Personalized Long-term Interactions in LLM-based Agents through Persistent Memory and User Profiles](https://arxiv.org/abs/2510.07925)** (*2025*) `Arxiv`
  > 以持久记忆与用户画像支撑 LLM 智能体的长期个性化交互。
- **[RGMem: Renormalization Group-inspired Memory Evolution for Language Agents](https://arxiv.org/abs/2510.16392)** (*2025*) `Arxiv`
  > 借鉴重整化群思想的记忆演化，分层粗粒化形成稳定用户模型。
- **[Sophia: A Persistent Agent Framework of Artificial Life](https://arxiv.org/abs/2512.18202)** (*2025*) `Arxiv`
  > 持久化 Agent 框架，长期保存并演化个体状态与人格。

**记忆评测基准：**

- **[LoCoMo: Evaluating Long-Term Conversational Memory in Multi-Session Dialogue](https://arxiv.org/abs/2402.17753)** (*2024*) `Arxiv`
  > 首个规模化多会话对话记忆评测，衡量事件与人物长期记忆能力。
- **[LongMemEval: Benchmarking Chat Assistants on Long-Term Interactive Memory](https://arxiv.org/abs/2410.10813)** (*2024*) `Arxiv`
  > 面向聊天助手的长期交互记忆基准，覆盖信息检索与更新。
- **[KnowMe-Bench: Benchmarking Person Understanding for Lifelong Digital Companions](https://arxiv.org/abs/2601.04745)** (*2026*) `Arxiv`
  > 面向终身数字伴侣的「人物理解」基准，从真实互动评测用户画像理解。
- **[STALE: Can LLM Agents Know When Their Memories Are No Longer Valid?](https://arxiv.org/abs/2605.06527)** (*2026*) `Arxiv`
  > 评测智能体识别记忆失效与信息过期的能力。

### 第四章 恰当回应人

#### 4.1 个性化信息选择与上下文构建

- **[LaMP: When Large Language Models Meet Personalization](https://arxiv.org/abs/2304.11406)** (*2023*) `Arxiv`
  > 提出 LaMP 个性化基准，定义何时及如何用个人历史来个性化输出。
- **[PRIME: Large Language Model Personalization with Cognitive Dual-Memory and Personalized Thought Process](https://arxiv.org/abs/2507.04607)** (*2025*) `EMNLP`
  > 认知双记忆与个性化思维过程，兼顾语义与情景记忆的个性化。
- **[Measuring What Makes You Unique: Difference-Aware User Modeling for Enhancing LLM Personalization](https://arxiv.org/abs/2503.02450)** (*2025*) `Arxiv`
  > 差异感知的用户建模，聚焦「个体独特性」以增强个性化。
- **[Hello Again! LLM-powered Personalized Agent for Long-term Dialogue](https://arxiv.org/abs/2406.05925)** (*2024*) `NAACL`
  > 提出 LD-Agent，用事件记忆感知、人物提取与响应生成支撑长期对话。
- **[Mem-PAL: Towards Memory-based Personalized Dialogue Assistants for Long-term User-Agent Interaction](https://arxiv.org/abs/2511.13410)** (*2025*) `AAAI`
  > 基于记忆的个性化对话助手，面向长期人机交互。

#### 4.2 回应动作与交互策略选择

- **[From Empathy to Personalized Empathy: Adapting Empathetic Strategies to Individual Users](https://arxiv.org/abs/2606.00728)** (*2026*) `Arxiv`
  > 从通用共情走向个性化共情，按个体用户调整共情策略。
- **[Learning to Clarify: Multi-turn Conversations with Action-Based Contrastive Self-Training](https://arxiv.org/abs/2406.00222)** (*2024*) `Arxiv`
  > 以动作对比自训练学习「何时澄清、如何澄清」的多轮策略。
- **[CLAM: Selective Clarification for Ambiguous Questions with Generative Language Models](https://arxiv.org/abs/2212.07769)** (*2022*) `Arxiv`
  > 面向歧义问题的选择性澄清，判断是否需要追问以降低误答。

#### 4.3 回应生成与个性化表达

- **[Personalized Pieces: Efficient Personalized Large Language Models through Collaborative Efforts](https://arxiv.org/abs/2406.10471)** (*2024*) `Arxiv`
  > 通过协作式参数片段实现高效个性化大模型。
- **[Personalized Steering of Large Language Models: Versatile Steering Vectors Through Bi-directional Preference Optimization](https://arxiv.org/abs/2406.00045)** (*2024*) `ICML`
  > 用双向偏好优化学习通用 steering 向量，控制个性化风格。
- **[Steerable Chatbots: Exploring Personalization Control Interfaces via LLM Activation Steering](https://arxiv.org/abs/2505.04260)** (*2025*) `Arxiv`
  > 通过激活 steering 提供个性化控制接口，让用户调节聊天机器人风格。

#### 4.4 回应评估、边界控制与反馈校准

- **[OP-Bench: Benchmarking Over-Personalization for Memory-Augmented Personalized Conversational Agents](https://arxiv.org/abs/2601.13722)** (*2026*) `Arxiv`
  > 评测记忆增强个性化对话中的「过度个性化」问题。
- **[Personalized Safety in LLMs: A Benchmark and A Planning-Based Agent Approach](https://arxiv.org/abs/2505.18882)** (*2025*) `Arxiv`
  > 个性化场景下 LLM 安全基准与规划式对抗方法。
- **[Learning Personalized Agents from Human Feedback](https://arxiv.org/abs/2602.16173)** (*2026*) `Arxiv`
  > 从人类反馈中学习个性化智能体，把用户纠正用于策略更新。
- **[SPECTRA: Revealing the Full Spectrum of User Preferences via Distributional LLM Inference](https://arxiv.org/abs/2509.24189)** (*2025*) `Arxiv`
  > 用分布式推断还原用户偏好的完整谱系，避免单一化假设。
- **[Unveiling Privacy Risks in LLM Agent Memory](https://arxiv.org/abs/2502.13172)** (*2025*) `Arxiv`
  > 揭示 LLM 智能体记忆中的隐私泄露风险与边界问题。

### 第五章 主动关心人

#### 5.1 持续情境监测与潜在需求检测

- **[PASK: Toward Intent-Aware Proactive Agents with Long-Term Memory](https://arxiv.org/abs/2604.08000)** (*2026*) `Arxiv`
  > 意图感知的主动智能体，用长期记忆判断用户潜在需求。
- **[Vinci2: Providing Proactive Assistance in Continuous Egocentric Videos](https://arxiv.org/abs/2607.11523)** (*2026*) `Arxiv`
  > 从连续第一视角视频识别需要帮助的时刻，提供主动协助。
- **[Proactive Agent: Shifting LLM Agents from Reactive Responses to Active Assistance](https://arxiv.org/abs/2410.12361)** (*2024*) `ICLR`
  > 用环境观测预测用户潜在任务，把 LLM 智能体从被动响应转向主动帮助。
- **[ProAgent: Harnessing On-Demand Sensory Contexts for Proactive Agent Systems in the Wild](https://arxiv.org/abs/2512.06721)** (*2025*) `IMWUT`
  > 面向现实生活的主动智能体系统，按需感知与上下文推理提供即时协助。

#### 5.2 主动帮助目标与内容规划

- **[Interpersonal Memory Matters: A New Task for Proactive Dialogue Utilizing Conversational History](https://arxiv.org/abs/2503.05150)** (*2025*) `CoNLL`
  > 提出记忆感知主动对话任务，在合适时机把话题引向相关历史。
- **[ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation](https://arxiv.org/abs/2509.21730)** (*2025*) `Arxiv`
  > 通过用户—助手模拟开发主动且个性化的 AI 助手。
- **[PRINCIPLES: Synthetic Strategy Memory for Proactive Dialogue Agents](https://arxiv.org/abs/2509.17459)** (*2025*) `Arxiv`
  > 合成式策略记忆，为主动对话智能体规划介入内容。

#### 5.3 介入时机与沉默决策

- **[Preference-Driven Online Adaptation for Personalized Interaction Initiation in Proactive AI Assistants](https://arxiv.org/abs/2608.04416)** (*2026*) `Arxiv`
  > 偏好驱动的在线自适应，个性化决定主动助手的介入发起时机。
- **[ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation](https://arxiv.org/abs/2509.21730)** (*2025*) `Arxiv`
  > 通过模拟交互学习什么时机主动介入更合适。
- **[Vinci2: Providing Proactive Assistance in Continuous Egocentric Videos](https://arxiv.org/abs/2607.11523)** (*2026*) `Arxiv`
  > 依据第一视角情境判断何时提供帮助才能避免打扰。
- **[Sensible Agent: A Framework for Unobtrusive Interaction with Proactive AR Agents](https://arxiv.org/abs/2509.09255)** (*2025*) `UIST`
  > 非侵入式交互框架，用多模态情境感知动态决定「提供什么」与「如何传递」。

#### 5.4 用户反馈与主动策略更新

- **[ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation](https://arxiv.org/abs/2509.21730)** (*2025*) `Arxiv`
  > 用用户反馈模拟更新主动策略，控制介入频率与程度。
- **[Preference-Driven Online Adaptation for Personalized Interaction Initiation in Proactive AI Assistants](https://arxiv.org/abs/2608.04416)** (*2026*) `Arxiv`
  > 从用户接受/拒绝中在线学习个性化主动偏好。

---

## 🤝 Contributing

欢迎提交 Issue 或 PR 补充遗漏论文、修正链接、会议标签或分类。

## 📝 Citing

综述论文撰写中，敬请期待。若本清单对你有帮助，欢迎引用并关注后续版本。