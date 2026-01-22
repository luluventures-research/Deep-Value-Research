# Investment Research Skills for Claude Code

This directory contains specialized skills for comprehensive stock analysis based on your value investing research frameworks.

## Available Skills

### 1. `/stock-analysis-buffett-longterm` ⭐ **PRIMARY FOR VALUE INVESTING**

**Purpose:** Comprehensive multi-decade analysis for mature companies using Buffett's forever-hold framework

**When to use:**
- Company has 10+ years of public financial data
- Evaluating "forever hold" investment candidates
- Building retirement/long-term portfolio
- Need recession-tested businesses
- Want Buffett's actual investment standards

**Key features:**
- ✅ **GATE ZERO**: Enforces 10+ year data requirement FIRST
- ✅ Multi-decade analysis (20-30 year track records ideal)
- ✅ Recession-by-recession testing (2008-09, 2020)
- ✅ Moat durability assessment over decades
- ✅ Owner Earnings focus (not GAAP earnings)
- ✅ Consistency scorecards (100-point rating)
- ✅ Confidence adjustment based on data availability
- ✅ Year-by-year tables required (not just averages)

**Minimum requirement:** Company MUST have 10+ years of audited public data

**Invoke with:** `/stock-analysis-buffett-longterm`

**Supporting reference files:**
- `MOAT_REFERENCE.md` - Deep dive on competitive moat types and testing
- `OWNER_EARNINGS.md` - Comprehensive Owner Earnings calculation guide
- `RECESSION_ANALYSIS.md` - Historical recession impact analysis framework

---

### 2. `/stock-analysis-growth` **FOR HIGH-GROWTH COMPANIES**

**Purpose:** Analyze high-growth companies using Peter Lynch, Stanley Druckenmiller, and Philip Fisher methodologies

**When to use:**
- Company has <10 years of public financial data
- Fast growers (15-25%+ annual growth)
- Recent IPOs or young public companies
- TAM expansion opportunities
- Identifying inflection points
- Unit economics and SaaS metrics evaluation

**Key features:**
- ✅ Peter Lynch's GARP methodology (PEG ratio, six categories, ten-bagger thinking)
- ✅ Druckenmiller's inflection point framework (5 types)
- ✅ Philip Fisher's 15-point scuttlebutt method
- ✅ Growth-specific metrics (TAM, LTV/CAC, Rule of 40, Magic Number)
- ✅ SaaS metrics (NRR, CAC payback, cohort analysis)
- ✅ Forward-looking potential analysis
- ✅ Scenario-based valuation (bull/base/bear cases)

**Philosophy:** Growth investing focuses on forward-looking potential before it's obvious to everyone

**Invoke with:** `/stock-analysis-growth`

---

### 3. `/stock-analysis-forensic` **FOR RED FLAG DETECTION**

**Purpose:** Deep forensic analysis of financial statements to detect accounting manipulation, hidden risks, and fraud

**When to use:**
- Investigating potential accounting fraud or manipulation
- Company has questionable earnings quality
- OCF diverging significantly from Net Income
- Analyzing footnotes in 10-K/10-Q
- Due diligence on acquisition target
- Evaluating short-seller reports
- Something "feels off" about the numbers
- Recent restatements or auditor changes

**Key features:**
- ✅ "Hunting Cockroaches" philosophy (one red flag = many more hidden)
- ✅ Tier 1 & 2 Red Flag checklists (automatic investigation triggers)
- ✅ Income Statement forensics (margin inversion detection)
- ✅ Cash Flow forensics (OCF vs NI divergence analysis)
- ✅ Balance Sheet forensics (goodwill, off-balance sheet liabilities)
- ✅ Working capital manipulation detection (DSO, DIO, DPO)
- ✅ Footnote deep dive priorities
- ✅ Management & governance forensics
- ✅ Industry-specific red flags

**Philosophy:** Trust but verify - Management controls what you see, footnotes contain what they hide

**Invoke with:** `/stock-analysis-forensic`

---

### 4. `/stock-analysis-quick-metrics` **FOR FAST SCREENING**

**Purpose:** Fast financial metrics screening and calculation for quick company evaluation

**When to use:**
- Need quick screening of multiple companies
- Want fast calculation of key metrics
- Initial evaluation before deep dive
- Comparing companies side-by-side
- Validating a quick investment idea
- Checking if company meets basic criteria

**Key features:**
- ✅ 6 Critical Numbers filter (30-second screening)
- ✅ Profitability quick check (ROE, ROA, ROIC, margins)
- ✅ Cash flow quality test (OCF/NI ratio, FCF margin)
- ✅ Balance sheet health (liquidity, leverage ratios)
- ✅ Valuation quick check (P/E, P/B, PEG, EV/EBITDA)
- ✅ Sector-specific screening templates
- ✅ Quick comparison tables for multiple companies
- ✅ Red flag quick checklist (instant disqualifiers)

**Philosophy:** Screen fast to say "NO" quickly to 90% of companies, so you can analyze the top 10% deeply

**Invoke with:** `/stock-analysis-quick-metrics`

---

### 5. `/value-investing-principles` **GENERAL FRAMEWORK**

**Purpose:** General value investing knowledge and principles (already existed)

**When to use:**
- Questions about value investing philosophy
- Understanding Buffett-Munger methodology
- Learning about valuation principles
- General investment education

**Invoke with:** `/value-investing-principles`

---

## Skill Selection Decision Tree

```
START: Need to analyze a company
  ↓
Does company have 10+ years of public data?
  ├─ YES ↓
  │    What type of analysis needed?
  │    ├─ Comprehensive long-term analysis → /stock-analysis-buffett-longterm ⭐
  │    ├─ Something seems suspicious → /stock-analysis-forensic
  │    └─ Quick initial screening → /stock-analysis-quick-metrics
  │
  └─ NO ↓
       Is it a high-growth company (<10 years, 15%+ growth)?
       ├─ YES → /stock-analysis-growth
       └─ NO → /stock-analysis-quick-metrics (then decide if worth deeper analysis)

SPECIAL CASES:
- Investigating fraud/manipulation → /stock-analysis-forensic (regardless of company age)
- Quick comparison of 5+ companies → /stock-analysis-quick-metrics
- Learning value investing concepts → /value-investing-principles
```

---

## Typical Analysis Workflow

### For Mature Companies (10+ years data):

```
Step 1: Quick Screening
Use /stock-analysis-quick-metrics
- Calculate 6 critical numbers
- Check if passes minimum standards
- If PASS → Continue
- If FAIL → Move to next company

Step 2: Comprehensive Analysis
Use /stock-analysis-buffett-longterm
- Full 10-20 year historical analysis
- Recession testing
- Moat assessment
- Owner Earnings calculation
- Investment decision

Step 3: If Red Flags Appear
Use /stock-analysis-forensic
- Deep dive into suspicious items
- Verify accounting quality
- Check for manipulation
- Final go/no-go decision
```

### For Growth Companies (<10 years data):

```
Step 1: Quick Screening
Use /stock-analysis-quick-metrics
- Check growth metrics (Rule of 40, PEG ratio)
- Verify unit economics
- If attractive → Continue

Step 2: Growth Analysis
Use /stock-analysis-growth
- TAM analysis
- Inflection point identification
- SaaS metrics deep dive
- Scenario valuation
- Investment decision

Step 3: If Concerns Arise
Use /stock-analysis-forensic
- Verify revenue quality
- Check for channel stuffing
- Analyze burn rate sustainability
```

---

## Skill Invocation Methods

### Method 1: Explicit Invocation (Recommended)

Simply type the skill name with a slash:

```
/stock-analysis-buffett-longterm
```

Then Claude will ask what company you want to analyze or wait for your specific request.

### Method 2: Natural Language (Auto-Discovery)

Claude will automatically suggest the appropriate skill when you make requests that match the skill descriptions:

**Examples that trigger skills:**

```
"Analyze Apple over the past 20 years using Buffett's framework"
→ Claude suggests: /stock-analysis-buffett-longterm

"Is Snowflake a good growth investment?"
→ Claude suggests: /stock-analysis-growth

"I think this company might be cooking the books"
→ Claude suggests: /stock-analysis-forensic

"Compare Coca-Cola, Pepsi, and Dr Pepper on key metrics"
→ Claude suggests: /stock-analysis-quick-metrics
```

---

## Understanding Skill Restrictions

Each skill has `allowed-tools` restrictions to optimize performance:

- **stock-analysis-buffett-longterm**: `Read, Grep, Glob, Bash(python:*)`
  - Read-only + Python calculations
  - Cannot modify files or search web (focused on local data analysis)

- **stock-analysis-growth**: `Read, Grep, Glob, WebFetch, Bash(python:*)`
  - Includes WebFetch for researching TAM, competitors, market trends
  - Growth analysis often requires external market data

- **stock-analysis-forensic**: `Read, Grep, Glob, Bash(python:*)`
  - Read-only + Python for calculations
  - Forensic analysis focuses on provided financial statements

- **stock-analysis-quick-metrics**: `Read, Bash(python:*)`
  - Minimal tools for speed
  - Quick calculations from provided data

---

## Reference Files

### Buffett Long-Term Skill References:

1. **MOAT_REFERENCE.md** (Loaded on demand)
   - The Four Primary Moat Types (Intangible, Switching Costs, Network Effects, Cost Advantages)
   - Testing frameworks for each moat type
   - Fake Moat rejection criteria
   - The Ultimate Moat Test: Pricing Power
   - Multi-decade moat durability assessment
   - Industry-specific moat analysis

2. **OWNER_EARNINGS.md** (Loaded on demand)
   - Complete Owner Earnings calculation guide
   - Step-by-step calculation methodology
   - Maintenance vs Growth CapEx estimation (5 methods)
   - Working capital adjustments
   - Multi-year analysis templates
   - Return on Retained Earnings test
   - Common calculation mistakes to avoid

3. **RECESSION_ANALYSIS.md** (Loaded on demand)
   - Major recessions framework (2001, 2008-09, 2020)
   - Three-phase analysis (Pre-recession, During, Recovery)
   - Six recession resilience tests (120-point scoring)
   - Industry-specific recession patterns
   - Red flags (permanent avoidance) vs Green flags (buy opportunities)
   - Multi-recession comparison templates

---

## Data Requirements Summary

| Skill | Minimum Data | Ideal Data | If Insufficient |
|-------|--------------|------------|-----------------|
| **buffett-longterm** | 10 years | 20+ years | REJECT or use growth skill |
| **growth** | 2 years | 5+ years | Acceptable for growth analysis |
| **forensic** | 3 years | 5+ years | Can analyze, but limited trend data |
| **quick-metrics** | 1 year | 3+ years | Can calculate, but trends limited |

---

## Key Principles Embedded in Skills

### From Buffett Long-Term:
> "Time is the friend of the wonderful business, the enemy of the mediocre."

- 10+ year track record proves durability
- Recession testing reveals true quality
- Owner Earnings > GAAP earnings
- Moat must widen over time, not require re-excavation

### From Growth Analysis:
> "If you wait until you can see the cathode ray tube, you've missed buying RCA." — Philip Fisher

- Forward-looking potential before it's obvious
- Inflection points create multi-baggers
- Unit economics must be positive
- TAM expansion is critical

### From Forensic Analysis:
> "If you find one cockroach in the kitchen, there's a whole nest you haven't seen."

- One red flag signals multiple problems
- Footnotes tell the truth headlines hide
- Cash doesn't lie, accounting does
- Trust, but verify - always

### From Quick Metrics:
> "Screen fast to say NO quickly to 90% of companies, so you can say YES slowly to the few that deserve deep analysis."

- Speed over accuracy for screening
- Use to filter, not to decide
- Deep analysis only for candidates that pass
- Time is your scarcest resource

---

## Tips for Effective Use

1. **Start with quick-metrics for ALL companies**
   - Even if you "know" it's good, run the numbers
   - Confirms intuition or reveals blind spots

2. **Use the right skill for the right company**
   - Don't force Buffett framework on 3-year-old startup
   - Don't use growth framework on 100-year-old utility

3. **Reference files are your friends**
   - Claude will load them when needed
   - They provide detailed methodologies
   - Use them to understand "why" behind calculations

4. **Combine skills when needed**
   - Quick screening → Buffett analysis → Forensic verification
   - Each skill serves a specific purpose in your workflow

5. **Trust the GATE ZERO requirement**
   - If Buffett-longterm rejects due to insufficient data, listen
   - 10-year minimum exists for a reason
   - No amount of narrative can replace historical proof

---

## Maintenance & Updates

These skills are based on your research reports in:
`/Users/fang/Developer/Deep-Value-Research/Value Investing Principles/`

If you update those research reports, consider updating the corresponding skills to reflect new insights.

**Skill versions:**
- Buffett Long-Term: v2 (with GATE ZERO and 10-year mandate)
- Growth: v1
- Forensic: v1
- Quick Metrics: v1

---

## Getting Help

If you need help with any skill:

```
/stock-analysis-buffett-longterm --help
```

Or ask Claude:
```
"How do I use the Buffett long-term analysis skill?"
"What's the difference between the growth and Buffett skills?"
"Show me an example of using the forensic skill"
```

---

**Your investment research toolkit is now complete. Use these skills to make better investment decisions based on rigorous, time-tested frameworks.**
