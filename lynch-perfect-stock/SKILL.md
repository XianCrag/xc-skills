---
name: lynch-perfect-stock
description: Scores a single stock against Peter Lynch's thirteen attributes of the "perfect stock" (One Up on Wall Street, Chapter 8 "The Perfect Stock, What a Deal!"), such as a dull name, a disagreeable or no-growth business, a niche, repeat purchases, spinoff status, low institutional ownership, insider buying, and share buybacks. Use when the user asks whether a stock is a "perfect stock", wants a Lynch Chapter 8 or thirteen-attribute test, or asks how boring, overlooked, or niche a company is.
---

# Lynch Perfect Stock Test

Source: Peter Lynch, *One Up on Wall Street*, Chapter 8 "The Perfect Stock, What a Deal!".

Lynch: "You never find the perfect company, but if you can imagine it, then you'll know how to recognize favorable attributes." The test measures how many of those attributes a company has. A high score points to a company Wall Street is likely to overlook. It does not mean the stock is cheap or that the business is sound.

## Workflow

1. **Gather data** for the ticker: company name, what it actually sells and to whom, industry growth rate, competitors and market share, corporate history (spinoff or parent), institutional ownership %, number of analysts covering it, insider transactions (Form 4) for the last 6–12 months, share count trend over 5+ years, buyback programs, and any reputational baggage. Use tools or data the user provides; mark anything unavailable as `unknown` instead of guessing.
2. **Describe the business** in one plain sentence, the way a customer would. If you can't, that already counts against attribute 1 (simple business).
3. **Score all 13 attributes** below as ✅ (has it), ⚠️ (partial), ❌ (doesn't have it), or ❓ (unknown).
4. **Run the sanity checks** (earnings, debt, price) and the overrides.
5. **Report** using the output template.

## The thirteen attributes

| # | Attribute | ✅ when | ❌ when |
|---|-----------|---------|---------|
| 1 | **It sounds dull, or even better, ridiculous** | Boring or silly name nobody brags about at a cocktail party (Pep Boys—Manny, Moe, and Jack; Bob Evans Farms) | Trendy, high-tech-sounding name (the "GeneSplice International" type) |
| 2 | **It does something dull** | Mundane product or service (bottle caps, coupon processing, replacement rental cars) | Glamorous product the press loves to cover |
| 3 | **It does something disagreeable** | Makes people shrug, retch, or turn away (degreasing auto parts, sludge, grease traps) | Pleasant, aspirational business |
| 4 | **It's a spinoff** | Recently spun off from a parent; parent literature understated; institutions dismissed the shares as found money. Stronger if new insiders buy 1–2 months after the spinoff | Not a spinoff (neutral: score ❌ without penalty) |
| 5 | **Institutions don't own it, analysts don't follow it** | Little or no institutional ownership; few or no analysts. Also counts: once-popular stock the professionals have abandoned | Heavy institutional ownership (for example, SCI over 50%) and broad analyst coverage |
| 6 | **The rumors abound: toxic waste and/or the Mafia** | Unfounded stigma or rumor keeps respectable investors away (waste management, casinos before Holiday Inn and Hilton entered) | No stigma; or the rumor is *true* and material (that's a real risk, not an attribute) |
| 7 | **There's something depressing about it** | Subject people avoid thinking about (funerals, SCI) | Upbeat subject |
| 8 | **It's a no-growth industry** | Industry grows ~0–3% a year, so no rivals want in and the company can keep gaining share | Hot, high-growth industry where "a thousand MIT graduates" are trying to make it cheaper |
| 9 | **It's got a niche** | Exclusive franchise: local geographic monopoly (rock pits, only daily paper in town), patents or regulatory approvals (drugs, pesticides), dominant brand (almost as good as a niche) | Competes head-on with many rivals (movie studios, jewelers, textile mills) |
| 10 | **People have to keep buying it** | Consumable, repeat purchase (drugs, soft drinks, razor blades, cigarettes) | One-time or fad purchase (the toy everybody has to have this year) |
| 11 | **It's a user of technology** | Benefits from falling tech prices by using tech to cut its own costs (payroll processor using cheaper computers, supermarket installing scanners) | Is the tech maker stuck in an endless price war |
| 12 | **The insiders are buyers** | Net insider buying. Stronger when many insiders buy at once, when lower-level officers buy amounts large relative to their pay ("seven VPs buying 1,000 shares apiece" beats "the president buying 5,000"), and when price is now *below* insiders' purchase price | No insider buying. Ignore routine selling. Flag selling only if many officers are dumping a majority of their shares after a big run-up |
| 13 | **The company is buying back shares** | Steady, multi-year reduction in shares outstanding (Crown, Cork & Seal, every year for 20 years); tender offers above market (Teledyne) | Share count growing (dilution, for example Navistar); capital diverted to diworseifying acquisitions instead (pre-refocus Gillette) |

Attributes 1, 2, 3, 6, and 7 overlap: they all measure how much a company repels Wall Street. Score each separately, but treat them together as one "neglect" theme in the verdict.

## Sanity checks (must pass regardless of score)

Every ideal example in the chapter also had the fundamentals. Lynch's own dream company (Cajun Cleansers) had 20% earnings growth for four years, never a down quarter, no debt, did well in the last recession, and he bought below the directors' price. Check:

- [ ] **Earnings**: consistent growth with no or few down quarters.
- [ ] **Balance sheet**: little or no debt, or debt being paid down from cash flow.
- [ ] **Price**: not already discovered. Once a stock is up tenfold and institutions own over half of it, the attributes are already priced in.
- [ ] **Management stake**: management holds a large personal stake in the company, not just a salary.

## Overrides

- A dull, disagreeable stock with deteriorating earnings or heavy debt is just a bad stock. Fail the verdict regardless of the attribute score.
- Watch for diworseification eroding the attributes over time. SCI lost its edge after unprofitable casket acquisitions and heavy institutional discovery.
- A stock's attributes describe the situation now. Re-score when institutional ownership, analyst coverage, or the share count trend changes.

## Scoring

Count ✅ as 1, ⚠️ as 0.5, ❌ and ❓ as 0. Report the score out of 13 and how many items are ❓.

| Score | Reading |
|-------|---------|
| 9–13 | Near-perfect profile; rare, so double-check the data |
| 6–8.5 | Strong Lynch-style profile |
| 3–5.5 | Some favorable traits; ordinary |
| 0–2.5 | Opposite of the perfect stock (glamorous, crowded, competitive) |

Weight attributes 9 (niche), 10 (repeat purchase), 12 (insider buying), and 13 (buybacks) more heavily when writing the verdict. They reflect business quality and shareholder alignment. The rest mostly measure neglect.

## Output template

```markdown
# [TICKER]: Lynch Perfect Stock Test

**Business in one sentence:** [plain description]
**Score:** [X] / 13 ([N] unknown)

| # | Attribute | Finding | Signal |
|---|-----------|---------|--------|
| 1 | Sounds dull or ridiculous | ... | ✅ / ⚠️ / ❌ / ❓ |
| 2 | Does something dull | ... | ... |
| 3 | Does something disagreeable | ... | ... |
| 4 | Spinoff | ... | ... |
| 5 | Institutions don't own it, analysts don't follow it | [inst. %, # analysts] | ... |
| 6 | Rumors: toxic waste and/or the Mafia | ... | ... |
| 7 | Something depressing about it | ... | ... |
| 8 | No-growth industry | [industry growth %] | ... |
| 9 | Has a niche | [type of franchise] | ... |
| 10 | People have to keep buying it | ... | ... |
| 11 | User of technology | ... | ... |
| 12 | Insiders are buyers | [who, how much, at what price] | ... |
| 13 | Buying back shares | [share count trend] | ... |

## Sanity checks
| Check | Finding | Signal |
|-------|---------|--------|
| Earnings consistency | ... | ... |
| Debt | ... | ... |
| Already discovered? | ... | ... |
| Management stake | ... | ... |

## Verdict
[Perfect-stock candidate / Has some traits / Not a perfect stock] with a one-line reason, the strongest attributes, and what would change the score (for example, institutions piling in, buybacks stopping).
```

Signal legend: ✅ favorable, ⚠️ partial, ❌ absent or unfavorable, ❓ unknown (data missing).

## Notes

- This test is about qualitative attributes. For valuation and category checks, use the `lynch-stock-checklist` skill as a complement; for classifying into the six stock categories, use `lynch-stock-categories`.
- Keep the verdict tied to the attributes; this is a research aid, not financial advice.
- If key data is missing, list which attributes are `unknown` and what would resolve them rather than filling gaps with assumptions.
