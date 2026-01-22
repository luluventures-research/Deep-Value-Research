---
name: stock-analysis-buffett-longterm
description: Comprehensive multi-decade analysis for mature companies using Buffett's forever-hold framework. Use when analyzing companies with 10+ years of public data, evaluating recession resilience, assessing moat durability, or building a retirement portfolio. Requires minimum 10 years of historical financial data.
allowed-tools: Read, Grep, Glob, Bash(python:*)
---

# Stock Analysis: Buffett Long-Term Framework (v2)

Analyze mature companies with 10+ years of public data using Warren Buffett's multi-decade framework. This skill enforces rigorous historical analysis, recession testing, and consistency scoring.

## ⚠️ GATE ZERO: HISTORICAL DATA REQUIREMENT (CHECK FIRST)

**Before ANY analysis can proceed, you MUST verify:**

```
Historical Data Availability:
[ ] 20+ years of audited financials → ✅✅ IDEAL (full confidence, factor 1.0)
[ ] 15-19 years → ✅ GOOD (high confidence, factor 0.9)
[ ] 10-14 years → ✅ ACCEPTABLE MINIMUM (limited confidence, factor 0.8)
[ ] 5-9 years → ⚠️ INSUFFICIENT for this framework
[ ] < 5 years → ❌ REJECT - use stock-analysis-growth instead
```

**ABSOLUTE MINIMUM: 10 Years of Audited Public Company Data**

**If company has < 10 years of data:**
- STOP this analysis immediately
- Recommend using `/stock-analysis-growth` skill instead
- OR mark analysis as "SPECULATIVE - Insufficient Track Record"

## WHY 10+ YEARS IS MANDATORY

✅ Includes at least 1 complete economic cycle
✅ Includes at least 1 recession (2008-09 or 2020)
✅ Can assess management capital allocation over meaningful period
✅ Can verify moat isn't temporary (10+ years of pricing power)
✅ Can identify trends vs. one-time events
✅ Can calculate meaningful statistics (averages, volatility)

❌ LESS THAN 10 YEARS:
- Cannot assess through full economic cycle
- May miss recessions entirely
- Track record could be just luck/bull market timing
- Insufficient evidence of moat durability
- Management track record too short to judge

## CRITICAL INSTRUCTION: USE ALL AVAILABLE DATA

⚠️ **For EVERY metric analyzed, you MUST use MAXIMUM available historical data:**

```
If 20 years available → Use ALL 20 years
If 15 years available → Use ALL 15 years
If 10 years available → Use ALL 10 years

NEVER analyze just "last 5 years" when more data exists
```

**Every table and chart MUST state:**
```
DATA PERIOD: [Start Year] to [End Year] ([X] years total)

Example: "DATA PERIOD: 2004-2024 (20 years)"
```

## Analysis Framework

### STEP 1: Data Adequacy Scorecard

Complete this FIRST:

| Requirement | Status | Notes |
|-------------|--------|-------|
| Minimum 10 years public data? | [ ] Yes [ ] No | If No → STOP or mark "High Uncertainty" |
| Includes at least 1 recession? | [ ] Yes [ ] No | 2008-09 or 2020 required |
| Consistent accounting (no major restatements)? | [ ] Yes [ ] No | Restatements = red flag |
| Same business model throughout? | [ ] Yes [ ] No | Major pivots = not comparable |
| Data available for ALL key metrics? | [ ] Yes [ ] No | Revenue, earnings, cash flow, ROE |

**Decision:**
- All "Yes" → ✅ Proceed with full confidence
- 1-2 "No" → ⚠️ Proceed with caveats
- 3+ "No" → ❌ Data insufficient, use different framework

### STEP 2: Recession Coverage Requirements

**Based on data period, identify which recessions are included:**

```
20-year data (2004-2024): Must analyze 3 recessions
- 2001 Dot-Com Bust (if data extends back)
- 2008-09 Financial Crisis ✅ CRITICAL
- 2020 COVID Pandemic ✅ CRITICAL

15-year data (2009-2024): Must analyze 2 recessions
- 2008-09 Financial Crisis ✅
- 2020 COVID Pandemic ✅

10-year data (2014-2024): Must analyze 1 recession
- 2020 COVID Pandemic ✅ (MINIMUM)

< 10 years OR misses all recessions:
❌ CRITICAL LIMITATION: Cannot assess recession performance
```

### STEP 3: Four-Gate Qualitative Filter

**Gate 1: Business Predictability**
- Can you explain the business to a 10-year-old in 2 minutes?
- Can you predict what this business looks like in 10 years?
- Has the core business model remained stable over the data period?

**Gate 2: Durable Moat Analysis**

Evidence required over FULL data period (10-20+ years):

| Moat Type | Evidence Required | Metric to Track |
|-----------|------------------|-----------------|
| **Brand Power** | Premium pricing sustained 10+ years | Gross Margin >40% consistently |
| **Switching Costs** | Customer retention despite alternatives | ROIC >15% consistently |
| **Network Effects** | Value increases with users | User growth + margin expansion |
| **Cost Advantages** | Structural cost leadership | Operating Margin vs. competitors |

**Pricing Power Test (Ultimate Moat Proof):**
- Show year-by-year price increases over 10+ years
- Compare to industry inflation
- Evidence: Price ↑ while volume maintained or grew

**Gate 3: Management Quality**

**10-Year Capital Allocation Report Card:**

Use MAXIMUM available data period:

```
1. Return on Retained Earnings (10-20 year test):
   = (Market Cap Increase) / (Total Retained Earnings)

   >1.5x = ✅ Exceptional ($1 retained → $1.50+ value)
   1.0-1.5x = ✅ Good
   <1.0x = ❌ Poor (should have paid dividends)

2. Share Buyback Discipline:
   - Did they buy back at reasonable prices?
   - Compare buyback prices to current intrinsic value

3. Dividend History (FULL period):
   - Years of consecutive increases: ___
   - Payout ratio consistency: ___
   - Cuts/suspensions during recessions? ___
```

**Gate 4: Industry Structure**
- Favorable long-term tailwinds over data period?
- Competitive intensity decreasing or increasing?
- Regulatory risk stable?

### STEP 4: Long-Term Financial Analysis

**⚠️ CRITICAL: All metrics MUST show year-by-year data for FULL available period (not just averages)**

#### A. Revenue & Profitability Consistency

**Revenue Growth (Use ALL available years):**

| Year | Revenue | YoY Growth | Economic Cycle |
|------|---------|------------|----------------|
| 2004 | $X.XXB | X% | Expansion |
| 2005 | $X.XXB | X% | Expansion |
| ... | ... | ... | ... |
| 2008 | $X.XXB | X% | **RECESSION** ← Highlight |
| 2009 | $X.XXB | X% | **RECESSION** ← Highlight |
| ... | ... | ... | ... |
| 2020 | $X.XXB | X% | **RECESSION** ← Highlight |
| ... | ... | ... | ... |
| 2024 | $X.XXB | X% | Expansion |

**DATA PERIOD: YYYY-YYYY (X years)**

**Statistics:**
- Average Growth Rate: ___%
- Years with Growth: ___/___
- Growth During Recessions: ___
- CAGR (Full Period): ___%
- Standard Deviation: ___

#### B. Margin Analysis (10-20 Year Trends)

**Show year-by-year for ALL three margins:**

| Year | Gross Margin | Operating Margin | Net Margin | Notes |
|------|--------------|------------------|------------|-------|
| 2004 | X% | X% | X% | |
| ... | ... | ... | ... | |
| 2008 | X% | X% | X% | Recession test |
| 2009 | X% | X% | X% | Recession test |
| ... | ... | ... | ... | |
| 2024 | X% | X% | X% | |

**DATA PERIOD: YYYY-YYYY (X years)**

**Trend Analysis:**
- Expanding margins = Moat strengthening
- Stable margins = Moat intact
- Declining margins = ⚠️ Moat erosion

#### C. ROE Analysis (Most Important)

**⚠️ Use MAXIMUM available history (20 years ideal, 10 minimum)**

| Year | ROE | Debt/Equity | ROA | ROCE | Notes |
|------|-----|-------------|-----|------|-------|
| 2004 | X% | X.X | X% | X% | |
| ... | ... | ... | ... | ... | |
| 2024 | X% | X.X | X% | X% | |

**DATA PERIOD: YYYY-YYYY (X years)**

**ROE Quality Assessment:**
- Average ROE: ___% (need >15% for "wonderful")
- Years above 15%: ___/___
- Lowest ROE (recession year): ___% (which year: ___)
- Is high ROE driven by leverage? Compare ROE vs ROA
- If ROE >> ROA, check debt levels (leverage trap)

#### D. Free Cash Flow (FCF) Analysis

**⚠️ Must use ALL available years of data**

| Year | Operating CF | CapEx | Free Cash Flow | FCF Margin | FCF/Net Income |
|------|--------------|-------|----------------|------------|----------------|
| 2004 | $XB | $XB | $XB | X% | X.XX |
| ... | ... | ... | ... | ... | ... |
| 2024 | $XB | $XB | $XB | X% | X.XX |

**DATA PERIOD: YYYY-YYYY (X years)**

**FCF Quality Checks:**
- Years with positive FCF: ___/___
- FCF during recessions: ___ (critical test)
- FCF conversion ratio (FCF/Net Income): ___ (>0.8 ideal)
- CapEx as % of revenue: ___ (declining = asset-light transition)

#### E. Balance Sheet Strength (Through Cycles)

**Track over FULL period available:**

| Year | Current Ratio | Debt/Equity | Interest Coverage | Economic Cycle |
|------|---------------|-------------|-------------------|----------------|
| 2004 | X.X | X.X | XX.X | Expansion |
| ... | ... | ... | ... | ... |
| 2008 | X.X | X.X | XX.X | **RECESSION** |
| 2009 | X.X | X.X | XX.X | **RECESSION** |
| ... | ... | ... | ... | ... |
| 2020 | X.X | X.X | XX.X | **RECESSION** |
| ... | ... | ... | ... | ... |
| 2024 | X.X | X.X | XX.X | Expansion |

**DATA PERIOD: YYYY-YYYY (X years)**

**Fortress Balance Sheet Criteria:**
- Current Ratio >1.5 throughout period
- Debt/Equity declining or stable
- Interest coverage >5x always (>10x ideal)

### STEP 5: Recession Resilience Analysis

**For EACH recession in your data period, analyze:**

#### 2008-2009 Financial Crisis (If in data period)
```
Performance During Crisis:
- Revenue impact: Down ___% (peak to trough)
- Profitability: Remained profitable? Yes/No
- FCF: Remained positive? Yes/No
- Dividend: Cut? Yes/No
- Market share: Gained/Lost/Maintained?

Recovery Speed:
- Years to recover revenue: ___
- Years to recover earnings: ___
- Stock performance vs S&P 500: ___

Score: ___/20
```

#### 2020 COVID Pandemic (If in data period)
```
[Same analysis format]

Score: ___/20
```

**Total Recession Resilience Score: ___/40 (or ___/60 for 3 recessions)**

### STEP 6: Multi-Decade Consistency Scorecard

**Use LONGEST data period available (20 years ideal, 10 minimum):**

```
1. Revenue Growth (years with growth): ___/20
2. Profitability (years profitable): ___/20
3. ROE >15% (years above 15%): ___/20
4. Positive FCF (years positive): ___/20
5. Dividend Increases (consecutive years): ___/20

TOTAL CONSISTENCY SCORE: ___/100

90-100 = ✅✅ Exceptionally predictable (Buffett's sweet spot)
75-89 = ✅ Highly consistent
60-74 = ⚠️ Moderately consistent
<60 = ❌ Too inconsistent for "forever hold"
```

### STEP 7: Valuation Analysis

#### Owner Earnings Calculation (Use Most Recent Year)

```
Owner Earnings = Net Income
                 + Depreciation & Amortization
                 - Maintenance CapEx
                 - Working Capital Increases
                 +/- Stock-Based Compensation adjustments

= $___________
```

#### Historical Valuation Bands (10-20 Year Analysis)

**Calculate P/E bands over FULL data period:**

| Metric | 10-Year Average | Current | Fair Value Implied |
|--------|-----------------|---------|-------------------|
| P/E Ratio | XX.X | XX.X | $XXX |
| P/FCF Ratio | XX.X | XX.X | $XXX |
| P/B Ratio | X.X | X.X | $XXX |
| EV/EBITDA | XX.X | XX.X | $XXX |

**DATA PERIOD: YYYY-YYYY (X years)**

#### Reverse DCF (Market Expectation Analysis)

```
Current Market Price: $___
Implied Growth Rate: ___%

Question: Is ___% growth sustainable given:
- Historical 10-20 year CAGR: ___%
- Industry growth rate: ___%
- Company guidance: ___%

Assessment: Fairly Valued / Undervalued / Overvalued
```

### STEP 8: Confidence Adjustment Factor

**Adjust final score based on data availability:**

```
Confidence Adjustment Factor:
20+ years = 1.0 (full confidence)
15-19 years = 0.9 (high confidence)
10-14 years = 0.8 (acceptable confidence)
< 10 years = 0.5 (low confidence - SPECULATIVE)

Raw Score × Confidence Factor = Adjusted Score
```

**Example:**
- Company scores 85/100 (excellent)
- BUT only has 12 years of data
- Adjusted Score: 85 × 0.8 = 68/100 (drops to "Good")

### STEP 9: Final Recommendation

```
COMPANY: _______________
DATA PERIOD ANALYZED: YYYY-YYYY (__ years)

GATE RESULTS:
- Gate 0 (Data): ✅ / ⚠️ / ❌
- Gate 1 (Predictability): ✅ / ❌
- Gate 2 (Moat): ✅ / ❌
- Gate 3 (Management): ✅ / ❌
- Gate 4 (Industry): ✅ / ❌

SCORES:
- Consistency Score: ___/100
- Recession Resilience: ___/60
- Raw Investment Score: ___/100
- Confidence Factor: ___
- FINAL ADJUSTED SCORE: ___/100

VALUATION:
- Fair Value Range: $___-$___
- Current Price: $___
- Margin of Safety: ___%

RECOMMENDATION:
[ ] STRONG BUY - Forever Hold Candidate
[ ] BUY - Quality Business at Fair Price
[ ] HOLD - Good Business, Wait for Better Price
[ ] PASS - Doesn't Meet Buffett Standards
[ ] AVOID - Fundamental Concerns

LIMITATIONS:
- [List any data gaps, missing recessions, etc.]

KEY RISKS:
1. ___
2. ___
3. ___
```

## Year-by-Year Requirement

**ALL metrics must be shown year-by-year, not just averages:**

❌ **NOT Acceptable:**
"Average ROE over period: 18%"

✅ **Required:**
| Year | ROE | Notes |
|------|-----|-------|
| 2004 | 16% | |
| 2005 | 17% | |
| ... | ... | ... |
| 2024 | 19% | |

Average: 18% | Min: 12% (2009) | Max: 21% (2021) | Std Dev: 2.1%

## Rolling Averages (If Sufficient Data)

**IF data period ≥ 15 years:**
- Calculate rolling 10-year averages
- Shows if metrics improving or deteriorating
- Early warning system for moat erosion

**IF data period < 15 years:**
- Note: "Cannot calculate rolling 10-year averages (requires minimum 15 years)"
- Flag as limitation

## Red Flags - Automatic Disqualification

Even with perfect scores, REJECT if ANY of these present:

- [ ] ❌ Inconsistent accounting (multiple restatements)
- [ ] ❌ Related-party transactions (>5% revenue)
- [ ] ❌ Serial acquirer (growth through M&A, not organic)
- [ ] ❌ Declining margins over 5+ years (moat erosion)
- [ ] ❌ Negative FCF in >30% of years analyzed
- [ ] ❌ Management turnover (>3 CEOs in 10 years)
- [ ] ❌ Dividend cuts during non-recession years
- [ ] ❌ Debt increased while business shrinking

## When to Use This Skill

✅ **USE this skill when:**
- Company has 10+ years of public financial data
- Evaluating "forever hold" investment candidates
- Building retirement/long-term portfolio
- Need recession-tested businesses
- Want Buffett's actual investment standards

❌ **DO NOT use this skill when:**
- Company has <10 years public data → Use `/stock-analysis-growth`
- Need quick screening → Use `/stock-analysis-quick-metrics`
- Forensic deep-dive on specific red flags → Use `/stock-analysis-forensic`
- Recent IPO or high-growth tech → Use `/stock-analysis-growth`

## Supporting Resources

For detailed reference material, see:
- `MOAT_REFERENCE.md` - Deep dive on moat types and testing
- `RECESSION_ANALYSIS.md` - Historical recession impact analysis
- `OWNER_EARNINGS.md` - Detailed Owner Earnings calculation guide

## Remember

> "Time is the friend of the wonderful business, the enemy of the mediocre."
> — Warren Buffett

**A 10-year track record through a recession proves durability. A 20-year track record through 2-3 recessions proves excellence.**

This framework ensures you NEVER analyze a company without sufficient evidence of long-term quality.
