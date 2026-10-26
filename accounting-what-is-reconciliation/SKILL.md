---
name: accounting-what-is-reconciliation
description: Use when understanding, designing, or performing reconciliation across various accounting domains including bank reconciliation, vendor AP reconciliation, customer AR reconciliation, and e-commerce marketplace reconciliation (Shopee, Lazada, TikTok Shop).
---

# Financial & Bank Reconciliation (การกระทบยอดธนาคารและบัญชีการเงิน)

## Overview

Reconciliation (การกระทบยอด) is the internal control procedure of comparing two sets of financial records—an internal ledger versus an external or independent source—to verify mathematical agreement, identify timing differences, detect errors, and prevent fraud.

The most critical corporate reconciliation is the **Bank Reconciliation (งบพิสูจน์ยอดเงินฝากธนาคาร)**, which reconciles the general ledger cash/bank account against the official Bank Statement issued by the financial institution.

---

## 1. Bank Reconciliation Framework: Correct Balance Method

Under the **Correct Balance Method (วิธีหายอดเงินฝากที่ถูกต้อง)**, both the Bank Statement balance and the Book balance are adjusted simultaneously until they converge to the exact same corrected figure:

```
[Bank Statement Balance]                        [General Ledger Book Balance]
  + Deposits in Transit (เงินฝากระหว่างทาง)         + Bank Collections / Notes / Interest
  - Outstanding Checks (เช็คสั่งจ่ายค้างขึ้นเงิน)    - Bank Service Charges & Fees
  ± Bank Recording Errors                         - Non-Sufficient Funds (NSF เช็คคืน)
                                                  ± Company Book Errors
           ||                                              ||
           \/                                              \/
 [Adjusted Bank Balance]       <=== MUST EQUAL ===>   [Adjusted Book Balance]
```

### Standard Reconciliation Statement Format

| Bank Statement Adjustments | Amount (THB) | Book Balance Adjustments | Amount (THB) |
|---|---:|---|---:|
| **Balance per Bank Statement** | **X,XXX** | **Balance per Books (Ledger)** | **Y,YYY** |
| *Add:* Deposits in Transit (เงินฝากระหว่างทาง) | + A | *Add:* Collections by Bank (ตั๋วเงินรับ/เงินโอน) | + D |
| *Add:* Bank Errors (understated deposits) | + B | *Add:* Interest Earned (ดอกเบี้ยรับ) | + E |
| | | *Add:* Book Errors (overstated disbursements) | + F |
| *Less:* Outstanding Checks (เช็คค้างจ่าย) | (C) | *Less:* Bank Charges & Fees (ค่าธรรมเนียม) | (G) |
| *Less:* Bank Errors (overstated deposits) | (D) | *Less:* NSF Returned Checks (เช็คคืนเงินไม่พอ) | (H) |
| | | *Less:* Book Errors (understated disbursements) | (I) |
| **Adjusted Bank Balance** | **Z,ZZZ** | **Adjusted Book Balance** | **Z,ZZZ** |

---

## 2. Rule for Adjusting Journal Entries

> **Golden Rule of Bank Reconciliation:**
> **Only adjustments made to the BOOK side require journal entries in the general ledger.**
> Items adjusting the Bank Statement (e.g., Deposits in Transit, Outstanding Checks) are timing differences that the bank will clear automatically; they are **never** recorded in company accounting journals.

### Standard Period-End Journal Entries (Book Adjustments)

#### A. Direct Deposits, Collections, and Interest Earned:
- **Dr.** Cash at Bank (เงินฝากธนาคาร)
- **Cr.** Notes / Accounts Receivable (ตั๋วเงินรับ / ลูกหนี้การค้า)
- **Cr.** Interest Income (ดอกเบี้ยรับ)

#### B. Bank Service Fees & Transaction Charges:
- **Dr.** Bank Charges Expense (ค่าธรรมเนียมธนาคาร)
- **Cr.** Cash at Bank (เงินฝากธนาคาร)

#### C. Customer Bounced / NSF Check (เช็คคืน):
- **Dr.** Accounts Receivable (ลูกหนี้การค้า - ตั้งลูกหนี้กลับคืน)
- **Cr.** Cash at Bank (เงินฝากธนาคาร)

#### D. Correction of Book Disbursing Error (e.g., Check written for 2,400 THB but booked as 4,200 THB):
- **Dr.** Cash at Bank (เงินฝากธนาคาร) 1,800
- **Cr.** Office Supplies / Expense (ค่าใช้จ่ายสำนักงาน) 1,800

---

## 3. The 5-Step Reconciliation Workflow

```
Step 1: Gather Records       ===> Bank Statement & Cash Book for the exact matching period.
Step 2: Tick-and-Cross Match ===> Match line-by-line: dates, amounts, check numbers.
Step 3: Extract Open Items   ===> Separate unmatched items into DIT, O/S checks, bank charges, NSF.
Step 4: Draft Statement      ===> Calculate Adjusted Bank & Book balances. Resolve differences.
Step 5: Post JVs & Archive   ===> Post book adjustment JVs; file signed reconciliation for audit.
```

*Audit Retention:* Retain signed bank reconciliation statements, monthly bank statements, and deposit slips for at least **5 years** under the Accounting Act B.E. 2543.

---

## 4. Other Vital Business Reconciliations

Beyond bank statements, three other reconciliation processes are essential for commercial entities:

### 4.1 Vendor / AP Reconciliation (กระทบยอดเจ้าหนี้การค้า)
- **Data compared:** Internal Accounts Payable Sub-ledger **vs.** Supplier's Statement of Account.
- **Key differences:**
  - Invoices for goods received but missing in AP (unbilled goods receipt notes).
  - Unapplied supplier credit notes (CN) for damaged goods or purchase returns.
  - Payments in transit dispatched by the company but not yet cleared by the vendor.
- **Goal:** Prevent duplicate payments and maintain trade credit.

### 4.2 Customer / AR Reconciliation (กระทบยอดลูกหนี้การค้า)
- **Data compared:** Internal Accounts Receivable Sub-ledger **vs.** Customer Payment Advices.
- **Key differences:**
  - Customer deductions for 3% withholding tax without mailing the 50 ทวิ certificate.
  - Short-payments due to disputed damaged goods or unauthorized cash discounts.
  - Unidentified customer bank transfers (ยอดเงินโอนไม่ทราบผู้โอน).
- **Goal:** Prevent aged bad debts and speed up dispute resolution.

### 4.3 E-Commerce Marketplace Reconciliation (Shopee / Lazada / TikTok Shop)
- **Data compared:** Sales Orders & GMV in Accounting/ERP **vs.** Platform Settlement & Payout Reports.
- **Key differences:**
  - **Platform Deductions:** Marketplace commission fees (3–7%), payment transaction fees (2–3%), service fees, and voucher subsidies deducted at source.
  - **Shipping Overcharges (ค่าขนส่งส่วนเกิน):** Discrepancies between estimated parcel weight and courier actual measured weight deducted from payout.
  - **Settlement Cut-off Timing:** Orders fulfilled in late December paid out in early January.
- **Goal:** Accurately recognize gross revenue while booking platform fees as selling expenses, rather than netting them directly against revenue.

---

## 5. Common Mistakes & Troubleshooting Table

| Common Mistake | Root Cause & Correct Treatment |
|---|---|
| *"Adjusted Bank Balance does not equal Adjusted Book Balance."* | **Transposition Error / Unreconciled Gap.** Check if difference is divisible by 9 (transposition of digits e.g. 54 vs 45) or divisible by 2 (item placed on wrong debit/credit side). Tick line-by-line. |
| *"Recording Outstanding Checks in the General Journal."* | **Double Deduction.** Outstanding checks are already recorded in the cash ledger when issued. Deduct only from the bank statement side on the worksheet. |
| *"Leaving unidentified bank deposits in bank account without investigating."* | **Distorted Liabilities / Unbilled VAT.** If money is received from a customer, tax points may be triggered under Sec. 78/78/1. Book to `เงินพักรอตรวจสอบ (Suspense Account)` and clear promptly. |
| *"Netting marketplace payouts directly as sales revenue."* | **Understated Revenue & VAT Non-Compliance.** E-commerce platforms deduct commission and shipping fees. Gross sales must be recorded as revenue, and platform fees recorded as selling expenses. |
| *"Waiting until year-end audit to reconcile bank accounts."* | **Severe Risk.** Bank reconciliation must be conducted monthly (or weekly for high-volume retail) to detect unauthorized withdrawals, duplicate charges, or bank errors within statutory reporting windows. |
