---
name: accounting-fixed-asset-management
description: Use when managing fixed assets (การบริหารสินทรัพย์ถาวร), compiling and auditing the Fixed Asset Register (ทะเบียนสินทรัพย์ถาวร), evaluating CAPEX vs OPEX for repairs and maintenance, applying Thai tax incentives for SME initial depreciation allowances (ค่าเสื่อมราคาเบื้องต้นตาม พ.ร.ฎ. 395/473), recording asset sales or disposals with Output VAT, or analyzing the Fixed Asset Turnover Ratio.
---

# Fixed Asset Management & Tax Strategy (การบริหารสินทรัพย์ถาวรและภาษี)

## Overview

Fixed Assets (Property, Plant, and Equipment - PPE / สินทรัพย์ถาวร) are tangible assets held for use in the production or supply of goods/services, for rental to others, or for administrative purposes, expected to be used for more than one accounting period (TAS 16 / TFRS for NPAEs Chapter 10).

Effective asset management oversees the 4 stages of the asset lifecycle:
1. **Acquisition (การจัดหา):** Capital budgeting, vendor selection, PO issuance, and initial cost capitalization.
2. **Utilization & Maintenance (การใช้งานและบำรุงรักษา):** Location tracking, maintenance logs, and CAPEX vs. OPEX classification.
3. **Measurement & Depreciation (การวัดมูลค่าและคิดค่าเสื่อมราคา):** Monthly depreciation, impairment testing, and tax allowance optimization.
4. **Disposal & Retirement (การจำหน่ายและตัดจำหน่าย):** Sale, scrapping, trade-in, and output VAT compliance.

---

## 1. Fixed Asset Register (ทะเบียนสินทรัพย์ถาวร)

A comprehensive Fixed Asset Register is required by the Revenue Department and external auditors. Every asset must carry an identification tag (Barcode / QR Code / Metal Tag).

### Essential Data Fields in the Register:

| Category | Specific Data Points | Purpose |
|---|---|---|
| **Identity** | Asset Tag Code, Asset Description, Brand, Model, Serial Number (S/N). | Unambiguous identification during physical audits. |
| **Location & Custody** | Department, Branch/Plant, Room/Floor, Named Custodian/Operator. | Custodial accountability; prevents theft or loss. |
| **Acquisition Data** | Purchase Date, Invoice / Tax Invoice No., Vendor Name, Purchase Cost. | Audit trail linking ledger balance to tax documents. |
| **Accounting Data** | Useful Life (Years), Salvage Value, Depreciation Method, Monthly Depreciation. | Periodic journal entry calculation. |
| **Carrying Amounts** | Cost, Accumulated Depreciation (Accounting & Tax), Net Book Value (NBV). | Balance sheet valuation and tax return reconciliation. |
| **Physical Status** | Condition (Active, Idle, Under Repair, Scrapped), Last Physical Count Date. | Impairment signals and disposal triggers. |

*Audit Requirement:* Perform a full physical count of fixed assets at least **once per fiscal year** before financial year-end closing.

---

## 2. CAPEX vs. OPEX: Accounting for Subsequent Costs

When money is spent on existing machinery, vehicles, or buildings, accountants must classify the expenditure correctly:

```
                                [Subsequent Expenditure]
                                           |
           +-------------------------------+-------------------------------+
           |                                                               |
  [Restores to Normal Condition]                                [Significantly Enhances]
  • Routine oil changes / servicing                            • Extends useful life (> 1-2 years)
  • Replacing worn belts / fuses                                • Substantially increases capacity (> 20%)
  • Repainting walls / minor patches                            • Re-engineers machine to new specs
           |                                                               |
           v                                                               v
  [OPEX - Revenue Expenditure]                                   [CAPEX - Capital Expenditure]
  • Expense immediately in current period                       • Capitalize into Asset Cost (Dr. Asset)
  • Deductible in full in current year                          • Depreciate over revised remaining life
```

### Journal Entries:
- **OPEX (e.g., Routine maintenance 25,000 THB + 7% VAT):**
  - Dr. Repairs & Maintenance Expense (ค่าซ่อมแซมและบำรุงรักษา) 25,000
  - Dr. Input VAT (ภาษีซื้อ) 1,750
  - Cr. Cash / Bank / AP 26,750
- **CAPEX (e.g., Major CNC overhaul increasing life by 3 years, 400,000 THB + 7% VAT):**
  - Dr. Machinery & Equipment (เครื่องจักรและอุปกรณ์ - เพิ่มราคาทุน) 400,000
  - Dr. Input VAT (ภาษีซื้อ) 28,000
  - Cr. Cash / Bank / AP 428,000

---

## 3. Thai Tax Depreciation & SME Special Initial Allowances

### 3.1 SME Statutory Definition
To qualify for SME tax incentives under the Thai Revenue Code, a company must meet **both** criteria at the end of the tax year:
1. Paid-up capital $\le$ **5,000,000 THB**, AND
2. Total annual revenue $\le$ **30,000,000 THB**.

### 3.2 Special Initial Depreciation Allowance (พ.ร.ฎ. ฉบับที่ 395/473)
Qualified SMEs are entitled to deduct an **Initial Allowance (ค่าเสื่อมราคาเบื้องต้น)** immediately on the acquisition date, then depreciate the remainder over the statutory useful life:

| Asset Category | Special Initial Allowance (Day 1) | Depreciation on Remaining Balance | Total Year 1 Tax Deduction |
|---|:---:|:---:|:---:|
| **Machinery & Equipment for Production** | **40%** of initial cost | Remainder (60%) over useful life (e.g., 5 yrs = 12%/yr) | **52%** of cost in Year 1 |
| **Computers, Peripherals & Software** | **40%** of initial cost | Remainder (60%) over 3 years (20%/yr) | **60%** of cost in Year 1 |
| **Factory Buildings for SME** | **25%** of initial cost | Remainder (75%) at 5%/yr (over 20 yrs) | **28.75%** of cost in Year 1 |

*Worked Example (SME buys CNC machine for 1,000,000 THB on 1 Jan, 5-year life):*
- Initial 40% Allowance = $1,000,000 \times 40\% = \mathbf{400,000}$ THB.
- Remaining basis = $600,000$ THB. Normal depreciation = $\frac{600,000}{5} = \mathbf{120,000}$ THB.
- **Total Year 1 Tax Depreciation = 400,000 + 120,000 = 520,000 THB.**
- *Accounting straight-line:* $\frac{1,000,000}{5} = 200,000$ THB.
- *Tax Shield benefit:* Additional 320,000 THB deduction reduces Year 1 taxable profit, saving 48,000 THB in corporate income tax (at SME rate of 15%).

### 3.3 Statutory Limitations on Passenger Cars (ม.65 ตรี (20) & พ.ร.ฎ. 315)
- For passenger motor vehicles with $\le 10$ seats: Tax depreciation cost base is strictly **capped at 1,000,000 THB**, regardless of the actual purchase price.
- If purchased for 2,500,000 THB, accounting depreciates the full 2.5M THB, but tax deduction is limited to $\frac{1,000,000}{5} = 200,000$ THB/year. The excess depreciation must be added back in Form ภ.ง.ด.50.

---

## 4. Asset Disposal & Replacement (การจำหน่ายสินทรัพย์)

When fixed assets are sold, scrapped, or retired:

### 4.1 Output VAT on Asset Sales
Selling business fixed assets (vehicles, machinery, furniture) is legally classified as a **Sale of Goods (การขายสินค้า)** under Revenue Code Section 77/1(8).
- The business **must issue a Tax Invoice and charge 7% Output VAT** on the agreed sales price.

### 4.2 Calculating Gain or Loss on Disposal
$$\text{Net Book Value (NBV)} = \text{Historical Cost} - \text{Accumulated Depreciation}$$
$$\text{Gain (Loss) on Disposal} = \text{Selling Price (Excl. VAT)} - \text{Net Book Value}$$

### 4.3 Standard Journal Entry for Asset Sale
*(Example: Machine sold for 700,000 THB + 7% VAT 49,000 THB. Cost = 1,000,000 THB; Accumulated Depreciation = 400,000 THB; NBV = 600,000 THB $\rightarrow$ Gain = 100,000 THB):*

| Account | Debit (THB) | Credit (THB) |
|---|---:|---:|
| **Cash / Bank / Receivable** | 749,000 | |
| **Accumulated Depreciation - Machinery (ล้างค่าเสื่อมสะสม)** | 400,000 | |
| **Machinery & Equipment (ล้างราคาทุนเดิม)** | | 1,000,000 |
| **Output VAT (ภาษีขาย 7% - ภ.พ.30)** | | 49,000 |
| **Gain on Disposal of Fixed Assets (กำไรจากการขาย - รายได้อื่น)** | | 100,000 |

---

## 5. Efficiency Metric: Fixed Asset Turnover Ratio

Evaluates how productively the company utilizes its fixed asset investment to generate sales:

$$\text{Fixed Asset Turnover Ratio} = \frac{\text{Net Sales / Total Revenue}}{\text{Average Net Fixed Assets}}$$

- **Interpretation:**
  - A higher ratio indicates efficient asset utilization and high production capacity utilization.
  - A declining ratio suggests over-investment in idle machinery, operational bottlenecks, or declining market demand.

---

## 6. Common Mistakes & Rationalization Table

| Common Rationalization / Mistake | Reality & Correct Treatment |
|---|---|
| *"We sold a company car to an employee, so we don't need to charge VAT."* | **Tax Violation.** Fixed asset sales are deemed sales of goods under Sec. 77/1(8). You must issue a Tax Invoice and remit 7% Output VAT. |
| *"We installed a new 500,000 THB automation arm on the old machine, but expensed it as repairs to reduce profit today."* | **Audit Risk.** Enhancements that materially boost capacity or life must be capitalized as CAPEX. Revenue officers will disallow the expense upon audit. |
| *"We are an SME, so we claimed 40% initial allowance on our luxury company van."* | **Illegal Deduction.** Initial allowances under Royal Decree 395 apply only to production machinery, computers, and factory buildings—not passenger cars. |
| *"Our old machine is fully depreciated to 1 baht book value, so we removed it from our records."* | **Asset Loss Risk.** As long as the physical machine remains in the factory and is operational, it must remain on the Fixed Asset Register at Cost = 1,000,000, Acc. Dep. = 999,999, NBV = 1 baht. |
| *"We don't need to do a physical asset count because everything is recorded in accounting software."* | **Ghost Asset Risk.** Physical verification reveals stolen, damaged, or discarded assets that must be written off to prevent insurance overpayment and property tax errors. |
