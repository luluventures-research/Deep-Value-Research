---
name: stock-analysis-quick-metrics
description: Fast financial metrics screening and calculation for quick company evaluation. Use for initial screening, comparing multiple companies, calculating key ratios (ROE, P/E, FCF, debt ratios), or getting a high-level financial snapshot. Optimized for speed over depth.
allowed-tools: Read, Bash(python:*)
---

# Stock Analysis: Quick Metrics Calculator

Rapidly calculate and screen key financial metrics for quick company evaluation. Use this for initial screening before deciding whether to conduct full analysis.

## When to Use This Skill

✅ **USE this skill when:**
- Need quick screening of multiple companies
- Want fast calculation of key metrics
- Initial evaluation before deep dive
- Comparing companies side-by-side
- Validating a quick investment idea
- Checking if company meets basic criteria

❌ **DO NOT use this skill when:**
- Need comprehensive multi-decade analysis → Use `/stock-analysis-buffett-longterm`
- Analyzing growth companies deeply → Use `/stock-analysis-growth`
- Investigating red flags or fraud → Use `/stock-analysis-forensic`
- Building investment thesis → Use comprehensive skills

## Quick Screening Framework

### STEP 1: Essential Metrics Snapshot (30 seconds)

**Basic Company Info:**
```
Company: _______________
Ticker: ___
Sector: _______________
Market Cap: $___B
Current Price: $___
```

**The 6 Critical Numbers:**

```
1. P/E Ratio: ___
2. ROE (Latest Year): ___%
3. Debt/Equity: ___
4. Current Ratio: ___
5. FCF Margin: ___%
6. Revenue Growth (3Y CAGR): ___%
```

**Instant Pass/Fail Filter:**
```
Minimum Standards (Adjust for sector):
[ ] P/E < 25 (or justified by growth)
[ ] ROE > 12%
[ ] Debt/Equity < 2.0
[ ] Current Ratio > 1.0
[ ] FCF Margin > 5%
[ ] Revenue Growth > 0% (not declining)

Pass: ___/6

6/6 = ✅✅ Excellent - Deep dive warranted
4-5/6 = ✅ Good - Investigate further
2-3/6 = ⚠️ Mixed - Selective analysis
0-1/6 = ❌ Fail - Move on
```

### STEP 2: Profitability Quick Check

**Margin Trio (Latest Year):**
```
Gross Margin: ___%
Operating Margin: ___%
Net Margin: ___%

Quality Check:
All three stable/growing? Yes/No
All three above industry avg? Yes/No
```

**Return Metrics (Latest Year):**
```
ROE = Net Income / Shareholders' Equity = ___%
ROA = Net Income / Total Assets = ___%
ROIC = NOPAT / Invested Capital = ___%

Quick Assessment:
ROE >15% = ✅ Strong
ROE 10-15% = ⚠️ Moderate
ROE <10% = ❌ Weak
```

### STEP 3: Cash Flow Quick Check

**OCF vs Net Income Test:**
```
Operating Cash Flow: $___M
Net Income: $___M
Ratio (OCF/NI): ___

>1.2 = ✅ Excellent cash conversion
0.8-1.2 = ✅ Good
<0.8 = ❌ Poor earnings quality
```

**Free Cash Flow:**
```
Operating Cash Flow: $___M
Less: CapEx: $___M
= Free Cash Flow: $___M

FCF Margin = FCF / Revenue = ___%

>15% = ✅ Excellent
8-15% = ✅ Good
<8% = ⚠️ Capital intensive
```

### STEP 4: Balance Sheet Health

**Liquidity Ratios:**
```
Current Ratio = Current Assets / Current Liabilities = ___
Quick Ratio = (CA - Inventory) / Current Liabilities = ___

Current Ratio >1.5 = ✅ Safe
Current Ratio 1.0-1.5 = ⚠️ Watch
Current Ratio <1.0 = ❌ Risky
```

**Leverage Ratios:**
```
Debt/Equity = Total Debt / Total Equity = ___
Debt/Assets = Total Debt / Total Assets = ___
Interest Coverage = EBIT / Interest Expense = ___

Leverage Assessment:
D/E <0.5 = ✅ Conservative
D/E 0.5-1.5 = ✅ Moderate
D/E >1.5 = ⚠️ High (sector dependent)

Interest Coverage >5x = ✅ Safe
Interest Coverage 2-5x = ⚠️ Adequate
Interest Coverage <2x = ❌ Risky
```

### STEP 5: Valuation Quick Check

**Basic Valuation Ratios:**
```
P/E Ratio = Price / EPS = ___
P/B Ratio = Price / Book Value per Share = ___
P/S Ratio = Market Cap / Revenue = ___
EV/EBITDA = Enterprise Value / EBITDA = ___

Sector Averages (Look up):
Industry P/E: ___
Industry P/B: ___
Industry EV/EBITDA: ___

Relative Valuation:
Trading below sector average? Yes/No
Discount/Premium: ___%
```

**PEG Ratio (If growth company):**
```
PEG = P/E / Growth Rate

P/E: ___
Expected Growth: ___%
PEG: ___

<1.0 = ✅ Undervalued
1.0-2.0 = ⚠️ Fair
>2.0 = ❌ Expensive
```

### STEP 6: Growth & Trends

**3-Year Revenue CAGR:**
```
Revenue 3 years ago: $___M
Revenue latest: $___M
CAGR = ((Latest/Start)^(1/3) - 1) × 100 = ___%

>15% = ✅ Fast growth
5-15% = ✅ Steady growth
0-5% = ⚠️ Slow growth
<0% = ❌ Declining
```

**3-Year Earnings CAGR:**
```
EPS 3 years ago: $___
EPS latest: $___
CAGR = ___%

Compare to Revenue CAGR:
Earnings growing faster = ✅ Margin expansion
Earnings growing slower = ⚠️ Margin compression
```

## Quick Screening Templates

### Template A: Value Stock Screener

```
Criteria for Value Stocks:
[ ] P/E < 15
[ ] P/B < 2.0
[ ] Dividend Yield > 2%
[ ] ROE > 12%
[ ] Debt/Equity < 1.0
[ ] FCF Margin > 8%
[ ] Current Ratio > 1.5

Pass: ___/7

6-7 = ✅ Strong value candidate
4-5 = ⚠️ Investigate
<4 = ❌ Pass
```

### Template B: Growth Stock Screener

```
Criteria for Growth Stocks:
[ ] Revenue Growth > 20%
[ ] Gross Margin > 50%
[ ] PEG Ratio < 2.0
[ ] Rule of 40 > 40% (Growth% + FCF Margin%)
[ ] Current Ratio > 1.0
[ ] Cash/Debt Ratio > 1.0 (if unprofitable)
[ ] Market Cap > $1B (liquidity)

Pass: ___/7

6-7 = ✅ Strong growth candidate
4-5 = ⚠️ Investigate
<4 = ❌ Pass
```

### Template C: Dividend Stock Screener

```
Criteria for Dividend Stocks:
[ ] Dividend Yield > 3%
[ ] Payout Ratio < 70%
[ ] FCF covers dividend (FCF/Dividend > 1.2)
[ ] 5+ years consecutive increases
[ ] Debt/Equity < 1.5
[ ] Current Ratio > 1.2
[ ] ROE > 10%

Pass: ___/7

6-7 = ✅ Strong dividend candidate
4-5 = ⚠️ Investigate
<4 = ❌ Pass
```

### Template D: Quality Stock Screener (Buffett-style)

```
Criteria for Quality Stocks:
[ ] ROE > 15% (3-year average)
[ ] ROIC > 12%
[ ] FCF Margin > 10%
[ ] Gross Margin > 35%
[ ] Revenue growth positive (3-year)
[ ] Debt/Equity < 0.8
[ ] OCF/NI > 1.0

Pass: ___/7

6-7 = ✅ High quality business
4-5 = ⚠️ Good quality
<4 = ❌ Mediocre
```

## Quick Calculation Formulas

### Profitability Metrics

```
ROE = Net Income / Shareholders' Equity × 100

ROA = Net Income / Total Assets × 100

ROIC = NOPAT / Invested Capital × 100
Where: NOPAT = Operating Income × (1 - Tax Rate)
       Invested Capital = Total Assets - Non-interest Bearing Current Liabilities

Gross Margin = (Revenue - COGS) / Revenue × 100

Operating Margin = Operating Income / Revenue × 100

Net Margin = Net Income / Revenue × 100

Asset Turnover = Revenue / Average Total Assets
```

### Cash Flow Metrics

```
Free Cash Flow = Operating Cash Flow - Capital Expenditures

FCF Margin = Free Cash Flow / Revenue × 100

OCF/NI Ratio = Operating Cash Flow / Net Income

Cash Conversion Cycle = DSO + DIO - DPO
Where:
  DSO (Days Sales Outstanding) = (A/R / Revenue) × 365
  DIO (Days Inventory Outstanding) = (Inventory / COGS) × 365
  DPO (Days Payable Outstanding) = (A/P / COGS) × 365
```

### Leverage Metrics

```
Debt-to-Equity = Total Debt / Total Equity

Debt-to-Assets = Total Debt / Total Assets

Interest Coverage = EBIT / Interest Expense

Current Ratio = Current Assets / Current Liabilities

Quick Ratio = (Current Assets - Inventory) / Current Liabilities

Cash Ratio = (Cash + Marketable Securities) / Current Liabilities
```

### Valuation Metrics

```
P/E Ratio = Stock Price / Earnings Per Share

P/B Ratio = Stock Price / Book Value Per Share

P/S Ratio = Market Cap / Annual Revenue

EV/EBITDA = Enterprise Value / EBITDA
Where: Enterprise Value = Market Cap + Total Debt - Cash

PEG Ratio = P/E Ratio / Expected Growth Rate %

Dividend Yield = Annual Dividend Per Share / Stock Price × 100

Payout Ratio = Dividends / Net Income × 100
```

### Growth Metrics

```
CAGR = ((Ending Value / Beginning Value)^(1/# of years) - 1) × 100

Revenue Growth = ((Current Revenue - Prior Revenue) / Prior Revenue) × 100

EPS Growth = ((Current EPS - Prior EPS) / Prior EPS) × 100

Rule of 40 = Revenue Growth % + Free Cash Flow Margin %
```

## Quick Comparison Table (Multiple Companies)

```
| Metric | Company A | Company B | Company C | Best |
|--------|-----------|-----------|-----------|------|
| P/E | ___ | ___ | ___ | ___ |
| ROE | ___% | ___% | ___% | ___ |
| Debt/Equity | ___ | ___ | ___ | ___ |
| FCF Margin | ___% | ___% | ___% | ___ |
| Revenue Growth | ___% | ___% | ___% | ___ |
| Dividend Yield | ___% | ___% | ___% | ___ |
| Current Ratio | ___ | ___ | ___ | ___ |
| Gross Margin | ___% | ___% | ___% | ___ |

Winner: ___
Concerns: ___
Next Step: Detailed analysis of ___
```

## Red Flag Quick Checklist

**Instant Disqualifiers (If ANY present, skip to next company):**

- [ ] ❌ Auditor resigned or qualified opinion
- [ ] ❌ Multiple restatements
- [ ] ❌ Revenue declining 3+ consecutive years
- [ ] ❌ Negative FCF for 3+ years
- [ ] ❌ Current ratio <0.8 (liquidity crisis)
- [ ] ❌ Interest coverage <1.0 (can't service debt)
- [ ] ❌ Debt/Equity >5.0 (unless financial company)
- [ ] ❌ Goodwill >70% of assets (acquisition zombie)

## Quick Decision Matrix

```
After calculating metrics, use this decision tree:

START
  ↓
Does it pass 6 Critical Numbers filter (≥4/6)?
  ├─ No → PASS (move to next company)
  └─ Yes ↓
       Does it pass sector-specific template (≥5/7)?
         ├─ No → PASS (move to next company)
         └─ Yes ↓
              Any instant disqualifier red flags?
                ├─ Yes → PASS (move to next company)
                └─ No ↓
                     Valuation reasonable vs sector?
                       ├─ No → WATCHLIST (wait for better price)
                       └─ Yes ↓
                            PROCEED TO DEEP ANALYSIS
                            ├─ 10+ years data → /stock-analysis-buffett-longterm
                            ├─ <10 years, high growth → /stock-analysis-growth
                            └─ Concerns about accounting → /stock-analysis-forensic
```

## Quick Score Summary Template

```
═══════════════════════════════════════
QUICK METRICS SCORECARD: _______________
═══════════════════════════════════════

PROFITABILITY: ___/10
- ROE: ___ (___pts)
- Margins: ___ (___pts)
- ROIC: ___ (___pts)

CASH FLOW: ___/10
- FCF Generation: ___ (___pts)
- OCF/NI Ratio: ___ (___pts)

BALANCE SHEET: ___/10
- Liquidity: ___ (___pts)
- Leverage: ___ (___pts)

VALUATION: ___/10
- Relative P/E: ___ (___pts)
- PEG Ratio: ___ (___pts)

GROWTH: ___/10
- Revenue CAGR: ___ (___pts)
- Earnings trend: ___ (___pts)

TOTAL SCORE: ___/50

45-50 = ✅✅ Exceptional - Priority deep dive
38-44 = ✅ Strong - Detailed analysis warranted
30-37 = ⚠️ Acceptable - Selective investigation
<30 = ❌ Weak - Move on

RECOMMENDATION:
[ ] PRIORITY - Analyze with /stock-analysis-buffett-longterm
[ ] GROWTH CANDIDATE - Analyze with /stock-analysis-growth
[ ] WATCHLIST - Monitor for better entry
[ ] PASS - Does not meet criteria

KEY STRENGTHS:
1. ___
2. ___

KEY CONCERNS:
1. ___
2. ___

NEXT STEP: ___
═══════════════════════════════════════
```

## Sector-Specific Quick Adjustments

### Technology (SaaS):
```
Adjust criteria:
- P/E <40 (can be higher for growth)
- Gross Margin >65%
- Rule of 40 >40%
- Magic Number >0.75
- Focus on: NRR, CAC payback
```

### Banking/Financials:
```
Adjust criteria:
- P/B ratio more relevant than P/E
- Tier 1 Capital Ratio >10%
- NPL Ratio <3%
- ROE >12% (leverage amplifies)
- Focus on: NIM, efficiency ratio
```

### Retail:
```
Adjust criteria:
- Inventory turnover (higher better)
- Same-store sales growth
- ROE >15% (low margin business)
- Asset turnover >2.0
- Focus on: Comp sales, inventory days
```

### Industrials/Manufacturing:
```
Adjust criteria:
- Asset turnover >0.8
- CapEx intensity (CapEx/Revenue)
- Operating margin >10%
- ROIC >10%
- Focus on: Capacity utilization, order backlog
```

## Time-Saving Tips

1. **Use latest 10-K/10-Q for most metrics** - Don't calculate from scratch if disclosed
2. **Focus on trends, not single numbers** - 3-year minimum for meaningful patterns
3. **Compare to sector averages always** - Context matters more than absolute numbers
4. **Use screening tools first** - Filter to 10-20 companies, then calculate manually
5. **Start with disqualifiers** - Check red flags first to save time
6. **Document reasoning** - Quick note on why passed/failed for future reference

## Remember

**This skill is for SCREENING, not INVESTING:**
- Quick metrics identify candidates
- Candidates need deep analysis before investment
- Never invest based solely on quick metrics
- Use comprehensive skills for actual investment decisions

**Speed vs. Accuracy Trade-off:**
- Quick metrics: 80% accuracy, 5% of time
- Deep analysis: 95% accuracy, 100% of time
- Use quick metrics to decide WHERE to spend deep analysis time

**Purpose:**
> "The quick metrics skill helps you say 'NO' quickly to 90% of companies, so you can say 'YES' slowly to the few that truly deserve deep analysis."

Screen fast. Analyze slow. Invest slower.
