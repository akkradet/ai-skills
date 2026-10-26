---
name: accounting-accounts-payable
description: Use when managing accounts payable (เจ้าหนี้การค้า, AP), conducting 3-way matching (PO, invoice/billing note, GRN), recording purchases of goods or services on credit, accounting for early payment cash discounts (ส่วนลดรับ e.g. 2/10 net 30), handling undue input VAT (ภาษีซื้อยังไม่ถึงกำหนด) and withholding tax (WHT หัก ณ ที่จ่าย ภ.ง.ด.3/53) upon payment, analyzing AP aging schedules (รายงานอายุหนี้เจ้าหนี้), or calculating Accounts Payable Turnover Ratio and Days Payable Outstanding (DPO).
---

# Accounts Payable Management (การบริหารเจ้าหนี้การค้า)

## Overview

Accounts Payable (AP - เจ้าหนี้การค้า) represents the short-term obligations owed by a business to suppliers for goods or services received on credit. Classified as a **Current Liability (หนี้สินหมุนเวียน)** on the balance sheet, AP is a vital source of spontaneous, interest-free working capital.

Effective AP management balances two critical goals:
1. **Preserving liquidity:** Holding cash as long as legally permitted under agreed credit terms without incurring penalties.
2. **Maintaining supplier trust & continuity:** Ensuring timely, accurate payments to avoid supply disruptions, credit cancellation, or damaged commercial terms.

---

## 1. Internal Control: 3-Way Matching Process

Before any payment voucher is approved and paid, accounts payable staff must perform **3-Way Matching** across three source documents:

```
[Purchase Order (PO)]  <====== Matches ======>  [Goods Receipt Note (GRN)]
   (Qty & Price Ordered)                             (Qty Received & Inspected)
            \                                                /
             \==== Matches === [Supplier Invoice] === Matches/
                                (Qty & Price Billed)
```

| Document | Issuer | What to Verify | Discrepancy Action |
|---|---|---|---|
| **Purchase Order (PO)** | Purchasing Dept. | Approved quantities, agreed unit prices, credit terms (e.g., Net 30), delivery dates. | If invoice price > PO price, reject until approved price change or credit memo is provided. |
| **Goods Receipt Note (GRN / ใบรับของ)** | Warehouse / Receiving | Actual quantity received, batch/lot condition, receiver signature. | If invoice qty > GRN qty (e.g., billed 500, received 480), request a corrected invoice or Debit Note for short-shipment. |
| **Supplier Invoice (ใบแจ้งหนี้ / ใบกำกับภาษี)** | Supplier / Vendor | Tax ID, company name/address, unit math, VAT calculation, bank account details. | Hold invoice if discrepancies exist; never pay unverified charges. |

*For services:* Replace the GRN with a **Service Acceptance Certificate (ใบตรวจรับงาน)** signed by the project manager or department head.

---

## 2. Standard Accounting Entries (Journal Entries)

### 2.1 Purchasing Goods on Credit (บันทึกซื้อสินค้าเป็นเงินเชื่อ)
Under Thai VAT law (Section 78(1)), the tax point for goods occurs upon delivery. The supplier issues a Tax Invoice upon delivery, allowing immediate input VAT recognition.

**At time of receiving goods & tax invoice (e.g., 50,000 baht + 7% VAT = 53,500 baht):**
- Dr. Inventory / Merchandise (สินค้าคงเหลือ) 50,000
- Dr. Input VAT (ภาษีซื้อ - เคลมใน ภ.พ.30) 3,500
- Cr. Accounts Payable (เจ้าหนี้การค้า) 53,500

**At time of payment upon due date:**
- Dr. Accounts Payable (เจ้าหนี้การค้า) 53,500
- Cr. Cash / Bank (เงินฝากธนาคาร) 53,500

---

### 2.2 Purchasing Services on Credit (บันทึกรับบริการเป็นเงินเชื่อ)
Under Revenue Code Section 78/1(1), the tax point for services occurs upon **payment receipt**, not delivery. Therefore, when receiving an invoice before payment, input VAT cannot be claimed yet and withholding tax (WHT) is not yet deducted.

**Step 1: At time of receiving service billing note / invoice (e.g., 100,000 baht + 7% VAT = 107,000 baht):**
- Dr. Service Expense (ค่าบริการ / ค่าจ้างทำของ) 100,000
- Dr. Undue Input VAT (ภาษีซื้อยังไม่ถึงกำหนด) 7,000
- Cr. Accounts Payable (เจ้าหนี้การค้า) 107,000

**Step 2: At time of payment (Supplier issues Tax Invoice/Receipt; Client deducts 3% WHT):**
- WHT base = 100,000 × 3% = 3,000 baht (Form ภ.ง.ด.53 / Certificate 50 ทวิ).
- Net cash payment = 107,000 - 3,000 = 104,000 baht.
- Dr. Accounts Payable (เจ้าหนี้การค้า) 107,000
- Dr. Input VAT (ภาษีซื้อ - โอนไปใช้สิทธิใน ภ.พ.30) 7,000
- Cr. Undue Input VAT (ภาษีซื้อยังไม่ถึงกำหนด - ล้างออก) 7,000
- Cr. Withholding Tax Payable (ภาษีเงินได้หัก ณ ที่จ่ายค้างจ่าย) 3,000
- Cr. Cash / Bank (เงินฝากธนาคาร) 104,000

---

### 2.3 Early Payment Cash Discounts (ส่วนลดรับ e.g., 2/10 Net 30)

"2/10 Net 30" means the buyer receives a 2% discount if paid within 10 days; otherwise, the full amount is due in 30 days.

**Worked Example (Goods 100,000 baht + 7% VAT = 107,000 baht, discount 2%):**
- Cash discount = 100,000 × 2% = 2,000 baht.
- VAT reduction (7% on discount) = 2,000 × 7% = 140 baht (Supplier issues Credit Note).
- Net payment = 107,000 - (2,000 + 140) = 104,860 baht.

**Journal Entry upon payment within 10 days (Gross Method):**
- Dr. Accounts Payable (เจ้าหนี้การค้า) 107,000
- Cr. Purchase Discount / Other Income (ส่วนลดรับ) 2,000
- Cr. Input VAT (ภาษีซื้อ - ปรับลดตามใบลดหนี้) 140
- Cr. Cash / Bank (เงินฝากธนาคาร) 104,860

*Annualized Return of Cash Discount:*
$$\text{Annualized Rate} = \frac{\text{Discount \%}}{100\% - \text{Discount \%}} \times \frac{365}{\text{Credit Term} - \text{Discount Period}} = \frac{2\%}{98\%} \times \frac{365}{20} \approx 37.24\% \text{ p.a.}$$
*Taking early payment discounts yields far higher returns than short-term bank deposits.*

---

## 3. AP Aging Schedule & Payment Prioritization

The AP Aging Schedule classifies outstanding balances by due date. Finance should review it weekly to manage cash outflows:

| Aging Bucket | Urgency / Status | Action & Strategy |
|---|---|---|
| **Not Yet Due (ยังไม่ครบกำหนด)** | Normal | Schedule for payment on the exact due date. Do not pay prematurely unless cash discounts apply. |
| **1 – 30 Days Overdue** | Warning | Contact vendor, verify any dispute or missing invoice, schedule for next payment run. |
| **31 – 60 Days Overdue** | High Priority | Risk of supply halt. Negotiate payment installment or release partial payment. |
| **Over 60 Days Overdue** | Critical | Immediate escalation. Risk of credit cut, blacklisting, or legal action. Settle immediately. |

### Prioritization Rules:
1. **Critical / Monopoly Suppliers:** Pay on time regardless of aging to avoid supply chain paralysis.
2. **High-Discount Invoices (e.g., 2/10):** Pay within the discount window.
3. **Small Non-Critical Suppliers:** Schedule strictly on credit maturity.

---

## 4. Key Performance Indicators (KPIs)

### 4.1 Accounts Payable Turnover Ratio
Measures how many times per year the company pays off its trade suppliers:
$$\text{AP Turnover Ratio} = \frac{\text{Cost of Goods Sold (COGS)}}{\text{Average Accounts Payable}}$$
$$\text{Average Accounts Payable} = \frac{\text{Beginning AP} + \text{Ending AP}}{2}$$

### 4.2 Days Payable Outstanding (DPO)
Measures the average number of days it takes to pay suppliers:
$$\text{DPO} = \frac{365}{\text{AP Turnover Ratio}} = \frac{\text{Average Accounts Payable} \times 365}{\text{COGS}}$$

- **Benchmark Interpretation:**
  - Standard credit term in Thailand is 30–60 days.
  - A higher DPO improves operating cash flow, but excessively high DPO indicates cash distress or supplier disputes.

---

## 5. Common Mistakes & Rationalization Table

| Common Rationalization / Mistake | Reality & Correct Treatment |
|---|---|
| *"We received the service bill, so let's claim Input VAT in this month's ภ.พ.30 right away."* | **Wrong.** Under Sec. 78/1(1), Tax Point for services occurs when payment is made. Record as `ภาษีซื้อยังไม่ถึงกำหนด (Undue Input VAT)` until payment. |
| *"The supplier called urgently, so let's pay before matching the Goods Receipt Note."* | **High Risk.** Leads to paying for missing, defective, or returned goods. 3-Way Matching must be completed before payment release. |
| *"We paid the service invoice in full without deducting 3% withholding tax."* | **Statutory Violation.** The payer is personally liable under Revenue Code Section 54 for the unwithheld tax plus 1.5%/month surcharge. |
| *"Paying 10 days early isn't worth the trouble for just 2%."* | **Financial Misjudgment.** A 2/10 Net 30 discount equals an annualized return of ~37.2% p.a., far exceeding short-term investment or borrowing rates. |
| *"We have multiple invoices from the same vendor, so we paid them in a single batch without checking invoice numbers."* | **Duplicate Payment Risk.** Always match individual invoice numbers and clear AP items line-by-line in the ledger. |
