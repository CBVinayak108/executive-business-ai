# Product Metrics and Funnels — Starting Framework

## 1. Start with the product decision

Before selecting a metric, state:

- **User and job:** who is trying to do what?
- **Business outcome:** what value should improve?
- **Decision:** what choice will this analysis or experiment inform?
- **Time window and population:** when and for whom is success measured?

A metric without a decision is reporting, not product analytics.

## 2. Metric hierarchy

| Layer | Purpose | Example: checkout |
| --- | --- | --- |
| North-star / outcome | Long-term value created for users and business | Completed, successful orders |
| Input / driver | Behaviour that plausibly drives the outcome | Payment-page completion |
| Guardrail | Harm that must not worsen | Refund rate, payment failure, support contacts |
| Diagnostic | Explains a change | Failure rate by payment method or device |
| Data-quality | Validates the measurement | Event coverage, duplicate-event rate |

A good metric is defined by its formula, event source, owner, grain, time window, eligible population, exclusions, and known limitations.

## 3. Funnel method

1. **Map the user journey** from entry to value.
2. **Define events** with unambiguous names, timestamps, user/session IDs, and relevant properties.
3. **Choose the conversion window** and denominator.
4. **Measure step conversion and cumulative conversion.**
5. **Segment deliberately:** new versus returning, device, channel, geography, payment method, plan, or risk tier.
6. **Diagnose before proposing a fix:** verify tracking, quantify impact, inspect UX/qualitative evidence, and test plausible causes.
7. **Prioritise** by expected impact, confidence, effort, and risk.
8. **Evaluate the change** with the primary metric plus guardrails.

## 4. Domain prompts

### E-commerce — checkout conversion

`Product view → add to cart → begin checkout → address → payment attempt → payment success → order confirmed`

Primary outcome: completed orders / users who began checkout.  
Key guardrails: payment failures, cancellations, refunds, customer-support contacts, contribution margin.

### Retail SaaS — activation

`Sign-up → workspace created → data connected → first key workflow completed → recurring weekly use`

Activation must represent an early action that predicts durable value, not merely account creation.

### Fintech — payment success

`Payment initiated → authentication requested → authentication completed → authorisation → settlement / confirmation`

Primary outcome: successful payments / eligible payment attempts.  
Key guardrails: fraud loss, false declines, latency, disputes, and compliance exceptions.

## 5. Practice assignment

Create one one-page metric tree for each domain above. For every tree, include:

- the user value proposition;
- one north-star metric and its exact formula;
- 3–5 drivers;
- 2–4 guardrails;
- required events and properties;
- one current diagnostic question;
- one experimentable intervention.

Next: convert the checkout funnel into an A/B-test design.
