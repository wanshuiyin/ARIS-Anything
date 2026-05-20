<p align="center">
  <img src="assets/aris_logo.svg" alt="ARIS — Auto Research in Sleep" width="640">
</p>

# ARIS-Anything

> *"研究"在中文里有两层意思：**科研** 是其中的窄义（学术研究），**研究** 是广义——投资研究 / 法律研究 / 产品研究 / 市场研究 / 自学 / 调查 / 工程复盘……所有"问 → 证 → 写"的结构化探究。*
>
> **ARIS-Anything** 把 ARIS 的方法论——跨模型对抗审查、skill-based workflow、持久化知识 wiki——从科研推广到任何形式的研究。

📖 **English version (default)**: [README.md](README.md)

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

## 🧭 同一个 loop，不同的封皮

| 领域 | 探究形态 | 最接近的 ARIS skill |
|---|---|---|
| 💰 **投资 / 尽调** | 股票研究、行业研究、并购尽调、竞品 landscape | `/research-lit`, `/peer-review`, `/research-wiki` |
| ⚖️ **法律研究** | 案例分析、合同审查、监管跟踪 | `/research-lit`, `/proof-checker`（论证有效性）, `/citation-audit` |
| 🏥 **医学文献综述** | 系统综述、疗法对比、剂量-反应 synthesis | `/research-lit`, `/idea-creator`, `/result-to-claim` |
| 📊 **市场 / 产品研究** | 用户研究、竞品分析、定位叙事 | `/idea-creator`, `/research-wiki`, `/paper-write` |
| 🎓 **自驱学习** | 长程学习计划、掌握度跟踪 | `/research-wiki`, `/interview-cheatsheet`, `/render-html` |
| 🔍 **调查 / 新闻** | 信源核实、叙事构建、claim 审计 | `/citation-audit`, `/paper-claim-audit`, `/kill-argument` |
| 🛠 **工程复盘** | 根因分析、事件时间线、行动项 | `/research-review`, `/proof-checker`（论证）, `/auto-review-loop` |
| 📚 **个人知识管理** | 桥接笔记、second-brain workflow | `/research-wiki`, `/render-html` |

[ARIS](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) 里 74+ 个 skill —— `/research-lit`, `/idea-creator`, `/proof-checker`, `/research-wiki`, `/peer-review`, `/citation-audit`, `/kill-argument` ... —— 都是为科研写的，但**结构动作大多可以推广**。这个仓库就是收集这些迁移方案的地方。

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
| [**Auto-claude-code-research-in-sleep**](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) | ARIS 主仓 —— 74+ 科研 skill，完整学术 workflow |
| [**ARIS-in-AI-Offer**](https://github.com/wanshuiyin/ARIS-in-AI-Offer) | 秋招 / AI campus-recruiting cheat sheet 合集，由 ARIS 生成 |
| [**Oh-My-ARIS**](https://github.com/wanshuiyin/Oh-My-ARIS) | 社区研究平台 |
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
