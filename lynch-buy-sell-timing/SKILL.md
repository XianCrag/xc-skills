---
name: lynch-buy-sell-timing
description: Judges whether now is a good time to buy or to sell a specific stock, using Peter Lynch's rules from One Up on Wall Street, Chapter 17 "The Best Time to Buy and Sell". Checks the two bargain windows for buying (year-end tax selling and market collapses) and the category-specific sell signals (slow grower, stalwart, cyclical, fast grower, turnaround, asset play). Use when the user asks "is it a good time to buy X", "should I sell X", "when should I sell", "have I held too long", "should I take profits", or mentions buy/sell timing with Peter Lynch.
---

# Lynch Buy/Sell Timing

Source: Peter Lynch, *One Up on Wall Street*, Chapter 17 "The Best Time to Buy and Sell".

Core idea: Lynch is not a market timer. Buy when you're convinced you've found solid merchandise at a good price; sell when the reason you bought no longer holds, or when another company has a better story. Ignore macro forecasts and market noise unless a specific business will clearly be affected in a specific way.

## Workflow

1. **Determine the question**: buy, sell, or both (for a current holding, evaluate the sell side first).
2. **Gather data** for the ticker: price and recent drawdown, current and historical P/E, industry P/E, earnings growth rate (past and projected), net cash per share, debt trend, inventories vs. sales, insider transactions, institutional ownership, analyst coverage, and anything category-specific listed below. Mark missing data as `unknown`; don't guess.
3. **Restate the original story**: why own (or would you own) this stock? For a holding, ask the user for their purchase reason if it isn't known, because "if you know why you bought a stock in the first place, you'll automatically have a better idea of when to say good-bye to it."
4. **Classify** the company with the `lynch-stock-categories` skill (slow grower, stalwart, cyclical, fast grower, turnaround, asset play). If it has changed category (most often a finished turnaround), reclassify it and judge it by the new category's sell rules.
5. **Run the buy check and/or the sell check** below.
6. **Filter out noise** using the "Bad reasons" list.
7. **Report** using the output template.

## Buy check

Prerequisite: the stock is already one you'd want to own (the fundamentals and story hold up; use the `lynch-stock-checklist` skill if that hasn't been checked). Timing only finds a better price for a good company; it never makes a bad company worth buying.

- [ ] **Good merchandise at a good price**: price is reasonable for the fundamentals (for example, P/E at or below its own history and industry, P/E at or below the growth rate for growers). This is the real buy signal; the windows below just make it more likely.
- [ ] **Bargain window 1, year-end tax selling (October–December)**: individuals harvest tax losses and institutions dump losers to tidy portfolios before evaluations. Low-priced issues get hit hardest: under about $6/share, stocks stop counting as margin collateral and some institutions can't hold them, so selling begets more selling. Is the stock down in this window for reasons unrelated to the business?
- [ ] **Bargain window 2, market collapse**: during broad sell-offs ("collapses, drops, burps, hiccups, and freefalls" every few years), healthy, profitable companies get dragged down with everything else. Has the stock fallen with the market while its earnings, cash, and outlook are intact?
- [ ] **Downside floor**: does net cash per share cover much of the price? (Dreyfus in 1987: stock at $16 with $15 net cash, so very little risk.)
- [ ] **Crisis beneficiary**: does the company actually benefit from the panic? (Dreyfus gained as investors moved into its money-market funds.)

Buy verdict:
- **Good time to buy**: good company, good price, and ideally inside a bargain window.
- **Fair**: good company at a fair price outside a window; buying is fine if convinced, or put it on a wish list with a target price for the next window.
- **Not now**: price is too high, the story is weak, or the decline reflects a real deterioration in the business.

## Sell check

### General rules (every category)

- [ ] **Is the original story still intact, or better?** If yes, the default is to hold. Before selling a winner, review why you bought it.
- [ ] **Is there a better story elsewhere?** Nine times out of ten Lynch sells because company 380 has a better story than company 212, especially when 212's story begins to sound unlikely.
- [ ] **Is a specific external factor clearly hitting this specific business?** Only then do macro conditions count (falling oil hurts oil-service companies, not drug makers; a falling dollar hurt foreign automakers that sold heavily in the U.S.).

### Slow grower

Sell after a 30–50% gain, or when the fundamentals have deteriorated even if the price has already fallen. Other signs:
- [ ] Lost market share two years running and is hiring a new ad agency.
- [ ] No new products; R&D cut; resting on its laurels.
- [ ] Two recent unrelated acquisitions look like diworseifications, and it's looking for more "at the leading edge of technology."
- [ ] Overpaid for acquisitions: balance sheet went from no debt and lots of cash to no cash and lots of debt, leaving no funds for buybacks even if the price falls sharply.
- [ ] Even at a lower price, the dividend yield won't be high enough to attract investors.

### Stalwart

Rotate: sell when the price rises above the earnings line or the P/E strays too far above its normal range, then buy it back lower or buy another stalwart. Don't expect a quick tenbagger. Other signs:
- [ ] New products from the last two years had mixed results; others are a year or more from market.
- [ ] P/E noticeably above similar-quality peers (for example, 15 vs. 11–12).
- [ ] No officers or directors bought shares in the last year.
- [ ] A major division (about 25% of earnings) is exposed to a slump that's already happening (housing starts, oil drilling, etc.).
- [ ] Growth is slowing and profits are being kept up by cost cuts, with limited room for more.

### Cyclical

Best time to sell is near the end of the cycle; prices often fall before earnings do (General Dynamics once fell 50% on higher earnings). Otherwise sell when something has actually started to go wrong:
- [ ] Costs are rising.
- [ ] Plants are at full capacity and the company is spending to add capacity.
- [ ] **Inventories building up** that can't be moved ("when the parking lot is full of ingots... you may be a little late").
- [ ] **Commodity prices falling**: they usually turn down several months before earnings.
- [ ] **Futures price below spot price.**
- [ ] New competitors entering, forcing price cuts across the industry.
- [ ] Two key union contracts expire within twelve months and labor wants full restoration of past concessions.
- [ ] Final demand for the product is slowing.
- [ ] Capital spending budget doubled to build a fancy new plant rather than cheaply modernizing old ones.
- [ ] Tried to cut costs but still can't compete with foreign producers.

Note: in a cyclical the P/E shrinks near the top of the cycle, so a low P/E is not a reason to hold.

### Fast grower

Don't lose the potential tenbagger, but watch for the end of the rapid-growth phase. If earnings shrink, the bid-up P/E shrinks too: an expensive double whammy. Signs:
- [ ] Expansion is ending: stopped opening new stores or entering new markets, old locations look shabby, product is out of fashion. Nowhere left to expand ("Where else could they expand? Mars?").
- [ ] Wall Street love-fest: dozens of analysts rate it a top buy, about 60%+ institutional ownership, the CEO is featured in national magazines.
- [ ] P/E at absurd levels for the company's size (P/E of 40–50 for a large company).
- [ ] Same-store sales are down (for example, -3% last quarter).
- [ ] New store or new market results are disappointing.
- [ ] Top executives and key employees leave for a rival.
- [ ] The company just did a "dog and pony" roadshow, pitching an extremely positive story to institutions.
- [ ] P/E far above the most optimistic growth projections (for example, P/E 30 vs. 15–20% projected growth).
- [ ] It now has traits from "Stocks I'd Avoid" (see the `lynch-stocks-to-avoid` skill); those are also traits of a stock to sell.

### Turnaround

Best time to sell is after it has turned around: troubles are over, everybody knows it, and shareholders aren't embarrassed to own it. Then **reclassify** it (growth company, cyclical, utility, etc.) and judge it by that category's rules. If you specialize in turnarounds, sell and find the next one. (Chrysler was a turnaround at $2–$10, but at $48 it was just a cyclical automaker.) Other signs:
- [ ] Debt had been falling for several quarters and just rose.
- [ ] Inventories rising about twice as fast as sales.
- [ ] P/E inflated relative to earnings prospects.
- [ ] Strongest division sells about half its output to one customer, and that customer's sales are slowing.

### Asset play

Hold while waiting for a raider or catalyst (activist, acquirer, large investor building a stake), as long as the company isn't going on a debt binge that erodes the assets. Don't sell before the catalyst shows up; after that a takeover, bidding war, or buyout may double or triple the price. Sell signs:
- [ ] Shares trade below real asset value, yet management plans to issue about 10% more shares to fund diversification.
- [ ] An asset sale brought much less than expected (a division expected to fetch $20M sold for $12M).
- [ ] A tax or regulatory change reduces the value of a key asset (for example, a lower corporate tax rate shrinking the value of tax-loss carryforwards).
- [ ] Institutional ownership has climbed sharply (for example, 25% to 60% over five years): the hidden value is no longer hidden.
- [ ] New debt being piled on, reducing what's left for shareholders.

## Bad reasons (don't let these drive the decision)

- **Technical chatter**: "the stock is extremely extended." Lynch sold Warner at $38 on this nagging thought; it went past $180.
- **"Take profits" / "don't be greedy"**: if the story is intact and getting better, a fivebagger can become a 25-bagger (Toys "R" Us sold at $5, went to $25). Brokers earn commission on both sides of a switch.
- **An outsider stopped buying**: Lynch sold Toys "R" Us when Milton Petrie stopped buying; irrelevant to the business.
- **A takeover that didn't happen**: selling Flowers and Lance out of boredom waiting for a takeover. A profitable company staying independent is fine.
- **A single insider selling** (as a reason not to buy): insiders sell for many personal reasons (La Quinta). Insider *buying* is the meaningful signal.
- **The drumbeat effect**: repeated macro scare stories (money supply, Fed rates, deficits, oil up or down, dollar strong or weak) that don't specifically affect this company.
- **Fear during a market drop**: that's usually when to buy, not sell, if the company is healthy.

Note: it's usually harder to stick with a winner after the price rises than to believe in it after it falls. Guard against selling winners too early.

## Output template

```markdown
# [TICKER]: Lynch Buy/Sell Timing

**Question:** [Buy / Sell / Both]
**Story:** [why own it, what must keep happening]
**Category:** [category] (reclassified from: [if a turnaround has finished, etc.])

## Buy check
| Item | Finding | Signal |
|------|---------|--------|
| Good merchandise at a good price | ... | ✅ / ⚠️ / ❌ / ❓ |
| Year-end tax-selling window | ... | ... |
| Market-collapse window | ... | ... |
| Net cash floor | ... | ... |
| Crisis beneficiary | ... | ... |

## Sell check
| Item | Finding | Signal |
|------|---------|--------|
| Original story intact? | ... | ... |
| Better story elsewhere? | ... | ... |
| Specific external hit? | ... | ... |
| [category-specific signs that apply] | ... | ... |

## Noise to ignore
- [any bad reasons present in the user's question or recent news, or "None"]

## Verdict
- **Buy:** [Good time / Fair / Not now] with a one-line reason.
- **Sell:** [Hold / Consider trimming or rotating / Sell] with a one-line reason.
- **Watch:** the one or two signals that would change the verdict.
```

Signal legend: ✅ favorable for the action in question, ⚠️ caution, ❌ unfavorable, ❓ unknown (data missing).

## Notes

- Tie the verdict to the checks; this is a research aid, not financial advice.
- Dollar figures and percentages in the signs are Lynch's examples; apply them proportionally rather than as hard thresholds.
- If key data is missing, list which items are `unknown` and what data would resolve them.
