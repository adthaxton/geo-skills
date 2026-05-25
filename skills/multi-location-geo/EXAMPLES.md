# Multi-Location GEO — Examples

Worked examples from multi-location GEO optimization across automotive, legal, and service business contexts.

---

## Example 1: Automotive Dealership Group — GEO Audit and Optimization

**Scenario:** A dealership group with 12 locations across 3 states. Some locations appear in AI responses for local queries; most don't. The brand has a strong Google presence but inconsistent AI visibility.

**Baseline audit findings:**

| Location | GBP Verified | Location Page | LocalBusiness Schema | AI Visibility |
|---|---|---|---|---|
| Flagship (City A) | Yes | Yes - 800 words | Yes | High |
| City B | Yes | Yes - 180 words | No | Low |
| City C | Yes | No - redirects to homepage | No | None |
| City D | Yes | Yes - 200 words (duplicate of B) | No | Low |
| City E | No | Yes - 400 words | No | None |
| Cities F-L | Mixed | Thin or missing | No | None |

**Root causes identified:**
1. Only flagship location has adequate content and schema
2. 1 location has no GBP listing
3. Most location pages are thin or duplicate
4. No LocalBusiness schema outside flagship
5. NAP inconsistencies found in 4 locations

**Prioritized fix plan:**

**Week 1-2: Foundation fixes**
- Verify GBP for City E
- Correct NAP inconsistencies in all affected listings
- Add LocalBusiness schema to all 12 locations

**Week 3-6: Content expansion**
- Expand City B, C, D pages to 500+ words of unique content
- Add FAQ section with 4-5 location-specific questions to each page
- Add FAQPage schema to all location pages

**Week 7-12: Polish and monitor**
- Complete GBP optimization (descriptions, services, photos) for all locations
- Add parentOrganization to all LocalBusiness schema
- Monitor AI visibility monthly

**Result (90 days post-implementation):**
- AI visibility improved from 2/12 to 9/12 locations
- 3 locations now appearing in Google AI Overviews for local queries
- GBP views increased 34% across the portfolio

---

## Example 2: Law Firm — Multi-City Expansion GEO Setup

**Scenario:** A personal injury law firm opening 4 new office locations. They want to establish AI search visibility from day one rather than building it retroactively.

**Day-one GEO setup for each new location:**

**Step 1: GBP setup**
- Create and verify GBP listing before the office opens (can be done up to 90 days in advance)
- Complete all fields: description, services, hours, photos (use exterior photos of the building)
- Set website URL to the location-specific page

**Step 2: Location page creation**
Structure for each new location page:

```
H1: Personal Injury Attorney in [City, State]

[Direct answer paragraph — who we are, what we do in this city, 
who we serve]

## Why Choose [Firm Name] in [City]

[Location-specific content — local courts, local knowledge, 
local community involvement]

## Practice Areas in [City]

[List of services with brief descriptions]

## Our [City] Office

[Address, phone, hours, parking/access info, staff bio if available]

## Frequently Asked Questions — [City] Personal Injury Cases

[5 location-specific FAQ questions with schema markup]
```

**Step 3: Schema implementation**
- LocalBusiness schema with LegalService subtype
- parentOrganization connecting to firm entity
- FAQPage schema on location page
- Person schema for the attorney assigned to that office

**Step 4: Directory submissions**
- GBP (done in step 1)
- Avvo listing for the assigned attorney
- FindLaw firm listing
- Martindale-Hubbell
- State bar association directory

**Result:** All 4 new locations appeared in AI responses for "[city] personal injury attorney" queries within 8 weeks of opening.

---

## Example 3: Franchise — Scaling GEO Across 50+ Locations

**Scenario:** A home services franchise with 52 locations wants to improve AI search visibility across the network. Manual optimization is not feasible at this scale.

**Scalable system built:**

**1. Master data spreadsheet**
Created a spreadsheet with all location data:
- Location name (standardized format)
- Address, city, state, zip
- Phone number
- Hours
- GPS coordinates
- GBP listing URL
- Website location page URL
- Primary category
- Services offered

**2. Schema template script**
Built a Python script that reads the spreadsheet and outputs valid LocalBusiness JSON-LD for each location. Each location's schema is generated in under 1 second, all 52 in under 1 minute.

**3. Location page template**
Created a CMS template where:
- H1, title tag, and meta description auto-populate with city name
- Address block auto-populates from the data feed
- Schema auto-generates from location data
- 3 content blocks require unique input per location:
  - Local service area description (1 paragraph)
  - Local team bio (1-2 sentences)
  - 3 location-specific FAQ questions

**4. GBP bulk update**
Used GBP bulk management to:
- Standardize business descriptions across all 52 listings
- Add missing services to all listings
- Update categories to the most specific available

**Time investment:** 40 hours initial setup, then approximately 2 hours per new location going forward.

**Result:** AI visibility across the franchise network improved from 8% of locations appearing in local AI queries to 61% within 4 months.

---

## Prompts to Use With This Skill

```
Audit the multi-location GEO setup for [brand name] with [X] locations.
Use the multi-location GEO framework to:
1. Identify the most common gaps across the location portfolio
2. Prioritize which locations to optimize first
3. Build a 90-day optimization roadmap
```

```
Write a location page content brief for:
Business type: [type]
Location: [city, state]
Services offered: [list]
Unique local context: [any local details]

Use the multi-location GEO content structure and include 
5 FAQ questions optimized for local AI responses.
```

```
Write LocalBusiness schema for the following location:
Business name: [name]
Address: [full address]
Phone: [number]
Hours: [hours]
Coordinates: [lat, long]
Parent brand: [brand name and URL]
GBP URL: [URL]

Use the multi-location GEO schema template.
```

```
I have [X] locations with inconsistent NAP data across GBP, 
the website, and directories. Build me an audit spreadsheet 
template and a prioritized correction checklist using the 
multi-location GEO NAP consistency framework.
```
