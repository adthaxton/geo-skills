# geo-skills

Open-source GEO (Generative Engine Optimization) skill frameworks for SEO practitioners and AI search strategists. Structured frameworks, platform benchmarks, diagnostic decision trees, and worked examples for optimizing brand visibility across LLMs and AI search interfaces.

Built by a practitioner who started tracking LLM citations manually before dedicated tools existed.

---

## What This Is

Each skill in this library covers one core area of GEO strategy. Every skill ships three files:

| File | Contents |
|---|---|
| `SKILL.md` | The framework — diagnostic process, decision trees, checklists, and methodology |
| `REFERENCE.md` | Benchmarks, platform behavior data, and reference tables |
| `EXAMPLES.md` | Worked examples with realistic scenarios and expected outputs |

Use these with any AI tool — Claude, ChatGPT, Gemini, Perplexity — or as standalone reference frameworks for your own GEO practice.

---

## Skills

| Skill | What It Covers |
|---|---|
| [`geo-citation-audit`](skills/geo-citation-audit/) | Full framework for auditing brand citation presence across LLM platforms — prompt construction, citation tracking, share of voice, gap analysis, and reporting |
| [`ai-overview-optimization`](skills/ai-overview-optimization/) | Strategies for appearing in Google AI Overviews — content structure, schema signals, and query targeting |
| [`schema-for-geo`](skills/schema-for-geo/) | Structured data decisions specifically for LLM discoverability — which schema types matter, how to implement them, and how to validate |
| [`multi-location-geo`](skills/multi-location-geo/) | GEO strategy for businesses with multiple locations — GBP signals, location page structure, and local citation in AI responses |
| [`eeat-signal-audit`](skills/eeat-signal-audit/) | E-E-A-T evaluation framework specific to AI search contexts — what signals LLMs use to assess credibility and how to strengthen them |
| [`llms-txt-generator`](skills/llms-txt-generator/) | Framework and templates for implementing llms.txt — the emerging standard for helping AI crawlers understand your site |

---

## Quick Start

**Option 1: Use as AI tool context**

Copy the contents of any `SKILL.md` into your AI tool's system prompt or context window. Then ask it to apply the framework to your client or site.

**Option 2: Use as a standalone reference**

Read the skill files directly as practitioner frameworks. Each one is written to be usable without any AI tooling.

**Option 3: Combine with the Python tools**

Pair these skill frameworks with the [`llm-citation-tracker`](https://github.com/adthaxton/llm-citation-tracker) repo for automated citation data collection.

---

## Related Tools

The [`llm-citation-tracker`](https://github.com/adthaxton/llm-citation-tracker) repo contains Python scripts that automate the data collection side of GEO auditing:

- `citation_tracker.py` — track brand citations across a fixed prompt set
- `prompt_variation_tester.py` — auto-generate and test prompt variations for any brand and topic
- `geo_content_auditor.py` — scrape and score any URL against a GEO readiness checklist

Use the skill frameworks here to interpret and act on the data those tools collect.

---

## Prompts Folder

The [`prompts/`](prompts/) folder contains a curated collection of GEO audit prompts ready to copy and paste into any AI platform.

---

## Author

Angie Thaxton — Senior SEO Strategist specializing in GEO and AI search visibility  
[linkedin.com/in/adthaxton](https://linkedin.com/in/adthaxton) | [myainotes.com](https://myainotes.com) | [llm-citation-tracker](https://github.com/adthaxton/llm-citation-tracker)

---

## License

MIT — use freely, attribution appreciated.
# geo-skills
