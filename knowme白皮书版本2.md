# Knowme 白皮书（版本 2 · 完整大纲）

> **核心主线：** 理解人 → 恰当回应人 → 主动关心人
> **系统闭环：** 个人证据 → 用户模型 → 互动决策 → 用户反馈 → 持续更新

---

## 第一章 引言

- **研究背景：** Personal Agent 正从单次任务工具，走向长期服务具体用户的智能体。
- **现有问题：** 长期记忆、用户画像、个性化生成与主动交互仍分散在不同研究线索中，缺少统一组织框架。
- **本文主线：** 用"理解人—恰当回应人—主动关心人"重新组织技术组件、代表方法和研究缺口。

**相关综述：**

- [2024/04] A Survey on the Memory Mechanism of Large Language Model based Agents. [paper](https://arxiv.org/abs/2404.13501)
- [2025/12] Memory in the Age of AI Agents. [paper](https://arxiv.org/abs/2512.13564)
- [2024/11] Personalization of Large Language Models: A Survey. [paper](https://arxiv.org/abs/2411.00027)
- [2026/02] Toward Personalized LLM-Powered Agents: Foundations, Evaluation, and Future Directions. [paper](https://arxiv.org/abs/2602.22680)
- [2023/05] A Survey on Proactive Dialogue Systems: Problems, Methods, and Prospects. [paper](https://arxiv.org/abs/2305.02750)
- Proactive Conversational AI: A Comprehensive Survey. [paper](https://doi.org/10.1145/3715097)

---

## 第二章 Personal Agent 的定义与能力框架

### 2.1 从通用智能体到 Personal Agent

比较任务型 Agent、个性化系统和数字陪伴系统，说明长期服务为何要跨会话保留经历、状态、偏好与目标。比较重点：任务完成 · 长期连续性 · 用户特定性。

本领域两块基石：[Generative Agents](https://arxiv.org/abs/2304.03442)（UIST 2023）用"记忆流—反思—规划"确立智能体长期行为范式；[CoALA](https://arxiv.org/abs/2309.02427)（TMLR 2024）划定工作/情景/语义/程序性记忆的认知架构，成为后续工作的默认框架。

### 2.2 Personal Agent 的操作性定义

从六个方面界定研究对象：用户授权、跨时间个人证据、动态用户模型、个性化行动、适度主动、用户控制。定义边界：可更新 · 可追溯 · 可修正 · 可撤销。

### 2.3 三类核心能力及其递进关系

理解人形成长期用户认识；恰当回应把认识用于已有交互；主动关心进一步处理没有明确请求时的介入判断。

### 2.4 综述范围与组件化分类方法

聚焦个人证据怎样改变互动决策；一般规划、工具调用和多智能体协作不全面展开。章内组件：存储 · 更新 · 检索 · 推断 · 决策 · 生成 · 反馈。

---

## 第三章 理解人——从记住经历到理解变化

### 3.1 记住用户的经历（记忆表示与存储结构）

知道用户说过什么、做过什么，以及事件发生的时间和关系。比较树、事件图、主题图、时间层级和多模态记忆图，重点看抽象结论能否回溯到原始个人经历。

**代表工作：**

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

### 3.2 发现用户的稳定特点（记忆写入与更新机制）

从多次经历中总结用户的偏好、习惯、兴趣、关系和行为规律。讨论新证据写入、重复信息合并、冲突保留以及旧结论的修改、删除与隐式失效判断。

**代表工作：**

- [2026/01] Inside Out: Evolving User-Centric Core Memory Trees for Long-Term Personalized Dialogue Systems. [paper](https://arxiv.org/abs/2601.05171)
- [2025/03] MemInsight: Autonomous Memory Augmentation for LLM Agents. [paper](https://arxiv.org/abs/2503.21760)
- [2026/05] STALE: Can LLM Agents Know When Their Memories Are No Longer Valid? [paper](https://arxiv.org/abs/2605.06527)
- [2023/03] Reflexion: Language Agents with Verbal Reinforcement Learning. [paper](https://arxiv.org/abs/2303.11366)
- [2024/06] Towards Lifelong Dialogue Agents via Timeline-based Memory Management. [paper](https://arxiv.org/abs/2406.10996)
- [2025/02] R³Mem: Bridging Memory Retention and Retrieval via Reversible Compression. [paper](https://arxiv.org/abs/2502.15957)
- [2025/08] Memory-R1: Enhancing Large Language Model Agents to Manage and Utilize Memories via Reinforcement Learning. [paper](https://arxiv.org/abs/2508.19828)
- [2025/08] Building Self-Evolving Agents via Experience-Driven Lifelong Learning: A Framework and Benchmark. [paper](https://arxiv.org/abs/2508.19005)
- [2025/03] In Prospect and Retrospect: Reflective Memory Management for Long-term Personalized Dialogue Agents. [paper](https://arxiv.org/abs/2503.08026)

### 3.3 理解特点背后的情境（用户记忆的检索策略）

理解某个偏好在什么情况下成立、用户当前目标是什么，以及长期偏好和临时状态的区别。比较层级、向量、图回溯、实体约束和多路检索，讨论相关性、时效性、可信度与检索成本的平衡。

**代表工作：**

- [2024/10] From Isolated Conversations to Hierarchical Schemas: Dynamic Tree Memory Representation for LLMs. [paper](https://arxiv.org/abs/2410.14052)
- [2026/04] GAM: Hierarchical Graph-based Agentic Memory for LLM Agents. [paper](https://arxiv.org/abs/2604.12285)
- [2025/08] Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory. [paper](https://arxiv.org/abs/2508.09736)
- [2024/01] RAPTOR: Recursive Abstractive Processing for Tree-Organized Retrieval. [paper](https://arxiv.org/abs/2401.18059)
- [2024/05] HippoRAG: Neurobiologically Inspired Long-Term Memory for Large Language Models. [paper](https://arxiv.org/abs/2405.14831)
- [2024/09] MemoRAG: Boosting Long Context Processing with Global Memory-Enhanced Retrieval Augmentation. [paper](https://arxiv.org/abs/2409.05591)
- [2025/05] MemGuide: Intent-Driven Memory Selection for Goal-Oriented Multi-Session LLM Agents. [paper](https://arxiv.org/abs/2505.20231)
- [2025/02] On Memory Construction and Retrieval for Personalized Conversational Agents. [paper](https://arxiv.org/abs/2502.05589)

### 3.4 理解人的变化与不确定性（用户模型构建与人物推断）

识别偏好变化、信息过期、行为冲突和用户纠正；证据不足时不强行形成结论。重点讨论时间建模、更新、冲突处理、遗忘和拒绝推断。

**代表工作：**

- [2026/01] TiMem: Temporal-Hierarchical Memory Consolidation for Long-Horizon Conversational Agents. [paper](https://arxiv.org/abs/2601.02845)
- [2026/04] PersonaVLM: Long-Term Personalized Multimodal LLMs. [paper](https://arxiv.org/abs/2604.13074)
- [2026/04] EgoSelf: From Memory to Personalized Egocentric Assistant. [paper](https://arxiv.org/abs/2604.19564)
- [2026/01] HumanLLM: Towards Personalized Understanding and Simulation of Human Nature. [paper](https://arxiv.org/abs/2601.15793)
- [2025/10] Enabling Personalized Long-term Interactions in LLM-based Agents through Persistent Memory and User Profiles. [paper](https://arxiv.org/abs/2510.07925)
- [2025/10] RGMem: Renormalization Group-inspired Memory Evolution for Language Agents. [paper](https://arxiv.org/abs/2510.16392)
- [2025/12] Sophia: A Persistent Agent Framework of Artificial Life. [paper](https://arxiv.org/abs/2512.18202)

**评测基准：**

- [2024/02] LoCoMo: Evaluating Long-Term Conversational Memory in Multi-Session Dialogue. [paper](https://arxiv.org/abs/2402.17753)
- [2024/10] LongMemEval: Benchmarking Chat Assistants on Long-Term Interactive Memory. [paper](https://arxiv.org/abs/2410.10813)
- [2026/01] KnowMe-Bench: Benchmarking Person Understanding for Lifelong Digital Companions. [paper](https://arxiv.org/abs/2601.04745)
- [2026/05] STALE: Can LLM Agents Know When Their Memories Are No Longer Valid? [paper](https://arxiv.org/abs/2605.06527)

**本章逻辑：** 记住什么 → 怎样形成认识 → 怎样长期维护 → 怎样验证理解是否正确

---

## 第四章 恰当回应人——从个性化表达走向个性化决策

### 4.1 回答当前请求（个性化信息选择与上下文构建）

系统主要根据当前输入，生成正确、相关、安全的回答。讨论信息不足与信息过度使用的两类问题，比较历史检索、经历与信念区分以及个体差异提取。

**代表工作：**

- [2023/04] LaMP: When Large Language Models Meet Personalization. [paper](https://arxiv.org/abs/2304.11406)
- [2025/07] PRIME: Large Language Model Personalization with Cognitive Dual-Memory and Personalized Thought Process. [paper](https://arxiv.org/abs/2507.04607)
- [2025/03] Measuring What Makes You Unique: Difference-Aware User Modeling for Enhancing LLM Personalization. [paper](https://arxiv.org/abs/2503.02450)
- [2024/06] Hello Again! LLM-powered Personalized Agent for Long-term Dialogue. [paper](https://arxiv.org/abs/2406.05925)
- [2025/11] Mem-PAL: Towards Memory-based Personalized Dialogue Assistants for Long-term User-Agent Interaction. [paper](https://arxiv.org/abs/2511.13410)

### 4.2 让回答符合个人偏好（回应动作与交互策略选择）

利用用户历史调整内容、风格、长度、推荐结果或表达方式。把回应视为动作选择问题，比较不同用户和情境下的澄清策略、信息询问与个体化共情支持。这是从个性化生成走向个性化互动策略。

**代表工作：**

- [2026/06] From Empathy to Personalized Empathy: Adapting Empathetic Strategies to Individual Users. [paper](https://arxiv.org/abs/2606.00728)
- [2024/06] Learning to Clarify: Multi-turn Conversations with Action-Based Contrastive Self-Training. [paper](https://arxiv.org/abs/2406.00222)
- [2022/12] CLAM: Selective Clarification for Ambiguous Questions with Generative Language Models. [paper](https://arxiv.org/abs/2212.07769)

### 4.3 根据用户和情境选择回应方式（回应生成与个性化表达）

不只是改变"答案内容"，而是决定应该直接回答、先问清楚、提供选项、提出建议，还是不使用个人历史。讨论用户经历、长期信念、语言习惯和情绪背景如何影响信息内容、措辞、语气与支持方式。

**代表工作：**

- [2024/06] Personalized Pieces: Efficient Personalized Large Language Models through Collaborative Efforts. [paper](https://arxiv.org/abs/2406.10471)
- [2024/06] Personalized Steering of Large Language Models: Versatile Steering Vectors Through Bi-directional Preference Optimization. [paper](https://arxiv.org/abs/2406.00045)
- [2025/05] Steerable Chatbots: Exploring Personalization Control Interfaces via LLM Activation Steering. [paper](https://arxiv.org/abs/2505.04260)

### 4.4 在长期互动中调整回应（回应评估、边界控制与反馈校准）

根据用户的接受、修改、拒绝和纠正，逐渐调整回应方式。研究无关记忆调用、过度迎合、追问失控和停止规则，并把用户纠正用于后续偏好与回应策略更新；同时处理旧偏好、隐私边界和过度个性化问题。

**代表工作：**

- [2026/01] OP-Bench: Benchmarking Over-Personalization for Memory-Augmented Personalized Conversational Agents. [paper](https://arxiv.org/abs/2601.13722)
- [2025/05] Personalized Safety in LLMs: A Benchmark and A Planning-Based Agent Approach. [paper](https://arxiv.org/abs/2505.18882)
- [2026/02] Learning Personalized Agents from Human Feedback. [paper](https://arxiv.org/abs/2602.16173)
- [2025/09] SPECTRA: Revealing the Full Spectrum of User Preferences via Distributional LLM Inference. [paper](https://arxiv.org/abs/2509.24189)
- [2025/02] Unveiling Privacy Risks in LLM Agent Memory. [paper](https://arxiv.org/abs/2502.13172)

**本章深度递进：** 回答正确 → 内容适合这个人 → 回应方式适合这个人 → 长期互动越来越合适

---

## 第五章 主动关心人——从发现机会到适度介入

### 5.1 发现用户可能需要帮助（持续情境监测与潜在需求检测）

区分"观察到事件"和"用户可能需要帮助"。从持续信息流、当前活动和历史情境中识别困难、风险与帮助机会，同时讨论需求推断的证据基础和误判风险。

**代表工作：**

- [2026/04] PASK: Toward Intent-Aware Proactive Agents with Long-Term Memory. [paper](https://arxiv.org/abs/2604.08000)
- [2026/07] Vinci2: Providing Proactive Assistance in Continuous Egocentric Videos. [paper](https://arxiv.org/abs/2607.11523)
- [2024/10] Proactive Agent: Shifting LLM Agents from Reactive Responses to Active Assistance. [paper](https://arxiv.org/abs/2410.12361)
- [2025/12] ProAgent: Harnessing On-Demand Sensory Contexts for Proactive Agent Systems in the Wild. [paper](https://arxiv.org/abs/2512.06721)

### 5.2 判断需要是否真实、重要（主动帮助目标与内容规划）

发现潜在需求以后，系统应该主动提供什么。比较主动话题、推荐、提醒、任务指导、安全警告和错误恢复等帮助目标，而不仅是判断要不要介入。

**代表工作：**

- [2025/03] Interpersonal Memory Matters: A New Task for Proactive Dialogue Utilizing Conversational History. [paper](https://arxiv.org/abs/2503.05150)
- [2025/09] ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation. [paper](https://arxiv.org/abs/2509.21730)
- [2025/09] PRINCIPLES: Synthetic Strategy Memory for Proactive Dialogue Agents. [paper](https://arxiv.org/abs/2509.17459)

### 5.3 权衡收益、打扰成本与介入时机（介入时机与沉默决策）

帮助内容正确时，何时出现才不会变成打扰。结合时间偏好、活动阶段、任务进展和历史反馈，在立即介入、延迟介入与保持沉默之间选择；并选择沉默、询问、提醒、建议或请求授权等不同方式。

**代表工作：**

- [2026/08] Preference-Driven Online Adaptation for Personalized Interaction Initiation in Proactive AI Assistants. [paper](https://arxiv.org/abs/2608.04416)
- [2025/09] ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation. [paper](https://arxiv.org/abs/2509.21730)
- [2026/07] Vinci2: Providing Proactive Assistance in Continuous Egocentric Videos. [paper](https://arxiv.org/abs/2607.11523)
- [2025/09] Sensible Agent: A Framework for Unobtrusive Interaction with Proactive AR Agents. [paper](https://arxiv.org/abs/2509.09255)

### 5.4 从结果中学习（用户反馈与主动策略更新）

根据用户对主动帮助的接受、拒绝和忽略，学习不同场景下的主动偏好，控制介入频率和程度，并考虑长期信任与实际收益。讨论模拟用户反馈和长期真实反馈之间的差距。

**代表工作：**

- [2025/09] ProPerSim: Developing Proactive and Personalized AI Assistants through User-Assistant Simulation. [paper](https://arxiv.org/abs/2509.21730)
- [2026/08] Preference-Driven Online Adaptation for Personalized Interaction Initiation in Proactive AI Assistants. [paper](https://arxiv.org/abs/2608.04416)

**本章逻辑：** 按规则提醒 → 预测潜在需要 → 判断是否应该介入 → 学会怎样长期、适度地主动

---

## 第六章 应用场景——不同环境怎样组合三类能力

### 6.1 教育与学习支持

学习记录、知识状态和当前困难如何影响解释、反馈、困难发现与主动提示。重点边界：过度帮助 · 错误标签 · 学生自主性 · 教师控制 · 未成年人隐私。

### 6.2 车载与驾驶辅助

驾驶偏好、路线、注意与疲劳状态对低打扰交互、危险预警和任务协助的影响。重点边界：实时性 · 误报 · 驾驶干扰 · 安全责任。

### 6.3 可穿戴设备与个人健康

活动、生理、位置、音频和第一视角视频如何形成长期健康规律，并支持建议、状态解释和风险提醒。重点边界：持续监测隐私 · 敏感授权 · 误报 · 健康焦虑 · 功耗。

### 6.4 跨行业比较

用统一维度（用户证据 · 用户模型 · 回应方式 · 主动行为 · 行业风险）比较教育、车载和可穿戴场景，分析哪些组件可以通用、哪些必须重新设计。

---

## 第七章 综合讨论与未来方向

### 7.1 从分散组件走向闭环 Personal Agent

建立"个人证据—用户模型—互动决策—用户反馈—模型更新"的长期闭环。核心缺口：现有研究多集中在能力链的单个局部组件。

### 7.2 多模态、动态且可追溯的用户模型

连接对话、行为、环境和生理信息，区分当前状态与稳定特征，让深层用户结论能够回到原始证据。关键要求：动态更新 · 证据追溯 · 不确定性表达。

### 7.3 回应内容与主动时机的联合决策

联合决定是否介入、提供什么、怎样表达、何时出现和何时停止，避免把内容与时机拆成两个独立问题。

### 7.4 真实反馈与长期在线适应

在长期交互中研究接受、忽略、拒绝和纠正，避免少量偶然反馈被固化为稳定偏好。研究缺口：真实长期反馈仍少于预设 Persona 与模拟用户。

### 7.5 用户授权、控制与安全边界

提供透明记忆管理、用户修正、授权控制、主动行为降级和可撤销机制。控制机制：查看 · 修正 · 授权 · 降级 · 撤销。

### 7.6 面向完整能力链的评测

同时衡量理解准确性、证据可追溯性、回应适当性、主动帮助价值、打扰成本和长期适应效果。评价目标：更准 · 更合适 · 更可控 · 更持续有效。

---

## 第八章 结论

三类能力共同定义以人为中心的 Personal Agent：

- **理解人：** 由长期个人证据形成动态、可追溯、允许修正的用户模型。
- **恰当回应与主动关心：** 把用户模型转化为合适的回应与适度的主动介入。
- **当前研究缺口：** 局部组件已有进展，但受控、可持续适应的完整闭环仍未形成。

**系统闭环：** 个人证据 → 用户模型 → 互动决策 → 用户反馈 → 持续更新