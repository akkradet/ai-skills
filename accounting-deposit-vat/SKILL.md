---
name: accounting-deposit-vat
description: Use when recording accounting entries and determining Thai tax treatments for deposits (เงินมัดจำ), reservation fees (เงินจอง), security deposits (เงินประกัน), advance payments (เงินจ่ายล่วงหน้า), or retention fees (เงินประกันผลงาน), including VAT liability and tax point under Revenue Code Section 78/78/1, withholding tax (หัก ณ ที่จ่าย), final invoicing deducting deposits, forfeiture of deposits (ริบเงินมัดจำ), and rental deposit exemptions under Departmental Instruction Por 73/2541.
---

# Accounting and VAT for Deposits (เงินมัดจำ เงินประกัน และภาษีมูลค่าเพิ่ม)

## Overview

A deposit is **neither revenue nor expense** when received or paid. It is a **liability** (เงินมัดจำรับ / เงินรับล่วงหน้า) for the recipient and an **asset** (เงินมัดจำจ่าย / เงินจ่ายล่วงหน้า) for the payer until the performance obligation is satisfied (goods delivered or services completed).

However, in Thai tax law:
> **The Tax Point for VAT triggers immediately upon receiving a deposit or advance payment** (Section 78(1)(b) for goods, Section 78/1(1) for services). A VAT-registered business must issue a tax invoice immediately on the payment receipt date, even if delivery or service has not yet taken place.

---

## 1. Classification Matrix: Deposit vs. Reservation vs. Security Deposit vs. Advance

| Type | Legal Character (Thai Law) | Accounting Treatment | VAT (ภาษีมูลค่าเพิ่ม) | WHT (หัก ณ ที่จ่าย) |
|---|---|---|---|---|
| **เงินมัดจำ (Deposit)** | Contract guarantee under Civil & Commercial Code Sec. 377–381; forfeitable if payer breaches. Offset against final price. | **Recipient:** Current Liability<br>**Payer:** Current Asset | **Subject to VAT immediately** on payment date. Must issue Tax Invoice. | • Goods: None<br>• Service: 3% withheld at payment |
| **เงินจ่ายล่วงหน้า (Advance Payment)** | Partial or full payment of purchase price before delivery. | **Recipient:** Current Liability<br>**Payer:** Current Asset | **Subject to VAT immediately** on payment date. Must issue Tax Invoice. | • Goods: None<br>• Service: 3% withheld at payment |
| **เงินจอง (Reservation Fee)** | Expression of intent to purchase; non-binding or binding depending on contract terms. | **Recipient:** Current Liability<br>**Payer:** Current Asset | **Subject to VAT immediately** if non-refundable or offset against sale price. | • Goods: None<br>• Service: 3% if offset against service |
| **เงินประกัน / มัดจำประกัน (Security Deposit)** | Guarantee against physical damage or contract breach (e.g., lease, meter deposit); **must be returned** upon expiry. | **Recipient:** Other Liability<br>**Payer:** Other Asset | **Exempt from VAT** if meeting Por 73/2541 conditions. Issue standard receipt, not tax invoice. | **No WHT** at time of deposit. |
| **เงินประกันผลงาน (Retention)** | Retention withheld from contractor progress billing (e.g., 5–10%) to guarantee work quality during warranty. | **Contractor:** Retention Receivable<br>**Client:** Retention Payable | **Full VAT on gross progress billing** (Retention does not reduce VAT base of invoice). | **Full WHT on gross progress billing** before retention deduction. |

---

## 2. VAT Rules & Calculation Formulas

### 2.1 Tax Point Rules (ประมวลรัษฎากร)
- **Sale of Goods (มาตรา 78 (1) (ข)):** Tax point normally arises upon delivery, **except** when payment (deposit) is received before delivery. The tax point arises on the receipt date for the amount received.
- **Service Provision (มาตรา 78/1 (1)):** Tax point arises upon receiving payment (deposit) or issuing a tax invoice, whichever is earlier.

### 2.2 VAT Amount Formulas
- **VAT-exclusive price:** $\text{VAT} = \text{Deposit Base} \times 7\%$
- **VAT-inclusive price:** $\text{VAT} = \text{Gross Amount Received} \times \frac{7}{107}$
  - Example: Received 107,000 baht incl. VAT $\rightarrow$ Base = 100,000 baht, Output VAT = 7,000 baht.

### 2.3 Non-VAT Registered Businesses
If the business is not registered for VAT:
- Issue a regular receipt (ใบเสร็จรับเงิน), not a tax invoice.
- Do not charge VAT. Record the gross amount into the liability account.

---

## 3. Withholding Tax (ภาษีเงินได้หัก ณ ที่จ่าย: WHT) Rules

Under Departmental Instruction **Por 73/2541** and **T.P. 4/2528**:
1. **Deposit for Goods:** No withholding tax (sale of goods is not subject to domestic withholding tax).
2. **Deposit for Services / Construction:** When a deposit represents an advance installment of service fees that will be offset against the final fee, the payer **must withhold tax (typically 3%)** from the pre-VAT deposit base at the time of paying the deposit.
3. **Refundable Security Deposit (เงินประกันการเช่า/ประกันสัญญา):** No withholding tax when received, because it is not income or service fee.

---

## 4. Standard Accounting Entries (บันทึกบัญชี)

### 4.1 Recipient Side (ผู้รับเงินมัดจำ)

#### A. Receiving Deposit for Services (e.g., 100,000 total, 30% deposit = 30,000 + VAT 2,100, WHT 3% = 900)
- Net cash received = 30,000 + 2,100 - 900 = 31,200 baht.
- Issue Tax Invoice / Receipt (ใบกำกับภาษี/ใบเสร็จรับเงิน) for 30,000 + VAT 2,100.

| Account | Debit (Dr) | Credit (Cr) |
|---|---|---|
| Cash / Bank (เงินสด/เงินฝากธนาคาร) | 31,200 | |
| Withholding Tax Withheld (ภาษีเงินได้ถูกหัก ณ ที่จ่าย - สินทรัพย์) | 900 | |
| Deposit Received / Advances from Customers (เงินมัดจำรับ / เงินรับล่วงหน้า - หนี้สิน) | | 30,000 |
| Output VAT (ภาษีขาย) | | 2,100 |

#### B. Final Delivery & Billing for Remaining Amount (70,000 remaining + VAT 4,900, WHT 3% = 2,100)
- Issue final Tax Invoice showing:
  - Total service fee: 100,000
  - Less: Previously invoiced deposit: (30,000)
  - Remaining taxable base: 70,000
  - Output VAT 7%: 4,900
  - Less: WHT 3% on remaining (70,000 × 3%): (2,100)
  - Net cash receivable: 72,800 baht.

| Account | Debit (Dr) | Credit (Cr) |
|---|---|---|
| Cash / Accounts Receivable (เงินสด/ลูกหนี้การค้า) | 72,800 | |
| Withholding Tax Withheld (ภาษีเงินได้ถูกหัก ณ ที่จ่าย) | 2,100 | |
| Deposit Received (เงินมัดจำรับ - ล้างหนี้สิน) | 30,000 | |
| Service Revenue (รายได้จากบริการ) | | 100,000 |
| Output VAT (ภาษีขาย) | | 4,900 |

---

### 4.2 Payer Side (ผู้จ่ายเงินมัดจำ)

#### A. Paying Deposit for Services (30,000 + VAT 2,100, WHT 3% = 900)
- Obtain Tax Invoice and issue 50 ทวิ certificate to vendor.

| Account | Debit (Dr) | Credit (Cr) |
|---|---|---|
| Deposit Paid / Advances to Suppliers (เงินมัดจำจ่าย / เงินจ่ายล่วงหน้า - สินทรัพย์) | 30,000 | |
| Input VAT (ภาษีซื้อ) | 2,100 | |
| Withholding Tax Payable (ภาษีเงินได้หัก ณ ที่จ่ายค้างจ่าย - ภ.ง.ด.53/3) | | 900 |
| Cash / Bank (เงินสด/เงินฝากธนาคาร) | | 31,200 |

#### B. Completion & Final Payment
- Recognize total expense of 100,000 baht and clear the asset.

| Account | Debit (Dr) | Credit (Cr) |
|---|---|---|
| Service Expense / Cost of Work (ค่าบริการ / ต้นทุนงาน) | 100,000 | |
| Input VAT (ภาษีซื้อ) | 4,900 | |
| Deposit Paid (เงินมัดจำจ่าย - ล้างสินทรัพย์) | | 30,000 |
| Withholding Tax Payable (ภาษีเงินได้หัก ณ ที่จ่ายค้างจ่าย) | | 2,100 |
| Cash / Accounts Payable (เงินสด/เจ้าหนี้การค้า) | | 72,800 |

---

## 5. Security Deposits for Leases (เงินประกันการเช่าตาม ป.73/2541)

To qualify for VAT exemption and no WHT under Departmental Instruction **Por 73/2541 Clause 3(2)**:
1. **Contractual obligation:** Agreement must explicitly state that the deposit will be returned immediately upon lease expiry without conditions requiring renewal.
2. **Lease duration:** Lease term must not exceed 3 years.
3. **Cap on deposit:** Total security deposits must not exceed 3 to 6 times the monthly rental.
4. **No compensation disguised:** Must not be treated as advance rent.

### Journal Entries for Qualified Lease Security Deposit (e.g., 60,000 baht)
- **Lessor (ผู้ให้เช่า):** Issue non-VAT receipt.
  - Dr. Bank 60,000
  - Cr. Security Deposit Received (เงินประกันการเช่ารับ - หนี้สิน) 60,000
- **Lessee (ผู้เช่า):**
  - Dr. Security Deposit Paid (เงินประกันการเช่าจ่าย - สินทรัพย์) 60,000
  - Cr. Bank 60,000

*Note: If the lessor later deducts unpaid rent or repair damages from this deposit, the deducted portion becomes taxable revenue and subject to VAT/WHT at that moment.*

---

## 6. Contract Breach, Forfeiture, and Refunds (ริบมัดจำ / คืนเงินมัดจำ)

### 6.1 Customer Breaches Contract $\rightarrow$ Seller Forfeits Deposit (ริบเงินมัดจำ)
- Under Civil and Commercial Code Section 378, the seller is entitled to forfeit the deposit.
- **Corporate Income Tax (CIT):** The forfeited deposit becomes **Other Income (รายได้อื่น - เงินมัดจำริบ)** and is subject to corporate income tax in ภ.ง.ด.50.
- **VAT:** The tax invoice was already issued and output VAT paid when the deposit was received. **Do NOT issue a new VAT invoice**, and **cannot issue a credit note** to cancel VAT.

| Account | Debit (Dr) | Credit (Cr) |
|---|---|---|
| Deposit Received (เงินมัดจำรับ - ล้างหนี้สิน) | 30,000 | |
| Other Income - Forfeited Deposit (รายได้อื่น - เงินมัดจำริบ) | | 30,000 |

### 6.2 Seller Breaches Contract $\rightarrow$ Returns Deposit + Penalty (คืนมัดจำ + จ่ายค่าปรับ)
- Under Civil and Commercial Code Section 380, if the seller breaches, the seller must return the deposit (and pay liquidated damages if agreed).
- **VAT on Return:** Issue a **Credit Note (ใบลดหนี้)** referencing the original tax invoice to adjust output VAT in ภ.พ.30.

| Account | Debit (Dr) | Credit (Cr) |
|---|---|---|
| Deposit Received (เงินมัดจำรับ) | 30,000 | |
| Output VAT (ภาษีขาย - จากการออกใบลดหนี้) | 2,100 | |
| Breach of Contract Expense (ค่าเสียหายจากการผิดสัญญา - ค่าใช้จ่ายอื่น) | 30,000 | |
| Cash / Bank (เงินสด/เงินฝากธนาคาร) | | 62,100 |

---

## 7. Retention in Construction Contracts (เงินประกันผลงาน)

In construction contracts, the owner often retains 5% or 10% from each progress bill:
- **Contractor billing:** Progress work 1,000,000 baht, VAT 7% = 70,000. Retention 10% = 100,000 baht.
- **Rule:** Retention does **not** reduce the VAT base or WHT base.
  - Tax invoice issued for: Base 1,000,000 + VAT 70,000 = 1,070,000.
  - Owner pays: $1,000,000 + 70,000 - 100,000 (\text{retention}) - 30,000 (\text{WHT 3\% on 1M}) = 940,000$ baht.
- **Contractor entry:**
  - Dr. Bank 940,000
  - Dr. Retention Receivable (ลูกหนี้เงินประกันผลงาน) 100,000
  - Dr. WHT Asset (ภาษีถูกหัก ณ ที่จ่าย) 30,000
  - Cr. Construction Revenue (รายได้ค่าก่อสร้าง) 1,000,000
  - Cr. Output VAT (ภาษีขาย) 70,000
- **Upon returning retention after warranty:**
  - Dr. Bank 100,000 / Cr. Retention Receivable 100,000 (No VAT, No WHT).

---

## 8. Common Mistakes & Rationalization Table

| Common Rationalization / Mistake | Reality & Correct Treatment |
|---|---|
| *"We received deposit money, so we can record it as Sales Revenue immediately."* | **Wrong.** Revenue cannot be recognized until performance obligations are satisfied (TFRS 15 / TFRS for NPAEs). Must be recorded as a Liability (เงินมัดจำรับ). |
| *"Goods/services are not delivered yet, so we will wait to issue the tax invoice later."* | **Wrong.** Under Sec. 78 and 78/1, receiving payment triggers the Tax Point immediately. Failure to issue a tax invoice results in fines, double penalties, and 1.5%/month surcharge under Sec. 89. |
| *"Deposit for buying equipment/goods must have 3% withholding tax."* | **Wrong.** Sales of goods are exempt from domestic withholding tax. Only services and hire of work incur withholding tax. |
| *"Gross payment is 107,000 incl. VAT, so VAT is 107,000 × 7% = 7,490 baht."* | **Wrong.** For VAT-inclusive totals, calculate with $\frac{7}{107}$. Base = 100,000 baht, VAT = 7,000 baht. |
| *"Rental security deposit must be charged 7% VAT."* | **Wrong.** If it complies with Por 73/2541 (term $\le$ 3 years, $\le$ 6 months rent, refundable), it is exempt from VAT. Issue a standard receipt, not a tax invoice. |
| *"On the final invoice, charge VAT on the entire 100,000 without deducting the 30,000 deposit already taxed."* | **Double taxation.** The final tax invoice must show the full price, deduct the previously invoiced deposit, and charge VAT only on the remaining 70,000 balance. |
| *"When customer cancels and we forfeit the deposit, we must issue a new tax invoice."* | **Wrong.** The tax invoice was already issued when cash was received. Record Dr. Deposit Received / Cr. Other Income. No new VAT invoice is needed. |
