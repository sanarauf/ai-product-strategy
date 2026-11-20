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
- **Vulnerability Scores:** Moat 3/5 · Data 4/5 · Platform 2/5
- **Top Risk:** High exposure to foundational AI model providers native retrieval capabilities, forcing us to rely heavily on our proprietary CoinDesk Indices and exclusive newsroom speed to avoid being commoditized as a generic financial research wrapper.
- **Confidence:** M
- **Prototype:** [coindesk-terminal-ai.vercel.app](https://coindesk-terminal-ai.vercel.app) (built in v0)
- **Kill Criteria:** If post-launch pilot feedback reveals that institutional analysts reject the AI briefs due to unresolvable hallucinations in regulatory interpretation, OR if time-to-insight exceeds targets during high-volatility market events, we kill the standalone terminal product and pivot.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 12/20 (Correction 2/5 · Preference 3/5 · Domain Context 5/5 · Network 2/5)
- **Weakest Loop:** Correction Loop (Score: 2/5) & Network Loop (Score: 2/5)
- **Top Encroachment Threat:** OpenAI (GPT-4o / Deep Research Agents)
- **Encroachment Defense:** Build an automated correction pipeline: whenever institutional compliance officers edit or correct a synthesized regulatory rule interpretation, automatically convert that edit into a verified output.
- **Vendor Portability:** Partial. Today we rely on a single vendor (OpenAI SDK, hardcoded routing). The 48-hour plan moves us to a provider-agnostic adapter (LiteLLM), dynamic routing, and provider-independent evals.

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 95.2% (legacy flat-seat SaaS)
- **Gross Margin (AI-adjusted):** 80.0% blended (81.6% on base tier); $165/user/month AI COGS
- **Pricing Model:** Hybrid. $4,500/month platform base (5 seats + 250 briefs) plus $15 per additional risk brief, replacing the $2,500/seat flat fee. Unit of work: audit-ready risk brief.
- **Cascading Strategy:** Triage: Claude 3.5 Haiku / Llama 3 70B (Fast, low-cost extraction); frontier: GPT-4o / Claude 3.5 Sonnet (Complex reasoning & compliance synthesis); ratio 65% Triage / 35% Frontier
- **Break-even at:** ~6 months payback on the $250K ask. The 12 pilot accounts at base tier generate $3,675 gross profit per account per month.

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** 92% accuracy (alert <88%), <1% hallucination rate (auto-rollback at >2%), ≤0.5%/week drift, and 100% of claims cited. Briefs are delivered in under a minute.
- **Golden Dataset:** 20 rows, 6 adversarial (target: 150 rows for v1)
- **Confidence UX:** Combination: Tiered confidence framework with an explicit evidence panel, real-time driver breakdown, and a mandatory human-in-the-loop escalation trigger for high-ambiguity financial claims.
- **HITL Architecture:** A human enters when confidence is <60%, a safety/hallucination flag fires, or a filing has high legal ambiguity. Reviewers are a senior crypto research analyst / compliance PM on weekdays and a senior CSM after hours. Corrections feed the Golden Dataset, and 5+ corrections on one query in a week trigger a retrieval/prompt revision.
- **Failure Mode Coverage:** Covered: fake regulatory claims, prompt injection / key extraction, out-of-scope trade execution, jailbreak trade orders, data poisoning, and price-target advice. Known gaps: non-English regulatory text, flash-crash multi-token correlation, and conflicting breaking-news claims.

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** Three feedback loops, all active. **Recursive Learning:** user corrections on briefs and regulatory summaries update retrieval weights and become Golden Dataset candidates. **Cross-Domain Transfer:** CoinDesk Indices (CDI) volatility streams and macro news feed cross-asset sentiment models (e.g., L1 gas fees → DeFi liquidations). **Network Intelligence:** anonymized query clusters surface systemic-risk alerts (e.g., spikes in SEC-related searches). Broken loop: Network Intelligence is siloed per fund by confidentiality rules. Fix: an aggregated, zero-knowledge telemetry pipeline that shows cross-firm trends without exposing any fund's positions or strategies.
- **Governance Posture:** Read-only research tool. The policy covers brief generation, news summarization, CDI data correlation, and regulatory risk analysis in Terminal AI; internal editorial tools and corporate dashboards are excluded. Tenant-isolated data, with no cross-contamination of client portfolios.
- **Autonomy Boundaries:** Auto: market risk briefs, cited index analysis, and regulatory summaries. Never auto: executing trades, changing ledger balances, or sending unreviewed communications to regulators or clients.
- **Escalation Triggers:** (1) Confidence <50% on index metrics or regulatory interpretation. (2) Input flagged for prompt injection, jailbreak, or data poisoning. (3) Contradictory primary sources (e.g., SEC filing vs. breaking news). (4) Hallucination rate >2% in evals. (5) Client requests human analyst verification.
- **Audit Cadence:** Weekly: automated evals against the 150+ row Golden Dataset. Monthly: human review of flagged low-confidence queries and client-reported corrections. Quarterly: full policy review with security, legal, and CTO sign-off.
- **Shadow AI Audit (user-side):** 6 workarounds found, all triaged: 3 build · 2 partner · 1 ignore. ~$900/mo adjacent spend; dominant signal is a workflow gap. **Build:** IC memo generator (replaces pasting into Claude), inline citation verifier (replaces Perplexity checks), portfolio VaR calculator (replaces Claude Code scripts). **Partner:** Telegram/Slack alert integration, charting/LP deck export. **Ignore + monitor:** APAC translation.
- **Agent Boundaries:** *Not shipping agents this version.*
- **Regulatory Exposure:** EU AI Act (high-risk AI system: financial services / institutional risk assessment), SEC/FINRA Rule 17a-4 record-keeping, SOC 2. Controls: output-lineage logging · no training on client PII or fund portfolio data · immutable audit trails for citation chains · DPIA and compliance documentation on file.

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):** 0–3 months. CDI and newsroom RAG ingestion (<1.5s), tiered confidence UX with citation panel, 65/35 model router, 150-row Golden Dataset and weekly evals, Rule 17a-4 WORM logging and injection guardrails, 12-account concierge pilot.
- **Horizon 2 (Next):** 3–9 months. Editorial-gated compliance correction queue, async HITL escalation for <60% confidence briefs, hybrid usage billing, multi-provider failover layer, EU AI Act conformity assessment.
- **Horizon 3 (Bet):** 9–18 months. Cross-firm anonymized regulatory benchmark, autonomous regulatory-impact agent for portfolio exposure, fine-tuned CoinDesk crypto-regulatory small language model (target: 60% lower inference COGS).
- **Board Narrative:** We are turning CoinDesk's exclusive newsroom speed and proprietary index data into a regulatory and market intelligence engine that gives institutional crypto analysts verified, citation-backed risk briefs in under a minute during high-volatility events.
- **Key Metric:** ≥80% pilot analyst acceptance of risk briefs delivered in under a minute (H1 go/no-go). The ask is $250K plus 3.5 FTE over 3 months.

→ Details: [`06-the-pitch/`](06-the-pitch/)
