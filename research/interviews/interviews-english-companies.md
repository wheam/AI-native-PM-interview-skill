---
captured: 2026-06-05
topic: AI 公司 PM 面试真题与流程（英文渠道：Anthropic/OpenAI/Google/Meta）
sources: IGotAnOffer, Exponent, StellarPeers, Glassdoor, Reddit, Blind
researcher: subagent (Sonnet 4.6)
---

# AI 公司 PM 面试真题与流程（英文渠道）

## 一、Anthropic

### 面试流程（4–8 周）
Recruiter Screen(30m) → Hiring Manager(45-60m，深挖项目+AI safety) → **Final Loop 同一天 5 轮**：
1. Case Presentation/Deep Dive（部分团队提前发 case prompt）
2. User Centricity
3. XFN Leadership
4. Engineering Partnership
5. **Culture & Values / AI Safety Judgment**（权重异常高）

### 5 大考察维度
Mission & Values Alignment｜AI Safety Judgment（安全是本能非合规层）｜Product Sense｜Technical Fluency（把安全需求转化为系统架构，考快速系统设计）｜PM Judgment

### 真实题
- "What draws you specifically to Anthropic?"（要具体、产品导向）
- "Describe a time when your personal values were at odds with business needs."
- "How do you approach GenAI safety in consumer products?"（区分开放 chatbot vs 任务型；stateful vs stateless；PII）
- "If you were PM for Claude's API, what policies would you set around misuse?"
- "What are LLM hallucinations and how would you mitigate them in a deployed product?"（三类：Intrinsic/Extrinsic/Fabrication；LLM-as-a-judge）
- "How would you design an evaluation framework for a new Claude feature?"
- "Walk me through how you'd decide if a new Claude capability is ready to ship."
- 行为题：bold and difficult decision / 冲突解决 / RICE 优先级
> 必读 Anthropic Responsible Scaling Policy。核心：不是管理路线图，而是"治理一个模型"。

## 二、OpenAI

### 面试流程（4–8 周，共 8 轮）
Recruiter(30-45m) → Hiring Manager(45m behavioral) → Product Design(30m) → Product Metrics(30m) → Skills Assessment(case/技术) → Onsite 4-6 轮（Behavioral+Product Sense+Technical+Analytical）

### 考察维度
Probabilistic thinking（为概率性 AI 设计）｜Safety-first product sense｜Mission alignment｜Technical depth（系统设计+ML 基础）

### 真实题
- "Why OpenAI？" / "What don't you like about OpenAI?"（批判性思维）
- "Can you provide an example of a trade-off between UX and technical feasibility?"
- Product Design："Design a solution to communicate with pets using AI." / "What goal would you set for an AI-only social network?" / "What industry could benefit most from enterprise ChatGPT?"
- Metrics："How would you measure success for OpenAI? What if instrumentation went down?"
- Technical："What's your criteria in selecting the right AI model for a product feature?" / "How do you balance model accuracy against latency?"
- AI/ML："Explain a Transformer to a non-technical executive." / "supervised vs unsupervised, when each?"
> 核心：理解 AI 产品本质是概率性系统，不能用传统线性用户旅程，要设计 guardrails。

## 三、Google

### 面试流程
Resume Screen(~90% 止步) → Recruiter(30m) → PM Phone Screen 1-2 轮 → Onsite 4-6 轮
**Onsite 6 维度**：Product Vision/Design｜Analytical/Metrics｜Strategy｜Leadership & Judgment｜Technical Depth｜Googleyness
**评分四维**：RRK / GCA / Leadership / Googleyness

### 真实题
- Design："How would you improve Google Maps?" / "Design a product for elderly users new to smartphones."
- Analytical："Google Search ad revenue dropped 10%. Investigate." / "Estimate Gmail users sending >10 emails/day."
- Strategy："Should Google build a standalone AI coding assistant vs Copilot?" / "Biggest threat to Google Search over next 5 years?"
- Technical："Design a real-time collaborative document editing system." / "YouTube recommendation system design."
- AI："How would you build a responsible GenAI feature for Search?" / "How would you evaluate a Gemini-powered feature?"
> 框架 BUS（Business objective→User problems→Solutions）。技术深度高于 Meta。

## 四、Meta

### 面试流程
Recruiter(20m) → Round1（2 轮：Product Sense + Analytical）→ Round2（3 轮：Product Sense 更难 + Analytical 深挖 + Leadership & Drive）
**Central Products 部门额外**：Product Sense with AI + Product Architecture
45 分钟节奏：5m warmup → 35m 核心+follow-up → 5m 你提问

### 考察维度
Product Sense（用户细分→痛点→方案）｜Analytical Thinking（指标定义/下跌诊断/A-B）｜Leadership & Drive｜Product Sense with AI（CP 部门）

### 真实题
- Product Sense："Design a sports product for Meta." / "Newsfeed PM: 'People You May Know' widget vs ad unit?"（Binary Tradeoff）
- AI："Design an AI feature for Instagram to help creators grow." / "Risks of GenAI for Messenger auto-replies at scale?" / "How would you stress test an AI feature before launch—what breaks at scale?"
- Architecture："Design the API for a social graph system." / "Content moderation system design."
- Analytical："Instagram Stories DAU dropped 10%. Investigate." / "North Star metric for WhatsApp Business?"
> 核心：User segmentation 是 Product Sense 核心；"It depends" 不够用，要明确推荐+理由。

## 五、跨公司对比

| 维度 | Anthropic | OpenAI | Google | Meta |
|---|---|---|---|---|
| 核心差异 | 治理模型=产品 | 概率性 AI 设计 | 经典产品严谨 | 用户细分+执行速度 |
| AI 专项轮 | ✅全程嵌入Safety | ✅AI/ML知识轮 | ⚠️部分角色 | ✅CP部门专轮 |
| Technical | 高(evals/LLM架构) | 高(系统+ML) | 高(工程深度) | 中(API设计) |
| Culture权重 | 极高(Safety=文化) | 高(Mission) | 中(Googleyness) | 中(L&D轮) |
| 轮数 | 5-6 | 8 | 4-6 | 5 |

## 六、AI PM 高频题总清单
**Product Sense(AI)**：GenAI safety in consumer products / Design AI feature for X / standalone vs integrate / harmful outputs at scale 怎么办
**Metrics**：measure success for LLM feature / A-B test AI feature / AI 使用量下跌诊断
**Technical**：hallucinations 缓解 / fine-tuning vs RAG 选型 / precision vs recall / eval framework 设计
**Behavioral/Mission**：Why this company / shipped 后有意外后果 / speed vs safety 平衡
