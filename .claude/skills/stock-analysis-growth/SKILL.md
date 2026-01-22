---
name: stock-analysis-growth
description: Analyze high-growth companies using Peter Lynch, Stanley Druckenmiller, and Philip Fisher methodologies. Use for companies with <10 years of data, fast growers (15-25%+ growth), inflection point analysis, TAM expansion opportunities, or unit economics evaluation. Focuses on forward-looking potential rather than historical track records.
allowed-tools: Read, Grep, Glob, WebFetch, Bash(python:*)
---

# Stock Analysis: Growth Company Framework

Analyze high-growth companies and recent IPOs using Peter Lynch's GARP methodology, Stanley Druckenmiller's inflection point framework, and Philip Fisher's scuttlebutt method.

## When to Use This Skill

✅ **USE this skill when:**
- Company has <10 years of public financial data
- Fast growers: 15-25%+ annual growth
- Recent IPOs or young public companies
- TAM expansion opportunities (market growing rapidly)
- Identifying inflection points
- Unit economics and SaaS metrics evaluation
- Growth at reasonable price (GARP) analysis

❌ **DO NOT use this skill when:**
- Company has 10+ years of data AND you want multi-decade analysis → Use `/stock-analysis-buffett-longterm`
- Need forensic deep-dive → Use `/stock-analysis-forensic`
- Quick metric screening → Use `/stock-analysis-quick-metrics`

## Framework Philosophy

**Key Difference from Value Investing:**
- Value investing: Historical track record proves quality
- Growth investing: Forward-looking potential before it's obvious

**The Growth Paradox:**
> "If you wait until you can see the cathode ray tube, you've missed buying RCA."
> — Philip Fisher

**The Risk:**
- Higher uncertainty (less historical evidence)
- More competition (obvious opportunities attract capital)
- Valuation sensitivity (growth expectations baked into price)

## LAYER 1: The Peter Lynch Classification System

### Six Categories of Stocks

**1. Slow Growers (0-5% annual growth)**
- Mature, large companies
- Stable dividends, minimal growth
- **Action:** Generally AVOID for growth portfolio

**2. Stalwarts (5-12% annual growth)**
- Large, established companies
- Dependable but unexciting
- **Action:** Hold during market volatility, sell at 30-50% gain

**3. Fast Growers (15-25%+ annual growth)** ⭐⭐⭐
- **WHERE THE BIG MONEY IS MADE - TEN BAGGERS**
- Small aggressive companies
- **PRIMARY FOCUS for this framework**
- **Risk:** Can't sustain growth forever, risk of collapse

**4. Cyclicals**
- Auto, airlines, steel, chemicals
- Timing is everything (buy at bottom of cycle)
- **Danger:** Mistaking cyclical recovery for growth

**5. Turnarounds**
- Depressed, making comeback
- High risk, high reward
- **Key:** Has turnaround actually begun?

**6. Asset Plays**
- Undervalued assets on balance sheet
- Real estate, resources, overlooked value
- **Key:** Is market recognizing the value?

### **CLASSIFICATION REQUIREMENT:**

```
Company Being Analyzed: _______________
Lynch Category: [ ] Slow [ ] Stalwart [ ] Fast Grower [ ] Cyclical [ ] Turnaround [ ] Asset

If NOT "Fast Grower" → Explain why using this growth framework
```

## LAYER 2: The Druckenmiller Inflection Point Framework

**Stanley Druckenmiller's Approach:**
> "Earnings don't drive stock prices. Earnings revisions drive stock prices."

### The Three-Layer Investment Process

#### Layer 2A: Macro Setup (Top-Down)

**Identify macro tailwinds:**
- [ ] Industry secular growth trend (TAM expanding)
- [ ] Regulatory changes favoring industry
- [ ] Technological shift enabling new models
- [ ] Demographic trends supporting demand
- [ ] Interest rate environment (low rates favor growth)

**Macro Risk Assessment:**
- What macro scenario breaks this thesis?
- How sensitive is company to economic cycles?
- Currency/geopolitical risks?

#### Layer 2B: Company/Industry Analysis (Bottom-Up)

**The 5 Types of Inflection Points:**

| Inflection Type | What to Look For | Example |
|----------------|------------------|---------|
| **1. Product** | New product driving acceleration | iPhone launch, AWS |
| **2. Market Share** | Taking share from incumbents | Netflix vs Cable |
| **3. Margin** | Operating leverage kicking in | SaaS reaching scale |
| **4. TAM Expansion** | Market growing faster than expected | Cloud computing TAM |
| **5. Competitive** | Competitor weakness or exit | Competitor bankruptcy |

**REQUIRED: Identify the specific inflection point:**
```
Inflection Point: _______________
Type: [ ] Product [ ] Market Share [ ] Margin [ ] TAM [ ] Competitive

Evidence:
1. _______________
2. _______________
3. _______________

Expected Duration: ___ quarters/years
Risk of Reversal: Low / Medium / High
```

#### Layer 2C: Risk Management & Position Sizing

**Druckenmiller's Rules:**
- When highly confident → Size up (concentrated bets)
- When thesis weakening → Exit rapidly, don't hope
- Position size reflects conviction level

**For this analysis:**
```
Conviction Level: Low / Medium / High
Suggested Position: ___ % of portfolio
Stop Loss Trigger: _______________
```

## LAYER 3: Philip Fisher's Scuttlebutt Method

**15 Points to Investigate (Research Beyond Financials)**

### Growth Prospects (Points 1-5)

**1. Does the company have products/services with sufficient market potential to make possible a sizable increase in sales for at least several years?**
- [ ] TAM Analysis complete (see below)
- Current TAM: $___B
- Expected TAM in 5 years: $___B
- Company's potential market share: ___%

**2. Does management have determination to continue to develop products/processes that will further increase total sales?**
- [ ] R&D spending: ___% of revenue (consistent/increasing?)
- [ ] New product pipeline: ___
- [ ] Innovation culture: Evidence ___

**3. How effective are company's R&D efforts relative to size?**
- [ ] R&D efficiency: Revenue per R&D dollar ___
- [ ] Time to market: ___
- [ ] Success rate of new products: ___%

**4. Does company have an above-average sales organization?**
- [ ] Sales efficiency: CAC payback period ___
- [ ] Sales team growth: ___
- [ ] Customer acquisition trends: ___

**5. Does company have a worthwhile profit margin?**
- [ ] Gross margin: ___% (expanding/stable/declining?)
- [ ] Path to profitability clear? Yes/No
- [ ] Unit economics positive? Yes/No

### Operational Excellence (Points 6-10)

**6. What is company doing to maintain or improve profit margins?**
- [ ] Operating leverage evidence: ___
- [ ] Margin expansion plan: ___

**7. Does company have outstanding labor/personnel relations?**
- [ ] Employee turnover: ___% (industry avg: ___%)
- [ ] Glassdoor rating: ___/5.0
- [ ] Stock options for employees: Yes/No

**8. Does company have outstanding executive relations?**
- [ ] Management tenure: ___
- [ ] Insider ownership: ___%
- [ ] Alignment with shareholders: ___

**9. Does company have depth to management?**
- [ ] Succession plan: Clear/Unclear
- [ ] Key person risk: High/Medium/Low
- [ ] Management team experience: ___

**10. How good are company's cost analysis and accounting controls?**
- [ ] Unit economics tracked: Yes/No
- [ ] Cohort analysis: Yes/No
- [ ] KPI dashboard: ___

### Integrity & Shareholder Orientation (Points 11-15)

**11. Are there other aspects of the business, somewhat peculiar to the industry involved, which will give investor important clues as to how outstanding the company may be in relation to its competition?**
- [ ] Industry-specific advantages: ___

**12. Does company have a short-range or long-range outlook in regard to profits?**
- [ ] Evidence of long-term thinking: ___
- [ ] Sacrificing short-term for long-term: Yes/No

**13. Will the growth of the company require such large financing that shareholder dilution will cancel gains?**
- [ ] Dilution rate (3-year): ___%
- [ ] Share count trend: ___
- [ ] Is dilution value-destructive? Yes/No

**14. Does management talk freely to investors about affairs when things are going well but clam up when troubles occur?**
- [ ] Transparency during setbacks: ___
- [ ] Earnings call quality: ___

**15. Does company have a management of unquestionable integrity?**
- [ ] Track record: ___
- [ ] Red flags: ___
- [ ] Reference checks: ___

## LAYER 4: Growth Metrics & Unit Economics

### A. Total Addressable Market (TAM) Analysis

**TAM Sizing (CRITICAL for growth stocks):**

```
Top-Down TAM:
- Global market size: $___B
- Relevant segment: $___B
- CAGR (5-year projection): ___%
- TAM in 2029: $___B

Bottom-Up TAM:
- Target customers: ___ million
- × ARPU: $___ per year
- = TAM: $___B

Serviceable Addressable Market (SAM):
- Realistic market company can address: $___B
- Current penetration: ___%
- Runway remaining: ___
```

**TAM Expansion Evidence:**
- [ ] Market growing faster than company (room to grow)
- [ ] Company growing faster than market (taking share)
- [ ] TAM expanding due to new use cases
- [ ] International expansion opportunity

### B. SaaS & Subscription Metrics (If Applicable)

**Magic Number (Sales Efficiency):**
```
Magic Number = (ARR Added This Quarter × 4) / S&M Spend Previous Quarter

> 1.0 = ✅ Excellent (efficient growth)
0.75-1.0 = ✅ Good
0.5-0.75 = ⚠️ Moderate (need improvement)
< 0.5 = ❌ Inefficient (burning cash)

Company's Magic Number: ___
```

**Rule of 40:**
```
Rule of 40 = Revenue Growth % + FCF Margin %

> 40% = ✅ Excellent (can grow profitably)
25-40% = ✅ Good
< 25% = ⚠️ Growth expensive or slowing

Company's Rule of 40: ___%
```

**LTV/CAC Ratio:**
```
Customer Lifetime Value (LTV):
= (ARPU × Gross Margin %) / Monthly Churn Rate

Customer Acquisition Cost (CAC):
= Sales & Marketing Expense / New Customers Acquired

LTV / CAC Ratio:
> 3.0 = ✅ Excellent unit economics
2.0-3.0 = ✅ Good, sustainable
1.0-2.0 = ⚠️ Marginal (watch closely)
< 1.0 = ❌ Destroying value on each customer

Company's LTV/CAC: ___
CAC Payback Period: ___ months (< 12 months ideal)
```

**Net Revenue Retention (NRR):**
```
NRR = (Starting ARR + Upsells - Downgrades - Churn) / Starting ARR

> 120% = ✅✅ Exceptional (expanding within base)
110-120% = ✅ Excellent
100-110% = ✅ Good
< 100% = ❌ Losing revenue from existing customers

Company's NRR: ___%
```

### C. Cohort Analysis (If Data Available)

**Revenue Retention by Cohort:**

| Cohort (Year Acquired) | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 |
|------------------------|--------|--------|--------|--------|--------|
| 2020 | $100 | $120 | $135 | $142 | $150 |
| 2021 | $100 | $125 | $140 | $148 | - |
| 2022 | $100 | $128 | $145 | - | - |
| 2023 | $100 | $130 | - | - | - |
| 2024 | $100 | - | - | - | - |

**Analysis:**
- Are newer cohorts retaining better? ___
- Product-market fit improving? ___
- Customer satisfaction trends: ___

### D. PEG Ratio (Lynch's Favorite Valuation Tool)

```
PEG Ratio = (P/E Ratio) / (Earnings Growth Rate %)

< 1.0 = ✅ Undervalued relative to growth
1.0-1.5 = ✅ Fair value
1.5-2.0 = ⚠️ Getting expensive
> 2.0 = ❌ Overvalued (growth not justifying price)

Company's PEG Ratio: ___

CRITICAL: Use realistic growth rate
- Historical 3-year growth: ___%
- Analyst consensus: ___%
- Your estimate: ___%
- Which to use: ___% (justify: ___)
```

### E. Price/Sales with Gross Margin Filter

**For unprofitable growth companies:**

```
P/S Ratio = Market Cap / Annual Revenue
Current P/S: ___

Industry Comparison:
- High-margin SaaS (>70% GM): P/S 10-20x acceptable
- Medium-margin Tech (40-70% GM): P/S 5-10x acceptable
- Low-margin Business (<40% GM): P/S 1-5x acceptable

Company Gross Margin: ___%
Is P/S justified by margin? Yes/No
```

## LAYER 5: Competitive Positioning

### Moat Assessment (Early-Stage Version)

**For young companies, moat is often BUILDING, not proven:**

| Moat Type | Evidence | Strength |
|-----------|----------|----------|
| **Network Effects** | User growth accelerating? | Weak/Moderate/Strong |
| **Switching Costs** | Customer stickiness data | Weak/Moderate/Strong |
| **Brand** | NPS score, brand recognition | Weak/Moderate/Strong |
| **Proprietary Tech** | Patents, unique algorithms | Weak/Moderate/Strong |
| **Data Advantage** | More data = better product | Weak/Moderate/Strong |

**WARNING: Moat must DEEPEN over time**
- Is competitive advantage widening? ___
- Can it be replicated by well-funded competitor? ___
- What's the timeline to "unassailable" position? ___

### Competitive Landscape

```
Top 3 Competitors:
1. _______________ (Market Share: ___%, Growth: ___%)
2. _______________ (Market Share: ___%, Growth: ___%)
3. _______________ (Market Share: ___%, Growth: ___%)

Company's Market Share: ___%
Share Trend: Gaining/Stable/Losing

Competitive Advantages:
1. _______________
2. _______________
3. _______________

Competitive Risks:
1. _______________
2. _______________
3. _______________
```

## LAYER 6: Financial Health & Runway

### Cash Burn Analysis (Critical for Unprofitable Growers)

```
Current Cash & Equivalents: $___M
Quarterly Cash Burn: $___M
Runway: ___ quarters (>6 quarters = comfortable)

Path to Profitability:
- Current losses: $___M per quarter
- Expected breakeven: Q___ YYYY
- Credibility of plan: High/Medium/Low

Financing Risk:
- Will need to raise capital? Yes/No
- At what valuation vs current? ___
- Dilution risk: High/Medium/Low
```

### Balance Sheet

```
Current Ratio: ___ (>1.5 = healthy for growth co)
Debt/Equity: ___ (low ideal for growth stocks)
Interest Coverage: ___ (if applicable)

Red Flags:
- [ ] Negative working capital trending worse
- [ ] Debt increasing while growth slowing
- [ ] Accounts receivable growing faster than revenue
```

## LAYER 7: Risk Assessment

### Growth-Specific Risks

**The Lynch Warning Checklist:**
- [ ] ❌ Hot stock in hot industry (everyone talking about it)
- [ ] ❌ Whisper stock (rumored to cure cancer, solve energy, etc.)
- [ ] ❌ Customer concentration (>25% revenue from single customer)
- [ ] ❌ Name in the news constantly (hype often precedes fall)
- [ ] ❌ Doing something you don't understand
- [ ] ❌ Growth through acquisition (not organic)

**Structural Risks:**
```
1. TAM Risk: What if market doesn't grow as expected?
   Mitigation: ___

2. Competition Risk: What if FAANG enters this space?
   Mitigation: ___

3. Technology Risk: What if technology becomes obsolete?
   Mitigation: ___

4. Regulatory Risk: What if regulations change?
   Mitigation: ___

5. Key Person Risk: What if founder/CEO leaves?
   Mitigation: ___
```

### Scenario Analysis

**Bull Case (+50% upside):**
- TAM grows to: $___B
- Market share reaches: ___%
- Margins expand to: ___%
- Valuation multiple: ___x
- **Target Price: $___**

**Base Case (Expected):**
- TAM grows to: $___B
- Market share reaches: ___%
- Margins reach: ___%
- Valuation multiple: ___x
- **Target Price: $___**

**Bear Case (-30% downside):**
- TAM stalls at: $___B
- Market share stuck at: ___%
- Margins stuck at: ___%
- Valuation multiple: ___x
- **Target Price: $___**

**Risk/Reward Ratio:**
```
Upside: +___%
Downside: -___%
Ratio: ___:1

> 3:1 = ✅ Attractive
2:1 - 3:1 = ✅ Acceptable
< 2:1 = ⚠️ Unfavorable risk/reward
```

## LAYER 8: Catalysts & Timing

**Druckenmiller's Insight:**
> "The way to build long-term returns is through preservation of capital and home runs. You can be far more aggressive when you're making good profits."

### Identified Catalysts (Next 12-18 Months)

```
1. Product Launch: _______________ (Expected: Q___ YYYY)
2. Market Expansion: _______________ (Expected: Q___ YYYY)
3. Partnership Announcement: _______________ (Expected: ___)
4. Profitability Milestone: _______________ (Expected: ___)
5. Regulatory Approval: _______________ (Expected: ___)

Which catalyst has highest probability? ___
Which has biggest potential impact? ___
```

### Timing Considerations

```
Entry Timing:
- Current Price: $___
- Price 3 months ago: $___ (trend: ___)
- Near 52-week low/high? ___
- Recent insider buying? Yes/No
- Institutional accumulation? Yes/No

Optimal Entry Strategy:
[ ] Buy now (catalyst imminent)
[ ] Start position, add on strength
[ ] Wait for pullback to $___
[ ] Wait for catalyst confirmation
```

## Final Recommendation Template

```
═══════════════════════════════════════════════════
GROWTH STOCK ANALYSIS: _______________
═══════════════════════════════════════════════════

CLASSIFICATION:
Lynch Category: _______________
Data History: ___ years (since IPO/public)

INFLECTION POINT:
Type: _______________
Evidence: _______________
Conviction: High / Medium / Low

TAM & GROWTH:
Current TAM: $___B
5-Year TAM: $___B
Market Share Opportunity: ___%
Revenue Growth (3Y CAGR): ___%

UNIT ECONOMICS:
Magic Number: ___ (Sales Efficiency)
Rule of 40: ___% (Growth + Margin)
LTV/CAC: ___ (Unit Profitability)
NRR: ___% (Customer Expansion)

COMPETITIVE POSITION:
Moat Strength: Weak / Building / Moderate / Strong
Market Position: Leader / Challenger / Niche
Sustainable Advantage: ___

FINANCIAL HEALTH:
Cash Runway: ___ quarters
Path to Profitability: Clear / Uncertain
Dilution Risk: Low / Medium / High

VALUATION:
PEG Ratio: ___ (vs. 1.0 benchmark)
P/S Ratio: ___ (vs. ___ industry avg)
Implied Growth: ___% (vs. ___% historical)
Assessment: Undervalued / Fair / Overvalued

RISK/REWARD:
Bull Case: +___%
Base Case: +___%
Bear Case: -___%
Ratio: ___:1

CATALYSTS (Next 12 months):
1. _______________
2. _______________
3. _______________

RECOMMENDATION:
[ ] STRONG BUY - High Conviction Growth
[ ] BUY - Attractive Risk/Reward
[ ] SPECULATIVE BUY - Small Position, High Upside
[ ] HOLD - Monitor for Entry Point
[ ] PASS - Too Expensive or Risky

POSITION SIZING SUGGESTION: ___% of portfolio

KEY RISKS:
1. _______________
2. _______________
3. _______________

MONITORING TRIGGERS:
Sell if: _______________
Add if: _______________
Re-evaluate if: _______________

CONFIDENCE LEVEL: High / Medium / Low
═══════════════════════════════════════════════════
```

## Peter Lynch's "10-Bagger" Checklist

**Before investing in a growth stock, verify:**

✅ **The Company:**
- [ ] Company name sounds dull or ridiculous (less competition)
- [ ] Company does something dull (boring = overlooked)
- [ ] Company does something disagreeable (waste, funerals)
- [ ] It's a spinoff (unloved by parent, management incentivized)
- [ ] Institutions don't own it, analysts don't follow (undiscovered)
- [ ] Company is buying back shares (management believes)
- [ ] Insiders are buying (skin in the game)

✅ **The Fundamentals:**
- [ ] PEG ratio <1.0 (growth not fully priced)
- [ ] Strong balance sheet (can weather storms)
- [ ] FCF positive or clear path (not burning indefinitely)
- [ ] Niche market leader (pricing power)
- [ ] Product people need/buy repeatedly (recurring revenue)

✅ **The Story:**
- [ ] You can explain it to a 10-year-old
- [ ] You personally use/understand the product
- [ ] The growth story is logical and believable
- [ ] Management articulates vision clearly

## Remember

> "Go for a business that any idiot can run — because sooner or later, any idiot is probably going to run it."
> — Peter Lynch

> "The stock market is a device for transferring money from the impatient to the patient."
> — Warren Buffett

**For growth stocks:**
- Higher risk requires higher conviction
- Size positions based on uncertainty
- Exit quickly when thesis breaks
- Let winners run when thesis intact

This framework helps you find growth before it's obvious, while managing the inherent risks of early-stage investing.
