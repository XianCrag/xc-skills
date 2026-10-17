---
name: lynch-stock-categories
description: Classifies a stock into one of Peter Lynch's six categories (slow grower, stalwart, fast grower, cyclical, turnaround, asset play) using One Up on Wall Street, Chapter 7 "I've Got It, I've Got It—What Is It?". Covers company size relative to its industry, each category's signature and expectations, turnaround and asset subtypes, secondary categories, and reclassification when a company moves between categories. Use when the user asks what kind of stock something is, which Lynch category it fits, or when another Lynch skill (lynch-stock-checklist, lynch-buy-sell-timing, lynch-stocks-to-avoid) needs a classification step.
---

# Lynch Stock Categories

Source: Peter Lynch, *One Up on Wall Street*, Chapter 7 "I've Got It, I've Got It—What Is It?".

Lynch: "Putting stocks in categories is the first step in developing the story. Now at least you know what kind of story it's supposed to be." The category decides which checks apply, what return to expect, and when to sell. "It's simply impossible to find a generic formula that sensibly applies to all the different kinds of stocks."

## Workflow

1. **Gather data**: market cap and size versus industry peers, earnings growth rate (5–10 years) versus GDP, whether earnings swing with the economy or a commodity, dividend record, recent losses or bankruptcy risk, and assets that may be worth more than the market credits (cash, land, resources, subsidiaries, tax-loss carryforwards). Mark missing data as `unknown`.
2. **Size first**: compare the company's size to others in its industry (see below).
3. **Assign one primary category** using the signatures below. Add a secondary category if one clearly applies.
4. **Check for a category change**: is the company in the middle of moving from one category to another?
5. **Report** using the output block, then continue with whichever skill asked for the classification.

## Size first

Before categorizing, Lynch establishes the company's size relative to others in its industry. "Big companies have small moves, small companies have big moves." A huge company can't grow fast "without taking over the world" (GE, with $3B+ in annual profit, moves slowly while La Quinta soars). Everything else equal, smaller companies do better: Pic 'N' Save beat Sears; Nucor beat U.S. Steel; SmithKline Beckman beat American Home Products.

## The six categories

Growth means "the company does more of whatever it does this year than it did last year," measured against the economy (GNP growth, about 3% a year when Lynch wrote). Three categories are defined by growth rate; three by situation.

| Category | Signature | Typical examples (from the book) |
|----------|-----------|----------------------------------|
| Slow grower (sluggard) | Large, aging company growing slightly faster than GNP (about 2–4%); pays a generous, regular dividend | Electric utilities, Houston Industries |
| Stalwart | Multibillion-dollar company with about 10–12% annual earnings growth | Coca-Cola, Bristol-Myers, Procter & Gamble, Hershey's, Ralston Purina, Colgate-Palmolive, Kellogg |
| Fast grower | Small, aggressive new enterprise growing 20–25% a year (sometimes 20–30%+) | Taco Bell, Wal-Mart, The Gap, Marriott, Anheuser-Busch |
| Cyclical | Sales and profits rise and fall in a regular, if not completely predictable, way | Autos, airlines, tires, steel, chemicals; defense behaves like one (Ford, AMR) |
| Turnaround | Battered, depressed, often near Chapter 11; "no growers," potential fatalities | Chrysler, Penn Central, Con Edison, General Public Utilities, Lockheed |
| Asset play | Sitting on something valuable that you know about but Wall Street has overlooked | Pebble Beach, Newhall Land, Alico, Penn Central, Liberty Corp., Telecommunications Inc. |

### Slow growers
- Started as fast growers and "pooped out," either reaching their limit or failing to make the most of their chances. When an industry slows, most companies in it slow too. Every fast-growing industry eventually becomes slow-growing (railroads, autos, steel, chemicals, utilities, aluminum, and mainframe computers).
- Chart is flat, like "the topographical map of Delaware."
- A generous, regular dividend is a "sure sign": companies pay out when they can't find ways to expand.
- Expectation: little price gain. Lynch owns few of them.

### Stalwarts
- Faster than slow growers but "not exactly agile climbers"; the chart is in the foothills.
- Return depends on when and at what price you buy. P&G bought in 1963 only made fourfold in 25 years, no better than bonds. Ask anyone bragging about a double: "And how long did you own it?"
- Lynch buys them for a 30–50% gain, then sells and repeats with similar issues that haven't yet risen. After a 50% rise in a year or two, consider selling.
- Good protection in recessions and crashes: they won't go bankrupt and are soon revalued. Bristol-Myers had one down quarter in 20 years; Kellogg none in 30 ("people still eat cornflakes").
- Even stalwarts can lose half their value in a bad market if bought overpriced (Bristol-Myers in 1973–74).

### Fast growers
- Lynch's favorites: "the land of the 10- to 40-baggers, and even the 200-baggers."
- Does not need a fast-growing industry, and Lynch would rather it weren't in one. It needs room to take share in a slow-growing industry (beer: Anheuser-Busch; hotels growing 2% while Marriott grew 20%).
- Growth engine: succeed in one place, then duplicate the formula mall by mall, city by city.
- Risks: young, overzealous, underfinanced companies can end up in Chapter 11; larger ones get punished hard when they slow and turn into slow growers. Once too big, "there's simply no place for it to stretch out."
- Look for good balance sheets and substantial profits. "The trick is figuring out when they'll stop growing, and how much to pay for the growth."

### Cyclicals
- Chart looks "like the polygraphs of liars, or the maps of the Alps."
- They rise faster than stalwarts coming out of recession and fall hard going in. You can lose more than 50% quickly when buying at the wrong point in the cycle, and wait years for the next upswing.
- "The most misunderstood of all the types of stocks": big, well-known cyclicals get mistaken for stalwarts. Ford is not Bristol-Myers. A stalwart may lose half in a slump; Ford lost 80% in the early 1980s.
- "Timing is everything." An industry edge (working in steel, aluminum, airlines, autos) matters most here.

### Turnarounds
- Not slow growers or rebounding cyclicals: potential fatalities. A poorly managed cyclical is always a candidate (Chrysler).
- Successful ones make up lost ground quickly, and their moves are the least related to the general market of any category. Failed ones disappear from the records.
- Subtypes:
  - **Bail-us-out-or-else**: survival depends on a government loan guarantee (Chrysler, Lockheed).
  - **Who-would-have-thunk-it**: a "safe" company collapses unexpectedly (Con Edison, $10 to $3, then back to $52).
  - **Little-problem-we-didn't-anticipate**: a minor tragedy perceived as worse than it is (GPU after Three Mile Island). Avoid tragedies with unmeasurable liability (Union Carbide after Bhopal, Johns-Manville).
  - **Perfectly-good-company-inside-a-bankrupt-company**: a sound business freed from a failing parent (Toys "R" Us out of Interstate Department Stores).
  - **Restructuring to maximize shareholder value**: shedding unprofitable subsidiaries from earlier diworseification (Penn Central, Goodyear, Merck).

### Asset plays
- The asset may be cash, real estate, metals, oil, timber, mineral rights, newspapers, TV stations, patented drugs, cable subscribers, or even past losses (a tax-loss carryforward, as with Penn Central).
- Value can exceed the whole market cap: Pebble Beach's gravel pit alone sold for more than investors paid for the company; Liberty Corp.'s TV properties equaled its share price, so the insurance business came free.
- Earnings may be poor and debt worrisome on traditional measures, yet the assets outweigh them (Telecommunications Inc.).
- This is where the local, personal edge matters most (realtors and residents near Newhall Ranch). After that, "all you need is patience."

## Secondary categories and category changes

"Companies don't stay in the same category forever." A company may fit two categories at once (Penn Central was a turnaround and an asset play). Disney passed through every major category: fast grower, stalwart, asset play, turnaround.

Common transitions:

| From | To | Example |
|------|----|---------|
| Fast grower | Slow grower or stalwart (growth burns out to single digits) | Carpets, plastics, calculators, disk drives, HMOs, computers; Dow Chemical, Tampa Electric |
| Slow grower | Fast grower (unusual) | Stop & Shop |
| Fast grower | Cyclical | Advanced Micro Devices, Texas Instruments |
| Cyclical with serious financial problems | Turnaround, then back to cyclical | Chrysler, LTV |
| Growth company that diworseifies | Turnaround | (none named in the chapter) |
| Slowed fast grower that owns real estate | Asset play | Holiday Inn, Federated, Allied Stores; possibly McDonald's |
| Growth company | Cyclical, then turnaround | Inco (International Nickel) |

When a transition is under way, classify by what the company is now, note what it was, and say which way it's heading. A finished turnaround must be reclassified and judged by its new category.

## Why it matters

Know what you're looking for: slow growth, fast growth, recession protection, a turnaround, a cyclical bounce, or assets. Generic rules like "sell when you double your money," "sell after two years," or "cut losses at 10%" are "absolute folly."
- Don't treat a potential Wal-Mart like a stalwart and sell it for 50% when it could deliver 1,000%.
- Don't hold a doubled Ralston Purina with unexciting fundamentals hoping for more.
- Don't expect a utility to do as well as Philip Morris (unless it's a turnaround).
- You can put away a well-bought Bristol-Myers for twenty years, but not Texas Air: "Shaky companies in cyclical industries are not the ones you sleep on through recessions."

## Output block

```markdown
**Size vs. industry:** [large / mid / small relative to peers]
**Category:** [primary] (secondary: [if any])
**Evidence:** [growth rate vs. GDP, cyclicality, dividend, distress, hidden assets]
**Transition:** [none / moving from X toward Y]
**What this implies:** [what return to expect and which checks matter]
```

## Notes

- Lynch gives growth bands (about 2–4%, 10–12%, 20–25%), not hard cutoffs. For a company between bands, weigh size, recession record, and dividend policy, and say the call is a judgment.
- If the data can't settle the category, list the candidates and what would decide between them.
