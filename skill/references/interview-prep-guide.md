# AI Native PM 面试备考指南

> 综合 12 家公司真实面试流程 + 高频真题 + 过来人经验提炼。
> 用途：作为 `ai-pm-interview` skill 的备考资料输出，也作为模拟面试出题的题库参考。

---

## 一、面试流程通用结构

**海外大厂（4–8 周）**
Recruiter Screen → Hiring Manager（深挖项目）→ Onsite Loop（4–8 轮）：Product Sense / Analytical / Technical / Behavioral，AI 公司额外加 **AI/Safety 专项轮**。

**国内大厂（5 轮）**
HR 初筛 → 业务一面（简历深挖 + AI 基础 + 项目）→ 业务二面（Case + 数据 + 竞品）→ Leader/总监面（战略 + 价值观）→ HR 面（薪资）。

---

## 二、六大考察板块 + 高频真题

### 板块 1：AI 技术理解（AI PM 专属，最易露馅）
- 什么是 LLM 幻觉？有哪几类（Intrinsic/Extrinsic/Fabrication）？**产品层面**如何缓解？
- Prompt vs RAG vs Fine-tuning：什么场景选哪个？决策树是什么？
- 怎么理解 RAG？优劣势、适用场景、如何构建知识库 + 优化检索？
- Token/上下文窗口/Embedding/Transformer/LoRA 对产品设计有什么影响？
- 解释思维链 CoT 为什么能提升推理？
- 你用过哪些大模型？对比它们的优劣？
- （腾讯混元等技术向）RLHF/PPO/DPO 区别、Transformer 注意力为何除以 √d_k
- **（agent 定位题）你的 agent 行为跑偏了，怎么定位？**（强答案：症状映射到 Context Pyramid——重复=State 污染 / 忽略已知事实=Knowledge 检索失败 / 人设崩=Identity / 跑题=Task 没说清；弱答案："再调调 prompt"）
- **答题要点**：别只背名词，一定要落到"产品层面怎么处理"。

> **高判别力机制探针（专治"答一堆名词显得很懂"，追问到机制级）**：
> - "你怎么**决定要写哪些 eval**？"（真 PM：先读 trace 做 error analysis 找 failure mode 再写；假的：测准确率/写测试用例）
> - "一个 agent 失败了，你怎么归因？"（看能否归到 Three Gulfs：看不懂数据 / prompt 没说清 / 泛化不了，而非盲目换模型）
> - "faithfulness 和 correctness 有什么区别？"（区分"有依据" vs "对"——多数人混为一谈）
> - "用 LLM 当裁判（LLM-as-judge）有哪些坑？"（position / verbosity / self-preference bias + 要先写 guideline）
> - "怎么评一个 **agent**（不是单次回答）的好坏？"（trajectory：路由决策 / 工具调用 / 收敛步数，非只看最终输出）
> - "fine-tune vs RAG 的机制区别？"（正确切分=**教行为/风格 vs 注入知识**，不是"同类问题 vs 通用问题"）

### 板块 2：Product Sense（AI 方向）
- 设计一个 AI 功能帮 [抖音创作者/Instagram creator/某平台] 提升 X
- 应该做独立 AI 产品还是集成进现有产品？（standalone vs integrate）
- 如果你的 AI 功能在 scale 时开始生成有害输出，怎么办？
- 为大模型设计一个 App Store / 插件平台，核心价值主张 + 生态健康怎么保障？
- **答题框架**：Clarify → Goal → 用户细分 → 痛点 → 多方案对比 → 推荐 + 理由 → 风险/Fallback。Meta 强调"It depends 不够用，要明确推荐"。

### 板块 3：Metrics / 数据
- 如何衡量一个 LLM 驱动功能的成功？（注意：别只说 DAU，要说 task completion rate、CSAT、留存、hallucination rate）
- A/B 测试 AI 功能很 tricky，你怎么设计实验？（概率性输出的对照难点）
- AI 功能使用量下跌 15%，走一遍你的诊断思路
- 如果埋点失效了你怎么衡量成功？
- **"How would you measure GPT-5?"**（Anthropic/OpenAI 出现过的开放指标题——别只给 benchmark，要谈真实价值、安全、失败率）
- 怎么评一个 **agent** 的好坏（trajectory：路由/工具调用/收敛步数），而不只是最终输出对不对？

### 板块 4：技术权衡 Case（字节经典真题）
> 现状 GPT-4：每次 ¥0.3、延迟 2 秒。目标：成本 ≤¥0.1、延迟 ≤0.8 秒。如何补差距？
- 解法框架：模型蒸馏 / 缓存复用 / 模板降级兜底 / 小模型路由 / 成本-体验权衡
- 考点：能否在成本、延迟、质量三角间做产品决策

### 板块 5：商业化 / 战略
- 设计两条变现路径（按量付费 vs 订阅），估算营收 + 识别风险
- 你觉得 [字节/阿里/Google] 在大模型上的优势和不足？
- 未来 1-2 年 AI 技术（多模态/Agent/推理）和产品形态会如何发展？
- 看好哪个 Agent 赛道？出海 AIGC 有什么建议？

### 板块 6：Behavioral / Mission
- 为什么选 [这家公司]？具体到他们的 AI 路线（别泛泛而谈）
- 讲一次你做出大胆而困难的决策
- 讲一次你推动跨职能（AI 研发/工程）协作，遇到什么冲突，怎么解决
- （Anthropic/OpenAI）你对 AI safety 怎么看？speed 与 safety 怎么平衡？
- 讲一个你印象深刻的 AI 输出或错误，你学到了什么？
- **"讲一个当时觉得对、现在会换做法的 AI 产品决策。"**（AI 专属版反思题，考迭代认知）
- **"讲一次你在 model accuracy 和 serving latency 之间做取舍。"**（AI 专属 behavioral，要有真实场景+数字）
- **（Anthropic culture 轮，被称最难）"有没有一个你很尊重、但在价值观上不认同的人？"**（哲学深挖，没有标准答案，考思考深度与真诚）

---

## 三、各公司针对性提示

| 公司 | 必做准备 |
|------|---------|
| Anthropic | 读 Responsible Scaling Policy；准备"治理一个模型"视角；**有独立 AI safety/ethics 轮 + culture 轮（哲学题，被称最难）**；Safety 是文化不是合规；用 Claude 自己模拟练习 |
| OpenAI | 准备"为什么/你不喜欢 OpenAI 什么"；**有"AI Product Sense"专轮：强制分开 model layer vs application layer、不被提示也要主动谈 safety、优先级用真实数字估算（别 high/med/low）、口述一个 eval harness + fallback + 成文 ship rule**；概率性系统 + guardrails 思维 |
| Google | BUS 框架；估算题；AI search 战略判断；技术深度高 |
| Meta | 用户细分要清晰；Binary tradeoff 给明确推荐；练 "stress test AI 输出" |
| xAI | **Product Lead 是另一个物种：30 min post-training 技术 case，如"两周内带 8–10 个标注员把模型 precision 提 20%"，追问数据利用/团队问责指标/风险缓解/cold-start；竞争味重、不告诉你成功标准** |
| 字节 | 必须用过豆包/Coze；准备模型选型故事；5Why 追问不慌；项目带数据 |
| 腾讯混元 | 大模型八股（RLHF/Transformer/LoRA）|
| Cursor/DeepSeek | 自己是 Agent 重度用户；能讲 Agent Loop/MCP/eval；最好能 Vibe Coding |
| v0/Bolt/Figma/Sierra 等 | **有现场建造轮（vibe-coding）**：必须提前刷工具 reps（见下节）|

---

## 四、新型考核形式（2025-2026，超出传统问答，知道它存在并准备）

传统"你会怎么做"的口头题正在被**让你当场做出来**的形式取代（效度更高、更难伪装）。备考要点：这些轮次没有框架能救，只能靠真刷过 reps。

1. **Vibe-coding 现场建造轮**：45 分钟内用任意 AI 工具（v0/Bolt/Cursor/Lovable/Replit）现场搭一个可运行原型，再 demo + 讲 scope 取舍。已确认：v0、Bolt、Figma、Perplexity（部分）；Aakash 还点名 Google India、Netflix、Stripe。真实 prompt 如"Build a prototype of an X 0→1 product"、"Design Google Maps for the Blind（带原型）"。**考的是 agency（卡住会不会 pivot）和 scope 判断**。原话："没开过这些工具，这轮你必挂，没有框架救得了你。"→ 备考：提前用这些工具搭过 3–5 个小原型。
2. **2 小时 plan→build→review（Sierra 范式，"AI-native 面试"）**：(1) Plan 候选人主导 ideation；(2) Build 2 小时独立用 AI 工具做出来、允许中途改 scope；(3) Review demo + 讨论数据模型/可扩展性/上生产路径。Sierra 原文是工程岗，但这套"建造型 onsite"正外溢到 PM-adjacent，作为**未来形态**预警。
3. **post-training 运营 case（xAI Product Lead）**：带外包标注团队提模型指标的项目案（见上节 xAI 行），比常规 AI PM 深一层。
4. **预期你 ship 过一个 AI 产品**：很多轮默认你自己上线过一个小 AI 产品（RAG app / classifier / agentic tool），好让你能讲真实的 design decision、eval set、failure mode，而不是只背框架。

> 注：trace-review（现场读 agent trace 找失败）目前多见于 eval 工具厂商博客而非公开面经，作为"很可能出现"的趋势准备；本 skill 的模拟面试已用"实际案例题"覆盖这种考法（给真实材料让你现场诊断）。

---

## 五、过来人经验教训（高频踩坑）

1. **技术别只会背名词**——一追问 RAG 原理或幻觉的产品处理就露馅
2. **项目经历要有数字**——"CSAT +10 点 / 人工转接率 -20%" 胜过"提升了满意度"
3. **准备 2-3 个完整 Case**——覆盖需求拆解 + 技术选型 + 上线评估 + 迭代优化
4. **了解目标公司 AI 产品线**——面字节必用豆包，面 Anthropic 要懂 Claude/MCP
5. **不要快速推翻自己判断**——被质疑时先坚持逻辑，再承认多视角
6. **反向提问要有质量**——"这个 AI 项目在哪个阶段？技术团队和 PM 配比？"
7. **展示你是 AI 重度用户**——能具体说出你每天怎么用 AI、踩过哪些坑

---

## 六、临阵磨枪 48 小时清单

- [ ] 把简历每段经历用"问题→方案→技术选型→量化结果"重述一遍
- [ ] 准备 1 个完整的 AI 产品设计 Case（端到端）
- [ ] 复习幻觉缓解、RAG vs Fine-tuning、eval 设计三道必考题
- [ ] **能讲清"怎么决定写哪些 eval"（error analysis → failure mode → 针对性 eval），不是"测准确率"**
- [ ] 研究目标公司最近的模型/产品发布，准备"为什么是你们"
- [ ] 想清楚 speed vs safety、成本 vs 体验 两个经典权衡的你的观点
- [ ] **若目标公司有现场建造轮：提前用 v0/Bolt/Cursor 等刷过 3–5 个小原型（reps 不能临时抱佛脚）**
- [ ] **准备一个"我自己 ship 过的 AI 产品"故事：design decision + eval set + 踩过的 failure mode**
- [ ] 准备 3 个高质量反向提问
