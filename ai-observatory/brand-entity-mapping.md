# ENTITY LABELS: FORM INPUT → QWIKI INPUT

These labels map each form input field to its corresponding QWIKI variable or prompt placeholder. This mapping enables the automated and structured generation of QWIKIs from the completed brand questionnaire.

| Form Field Prompt (#/Section)                                        | ENTITY LABEL               | QWIKI Placeholder / Use                                                            | Notes                                                                            |
| -------------------------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| \[system] Provider name (e.g., OpenAI, Google)                       | `provider`                 | \$Provider                                                                         | Required for LLM audit context, sourcing, and comparison                         |
| \[system] LLM model/version (e.g., GPT-4o, Gemini 1.5, Claude 3)     | `llm_model`                | \$LLMModel                                                                         | For repeatability, source context, and benchmarking                              |
| \[system] Date of audit                                              | `audit_date`               | \$AuditDate                                                                        | For recency and trend context                                                    |
| 1.1: What is your official brand name?                               | `brand_name`               | \$BrandName                                                                        | Used throughout for brand description, comparisons, and sentiment.               |
| 1.2: What is your primary business description?                      | `business_description`     | \$BrandDescription                                                                 | Used in Brand Overview and summary responses.                                    |
| 1.3: What is your primary industry / market category?                | `industry`                 | \$IndustryCategory, \$industry, \$category, \$sector                               | Populates \[industry], \[sector], and comparison contexts.                       |
| 1.4: What is your brand’s overall reputation & perception?           | `reputation_perception`    | \$BrandReputation                                                                  | Used for "general perception," "sentiment," and user reputation cues.            |
| 1.5: What was your brand’s founding date?                            | `founding_date`            | \$BrandFounded, \$FoundedDate                                                      | Used in brand history and authority.                                             |
| 1.6: What are your key awards & recognitions?                        | `awards`                   | \$BrandAwards, \$Awards                                                            | Used in "awards, recognitions, certifications" context.                          |
| 1.7: What is the size of your company?                               | `company_size`             | \$CompanySize                                                                      | For credibility, scale, and company context.                                     |
| 1.8: Where is your company headquartered?                            | `headquarters_location`    | \$HeadquartersLocation                                                             | For local/market/authority questions and regional relevance.                     |
| 1.9: What is your brand mission?                                     | `brand_mission`            | \$BrandMission                                                                     | Used in authority, trust, and positioning.                                       |
| 1.10: What is your brand vision?                                     | `brand_vision`             | \$BrandVision                                                                      | Used for long-term, aspiration, leadership context.                              |
| 1.11: What is the official website and other key online properties?  | `official_website`         | \$OfficialWebsites, \$OfficialWebsite                                              | Used for sources, references, and QWIKI answer sourcing.                         |
| 1.12: What are your key social profiles?                             | `social_profiles`          | \$SocialProfiles                                                                   | Key for up-to-date answers, authority, and online presence.                      |
| 2.1: What is your focus offering name?                               | `product_name`             | \$ProductName                                                                      | Used for all product/service-specific queries.                                   |
| 2.2: What is the general product/service type?                       | `product_type`             | \$ProductType                                                                      | Used for type, comparison, and market fit.                                       |
| 2.3: What are your key offerings/features?                           | `product_features`         | \$ProductFeatures                                                                  | Maps to features/comparison/USP queries.                                         |
| 2.4: What is the typical pricing structure?                          | `product_pricing`          | \$ProductPricing, \$Pricing                                                        | Used in pricing, comparison, and update queries.                                 |
| 2.5: Are there any known limitations or drawbacks?                   | `product_limitations`      | \$ProductLimitations                                                               | Used in "limitations," "drawbacks," and objection handling.                      |
| 2.6: How frequently is this product/service updated or improved?     | `product_update_frequency` | \$ProductUpdateFrequency                                                           | Used for AI recency/freshness and feature questions.                             |
| 3.1: What are your primary target audience(s)?                       | `target_audience`          | \$TargetAudience                                                                   | Used for suitability, fit, and persona-based scenarios.                          |
| 3.2: What core problems does your offering solve?                    | `problems_solved`          | \$CoreProblemsSolved, \$ProblemsSolved, \$Benefit, \$DesiredOutcome                | Used in "problem solving," "benefit," and "value" contexts.                      |
| 3.3: Are there specific use cases or scenarios?                      | `use_cases`                | \$UseCases, \$UseCase, \$Scenario                                                  | Populates "specific use case," scenario-based reasoning, and value proof points. |
| 4.1: Who are your top 2–3 direct competitors for this offering?      | `competitors`              | \$CompetitorName                                                                   | Used for all comparison and benchmarking questions.                              |
| 4.2: What are their comparable product/service names?                | `competitor_products`      | \$CompetitorProductName                                                            | Used in comparison, competitive positioning, and alternatives.                   |
| 4.3: What are your key differentiators from competitors?             | `differentiators`          | \$KeyDifferentiators, \$Differentiators, \$UniqueSellingPoints                     | Used for "why choose us," "USP," and competitive analysis.                       |
| 5.1: What are the key review platforms for your brand or offering?   | `review_platforms`         | \$ReviewPlatforms, \$ReviewSources                                                 | Used for Trust & Reviews category, answer citations, and reputation monitoring.  |
| 5.2: Where do you publish official news or updates?                  | `news_channel`             | \$NewsSources, \$NewsChannel, \$OfficialNews                                       | For "recent announcements," product update sourcing, and recency questions.      |
| 5.3: What are your main thought leadership or educational resources? | `thought_leadership`       | \$ThoughtLeadershipResources, \$ThoughtLeadership, \$EducationalResources, \$Topic | For authoritative resources, industry context, and contribution mapping.         |

---

## Example JSON Mapping

```json
{
  "provider": "OpenAI",
  "llm_model": "GPT-4o",
  "audit_date": "2025-06-01",
  "brand_name": "ACME Inc.",
  "business_description": "Leading provider of B2B SaaS tools.",
  "industry": "Enterprise Software",
  "reputation_perception": "Widely known for reliability and innovation.",
  "founding_date": "2005",
  "awards": "Forbes Cloud 100, 2023; Gartner Magic Quadrant Leader, 2022",
  "company_size": "200 employees",
  "headquarters_location": "London, UK",
  "brand_mission": "Empower businesses with seamless automation.",
  "brand_vision": "To become the global standard in business productivity.",
  "official_website": "https://acme.com",
  "social_profiles": {
    "linkedin": "https://linkedin.com/company/acme",
    "twitter": "https://twitter.com/acme",
    "facebook": "https://facebook.com/acme"
  },
  "product_name": "ACME Cloud Suite",
  "product_type": "Business Automation Platform",
  "product_features": "Unified dashboard, AI-powered analytics, automated workflows",
  "product_pricing": "Three tiers: Basic, Pro, Enterprise. Ranges from $99 to $999/month.",
  "product_limitations": "Requires internet connection, steep learning curve for new users.",
  "product_update_frequency": "Major update every 6 months",
  "target_audience": "Mid-size and large enterprises in the US and EU.",
  "problems_solved": "Streamlines business operations and enhances data-driven decision-making.",
  "use_cases": "Cross-departmental reporting, remote team coordination, compliance audits.",
  "competitors": ["MegaCloud", "SoftSuite", "DataPro"],
  "competitor_products": ["MegaCloud Platform", "SoftSuite Pro", "DataPro Analytics"],
  "differentiators": "Seamless integration, customisable modules, industry-best uptime.",
  "review_platforms": ["G2", "Trustpilot", "Capterra"],
  "news_channel": "https://acme.com/newsroom",
  "thought_leadership": ["https://acme.com/resources", "https://acme.com/whitepapers"]
}
```

---

## QWIKI Variable Mapping Table

| ENTITY LABEL               | Used In QWIKI As                                                                      |
| -------------------------- | ------------------------------------------------------------------------------------- |
| provider                   | \$Provider                                                                            |
| llm\_model                 | \$LLMModel                                                                            |
| audit\_date                | \$AuditDate                                                                           |
| brand\_name                | \$BrandName                                                                           |
| business\_description      | \$BrandDescription                                                                    |
| industry                   | \$IndustryCategory / \$industry / \$category                                          |
| reputation\_perception     | \$BrandReputation                                                                     |
| founding\_date             | \$BrandFounded / \$FoundedDate                                                        |
| awards                     | \$BrandAwards / \$Awards                                                              |
| company\_size              | \$CompanySize                                                                         |
| headquarters\_location     | \$HeadquartersLocation                                                                |
| brand\_mission             | \$BrandMission                                                                        |
| brand\_vision              | \$BrandVision                                                                         |
| official\_website          | \$OfficialWebsites / \$OfficialWebsite                                                |
| social\_profiles           | \$SocialProfiles                                                                      |
| product\_name              | \$ProductName                                                                         |
| product\_type              | \$ProductType                                                                         |
| product\_features          | \$ProductFeatures                                                                     |
| product\_pricing           | \$ProductPricing / \$Pricing                                                          |
| product\_limitations       | \$ProductLimitations                                                                  |
| product\_update\_frequency | \$ProductUpdateFrequency                                                              |
| target\_audience           | \$TargetAudience                                                                      |
| problems\_solved           | \$CoreProblemsSolved / \$ProblemsSolved / \$Benefit / \$DesiredOutcome                |
| use\_cases                 | \$UseCases / \$UseCase / \$Scenario                                                   |
| competitors                | \$CompetitorName                                                                      |
| competitor\_products       | \$CompetitorProductName                                                               |
| differentiators            | \$KeyDifferentiators / \$Differentiators / \$UniqueSellingPoints                      |
| review\_platforms          | \$ReviewPlatforms / \$ReviewSources                                                   |
| news\_channel              | \$NewsSources / \$NewsChannel / \$OfficialNews                                        |
| thought\_leadership        | \$ThoughtLeadershipResources / \$ThoughtLeadership / \$EducationalResources / \$Topic |

---

**Instructions:**

* For each form response, extract the value and assign to the matching ENTITY LABEL.
* When generating a QWIKI question or answer, substitute placeholders (e.g., `$BrandName`) with values from the mapped entity.
* All variables in QWIKI output are referenced by the ENTITY LABEL mapping above.
* Always include the provider, model, and audit date metadata for context and repeatability.

---
