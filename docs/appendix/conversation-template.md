# Conversation Flow Template

Use this template to map out the structure, tone, logic, and purpose of any conversational journey — whether for a chatbot, voice assistant, in-app prompt, or live agent handoff.

---

## 1. Conversation Overview

| Field                 | Description                                      |
|-----------------------|--------------------------------------------------|
| **Flow Name**         | What is this flow called?                        |
| **Owner**             | Who's responsible for maintaining it?            |
| **Primary Goal**      | What outcome should this flow achieve?           |
| **Secondary Goals**   | What else should it support or uncover?          |
| **Trigger Point**     | When or where does this flow start?              |
| **Audience Segment**  | Who is this for? (Persona, behaviour, intent)    |

---

## 2. Entry Message

> **What does the first message say?**  
> Tip: Make it clear, engaging, and purpose-driven.

```

Hi there 👋 Need help choosing the right plan? Let’s figure it out together.

```

---

## 3. Key Decision Branches

List the main paths a user can take. Use natural language options, not technical flow names.

| User Input / Choice         | Bot/Brand Response                     | Next Step                                  |
|-----------------------------|----------------------------------------|---------------------------------------------|
| "I want to compare plans"   | “Great! Do you prefer monthly or annual?” | Show plan comparison or ask next question   |
| "I have a billing issue"    | “Sorry to hear that! Let’s fix it.”    | Escalate to support or guide to solution    |
| No response after 10 sec    | “Still there? I can help if you need.” | Offer help, exit, or pause conversation     |

---

## 4. Tone & Voice Guidelines

Define how the brand should sound in this flow.

| Tone Attribute    | Example Phrase or Behaviour                     |
|-------------------|--------------------------------------------------|
| Friendly          | “Awesome, let’s get started!”                    |
| Reassuring        | “No worries — I can walk you through it.”       |
| Direct            | “There are 2 main options. Want the summary?”    |
| Brand-specific phrases | “Let’s LEGO this!” or “Bank on it with Monzo” |

---

## 5. Fallbacks & Escalation

| Scenario                            | Fallback Copy / Next Action              |
|-------------------------------------|------------------------------------------|
| Unknown user input                  | “Hmm, I didn’t catch that. Can you rephrase?” |
| Repeated fallback                   | “I think it’s time we bring in a human.” |
| Urgent/negative sentiment detected  | Escalate to live agent with transcript   |

---

## 6. Success Criteria

Define what success looks like for this flow.

- User reaches a decision (e.g. chooses plan, books demo)  
- User is routed to correct team without drop-off  
- Feedback or satisfaction score collected  
- Conversion, resolution, or next step logged

---

## 7. Optimisation Notes (Post-Launch)

Use this section to track feedback and future improvements.

| Issue / Insight                  | Proposed Change                        | Owner        |
|----------------------------------|----------------------------------------|--------------|
| Drop-off after plan comparison   | Add follow-up question or CTA          | Marketing    |
| Too formal tone in fallback      | Rewrite fallback with softer tone      | Content team |
| Missing product FAQ              | Add content block for pricing queries  | Product      |

---

Save this template for every major flow. Review and iterate monthly as part of your [continuous improvement loop](../part4/continuous-improvement.md).
