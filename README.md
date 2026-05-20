<p align="center">
  <img src="assets/aris_logo.svg" alt="ARIS — Auto Research in Sleep" width="640">
</p>

# ARIS-Anything

> *Research as **科研** (kēyán) covers academic science.
> Research as **研究** (yánjiū) covers everything else — investment, law, product, market, learning, investigation, journalism, engineering post-mortems, ...*
>
> **ARIS-Anything** explores how the ARIS methodology — cross-model adversarial review, skill-based workflows, persistent knowledge wikis — generalizes from academic research to any structured inquiry.

📖 **中文版 (Chinese version)**: [README_CN.md](README_CN.md)

---

## 🏆 Why this isn't vaporware

ARIS-Anything is an exploration, not a from-scratch venture. The methodology is **already battle-tested at scale**:

[![Stars](https://img.shields.io/github/stars/wanshuiyin/Auto-claude-code-research-in-sleep?style=flat&logo=github&logoColor=white&color=gold&label=Stars)](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/stargazers) · [![arXiv](https://img.shields.io/badge/arXiv-2605.03042-b31b1b?style=flat&logo=arxiv)](https://huggingface.co/papers/2605.03042) · [![HF Daily #1](https://img.shields.io/badge/HF%20Daily%20Papers-%231-yellow?style=flat)](https://huggingface.co/papers/2605.03042) · [![PaperWeekly](https://img.shields.io/badge/Featured%20on-PaperWeekly-red?style=flat)](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) · [![awesome-agent-skills](https://img.shields.io/badge/Featured%20in-awesome--agent--skills-blue?style=flat&logo=github)](https://github.com/VoltAgent/awesome-agent-skills) · [![Project of the Day](https://img.shields.io/badge/AI%20Digital%20Crew-Project%20of%20the%20Day-orange?style=flat)](https://aidigitalcrew.com)

- ⭐ **~10k GitHub stars** on the [main ARIS repo](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) — top-trending AI research agent
- 🥇 **HuggingFace Daily Papers #1** — [arXiv:2605.03042](https://huggingface.co/papers/2605.03042) top of the day
- 🏆 **AI Digital Crew · Project of the Day** (2026-03-14)
- 📰 **Featured on PaperWeekly** + [awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)
- 🛠 **74+ research skills** spanning idea exploration → experiments → papers → rebuttals → talks
- 🌐 **7+ platforms supported** — Claude Code · Codex CLI · Cursor · Trae · Antigravity · GitHub Copilot CLI · OpenClaw
- 🔧 **ARIS-Code standalone CLI** — multi-provider runtime, no Claude Code dependency required
- 📚 **First downstream sibling already shipped**: [**ARIS-in-AI-Offer**](https://github.com/wanshuiyin/ARIS-in-AI-Offer) — 23 bilingual interview cheat sheets, auto-generated end-to-end via the same workflow. Proof that ARIS's loop carries beyond science papers.

ARIS-Anything is the next reach: take the proven loop, point it at non-academic structured inquiry. Everything below is grounded in what already works — not a wishlist.

---

## 🌟 The Premise

[**ARIS — Auto Research in Sleep**](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) was built for academic research: find ideas → run experiments → write papers → handle rebuttals. But the underlying loop is general:

1. **Plan** the inquiry — structure the question, scope, deliverable
2. **Draft** the work — executor model produces the first version
3. **Review** adversarially — a different-family reviewer model finds flaws (Claude × GPT-5.5 xhigh × Gemini)
4. **Iterate** until convergence — fix → re-review → ship
5. **Persist** — write findings to a versioned wiki so future-you starts from the cumulative state, not zero

The Chinese wordplay matters: **科研 ⊂ 研究**. Academic research is one specific shape of inquiry; the broader 研究 covers any structured investigation where you have a question, evidence, and a deliverable. The same five-step loop carries over.

---

## 🚀 Incoming siblings

The "Anything" exploration runs in parallel with several domain-specific repos under early development. Each one re-uses the ARIS core loop with a domain-appropriate deliverable shape — same five-step inquiry, different cover sheet:

| Repo | Domain | Key idea |
|---|---|---|
| 🎬 **ARIS-Movie** | Long-form video generation | Persistent **movie wiki** as the durable narrative state → adversarial cross-model review on plot continuity / character arc / scene consistency → video generated conditioned on wiki state. Same loop as `/paper-writing` + `/research-wiki`, but the deliverable is a video instead of a paper. |
| 📐 **ARIS-PRD** | Product requirements | Auto-draft PRDs with cross-model adversarial review on user-story coverage, success metrics, edge-case completeness, and tradeoff explicitness. PM-as-executor + PM-as-reviewer (different model families) loop. |
| 🎨 **ARIS-Design** | Design (UX · brand · visual) | Cross-model adversarial critique on design briefs, mood boards, and iteration cycles. Persistent design-system wiki anchors choices to constraints; reviewer model challenges every decision against the brief. |
| 🏋️ **ARIS-Gym** | Skill benchmarking & training environments | Canonical task suites + standardized evaluation harness for measuring ARIS-skill performance. Think **OpenAI Gym for research agents** — drop in a skill (`/research-lit`, `/proof-checker`, `/paper-write`, ...), get reproducible scores across domain benchmarks (literature search · proof verification · paper drafting · rebuttal handling · ...), with cross-model adversarial scoring. The meta-layer that makes Movie / PRD / Design / Anything's other domains measurable instead of vibe-graded. |

These are **scheduled rather than promised** — code drops in this repo and the matching `wanshuiyin/ARIS-*` repos when ready. If one of these domains is your day job, [open an issue](https://github.com/wanshuiyin/ARIS-Anything/issues/new) — you can shape the API.

---

## 🧭 Where the loop applies

Same loop, different cover sheet:

| Domain | Inquiry shape | ARIS skill closest to it |
|---|---|---|
| 💰 **Investment / due diligence** | Equity / sector research, M&A diligence, competitive landscape | `/research-lit`, `/peer-review`, `/research-wiki` |
| ⚖️ **Legal research** | Case law analysis, contract review, regulatory tracking | `/research-lit`, `/proof-checker` (for argument validity), `/citation-audit` |
| 🏥 **Medical / clinical literature** | Systematic review, treatment comparison, dose-response synthesis | `/research-lit`, `/idea-creator`, `/result-to-claim` |
| 📊 **Market / product research** | User studies, competitive analysis, positioning narrative | `/idea-creator`, `/research-wiki`, `/paper-write` |
| 🎓 **Self-directed learning** | Long-horizon study plans, mastery tracking | `/research-wiki`, `/interview-cheatsheet`, `/render-html` |
| 🔍 **Investigation / journalism** | Source verification, narrative construction, claim auditing | `/citation-audit`, `/paper-claim-audit`, `/kill-argument` |
| 🛠 **Engineering post-mortems** | Root-cause analysis, incident timeline, action items | `/research-review`, `/proof-checker` (for argument), `/auto-review-loop` |
| 📚 **Personal knowledge management** | Bridging notes, second-brain workflows | `/research-wiki`, `/render-html` |

The 74+ skills in [ARIS](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) — `/research-lit`, `/idea-creator`, `/proof-checker`, `/research-wiki`, `/peer-review`, `/citation-audit`, `/kill-argument`, ... — were built for science, but **most of the structural moves generalize**. This repo is where we collect the adaptations.

---

## 🧱 Core invariants (preserved from main ARIS)

These do not change across domains:

- **Cross-model adversarial review** — executor and reviewer must come from different model families. No LLM ever judges its own output.
- **Reviewer independence** — only the artifact is passed to the reviewer, never the executor's summary or fix list. Fresh thread per round.
- **Persistent wiki** — accumulated findings live in a typed knowledge wiki, not in conversation context. Future runs start from the cumulative state.
- **Skill-based composition** — every workflow is a SKILL.md contract. Re-use, fork, and remix freely.

What changes per domain: the **deliverable shape** (a paper vs. an investment memo vs. a legal brief vs. a study plan), the **evidence sources**, and the **claim taxonomy**.

---

## 🌱 Status

🌿 **Early genesis** (2026-05). This repo is a placeholder for an exploration: which ARIS skills generalize, which need a re-skin, which need fresh design.

**If you have a domain in mind:**

1. Pick the closest existing ARIS skill from the table above
2. Try it on your domain — note what breaks, what fits
3. Open an [issue](https://github.com/wanshuiyin/ARIS-Anything/issues/new) with the friction points
4. We'll figure out together what the "Anything" version should look like

Early focus areas being prototyped:

- [ ] **Investment due diligence** — equity research with cross-model review of bull/bear claims
- [ ] **Legal case analysis** — argument-structure auditing via `/proof-checker` on legal logic
- [ ] **Self-directed learning** — re-using `/interview-cheatsheet` for arbitrary curricula
- [ ] **Personal post-mortem** — applying paper-review skills to incident reports

---

## 🔗 Related repos

| Repo | What |
|---|---|
| [**Auto-claude-code-research-in-sleep**](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) | ARIS main repo — 74+ research skills, the academic-research workflow |
| [**ARIS-in-AI-Offer**](https://github.com/wanshuiyin/ARIS-in-AI-Offer) | 秋招 / AI campus-recruiting cheat sheet collection (23 bilingual cheat sheets), generated via ARIS — proof the loop generalizes |
| **ARIS-Anything** *(this repo)* | Generalizing ARIS beyond 科研 → any structured 研究 |

---

## 💬 Community

Shared community with the [main ARIS repo](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) — same WeChat group covers methodology discussions, the AI-Offer cheat sheets, and this exploration:

<p align="center">
  <img src="assets/wechat_group.jpg" alt="WeChat Group QR Code (shared with ARIS main repo)" width="300">
</p>

---

## License

[MIT](LICENSE) — open, fork-friendly, remix-friendly. The methodology is the gift; the implementations should be everyone's.
