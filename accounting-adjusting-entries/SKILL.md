---
name: accounting-adjusting-entries
description: Use when preparing period-end adjusting entries (รายการปรับปรุงบัญชี) under accrual basis accounting (เกณฑ์คงค้าง), recording accrued revenue (รายได้ค้างรับ), accrued expenses (ค่าใช้จ่ายค้างจ่าย), deferred or unearned revenue (รายได้รับล่วงหน้า e.g. SaaS subscriptions), prepaid expenses (ค่าใช้จ่ายจ่ายล่วงหน้า e.g. insurance or rent), calculating depreciation and allowance for doubtful accounts, executing reversing entries (การกลับรายการต้นงวด), or compiling an adjusted trial balance (งบทดลองหลังปรับปรุง) prior to closing the books.
---

# Adjusting Entries for Period-End Closing (รายการปรับปรุงบัญชีวันสิ้นงวด)

## Overview

Under the **Accrual Basis (เกณฑ์คงค้าง)** of accounting (TFRS for NPAEs Chapter 2 / TAS 1), revenue must be recognized when earned (performance obligations satisfied) and expenses must be recognized when incurred (economic benefits consumed)—**not when cash is received or paid**.

Adjusting entries are posted at the end of each accounting period (monthly or annually) via the General Journal (ใบสำคัญรายวันทั่วไป: JV) to update asset, liability, revenue, and expense accounts prior to issuing financial statements.

---

## 1. The 6 Core Categories of Adjusting Entries

| Category | Economic Trigger | Initial Entry / Timing | Period-End Adjustment |
|---|---|---|---|
| **1. Accrued Revenue (รายได้ค้างรับ)** | Service rendered or goods delivered, but invoice not yet issued or cash not received. | No prior entry. | **Dr.** Accrued Revenue (Asset)<br>**Cr.** Service / Sales Revenue |
| **2. Accrued Expenses (ค่าใช้จ่ายค้างจ่าย)** | Services/utilities used or goods received, but supplier invoice not yet arrived. | No prior entry. | **Dr.** Expense (Income Statement)<br>**Cr.** Accrued Expenses (Liability) |
| **3. Deferred / Unearned Revenue (รายได้รับล่วงหน้า)** | Cash received from customer before delivering service (e.g., annual SaaS subscription). | **Dr.** Cash<br>**Cr.** Unearned Revenue (Liability) | **Dr.** Unearned Revenue (Liability)<br>**Cr.** Earned Revenue |
| **4. Prepaid Expenses (ค่าใช้จ่ายจ่ายล่วงหน้า)** | Cash paid in advance for future benefits (e.g., 1-year insurance, prepaid rent). | **Dr.** Prepaid Expense (Asset)<br>**Cr.** Cash | **Dr.** Expense (Income Statement)<br>**Cr.** Prepaid Expense (Asset) |
| **5. Depreciation (ค่าเสื่อมราคา)** | Systematic allocation of fixed asset cost over its useful economic life. | Asset registered on balance sheet. | **Dr.** Depreciation Expense<br>**Cr.** Accumulated Depreciation |
| **6. Allowance for Doubtful Accounts (ค่าเผื่อหนี้สงสัยจะสูญ)** | Estimation of uncollectible trade receivables based on aging analysis. | Accounts Receivable outstanding. | **Dr.** Bad Debt Expense (or ECL)<br>**Cr.** Allowance for Doubtful Accounts |

---

## 2. B2B Practical Cases & Journal Entries

### Case 1: Accrued Revenue (งานที่ปรึกษาส่งมอบแล้วแต่วางบิลปีถัดไป)
- **Scenario:** A consulting firm completes and delivers a milestone system report to a corporate client on 22 December valued at 150,000 baht. Per contract terms, the formal billing note will be issued on 5 January.
- **At 31 December (Fiscal Year-End):**
  - Dr. Accrued Consulting Revenue (รายได้ค้างรับ - สินทรัพย์หมุนเวียน) 150,000
  - Cr. Consulting Revenue (รายได้ค่าที่ปรึกษา - งบกำไรขาดทุน) 150,000
  *(Note: Output VAT is not recorded yet because under Sec. 78/1(1), Tax Point for services occurs upon payment or tax invoice issuance).*

### Case 2: Accrued Expenses (ค่าบริการขนส่งที่ยังไม่ได้รับ Invoice)
- **Scenario:** A distributor used logistics services throughout December totaling approximately 45,000 baht. The freight provider has not yet mailed the invoice by 31 December.
- **At 31 December:**
  - Dr. Freight & Logistics Expense (ค่าขนส่งสินค้า - ค่าใช้จ่าย) 45,000
  - Cr. Accrued Freight Expense (ค่าใช้จ่ายค้างจ่าย - หนี้สินหมุนเวียน) 45,000
  *(Note: Input VAT and WHT 3% are not recorded until payment is made and tax invoice is received).*

### Case 3: Deferred Revenue (สัญญาบริการ SaaS รายปี)
- **Scenario:** On 1 November 2024, a SaaS provider receives 120,000 baht in advance for an annual subscription covering 1 November 2024 to 31 October 2025 (10,000 baht/month).
- **At Initial Receipt (1 Nov):** Dr. Bank 120,000 / Cr. Unearned SaaS Revenue 120,000 (plus VAT if applicable).
- **At 31 December (2 months elapsed: Nov & Dec = 20,000 baht earned):**
  - Dr. Unearned SaaS Revenue (รายได้รับล่วงหน้า - หนี้สิน) 20,000
  - Cr. Subscription Revenue (รายได้ค่าบริการ SaaS - รายได้) 20,000
  *(Remaining liability of 100,000 baht carries forward to 2025).*

### Case 4: Prepaid Expense (เบี้ยประกันภัยจ่ายล่วงหน้า)
- **Scenario:** On 1 September 2024, a company pays 36,000 baht for 1-year fire and property insurance covering 1 September 2024 to 31 August 2025 (3,000 baht/month).
- **At Initial Payment (1 Sep):** Dr. Prepaid Insurance 36,000 / Cr. Bank 36,000.
- **At 31 December (4 months elapsed: Sep, Oct, Nov, Dec = 12,000 baht expired):**
  - Dr. Insurance Expense (ค่าเบี้ยประกันภัย - ค่าใช้จ่าย) 12,000
  - Cr. Prepaid Insurance (ค่าเบี้ยประกันจ่ายล่วงหน้า - สินทรัพย์) 12,000
  *(Remaining asset of 24,000 baht carries forward to 2025).*

---

## 3. Reversing Entries (การกลับรายการต้นงวดถัดไป)

To simplify routine accounting entries in subsequent periods, accountants often post **Reversing Entries** on the first day of the new period (1 January):

### Comparison: Reversing vs. Non-Reversing (For Case 1 Accrued Revenue of 150,000 Baht)

| Workflow | Method A: With Reversing Entry (Recommended for B2B) | Method B: Without Reversing Entry |
|---|---|---|
| **31 Dec (Adjustment)** | Dr. Accrued Revenue 150,000<br>Cr. Revenue 150,000 | Dr. Accrued Revenue 150,000<br>Cr. Revenue 150,000 |
| **1 Jan (Day 1)** | **Dr. Revenue 150,000**<br>**Cr. Accrued Revenue 150,000** | *(No entry posted)* |
| **5 Jan (Invoice Issued)** | **Dr. Accounts Receivable 150,000**<br>**Cr. Revenue 150,000**<br>*(Net 2025 Revenue = 150k - 150k = 0)* | **Dr. Accounts Receivable 150,000**<br>**Cr. Accrued Revenue 150,000**<br>*(Must remember not to credit revenue)* |

**Rule of Thumb for Reversing Entries:**
- **Always reverse:** Accrued revenues and accrued expenses.
- **Do not reverse:** Depreciation, bad debt allowance, or deferrals recorded initially in balance sheet accounts.

---

## 4. Closing Process: Adjusting Entries vs. Closing Entries

```
[Unadjusted Trial Balance]
           |
           v
[Adjusting Journal Entries (JVs)]  <=== 1. Accruals, Prepaids, Depreciation, ECL
           |
           v
[Adjusted Trial Balance]           <=== 2. Proves Dr = Cr; Basis for Financial Statements
           |
           v
[Financial Statements Issued]      <=== 3. Balance Sheet & Income Statement
           |
           v
[Closing Journal Entries]          <=== 4. Clears temporary accounts (Revenues/Expenses) to Retained Earnings
```

- **Adjusting Entries:** Align ledger balances with reality under the accrual basis before statements are prepared.
- **Closing Entries:** Transfer balances of temporary accounts (Revenues and Expenses) to Income Summary / Retained Earnings to reset them to zero for the new fiscal year.

---

## 5. Period-End Checklist & Common Mistakes

### 5-Step Closing Checklist:
1. **Accruals Check:** Scan open deliveries and milestone sign-offs lacking billings; scan recurring utilities/freight lacking vendor invoices.
2. **Prepaids & Deferrals Schedule:** Update amortization tables for insurance, rent, SaaS subscriptions, and software licenses.
3. **Fixed Assets Register:** Ensure all additions/disposals during the month are recorded; calculate monthly depreciation.
4. **Debtor Aging & ECL:** Review overdue trade receivables and record allowance for doubtful accounts.
5. **Adjusted Trial Balance:** Confirm total Debits equal total Credits; cross-reconcile with bank reconciliation and subsidiary ledgers.

### Common Pitfalls:
- **Omitting Year-End Accruals:** Omitting late December services causes revenue or expenses to shift into the wrong tax year, distorting corporate income tax (ภ.ง.ด.50).
- **Double Counting on Invoicing:** Crediting Revenue again when billing an already accrued revenue item without posting a reversing entry.
- **Expensing 100% of Prepaids Immediately:** Booking 1-year insurance directly to expense distorts quarterly and monthly profitability.
- **Confusing Adjusting Entries with Tax Points:** Accruing service revenue does not require issuing a tax invoice until payment or billing occurs under Sec. 78/1.
