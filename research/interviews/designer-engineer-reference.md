---
captured: 2026-06-05
topic: AI 公司设计师 & 工程师岗位 JD 与面试考点（反哺 PM 准备）
sources: Anthropic/OpenAI/Cursor 官方职位页, Exponent, 知乎/CSDN
researcher: subagent (Sonnet 4.6)
---

# AI 公司设计师 & 工程师岗位 JD 与面试考点（反哺 PM）

## 一、设计师（Product Designer / AI UX Designer）

### Anthropic — Product Designer, Enterprise
- 8+ 年；将 Claude 从"工具"设计为"trusted collaborator"；为企业去除 AI 采用障碍
- **AI native**：理解 LLM 能力边界，基于 LLM 特性设计新交互范式；用 prototyping（含 HTML/CSS/JS）快速验证
- 同时承担 PM/Designer/Brand 角色；$305K–$385K
- 原文："Design new, functional, easy-to-use **interaction conventions at the frontier**." / "Technical understanding of LLMs and ability to build on top of them."

### OpenAI — Product Designer, ChatGPT
- 4+ 年；**会写前端代码（用 Codex 推细节）**，承担设计+品牌+文案多职能
- 加分：有 AI 设计作品集，能讲清"AI 产品与非 AI 产品的不同"

### 设计师面试流程（OpenAI 为例）
Recruiter → **Portfolio Review（最大筛选关，~25% pass）** → Portfolio Presentation(~10人panel) → Portfolio Follow-up(高级设计负责人追问) → Whiteboarding(设计 AI 产品实操) → App Critique → Behavioral

**关键考点**：
- Portfolio：考 narrative 而非视觉，AI 项目要突出"AI 产品与非 AI 的差异"
- Whiteboarding："Design an app that incorporates X with AI"——定义模糊问题+有意义的 AI 整合（不为 AI 而 AI）
- App Critique：批判"决策"不是描述 UI
- Follow-up 压力测试：设计能否承受 speed/latency/scalability/actual vs perceived performance 约束

### 🔑 对 PM 的启发
| 设计师能力 | PM 启发 |
|---|---|
| 设计"不确定性"的 UX | PM 方案需考虑 confidence UI、fallback |
| Latency 与感知性能 | 定义"AI 响应速度"体验指标 |
| Trust-building 设计 | PRD 含 trust & safety 模块 |
| Interaction conventions at frontier | 从零定义新场景用户旅程 |
| Rapid prototyping with code | 掌握基础 prompt 工程能跑 demo |

---

## 二、工程师（AI Engineer / Research Engineer / FDE）

### Anthropic — Research Engineer, Model Evaluations
- 构建 Eval 基础设施，将模糊的"智能"转化为清晰可辩护的指标
- 设计 eval 实验；大规模运行 eval 系统；解读 training checkpoint 结果；$320K–$485K
- 原文："Transform ambiguous notions of 'intelligence' into clear, defensible metrics."

### Cursor — Forward Deployed Engineer
- 嵌入客户工程团队，端到端 own 生产级 AI workflow
- Discovery(识别真正瓶颈)→快速 ship(days)→硬化为可靠系统(weeks)→沉淀可复用 pattern
- 生产质量：Tracing & evals、Metrics & debugging、Model behavior analysis、Latency/cost tradeoffs、Failure mode
- 原文："This is **not a demo role**." / "built and owned AI-native workflows in production—not just prototypes—and have debugged real-world model failures."

### 字节/国内大厂 — AI Agent 工程师
- Agent 架构（任务规划/工具调用/多 Agent）；Prompt Engineering（CoT/Few-shot）；RAG+向量库
- 框架 LangChain/LangGraph/AutoGen/CrewAI/Coze；Python/Go；Docker/K8s
- 字节 30%+ 后端岗位要求大模型开发能力

### AI 工程师面试考点（2025-26）
**基础层**：Transformer & Attention（Q/K/V/multi-head）；Tokenization（BPE，token≠word）；Prompt vs RAG vs Fine-tuning 决策树；Embeddings & Vector Search
**核心层**：RAG Pipeline（chunking/reranker/hybrid/抑制幻觉）；**Eval 方法论**（golden set/LLM-as-judge/Faithfulness-Relevance-Groundedness）；Agent 架构（ReAct/Supervisor-Worker/Tool calling/Memory）；Agentic System Design（任务分解/循环控制/Prompt injection 防御）
**进阶层**：生产质量（Tracing/Latency-Cost tradeoff）；Failure mode 分析；Model Evaluation infra；架构 tradeoff
**软性**："What AI coding assistants do you use, and why?"（技术品味）；"Design an AI pipeline for fuzzy scenario"；"How would you debug this agent loop?"

### 🔑 对 PM 的启发
| 工程师能力 | PM 启发 |
|---|---|
| Eval 设计思维 | 定义 AI 产品 success metrics（task completion rate/hallucination rate 而非只 engagement）|
| RAG vs Fine-tuning 选型 | 能与工程师讨论"知识注入"路径 |
| Agent 规划能力 | 定义功能时像 agent planner 做任务分解 |
| Failure mode 意识 | PRD 含"AI 失败时 fallback 流程" |
| Latency/Cost tradeoff | 理解 token 成本/推理时间对体验和商业的影响 |
| Discovery 能力(FDE) | user research 本质是找真实痛点 |

---

## 三、三类岗位共同 AI Native 能力核心（PM 复习优先级）
1. 理解 LLM 能力边界（幻觉/上下文窗口/不确定性）
2. 从模糊问题→清晰可执行 scope
3. 以指标/eval 衡量 AI 产出质量
4. 快速原型验证（设计师用 code，工程师用 demo）
5. 生产级思维：failure mode/fallback/监控
6. 用户信任构建（reliability/transparency/safety）

**PM 独有延伸**：Roadmap 优先级+商业 impact｜跨职能对齐｜AI 产品 GTM 与 adoption 策略

### PM 备考行动（从设计师&工程师 JD 反推）
- 学会用 "trust"/"interpretability"/"interaction convention" 描述 AI UX 决策
- 练习 AI 产品 critique（批判 AI 能力整合决策）
- 案例中主动提 AI-specific metrics
- 能口述 Agent 与 Chatbot 本质区别及为何选 Agent 架构
- 用 "discovery→fast ship→harden" 框架讲产品迭代经历
