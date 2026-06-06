# AI 产品经理面试 Skill —— 研究项目

> 目标：打造一个 AI native 产品经理面试 skill，覆盖各大 AI 公司（Anthropic/OpenAI/Google/DeepSeek/字节/MiniMax/智谱/Kimi/Meta/Cursor/Manus 等）招 PM / Product Builder 岗位的真实强度、考点、JD 要求。
> 维护者：Diana ｜ 所有者：wheam ｜ 创建：2026-06-05

## 项目结构

```
ai-pm-interview-skill/
├── README.md
├── research/
│   ├── xiaohongshu-bytedance-ai-pm-2nd-round.md   # 字节 AI 产品二面面经（种子素材）
│   ├── thought-leaders/                            # 业内大神方法论
│   │   └── ai-pm-thought-leaders.md                # Lenny/Krieger/Shreyas/a16z + Hamel/Eugene Yan/Aman Khan/Marily Nika 等 15 位
│   ├── interviews/                                 # 真实面试题与流程
│   │   ├── interviews-english-companies.md         # Anthropic/OpenAI/Google/Meta 面试真题
│   │   ├── interviews-china-companies.md           # 字节/腾讯/阿里/百度等中文面经
│   │   ├── interviews-2026-new-formats.md          # 新型考核形式：vibe-coding 建造轮/Sierra/xAI post-training case
│   │   └── designer-engineer-reference.md          # 设计师/工程师 JD 反哺 PM
│   └── companies/                                  # 各公司招聘 JD 抓取
│       ├── anthropic.md ... (11 家)
│       └── more-ai-native-companies.md             # Mistral/Perplexity/Cohere/Scale 等 8 家
```

## 进度

- [x] 项目初始化 + 字节面经存档
- [x] 抓取各公司招 PM/Product Builder 的 JD（19 家公司，~60 个岗位）
  - 前沿：Anthropic、OpenAI、Google DeepMind、Meta
  - 中国大模型：字节 Seed/豆包、DeepSeek、MiniMax、智谱、Kimi
  - AI-native 产品：Cursor、Manus、Mistral、Perplexity、Cohere、Scale、Character.AI、Hugging Face、Replit、xAI
- [x] 业内大神方法论（Lenny/Mike Krieger/Shreyas Doshi/a16z/Claire Vo/Aakash 等 9 位）
- [x] 真实面试题与流程（英文 4 家 + 中文 8 家 + 设计师/工程师反哺）
- [x] 汇总分析共性考点与能力模型 → `skill/references/ai-native-pm-competency-model.md`
- [x] 提炼成 `ai-pm-interview` skill → `skill/SKILL.md`

## ✅ Skill 已完成

`skill/` 目录即可安装的 Hermes skill，提供 4 大能力：
1. **能力模型 & 备考指南输出** — AI native PM 六大能力 + 各公司侧重 + 大神框架
2. **知识点测试** — 学完某领域（如模型评估）后出题自测 + 点评 + 学习建议
3. **简历筛选** — 给简历（PDF/MD），分析是否通过 + 评分 + 改进建议
4. **模拟面试** — 三种模式(A 快速问答 / B 实际案例 / C 完整三轮可存档续面) + 自评闭环 + 逐句回放，给通过判定 + 打分（2.0/2.5/3/3+/3.5/4.0），六步流程含 Bar-raiser 复评防捧杀

```
skill/
├── SKILL.md                                    # 主文件，4 大能力工作流
└── references/
    ├── ai-native-pm-competency-model.md        # 六大能力模型(含 eval how-to/Context Pyramid) + 各公司侧重 + 大神框架
    ├── interview-prep-guide.md                 # 面试流程 + 六板块高频真题 + 新型考核形式 + 经验教训
    ├── scoring-rubric.md                       # 6 档打分 + 六能力细则 + 六步打分流程(证据强制/Bar-raiser 复评)
    └── calibration-anchor-3.0.md               # 3.0 校准锚点样本(2.5/3.5 待补)
```

**安装**：把 `skill/` 内容放到 Hermes skills 目录（如 `~/.hermes/skills/career/ai-pm-interview/`）。
