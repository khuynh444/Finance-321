# DECISION MEMO

| | |
|---|---|
| **TO** | Chief Financial Officer |
| **FROM** | Treasury / Risk Management |
| **DATE** | April 1, 2026 |
| **RE** | FX Receivable Exposure & Hedging Recommendation |
| **CLASSIFICATION** | Internal – Confidential |

---

## 1. Exposure Summary

Our firm is scheduled to receive **€5,000,000 (EUR)** from a European client under an executed export contract. Payment is confirmed for **June 30, 2026** — approximately 90 days from today. The contract is denominated in euros; our functional and reporting currency is the U.S. dollar (USD).

At today's spot rate of approximately **1.0820 USD/EUR**, the expected USD proceeds total roughly **$5,410,000**. This figure represents a material revenue line for Q2 and will flow directly into our operating cash position.

---

## 2. The Risk

Exchange rate volatility between now and June 30 could meaningfully reduce our dollar proceeds. The euro has historically moved ±5–8% over a 90-day window during periods of monetary policy divergence. A 5% adverse move — EUR/USD falling to ~1.0279 — would reduce receipts by approximately **$270,500**, enough to erase a significant portion of our operating margin on this contract.

Specific risks include:

- **Policy divergence:** If the Federal Reserve signals rate hikes while the ECB eases, EUR weakens against USD.
- **Geopolitical shock:** European energy or fiscal disruptions historically pressure the euro.
- **Unhedged default scenario:** If we do nothing and the euro depreciates, we bear the full loss with no offset mechanism.

The exposure is unhedged today. Action is warranted before further rate drift occurs.

---

## 3. Hedging Strategies — Quick Comparison

### A. Forward Contract (Vanilla FX Forward)
Lock in today's forward rate (~1.0795 USD/EUR) for delivery on June 30.

| | |
|---|---|
| **Pro** | Certainty — eliminates downside risk entirely; simple to execute via our banking relationship. |
| **Con** | Forfeits upside if EUR appreciates; contractual obligation regardless of whether the receivable is collected. |

### B. FX Option (Purchased EUR Put / USD Call)
Buy the right — but not the obligation — to sell EUR at a strike rate (e.g., 1.0750) on or before expiry.

| | |
|---|---|
| **Pro** | Protects the downside floor while preserving upside if EUR strengthens; flexible if the receivable is delayed or cancelled. |
| **Con** | Upfront premium cost (estimated 1.0–1.5% of notional, or ~$54,000–$81,000); reduces net proceeds even in favorable scenarios. |

### C. Participating Forward (Zero-Cost Collar)
Combine a sold EUR call at a cap with a purchased EUR put at a floor, structured for zero net premium.

| | |
|---|---|
| **Pro** | No upfront cost; downside protected; retains partial upside participation between floor and cap. |
| **Con** | More complex to structure and explain; upside is capped; requires credit facility with counterparty bank. |

---

## 4. Next Steps

This memo initiates a four-stage analytical process to reach a final, data-driven recommendation:

- **Stage 2 — Excel Model Build:** Construct a working spreadsheet model that computes and compares hedge outcomes across the three strategies above under multiple EUR/USD scenarios (bear, base, bull). Outputs will include net USD proceeds, hedge cost, and breakeven rates for each approach.

- **Stage 3 — Technical Specification:** Document the model's architecture and assumptions in a structured spec precise enough to allow reconstruction by a developer or AI system. This will also include an improved model design with sensitivity tables and dynamic inputs.

- **Stage 4 — Final Analysis & Recommendation:** Synthesize model results into a strategy selection, draft a structured AI prompt for ongoing FX analysis, and present the final hedging recommendation to you in a formal CFO briefing.

We expect to complete Stages 2–4 within the next two weeks and return with a specific recommendation and implementation plan. Please advise if you require earlier escalation or wish to set a risk tolerance threshold before Stage 2 begins.

---

*Prepared by Treasury / Risk Management — For internal use only.*
