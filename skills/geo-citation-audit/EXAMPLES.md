# GEO Citation Audit — Examples

Worked examples showing how to apply the citation audit framework in real scenarios.

---

## Example 1: New Client Baseline Audit (B2B SaaS)

**Scenario:** A B2B project management SaaS company has never tracked LLM visibility. They want to know where they stand before starting a GEO program.

**Step 1: Prompt set construction**

Category A (direct category):
- "What are the best project management tools for small teams?"
- "Which project management software do you recommend for agencies?"
- "Top project management platforms for remote teams"

Category B (problem-first):
- "My team struggles to stay on top of client deliverables. What tools can help?"
- "We keep missing deadlines. What project management software would help?"
- "I need a better way to manage multiple client projects. What do you recommend?"

Category C (comparison/validation):
- "Is [Brand] a good project management tool for a 10-person agency?"
- "Compare [Brand] vs Asana vs Monday.com for agency use"
- "What do people say about [Brand] project management software?"

**Step 2: Run on Perplexity and Google AI Overviews first**

**Step 3: Results logged**

| Platform | Category A | Category B | Category C | Overall |
|---|---|---|---|---|
| Google AIO | 2/5 (40%) | 0/5 (0%) | 3/5 (60%) | 33% |
| Perplexity | 3/5 (60%) | 1/5 (20%) | 4/5 (80%) | 53% |

**Step 4: Interpretation**

- Brand has moderate presence in Perplexity but weaker in Google AIO
- Category B (problem-first) is almost zero — major gap
- Category C is strongest — brand appears in comparison contexts
- Priority: Create problem-focused content that mirrors how buyers describe their pain

**Step 5: Recommendations**

1. Publish 3-5 blog posts framed around specific pain points ("How agencies manage client deadlines") rather than feature-focused content
2. Add FAQPage schema to the homepage and pricing page
3. Ensure Organization schema is complete with description, founding date, and sameAs links to LinkedIn and Crunchbase
4. Target 2-3 review platforms to build third-party citation presence (G2, Capterra, Trustpilot)

---

## Example 2: Citation Accuracy Issue (Local Service Business)

**Scenario:** A multi-location HVAC company is being cited in AI responses but described inaccurately — the AI says they only serve one city when they serve six.

**Diagnosis prompts:**
- "What HVAC companies serve [City 1] and surrounding areas?"
- "Is [Brand] available in [City 3]?"
- "Does [Brand] do commercial HVAC or just residential?"

**Root cause identified:**
- Homepage only mentions the original city in the body copy
- LocalBusiness schema only lists one address (the main office)
- GBP listings for branch locations are incomplete

**Fixes applied:**
1. Updated homepage to explicitly list all six service areas
2. Added service area markup to LocalBusiness schema
3. Created individual location pages for each city with complete NAP
4. Completed and verified all GBP listings with consistent descriptions

**Result (re-audit 6 weeks later):**
- Geographic accuracy in AI responses improved from 1/6 cities to 5/6 cities
- Category A citation rate increased from 20% to 45%

---

## Example 3: Competitor Share of Voice Analysis

**Scenario:** An SEO agency wants to understand its LLM share of voice against three competitors before pitching a GEO program to a client.

**Prompt set (run for all four brands):**
1. "What are the top SEO agencies for e-commerce brands?"
2. "Which SEO agency specializes in Shopify stores?"
3. "Best SEO companies for DTC brands"
4. "I run a DTC brand and need help with organic search. Which agencies should I talk to?"
5. "Compare [Agency A] vs [Agency B] for e-commerce SEO"

**Share of voice results:**

| Brand | Perplexity | ChatGPT | Google AIO | Avg SOV |
|---|---|---|---|---|
| Client Brand | 20% | 0% | 40% | 20% |
| Competitor A | 100% | 80% | 80% | 87% |
| Competitor B | 60% | 40% | 60% | 53% |
| Competitor C | 40% | 20% | 20% | 27% |

**Key finding:** Competitor A dominates because they have:
- A widely-cited "E-commerce SEO benchmark" report (original research)
- 50+ third-party mentions on e-commerce industry sites
- Complete FAQPage schema on key service pages
- Active case study content with named client results

**Recommended program:**
1. Publish one piece of original research with data (e-commerce SEO benchmark)
2. Pursue 10 guest posts or features on e-commerce industry publications
3. Add FAQPage schema to all service pages
4. Build out case study content with specific results

**Expected timeline:** 3-6 months to measurable SOV improvement

---

## Prompts to Use With This Skill

Paste these into any AI tool with this skill loaded:

```
Run a GEO citation audit for [Brand Name] in the [industry/category] space.
Use the citation audit framework to:
1. Build a 15-prompt test set across all three query categories
2. Identify which platforms to prioritize
3. Give me a reporting template for this client
```

```
I ran citation tracking for [Brand] and found a [X]% citation rate on Perplexity
and [Y]% on Google AI Overviews. Category B (problem-first) prompts returned 0%
citations. Use the gap analysis framework to diagnose why and give me a
prioritized recommendation list.
```

```
Compare the GEO citation presence of [Brand A] vs [Brand B] vs [Brand C]
in the [category] space. Build a share of voice table and identify what
the highest-cited brand is doing differently.
```
