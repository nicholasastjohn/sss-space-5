# SSS Space 5

**The weekly top-five public space-company watchlist based on transparent metrics.**

SSS Space 5 is a public, versioned research artifact from St. John Space Solutions. It scores listed space companies using a repeatable 0–100 framework covering space relevance, demand, technical moat, growth, financial durability, and strategic importance.

> **Launch status:** The research system is live. The first ranking is intentionally left unfilled until a separate, source-backed research pass is complete.

## What this is

- A weekly research watchlist of five publicly traded space companies.
- A transparent scoring model with dated evidence and an audit trail.
- A way to track how new filings, contracts, technical milestones, and balance-sheet changes affect a company’s standing.
- An early space-economy intelligence product from St. John Space Solutions (SSS).

## What this is not

- Financial, investment, legal, tax, or accounting advice.
- A valuation model, price target, trading signal, or recommendation to buy, sell, or hold a security.
- A ranking of private companies alongside public securities.
- A vehicle for employer-confidential, customer-confidential, proprietary, classified, controlled, procurement-sensitive, or export-controlled information.

## Scoring model

Each eligible company receives six category scores from 0 to 100.

| Category | Weight | Question |
|---|---:|---|
| Space relevance | 20% | How directly does enterprise value depend on the space economy? |
| Revenue / backlog strength | 20% | How strong and credible is demonstrated demand? |
| Technical moat | 20% | How difficult are the company’s capabilities to reproduce? |
| Growth trajectory | 15% | Are revenue, deployments, customers, and execution improving? |
| Financial durability | 15% | Can the company fund execution without disproportionate balance-sheet or dilution risk? |
| Strategic importance | 10% | How important is the company to resilient, long-duration space infrastructure? |

```text
SSS Score =
  0.20 × Space relevance
+ 0.20 × Revenue / backlog strength
+ 0.20 × Technical moat
+ 0.15 × Growth trajectory
+ 0.15 × Financial durability
+ 0.10 × Strategic importance
```

Read the complete rules in [methodology.md](methodology.md).

## Weekly workflow

1. Define the week-ending date and eligible public-company universe.
2. Collect current primary sources: regulatory filings, earnings materials, official contract records, and dated technical evidence.
3. Record evidence and score every category. Do not infer missing facts.
4. Apply the formula, run eligibility checks, and rank the five highest-scoring companies.
5. Publish the dated ranking, append the score history, and record material changes in the changelog.
6. Preserve the prior week. Never silently rewrite historical rankings.

The reusable workflow is in [weekly-chatgpt-prompt.md](weekly-chatgpt-prompt.md).

## Repository map

```text
README.md                    Project overview and operating rules
methodology.md               Eligibility, scoring, and ranking methodology
weekly-chatgpt-prompt.md     Reusable weekly research prompt
disclaimer.md                Research and compliance boundaries
data/companies.csv           Company-universe template
data/scores_weekly.csv       Append-only weekly score template
rankings/2026-09-01.md       Initial placeholder ranking
sources/source_policy.md     Evidence hierarchy and citation rules
website/index.html           Single-page landing page
CHANGELOG.md                 Version history
```

## Integrity rules

- A company cannot rank without current, citable evidence for all six categories.
- Material uncertainty lowers confidence; it does not justify invented precision.
- Private companies may appear only in a separately labeled watchlist and never in the public-company top five.
- SSS is the analyst/operator behind the artifact. It does not receive special treatment and is not eligible for the public-company ranking unless it independently satisfies the same published rules.
- Historical files remain immutable except for clearly labeled factual corrections.

See [disclaimer.md](disclaimer.md) before using this research.
