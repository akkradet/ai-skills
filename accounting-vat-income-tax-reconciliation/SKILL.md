---
name: accounting-vat-income-tax-reconciliation
description: Use when reconciling monthly VAT returns (ภ.พ.30) against accounting revenue in the income statement or against income tax return filings (ภ.ง.ด.50), explaining differences between VAT sales base and book revenue, checking output VAT (ภาษีขาย) from tax invoices with the 7/107 formula, handling cash bills without VAT split, credit notes crossing periods, zero-rated or exempt sales, non-VAT income such as interest or exchange gains, or deciding whether to file a corrected ภ.พ.30.
---

# VAT to Accounting and Income Tax Reconciliation (กระทบยอด ภ.พ.30 กับบัญชีและภาษีเงินได้)

## Overview

Reconcile the VAT sales base in the 12 monthly ภ.พ.30 returns against revenue in the annual income statement. The two rarely match exactly, and that is normal. The rule is: **every difference must have a named cause, a supporting document, and a decision (adjust, explain, or correct the return).** A difference you cannot explain is an open item, not a rounding error.

Reference figures and examples in this skill are illustrative; use the company's own ledger and returns.

## Step 1: Sum the VAT Sales Base

- Total the sales base (before VAT) from all 12 ภ.พ.30 returns in the accounting period, separated by rate: 7%, 0% (export), and exempt.
- Do not mix gross (VAT-inclusive) totals with net totals. Confirm each month's figure is stated before VAT.
- If the accounting period is not January to December, use the 12 months that match it.

## Step 2: Start From Income Statement Revenue

Build the bridge from book revenue to the VAT base:

| Line | Item | Example (baht) |
|------|------|----------------|
| 1 | Total revenue per income statement | 16,988,000 |
| 2 | Less: non-VAT income (interest, exchange gain, other non-sales) | (38,000) |
| 3 | Sales revenue per income statement | 16,950,000 |
| 4 | Adjust for timing or classification (see Step 4) | ± |
| 5 | Expected VAT sales base | = |
| 6 | Sales base per ภ.พ.30 (12 months, all rates) | compare |
| 7 | Unexplained difference | must be 0 or documented |

Do not compare total revenue (which includes interest or exchange gains) with the VAT base. Remove non-sales income first.

## Step 3: Check Output VAT From Tax Invoices

- For VAT-inclusive prices: output VAT = total × 7 ÷ 107. Never total × 7%.
  - Example: 12,840,000 incl. VAT → base 12,000,000 → output VAT 840,000.
- For VAT-exclusive prices: output VAT = base × 7%.
- Cash bills without a VAT split: treat the amount as VAT-inclusive and apply 7 ÷ 107. Abbreviated tax invoices are normally for totals up to 1,000 baht including VAT; full tax invoices are needed when the buyer asks or the amount is larger.
- Reconcile the cash register or POS daily totals with the sales ledger and with money received (cash, card, transfer). Unrecorded sales appear as a gap here.
- Match output VAT month by month against the return, which finds errors faster than a yearly total.
- Output VAT is recorded on the tax invoice date, not the payment date.

## Step 4: Explain Each Difference

| Cause | Typical example | Effect on VAT | Action |
|-------|-----------------|---------------|--------|
| Non-VAT income in revenue | Interest, exchange gain | None on VAT base | Remove in Step 2, keep for corporate tax |
| Zero-rated sales | Export sales at 0% | Included in base, no output VAT | Keep supporting export documents |
| Exempt sales | Exempt goods or services | Excluded from VAT, affects input VAT apportionment | Keep evidence of exemption |
| Credit note in a different period | Credit note issued in December, book recorded next year | Output VAT reduced in the month issued | Align book and return, or document the timing |
| Cut-off on tax invoices | Invoice dated after period end but sale in period | Timing | Check dates on both sides of period end |
| Gross vs net confusion | VAT-inclusive total entered as base | Large unexplained difference | Recalculate using 7 ÷ 107 |
| Unrecorded cash sales | Cash bills not in ledger | Missing output VAT | Add to the month of sale, file corrected return if needed |
| Data entry error | Wrong month or digit | Varies | Trace to source document |

If the difference matches a single item exactly (for example 100,000 equal to an exchange gain), test that hypothesis first against the general ledger, but confirm with the source documents before adjusting.

## Step 5: Decide the Correction

- **Book error** (income recorded in the wrong account, or missing entries): post an adjusting entry in the current period. Example: move an exchange gain booked as sales to its own income account.
  - Dr sales revenue / Cr exchange gain (for the misclassified amount)
- **VAT return error** (a non-VAT item included in the base, or output VAT understated):
  - Output VAT understated: file a corrected ภ.พ.30 for that month and pay the shortfall with surcharges. Surcharge is commonly 1.5% per month from the original due date (Revenue Code section 89); confirm current rates with the Revenue Department.
  - Output VAT overstated: file a corrected return to reduce the amount, and claim the refund or offset under Revenue Department procedure. Do not treat it as input VAT.
- **Credit note timing:** if the credit note reduced output VAT in the month it was issued, the book entry should follow in the same period. If it was booked later, record the correction in the period it belongs, and document why.
- **Reversals:** if a prior year's entry is corrected after statements are issued, apply the accounting standard for prior-period errors and consult the auditor.

Never edit a filed return or an issued tax invoice. Use a corrected return, a debit note, or a credit note.

## Step 6: Non-VAT Income and Corporate Tax

- Interest from deposits: no VAT. Bank withholding tax (typically 15%) and the 50 ทวิ certificate are needed for corporate tax credit. Include the interest in profit for ภ.ง.ด.50.
- Exchange gains: not sales; keep the calculation with the exchange rate used. Unrealised gains on foreign-currency balances at year-end require revaluation.
- Non-VAT income is still taxable income for corporate income tax, even though it is outside the VAT base.

## Step 7: Working Paper

Keep a working paper with:
1. Monthly comparison of ภ.พ.30 base against the ledger (12 rows)
2. Bridge from income statement revenue to VAT base (Step 2)
3. Explanation for each difference with source reference
4. Calculation of output VAT with 7 ÷ 107 where applicable
5. Cut-off list for invoices and credit notes near period end
6. Journal entries for any adjustment, with the reason, and the reversal in the next period if relevant
7. Calculation of VAT payable or receivable at period end, accrued to the accounts
8. Evidence: tax invoices (full and abbreviated), credit and debit notes, Z-reports, bank statements, export documents, interest statements, 50 ทวิ certificates, and copies of filed returns with payment slips

Retain for at least 5 years from filing (Revenue Code section 87/3 as commonly cited).

## Common Mistakes

- Comparing total revenue, including interest and exchange gains, with the VAT base.
- Calculating output VAT as total × 7% instead of × 7/107 for VAT-inclusive prices.
- Leaving cash bills without a VAT split out of the calculation.
- Letting credit notes shift between periods without documentation.
- Treating an "unexplained" difference as acceptable without investigation.
- Adjusting the income statement when the error is only in the VAT return, or the reverse.
- Claiming an overpayment as input VAT instead of following the refund or offset procedure.
- Editing a filed ภ.พ.30 instead of filing a corrected return.
- Forgetting that zero-rated sales still belong in the base but carry no output VAT.
- Ignoring apportionment of input VAT when there are exempt sales.

## Disclaimer

This reference describes common reconciliation method and Thai tax concepts. Rates, surcharge terms, deadlines, and correction procedures change. Confirm with the Revenue Department and an accountant or auditor before filing a corrected return or posting an adjustment.
