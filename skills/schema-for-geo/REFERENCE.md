# Schema for GEO — Reference Data

Schema type reference, required properties, validation tools, and implementation benchmarks.

---

## Schema Type Quick Reference

### FAQPage
**GEO Impact:** Very High  
**Required properties:** mainEntity (array of Question)  
**Question required:** name (question text), acceptedAnswer  
**Answer required:** text  
**Validator:** search.google.com/test/rich-results  
**Notes:** Maximum impact on AIO inclusion. Add to any page answering questions.

### Organization
**GEO Impact:** High  
**Required properties:** name  
**Recommended:** url, logo, description, sameAs, address, foundingDate  
**Validator:** validator.schema.org  
**Notes:** Entity foundation. Use on homepage and About page. Strong sameAs profile is critical.

### Person
**GEO Impact:** High  
**Required properties:** name  
**Recommended:** url, jobTitle, worksFor, sameAs, image, description  
**Validator:** validator.schema.org  
**Notes:** Use on author pages and team pages. Connect to Organization via worksFor.

### Article / BlogPosting / NewsArticle
**GEO Impact:** High  
**Required properties:** headline, author, datePublished  
**Recommended:** dateModified, publisher, description, image  
**Validator:** search.google.com/test/rich-results  
**Notes:** Always include author as Person entity, not just a string.

### HowTo
**GEO Impact:** Medium-High  
**Required properties:** name, step  
**Recommended:** description, totalTime, estimatedCost, supply, tool  
**Validator:** search.google.com/test/rich-results  
**Notes:** Each step needs name and text. Image per step is optional but improves rich result eligibility.

### LocalBusiness
**GEO Impact:** High (for local businesses)  
**Required properties:** name, address  
**Recommended:** telephone, url, openingHours, geo, priceRange, aggregateRating, sameAs  
**Validator:** search.google.com/test/rich-results  
**Notes:** Use more specific subtype when available (e.g., AutoDealer, LegalService, MedicalBusiness).

### Product
**GEO Impact:** Medium  
**Required properties:** name  
**Recommended:** description, image, brand, offers, aggregateRating  
**Validator:** search.google.com/test/rich-results  
**Notes:** Include Review or AggregateRating for richer AI description.

### Service
**GEO Impact:** Medium  
**Required properties:** name  
**Recommended:** description, provider, areaServed, serviceType  
**Validator:** validator.schema.org  
**Notes:** No Google rich result, but valuable for entity and LLM understanding.

### BreadcrumbList
**GEO Impact:** Medium  
**Required properties:** itemListElement (array of ListItem)  
**ListItem required:** position, name, item (URL)  
**Validator:** search.google.com/test/rich-results  
**Notes:** Implement site-wide. Helps LLMs understand content hierarchy and site structure.

### Speakable
**GEO Impact:** Medium (emerging)  
**Required properties:** cssSelector or xpath  
**Validator:** validator.schema.org  
**Notes:** Marks sections for AI and voice extraction. Underused — early adoption advantage.

---

## sameAs Priority Targets by Entity Type

### For Organizations
| Platform | Priority | Notes |
|---|---|---|
| LinkedIn company page | High | Most authoritative professional entity signal |
| Wikipedia | High | If eligible — very strong signal |
| Wikidata | High | Create record if none exists — free, open |
| Crunchbase | High | Strong for B2B and tech companies |
| Google Business Profile | Medium-High | Especially important for local businesses |
| Facebook business page | Medium | Consumer brands |
| Twitter / X | Medium | If actively maintained |
| Industry directories | Medium | Varies by vertical |
| BBB listing | Low-Medium | Trust signal for service businesses |

### For People (Authors/Experts)
| Platform | Priority | Notes |
|---|---|---|
| LinkedIn profile | High | Most authoritative professional identity |
| Twitter / X | Medium-High | If actively used for professional content |
| Google Scholar | High | Academic and research contexts |
| Personal website | Medium-High | Author's own domain |
| Wikipedia | High | If eligible |
| Wikidata | High | Create record for notable individuals |
| ORCID | Medium | Research and academic contexts |

---

## Required vs Recommended Properties Cheat Sheet

| Schema Type | Required | Strongly Recommended for GEO |
|---|---|---|
| Organization | name | url, description, sameAs, logo |
| Person | name | url, jobTitle, worksFor, sameAs |
| Article | headline, author, datePublished | dateModified, publisher, image |
| FAQPage | mainEntity | (all question/answer pairs) |
| Question | name, acceptedAnswer | — |
| Answer | text | — |
| LocalBusiness | name, address | telephone, geo, openingHours, sameAs |
| HowTo | name, step | description, totalTime |
| BreadcrumbList | itemListElement | — |

---

## Validation Tools

| Tool | URL | What It Checks |
|---|---|---|
| Schema Markup Validator | validator.schema.org | All schema types — errors and warnings |
| Google Rich Results Test | search.google.com/test/rich-results | Google-eligible rich result types |
| Google Search Console | search.google.com/search-console | Site-wide schema health and errors |
| JSON Lint | jsonlint.com | JSON syntax validation |
| Screaming Frog | Desktop app | Site-wide schema audit via crawl |
| Merkle Schema Markup Generator | technicalseo.com/tools/schema-markup-generator | Visual schema builder |

---

## Common Schema Errors Reference

| Error | Cause | Fix |
|---|---|---|
| Missing required field | Required property omitted | Add the required property |
| Invalid URL | Malformed or relative URL in url/sameAs | Use full absolute URLs (https://...) |
| Schema not matching page content | Describes content not visible on page | Align schema with actual page content |
| Duplicate @type | Multiple schema blocks for same entity | Consolidate into single block |
| Author as string | author: "Name" instead of Person entity | Use author: {"@type": "Person", "name": "..."} |
| Invalid JSON | Syntax errors — missing commas, brackets | Validate with jsonlint.com before deploying |
| Wrong @type | Using generic type when specific subtype exists | Use AutoDealer instead of Organization for car dealers |

---

## LocalBusiness Subtypes Relevant to Common Verticals

| Industry | Schema Subtype |
|---|---|
| Automotive dealership | AutoDealer |
| Law firm | LegalService |
| Medical practice | MedicalBusiness, Physician |
| Dental practice | Dentist |
| Real estate agency | RealEstateAgent |
| Restaurant | Restaurant, FoodEstablishment |
| Hotel | Hotel, LodgingBusiness |
| Home services | HomeAndConstructionBusiness |
| Financial services | FinancialService |
| Accounting | AccountingService |

---

## Schema Implementation Benchmarks

Based on practitioner observation across client sites:

| Metric | Typical Baseline | After Schema Implementation |
|---|---|---|
| AIO inclusion rate (pages with FAQPage schema) | Low | 2-4x improvement in 4-8 weeks |
| Rich result eligibility | Limited | FAQ and Article rich results within 2-4 weeks |
| GSC impressions for FAQ-targeted queries | Baseline | 15-40% increase over 60-90 days |
| LLM citation accuracy | Variable | Measurable improvement in 6-12 weeks |

Note: Results vary significantly by domain authority, content quality, and competitive landscape.
