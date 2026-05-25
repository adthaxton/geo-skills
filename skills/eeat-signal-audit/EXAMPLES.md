# E-E-A-T Signal Audit — Examples

Worked examples showing E-E-A-T auditing and improvement across common scenarios.

---

## Example 1: B2B SaaS Company — Full E-E-A-T Audit

**Scenario:** A project management SaaS company ranks well organically but rarely appears in AI responses. When they do appear, the description is vague — "a project management tool." Competitors with weaker organic rankings are cited more often and described more specifically.

**E-E-A-T audit results:**

| Signal Area | Score | Key Gaps |
|---|---|---|
| Experience | 2/5 | No case studies, no first-person content, generic blog posts |
| Expertise | 2/5 | No author bylines, no author pages, team page has names only |
| Authoritativeness | 3/5 | Some backlinks, no press coverage, not in industry publications |
| Trustworthiness | 4/5 | HTTPS, privacy policy, contact page all present. No source citations. |
| **Total** | **11/20** | **Significant gaps limiting AI citation** |

**Priority fix plan:**

**Month 1 — Expertise and experience:**
1. Add author bylines to all 47 existing blog posts
2. Create author pages for the 3 primary content contributors with full bios and Person schema
3. Rewrite the 5 highest-traffic blog posts to include first-person perspective and specific examples from real customer use cases
4. Add source citations to all statistical claims

**Month 2 — Authoritativeness:**
1. Pitch 3 guest posts to SaaS and project management industry publications
2. Submit to 5 relevant industry directories and associations
3. Reach out to 2 industry podcasts for interview opportunities

**Month 3 — Experience deepening:**
1. Publish 3 detailed case studies with specific results and client context
2. Add "Last updated" dates to all evergreen content
3. Update About page with company history, founding story, and team credentials

**Re-audit results (90 days later):**

| Signal Area | Before | After |
|---|---|---|
| Experience | 2/5 | 4/5 |
| Expertise | 2/5 | 4/5 |
| Authoritativeness | 3/5 | 4/5 |
| Trustworthiness | 4/5 | 5/5 |
| **Total** | **11/20** | **17/20** |

AI citation behavior changed noticeably — the brand began appearing in responses describing them specifically as "project management software built for agency workflows" rather than the previous generic framing.

---

## Example 2: Medical Practice — YMYL E-E-A-T Audit

**Scenario:** A multi-location orthopedic practice publishes health information content but is not appearing in AI responses for queries like "symptoms of a torn ACL" or "when to see a doctor for knee pain" — queries they rank for organically.

**Root cause:** Content lacks YMYL-grade E-E-A-T. No physician authorship is credited, no credentials are shown, and content reads like marketing copy rather than medical information.

**Specific gaps identified:**
- Blog posts have no author bylines
- The doctors page has names and photos but no bios or credentials
- Content makes medical claims without sourcing
- No "reviewed by" or "medically reviewed" notation
- No publication or update dates on any content

**Fixes implemented:**

1. **Physician authorship** — Every health information article now has a byline crediting the authoring physician. Author pages built for each doctor with:
   - Medical school and residency
   - Board certifications
   - Years of practice
   - Specializations
   - Publications or research
   - Person schema with sameAs linking to state medical board listing

2. **Medical review notation** — Added "Medically reviewed by [Dr. Name], [credentials]" to all existing health content

3. **Source citations** — Added citations to peer-reviewed sources (PubMed, AAOS) for all clinical claims

4. **Content updates** — Added publication and last-reviewed dates to all articles

5. **Schema** — Added MedicalWebPage schema to health content pages with reviewedBy field pointing to physician Person entity

**Result:** 6 health information pages began appearing in Google AI Overviews within 8 weeks. The AI descriptions changed from absent to specific citations crediting the practice's physicians.

---

## Example 3: Law Firm — Building External Authority

**Scenario:** A personal injury law firm has strong on-site E-E-A-T (attorney bios, credentials, schema) but weak external authority. AI responses for "personal injury attorney [city]" consistently cite two competitor firms instead.

**External authority gap analysis:**

Competitor A (cited in 80% of AI responses):
- Featured in 12 local news articles in past 2 years
- Attorneys listed on Avvo with 50+ client reviews each
- Active legal blog with 3 external sites citing their content
- Wikipedia mention in a local legal case article
- Martindale-Hubbell AV Preeminent rating

Client firm (cited in 10% of AI responses):
- No press coverage in 2 years
- Avvo profiles exist but minimal reviews
- No external sites citing their content
- No directory listings beyond basic ones

**Authority building plan:**

**Digital PR (ongoing):**
- Monthly press release to local media on significant case results (no client names)
- Pitch attorneys as expert sources to local journalists covering legal topics
- Submit commentary to local business publications on legal issues affecting businesses

**Directory and listing authority:**
- Complete Avvo profiles with all credentials, case results, and client reviews
- Submit to Martindale-Hubbell for rating
- Join and get listed by state and local bar associations
- Submit to FindLaw and Justia

**Content-based authority:**
- Publish original research: "Most Common Causes of Car Accidents in [State] — 5 Year Analysis"
- Pitch guest columns to local newspaper legal section
- Appear on 2-3 local legal or business podcasts

**Result (6 months):** Citation rate in AI responses increased from 10% to 55%. The firm's attorneys began being cited by name in AI responses as "experienced personal injury attorneys" in the local market.

---

## Prompts to Use With This Skill

```
Conduct an E-E-A-T signal audit for this website:
[paste URL or site description]

Use the E-E-A-T signal audit framework to:
1. Score each signal area from 1-5
2. Identify the top 3 gaps limiting AI citation
3. Build a prioritized 90-day improvement plan
```

```
Review this author bio for E-E-A-T strength:
[paste bio]

Score it against the author page requirements and rewrite it
to strengthen expertise and experience signals for AI search.
```

```
This is a [YMYL topic] page. Audit it for YMYL E-E-A-T compliance:
[paste content]

Identify every gap that would cause Google or an LLM to 
discount this content as a credible source.
```

```
Write an author page bio for:
Name: [name]
Title: [title]
Credentials: [list credentials]
Experience: [years and context]
Published work: [any publications]

Optimize for E-E-A-T signals and include Person schema.
```
