# E-E-A-T Signal Audit — Reference Data

Benchmarks, signal checklists, and reference data for E-E-A-T auditing in AI search contexts.

---

## E-E-A-T Signal Weight by Content Type

Different content types require different E-E-A-T emphasis. Use this table to prioritize signals by page type.

| Content Type | Most Critical Signals | Secondary Signals |
|---|---|---|
| Blog posts / guides | Expertise (author), Experience | Authoritativeness (external links) |
| Service pages | Trustworthiness, Experience | Expertise (org credentials) |
| About page | All four equally | — |
| Product pages | Trustworthiness (reviews), Experience | Expertise (brand authority) |
| YMYL health content | Expertise (credentials), Trustworthiness | Authoritativeness (citations) |
| YMYL financial content | Expertise, Trustworthiness (disclaimers) | Authoritativeness |
| YMYL legal content | Expertise (attorney authorship), Trust | Authoritativeness |
| News / current events | Authoritativeness, Trustworthiness | Experience |
| Local business pages | Trustworthiness (NAP, reviews) | Experience (local knowledge) |

---

## Author Page Requirements for Strong E-E-A-T

A well-structured author page is one of the highest-impact E-E-A-T improvements available. Each author page should include:

**Required elements:**
- Full name and professional headshot
- Current job title and organization
- Brief bio (150-300 words) emphasizing relevant expertise
- List of credentials, certifications, or degrees relevant to the content area
- Links to published work on the site
- Person schema with jobTitle, worksFor, sameAs

**Strongly recommended:**
- Links to third-party publications or guest posts
- LinkedIn profile link (in sameAs)
- Years of experience in the field stated explicitly
- Notable clients, projects, or achievements
- Contact information or preferred contact method

**Person schema template for author pages:**
```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Author Full Name",
  "jobTitle": "Job Title",
  "url": "https://www.domain.com/author/name",
  "image": "https://www.domain.com/images/author-name.jpg",
  "description": "Brief professional bio emphasizing expertise.",
  "worksFor": {
    "@type": "Organization",
    "name": "Organization Name",
    "url": "https://www.domain.com"
  },
  "sameAs": [
    "https://www.linkedin.com/in/authorname",
    "https://twitter.com/authorhandle",
    "https://authorpersonalsite.com"
  ]
}
```

---

## External Authority Building — Priority Tactics by Industry

### B2B and Professional Services
| Tactic | Authority Impact | Time to Impact |
|---|---|---|
| Guest posts on industry publications | High | 2-4 months |
| Podcast appearances | Medium-High | 1-3 months |
| Industry association membership and listing | Medium | 1-2 months |
| Speaking at industry events | High | 3-6 months |
| Contributed data or research to industry reports | Very High | 3-6 months |

### Local Service Businesses
| Tactic | Authority Impact | Time to Impact |
|---|---|---|
| Local press coverage | High | 1-3 months |
| Chamber of commerce listing | Medium | 1 month |
| Local business awards | Medium-High | Varies |
| Community involvement coverage | Medium | 1-3 months |
| Industry association listings | Medium | 1-2 months |

### E-commerce and Consumer Brands
| Tactic | Authority Impact | Time to Impact |
|---|---|---|
| Product reviews on authoritative sites | High | Ongoing |
| Influencer or media coverage | High | 1-3 months |
| Industry awards | Medium-High | Varies |
| User-generated content and reviews | Medium | Ongoing |

---

## Trust Signal Checklist — Quick Reference

| Signal | Location | Status Check |
|---|---|---|
| HTTPS | All pages | Check browser address bar for padlock |
| Privacy policy | Footer link | Present and dated within 2 years |
| Terms of service | Footer link | Present |
| Contact page | Navigation or footer | Real address, phone, email |
| About page | Navigation | Describes org history and team |
| Author bylines | All content pages | Name links to author page |
| Source citations | All factual claims | Links to original sources |
| Review responses | GBP, Yelp, etc. | All reviews responded to |
| Physical address | Contact page, schema | Matches GBP and directories |

---

## YMYL Topic Categories Reference

Google and LLMs apply heightened scrutiny to content in these areas. Strong E-E-A-T is non-negotiable.

**High YMYL:**
- Medical diagnosis, treatment, or medication information
- Mental health advice
- Financial investment advice
- Legal advice on specific situations
- Safety instructions for dangerous activities
- News about elections, government, or public policy

**Medium YMYL:**
- General health and wellness information
- General financial information (budgeting, saving)
- General legal information (not specific advice)
- Parenting and child development
- Nutrition and diet

**Lower YMYL:**
- General how-to content
- Entertainment and hobby content
- Historical information
- Technology tutorials

---

## E-E-A-T Audit Scoring Benchmarks

Based on practitioner observation across content sites:

| Score Range | Typical AI Citation Behavior |
|---|---|
| 20-25 | Brand cited regularly, described accurately, recommended in relevant queries |
| 15-19 | Brand cited sometimes, description mostly accurate, competitive in AI responses |
| 10-14 | Brand cited rarely, description may be vague or inconsistent |
| Under 10 | Brand largely absent from AI responses or described inaccurately |

---

## Common E-E-A-T Mistakes That Hurt AI Visibility

| Mistake | Impact | Fix |
|---|---|---|
| No author bylines | High — LLMs can't assess expertise | Add author bylines to all content |
| Generic author bios | Medium — credentials not visible | Rewrite bios with specific expertise |
| No source citations | High — reduces trust signals | Add links to authoritative sources |
| Outdated content (no update dates) | Medium — freshness signal missing | Add/update dateModified in schema and on page |
| No About page | High — organization identity unclear | Create comprehensive About page |
| Contact page with only a form | Medium — reduces trust | Add physical address and phone |
| Self-declared expertise only | High — no external validation | Build third-party mentions and links |
| YMYL content without credentials | Very High | Add credentialed author or reviewer |
