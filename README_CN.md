<p align="center">
  <img src="assets/aris_logo.svg" alt="ARIS — Auto Research in Sleep" width="640">
</p>

# ARIS-Anything

> *"研究"在中文里有两层意思：**科研** 是其中的窄义（学术研究），**研究** 是广义——投资研究 / 法律研究 / 产品研究 / 市场研究 / 自学 / 调查 / 工程复盘……所有"问 → 证 → 写"的结构化探究。*
>
> **ARIS-Anything** 把 ARIS 的方法论——跨模型对抗审查、skill-based workflow、持久化知识 wiki——从科研推广到任何形式的研究。

📖 **English version (default)**: [README.md](README.md)

---

## 🏆 为什么这不是空中楼阁

ARIS-Anything 是一次推广，不是从 0 起跳。底层方法论**已经在大规模上验证过了**：

[![Stars](https://img.shields.io/github/stars/wanshuiyin/Auto-claude-code-research-in-sleep?style=flat&logo=github&logoColor=white&color=gold&label=Stars)](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/stargazers) · [![arXiv](https://img.shields.io/badge/arXiv-2605.03042-b31b1b?style=flat&logo=arxiv)](https://huggingface.co/papers/2605.03042) · [![HF Daily #1](https://img.shields.io/badge/HF%20Daily%20Papers-%231-yellow?style=flat)](https://huggingface.co/papers/2605.03042) · [![PaperWeekly](https://img.shields.io/badge/Featured%20on-PaperWeekly-red?style=flat)](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) · [![awesome-agent-skills](https://img.shields.io/badge/Featured%20in-awesome--agent--skills-blue?style=flat&logo=github)](https://github.com/VoltAgent/awesome-agent-skills) · [![Project of the Day](https://img.shields.io/badge/AI%20Digital%20Crew-Project%20of%20the%20Day-orange?style=flat)](https://aidigitalcrew.com)

- ⭐ **~10k GitHub stars**，[ARIS 主仓](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep)长期 top-trending AI research agent
- 🥇 **HuggingFace Daily Papers #1** —— [arXiv:2605.03042](https://huggingface.co/papers/2605.03042) 当日榜首
- 🏆 **AI Digital Crew · Project of the Day**（2026-03-14）
- 📰 **PaperWeekly 专题报道** + [awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) 收录
- 🛠 **75+ 个研究 skill** —— 从找 idea → 跑实验 → 写论文 → rebuttal → 做 talk 的全流程
- 🌐 **7+ 平台支持** —— Claude Code · Codex CLI · Cursor · Trae · Antigravity · GitHub Copilot CLI · OpenClaw
- 🔧 **ARIS-Code 独立 CLI** —— 多 provider runtime，不绑定 Claude Code
- 📚 **第一个 downstream 仓库已经发了两个 production artifact**：[**ARIS-in-AI-Offer**](https://github.com/wanshuiyin/ARIS-in-AI-Offer) 在同一套 `/render-html` workflow 上跑出两个产品 —— (1) 23 篇双语面试 cheat sheet（原始 deliverable），(2) [**ARIS-Homepage v1**](https://wanshuiyin.github.io/)（`/homepage-generator` skill：CV → fact-checked 单文件学术主页；DBLP/arXiv 硬审查 venue/年份/作者不一致与编造奖项）。两个完全不同的 deliverable、同一个 workflow —— 证明 ARIS 的 pattern 能跳出 science paper

ARIS-Anything 是下一步 —— 把已经跑通的 loop 推广到非学术的结构化探究。下面所有的内容都建立在已经 work 的基础上，**不是 wishlist**。

---

## 🌟 思路

[**ARIS — Auto Research in Sleep**](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) 原本是为学术科研设计的：找 idea → 跑实验 → 写论文 → 处理 rebuttal。但底层 loop 是通用的：

1. **Plan** —— 把问题、scope、deliverable 结构化
2. **Draft** —— executor 模型产出初稿
3. **Review** —— 不同家族的 reviewer 模型对抗审查（Claude × GPT-5.5 xhigh × Gemini）
4. **Iterate** —— 修复 → 重审，直到收敛
5. **Persist** —— 把结论写进持久 wiki，下次启动是累积态而不是从 0

中文的双关很关键：**科研 ⊂ 研究**。学术研究只是研究的一种形态，但凡有"问题 + 证据 + 产出"的结构化探究，这套五步 loop 都适用。

---

## 🚀 在路上的姊妹仓库

"Anything" 的探索同时并行几个 domain-specific 仓库，每个都复用同一个 ARIS 五步 loop，只是换了 deliverable 形态：

| 仓库 | 领域 | 核心 idea |
|---|---|---|
| 🎬 **ARIS-Movie** | 长视频生成 | 持久 **movie wiki** 当 narrative 状态 → 跨模型对抗审查 plot 连续性 / 人物弧线 / 场景一致性 → 视频条件 wiki state 生成。同一个 `/paper-writing` + `/research-wiki` loop，deliverable 从论文换成视频 |
| 📐 **ARIS-PRD** | 产品需求文档 | 自动起草 PRD，跨模型对抗审查 user story 覆盖度、成功指标、edge case 完备性、tradeoff 显式度。PM-as-executor + PM-as-reviewer（不同模型家族）loop |
| 🎨 **ARIS-Design** | 设计（UX · brand · 视觉） | 跨模型对抗式评审设计 brief、mood board、迭代周期。持久 design-system wiki 把每个决策锚到约束上；reviewer model 拿着 brief 挑战每一个设计选择 |
| 🏋️ **ARIS-Gym** | Skill 评测 + 训练环境 | 标准任务套件 + 统一评测 harness，给 ARIS skill 跑分。类比 **OpenAI Gym for research agents** —— 塞一个 skill (`/research-lit` / `/proof-checker` / `/paper-write` ...) 进去，跨多领域 benchmark（文献搜索 · 证明验证 · 论文起草 · rebuttal 等）出可复现分数，跨模型对抗式打分。这是让 Movie / PRD / Design / Anything 其他领域**可量化**而不是 vibe-graded 的 meta 层 |

**计划项不等于承诺** —— 等代码 ready 了会在这个仓库和对应的 `wanshuiyin/ARIS-*` 仓库发出来。如果这些领域是你的日常工作，[来 issue 讨论](https://github.com/wanshuiyin/ARIS-Anything/issues/new) —— 你可以参与定义 API。

---

## 🧭 同一个 loop，不同的封皮

| 领域 | 探究形态 | 最接近的 ARIS skill |
|---|---|---|
| 💰 **投资 / 尽调** | 股票研究、行业研究、并购尽调、竞品 landscape | `/research-lit`, `/peer-review`, `/research-wiki` |
| ⚖️ **法律研究** | 案例分析、合同审查、监管跟踪 | `/research-lit`, `/proof-checker`（论证有效性）, `/citation-audit` |
| 🏥 **医学文献综述** | 系统综述、疗法对比、剂量-反应 synthesis | `/research-lit`, `/idea-creator`, `/result-to-claim` |
| 📊 **市场 / 产品研究** | 用户研究、竞品分析、定位叙事 | `/idea-creator`, `/research-wiki`, `/paper-write` |
| 🎓 **自驱学习** | 长程学习计划、掌握度跟踪 | `/research-wiki`, `/interview-cheatsheet`, `/render-html` |
| 🌐 **学术主页 / 秋招个人 portfolio** ✅ 已发布 | CV → fact-checked 单文件主页（含论文 bib + 导师 + 时间 + 奖项），发布前拦截幻觉 | [`/homepage-generator`](https://github.com/wanshuiyin/ARIS-in-AI-Offer/blob/main/skills/homepage-generator/SKILL.md)（ARIS-Homepage v1，住在 AI-Offer 里）—— DBLP/arXiv 硬审查 |
| 🔍 **调查 / 新闻** | 信源核实、叙事构建、claim 审计 | `/citation-audit`, `/paper-claim-audit`, `/kill-argument` |
| 🛠 **工程复盘** | 根因分析、事件时间线、行动项 | `/research-review`, `/proof-checker`（论证）, `/auto-review-loop` |
| 📚 **个人知识管理** | 桥接笔记、second-brain workflow | `/research-wiki`, `/render-html` |

[ARIS](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) 里 75+ 个 skill —— `/research-lit`, `/idea-creator`, `/proof-checker`, `/research-wiki`, `/peer-review`, `/citation-audit`, `/kill-argument` ... —— 都是为科研写的，但**结构动作大多可以推广**。这个仓库就是收集这些迁移方案的地方。

---

## 🧱 核心不变量（从 ARIS 主仓承袭）

跨领域不变：

- **跨模型对抗审查** —— executor 和 reviewer 必须不同模型家族，绝不让 LLM 自己审自己
- **Reviewer 独立性** —— 给 reviewer 只传 artifact，不传 executor 的摘要 / fix list；每轮 fresh thread
- **持久 wiki** —— 累积发现写入有 schema 的知识 wiki，不靠 conversation context；下次启动是累积态
- **Skill-based 组合** —— 每个 workflow 都是 SKILL.md contract，可复用、可 fork、可 remix

跨领域改变的：**deliverable 形态**（论文 vs 投资 memo vs 法律意见书 vs 学习计划）、**证据来源**、**claim 分类法**。

---

## 🌱 状态

🌿 **早期 genesis**（2026-05）。这个仓库是个 placeholder：哪些 ARIS skill 能直接通用，哪些要 re-skin，哪些要重新设计——还在探索。

**如果你有具体领域想试试**：

1. 从上面的表里挑一个最接近的 ARIS skill
2. 用到你的领域上跑一遍——记录哪里不顺、哪里好用
3. 来 [issue](https://github.com/wanshuiyin/ARIS-Anything/issues/new) 里反馈摩擦点
4. 一起讨论 "Anything 版" 该长什么样

**早期 prototype 方向**：

- [ ] **投资尽调** —— 股票研究 + 对抗审查 bull/bear claim
- [ ] **法律案例分析** —— 用 `/proof-checker` 审法律论证结构
- [ ] **自驱学习** —— `/interview-cheatsheet` 推广到任意学习主题
- [ ] **个人复盘** —— 把 paper-review skill 用到 incident report

---

## 🔗 相关仓库

| 仓库 | 内容 |
|---|---|
| [**Auto-claude-code-research-in-sleep**](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) | ARIS 主仓 —— 75+ 科研 skill，完整学术 workflow |
| [**ARIS-in-AI-Offer**](https://github.com/wanshuiyin/ARIS-in-AI-Offer) | 秋招 / AI campus-recruiting cheat sheet（23 篇双语）+ [**ARIS-Homepage v1**](https://wanshuiyin.github.io/)（CV → fact-checked 单文件学术主页）—— loop 通用性的存在性证明 |
| **ARIS-Anything** *(本仓)* | 把 ARIS 从科研推广到任何研究 |

---

## 💬 社区

与 [ARIS 主仓](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) 共享一个社区 —— 同一个微信群讨论方法论、AI Offer cheat sheet、以及这里的探索：

<p align="center">
  <img src="assets/wechat_group.jpg" alt="WeChat 群二维码（与 ARIS 主仓共享）" width="300">
</p>

---

## License

[MIT](LICENSE) —— 开源、可 fork、可 remix。方法论是礼物，实现应该属于所有人。
