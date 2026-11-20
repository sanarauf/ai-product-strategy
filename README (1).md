# My AI Product Strategy

> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS your strategy — version-controlled, board-ready, portable.

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

- **Product:** CoinDesk Terminal AI (Autonomous Market & Regulatory Intelligence Engine). An oracle for institutional crypto analysts and compliance teams that turns breaking CoinDesk news and proprietary CoinDesk Indices (CDI) data into audit-ready, citation-backed risk briefs in under a minute.
- **AI Value Archetype:** Oracle
- **Vulnerability Scores:** Moat 3/5 · Data 4/5 · Platform 2/5
- **Top Risk:** Foundation-model providers' native retrieval (e.g., OpenAI Deep Research) commoditizing us into a generic financial research wrapper. Our defense is CDI data, newsroom speed, and compliance-grade guarantees.
- **Confidence:** M
- **Prototype:** [coindesk-terminal-ai.vercel.app](https://coindesk-terminal-ai.vercel.app) (built in v0)
- **Kill Criteria:** If pilot analysts reject briefs due to unresolvable regulatory hallucinations, or time-to-insight exceeds one minute during high-volatility events, kill the standalone terminal and pivot to a headless API data-enrichment layer (e.g., Bloomberg/Refinitiv plug-ins).

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 12/20 (Correction 2 · Preference 3 · Domain Context 5 · Network 2)
- **Weakest Loop:** Correction and Network (both 2/5). Fix: convert verified compliance-officer edits into ground-truth retrieval anchors.
- **Competitive Position:** Axes are *proprietary data access* (public → exclusive) × *workflow depth* (ad-hoc search → embedded compliance workflow). CoinDesk sits high on data (exclusive CDI and newsroom pre-feeds) and mid on workflow. OpenAI/Perplexity are low-data and shallow-workflow but have free distribution. Messari is high on crypto data and deep in analyst workflow (already active). Bloomberg is deep in TradFi workflow and 6–12 months from crypto AI synthesis. The goal is to move up the workflow axis.
- **Encroachment Defense:** Lock exclusive CDI API rights and reposition from "news summarizer" to an Audit-Ready Regulatory Oracle, with verified citation logs, compliance guarantees, and newsroom pre-feed speed that public crawlers can't reach. Up to 60% of value (generic news/sentiment queries) is at risk within 3–6 months.
- **Vendor Portability:** Partial. Today we rely on a single vendor (OpenAI SDK, hardcoded routing). The 48-hour plan moves us to a provider-agnostic adapter (LiteLLM), dynamic routing, and provider-independent evals.

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 95.2% (legacy flat-seat SaaS)
- **Gross Margin (AI-adjusted):** 80.0% blended (81.6% on base tier); $165/user/month AI COGS
- **Pricing Model:** Hybrid. $4,500/month platform base (5 seats + 250 briefs) plus $15 per additional risk brief, replacing the $2,500/seat flat fee. Unit of work: audit-ready risk brief.
- **Cascading Strategy:** 65% Triage (Claude Haiku / Llama 3 70B) for headlines, sentiment, and index lookups; 35% Frontier (GPT-4o / Claude Sonnet) for cross-referencing multi-document SEC text against CDI anomalies. If inference costs triple, shift to 80/20.
- **Break-even at:** ~6 months payback on the $250K ask. The 12 pilot accounts at base tier generate $3,675 gross profit per account per month.

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** 92% accuracy (alert <88%), <1% hallucination rate (auto-rollback at >2%), ≤0.5%/week drift, and 100% of claims cited. Briefs are delivered in under a minute.
- **Golden Dataset:** 20 rows, 6 adversarial (target: 150 rows for v1)
- **Confidence UX:** Three tiers. High (>90%) shows the full brief with lineage badges and export. Uncertain (50–90%) shows hedged copy and a driver scorecard, and export is locked until the analyst reviews. Not confident (<50%) blocks generation and routes to an analyst. Admins can tune the confidence gates by fund policy.
- **HITL Architecture:** A human enters when confidence is <60%, a safety/hallucination flag fires, or a filing has high legal ambiguity. Reviewers are a senior crypto research analyst / compliance PM on weekdays and a senior CSM after hours. Corrections feed the Golden Dataset, and 5+ corrections on one query in a week trigger a retrieval/prompt revision.
- **Failure Mode Coverage:** Covered: fake regulatory claims, prompt injection / key extraction, out-of-scope trade execution, jailbreak trade orders, data poisoning, and price-target advice. Known gaps: non-English regulatory text, flash-crash multi-token correlation, and conflicting breaking-news claims.

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

- **Compounding System:** Three loops. Recursive learning: user corrections become retrieval weights and Golden Dataset rows. Cross-domain transfer: CDI volatility and macro news feed cross-asset sentiment models. Network intelligence: anonymized query clusters produce systemic-risk alerts. The network loop is currently siloed per fund; the fix is a zero-knowledge aggregated telemetry pipeline.
- **Governance Posture:** Read-only oracle. Briefs and cited index/regulatory summaries generate automatically. Five escalation triggers (low confidence, injection, contradictory sources, >2% hallucination, client request). Audits run weekly (automated evals), monthly (HITL review), and quarterly (security/legal/CTO sign-off).
- **Shadow AI Status:** 6 tools found, 6 triaged (3 build · 2 partner · 1 ignore). ~$900/month adjacent spend; the dominant signal is a workflow gap.
- **Agent Boundaries:** No agents ship in this version. Executing trades, modifying ledgers, or sending unreviewed communications to regulators or clients is never automatic.
- **Regulatory Exposure:** EU AI Act high-risk system (financial services), SEC/FINRA Rule 17a-4 record-keeping, SOC 2. Controls: output-lineage logging, no training on client PII or portfolio data, immutable citation audit trails, DPIA on file.

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
