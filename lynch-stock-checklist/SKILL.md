---
name: lynch-stock-checklist
description: Evaluates a single stock against Peter Lynch's "Final Checklist" (One Up on Wall Street, Chapter 15). Classifies the company into one of six categories (slow grower, stalwart, cyclical, fast grower, turnaround, asset play) and checks the category-specific fundamentals. Use when the user asks to analyze, screen, vet, or review a stock or ticker, asks "should I buy X", or mentions Peter Lynch, a stock checklist, or the six stock categories.
---

# Lynch Stock Checklist

Source: Peter Lynch, *One Up on Wall Street*, Chapter 15 "The Final Checklist".

## Workflow

1. **Gather data** for the ticker: P/E (current and historical), industry P/E, earnings history (5–10 years), revenue mix by product or segment, debt-to-equity, net cash, dividend history and payout ratio, institutional ownership, insider transactions, buybacks, share count trend. Use tools or data the user provides; mark anything unavailable as `unknown` instead of guessing.
2. **Write the story** in 2–3 sentences: why would someone own this, and what has to happen for it to work? "It is really going up!" doesn't count.
3. **Classify** the company with the `lynch-stock-categories` skill: one primary category (slow grower, stalwart, cyclical, fast grower, turnaround, asset play), plus a secondary category if one applies (for example, a turnaround that is also an asset play).
4. **Run the general checklist**, then the checklist for each category that applies.
5. **Apply the red flags and pointers**.
6. **Report** using the output template.

## General checklist (every stock)

- [ ] **P/E ratio**: high or low for this company's own history and versus similar companies in the same industry?
- [ ] **Institutional ownership**: the lower the better.
- [ ] **Insider buying and company buybacks**: both are positive signs.
- [ ] **Earnings record**: growth to date; consistent or sporadic? (Earnings matter in every category except the asset play.)
- [ ] **Balance sheet**: strong or weak (debt-to-equity)? How is it rated for financial strength?
- [ ] **Cash position**: net cash per share acts as a floor under the stock price.

## Category checklists

### Slow growers
- [ ] Dividends have always been paid and are routinely raised.
- [ ] Payout ratio: a low percentage of earnings leaves a cushion in hard times; a high percentage makes the dividend riskier.

### Stalwarts
- [ ] Big companies that aren't likely to go out of business, so price is the key issue: does the P/E say you are paying too much?
- [ ] Possible diworseifications (acquisitions outside the core business) that may reduce future earnings.
- [ ] Long-term growth rate, and whether the same momentum has held in recent years.
- [ ] If holding long term: how did it fare in previous recessions and market drops?

### Cyclicals
- [ ] Inventories and the supply-demand relationship.
- [ ] New entrants into the market (usually a dangerous development).
- [ ] Expect the P/E to shrink as the business recovers and investors look ahead to peak earnings at the end of the cycle.
- [ ] Where are we in the cycle? The worse the slump, the better the recovery. Upturns are easier to predict than downturns.

### Fast growers
- [ ] The product expected to drive growth is a major part of the company's business, not a minor line.
- [ ] Recent earnings growth rate. Ideal is 20–25%; be wary above 25%, as 50%+ growers are usually in hot industries.
- [ ] The company has duplicated its success in more than one city or market, proving the expansion works.
- [ ] Room left to grow (one region with dozens of markets left to enter, not already everywhere).
- [ ] P/E at or near the growth rate.
- [ ] Expansion speeding up or slowing down (for example, 3 new stores then 5, versus 5 then 3). For "one-shot" sales businesses (no recurring revenue), a growth slowdown can make earnings dive, not just slow.
- [ ] Few institutions own it and only a handful of analysts follow it (a big plus).

### Turnarounds
- [ ] **Most important**: can it survive a raid by its creditors? Cash versus debt.
- [ ] Debt structure: how long can it operate in the red while fixing problems without going bankrupt?
- [ ] Dilution risk: issuing many new shares can mean the company turns around but the stock doesn't.
- [ ] If already bankrupt: what's left for shareholders?
- [ ] The turnaround mechanism: shedding unprofitable divisions (one-time write-off, then earnings jump), business coming back, cost cuts and their expected effect.

### Asset plays
- [ ] Value of the assets; any hidden assets?
- [ ] Debt that detracts from the assets (creditors are first in line).
- [ ] New debt being taken on, making the assets less valuable.
- [ ] A raider or catalyst in the wings to help shareholders realize the value.

## Red flags and pointers

Positive signals:
- Simple, dull, mundane, out-of-favor business that Wall Street hasn't noticed.
- Moderately fast grower (20–25%) in a nongrowth industry: the ideal investment.
- Has a niche.
- Small company that is already profitable and has proven its concept can be replicated.
- Consistent share buybacks; insider buying, especially several insiders at once.
- Management has a significant personal investment, not just a salary.
- Little or no institutional ownership.
- No debt (a company with no debt can't go bankrupt).

Negative signals:
- Growth rates of 50–100% a year.
- Hot stock in a hot industry.
- Diversification, which usually turns into diworseification.
- Long shot.
- Grossly overpriced P/E: even if everything else goes right, you won't make money.
- Troubled company with loads of bank debt (prefer troubled companies with superior financial positions).
- Thesis relies on stated book value alone; real value is what counts.
- Thesis relies on management's resume or speaking ability rather than the company's prospects.
- Thesis is just a tip; judge the tip separately from the tipper.

Expectations:
- Big companies have small moves; small companies have big moves. Consider company size relative to the product expected to drive profit.
- It's better to miss the first move and wait to see if the company's plans are working out.
- When in doubt, tune in later.

## Output template

```markdown
# [TICKER]: Lynch Checklist

**Story:** [2–3 sentences: why own it, what must happen]
**Category:** [primary] (secondary: [if any])

## General
| Item | Finding | Signal |
|------|---------|--------|
| P/E vs history / industry | ... | ✅ / ⚠️ / ❌ / ❓ |
| Institutional ownership | ... | ... |
| Insider buying / buybacks | ... | ... |
| Earnings record | ... | ... |
| Balance sheet | ... | ... |
| Net cash per share | ... | ... |

## [Category] checks
| Item | Finding | Signal |
|------|---------|--------|
| ... | ... | ... |

## Red flags
- [any triggered, or "None found"]

## Verdict
[Pass / Watch / Fail] with a one-line reason, plus the story line to monitor going forward.
```

Signal legend: ✅ favorable, ⚠️ caution, ❌ unfavorable, ❓ unknown (data missing).

## Notes

- Keep the verdict tied to the checklist; this is a research aid, not financial advice.
- If key data is missing, say which items are `unknown` and what would resolve them rather than filling gaps with assumptions.
