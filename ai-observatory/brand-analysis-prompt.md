# AI Visibility JSON Output Prompt

Process each user query to provide a comprehensive analysis of every question in a sequential manner, using **ONLY** the following categories:

- Brand Category
- Offering
- Problem Solving
- Trust & Social Proof
- How-To & Support
- Comparison & Alternatives
- Reputation & Authority
- Industry & Topical

---

## For each query, extract and present the following in JSON, matching the mapping from the questionnaire/form:

- **section**: The section heading/title as per the form.
- **section_ref**: The section reference number or code (e.g., "1", "2", "3").
- **query_ref**: The question reference number or ID (e.g., "1.2", "4.1").
- **category**: One of the above categories only.
- **query**: The original question from the user.
- **ai_answer**: A detailed, simulated answer in the style of top AI engines (ChatGPT, Perplexity, Copilot, Gemini).
- **brands_mentioned**:  
    - List **all brands or companies mentioned** in your answer.
    - This array is used as a leaderboard for indexing, frequency analysis, and competitive landscape mapping.
- **sources_cited**: Any URLs, sources, or publications cited.
- **sentiment**: The sentiment toward the primary brand ("positive", "neutral", "negative", or "mixed").
- **accuracy**: "accurate", "partially accurate", "inaccurate", or "unknown".
- **summary**: A 1–2 sentence summary of your answer.
- **flags**: List any flags such as ["missing brand mention", "no sources cited", "potential bias", "outdated information"].

---

## Output Format

- Respond in valid JSON only, with **all fields present, matching the form/questionnaire mapping**.
- Do **NOT** include any extra commentary or markdown.

---

## Example

**Input:**  
Who are the main competitors for Salesforce in cloud CRM?

**Ideal JSON Output:**
```json
{
  "section": "Competitive Landscape",
  "section_ref": "4",
  "query_ref": "4.1",
  "category": "Comparison & Alternatives",
  "query": "Who are the main competitors for Salesforce in cloud CRM?",
  "ai_answer": "[Simulated, detailed answer listing competitors and comparison points]",
  "brands_mentioned": ["Salesforce", "Microsoft", "Oracle", "HubSpot", "Zoho"],
  "sources_cited": ["https://www.g2.com/categories/crm", "https://www.gartner.com/reviews/crm"],
  "sentiment": "neutral",
  "accuracy": "accurate",
  "summary": "Salesforce faces competition from Microsoft Dynamics 365, Oracle CRM, HubSpot, and Zoho, each with their own strengths in cloud CRM.",
  "flags": []
}
````

---

## Notes

* Always list every brand or company referenced, no matter how minor, in the `"brands_mentioned"` array. This enables leaderboard/frequency analysis.
* Each output JSON object **must always include**: section, section\_ref, query\_ref, category, query, ai\_answer, brands\_mentioned, sources\_cited, sentiment, accuracy, summary, and flags.
* This enables direct mapping between user input, internal entity models, and QWIKI outputs.
* Map each user question to the most accurate category using the categories above.
* Each answer must robustly handle brand mentions, sources, sentiment, potential bias, and flag missing or questionable data.
* Never omit required fields, even if empty.




