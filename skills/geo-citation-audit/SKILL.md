---
skill: geo-citation-audit
version: 1.0.0
author: Angie Thaxton
expertise: GEO, AI Search Visibility, LLM Citation Strategy
tools: ChatGPT, Claude, Gemini, Perplexity, Google AI Overviews
tested: 2026-05
---

# GEO Citation Audit Skill

## What This Skill Does

This skill provides a structured framework for auditing how a brand is cited — or not cited — across LLM platforms and AI search interfaces. It covers manual and tool-assisted citation tracking, share of voice analysis, citation accuracy assessment, and gap identification.

Use this skill when you need to:
- Establish a citation baseline for a brand new to GEO
- Diagnose why a brand is not appearing in AI-generated responses
- Track citation rate changes after content or schema updates
- Compare brand citation share of voice against competitors
- Report GEO performance to clients or stakeholders

---

## Framework: The Citation Audit Process

### Phase 1 — Platform Inventory

Before running any prompts, establish which platforms matter for your client:

| Platform | When It Matters |
|---|---|
| Google AI Overviews | Always — highest volume, most visible to end users |
| Perplexity | B2B, research-oriented, technical audiences |
| ChatGPT | Brand awareness, consideration stage queries |
| Claude | Technical, professional, and research queries |
| Gemini | Google ecosystem users, mobile search |
| Microsoft Copilot | Enterprise, Office 365 users |

**Decision rule:** Start with Google AI Overviews and Perplexity for every audit. Add others based on where the client's audience lives.

---

### Phase 2 — Prompt Set Construction

Build a prompt set that covers three query intent categories:

**Category A — Direct category queries**
The brand should appear here if it has any LLM visibility at all.
- "What are the best [category] companies?"
- "Who are the leading [service type] providers?"
- "Which [type of business] should I consider?"

**Category B — Problem-first queries**
These reflect how real buyers search. Harder to rank for, higher value when achieved.
- "I need help with [specific problem]. Who should I talk to?"
- "What's the best way to solve [problem]? Who does this well?"
- "My [business type] is struggling with [challenge]. What are my options?"

**Category C — Comparison and validation queries**
Appear here to influence buyers already in consideration.
- "Is [Brand] a good choice for [use case]?"
- "Compare [Brand] vs [Competitor] for [specific need]"
- "What do people say about [Brand]?"

**Minimum prompt set:** 5 prompts per category = 15 prompts total per platform.

---

### Phase 3 — Citation Tracking

For each prompt run, record:

| Field | What to Capture |
|---|---|
| Date | Run date for trend tracking |
| Platform | Which LLM or AI interface |
| Prompt | Exact prompt text |
| Cited | YES / NO |
| Position | First mention, middle, end of response |
| Framing | How the brand is described |
| Accuracy | Is the description accurate? |
| Competitors cited | Which other brands appear |
| Source signals | Does the response cite web sources? Which? |

**Framing categories to watch:**
- **Authoritative** — brand cited as a leader or recommended choice
- **Neutral** — brand mentioned without strong recommendation
- **Qualified** — brand mentioned with caveats ("some users report...")
- **Negative** — brand mentioned in a negative context
- **Absent** — brand not cited at all

---

### Phase 4 — Share of Voice Calculation

For each prompt category, calculate:

```
Citation Rate = (Prompts where brand cited / Total prompts run) x 100
```

**Share of Voice vs Competitors:**
Run the same prompt set for 2-3 competitors. Compare citation rates side by side.

| Brand | Category A SOV | Category B SOV | Category C SOV | Overall |
|---|---|---|---|---|
| Your Brand | 40% | 20% | 60% | 40% |
| Competitor A | 80% | 60% | 40% | 60% |
| Competitor B | 20% | 40% | 20% | 27% |

---

### Phase 5 — Accuracy Audit

When a brand IS cited, assess the accuracy of the description:

**Check for:**
- Correct service/product description
- Accurate geographic coverage
- Current pricing or positioning (if referenced)
- Correct target audience description
- Accurate differentiators

**Common accuracy issues:**
- Outdated positioning from old web content
- Incorrect geographic coverage
- Missing recent services or products
- Attributed to wrong industry vertical
- Confused with similarly named competitor

**Root cause of inaccurate citations:** Usually stale content on the brand's own site, or thin/inconsistent entity signals across the web.

---

### Phase 6 — Gap Analysis & Recommendations

Use this decision tree to prioritize recommendations:

```
Is the brand cited at all?
├── NO → Start with entity establishment (org schema, About page, Wikipedia/Wikidata if eligible)
│         Then move to content gap analysis
└── YES → Is citation rate above 40%?
          ├── NO → Audit content structure for citation-friendly formatting
          │         Add FAQ schema, improve heading hierarchy
          └── YES → Is framing accurate and positive?
                    ├── NO → Audit source content for accuracy
                    │         Update About page, service descriptions
                    └── YES → Focus on expanding to Category B/C queries
                               and increasing share of voice vs competitors
```

---

## Diagnostic Questions to Ask Before Auditing

1. Does the brand have a clear, crawlable About page with entity signals?
2. Is Organization or LocalBusiness schema implemented?
3. Does the site have FAQ schema on key pages?
4. Is the brand mentioned on authoritative third-party sites (directories, press, industry publications)?
5. Are there consistent NAP signals across the web (for local businesses)?
6. Has the brand published any original research, data, or thought leadership?
7. Are there author pages with bylines linking to content?

---

## Reporting Citation Audit Results

**For client reporting, use this structure:**

1. **Executive summary** — overall citation rate, key finding, top recommendation
2. **Platform breakdown** — citation rate by platform
3. **Query category breakdown** — citation rate by intent category
4. **Share of voice** — brand vs 2-3 competitors
5. **Accuracy assessment** — is the brand described correctly when cited?
6. **Gap analysis** — where and why citations are missing
7. **Recommendations** — prioritized action list with expected impact

**Framing for clients unfamiliar with GEO:**
"Traditional SEO measures where you rank when someone searches Google. This audit measures whether AI tools — which an increasing share of your buyers use to research decisions — know who you are, describe you accurately, and recommend you in relevant conversations."
