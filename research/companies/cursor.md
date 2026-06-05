---
company: Cursor (Anysphere)
captured: 2026-06-05
source: cursor.com/careers
roles_found: 7
researcher: subagent (Sonnet 4.6)
note: AI-native 公司，PM = 技术型 Builder，大量用 "Product Engineer" 称呼
---

# Cursor (Anysphere) — 产品岗位 JD 汇总

> AI-native 代码编辑器，使命"Automate coding"。估值 $293亿，ARR >$10亿，~300 人，人均 ARR ~$500万。文化：Flat / Talent-dense / Ship code / Truth-seeking。**没有 "Product Builder" 头衔，但大量用 "Product Engineer"**。

## 1. Product Manager（通用）⭐ PM 即 Builder
- **地点**：SF/NY（必须 in-person）
- **定位**："product-minded engineers 构建开发者工具。不是传统 PM 组织，没有 roadmap 委员会，每个项目都模糊。" PM 是**技术型 Builder，自己写代码部署**
- **职责**：自己构建功能第一版（用 AI coding 原型→推用户迭代→交工程 scale）；feature strategy；端到端 own 发布；客户/销售/Field Engineering 合作；优先处理"1000 paper cuts"信任问题；与 Data Science 做 instrumentation
- **要求**：**每天用 AI coding tools**（功能性使用）；有工程背景或深度 dev tools 经验，**能独立浏览 codebase**；infra/cloud/platform 产品经验（不看重窄消费产品）；**能 build 和 deploy 应用**；默认 ship 不 explore 数月
- **AI native**：用 AI 工具自己原型功能，而非写 PRD 等工程师实现

## 2. Product Manager, Agent Harness ⭐⭐
- **定位**："When an agent gets stuck, loops, or hallucinates, the harness is why—and how you fix it." **不是写 spec，而是读 agent traces、识别 failure pattern、设计 eval**
- **关键领域**：Agent 规划执行框架（任务分解/工具选择/failure recovery）；开发者观察控制（实时进度/guardrail/mid-task 重定向）；评估基准系统（任务完成率/错误恢复/幻觉频率）；**大规模 agent trace 分析**；扩展性 primitives（MCP/Marketplace）；"Auto"模型智能选择；多 agent 协调
- **要求**：构建或评估过 AI agents/LLM 应用/ML dev tools；深度技术能读代码分析 traces；强 eval 和 metrics 直觉（定义质量指标非活动指标）；研究邻近环境工作
- **加分**：RL 经验、agent framework 经验

## 3. Product Manager, Cloud Agents
- **定位**："进入 AI 软件开发第三纪元——开发者指挥 agent 舰队。**Cursor 内部 >33% PR 已由云端 VM 自主 agent 创建**"
- **关键领域**：任务交接 UX；agent 编排（sandboxing/并行/retry/错误恢复）；产出物 review 层（logs/截图/视频/live preview）；自托管企业部署；成功度量（完成率/time-to-value/cost-per-task）；cloud-to-local 交接
- **要求**：发布过 dev tools/infra/AI 应用；理解分布式系统能读 PR 架构图（**不要求写生产代码**）；强 developer intuition；重度用 AI coding tools；不依赖冗长 PRD

## 4. Software Engineer, Product（Product Engineer）⭐
- **定位**：构建面向用户的产品（编辑器本体）
- **样例项目**：为 AI 生成代码的 PR Review 发明新 UX；两周 sprint 从零建新方向（AI bug detection）；数百万用户上 A/B test 推进 agent 质量（sub-agents/memories/PR retrieval）
- **要求**：构建过优秀产品；**融合工程能力与对模型(models)和设计的品味(taste)**；不牺牲易用性做强大工具
- **AI native**："Taste for models" 是明确招聘标准

## 5. Software Engineer, Enterprise（Enterprise Product Engineer）
- 端到端构建企业级功能；创业精神；AI 转型前沿；工程卓越+模型/设计品味

## 6. Software Engineer, Growth（Product Engineer, Growth）
- Onboarding/Monetization/核心体验的系统与功能；创业精神；工程+模型/设计品味

## 7. Product Quality Engineer（Remote）
- **定位**："Own the feedback loop between users and product"
- **职责**：构建 **AI-native 全球首创 VoC 系统**；实时反馈闭环；**agentic bug 优先级**（人工 triage → 自动化 pipeline）；高级升级节点
- **要求**：深厚产品技术知识快速诊断 bug；强 debugging/reproduction；P0 判断力；高 ownership；**厌恶手工劳动有自动化思维**

---

## 🔑 Cursor 产品岗 AI-native 能力模型
- **AI 工具重度使用者**：每天用，有强烈好坏观点
- **自己动手 Build**：PM 自己原型，不等工程师；工程师自己做产品决策
- **工程+产品双栖**：能读代码/架构图，推理技术 tradeoff
- **Speed & Shipping**：默认 ship，two-week sprint 常态
- **Ambiguity Tolerance**：没现成 roadmap
- **Empirical/Data-Driven**：eval 数据/A/B/agent traces 驱动，非直觉或 spec
- **Taste for Models**：对模型能力有品味直觉

**明确不看重**：窄领域消费产品经验、传统 spec-writing PM 思维、依赖 roadmap 委员会/PRD
