# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Single-vendor reliance on OpenAI API (GPT-4o/o3) for core synthesis and retrieval reasoning. | H | Swap API endpoint configuration to Anthropic Claude 3.5 Sonnet / AWS Bedrock fallbacks via environment flag. |
| **Abstraction** | Direct OpenAI SDK integration embedded across prompt pipelines without a unified model adapter layer. | H | Refactor model calls into a provider-agnostic LLM interface (e.g., LiteLLM or Vercel AI SDK wrappers). |
| **Routing** | Static model routing; all institutional research queries are hardcoded to hit OpenAI's frontier endpoints. | M | Implement dynamic model routing (e.g., OpenRouter / custom gateway) based on latency, price, and model availability. |
| **Eval** | Model evaluations and accuracy scoring tied to OpenAI-specific prompt structures and JSON schema outputs. | M | Standardize evaluation benchmark datasets using open-source eval harnesses independent of underlying provider APIs. |

---

## Portability Score
Partial

---

## If OpenAI doubles pricing tomorrow:
Reroute standard news synthesis and basic watchlist queries to open-source or lower-cost models (e.g., Llama 3 / DeepSeek via AWS Bedrock), reserving premium frontier models (Claude 3.5 Sonnet / GPT-4o) strictly for complex, multi-jurisdictional compliance and index anomaly analysis to protect gross margins.

---

## If OpenAI ships a competing product:
We double down on what base models cannot replicate: exclusive, real-time access to sub-second **CoinDesk Indices (CDI)** benchmark data, proprietary newsroom pre-feed alerts, and audit-ready regulatory compliance guarantees with full citation chains. Base models provide generic summaries; our value is tied directly to CoinDesk's proprietary data engine and enterprise workflow lock-in.