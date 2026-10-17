---
name: lynch-stocks-to-avoid
description: Tests a single stock against Peter Lynch's "Stocks I'd Avoid" (One Up on Wall Street, Chapter 9), flagging the six warning types - the hottest stock in the hottest industry, "the next" IBM/McDonald's/etc., diworseification through acquisitions, whisper stocks and longshot IPOs, the middleman dependent on one big customer, and the stock with the exciting name. Use when the user asks whether to avoid a stock, wants red flags or a Lynch Chapter 9 test, or asks if a ticker is a hot stock, a hyped IPO, a "next something", a diworseifier, or too dependent on a single customer.
---

# Lynch Stocks to Avoid

Source: Peter Lynch, *One Up on Wall Street*, Chapter 9 "Stocks I'd Avoid".

Lynch: "If I could avoid a single stock, it would be the hottest stock in the hottest industry." Hot stocks rise "out of sight of any of the known landmarks of value," and when they fall, "it's not going to fall slowly, nor is it likely to stop at the level where you jumped on." The test looks for the six warning types in the chapter. Each flag is a reason to stay away, or at least to wait until the company has a record.

## Workflow

1. **Gather data** for the ticker: what it sells, industry growth rate and how it's trending, number of competitors and recent entrants, barriers to entry (patents, niche, brand), price history (the run-up over 1–3 years), media and analyst attention, how it is marketed or described ("the next X"), acquisitions over 5–10 years (size, price paid, how related to the core business), goodwill and write-offs, buybacks and dividends versus acquisition spending, earnings and revenue history, IPO date and whether it was a spinoff, customer concentration (10-K "major customers" disclosure), any recent name change, and debt trend. Use tools or data the user provides; mark anything unavailable as `unknown` instead of guessing.
2. **Describe the business** in one plain sentence, then state the bull story you hear for it. If the story is all "sizzle" with no earnings behind it, note it.
3. **Run all six tests** below. Score each as ✅ (clear), ⚠️ (partial or emerging), ❌ (flag raised), or ❓ (unknown).
4. **Apply the exceptions**, then **report** using the output template.

## The six tests

### 1. Hottest stock in the hottest industry
Flag when the stock is the one "every investor hears about in the car pool," and the price has run far ahead of earnings or assets.
- [ ] Price has run up far faster than earnings (Home Shopping Network went from $3 to $47 and back to $3 in 16 months).
- [ ] Analysts predict double-digit growth "forever" for the whole industry (mobile homes, digital watches, HMOs, carpets, disk drives, oil services).
- [ ] Competitors are pouring in. Hot industries "attract a very smart crowd"; disk drives grew 52% a year, but with 30–35 rivals nobody made a profit. Carpets went from five or six producers to two hundred.
- [ ] No patent, niche, or brand to stop imitators ("imitation is the sincerest form of battery").
- [ ] Balance sheet getting worse (HSN took on debt to buy TV stations; Tom Brown, Inc. had "useless rigs, ... some impressive debts, and a bad balance sheet").

Contrast: Xerox controlled copying, yet lost 84% once Japan, IBM, and Kodak got into copiers. Philip Morris, in a negative-growth industry, rose from $14 to $90 because "negative-growth industries do not attract flocks of competitors."

### 2. "The next something"
Flag when the company is pitched as the next IBM, McDonald's, Intel, Disney, Toys "R" Us, or Price Club.
- [ ] Marketing, analysts, or media frame it as a copy of a famous winner. "The next of something almost never is."
- [ ] Copycat business model with no edge over the original (Circuit City's "nexts" such as Crazy Eddie and Highland Superstores lost 59–96%; Child World and Warehouse Club both stumbled).
- [ ] Also consider the original: when competitors are being called "the next X," it often marks the end of prosperity for X too (IBM).

### 3. Diworseification
Flag when a profitable company spends its cash on acquisitions instead of buybacks or dividends.
- [ ] Acquisitions are **unrelated** to the core business, or overpriced, or "completely beyond [management's] realm of understanding" (Mobil buying Marcor/Montgomery Ward; Gillette's digital watches; Genesco making 150 acquisitions in 17 years).
- [ ] Acquisitions are rapid or serial rather than one at a time, each proven before the next (Genesco's frenzy versus Melville's measured CVS → Marshall's → Kay-Bee).
- [ ] Sales grow on paper while fundamentals (margins, returns, earnings per share) deteriorate.
- [ ] Goodwill write-offs or divestitures of past acquisitions at a loss (the acquire-regret-divest cycle).
- [ ] Little or no buyback, which Lynch calls "the purest synergy of all."

Not a flag: related acquisitions with clear synergy (Marriott buying Big Boy; Gillette buying Foamy), or a company escaping a terrible core business that knows how to buy and run what it acquires (Berkshire Hathaway leaving textiles; Loews). Lynch still says "acquisitions in general make me nervous."

### 4. Whisper stock (longshot)
Flag when the story is a whiz-bang solution with no earnings: "the sizzle is so delectable that you forget to notice there's no steak."
- [ ] No earnings, so no P/E ratio, "but there's no shortage of microscopes, Ph.D.'s, high hopes, and cash from the stock sale."
- [ ] Story promises to solve the latest national problem, and the solution is "(a) very imaginative, or (b) impressively complicated" (miracle cures, energy breakthroughs "that violate the laws of physics").
- [ ] Shifting business focus year to year (KMS Industries went from photovoltaics to fusion to immunoassays and fell from $40 to $2).
- [ ] Pitched as too small or too early for the professionals, and pressure to buy now or miss out.
- [ ] **IPO of a brand-new enterprise** with no track record: "three out of four have been long-term disappointments." Spinoffs or IPOs of established businesses (Toys "R" Us, Safety-Kleen) are fine because they can be researched like any other company.

Lynch's remedy: "Wait for the earnings ... When in doubt, tune in later."

### 5. The middleman
Flag when the company depends on one or a few big customers.
- [ ] A single customer accounts for **25–50%** of sales (SCI Systems selling to IBM). Treat 10–25% as ⚠️.
- [ ] Losing that customer would be catastrophic, or the customer could make the part itself (Tandon and other disk-drive makers depended on a few clients).
- [ ] The customer has the leverage to squeeze prices and margins. "It's rare that a great investment could result from such an arrangement."

### 6. The exciting name
Flag when a flashy name gives a mediocre company "a false sense of security."
- [ ] Name uses "advanced," "leading," "micro," an x, a buzzword of the moment, or a mystifying acronym.
- [ ] Recent rebrand to sound trendy (UAL renaming itself Allegis).
- [ ] The name draws more attention than the fundamentals justify. Contrast: Crown, Cork & Seal kept its dull name.

This test is weak on its own. Use it to explain excess attention, not as a reason by itself to avoid a sound company.

## Verdict rules

- **Avoid**: test 1 (hottest stock) or test 4 (whisper stock) is ❌, or two or more tests are ❌.
- **Caution**: exactly one ❌ among tests 2, 3, 5, or 6, or two or more ⚠️. Name what to watch.
- **Clear**: no ❌ and at most one ⚠️. Clear only means none of the Chapter 9 warning types apply; it isn't a buy signal.

Many ❓ items make any verdict weak. Say so and name what data would settle it.

## Exceptions

- A former hot stock that has already collapsed may now be a turnaround (Lynch rebought Apple only after it "collapsed and became a turnaround"). Reclassify it with `lynch-stock-categories` and judge it on the turnaround checks in `lynch-stock-checklist`, not on test 1.
- Victims of diworseification that are now restructuring, and companies being acquired by a diworseifier, can be opportunities. Flag test 3 only for the acquirer that is still on a buying spree.
- A "next something" or whisper company that has since built a real earnings record should be judged on that record.

## Output template

```markdown
# [TICKER]: Lynch Stocks-to-Avoid Test

**Business in one sentence:** [plain description]
**The bull story:** [what the crowd says]

| # | Test | Finding | Signal |
|---|------|---------|--------|
| 1 | Hottest stock in hottest industry | [run-up, industry growth, # competitors, moat] | ✅ / ⚠️ / ❌ / ❓ |
| 2 | "The next something" | [how it's pitched] | ... |
| 3 | Diworseification | [acquisitions, relatedness, write-offs, buybacks] | ... |
| 4 | Whisper stock / longshot IPO | [earnings, track record, IPO age] | ... |
| 5 | Middleman | [top customer % of sales] | ... |
| 6 | Exciting name | [name, any rebrand] | ... |

## Flags raised
- [each ❌ / ⚠️ with the evidence, or "None found"]

## Verdict
[Avoid / Caution / Clear] with a one-line reason and what would change it (for example, earnings established, customer concentration falling, acquisition spree ending).
```

Signal legend: ✅ clear of the warning, ⚠️ partial or emerging, ❌ warning present, ❓ unknown (data missing).

## Notes

- This test only screens for what to avoid. Pair it with `lynch-perfect-stock` (Chapter 8, favorable attributes) and `lynch-stock-checklist` (Chapter 15, category fundamentals) for a full view.
- Keep the verdict tied to the six tests; this is a research aid, not financial advice.
- If key data is missing, list which tests are `unknown` and what would resolve them rather than filling gaps with assumptions.
