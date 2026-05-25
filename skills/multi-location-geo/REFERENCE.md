# Multi-Location GEO — Reference Data

Benchmarks, tools, and reference data for multi-location GEO optimization.

---

## GBP Category Reference — Common Business Types

Using the most specific available primary category is one of the highest-impact GBP optimizations.

| Business Type | Recommended Primary Category |
|---|---|
| New car dealership | Car dealer |
| Used car dealership | Used car dealer |
| Auto repair | Auto repair shop |
| Personal injury law | Personal injury attorney |
| Family law | Family law attorney |
| General dentist | Dentist |
| Cosmetic dentist | Cosmetic dentist |
| HVAC contractor | HVAC contractor |
| Plumber | Plumber |
| Real estate agency | Real estate agency |
| Urgent care | Urgent care center |
| Physical therapy | Physical therapist |
| Accounting firm | Accountant |
| Insurance agency | Insurance agency |

---

## Location Page Content Benchmarks

| Page Type | Minimum Word Count | Recommended Word Count |
|---|---|---|
| Single location page | 400 words | 600-900 words |
| Location + service combo page | 500 words | 800-1200 words |
| Regional hub page (covers multiple locations) | 600 words | 1000-1500 words |
| Franchise location page | 400 words | 600-800 words |

---

## LocalBusiness Schema — Complete Multi-Location Template

```json
{
  "@context": "https://schema.org",
  "@type": "[BusinessSubtype]",
  "name": "[Brand Name] - [City] Location",
  "url": "https://www.domain.com/locations/[city]",
  "telephone": "+1[AreaCode][Number]",
  "email": "[location-email@domain.com]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Street Address]",
    "addressLocality": "[City]",
    "addressRegion": "[State Abbreviation]",
    "postalCode": "[ZIP]",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": [latitude],
    "longitude": [longitude]
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
  "priceRange": "$$",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "127"
  },
  "parentOrganization": {
    "@type": "Organization",
    "name": "[Brand Name]",
    "url": "https://www.domain.com"
  },
  "sameAs": [
    "https://www.google.com/maps?cid=[GBP_CID]",
    "https://www.facebook.com/[location-page]",
    "https://www.yelp.com/biz/[location-slug]"
  ]
}
```

---

## NAP Consistency Audit Template

Use this spreadsheet structure to audit NAP across all locations and channels:

| Location | Correct Name | Correct Address | Correct Phone | Website NAP | GBP NAP | Yelp NAP | Facebook NAP | Bing NAP | Notes |
|---|---|---|---|---|---|---|---|---|---|
| Location 1 | Brand - City | 123 Main St | 555-123-4567 | Match | Match | Mismatch | Match | Not listed | Update Yelp |
| Location 2 | Brand - City 2 | 456 Oak Ave | 555-234-5678 | Match | Old address | Match | Match | Match | Update GBP |

---

## Citation Management Tools

| Tool | Best For | Cost |
|---|---|---|
| BrightLocal | Citation audit and building, reputation management | Paid |
| Whitespark | Citation finding and building | Paid |
| Yext | Enterprise-scale listing management and sync | Paid (enterprise) |
| Moz Local | Citation monitoring and cleanup | Paid |
| GBP Bulk Management | Managing 10+ locations in GBP directly | Free (via GBP) |
| Manual audit | Small portfolios (under 10 locations) | Free |

---

## Priority Directories for Multi-Location Businesses

**Tier 1 — Must be present and accurate:**
- Google Business Profile
- Apple Maps (via Apple Business Connect)
- Bing Places
- Facebook Business Page
- Yelp

**Tier 2 — High value:**
- Yellow Pages
- Foursquare / Factual (data aggregator — feeds many other directories)
- Infogroup / Data Axle (data aggregator)
- Neustar Localeze (data aggregator)
- BBB (Better Business Bureau)

**Tier 3 — Industry-specific:**
- Varies by vertical — legal (Avvo, FindLaw), medical (Healthgrades, Zocdoc), automotive (Cars.com, DealerRater), home services (Angi, HomeAdvisor, Thumbtack)

---

## GBP Photo Benchmarks

| Photo Type | Minimum | Recommended |
|---|---|---|
| Exterior (storefront) | 2 | 4-6 |
| Interior | 2 | 4-6 |
| Team / staff | 1 | 3-5 |
| Products or services | 3 | 8-12 |
| Logo | 1 | 1 |
| Cover photo | 1 | 1 (updated seasonally) |

Listings with 10+ photos receive significantly more views and engagement than those with fewer. Photo quality matters — use professional or high-quality smartphone photos.

---

## AI Visibility Benchmarks for Multi-Location Businesses

| Scenario | Typical AI Visibility |
|---|---|
| Well-optimized GBP + location page + schema | High — appears in most local AI queries |
| GBP only, no location page | Medium — appears in some queries, limited context |
| Location page only, no GBP | Low — GBP is essential for local AI |
| Inconsistent NAP across channels | Low — confuses entity signals |
| Thin location page (under 300 words) | Low — insufficient content for extraction |
| Duplicate content across all location pages | Low-Medium — reduces individual page authority |

---

## Geo Coordinates Reference

Accurate geo coordinates in LocalBusiness schema improve local AI response accuracy, particularly for:
- Gemini local responses
- Google AI Overviews for "near me" queries
- Apple Maps Siri responses

**How to get accurate coordinates:**
- Google Maps: right-click on location pin > coordinates appear at top of context menu
- Google Search: search the address, coordinates shown in URL
- GPS Coordinates tool: gps-coordinates.net

Always use decimal degree format (e.g., 39.7817, -89.6501) not degrees/minutes/seconds.
