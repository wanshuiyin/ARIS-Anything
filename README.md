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

## 🌟 The Premise

[**ARIS — Auto Research in Sleep**](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) was built for academic research: find ideas → run experiments → write papers → handle rebuttals. But the underlying loop is general:

1. **Plan** the inquiry — structure the question, scope, deliverable
2. **Draft** the work — executor model produces the first version
3. **Review** adversarially — a different-family reviewer model finds flaws (Claude × GPT-5.5 xhigh × Gemini)
4. **Iterate** until convergence — fix → re-review → ship
5. **Persist** — write findings to a versioned wiki so future-you starts from the cumulative state, not zero

The Chinese wordplay matters: **科研 ⊂ 研究**. Academic research is one specific shape of inquiry; the broader 研究 covers any structured investigation where you have a question, evidence, and a deliverable. The same five-step loop carries over.

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
| [**ARIS-in-AI-Offer**](https://github.com/wanshuiyin/ARIS-in-AI-Offer) | 秋招 / AI campus-recruiting cheat sheet collection, generated via ARIS |
| [**Oh-My-ARIS**](https://github.com/wanshuiyin/Oh-My-ARIS) | Community research platform |
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
