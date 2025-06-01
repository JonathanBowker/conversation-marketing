# NimbusPay – Full AI Observatory Report (Example)

---

## ![NimbusPay Logo](https://nimbuspay.com/logo.svg)

## AI Observatory Report: Brand & Product Visibility

**Audit Date:** 2025-06-01
**Provider/LLM Model(s):** OpenAI GPT-4o, Google Gemini 1.5 Pro, Perplexity Llama-3

---

### 1. Introduction & Methodology

* **Overview:**
  Comprehensive audit of NimbusPay’s representation, factual accuracy, and competitive position in answer engines powered by LLMs.
* **Scope:**

  * Engines: ChatGPT (OpenAI GPT-4o), Google Gemini 1.5 Pro, Perplexity (Llama-3)
  * Coverage: Brand facts, product features, pricing, competitor landscape, trust signals
* **Process:**
  27 QWIKI-aligned queries, 3 engines, outputs mapped to internal schema for traceability.

---

### 2. Executive Summary

* **Overall AI Brand Health Score:** **B**
* **Headline Findings:**

  * Sentiment: Mostly positive, with some neutral/uncertain sentiment in competitor comparisons.
  * Most-cited brands: Stripe (22), NimbusPay (19), Revolut (15).
  * Official NimbusPay sources cited in 60% of responses.
  * Main risks: Pricing information outdated in Perplexity; Gemini sometimes describes Stripe as the default for “global payments API.”

---

### 3. Brand Visibility & Sentiment Analysis

| Brand     | Mentions | Positive | Neutral | Negative |
| --------- | -------- | -------- | ------- | -------- |
| NimbusPay | 19       | 14       | 5       | 0        |
| Stripe    | 22       | 16       | 6       | 0        |
| Revolut   | 15       | 10       | 4       | 1        |
| PayPal    | 8        | 4        | 4       | 0        |

* **Engine Coverage Table:**

| Engine     | NimbusPay Mentioned | Most-Common Competitor | % Official Source |
| ---------- | ------------------- | ---------------------- | ----------------- |
| GPT-4o     | 9                   | Stripe                 | 82%               |
| Gemini     | 5                   | Stripe                 | 45%               |
| Perplexity | 5                   | Revolut                | 52%               |

---

### 4. Fact Accuracy & Source Mapping

| Query Ref | Engine     | Cited Source    | Official/Unofficial | Accurate? | Flags                |
| --------- | ---------- | --------------- | ------------------- | --------- | -------------------- |
| 1.1       | GPT-4o     | nimbuspay.com   | Official            | Yes       |                      |
| 2.4       | Gemini     | trustpilot.com  | Third Party         | Partial   | Outdated pricing     |
| 2.6       | Perplexity | blog.stripe.com | Competitor          | No        | No NimbusPay mention |
| ...       | ...        | ...             | ...                 | ...       | ...                  |

* **Top Sources:**

  * Trustpilot, nimbuspay.com, fintechmagazine.com

---

### 5. Brand Narrative & Reputation

* **Mission:** “Making global payments simple for every business” – correctly cited in GPT-4o and Perplexity, omitted in Gemini.
* **Risks:**

  * Gemini frequently attributes features to Stripe unless prompted specifically about NimbusPay.
  * Some Perplexity answers show out-of-date fee structure.

---

### 6. Competitive Intelligence

| Brand     | Share (%) | Most-Cited Features                              |
| --------- | --------- | ------------------------------------------------ |
| NimbusPay | 42%       | Multi-currency API, 24/7 support, SMB onboarding |
| Stripe    | 35%       | Instant payouts, global reach, compliance        |
| Revolut   | 23%       | Prepaid cards, integrations                      |

---

### 7. Risks, Issues & Action List

* **Issues:**

  * Gemini lacks source citations in 55% of answers for NimbusPay.
  * Outdated product and pricing info in Perplexity.
* **Actions:**

  * Update NimbusPay website with latest pricing/features in schema.
  * Increase publishing to Trustpilot, G2, and news outlets.
  * Address competitor confusion with schema.org and FAQ optimization.

---

### 8. Appendix: Full Query Results

* **All JSON Outputs:**

  * (Example below)

```json
{
  "provider": "OpenAI",
  "llm_model": "GPT-4o",
  "audit_date": "2025-06-01",
  "section": "General Brand Information",
  "section_ref": "1",
  "query_ref": "1.1",
  "category": "Brand Category",
  "query": "What is your official brand name?",
  "ai_answer": "The official brand name is NimbusPay, a UK-based fintech provider focused on global digital payments for small and medium businesses.",
  "brands_mentioned": ["NimbusPay"],
  "sources_cited": ["https://nimbuspay.com/about"],
  "sentiment": "positive",
  "accuracy": "accurate",
  "summary": "NimbusPay is correctly identified by name and focus area in most major LLMs.",
  "flags": []
}
```

* **Screenshots:** (on request; sample omitted)

---

### 9. About CREWE AI & Methodology

Advanced Analytica's AI Observatory is an independent LLM visibility and brand safety audit system, combining automated QWIKI-style queries, leaderboard analytics, and schema recommendations for brand owners in the age of answer engines.

---
