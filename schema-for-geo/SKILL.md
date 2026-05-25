---
skill: schema-for-geo
version: 1.0.0
author: Angie Thaxton
expertise: GEO, Structured Data, Schema Markup, LLM Discoverability
tools: Screaming Frog, Google Search Console, Schema Markup Validator, JSON-LD
tested: 2026-05
---

# Schema for GEO Skill

## What This Skill Does

This skill provides a structured framework for implementing and validating schema markup specifically to improve LLM discoverability and AI search visibility. It covers which schema types matter most for GEO, implementation priorities, validation, and common mistakes.

Use this skill when you need to:
- Audit a site's structured data for GEO readiness
- Prioritize schema implementation for maximum AI search impact
- Implement schema on pages with no existing structured data
- Fix broken or incomplete schema that is limiting AI visibility
- Build a schema implementation roadmap for a client

---

## Framework: Schema for GEO Implementation Process

### Phase 1 — Schema Audit

Before implementing anything, audit what already exists.

**Audit methods:**

1. **Google Search Console** — Rich Results report shows schema Google has detected and any errors
2. **Screaming Frog** — Crawl the site, export structured data report to see all schema across all pages
3. **Schema Markup Validator** — Test individual pages at validator.schema.org
4. **Google Rich Results Test** — Test at search.google.com/test/rich-results

**What to document in your audit:**

| Page | Schema Present | Schema Type | Errors | GEO Gap |
|---|---|---|---|---|
| Homepage | Yes | Organization | None | Missing sameAs links |
| /about | No | None | None | No Person or Organization schema |
| /blog/[post] | Partial | Article | Missing author | No author entity |
| /services/[service] | No | None | None | No Service or FAQPage schema |
| /faq | No | None | None | Critical — FAQPage schema missing |

---

### Phase 2 — GEO Schema Priority Map

Not all schema types have equal impact on LLM discoverability. Use this priority map to sequence implementation.

**Tier 1 — Implement first (highest GEO impact):**

| Schema Type | Where to Implement | Why It Matters for GEO |
|---|---|---|
| FAQPage | Any page with Q&A content, FAQ pages, service pages | Direct extraction signal — LLMs pull FAQ content into responses |
| Organization | Homepage, About page | Establishes brand entity — helps LLMs identify and describe your brand accurately |
| Person | Author pages, team pages, About page | Establishes individual expertise — supports E-E-A-T and citation credibility |

**Tier 2 — Implement second (high GEO impact):**

| Schema Type | Where to Implement | Why It Matters for GEO |
|---|---|---|
| Article / BlogPosting | All blog posts and guides | Signals authoritative published content — LLMs weight published articles |
| HowTo | Step-by-step instructional content | Directly maps to how-to query intent — high AIO extraction rate |
| LocalBusiness | Homepage and location pages (local businesses) | Feeds local AI Overview and Gemini local responses |

**Tier 3 — Implement third (medium GEO impact):**

| Schema Type | Where to Implement | Why It Matters for GEO |
|---|---|---|
| Product / Service | Product and service pages | Helps AI describe what you offer accurately |
| BreadcrumbList | All pages | Site structure signal — helps LLMs understand content hierarchy |
| Speakable | Key informational sections | Marks content specifically for AI and voice extraction |
| Review / AggregateRating | Pages with reviews | Social proof signal — LLMs reference ratings in recommendations |

---

### Phase 3 — Implementation Guidelines

**General rules for GEO-optimized schema:**

1. **Use JSON-LD format** — Google and LLMs prefer JSON-LD over Microdata or RDFa. Place in `<head>` or at end of `<body>`.

2. **Be specific, not generic** — Vague descriptions hurt more than no schema. "A company that provides services" tells LLMs nothing.

3. **Match schema content to page content** — Schema that describes things not on the page is flagged as spam by Google.

4. **Use sameAs extensively** — Linking your Organization schema to LinkedIn, Wikipedia, Wikidata, Crunchbase, and other authoritative profiles strengthens entity recognition.

5. **Nest entities** — Connect Person schema to Organization schema, Article schema to Person schema. Connected entities are stronger than isolated ones.

6. **Keep it current** — Update dateModified on Article schema whenever you update content. Stale dates signal outdated content.

---

### Phase 4 — Entity Establishment via Schema

For LLMs to cite your brand accurately, they need a clear entity signal. Schema is one of the most direct ways to establish this.

**Organization entity checklist:**
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Your Brand Name",
  "url": "https://yourdomain.com",
  "logo": "https://yourdomain.com/logo.png",
  "description": "Clear, specific description of what your organization does and who it serves.",
  "foundingDate": "YYYY",
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "value": 50
  },
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "City",
    "addressRegion": "State",
    "addressCountry": "US"
  },
  "sameAs": [
    "https://www.linkedin.com/company/your-brand",
    "https://twitter.com/yourbrand",
    "https://en.wikipedia.org/wiki/Your_Brand",
    "https://www.crunchbase.com/organization/your-brand",
    "https://www.wikidata.org/wiki/QXXXXXXX"
  ]
}
```

**Key field: description**
This is one of the most important fields for GEO. LLMs use the organization description to understand and describe your brand. Write it as a clear, accurate, one-to-two sentence description of what you do and who you serve.

**Key field: sameAs**
Each sameAs link is a connection to an authoritative entity record. The more quality sameAs links, the stronger the entity signal. Priority targets:
- LinkedIn company page
- Wikipedia (if eligible)
- Wikidata (create a record if you don't have one)
- Crunchbase
- Industry directories
- Google Business Profile URL

---

### Phase 5 — FAQPage Schema Best Practices

FAQPage schema is the single highest-impact schema type for GEO. Use it aggressively.

**Where to add FAQPage schema:**
- Dedicated FAQ pages (obvious)
- Service pages (add 4-5 questions about the service)
- Product pages (add questions about the product)
- Blog posts that answer questions (add related questions)
- Homepage (add 3-5 brand/category questions)
- Location pages (add local service questions)

**Writing FAQ content for GEO:**
- Write questions the way a user would actually ask them
- Keep answers concise — 2-4 sentences per answer
- Answer directly — no preamble before the actual answer
- Include your brand name naturally where relevant
- Use consistent terminology with your other content

**FAQ question types that perform well in AI responses:**
- Definition questions: "What is [topic]?"
- Process questions: "How does [process] work?"
- Comparison questions: "What is the difference between X and Y?"
- Eligibility questions: "Who needs [service]?"
- Cost questions: "How much does [service] cost?"

---

### Phase 6 — Validation and QA

Never deploy schema without validating it first.

**Validation checklist:**
- [ ] Test with Schema Markup Validator (validator.schema.org)
- [ ] Test with Google Rich Results Test (search.google.com/test/rich-results)
- [ ] Confirm no errors or warnings in GSC Rich Results report after deployment
- [ ] Verify JSON is valid (no syntax errors) using jsonlint.com
- [ ] Confirm schema content matches visible page content
- [ ] Check that all required properties are present for each schema type

**Common schema errors that hurt GEO:**
- Missing required fields (name, url for Organization)
- Incorrect @type values
- Schema describing content not on the page
- Duplicate schema blocks for the same entity
- Invalid JSON syntax (missing commas, unclosed brackets)
- Using Microdata instead of JSON-LD

---

## Decision Tree: Which Schema Should I Add First?

```
Does the site have Organization schema on the homepage?
├── NO → Add Organization schema first
│         This is your entity foundation
└── YES → Does it have sameAs links?
          ├── NO → Add sameAs links to existing Organization schema
          └── YES → Does the site have FAQPage schema anywhere?
                    ├── NO → Add FAQPage schema to top service/product pages
                    └── YES → Do blog posts have Article schema with author?
                              ├── NO → Add Article + Person schema to blog posts
                              └── YES → Add HowTo schema to instructional content
                                        Then add Speakable to key informational sections
```
