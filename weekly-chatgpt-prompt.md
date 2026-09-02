# Weekly ChatGPT Research Prompt

Use this prompt once per week in a browsing-enabled ChatGPT conversation. Replace the bracketed values before running it.

---

## Prompt

You are producing the weekly **SSS Space 5**, a transparent research watchlist of five publicly traded space companies.

**Research cutoff:** [YYYY-MM-DD HH:MM TIME ZONE]  
**Week of:** [YYYY-MM-DD]  
**Prior ranking file:** [paste or attach the prior dated ranking, if one exists]  
**Current company universe:** [paste or attach `data/companies.csv`]

Follow `methodology.md`, `sources/source_policy.md`, and `disclaimer.md` exactly.

### Objective

Rank the five strongest eligible public space companies under the published SSS methodology. This is a watchlist-quality assessment, not a forecast of stock returns. Do not call any company a buy, sell, or hold.

### Research rules

1. Browse the web and use current information available by the research cutoff.
2. Prefer primary sources: regulatory filings, official earnings materials, government award records, mission records, and technical documentation.
3. Cite a direct URL and publication date for every material factual claim.
4. Distinguish funded backlog from contract ceilings, options, memoranda, and promotional headline values.
5. Never invent a number, source, quote, ticker, contract value, or technical milestone.
6. If a material fact cannot be verified, label it unavailable. If the gap could change the ranking, mark the company ineligible rather than filling it with an assumption.
7. Score each category independently of the prior ranking. Use five-point increments unless finer precision is explicitly justified.
8. Keep private companies out of the public-company top five.
9. Do not use employer-confidential, customer-confidential, classified, controlled, proprietary, procurement-sensitive, or export-controlled information.
10. Disclose material conflicts or relationships found in public sources. Do not give SSS preferential treatment.

### Required analysis

For every eligible candidate, provide:

- Company, ticker, exchange, and primary space segment.
- Space relevance score (20%).
- Revenue / backlog strength score (20%).
- Technical moat score (20%).
- Growth trajectory score (15%).
- Financial durability score (15%).
- Strategic importance score (10%).
- Weighted SSS Score, calculated exactly and rounded to one decimal place.
- Evidence confidence: high, medium, or low.
- A one-sentence thesis and one-sentence main risk.
- Direct source URLs supporting the material facts.

### Quality-control pass

Before answering:

- Recalculate every composite score.
- Confirm the displayed order uses unrounded scores.
- Confirm every top-five company is eligible and has at least medium confidence.
- Check all dates, tickers, exchange names, units, and period comparisons.
- Identify any ranking change driven mostly by a judgment call rather than new evidence.
- Remove unsupported claims and false precision.

### Return exactly four sections

#### 1. Research log

State the cutoff, candidates reviewed, exclusions with reasons, and material source gaps.

#### 2. Dated ranking Markdown

Return a complete file for `rankings/[WEEK_OF].md` with:

- Research cutoff.
- Top-five table: rank, company, ticker, SSS Score, confidence, thesis, main risk.
- Category-score table for the five ranked companies.
- Source notes with direct links.
- Changes from the prior week.
- The standard research-only disclaimer.

#### 3. CSV rows

Return append-ready rows for `data/scores_weekly.csv` using its existing header and pipe-separated source URLs.

#### 4. Changelog entry

Return one concise dated entry describing the published ranking and any methodology or data changes.

If the evidence is insufficient for a defensible top five, say so and return no ranking rather than lowering the standard.

---

Human review is required before committing any weekly output. Verify sources, calculations, eligibility, and compliance boundaries directly.
