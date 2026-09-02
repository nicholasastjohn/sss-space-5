# SSS Space 5 Methodology

Version 0.1 — 2026-09-01

## Objective

SSS Space 5 identifies five publicly traded companies that currently show the strongest combination of direct space exposure, demonstrated demand, defensible capability, execution momentum, financial durability, and strategic importance.

The score measures **watchlist quality under this framework**, not expected stock return. It deliberately does not estimate intrinsic value or price upside.

## Eligible universe

A company is eligible for the ranked list only when all of the following are true:

1. Its common equity is publicly traded on a recognized exchange and is reasonably accessible to ordinary investors.
2. Space-related activity is economically material or strategically central to the company.
3. Current public evidence exists for every scoring category.
4. The evidence packet includes at least one primary financial source and one primary operating or technical source dated or reviewed within the current research window.
5. The company is not included solely because of narrative attention, expected future listing, or an undisclosed relationship.

Private companies may be tracked separately but cannot enter the ranked top five. Diversified primes may qualify, but their space exposure must be scored conservatively when segment disclosure is limited.

## Formula

Every category is scored from 0 to 100. The composite score is rounded to one decimal place.

```text
SSS Score =
  0.20 × Space relevance
+ 0.20 × Revenue / backlog strength
+ 0.20 × Technical moat
+ 0.15 × Growth trajectory
+ 0.15 × Financial durability
+ 0.10 × Strategic importance
```

The displayed rank is determined by the unrounded composite score. Ties are broken, in order, by financial durability, revenue/backlog strength, and evidence confidence.

## Common score anchors

Use these anchors across all six categories. Intermediate scores require evidence proportionate to their precision.

| Score | Interpretation |
|---:|---|
| 0 | No credible positive evidence, or evidence is directly adverse |
| 25 | Weak, early, or mostly unproven |
| 50 | Mixed or average; material strengths and weaknesses |
| 75 | Strong, demonstrated, and supported by current evidence |
| 100 | Exceptional, durable, and supported by multiple high-quality sources |

Scores should normally use five-point increments. Use a more precise score only when the evidence clearly supports it.

## Category rules

### 1. Space relevance — 20%

Consider the share of revenue, backlog, assets, technical roadmap, and enterprise identity directly tied to launch, spacecraft, satellite services, Earth observation, in-space infrastructure, space-qualified components, or other space systems.

- Score pure-play companies highest.
- Discount diversified firms when space is a small or opaque segment.
- Do not equate defense exposure generally with space relevance.

### 2. Revenue / backlog strength — 20%

Consider reported revenue, funded backlog, contract quality, customer concentration, repeat demand, award convertibility, and evidence that orders become recognized revenue.

- Prefer filed or audited figures.
- Distinguish funded backlog from indefinite-delivery ceilings, options, memoranda, and press-release headline values.
- Discount revenue that is unusually concentrated, nonrecurring, or dependent on unresolved milestones.

### 3. Technical moat — 20%

Consider flight heritage, qualification barriers, intellectual property, manufacturing learning curves, infrastructure, proprietary data, switching costs, regulatory position, and integration depth.

- Reward demonstrated performance over roadmap claims.
- Treat patents and first-mover status as inputs, not proof of a moat.
- Separate technical difficulty from commercial defensibility.

### 4. Growth trajectory — 15%

Consider year-over-year revenue growth, backlog conversion, launches or deployments, customer additions, capacity expansion, milestone reliability, and the direction of execution quality.

- Use comparable periods and disclose one-time effects.
- Penalize repeated schedule slips, mission failures, customer losses, or growth purchased without durable economics.

### 5. Financial durability — 15%

Consider cash and equivalents, operating cash use, debt, near-term maturities, gross margin, credible profitability path, capital intensity, and dilution risk.

- Runway estimates must state the method and source period.
- Do not treat access to capital as equivalent to financial strength.
- Score conservatively when liquidity depends on repeated equity issuance or uncertain financing.

### 6. Strategic importance — 10%

Consider the company’s importance to resilient communications, navigation, sensing, launch access, national security, infrastructure, autonomy, power, logistics, or other bottlenecks in a durable space economy.

- Reward enabling infrastructure and hard bottlenecks.
- Do not substitute geopolitical rhetoric for demonstrated operational relevance.

## Evidence confidence

Assign one confidence label to each company-week:

- **High:** all material claims are supported by current primary sources, with limited ambiguity.
- **Medium:** evidence is credible but one or more material figures require estimation or secondary corroboration.
- **Low:** material evidence is missing, stale, contradictory, or mostly promotional. A low-confidence company is not eligible for the published top five.

Missing data is not scored as zero unless zero is itself supported by evidence. If missing information could materially change the result, mark the company ineligible for that week.

## Weekly change protocol

1. Freeze the research cutoff time and record it in the ranking file.
2. Update the company universe before scoring.
3. Capture source URLs and publication dates.
4. Score independently from the prior rank, then compare with the previous week.
5. Explain any composite move of 5.0 points or more and every entry into or exit from the top five.
6. Append one row per company to `data/scores_weekly.csv`.
7. Create a new dated file under `rankings/` and update `CHANGELOG.md`.
8. Preserve prior records. Corrections must state what changed and why.

## CSV conventions

- Dates use ISO 8601 format: `YYYY-MM-DD`.
- Scores are numeric from 0 through 100.
- `sss_score` is the calculated weighted composite rounded to one decimal place.
- `rank` is blank for companies outside the top five.
- Multiple source URLs in one field are separated with `|`.
- Free-text fields must be quoted when they contain commas.
- `eligible` is `true` or `false`; `confidence` is `high`, `medium`, or `low`.

## Known limitation

The framework assesses company and strategic quality, not whether the current security price offers an attractive expected return. Valuation, liquidity, volatility, taxes, portfolio fit, and investor circumstances sit outside the model. The output is therefore a research watchlist, not an investment recommendation.
