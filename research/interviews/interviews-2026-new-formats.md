---
captured: 2026-06-06
topic: AI PM 面试新型考核形式与新增真题（2024-2026，超出传统问答）
sources: Aakash Gupta newsletter, Sierra blog, Exponent, InterviewQuery, IGotAnOffer, DeepLearning.AI
researcher: Opus 4.8 (第二批 sub-agent 调研)
note: 本文件是 skill/references/interview-prep-guide.md「第四节 新型考核形式」的溯源底稿
---

# AI PM 面试新型考核形式与新增真题（2024-2026）

> 收录原则：只记**超出已有题库**（幻觉/RAG/微调树、字节成本延迟、Meta 用户细分、常规"衡量 X 成功"）的净增量。

## 1. Vibe-coding 现场建造轮（最大的新增形式）
- **形式**：45 分钟内用任意 AI 工具（Cursor / Bolt / Lovable / v0 / Replit / Base44）现场搭出某 feature 的可运行原型，再 demo + 讲 scope 取舍。有的内嵌在 30–60 min 产品设计 case，有的是 homework 交「1-pager + 原型链接」。
- **出处**：v0、Bolt、Figma、Perplexity（部分）已确认；Aakash Gupta 另点名 Google India、Netflix、Stripe。
- **真实 prompt 例**："Design Google Maps for the Blind"、"How would you prototype a Facebook Dating app"、"Design a Netflix product to support Partner Studios"、"Build a prototype of an X 0→1 product"。
- **考点**：agency（卡住会不会 pivot）+ scope 判断，不是嘴上框架。原话："If you've never opened these tools, you will fail this round. No framework saves you."
- **来源**：https://www.news.aakashg.com/p/vibe-coding-interview ｜ https://www.news.aakashg.com/p/ai-pm-interview-guide-2026

## 2. Sierra「AI-native onsite」：2 小时 plan→build→review
- **形式**：(1) Plan——候选人主导 ideation，面试官只问澄清；(2) Build——2 小时独立用任意 AI 工具把 idea 做出来，允许中途改 scope；(3) Review——demo + 讨论 product flows、数据模型/抽象/可扩展性、上生产路径。
- **注意**：Sierra 原文明写是**工程岗**，但它是"2 小时建造型 onsite"范式标杆，正外溢到 PM-adjacent。评估维度（agency / judgment / 取舍）对 AI PM 适用，作为**未来形态**收录。
- **来源**：https://sierra.ai/blog/the-ai-native-interview

## 3. xAI Product Lead：post-training 技术 case（另一个物种）
- **形式**：30 min 技术 case（常 20 min 提前结束）：**"两周内把模型 precision 提升 20%，你有 8–10 个外包标注员，怎么做？"** 追问数据利用、团队问责指标、风险缓解、regularization、cold-start。HM 轮还问 autocomplete 预测如何用底层数据。
- **本质**：human-data / post-training 运营型 PM，带外包团队做模型改进，比常规 AI PM 深一层。候选人反馈"更像深度 ML/post-training 面，竞争味重、没人告诉你成功标准"。
- **来源**：https://www.tryexponent.com/experiences/x-ai-product-manager-interview-e01111

## 4. OpenAI「AI Product Sense」专轮 + 写 eval 成核心技能
- **形式**：必考轮，要求把 **model layer 与 application layer 显式分开**谈；不被提示就要主动谈 safety；优先级用**真实数字估算**而非 high/med/low；会让你**口述一个 eval harness + fallback path + 一条成文的"何时上 AI 版 vs 确定性版本"的 ship rule**。
- **关键引用**：Kevin Weil（OpenAI CPO）："Writing evals is going to become a core skill for product managers."
- **来源**：https://www.news.aakashg.com/p/ai-pm-interview-guide-2026 ｜ https://www.news.aakashg.com/p/ai-evals

## 5. Anthropic：独立 safety 轮 + culture 轮（哲学深挖）
- **形式**：有**专门的 AI safety/ethics 轮**（OpenAI 则把 safety 揉进每一轮）。culture 轮被拿 offer 者称最难，问 **"你尊重但在价值观上不认同谁？"** 这类哲学题。指标题如 "How would you measure GPT-5?" / "怎么评估 Netflix 砸 $400M 拍一部剧"。
- **来源**：https://www.interviewquery.com/interview-guides/anthropic-product-manager ｜ https://www.news.aakashg.com/p/ai-pm-interview-guide-2026

## 6. 预期：已上线过一个 AI 产品
- 很多轮默认候选人**自己 ship 过一个小 AI 产品**（RAG app / classifier / agentic tool），好让你能讲真实 design decision、eval set、failure mode，而非只背框架。AI 素养判定 = 能否讲清 eval harness + 模型错时 fallback + 成文 ship rule。
- **来源**：https://igotanoffer.com/en/advice/ai-product-manager-interview

## 7. 重构后的 behavioral（AI 专属版）
- "Walk me through an AI product decision that seemed right but you'd approach differently now."
- "Describe a time you chose between **model accuracy and serving latency**."
- **来源**：https://www.news.aakashg.com/p/ai-pm-interview-guide-2026

---

## ⚠️ 诚实更正（别误收）
- **Perplexity** 经核实目前仍是**传统问答 loop**（约 7 场对话，无 take-home / 原型轮），不要把它列进"建造轮已确认"。
- **现场读 agent trace / 标注 traces** 没找到公开可引的真实原题（多来自 eval 工具厂商博客，非面经）。作为"很可能出现"的趋势准备；本 skill 的模拟面试已用**实际案例模式**覆盖这种考法。
