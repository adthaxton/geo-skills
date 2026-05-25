# Schema for GEO — Examples

Worked examples showing schema implementation for LLM discoverability across common scenarios.

---

## Example 1: Full Organization Schema for a B2B SaaS Company

**Scenario:** A project management SaaS company has no Organization schema. LLMs describe them inconsistently — sometimes accurately, sometimes confusing them with a competitor.

**Root cause:** No entity anchor on the site. LLMs are piecing together descriptions from scattered web mentions.

**Implementation:**

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Acme Project Co",
  "url": "https://www.acmeprojectco.com",
  "logo": "https://www.acmeprojectco.com/images/logo.png",
  "description": "Acme Project Co is a project management platform built for creative agencies, helping teams manage client work, deadlines, and billing in one place.",
  "foundingDate": "2018",
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "value": 45
  },
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Austin",
    "addressRegion": "TX",
    "addressCountry": "US"
  },
  "sameAs": [
    "https://www.linkedin.com/company/acme-project-co",
    "https://twitter.com/acmeprojectco",
    "https://www.crunchbase.com/organization/acme-project-co",
    "https://www.g2.com/products/acme-project-co/reviews"
  ]
}
```

**Key decisions:**
- Description is specific — names the target customer (creative agencies) and the core value prop
- sameAs includes LinkedIn, Twitter, Crunchbase, and G2 — four strong entity anchors
- numberOfEmployees included — helps LLMs characterize company size accurately

**Result:** LLM description accuracy improved significantly within 8 weeks. ChatGPT began consistently describing the product as "project management for agencies" rather than generic project management.

---

## Example 2: FAQPage Schema on a Service Page

**Scenario:** A digital marketing agency wants their SEO services page to appear in AI Overviews for queries like "what does an SEO agency do" and "how much does SEO cost."

**Step 1: Identify target questions**
- What does an SEO agency do?
- How much does SEO cost?
- How long does SEO take to work?
- What is the difference between SEO and PPC?
- Do I need an SEO agency or can I do it myself?

**Step 2: Write direct answers (GEO-optimized)**

Each answer leads with the direct response — no preamble.

**Step 3: Implement FAQPage schema**

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What does an SEO agency do?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "An SEO agency improves a website's visibility in search engine results through technical optimization, content strategy, and link building. Services typically include technical audits, keyword research, on-page optimization, content creation, and performance reporting."
      }
    },
    {
      "@type": "Question",
      "name": "How much does SEO cost?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "SEO agency services typically range from $1,500 to $10,000 per month depending on the scope of work, business size, and competitive market. Project-based SEO engagements may range from $5,000 to $30,000 depending on complexity."
      }
    },
    {
      "@type": "Question",
      "name": "How long does SEO take to work?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Most SEO campaigns produce measurable ranking improvements within 3-6 months. Significant traffic increases typically follow at 6-12 months. Competitive markets and new domains may take longer to show results."
      }
    },
    {
      "@type": "Question",
      "name": "What is the difference between SEO and PPC?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "SEO (search engine optimization) earns organic traffic through content and technical optimization without paying for clicks. PPC (pay-per-click) buys traffic through paid ads. SEO builds long-term visibility; PPC delivers immediate traffic while the budget runs."
      }
    }
  ]
}
```

---

## Example 3: Article Schema with Nested Person Entity

**Scenario:** A law firm blog has no schema. Articles are not appearing in AI Overviews despite ranking in the top 5 for target queries. E-E-A-T is the gap — Google can't identify the author's credentials.

**Before:** No schema, no author byline on articles.

**After — Article schema with nested Person:**

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "What to Do After a Car Accident in Texas: A Step-by-Step Guide",
  "datePublished": "2025-09-10",
  "dateModified": "2026-04-15",
  "description": "A practical guide to the steps Texas drivers should take immediately after a car accident, from documenting the scene to filing an insurance claim.",
  "author": {
    "@type": "Person",
    "name": "James R. Holloway",
    "jobTitle": "Personal Injury Attorney",
    "url": "https://www.hollowayfirm.com/attorneys/james-holloway",
    "sameAs": [
      "https://www.linkedin.com/in/jamesrholloway",
      "https://www.avvo.com/attorneys/james-holloway"
    ]
  },
  "publisher": {
    "@type": "Organization",
    "name": "Holloway Law Firm",
    "url": "https://www.hollowayfirm.com",
    "logo": "https://www.hollowayfirm.com/logo.png"
  }
}
```

**Key decisions:**
- Author is a Person entity with jobTitle and sameAs — not just a name string
- sameAs for the author includes LinkedIn and Avvo (authoritative legal directory)
- dateModified reflects recent review — freshness signal
- Publisher is nested Organization entity connecting article to the firm

**Result:** Two articles appeared in AI Overviews within 6 weeks of schema deployment. GSC showed AIO impressions beginning at week 4.

---

## Example 4: Multi-Location LocalBusiness Schema

**Scenario:** An automotive dealership group has 8 locations. LLMs only mention their flagship location and underrepresent their geographic coverage.

**Approach:** Implement individual LocalBusiness schema on each location page, connected to the parent Organization.

**Per-location schema pattern:**

```json
{
  "@context": "https://schema.org",
  "@type": "AutoDealer",
  "name": "Sunrise Auto Group - Northside",
  "url": "https://www.sunriseautogroup.com/locations/northside",
  "telephone": "+15551234567",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "1234 North Main Street",
    "addressLocality": "Springfield",
    "addressRegion": "IL",
    "postalCode": "62701",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 39.7817,
    "longitude": -89.6501
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
      "opens": "09:00",
      "closes": "18:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": "Saturday",
      "opens": "09:00",
      "closes": "17:00"
    }
  ],
  "parentOrganization": {
    "@type": "Organization",
    "name": "Sunrise Auto Group",
    "url": "https://www.sunriseautogroup.com"
  },
  "sameAs": [
    "https://www.google.com/maps?cid=XXXXXXXXXXXXXXX",
    "https://www.facebook.com/sunriseautogroup.northside"
  ]
}
```

**Key decisions:**
- Uses AutoDealer subtype (not generic Organization)
- parentOrganization connects each location to the brand entity
- geo coordinates improve local AI response accuracy
- GBP URL in sameAs connects schema to Google's own entity data

---

## Prompts to Use With This Skill

```
Audit the schema markup on this page for GEO readiness:
[paste URL or page source]

Use the schema-for-geo framework to:
1. Identify what schema is present and what is missing
2. Prioritize additions by GEO impact
3. Write the JSON-LD for the highest-priority missing schema type
```

```
Write complete Organization schema for this company:
Name: [company name]
Description: [what they do]
Location: [city, state]
Founded: [year]
LinkedIn: [URL]
Other profiles: [list any known URLs]

Include all recommended GEO fields and sameAs links.
```

```
Write FAQPage schema for the following questions and answers:
[paste Q&A content]

Format as valid JSON-LD. Write answers to be direct and citation-friendly.
```

```
I have an Article schema where the author is listed as a plain string.
Rewrite it with the author as a nested Person entity with sameAs links.
Author name: [name]
Author title: [title]
Author LinkedIn: [URL]
Author bio page: [URL]
```
