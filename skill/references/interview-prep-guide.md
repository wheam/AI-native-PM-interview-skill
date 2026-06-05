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
- **答题要点**：别只背名词，一定要落到"产品层面怎么处理"。

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

---

## 三、各公司针对性提示

| 公司 | 必做准备 |
|------|---------|
| Anthropic | 读 Responsible Scaling Policy；准备"治理一个模型"视角；Safety 是文化不是合规；用 Claude 自己模拟练习 |
| OpenAI | 准备"为什么/你不喜欢 OpenAI 什么"；概率性系统 + guardrails 思维；准备 1-2 个 AI 设计题 |
| Google | BUS 框架；估算题；AI search 战略判断；技术深度高 |
| Meta | 用户细分要清晰；Binary tradeoff 给明确推荐；练 "stress test AI 输出" |
| 字节 | 必须用过豆包/Coze；准备模型选型故事；5Why 追问不慌；项目带数据 |
| 腾讯混元 | 大模型八股（RLHF/Transformer/LoRA）|
| Cursor/DeepSeek | 自己是 Agent 重度用户；能讲 Agent Loop/MCP/eval；最好能 Vibe Coding |

---

## 四、过来人经验教训（高频踩坑）

1. **技术别只会背名词**——一追问 RAG 原理或幻觉的产品处理就露馅
2. **项目经历要有数字**——"CSAT +10 点 / 人工转接率 -20%" 胜过"提升了满意度"
3. **准备 2-3 个完整 Case**——覆盖需求拆解 + 技术选型 + 上线评估 + 迭代优化
4. **了解目标公司 AI 产品线**——面字节必用豆包，面 Anthropic 要懂 Claude/MCP
5. **不要快速推翻自己判断**——被质疑时先坚持逻辑，再承认多视角
6. **反向提问要有质量**——"这个 AI 项目在哪个阶段？技术团队和 PM 配比？"
7. **展示你是 AI 重度用户**——能具体说出你每天怎么用 AI、踩过哪些坑

---

## 五、临阵磨枪 48 小时清单

- [ ] 把简历每段经历用"问题→方案→技术选型→量化结果"重述一遍
- [ ] 准备 1 个完整的 AI 产品设计 Case（端到端）
- [ ] 复习幻觉缓解、RAG vs Fine-tuning、eval 设计三道必考题
- [ ] 研究目标公司最近的模型/产品发布，准备"为什么是你们"
- [ ] 想清楚 speed vs safety、成本 vs 体验 两个经典权衡的你的观点
- [ ] 准备 3 个高质量反向提问
