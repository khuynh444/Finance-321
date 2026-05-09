# FX Hedge Analysis — Executive Memo & Strategic Recommendation
**Stage 4 | Treasury / Risk Management**
*Prepared: April 2026 | Analyst: [HUYNH]*

---

## A. Exposure Summary

The firm holds a confirmed **€5,000,000 EUR receivable** due for settlement on **30 June 2026** (90 days from 01 April 2026). The receivable arises from a commercial transaction invoiced in euros; USD is the firm's functional currency.

The core risk is straightforward: every 1% depreciation of EUR against USD reduces realized USD proceeds by approximately **$54,100**. At inception, the unhedged position is worth **$5,410,000** at the spot rate of 1.0820. A 5% adverse move — well within the historical range for a 90-day EUR/USD window — would reduce proceeds to roughly **$5,139,500**, a **$270,500 shortfall** relative to spot-implied value.

The CFO must decide whether to lock in certainty, buy downside protection, or accept market exposure — each carrying a different cost, flexibility, and cash flow profile. This memo presents the analysis and a clear recommendation.

---

## B. Summary of Hedge Outcomes

All proceeds are stated at the base case of S_T = S0 = 1.0820 USD/EUR unless otherwise noted.

### Forward Hedge
- **Locked-in USD proceeds: $5,433,461**
- The forward rate of 1.08669 (IRP-implied) locks in proceeds regardless of where EUR/USD settles on 30 June. The firm gives up all upside if EUR strengthens, but eliminates all downside risk. No premium is paid; the cost is embedded in the forward points (USD rates exceed EUR rates, yielding a slightly favorable forward vs. spot). This is the most operationally simple hedge: one transaction, one outcome.

### Money Market Hedge
- **USD proceeds: $5,433,461** (identical to forward by IRP parity)
- The firm borrows €4,956,015 today (the PV of the receivable at R_FC = 3.55%), converts to USD at spot, and invests at R_USD = 5.30% for 90 days. The future value exactly replicates the forward hedge outcome. The practical difference is balance sheet impact: this structure draws on the firm's credit facility (EUR borrowing capacity) and temporarily inflates both assets and liabilities. Preferred only if the forward market is inaccessible or if the firm has a natural EUR liability to offset.

### EUR Put Option
- **USD proceeds at S0: $5,350,000 | Floor: $5,315,000**
- Purchasing a EUR put (K_PUT = 1.0750, premium $0.0120/EUR = $60,000 total) provides a guaranteed minimum of $5,315,000 while preserving full upside if EUR appreciates. The premium is a sunk cost paid at inception. The strategy is most valuable when EUR appreciation is expected but downside protection is still required — i.e., the firm wants insurance, not a lock-in.

### Zero-Cost Collar
- **USD proceeds at S0: $5,382,500 | Floor: $5,347,500 | Ceiling: $5,422,500**
- Buying the put (K_PUT = 1.0750) and selling the call (K_CALL = 1.0900) produces a net debit of $27,500 — reducing but not eliminating the premium cost. The collar sacrifices upside above K_CALL in exchange for a lower net premium than the standalone put. The name "zero-cost" is a market convention for a version where the strikes are set so net premium equals zero; this model's strikes produce a small net debit, not full zero cost. Nevertheless, the collar offers a useful middle ground: defined floor, reduced premium, limited upside.

### No Hedge (Unhedged Baseline)
- **USD proceeds at S0: $5,410,000**
- The unhedged position is worth $57,949 more than the forward at today's spot — but that advantage evaporates immediately if EUR weakens. The unhedged outcome is purely a function of S_T: for every cent EUR falls, the firm loses $50,000. This is a risk position, not a strategy, and is retained only if management has a high-conviction view on EUR appreciation and the balance sheet can absorb the downside.

---

## C. Sensitivity Interpretation

The sensitivity table spans S_T from **1.0279** (EUR −5%) to **1.1361** (EUR +5%) in 1% increments, producing eleven scenarios.

### EUR Depreciation Scenarios (S_T < S0)
This is where hedging earns its value. At S_T = 1.0279 (−5%):

| Strategy      | USD Proceeds  | vs. Unhedged |
|---------------|---------------|--------------|
| Forward / MM  | $5,433,461    | +$293,961    |
| EUR Put       | $5,315,000    | +$175,500    |
| Collar        | $5,347,500    | +$208,000    |
| **Unhedged**  | **$5,139,500**| —            |

The forward and money market hedges fully insulate the firm; proceeds are constant across all depreciation scenarios. The put floors proceeds at $5,315,000 — $175,500 better than unhedged at the worst scenario. The collar adds an additional $32,500 relative to the put, at the cost of capping upside.

### EUR Appreciation Scenarios (S_T > S0)
At S_T = 1.1361 (+5%):

| Strategy      | USD Proceeds  | vs. Forward  |
|---------------|---------------|--------------|
| Unhedged      | $5,680,500    | +$247,039    |
| EUR Put       | $5,620,500    | +$187,039    |
| Collar        | $5,422,500    | −$10,961     |
| Forward / MM  | $5,433,461    | —            |

Here the unhedged and put strategies capture upside; the collar is capped and trails the forward by a small amount (net premium effect). The forward forgoes $247,039 of potential gain — the "opportunity cost of certainty."

### Key Insight
The forward and money market hedges eliminate volatility entirely but at the cost of upside participation. The put option is the only strategy that provides both a hard floor and unlimited upside, making it the most flexible — but it requires a $60,000 upfront premium. The collar is the most cost-efficient floor, but truncates the upside that justifies the option purchase in the first place. The unhedged position is only rational if EUR appreciation is high-confidence and the downside is tolerable.

---

## D. Strategic Recommendation

**Recommended strategy: EUR Put Option**

The firm should purchase a 90-day EUR put with strike K_PUT = 1.0750, paying a total premium of **$60,000** (1.11% of notional).

This recommendation is supported by three considerations:

1. **Downside protection is non-negotiable.** A $270,500 adverse move is meaningful relative to typical operating margins. The put floors USD proceeds at $5,315,000, capping the maximum loss at $95,000 vs. today's spot value — a defined, manageable outcome.

2. **Upside optionality has real value.** EUR/USD has shown approximately 7.5% annualized implied volatility. In a 90-day window, EUR appreciation to 1.10+ is plausible. The forward locks in proceeds below the collar ceiling; the put allows the firm to benefit from any appreciation above S0.

3. **The premium is proportionate.** At $60,000 on a $5.4M exposure, the put costs approximately **111 bps** — a reasonable insurance premium for a quarter of downside elimination on a material receivable.

If budget certainty is the overriding priority and the treasury team has no view on EUR direction, the **forward hedge** is the appropriate fallback: zero premium, maximum certainty, simplest execution.

---

## E. Executive Justification

**Cash flow stability:** The put option guarantees a minimum USD receipt of $5,315,000 — sufficient to meet budgeted USD targets (assuming budget rate ≤ 1.063 USD/EUR). Finance can plan with a defined floor rather than an open-ended range.

**Budget certainty:** If the firm set its internal budget rate at or below 1.063, even the put-floored outcome clears the target. The forward provides absolute certainty; the put provides near-certainty with optionality.

**Liquidity impact:** The put premium of $60,000 is paid at inception — a known, manageable cash outflow that should be accrued as a hedging cost in the current period. The money market hedge, by contrast, draws on credit lines and temporarily inflates the balance sheet, which may affect debt covenants.

**Optionality value:** The put is the only instrument that preserves upside. If the euro strengthens to 1.10, the firm receives ~$5,560,500 net — $127,039 more than the forward. This optionality is worth paying for when the direction of EUR/USD is uncertain and the receivable is material.

**Premium cost vs. alternatives:** The collar reduces net premium to $27,500 but caps upside at K_CALL = 1.09. Given that upside is the primary argument for avoiding the forward, truncating that upside significantly undermines the rationale for paying any premium at all. The standalone put is the cleaner, more defensible choice.

**Accounting note (optional):** Designating the put as a cash flow hedge under ASC 815 would allow changes in fair value to flow through OCI rather than P&L, reducing earnings volatility. This designation requires formal documentation at inception — consult Controllers before execution.

---

## F. Structured AI Prompt

*The following prompt is written to instruct an AI assistant (e.g., Claude) to reconstruct and improve the FX hedge Excel model from scratch. It is designed to be self-contained and reproducible.*

---

```
# GOAL

Build a professional Excel workbook modeling four FX hedging strategies for a EUR
receivable. The model must be fully formula-driven, use standardized named ranges,
include a sensitivity table, a Black-Scholes option pricer, and produce a
comparison summary. It should be auditable by a treasury analyst with no additional
context beyond this prompt.

---

# INPUT VARIABLES

Use the following named ranges exactly as specified. These are editable inputs
(yellow background, blue text):

  FC_AMT       = 5,000,000       (EUR; notional receivable)
  S0_in        = 1.0820          (USD per EUR; spot rate at inception, 01-Apr-2026)
  R_USD        = 0.0530          (annual rate; ACT/360; approx. 90-day T-Bill/SOFR)
  R_FC         = 0.0355          (annual rate; ACT/360; approx. ECB/EURIBOR 3M)
  T_DAYS       = 90              (calendar days; 01-Apr-2026 to 30-Jun-2026)
  K_PUT        = 1.0750          (USD per EUR; EUR put strike)
  K_CALL       = 1.0900          (USD per EUR; EUR call strike; collar leg)
  SIGMA        = 0.0750          (annual implied volatility; 7.50%; used in BSM pricer)

Do NOT hardcode PREM_PUT or PREM_CALL. These must be computed by a Black-Scholes
function using S0_in, K_PUT or K_CALL, R_USD, R_FC, T_FRAC, and SIGMA.

---

# DERIVED CONSTANTS

Compute these as formula-driven cells (blue text, derived section):

  T_FRAC       = T_DAYS / 360
  F0_in        = S0_in × (1 + R_USD × T_FRAC) / (1 + R_FC × T_FRAC)
  PREM_PUT     = BSM_PUT(S0_in, K_PUT, R_USD, R_FC, T_FRAC, SIGMA)   [USD per EUR]
  PREM_CALL    = BSM_CALL(S0_in, K_CALL, R_USD, R_FC, T_FRAC, SIGMA) [USD per EUR]
  PREM_PUT_$   = FC_AMT × PREM_PUT
  PREM_CALL_$  = FC_AMT × PREM_CALL
  NET_COLLAR   = PREM_PUT_$ − PREM_CALL_$

For the Black-Scholes pricer, implement as helper formulas using NORM.S.DIST():
  d1 = [LN(S0/K) + (R_USD − R_FC + 0.5 × SIGMA²) × T_FRAC] / (SIGMA × SQRT(T_FRAC))
  d2 = d1 − SIGMA × SQRT(T_FRAC)
  Put  = K × EXP(−R_USD × T_FRAC) × NORM.S.DIST(−d2,1) − S0 × EXP(−R_FC × T_FRAC) × NORM.S.DIST(−d1,1)
  Call = S0 × EXP(−R_FC × T_FRAC) × NORM.S.DIST(d1,1) − K × EXP(−R_USD × T_FRAC) × NORM.S.DIST(d2,1)

---

# MODEL LOGIC

Build the following sections in sequence on a single sheet named "FX Hedge Model":

## Section 1 — Forward Hedge
  Forward_Proceeds = FC_AMT × F0_in
  [Label outcome, show formula in adjacent cell as text for auditability]

## Section 2 — Money Market Hedge (3 steps)
  Step 1: EUR_Borrow   = FC_AMT / (1 + R_FC × T_FRAC)
  Step 2: USD_Convert  = EUR_Borrow × S0_in
  Step 3: MM_Proceeds  = USD_Convert × (1 + R_USD × T_FRAC)

## Section 3 — EUR Put Option
  At any S_T:
    Gross_Put   = FC_AMT × MAX(K_PUT, S_T)
    Put_Proceeds = Gross_Put − PREM_PUT_$

## Section 4 — Zero-Cost Collar
  At any S_T:
    Gross_Collar   = FC_AMT × MIN(K_CALL, MAX(K_PUT, S_T))
    Collar_Proceeds = Gross_Collar − NET_COLLAR

## Section 5 — Sensitivity Table
  Vary S_T from S0_in × 0.95 to S0_in × 1.05 in 11 equal steps (1% increments).
  For each S_T row, compute and display:
    - S_T value
    - % change vs S0_in
    - Forward_Proceeds  (constant = FC_AMT × F0_in)
    - MM_Proceeds       (constant = same as Forward)
    - Put_Proceeds      = FC_AMT × MAX(K_PUT, S_T) − PREM_PUT_$
    - Collar_Proceeds   = FC_AMT × MIN(K_CALL, MAX(K_PUT, S_T)) − NET_COLLAR
    - Unhedged          = FC_AMT × S_T
  Follow each row with a line chart (5 series, S_T on x-axis, USD proceeds on y-axis).
  Title the chart: "USD Proceeds by Hedge Strategy vs. Settlement Rate (S_T)"

## Section 6 — Summary Output Table
  One row per strategy: Forward, Money Market, EUR Put, Collar, Unhedged
  Columns: Strategy | USD Proceeds (at S0) | Notes
  Add a "Recommended Hedge" row with a placeholder: [See Stage 4 memo]

## Section 7 — Additional Metrics (improvements over Stage 2)
  Break-even S_T (Put):    K_PUT − (PREM_PUT_$ / FC_AMT)
  Break-even S_T (Collar): K_PUT − (NET_COLLAR / FC_AMT)
  Put cost in bps:         (PREM_PUT_$ / (FC_AMT × S0_in)) × 10000
  Collar cost in bps:      (NET_COLLAR / (FC_AMT × S0_in)) × 10000

---

# VERIFICATION

Include a verification section (gray background, labeled "Checks"):
  Parity Check:   |Forward_Proceeds − MM_Proceeds| → must equal 0 (or < $1 rounding)
  F0 IRP Check:   |F0_in − (S0_in × (1+R_USD×T_FRAC)/(1+R_FC×T_FRAC))| → must equal 0
  BSM Put-Call Parity: PREM_CALL − PREM_PUT − S0×EXP(−R_FC×T_FRAC) + K×EXP(−R_USD×T_FRAC) ≈ 0
  Flag any check that fails with conditional formatting (red cell fill).

---

# FORMATTING

Color coding (apply throughout):
  Yellow background (#FFFF00), blue text: all editable inputs (Section 1 named ranges)
  Blue text on white: derived constants (T_FRAC, F0_in, premiums)
  Black text: all formula-driven calculation cells
  Gray background (#D9D9D9): output summary cells and verification checks

Additional formatting:
  - Use Arial 11pt throughout
  - Format all USD amounts as $#,##0 with no decimals
  - Format exchange rates to 5 decimal places
  - Format percentages to 2 decimal places (0.00%)
  - Bold all section headers
  - Freeze top 4 rows (title + color key + blank + header)
  - Column widths: description columns 30–35 characters, value columns 15 characters

Add a second sheet named "Notes & Assumptions" with:
  - Model purpose, analyst name, date built
  - Rate sources and day count convention
  - One paragraph each on Forward, MM, Put, and Collar logic
  - List of items not modeled (credit risk, taxes, ASC 815, bid/ask)

---

# EXPORT

Save as: FX-Hedge-Model-Improved.xlsx
Ensure zero formula errors (#REF!, #DIV/0!, #VALUE!, #NAME?) before delivery.
All formulas must recalculate correctly if any input in Section 1 is changed.
```

---

## Extra Credit: Areas for Further Study

### 1. AI Skills & Automation

The structured prompt in Section F demonstrates one half of the AI automation workflow — converting a specification into a model. The other half is dynamic: rather than using static inputs, an AI agent equipped with a web search or market data tool (e.g., Bloomberg API, FRED, or a live FX feed) could pull the current EUR/USD spot rate, SOFR, and EURIBOR at model-open and populate `S0_in`, `R_USD`, and `R_FC` automatically. Claude's tool-use capabilities, for instance, could be wired to fetch rates on demand, reprice the Black-Scholes option premiums using current implied volatility from an options chain, and regenerate the sensitivity table — all without manual input. Extending further, a Monte Carlo simulation layer (10,000 paths of EUR/USD using geometric Brownian motion calibrated to the current implied vol) would replace the deterministic ±5% sensitivity table with a full probability distribution of USD proceeds, allowing the treasury analyst to report a "5th-percentile outcome" rather than a worst-case point estimate.

### 2. GitHub & Version Control

Committing Stages 1–4 to a GitHub repository creates something more valuable than a filing cabinet: it creates a reproducible, auditable model lineage. Each commit carries a timestamp, author, and diff — meaning a reviewer can reconstruct exactly what assumptions were in place on any given date, and why they changed. This directly addresses a core requirement of ASC 815 hedge accounting: documentation of risk management objective and hedging relationship must exist *at inception*, not reconstructed after the fact. A GitHub commit timestamped before settlement serves as contemporaneous evidence. Beyond compliance, version control enables the analyst-to-automation workflow demonstrated in this project: the Stage 3 spec (committed as `stage3-spec.md`) feeds the Stage 4 AI prompt (committed as `stage4-prompt.md`), which regenerates a new model version (committed as `FX-Hedge-Model-v2.xlsx`) — creating a fully auditable chain from business problem to executable model.

### 3. Accounting & Audit Integration

Hedge accounting under ASC 815 requires the firm to designate and document the hedging relationship, the risk being hedged, and the method of assessing effectiveness — all before or at inception. In this project, the Stage 3 specification doubles as a preliminary documentation artifact: it identifies the hedged item (the EUR receivable), the hedging instrument (EUR put or forward), and the risk (EUR/USD spot rate). A more rigorous version would include a quantitative effectiveness test (e.g., dollar-offset method comparing changes in fair value of the hedge vs. the hedged item) computed inside the Excel model itself. If the firm designates the put as a cash flow hedge, changes in the option's intrinsic value flow through OCI, reducing P&L volatility — a meaningful accounting benefit that the CFO should factor into the strategy selection. GitHub version history, combined with model snapshots at inception and each reporting date, could serve as audit evidence that the hedging documentation was contemporaneous and the effectiveness assessment was performed consistently.
