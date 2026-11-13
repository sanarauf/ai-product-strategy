# CoinDesk Terminal AI (Autonomous Market & Regulatory Intelligence Engine)

> We are building an autonomous research oracle for institutional crypto analysts that converts breaking news and proprietary CoinDesk Index feeds into instantaneous, audit-ready market risk briefs.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** CoinDesk Terminal AI (Autonomous Market & Regulatory Intelligence Engine)
- **AI Value Archetype:** Oracle
- **Vulnerability Scores:** _(add: Moat 3/5 · Data 4/5 · Platform 2/5)_
- **Top Risk:** High exposure to foundational AI model providers native retrieval capabilities, forcing us to rely heavily on our proprietary CoinDesk Indices and exclusive newsroom speed to avoid being commoditized as a generic financial research wrapper.
- **Confidence:** M
- **Prototype:** First attempt: https://coindesk-terminal-ai-prototype-rvqf8ppf.v0.build/
- **Kill Criteria:** If post-launch pilot feedback reveals that institutional analysts reject the AI briefs due to unresolvable hallucinations in regulatory interpretation, OR if time-to-insight exceeds 5 seconds during high-volatility market events, we kill the standalone terminal product and pivot …

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 12/20
- **Weakest Loop:** Correction Loop (Score: 2/5) & Network Loop (Score: 2/5)
- **Top Encroachment Threat:** OpenAI (GPT-4o / Deep Research Agents)
- **Encroachment Defense:** Build an automated RLHF/RAG correction pipeline: whenever institutional compliance officers edit or correct a synthesized regulatory rule interpretation, automatically convert that edit into a verified high-confidence ground-truth anchor for all future retrieval queries across the platform.
- **Vendor Portability:** Partial

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 95.2%
- **Gross Margin (AI-adjusted):** 80.0%
- **Pricing Model:** hybrid (seat base + outcome/usage tier)
- **Pricing Today → Tomorrow:** $2,500/month flat enterprise user seat (Legacy CoinDesk Data/Terminal SaaS) → $4,500/month base platform fee (includes 5 seats & 250 briefs) + $15/additional risk brief
- **Total AI COGS / unit:** $165.00
- **Cascading Strategy:** Triage: Claude 3.5 Haiku / Llama 3 70B (Fast, low-cost extraction); frontier: GPT-4o / Claude 3.5 Sonnet (Complex reasoning & compliance synthesis); ratio 65% Triage / 35% Frontier
- **Net Margin Shift:** -15.2%
- **Break-even at:**

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:**
- **Golden Dataset:** 
- **Confidence UX:** Combination: Tiered confidence framework with an explicit evidence panel, real-time driver breakdown, and a mandatory human-in-the-loop escalation trigger for high-ambiguity financial claims.
- **HITL Architecture:** ### Trigger: When does a human enter the loop? * Model confidence score drops below **60%**. * Financial safety / hallucination rubric flag fires on a customer-facing risk brief.…
- **Failure Mode Coverage:**

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | | ----- | ----- | ----- | ----- | ----- | | **Recursive Learning** | User corrections on generated risk briefs & regulatory summaries | Retrained retrieval weights & verifi…
- **Governance Posture:** AI features in the CoinDesk Terminal AI product line, automated research brief synthesis, real-time news summarization, CoinDesk Index (CDI) data correlation, and regulatory risk analysis.…
- **Autonomy Boundaries:** Synthesizing breaking market risk briefs, auto. Generating citation-backed index analysis and regulatory summaries, auto. Executing institutional trades, modifying ledger balances, or transmitting unreviewed automated communications directl…
- **Escalation Triggers:** (1) Model confidence < 50% on quantitative index metrics or regulatory interpretation. (2) Customer input flagged for adversarial prompt injection, jailbreak attempts, or data poisoning.…
- **Audit Cadence:** Weekly, Automated evaluation against the 150+ row ground-truth Golden Dataset. Monthly, Human-in-the-Loop (HITL) review of all flagged low-confidence queries and client-reported edge-case corrections.…
- **Shadow AI Audit (user-side):**
- **Agent Boundaries:** *Not shipping agents this version.*
- **Regulatory Exposure:** EU AI Act, SEC/FINRA record-keeping (Rule 17a-4), SOC 2. Risk tier: High-risk AI system (financial services / institutional risk assessment).…

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** **The case:**
- **Ask:** ## M1 Baseline vs. Now
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
