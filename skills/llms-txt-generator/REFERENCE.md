# llms.txt Generator — Reference Data

Templates, platform implementation guides, and reference data for llms.txt.

---

## llms.txt Templates by Business Type

### B2B SaaS Company

```
# [Company Name]

> [Company Name] is a [category] platform that helps [target customer]
> [achieve specific outcome].

[Company Name] builds software for [target market]. Founded in [year],
the platform serves [number]+ companies across [industries or regions].

This website covers [main topics]: product documentation, customer
case studies, integration guides, and thought leadership on [relevant topics].

## About

- Company: [URL/about]
- Team: [URL/team]
- Careers: [URL/careers]
- Contact: [URL/contact]

## Key Pages

- Homepage: [URL]
- Product Overview: [URL/product]
- Pricing: [URL/pricing]
- Integrations: [URL/integrations]
- Blog: [URL/blog]
- Documentation: [URL/docs]

## Topics Covered

- [Core topic 1]
- [Core topic 2]
- [Core topic 3]
- [Core topic 4]

## Organization Details

- Founded: [Year]
- Headquarters: [City, State]
- Industry: [Industry]
- Company size: [Range]

## Social and Entity Links

- LinkedIn: [URL]
- Twitter/X: [URL]
- GitHub: [URL if applicable]
- G2: [URL if applicable]
- Crunchbase: [URL]
```

---

### Local Service Business (Single Location)

```
# [Business Name]

> [Business Name] is a [business type] serving [city and surrounding areas],
> specializing in [core services].

[Business Name] has served [city] since [founding year]. [2-3 sentences
about what the business does, who it serves, and what makes it notable.]

This website provides information about [services offered], service areas,
pricing, and resources for [target customers].

## About

- About Us: [URL/about]
- Our Team: [URL/team]
- Contact: [URL/contact]

## Key Pages

- Homepage: [URL]
- Services: [URL/services]
- [Service 1]: [URL]
- [Service 2]: [URL]
- Service Areas: [URL/service-areas]
- Reviews: [URL/reviews]

## Topics Covered

- [Service type] in [City]
- [Related topic]
- [Related topic]

## Organization Details

- Founded: [Year]
- Location: [Full Address]
- Phone: [Number]
- Service Area: [Cities/regions served]
- Hours: [Hours]

## Social and Entity Links

- Google Business Profile: [URL]
- Facebook: [URL]
- Yelp: [URL]
```

---

### Multi-Location Business

```
# [Brand Name]

> [Brand Name] is a [business type] with [X] locations across [region],
> serving [customer type] with [core services].

[Brand Name] operates [X] locations in [states/regions]. Founded in [year],
the company serves [customer description]. [1-2 sentences about specialization
or notable differentiators.]

This website provides location information, service details, and resources
for customers across all [X] locations.

## About

- About: [URL/about]
- Locations: [URL/locations]
- Contact: [URL/contact]

## Locations

- [City 1]: [URL/locations/city-1]
- [City 2]: [URL/locations/city-2]
- [City 3]: [URL/locations/city-3]
[Continue for all locations]

## Services

- [Service 1]: [URL]
- [Service 2]: [URL]
- [Service 3]: [URL]

## Organization Details

- Founded: [Year]
- Headquarters: [City, State]
- Total Locations: [Number]
- Service Region: [States or regions]

## Social and Entity Links

- LinkedIn: [URL]
- Facebook: [URL]
- Google Business Profile (main): [URL]
```

---

### Law Firm

```
# [Firm Name]

> [Firm Name] is a [practice area] law firm serving clients in [state/region]
> from offices in [cities].

[Firm Name] represents [client type] in [practice areas]. Founded in [year],
the firm has [notable credential — recovered X in settlements, X years combined
experience, recognized by Super Lawyers, etc.].

This website provides legal information for [target clients] in [state],
including guides on [topics covered]. Content is authored by licensed
[state] attorneys.

## About

- About the Firm: [URL/about]
- Our Attorneys: [URL/attorneys]
- Contact: [URL/contact]

## Practice Areas

- [Practice Area 1]: [URL]
- [Practice Area 2]: [URL]
- [Practice Area 3]: [URL]

## Office Locations

- [City 1]: [URL/locations/city-1]
- [City 2]: [URL/locations/city-2]

## Topics Covered

- [Legal topic 1] in [State]
- [Legal topic 2] in [State]
- [Legal topic 3]

## Organization Details

- Founded: [Year]
- Bar Admission: [State(s)]
- Offices: [Cities]

## Attorney Profiles

- [Attorney Name], [Title]: [URL/attorneys/name]
- [Attorney Name], [Title]: [URL/attorneys/name]

## Social and Entity Links

- LinkedIn: [URL]
- Avvo: [URL]
- Martindale-Hubbell: [URL]
- FindLaw: [URL]
```

---

## CMS Implementation Quick Reference

| Platform | Method | File Location |
|---|---|---|
| WordPress | FTP/SFTP upload to root | /public_html/llms.txt |
| WordPress | Plugin (e.g., Yoast custom files) | Managed by plugin |
| Shopify | Settings > Files upload | Served at /llms.txt automatically |
| Squarespace | Not directly supported | Use custom code injection workaround |
| Webflow | Upload to Assets, add redirect rule | /llms.txt via redirect |
| Hugo | Place in /static directory | Auto-served at root |
| Jekyll | Place in root directory | Auto-served at root |
| Next.js | Place in /public directory | Auto-served at root |
| Custom server | Upload to web root | /var/www/html/llms.txt or equivalent |

---

## AI Systems That Support llms.txt

Adoption is evolving. As of early 2026:

| System | llms.txt Support |
|---|---|
| Perplexity | Reported to read llms.txt when crawling |
| Claude (Anthropic) | Anthropic has indicated awareness of the standard |
| ChatGPT / OpenAI | Not confirmed |
| Gemini / Google | Not confirmed — Google uses its own crawl signals |
| You.com | Reported to support |
| Bing / Copilot | Not confirmed |

**Important note:** Even where formal support is not confirmed, a well-written llms.txt signals GEO sophistication and provides accurate entity information to any AI system that reads it during crawling.

---

## Validation Checklist

Before publishing your llms.txt:

- [ ] File is named exactly `llms.txt` (lowercase)
- [ ] File is accessible at yourdomain.com/llms.txt without redirect
- [ ] Description section is specific, accurate, and entity-rich
- [ ] All URLs listed are live and return 200 status
- [ ] No marketing language — written for AI, not humans
- [ ] Organization details match schema on the website
- [ ] Social/entity links match sameAs in Organization schema
- [ ] File returns as plain text (Content-Type: text/plain)
