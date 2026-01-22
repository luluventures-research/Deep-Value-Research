---
name: stock-analysis-forensic
description: Deep forensic analysis of financial statements to detect accounting manipulation, hidden risks, and red flags. Use when investigating potential fraud, analyzing footnotes, detecting earnings quality issues, evaluating cash flow divergence, or conducting due diligence on suspicious companies. Focuses on what management is hiding.
allowed-tools: Read, Grep, Glob, Bash(python:*)
---

# Stock Analysis: Forensic Financial Framework

Detect accounting manipulation, hidden risks, and red flags through deep forensic analysis of financial statements. This skill implements a "trust but verify" approach to uncover what management doesn't want you to see.

## Philosophy: Hunting Cockroaches

> **"If you find one cockroach in the kitchen, there's a whole nest you haven't seen."**

**The Forensic Mindset:**
- Management controls what you see in financial statements
- Incentives often misaligned (bonuses tied to metrics)
- Footnotes contain truth the headlines hide
- One red flag usually signals multiple problems
- Skepticism is healthy; blind trust is dangerous

## When to Use This Skill

✅ **USE this skill when:**
- Investigating potential accounting fraud or manipulation
- Company has questionable earnings quality
- OCF diverging significantly from Net Income
- Analyzing footnotes in 10-K/10-Q
- Due diligence on acquisition target
- Evaluating short-seller reports
- Something "feels off" about the numbers
- Recent restatements or auditor changes

❌ **DO NOT use this skill when:**
- Need comprehensive long-term analysis → Use `/stock-analysis-buffett-longterm`
- Analyzing growth company fundamentals → Use `/stock-analysis-growth`
- Quick metric screening → Use `/stock-analysis-quick-metrics`

## CRITICAL RED FLAGS - Immediate Investigation Required

If ANY of these are present, conduct full forensic audit:

### Tier 1: Critical Red Flags (Potential Fraud)

- [ ] ❌ **Auditor resigned or was fired** (especially if didn't finish term)
- [ ] ❌ **CFO or CEO sudden departure** without clear succession
- [ ] ❌ **Multiple restatements** in past 3 years
- [ ] ❌ **Qualified audit opinion** or "going concern" warning
- [ ] ❌ **Related-party transactions >5% of revenue** without business justification
- [ ] ❌ **Channel stuffing evidence** (DSO spiking, unusual Q4 revenue concentration)
- [ ] ❌ **Frequent changes in accounting policies** (depreciation, revenue recognition)
- [ ] ❌ **Large goodwill impairments** repeatedly
- [ ] ❌ **Insider selling >50% of holdings** (especially if multiple executives)
- [ ] ❌ **SEC investigation or subpoena** disclosed in filings

**Action if ANY Tier 1 present:** Deep investigation required before any investment consideration

### Tier 2: Warning Red Flags (Earnings Quality Issues)

- [ ] ⚠️ **Net Income growing >20% faster than OCF** for 3+ consecutive years
- [ ] ⚠️ **Accounts Receivable growing >15% faster than Revenue** (2+ years)
- [ ] ⚠️ **Inventory growing >15% faster than COGS** (2+ years)
- [ ] ⚠️ **Depreciation useful life extended** in recent years
- [ ] ⚠️ **Sudden spike in "Other Income"** (>10% of Net Income)
- [ ] ⚠️ **Stock-Based Compensation >15% of Net Income** (massive dilution)
- [ ] ⚠️ **Deferred revenue declining** while revenue growing (SaaS red flag)
- [ ] ⚠️ **Days Sales Outstanding (DSO) >90 days** or increasing trend
- [ ] ⚠️ **Debt increasing while revenue flat/declining**
- [ ] ⚠️ **Working capital consistently negative** and worsening

**Action if 2+ Tier 2 present:** Detailed forensic review recommended

## LAYER 1: Income Statement Forensic Analysis

### The Three Margins Hierarchy

**Analyze 5-year trend for ALL three margins:**

| Year | Gross Margin | Operating Margin | Net Margin | Quality Score |
|------|--------------|------------------|------------|---------------|
| 2020 | X% | X% | X% | ✅/⚠️/❌ |
| 2021 | X% | X% | X% | ✅/⚠️/❌ |
| 2022 | X% | X% | X% | ✅/⚠️/❌ |
| 2023 | X% | X% | X% | ✅/⚠️/❌ |
| 2024 | X% | X% | X% | ✅/⚠️/❌ |

**Quality Scoring:**
- ✅ **Healthy**: All three margins stable or expanding together
- ⚠️ **Warning**: Net Margin expanding while Gross/Operating stable or declining
- ❌ **Red Flag**: Net Margin up significantly, but Gross/Operating down

**The Margin Inversion Red Flag:**

```
If Net Margin ↑ while Gross Margin ↓ → INVESTIGATE

Possible causes:
1. One-time gains inflating Net Income (asset sales, tax benefits)
2. Cutting OpEx unsustainably (R&D, marketing)
3. Accounting tricks (capitalizing expenses, extending depreciation)
4. Financial engineering (debt refinancing gains)

Required: Read MD&A and footnotes to identify source
```

### Revenue Quality Analysis

#### Test 1: Revenue Recognition Policy Changes

**Check for in 10-K footnotes:**
- [ ] Has revenue recognition policy changed in past 3 years?
- [ ] If yes, what was impact on revenue? $___
- [ ] Was change disclosed prominently? Yes/No
- [ ] Does change align with new accounting standard (ASC 606) or management discretion?

**Red Flag:** Management discretion changes that boost revenue

#### Test 2: Revenue Concentration Risk

```
Top 5 Customers as % of Revenue:
Customer 1: ___%
Customer 2: ___%
Customer 3: ___%
Customer 4: ___%
Customer 5: ___%
TOTAL: ___%

> 50% = ❌ Critical concentration risk
25-50% = ⚠️ High concentration risk
< 25% = ✅ Diversified

Action: If >25%, identify customers and assess loss risk
```

#### Test 3: Seasonality & Q4 Loading

**Quarterly Revenue Pattern:**

| Q1 | Q2 | Q3 | Q4 | Total |
|----|----|----|----|----|
| __% | __% | __% | __% | 100% |

**Red Flags:**
- Q4 >40% of annual revenue (potential channel stuffing)
- Q4 revenue suddenly spiking vs. historical pattern
- Q4 miss followed by Q1 inventory returns

**Required:** Compare to industry norms for seasonality

### Expense Manipulation Detection

#### Test 4: Depreciation & Amortization Changes

**Useful Life Analysis:**

| Asset Class | Previous Life | Current Life | Change | Impact on Earnings |
|-------------|---------------|--------------|--------|-------------------|
| Buildings | ___ years | ___ years | +/- ___ | $___M |
| Equipment | ___ years | ___ years | +/- ___ | $___M |
| Software | ___ years | ___ years | +/- ___ | $___M |

**Red Flag:** Extending useful life increases earnings artificially

**Recalculation Required:**
```
If useful life extended:
1. Calculate depreciation using OLD useful life
2. Compare to REPORTED depreciation
3. Difference = Artificial earnings boost

Adjusted Net Income = Reported - Artificial Boost
```

#### Test 5: Capitalization vs. Expensing

**CapEx Breakdown (from Cash Flow Statement + Footnotes):**

```
Total CapEx: $___M

Breakdown:
- Maintenance CapEx: $___M (___%)
- Growth CapEx: $___M (___%)
- Capitalized Software Development: $___M (___%)
- Capitalized Interest: $___M (___%)

Red Flags:
- [ ] Capitalized software >30% of total CapEx (aggressive)
- [ ] Maintenance CapEx declining while assets aging
- [ ] R&D expenses declining while "capitalized development" increasing
```

**Aggressive Capitalization Test:**
```
If company capitalizes development costs:

1. Find "Capitalized Development Costs" on balance sheet
2. Find "Amortization of Capitalized Costs" in footnotes
3. Compare: New Capitalization vs. Amortization

If New Cap > Amortization by >50% for 3+ years:
= ⚠️ Potentially deferring expenses to inflate earnings
```

#### Test 6: One-Time Items & Adjustments

**"Adjusted" Earnings Reconciliation:**

```
Reported Net Income: $___M

Management's "Adjustments":
+ Restructuring charges: $___M
+ Acquisition costs: $___M
+ Impairment charges: $___M
+ Legal settlements: $___M
+ "Other" adjustments: $___M
= "Adjusted" Net Income: $___M

Frequency Test:
- Are "one-time" charges recurring every year? Yes/No
- Is "Adjusted" earnings >20% higher than GAAP? Yes/No

❌ Red Flag: "One-time" charges that happen every year aren't one-time
```

## LAYER 2: Cash Flow Statement Forensic Analysis

### The Ultimate Test: OCF vs. Net Income

**5-Year Divergence Analysis:**

| Year | Net Income | Operating CF | OCF/NI Ratio | Quality |
|------|------------|--------------|--------------|---------|
| 2020 | $___M | $___M | ___ | ✅/⚠️/❌ |
| 2021 | $___M | $___M | ___ | ✅/⚠️/❌ |
| 2022 | $___M | $___M | ___ | ✅/⚠️/❌ |
| 2023 | $___M | $___M | ___ | ✅/⚠️/❌ |
| 2024 | $___M | $___M | ___ | ✅/⚠️/❌ |

**Quality Scoring:**
- ✅ **High Quality**: OCF/NI ratio >1.0 consistently (cash exceeds earnings)
- ⚠️ **Moderate Quality**: OCF/NI ratio 0.8-1.0 (earnings mostly convert to cash)
- ❌ **Low Quality**: OCF/NI ratio <0.8 for 2+ years (earnings not converting to cash)

**Critical Red Flag:**
```
If Net Income growing but OCF flat/declining for 3+ years:
= ❌ EARNINGS QUALITY EXTREMELY QUESTIONABLE

Investigate:
- Working capital manipulation
- Aggressive revenue recognition
- Expense capitalization
- Channel stuffing

Action: Assume earnings are inflated until proven otherwise
```

### Working Capital Manipulation Detection

#### Test 7: Accounts Receivable Analysis (Channel Stuffing)

**Days Sales Outstanding (DSO) Trend:**

```
DSO = (Accounts Receivable / Revenue) × 365

| Year | A/R | Revenue | DSO | Change | Industry Avg |
|------|-----|---------|-----|--------|--------------|
| 2020 | $___M | $___M | ___ days | - | ___ days |
| 2021 | $___M | $___M | ___ days | +___ | ___ days |
| 2022 | $___M | $___M | ___ days | +___ | ___ days |
| 2023 | $___M | $___M | ___ days | +___ | ___ days |
| 2024 | $___M | $___M | ___ days | +___ | ___ days |

Red Flags:
- [ ] DSO increasing >10 days per year
- [ ] DSO >Industry average by >20 days
- [ ] A/R growing >15% faster than Revenue

WARNING: Rising DSO = Potential channel stuffing or collection problems
```

**The Channel Stuffing Test:**
```
If DSO rising significantly:

1. Check Q4 revenue spike (channel stuffing often happens in Q4)
2. Check Q1 returns/credits (stuffed channel returns product)
3. Check allowance for doubtful accounts (should rise with DSO)
4. Check customer concentration (stuffing often to few customers)
5. Read MD&A for explanation

If no credible explanation = ❌ Assume channel stuffing
```

#### Test 8: Inventory Analysis

**Days Inventory Outstanding (DIO) Trend:**

```
DIO = (Inventory / COGS) × 365

| Year | Inventory | COGS | DIO | Change | Industry Avg |
|------|-----------|------|-----|--------|--------------|
| 2020 | $___M | $___M | ___ days | - | ___ days |
| 2021 | $___M | $___M | ___ days | +___ | ___ days |
| 2022 | $___M | $___M | ___ days | +___ | ___ days |
| 2023 | $___M | $___M | ___ days | +___ | ___ days |
| 2024 | $___M | $___M | ___ days | +___ | ___ days |

Red Flags:
- [ ] DIO increasing while revenue slowing (unsold inventory piling up)
- [ ] Inventory growing >15% faster than COGS
- [ ] DIO >Industry average by >20 days

WARNING: Rising DIO = Overproduction, obsolescence, or demand weakness
```

**Inventory Quality Analysis:**

```
Check inventory footnote for composition:
- Raw materials: $___M (___%)
- Work in progress: $___M (___%)
- Finished goods: $___M (___%)

Red Flag: Finished goods >60% (hardest to sell, most obsolescence risk)

Check inventory reserves:
- Inventory reserve: $___M
- As % of gross inventory: ___%
- Trend: Increasing/Stable/Decreasing

Red Flag: Reserves declining while DIO rising (hiding obsolescence)
```

#### Test 9: Accounts Payable Analysis

**Days Payable Outstanding (DPO) Trend:**

```
DPO = (Accounts Payable / COGS) × 365

| Year | A/P | COGS | DPO | Change | Industry Avg |
|------|-----|------|-----|--------|--------------|
| 2020 | $___M | $___M | ___ days | - | ___ days |
| 2021 | $___M | $___M | ___ days | +___ | ___ days |
| 2022 | $___M | $___M | ___ days | +___ | ___ days |
| 2023 | $___M | $___M | ___ days | +___ | ___ days |
| 2024 | $___M | $___M | ___ days | +___ | ___ days |

Red Flags:
- [ ] DPO increasing >15 days per year (delaying payments)
- [ ] Sudden spike in A/P without revenue growth (cash flow crisis)
- [ ] DPO >Industry average by >30 days (supplier relationship stress)

WARNING: Rising DPO = Cash flow stress, delaying supplier payments
```

**Cash Conversion Cycle (CCC):**

```
CCC = DSO + DIO - DPO

| Year | DSO | DIO | DPO | CCC | Trend |
|------|-----|-----|-----|-----|-------|
| 2020 | ___ | ___ | ___ | ___ days | - |
| 2021 | ___ | ___ | ___ | ___ days | Better/Worse |
| 2022 | ___ | ___ | ___ | ___ days | Better/Worse |
| 2023 | ___ | ___ | ___ | ___ days | Better/Worse |
| 2024 | ___ | ___ | ___ | ___ days | Better/Worse |

Interpretation:
- CCC declining = ✅ Working capital efficiency improving
- CCC rising = ⚠️ More cash tied up in operations
- CCC >100 days = ⚠️ Capital intensive, watch closely
```

### Free Cash Flow Quality

#### Test 10: FCF Sustainability

**True Free Cash Flow Calculation:**

```
Operating Cash Flow: $___M
Less:
- Maintenance CapEx: $___M (estimate from footnotes)
- Stock-Based Comp (cash portion): $___M
= Adjusted Free Cash Flow: $___M

Compare to Reported FCF: $___M
Difference: $___M

Red Flags:
- [ ] Company doesn't disclose maintenance vs growth CapEx
- [ ] Reported FCF includes "adjustments" >10%
- [ ] CapEx declining while PPE aging (deferred maintenance)
```

**FCF Conversion Test:**

```
FCF Margin = FCF / Revenue

| Year | FCF | Revenue | FCF Margin | NI Margin | Conversion |
|------|-----|---------|------------|-----------|------------|
| 2020 | $___M | $___M | __% | __% | __% |
| 2021 | $___M | $___M | __% | __% | __% |
| 2022 | $___M | $___M | __% | __% | __% |
| 2023 | $___M | $___M | __% | __% | __% |
| 2024 | $___M | $___M | __% | __% | __% |

Target: FCF Margin >80% of NI Margin (high conversion)
Red Flag: FCF Margin <50% of NI Margin for 3+ years
```

## LAYER 3: Balance Sheet Forensic Analysis

### Asset Quality Assessment

#### Test 11: Goodwill & Intangibles Analysis

**Goodwill as % of Total Assets:**

```
| Year | Goodwill | Intangibles | Total Assets | Goodwill % | Quality |
|------|----------|-------------|--------------|------------|---------|
| 2020 | $___M | $___M | $___M | __% | ✅/⚠️/❌ |
| 2021 | $___M | $___M | $___M | __% | ✅/⚠️/❌ |
| 2022 | $___M | $___M | $___M | __% | ✅/⚠️/❌ |
| 2023 | $___M | $___M | $___M | __% | ✅/⚠️/❌ |
| 2024 | $___M | $___M | $___M | __% | ✅/⚠️/❌ |

Quality Scoring:
- ✅ Good: Goodwill <25% of total assets
- ⚠️ Warning: Goodwill 25-50% of total assets
- ❌ Red Flag: Goodwill >50% of total assets

CRITICAL: If >50%, most "assets" are intangible (acquisition premium)
```

**Impairment History:**

```
Goodwill impairments (past 5 years):
Year | Amount | % of Goodwill | Reason
_____|________|_______________|________
2020 | $___M | __% | ___
2021 | $___M | __% | ___
2022 | $___M | __% | ___
2023 | $___M | __% | ___
2024 | $___M | __% | ___

Red Flags:
- [ ] Repeated impairments (poor M&A track record)
- [ ] Large impairment (>20% of goodwill in single year)
- [ ] Impairments soon after acquisition (overpaid)
```

**Goodwill by Reporting Unit (from footnotes):**

```
Check if goodwill concentrated in specific units:
Unit A: $___M (at risk? Yes/No - why: ___)
Unit B: $___M (at risk? Yes/No - why: ___)
Unit C: $___M (at risk? Yes/No - why: ___)

Future impairment risk: Low / Medium / High
```

#### Test 12: Off-Balance Sheet Liabilities

**Operating Leases (Check footnotes):**

```
Future operating lease commitments:
Within 1 year: $___M
1-3 years: $___M
3-5 years: $___M
After 5 years: $___M
TOTAL: $___M

As % of Total Debt: ___%

Red Flag: >50% of stated debt (large hidden obligation)
```

**Other Off-Balance Sheet Items:**
- [ ] Joint ventures: $___M
- [ ] Special purpose entities: $___M
- [ ] Guarantees: $___M
- [ ] Purchase commitments: $___M

**Total Hidden Liabilities: $___M**

#### Test 13: Pension & Retirement Obligations

**Pension Status (from footnotes):**

```
Projected Benefit Obligation (PBO): $___M
Fair Value of Plan Assets: $___M
Funded Status: $___M (Deficit/Surplus)

Funded Ratio = Assets / PBO = ___%

< 80% = ❌ Significantly underfunded
80-100% = ⚠️ Underfunded
> 100% = ✅ Overfunded

Assumptions Check:
- Discount rate: __% (vs. industry: __%)
- Expected return on assets: __% (realistic? Yes/No)
- Salary increase assumption: __% (conservative? Yes/No)

Red Flag: Overly optimistic assumptions reduce reported liability
```

### Debt Quality & Sustainability

#### Test 14: Debt Maturity Profile

**Debt Schedule (from footnotes):**

```
Current portion (due <1 year): $___M
Due in 1-2 years: $___M
Due in 2-3 years: $___M
Due in 3-5 years: $___M
Due after 5 years: $___M
TOTAL: $___M

Refinancing Risk Assessment:
- Debt due in next 2 years: $___M
- Current cash + OCF (annual): $___M
- Can service without refinancing? Yes/No

Red Flags:
- [ ] >30% of debt due within 2 years
- [ ] Insufficient cash/OCF to service debt
- [ ] Debt maturing in rising rate environment
```

#### Test 15: Debt Covenants

**Covenant Analysis (from credit agreement footnotes):**

```
Key covenants:
1. Debt/EBITDA < ___ (Current: ___, Cushion: __%)
2. Interest Coverage > ___ (Current: ___, Cushion: __%)
3. Minimum Liquidity > $___ (Current: $___, Cushion: __%)
4. Other: ___

Covenant Cushion Score:
>20% cushion = ✅ Comfortable
10-20% cushion = ⚠️ Watch closely
<10% cushion = ❌ High risk of breach

Most at-risk covenant: ___
Likelihood of breach: Low / Medium / High
Consequences if breached: ___
```

## LAYER 4: Footnote Forensic Deep Dive

### The Footnote Priority List

**Read in this order (most important first):**

1. **Significant Accounting Policies** (Footnote 1 or 2)
   - [ ] Revenue recognition policy
   - [ ] Depreciation methods & useful lives
   - [ ] Inventory valuation method
   - [ ] Goodwill impairment testing
   - Any changes? Yes/No - Impact: ___

2. **Revenue Recognition** (Usually Footnote 2 or 3)
   - [ ] Multiple revenue streams?
   - [ ] Deferred revenue trends
   - [ ] Unbilled receivables
   - [ ] Customer concentration

3. **Related-Party Transactions** (Usually near end)
   - [ ] Transactions with executives/directors
   - [ ] Transactions with affiliates
   - [ ] Terms: Arms-length? Yes/No
   - Total amount: $___M (___% of revenue)

4. **Commitments & Contingencies**
   - [ ] Legal proceedings
   - [ ] Environmental liabilities
   - [ ] Guarantees & indemnifications
   - Potential exposure: $___M

5. **Stock-Based Compensation**
   - [ ] Total SBC expense: $___M
   - As % of Net Income: ___%
   - Dilution from options: ___%
   - Repricing history: Yes/No

6. **Segment Reporting**
   - [ ] Which segments profitable?
   - [ ] Which segments growing?
   - [ ] Profitability by segment
   - Cross-subsidization? Yes/No

### Related-Party Transaction Red Flags

**Detailed Analysis Required:**

```
Transaction Type | Counterparty | Amount | % of Total | Red Flag?
_______________|______________|________|____________|___________
Sales to affiliate | ___ | $___M | __% | Yes/No
Purchases from affiliate | ___ | $___M | __% | Yes/No
Loans to executives | ___ | $___M | __% | Yes/No
Property lease from CEO | ___ | $___M | __% | Yes/No
Consulting fees to family | ___ | $___M | __% | Yes/No

Critical Questions:
1. Are terms disclosed as "arms-length"? Yes/No
2. Are prices comparable to third-party? Yes/No
3. Is there legitimate business purpose? Yes/No
4. Is disclosure prominent and clear? Yes/No

If ANY "No" → ❌ Investigate potential self-dealing
```

## LAYER 5: Management & Governance Forensics

### Insider Trading Analysis

**Recent Insider Transactions (6 months):**

```
| Date | Insider | Position | Type | Shares | Price | Value |
|------|---------|----------|------|--------|-------|-------|
| ___ | ___ | CEO | Sell | ___ | $___ | $___M |
| ___ | ___ | CFO | Sell | ___ | $___ | $___M |
| ___ | ___ | Director | Buy | ___ | $___ | $___M |

Pattern Analysis:
- Insider buying: ___ transactions, $___M total
- Insider selling: ___ transactions, $___M total
- Net: ___

Red Flags:
- [ ] CEO/CFO selling >50% of holdings
- [ ] Multiple executives selling simultaneously
- [ ] Selling accelerating before earnings miss
- [ ] No insider buying in past 2 years

Green Flags:
- [ ] Insiders buying in open market
- [ ] Executives increasing stake
- [ ] Selling only for 10b5-1 plans (scheduled)
```

### Compensation Alignment

**Executive Compensation Analysis (from DEF 14A):**

```
CEO Total Compensation: $___M
Breakdown:
- Base salary: $___M
- Bonus: $___M
- Stock options: $___M
- Other: $___M

Metrics for bonus/options:
1. ___ (___% weight)
2. ___ (___% weight)
3. ___ (___% weight)

Red Flags:
- [ ] Bonuses based on "adjusted" earnings (easy to manipulate)
- [ ] Short-term metrics (quarterly) vs long-term (3+ years)
- [ ] No clawback provisions
- [ ] Options repriced after stock decline
- [ ] Peers selection questionable (inflates compensation)

Green Flags:
- [ ] Long-term metrics (3-5 year vesting)
- [ ] FCF or ROIC based (quality metrics)
- [ ] Significant stock ownership requirement
- [ ] Clawback for misconduct/restatements
```

### Board Independence

```
Board Composition:
- Total directors: ___
- Independent directors: ___ (___%)
- Former executives: ___
- Family members: ___

Key Committee Independence:
- Audit Committee: ___% independent
- Compensation Committee: ___% independent
- Nominating Committee: ___% independent

Red Flags:
- [ ] Board <50% independent
- [ ] Audit committee not 100% independent
- [ ] Long-tenured directors (>15 years)
- [ ] Directors serve on >5 boards (overextended)
- [ ] CEO also serves as Chairman (poor governance)

Audit Committee Financial Expertise:
- Members with accounting background: ___
- CPA on committee: Yes/No
Red Flag: No financial expert on audit committee
```

## LAYER 6: Auditor & Regulatory Analysis

### Auditor Assessment

```
Current Auditor: _______________
Tenure: ___ years

Auditor Quality Tier:
[ ] Big 4 (Deloitte, PwC, EY, KPMG) - Highest quality
[ ] Second-tier national firm - Good quality
[ ] Regional firm - Acceptable
[ ] Unknown/small firm - ⚠️ Red flag for public company

Auditor Changes (past 5 years):
Year | Old Auditor | New Auditor | Reason Given | Red Flag?
_____|_____________|_____________|______________|___________
___ | ___ | ___ | ___ | Yes/No

Critical Red Flags:
- [ ] Auditor resigned (vs. fired) - very serious
- [ ] Change happened mid-year (emergency)
- [ ] Multiple changes in 5 years
- [ ] Downgrade from Big 4 to smaller firm
- [ ] Reason: "Disagreement on accounting" - CRITICAL

Audit Opinion:
- [ ] Unqualified/Clean opinion ✅
- [ ] Qualified opinion (except for...) ⚠️
- [ ] Adverse opinion ❌
- [ ] Disclaimer of opinion ❌
- [ ] Going concern warning ❌

Audit Fees:
- Audit fees: $___M
- Audit-related fees: $___M
- Tax fees: $___M
- All other fees: $___M
- TOTAL: $___M

Red Flag: Non-audit fees >50% of total (independence question)
```

### SEC Filings & Regulatory

```
Recent SEC Actions:
- [ ] SEC comment letters (past 2 years): ___
- [ ] SEC investigation disclosed: Yes/No
- [ ] Restatements required: ___
- [ ] Late filings (NT 10-K/Q): ___

Comment Letter Analysis:
Topic of SEC questions:
1. ___
2. ___
3. ___

Management's response quality: Transparent / Evasive / Unclear

Red Flags:
- [ ] Multiple comment letters on same topic
- [ ] Formal investigation disclosed
- [ ] Wells notice received
- [ ] Restatement ordered by SEC
```

## LAYER 7: Industry-Specific Red Flags

### Sector-Specific Warning Signs

**Technology/SaaS:**
- [ ] Deferred revenue declining (bookings slowing)
- [ ] CAC payback >24 months (inefficient growth)
- [ ] Negative NRR (losing existing customers)
- [ ] Stock-based comp >30% of revenue (massive dilution)

**Retail:**
- [ ] Same-store sales declining (losing to competition)
- [ ] Inventory turns slowing (merchandise not selling)
- [ ] EBITDA includes "non-cash rent" (hiding real costs)
- [ ] Store closure accruals insufficient

**Manufacturing:**
- [ ] Utilization rates declining (excess capacity)
- [ ] Scrap/waste increasing (quality issues)
- [ ] Warranty reserves declining while sales up (hiding issues)
- [ ] PPE aging but CapEx declining (deferred maintenance)

**Financial Services:**
- [ ] Loan loss reserves declining while NPLs rising
- [ ] Tier 1 capital ratio declining
- [ ] Net interest margin compressing
- [ ] Off-balance sheet vehicles growing

**Energy/Resources:**
- [ ] Reserve replacement ratio <100% (depleting reserves)
- [ ] Finding & development costs rising
- [ ] Proved developed reserves declining
- [ ] Hedges unwinding (price exposure)

## Final Forensic Risk Score

```
═══════════════════════════════════════════════════
FORENSIC ANALYSIS SUMMARY: _______________
═══════════════════════════════════════════════════

TIER 1 RED FLAGS (Critical - Potential Fraud):
Count: ___ / 10
Specific flags: ___
Assessment: None / Few / Multiple

TIER 2 RED FLAGS (Earnings Quality Issues):
Count: ___ / 10
Specific flags: ___
Assessment: None / Few / Multiple

FORENSIC TEST RESULTS:

Income Statement Quality:
- Margin trend: ✅ / ⚠️ / ❌
- Revenue quality: ✅ / ⚠️ / ❌
- Expense manipulation: None / Possible / Likely

Cash Flow Quality:
- OCF vs NI: ✅ / ⚠️ / ❌
- Working capital: ✅ / ⚠️ / ❌
- FCF sustainability: ✅ / ⚠️ / ❌

Balance Sheet Quality:
- Asset quality: ✅ / ⚠️ / ❌
- Liability transparency: ✅ / ⚠️ / ❌
- Debt sustainability: ✅ / ⚠️ / ❌

Governance & Management:
- Insider alignment: ✅ / ⚠️ / ❌
- Board independence: ✅ / ⚠️ / ❌
- Auditor quality: ✅ / ⚠️ / ❌

OVERALL FORENSIC SCORE:
Points: ___/100

90-100 = ✅✅ Clean - High confidence in financials
70-89 = ✅ Good - Minor issues, acceptable
50-69 = ⚠️ Caution - Significant concerns, investigate further
<50 = ❌ High Risk - Multiple red flags, avoid

SPECIFIC CONCERNS IDENTIFIED:
1. _______________
2. _______________
3. _______________

INVESTIGATION PRIORITY:
[ ] Immediate deep dive required (Tier 1 flags present)
[ ] Further research recommended (multiple Tier 2 flags)
[ ] Monitor closely (some concerns)
[ ] Acceptable for investment consideration (clean)

RECOMMENDATION:
[ ] AVOID - Too many red flags
[ ] HIGH RISK - Only for sophisticated investors
[ ] PROCEED WITH CAUTION - Monitor closely
[ ] ACCEPTABLE - Concerns manageable

NEXT STEPS:
1. _______________
2. _______________
3. _______________
═══════════════════════════════════════════════════
```

## Remember

> **"Price is what you pay. Value is what you get. But sometimes price is what you pay, and fraud is what you get."**

**Key Forensic Principles:**
1. Trust, but verify - Always
2. One cockroach means many more
3. Footnotes tell the truth headlines hide
4. Cash doesn't lie, but accounting does
5. If it's too complex to understand, it's too risky to own

**When in doubt, stay out.** The best investment is the one you didn't make in a company cooking the books.
