# AI Native 产品经理面试 Skill

一个面向 **AI native 产品经理 / Product Builder** 岗位的面试与备考 skill：基于 19 家 AI 公司真实 JD、多渠道面试真题、15 位业内方法论提炼，提供能力模型、知识自测、简历筛选、模拟面试打分四大能力。

## 四大能力

1. **能力模型 & 备考指南** — AI native PM 六大能力（模型 Sense / Eval / Product Sense / Builder / 数据商业化 / 跨职能·Safety）+ 各公司侧重 + 业内方法论框架。
2. **知识点测试** — 选定领域（模型评估 / RAG / Agent 等）出递进题自测，逐题点评 + 掌握度评估 + 学习建议。
3. **简历筛选** — 给简历（PDF/MD），按六大能力评估是否通过 + 分数档 + 逐条优势短板 + 改进建议。
4. **模拟面试** — 三种模式（A 快速问答 / B 实际案例 / C 完整三轮可存档续面），单题闭卷追问 + 挑战式追问 + 自评闭环 + 逐句回放，给通过判定与打分（2.0–4.0）。打分含证据强制、Bar-raiser 复评等防捧杀机制。

## 安装与使用

把 `skill/` 目录内容放到你的 skills 目录（Hermes 示例：`~/.hermes/skills/career/ai-pm-interview/`），随后用自然语言触发，例如：

- "给我 AI PM 能力模型 / 怎么准备面试"
- "测测我对模型评估的理解"
- "看看这份简历能不能过 AI PM 筛选"
- "模拟面试一次"

> skill 与具体模型解耦，在 Claude / Qwen 等模型上均可运行（打分严格度与流程纪律的执行效果依赖所用模型的能力）。

## 目录结构

```
skill/                                     # 可安装的 skill 本体
├── SKILL.md                               # 主文件，4 大能力工作流
└── references/                            # 按需加载的参考
    ├── ai-native-pm-competency-model.md   # 六大能力模型 + 各公司侧重 + 方法论
    ├── interview-prep-guide.md            # 面试流程 + 高频真题 + 新型考核形式
    ├── scoring-rubric.md                  # 6 档打分 + 六维细则 + 六步打分流程
    └── calibration-anchor-3.0.md          # 3.0 校准锚点样本

research/                                  # 支撑素材（研究参考，非定论）
├── companies/                             # 19 家 AI 公司招聘 JD
├── interviews/                            # 多渠道面试真题与流程（含若干个人面经，仅供参考）
└── thought-leaders/                       # 15 位业内方法论汇编
```

## 研究依据

能力模型与评分标准提炼自三类素材的交叉验证：

- **19 家 AI 公司 JD** — Anthropic / OpenAI / Google / Meta / 字节 Seed·豆包 / DeepSeek / MiniMax / 智谱 / Kimi / Cursor / Manus / Mistral / Perplexity / Cohere / Scale / Character.AI / Hugging Face / Replit / xAI
- **多渠道面试真题与流程** — 海外 4 家 + 中文多家 + 2025–2026 新型考核形式（vibe-coding 建造轮、post-training case 等）
- **15 位业内方法论** — Lenny / Mike Krieger / Shreyas Doshi / a16z / Claire Vo / Aakash Gupta / Hamel Husain / Eugene Yan / Chip Huyen / Aman Khan / Marily Nika / Miqdad Jaffer 等

> `research/` 下的个人面经（如小红书帖）是**单一来源参考，不代表权威结论**；能力模型一律以多公司 JD + 业内方法论的交叉验证为准。

---

维护者：Diana ｜ 所有者：wheam
