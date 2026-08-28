# Knowme: 以人为中心的 Personal Agent 综述

> **理解人 · 恰当回应人 · 主动关心人**
>
> 📋 完整大纲见 [knowme白皮书版本2.md](./knowme白皮书版本2.md) · 综述撰写中，论文列表持续更新

一篇关于 **Personal Agent（个人智能体）** 的综述论文之配套仓库。我们以"**理解人 → 恰当回应人 → 主动关心人**"为主线，系统整理长期记忆、用户建模、个性化回应与主动介入等技术组件的代表工作。

**核心系统闭环：** 个人证据 → 用户模型 → 互动决策 → 用户反馈 → 持续更新

---

## 🎯 必读经典（Agent Memory 与 Personal Agent 领域）

### 奠基工作与认知框架

- [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442) — UIST 2023 — 记忆流+反思+规划，智能体长期行为模拟的开山之作
- [Cognitive Architectures for Language Agents (CoALA)](https://arxiv.org/abs/2309.02427) — TMLR 2024 — 智能体记忆分类的"默认"认知框架：工作/情景/语义/程序性记忆
- [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) — arXiv 2023 — 借操作系统虚拟内存思想分层管理 LLM 上下文（Letta 前身）

### 记忆系统与工程框架

- [MemoryBank](https://arxiv.org/abs/2305.10250) — AAAI 2024 — 艾宾浩斯遗忘曲线启发的长期记忆机制
- [Mem0](https://arxiv.org/abs/2504.19413) — arXiv 2025 — 生产级可扩展记忆层：抽取-更新式事实记忆（59k+ star 开源框架）
- [Zep: A Temporal Knowledge Graph Architecture for Agent Memory](https://arxiv.org/abs/2501.13956) — arXiv 2025 — 双时态知识图谱记录事实有效期（Graphiti 引擎）
- [A-Mem: Agentic Memory for LLM Agents](https://arxiv.org/abs/2502.12110) — arXiv 2025 — 卡片盒笔记法（Zettelkasten）启发的自组织记忆网络
- [MemoryOS](https://arxiv.org/abs/2506.06326) — EMNLP 2025 — 短期/中期/长期三层记忆的操作系统式管理，热度驱动动态升级
- [MemOS: A Memory OS for AI System](https://arxiv.org/abs/2507.03724) — arXiv 2025 — 统一明文/激活/参数三类记忆的调度与演化，MemCube 记忆单元
- [HippoRAG](https://arxiv.org/abs/2405.14831) — NeurIPS 2024 — 海马体索引理论启发，KG+PageRank 检索
- [RAPTOR](https://arxiv.org/abs/2401.18059) — ICLR 2024 — 递归抽象处理的树形组织检索，层级记忆检索经典
- [GraphRAG](https://arxiv.org/abs/2404.16130) — arXiv 2024 — 从局部到全局的知识图谱式检索与摘要
- [MemoRAG](https://arxiv.org/abs/2409.05591) — arXiv 2024 — 全局记忆模型生成检索线索，引导证据检索
- [MemInsight](https://arxiv.org/abs/2503.21760) — arXiv 2025 — 自主属性挖掘，增强记忆的检索与推荐
- [Memory3](https://arxiv.org/abs/2407.01178) — arXiv 2024 — 显式记忆作为独立于参数与上下文的第三种知识形态
- [MemoryLLM](https://arxiv.org/abs/2402.04624) — ICML 2024 — 参数内自可更新记忆池；扩展版 [M+](https://arxiv.org/abs/2502.00592) 支持长期记忆

### 领域综述

- [A Survey on the Memory Mechanism of LLM based Agents](https://arxiv.org/abs/2404.13501) — ACM TOIS 2025 — 最早的智能体记忆系统综述之一：写什么/怎么管/怎么读
- [Memory in the Age of AI Agents](https://arxiv.org/abs/2512.13564) — arXiv 2025 — 47 位作者大综述：形式/功能/动态三轴分类法
- [Personalization of Large Language Models: A Survey](https://arxiv.org/abs/2411.00027) — arXiv 2024 — LLM 个性化的数据、技术、评测与应用分类框架
- [A Survey on Proactive Dialogue Systems](https://arxiv.org/abs/2305.02750) — IJCAI 2023 — 首篇系统综述主动对话系统
- [Proactive Conversational AI: A Comprehensive Survey](https://doi.org/10.1145/3715097) — ACM TOIS 2025 — 覆盖各类对话中主动性的最新综述

---

## 📑 目录

- [必读经典](#-必读经典agent-memory-与-personal-agent-领域)
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

Personal Agent 正从单次任务工具，走向长期服务具体用户的智能体。现有研究中长期记忆、用户画像、个性化生成与主动交互仍分散在不同研究线索中，本综述用统一能力框架重新组织。领域综述见上方 [必读经典 · 领域综述](#领域综述) 板块。

## 第二章 定义与能力框架

界定 Personal Agent 与一般 Agent 的根本区别（任务完成 · 长期连续性 · 用户特定性），从用户授权、跨时间个人证据、动态用户模型、个性化行动、适度主动和用户控制六个方面给出操作性定义。

核心参考：[Generative Agents](https://arxiv.org/abs/2304.03442)、[CoALA](https://arxiv.org/abs/2309.02427)、[MemGPT](https://arxiv.org/abs/2310.08560)（见必读经典板块）。

## 第三章 理解人

### 3.1 记忆表示与存储结构

比较树、事件图、主题图、时间层级和多模态记忆图，重点看抽象结论能否回溯到原始个人经历。

- [MemTree](https://arxiv.org/abs/2410.14052) — ICLR 2025 — 动态树结构组织长期记忆，支持多抽象层检索
- [GAM](https://arxiv.org/abs/2604.12285) — arXiv 2026 — 分层图记忆解耦编码与巩固，兼顾效率一致性
- [M3-Agent](https://arxiv.org/abs/2508.09736) — arXiv 2025 — 多模态实体中心记忆图，RL 训练迭代推理
- [M2A](https://arxiv.org/abs/2602.07624) — arXiv 2026 — 双层混合记忆在线更新，长期多模态个性化

经典记忆框架（详见 [必读经典板块](#-必读经典agent-memory-与-personal-agent-领域)）：MemGPT · MemoryBank · Mem0 · Zep · A-Mem · MemoryOS · MemOS · RAPTOR · GraphRAG · HippoRAG · Memory3 · MemoryLLM/M+

### 3.2 记忆写入与更新机制

新证据写入、重复信息合并、冲突保留以及旧结论的修改、删除与隐式失效判断。

- [Inside Out](https://arxiv.org/abs/2601.05171) — arXiv 2026 — PersonaTree 核心记忆树，可控演化的用户画像
- [STALE](https://arxiv.org/abs/2605.06527) — arXiv 2026 — 评测 LLM 智能体能否识别记忆失效并修正过时用户状态
- [MemInsight](https://arxiv.org/abs/2503.21760) — arXiv 2025 — 自主属性挖掘增强记忆

### 3.3 记忆检索策略

比较层级、向量、图回溯、实体约束和多路检索，讨论相关性、时效性、可信度与检索成本的平衡。

- [MemTree](https://arxiv.org/abs/2410.14052) — ICLR 2025
- [GAM](https://arxiv.org/abs/2604.12285) — arXiv 2026
- [M3-Agent](https://arxiv.org/abs/2508.09736) — arXiv 2025
- [HippoRAG](https://arxiv.org/abs/2405.14831) — NeurIPS 2024 — KG+PageRank 多跳检索
- [RAPTOR](https://arxiv.org/abs/2401.18059) — ICLR 2024 — 树形层级检索
- [MemoRAG](https://arxiv.org/abs/2409.05591) — arXiv 2024 — 全局记忆引导检索

### 3.4 用户模型与人物推断

个人证据怎样转化为状态、画像、动机与未来选择；重点看深层结论能否由历史证据支持并允许用户修正。

- [TiMem](https://arxiv.org/abs/2601.02845) — ACL 2026 Findings — 时间记忆树五层固化，从事实到人格画像
- [PersonaVLM](https://arxiv.org/abs/2604.13074) — CVPR 2026 — 多模态记忆库加人格演化，长期个性化助手
- [EgoSelf](https://arxiv.org/abs/2604.19564) — arXiv 2026 — 第一视角图记忆建模用户习惯，预测交互
- [HumanLLM](https://arxiv.org/abs/2601.15793) — KDD 2026 — 认知基因组数据集微调，模拟个人行为思维

**记忆评测基准：**

- [LoCoMo](https://arxiv.org/abs/2402.17753) — ACL 2024 — 超长对话记忆基准：问答、摘要与生成
- [LongMemEval](https://arxiv.org/abs/2410.10813) — ICLR 2025 — 五大记忆能力评测：抽取、多会话、时序等
- [KnowMe-Bench](https://arxiv.org/abs/2601.04745) — ACL 2026 — 自传叙事三层评测，衡量对"人"的理解
- [STALE](https://arxiv.org/abs/2605.06527) — arXiv 2026 — 记忆时效性评测

## 第四章 恰当回应人

### 4.1 个性化信息选择与上下文构建

当前回应应该调用哪些用户历史；讨论信息不足与信息过度使用两类问题。

- [LaMP](https://arxiv.org/abs/2304.11406) — ACL 2023 — 首个 LLM 个性化基准，覆盖多任务个性化生成与分类
- [PRIME](https://arxiv.org/abs/2507.04607) — arXiv 2025 — 认知双记忆模型，情景/语义记忆加个性化慢思考
- [DPL](https://arxiv.org/abs/2503.02450) — arXiv 2025 — 用户间差异感知建模，提取结构化差异定制生成

### 4.2 回应动作与交互策略选择

把回应视为动作选择问题：直接回答、澄清、询问、建议还是提供支持。

- [PereGRM](https://arxiv.org/abs/2606.00728) — arXiv 2026 — 个性化共情奖励建模（含 PersonaEmp 数据集），按用户特质自适应共情策略
- [ACT](https://arxiv.org/abs/2406.00222) — ICLR 2025 — 动作对比自训练，教会多轮代理主动澄清歧义
- [CLAM](https://arxiv.org/abs/2212.07769) — arXiv 2022 — LLM 澄清提问经典：选择性检测歧义并生成澄清问题

### 4.3 回应生成与个性化表达

用户经历、长期信念、语言习惯和情绪背景如何影响信息内容、措辞、语气与支持方式。

- [LaMP](https://arxiv.org/abs/2304.11406) — ACL 2023
- [PER-PCS](https://arxiv.org/abs/2406.10471) — EMNLP 2024 — 用户共享 PEFT 参数片段组装个性化适配器，兼顾隐私与效率
- [BiPO](https://arxiv.org/abs/2406.00045) — arXiv 2024 — 双向偏好优化生成通用转向向量，可控调节个性化行为
- [Steerable Chatbots](https://arxiv.org/abs/2505.04260) — arXiv 2025 — 偏好激活转向，推理时轻量对齐用户偏好

### 4.4 回应评估、边界控制与反馈校准

什么时候应该克制、停止追问或承认信息不足；把用户纠正用于后续策略更新。

- [OP-Bench](https://arxiv.org/abs/2601.13722) — arXiv 2026 — 首个过度个性化基准：无关/重复/谄媚三类失败模式
- [PENGUIN](https://arxiv.org/abs/2505.18882) — NeurIPS 2025 — 个性化安全基准（1.4 万敏感场景）与规划式代理 RAISE
- [PAHF](https://arxiv.org/abs/2602.16173) — arXiv 2026 — 事前澄清+事后反馈双通道在线学习，适应用户偏好漂移
- [PET](https://arxiv.org/abs/2509.24189) — arXiv 2025 — 偏好建模为可解释偏好簇分布，追踪动态演化

## 第五章 主动关心人

### 5.1 持续情境监测与潜在需求检测

区分"观察到事件"和"用户可能需要帮助"；讨论需求推断的证据基础和误判风险。

- [PASK](https://arxiv.org/abs/2604.08000) — arXiv 2026 — 需求检测（IntentFlow）+ 自演化长期记忆 + 流式主动 Agent
- [Vinci2](https://arxiv.org/abs/2607.11523) — ECCV 2026 — 首个第一视角主动服务基准 EgoServe 与智能体 EgoMemo
- [Proactive Agent](https://arxiv.org/abs/2410.12361) — arXiv 2024 — ProactiveBench，从被动响应转向主动协助

### 5.2 主动帮助目标与内容规划

比较主动话题、推荐、提醒、任务指导、安全警告和错误恢复等帮助目标。

- [MapDia](https://arxiv.org/abs/2503.05150) — CoNLL 2025 — 记忆感知主动对话任务，适时转向历史话题
- [ProPerSim](https://arxiv.org/abs/2509.21730) — arXiv 2025 — 家庭场景用户-助手仿真，学习合适时机的个性化推荐

### 5.3 介入时机与沉默决策

结合时间偏好、活动阶段、任务进展和历史反馈，在立即介入、延迟介入与保持沉默之间选择。

- [EOPA](https://arxiv.org/abs/2608.04416) — arXiv 2026 — 证据驱动在线适配，学习用户专属交互时机偏好
- [ProPerSim](https://arxiv.org/abs/2509.21730) — arXiv 2025
- [Vinci2](https://arxiv.org/abs/2607.11523) — ECCV 2026

### 5.4 用户反馈与主动策略更新

利用真实反馈调整主动内容、频率与时机；讨论模拟反馈与长期真实反馈的差距。

- [ProPerSim](https://arxiv.org/abs/2509.21730) — arXiv 2025
- [EOPA](https://arxiv.org/abs/2608.04416) — arXiv 2026

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
