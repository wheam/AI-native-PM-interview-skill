# AI Native PM 能力模型

> 综合 19 家公司 JD（Anthropic/OpenAI/Google/Meta/字节/DeepSeek/MiniMax/智谱/Kimi/Cursor/Manus/Mistral/Perplexity/Cohere/Scale/Character.AI/HuggingFace/Replit/xAI）+ 9 位业内大神方法论 + 12 家面试真题提炼。
> 用途：作为 `ai-pm-interview` skill 的能力基准，用于知识点测试、简历筛选、模拟面试的评判标尺。

---

## 一、一句话定义

> **AI Native PM = 能把概率性 AI 能力转化为用户可信赖产品价值的人。**
> 区别于传统 PM 的本质：传统 PM 管理"确定性功能的交付"；AI PM 引导"概率性模型达成结果"，工作核心从"写 spec 等实现"转向"决策做什么 + 评判 AI 输出好坏"。

Mike Krieger（Anthropic CPO）："瓶颈已从工程（写代码）转移到决策（做什么）。"

---

## 二、六大核心能力（横向汇总，按出现频率排序）

### 能力 1：模型能力边界感知（Model Sense）⭐ 最高频
**定义**：准确判断当前模型"能做什么、不能做什么、什么时候会失败"，用以指导产品设计。

- 理解 LLM 工作机制：Token/上下文窗口/Embedding/Transformer/注意力/MoE
- 理解局限：幻觉（类型 + 产品层面缓解）、复读、中间遗忘、概率性不确定
- 区分 Prompt vs RAG vs Fine-tuning 的适用场景与决策树
- 懂 Agent 机制：Agent Loop、Tool Use、Planning、Memory、MCP、Multi-Agent
- **判断信号**：能否在不写代码的前提下，与研究员/工程师就模型能力做有深度的对话

> JD 证据：几乎所有公司都要求。Anthropic"technical fluency"、字节"模型能力边界感知"、DeepSeek"理解 LLM 及 Agent 机制（KV Cache/Agent Loop/MCP）"、Meta"理解模型边界设合理预期"。

### 能力 2：Eval / 评估能力 ⭐ 高级岗标配
**定义**：能定义并构建衡量 AI 产出质量的评估体系——这是传统 PM 岗不需要的差异化能力。

- 设计量化评估指标（而非活动指标）：task completion rate、hallucination rate、faithfulness、groundedness
- 构建 golden set、人工评估 + 自动化评估（LLM-as-judge）融合
- 把模糊的"智能/好"转化为清晰可辩护的指标
- 评估结果反哺模型迭代方向

> JD 证据：Anthropic Claude Code Model Perf PM"亲手构建过 agentic evals"、Cursor Agent Harness PM"定义质量指标驱动研发"、字节评测 PM、Kimi"Agent 模型评估 PM"、a16z"像访谈用户一样访谈模型，会写 evals"。

### 能力 3：产品判断力 / Product Sense
**定义**：识别真实用户摩擦点、定义问题、在不确定中做有据可查的决策。Shreyas Doshi 称之为"唯一长期护城河"。

- 五力（Shreyas）：强同理心、推演能力、战略思维、好品味（多个 AI 方案选最优并解释）、创造性执行
- 用户细分 → 痛点 → 方案（Meta 核心考法）
- 找 Model-Product-Market Fit（模型能力、产品形态、市场需求三角共振）
- 为不确定性/可解释性/信任设计 UX（confidence UI、fallback、引用来源）

### 能力 4：Builder / 动手能力 ⭐ AI-native 公司硬要求
**定义**：自己能用 AI 工具原型验证想法，而非写 PRD 等工程师实现。

- 每天高强度使用 AI 工具（Claude Code/Cursor/ChatGPT 等），有强烈好坏判断
- 能 Vibe Coding / 用 AI 辅助写代码、跑 demo（DeepSeek、Cursor 列为硬要求）
- 数据分析能力（部分岗要求 SQL/Python，如 Scale AI mandatory）
- 默认 ship 而非 explore 数月

> JD 证据：Cursor"PM 自己构建功能第一版"、DeepSeek"能用 Vibe Coding 写代码"、Replit"本人是活跃用户（明确要求）"、a16z"每天用 AI 成为公司标杆"、Claire Vo"PM 须会写代码原型"。

### 能力 5：数据驱动 + 商业化
**定义**：用数据（而非直觉）驱动决策，并能跳出功能思考商业模式。

- AI 产品度量的特殊性：传统 engagement 指标（DAU/会话数）有误导性，真正指标是"实际创造的价值"（省了多少时间/解决什么问题）——Mike Krieger
- A/B 测试 AI 功能的特殊性（概率性输出难做对照）
- 增长漏斗（acquisition/activation/retention/monetization，D1/D7/D30）
- 商业化：按量付费 vs 订阅，定价分层，LTV/ARPU/CAC，企业 GTM（pricing/packaging/positioning）

### 能力 6：跨职能 + Safety/Responsible AI 意识
**定义**：能对齐研究/工程/设计/Sales/Legal，并把安全内建于产品。

- Research Partnership：能直接影响研究团队，非纯执行（Anthropic"嵌入研究团队 = 10x 价值"）
- Safety-by-design：安全是产品本能不是事后合规（Anthropic 面试 Safety 专项轮，权重极高）
- Responsible AI：bias 消除、red-teaming、内容安全边界、合规（尤其多模态/ToB/面向青少年场景）
- 在模糊（ambiguity）中驱动共识——所有公司高频词

---

## 三、各公司侧重差异（面试针对性准备用）

| 公司 | 最看重 | 独特考点 |
|------|--------|---------|
| **Anthropic** | AI Safety Judgment（权重极高） | "治理一个模型"；MCP；Responsible Scaling Policy；model taste |
| **OpenAI** | 概率性思维 + Mission | 为概率系统设计 guardrails；批判性（"你不喜欢 OpenAI 什么"）|
| **Google** | 经典产品严谨 + 技术深度 | BUS 框架；AI search 战略判断；估算题 |
| **Meta** | 用户细分 + 执行速度 | Binary tradeoff 题；stress test AI 输出"什么会在 scale 时崩" |
| **字节 Seed/豆包** | 主动技术学习（读论文搭 Demo） | 5Why 深挖；模型选型；幻觉产品处理；Prompt 案例 |
| **DeepSeek** | Agent 重度用户 + Vibe Coding | 几乎是"工程师即 PM"；懂 Agent Loop/MCP/Context Engineering |
| **腾讯混元** | 大模型八股 | RLHF/PPO/DPO/LoRA/Transformer 原理 |
| **Cursor** | PM 即 Builder | 读 agent traces；定义 eval；默认 ship；taste for models |
| **Manus** | AI 能力转化 + 普通话 | 把 LLM/Agent 能力转可靠产品；负责任 AI |

**趋势**：xAI/Cursor/DeepSeek 模糊了 PM 与工程边界——"工程师即 PM"或"PM 即 Builder"是最 AI-native 的形态。

---

## 四、9 位大神框架速查（评判时引用）

| 作者 | 框架 | 核心 |
|------|------|------|
| Lenny Rachitsky | PM 技能🤖冲击矩阵 | AI 冲击最大的是高阶技能（战略/愿景）；人际对齐/品味/创造力是护城河 |
| Mike Krieger (Anthropic CPO) | 决策力替代编码力 | 瓶颈转向"做什么"；嵌入研究团队 10x；度量"实际价值"非 engagement |
| a16z (Anish) | 5 原则 | 访谈模型/极端定价/先发+情感护城河/模型是平台/每天用 AI |
| Claire Vo | Automate-AddSkills-Multiply | 传统 PM 已死；做"乘法器"非"贡献者" |
| Shreyas Doshi | Product Sense 五力 | Product Sense 是唯一长期护城河；AI 工具熟练度会贬值 |
| HelloPM (Ankit) | POWER（5步） | 先解决问题空间再解决方案空间；Top1% 用 AI 解决自己的问题 |
| Aakash Gupta | 传统 vs AI PM 对比 | ML 直觉（precision/recall 是产品决策）+ 数据飞轮 + 伦理 |
| Kenny（中文） | Model-Product-Market Fit | 全链路判断；警惕路径依赖；0-1 要精细完美才成立=不成立 |
| Fiona Fung (Anthropic Eng) | AI-native 组织重构 | 聚焦比工具更重要 |

---

## 五、能力自检清单（候选人对照）

- [ ] 我能讲清 LLM 的幻觉有哪几类，以及产品层面怎么缓解（不只是技术层面）
- [ ] 我能说出某个场景该选 Prompt / RAG / Fine-tuning，并解释为什么
- [ ] 我亲手为某个 AI 功能设计过评估方法（指标 + 测试集）
- [ ] 我每天/每周高强度使用至少 2-3 个 AI 产品，且能说出它们的优劣差异
- [ ] 我能用 AI 工具自己跑出一个产品原型/demo（不依赖工程师）
- [ ] 我的项目经历里有量化结果（不是"提升了体验"而是"X 指标 +Y%"）
- [ ] 我能解释为什么 AI 产品的成功指标不能只看 DAU/engagement
- [ ] 我能就模型能力与工程师/研究员做有深度的技术对话
- [ ] 我有对 AI safety / responsible AI 的真实思考（非口号）
- [ ] 我能找到一个 Model-Product-Market Fit 的具体例子并分析
