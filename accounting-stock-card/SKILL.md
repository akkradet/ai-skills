---
name: accounting-stock-card
description: Use when building or checking a stock card (บัตรคุมสินค้า, บัตรสต๊อกสินค้า, Stock Card) for inventory, recording goods received, sold, returned, or lost, computing running balances and inventory cost under FIFO or moving weighted-average methods, costing cost of goods sold (ต้นทุนขาย), handling physical count shortages or shrinkage (สินค้าขาด, ยอดไม่ตรงนับ), accounting for deemed sales and Output VAT under Revenue Code Section 77/1(8)(j), understanding differences between Stock Cards and VAT Goods and Materials Reports (รายงานสินค้าและวัตถุดิบ ตาม ม.87(3)), setting reorder points, or setting up inventory spreadsheets in Excel or Google Sheets.
---

# Stock Card (บัตรคุมสินค้า)

## Overview

A stock card records every movement of one product, in date order: what came in, what went out, and the balance after each line. **One product, one card.**

The card answers three fundamental questions:
1. How much is on hand now?
2. Which document caused each movement?
3. What did those goods cost?

Keep the card in a single unit of measure, and correct errors with a visible adjustment line—**never by editing or overwriting a past balance**.

---

## 1. Document Comparison: Stock Card vs. Goods & Materials Report vs. Count Sheet

| Comparison Dimension | บัตรคุมสินค้า (Stock Card) | รายงานสินค้าและวัตถุดิบ (ม.87(3)) | ใบตรวจนับสินค้า (Count Sheet) |
|---|---|---|---|
| **Authority / Requirement** | **Internal business policy** (Warehouse / Accounting). | **Mandatory by VAT Law** (Revenue Code Sec. 87(3) & DG Notification No. 89). | **Internal business policy** (Stock Count Committee). |
| **Purpose** | Track unit movements, running balance, and itemized inventory costing for internal control and COGS calculation. | Official tax record provided to Revenue Department officers to audit quantities received, issued, and on hand per business place/branch. | Record actual physical count on a specific date to reconcile against stock cards. |
| **Legal / Tax Consequences** | No statutory template, but must be retained for at least 5 years under the Accounting Act B.E. 2543. | Must record entries within **3 working days**. Unexplained shortages are **deemed a sale under Sec. 77/1(8)(j)** subject to 7% Output VAT. | Serves as evidentiary support for adjustment vouchers (`ADJ-...`). Without signed count sheets, shortages cannot be defended in a tax audit. |

---

## 2. Card Layout and Essential Columns

**Header Information:**
- Product Name & Product Code (e.g., `PEN-BL-05`)
- Single Unit of Measure (e.g., Box of 50 pens)
- Storage Location (e.g., Shelf A2)
- Reorder Point (จุดสั่งซื้อ - e.g., 40 boxes)
- Costing Method (FIFO or Moving Weighted Average)

**Body Columns:**

| Column | Content | Notes |
|---|---|---|
| **Date** | Date the movement occurred | Chronological order |
| **Document No.** | Reference voucher (PO, Invoice, Delivery Note, CN, ADJ) | Mandatory for audit trail |
| **Description** | Supplier lot, customer name, return, or count adjustment | Plain and specific |
| **Qty In (รับ)** | Units received | Purchases, customer returns |
| **Qty Out (จ่าย)** | Units issued | Sales, internal withdrawals, scrap |
| **Balance Qty (คงเหลือ)** | Cumulative balance | Previous Balance + In − Out |
| **Unit Cost (ต้นทุน/หน่วย)** | Cost per unit for this line | Required for costing stock cards |
| **Value In / Out / Balance** | Monetary amounts | Total inventory value tracking |

*For perishable or medical goods, add **Lot Number** and **Expiry Date** columns, enforcing First-Expired, First-Out (FEFO).*

---

## 3. Operational Rules

1. **Strict Unit of Measure:** Use one consistent unit across the entire card. If purchased in cartons but sold in boxes, convert at the header level before entry. Mixing units is the #1 cause of stock balance errors.
2. **No Movement Without Documents:** Every line must cite an authorized document. Goods cannot leave the warehouse without an approved invoice or internal withdrawal slip.
3. **Timing:** Log movements daily, or at least within 3 working days for VAT-registered businesses.
4. **Permanent Audit Trail:** Never overwrite past balances or delete rows. Correct errors by posting a new adjustment line citing an adjustment memo (`ADJ-...`).
5. **Reorder Point Monitoring:** Trigger purchase orders when the running balance falls below the reorder threshold.

---

## 4. Costing Methods (TFRS for NPAEs Chapter 8)

Businesses choose from three accepted costing methods under Thai accounting standards:
- **FIFO (First-In, First-Out):** Goods sold take the unit cost from the oldest available batches.
- **Moving Weighted Average (ถัวเฉลี่ยเคลื่อนที่):** Recompute the weighted average unit cost after every receipt:
  $$\text{New Average Unit Cost} = \frac{\text{Previous Balance Value} + \text{Received Value}}{\text{Previous Balance Qty} + \text{Received Qty}}$$
  Issues and sales use this current average until the next receipt.
- **Specific Identification (วิธีราคาเจาะจง):** Used for unique, high-value, non-interchangeable goods.

*Consistency Rule:* Once chosen, the method must be applied consistently across periods. Switching methods requires justified accounting changes and financial statement disclosure.

---

## 5. Worked Example: Khun Ta's Stationery Wholesale

**Product:** Blue ballpoint pen 0.5 mm (Box of 50), PEN-BL-05.
- 1 Oct: Opening balance: 40 boxes @ 200 baht = 8,000 baht.
- 4 Oct (PI-003): Purchased Lot 1: 60 boxes @ 200 baht = 12,000 baht. (Balance: 100 boxes)
- 10 Oct (IV-021): Sold 70 boxes to school. (Balance: 30 boxes $\rightarrow$ below reorder point of 40!)
- 15 Oct (PI-009): Purchased Lot 2: 120 boxes @ 225 baht = 27,000 baht. (Balance: 150 boxes)
- 22 Oct (IV-058): Sold 80 boxes to copy shop. (Balance: 70 boxes)
- 27 Oct (CN-004): Customer return from copy shop: 2 boxes. (Balance: 72 boxes)
- 31 Oct (ADJ-001): Physical stock count found only 71 boxes $\rightarrow$ **Shortage of 1 box**.

### Cost Allocation Comparison (Total Cost Pool = 47,000 Baht)

| Item | FIFO | Moving Weighted Average |
|---|---|---|
| **Balance after 10 Oct sale (30 boxes)** | $30 \times 200 = 6,000$ | $30 \times 200 = 6,000$ |
| **Balance after Lot 2 purchase (150 boxes)** | $30 \times 200 + 120 \times 225 = 33,000$ | 150 boxes, 33,000 baht ($\text{Avg} = 220/\text{box}$) |
| **Cost of Sale 22 Oct (80 boxes)** | $30 \times 200 + 50 \times 225 = 17,250$ | $80 \times 220 = 17,600$ |
| **Return 27 Oct (2 boxes)** | Reverse $2 \times 225 = (450)$ | Reverse $2 \times 220 = (440)$ |
| **Net Cost of Goods Sold (COGS)** | **30,800** ($14,000 + 17,250 - 450$) | **31,160** ($14,000 + 17,600 - 440$) |
| **Shortage 31 Oct (1 box write-off)** | $1 \times 225 = \mathbf{225}$ | $1 \times 220 = \mathbf{220}$ |
| **Ending Inventory Value (71 boxes)** | $71 \times 225 = \mathbf{15,975}$ | $71 \times 220 = \mathbf{15,620}$ |
| **Reconciliation Check** | $30,800 + 225 + 15,975 = \mathbf{47,000}$ | $31,160 + 220 + 15,620 = \mathbf{47,000}$ |

*Key Takeaway:* In an inflationary environment (purchase price rising from 200 to 225), **FIFO yields lower COGS, higher reported net income, and higher ending inventory on the balance sheet** compared to Weighted Average.

---

## 6. Physical Count Shortage & Thai Tax Law (ม.77/1(8)(จ))

When actual stock is less than the book balance:

### 6.1 Stock Card Adjustment Entry
Add an adjustment line on the count date:
- Date: 31 Oct
- Doc No: `ADJ-6910-001`
- Description: "ปรับปรุงสินค้าขาดจากการตรวจนับ 1 กล่อง"
- Qty Out: 1 box
- Running Balance: 71 boxes

### 6.2 VAT Implications: Deemed Sale (ถือเป็นการขาย)
Under **Revenue Code Section 77/1(8)(j)**:
- Inventory shortages from the Goods and Materials Report that cannot be proven as resulting from force majeure (เหตุสุดวิสัย) are legally **deemed a sale**.
- The business must pay **7% Output VAT based on the Market Price (ราคาตลาด)** of the missing goods.
- **Invoicing & Reporting:** Do **not** issue a tax invoice to any customer. Record the output VAT directly in the **Output VAT Report (รายงานภาษีขาย)** under the description "สินค้าขาดจากรายงานตาม ม.77/1(8)(จ)" and remit via Form ภ.พ.30.
- **Corporate Income Tax (CIT):** The Output VAT paid cannot be collected from anyone; it is an expense of the business, but is a **non-deductible tax expense under Section 65 Ter (6)** (ต้องบวกกลับใน ภ.ง.ด.50).

### 6.3 Standard Journal Entries (Perpetual System)

**A. Write-off Inventory Shortage (FIFO basis = 225 baht):**
- Dr. Loss on Inventory Shortage (ขาดทุนจากสินค้าขาดตรวจนับ - ค่าใช้จ่ายอื่น) 225
- Cr. Finished Goods / Inventory (สินค้าคงเหลือ) 225

**B. Output VAT on Deemed Sale (e.g., selling price = 300 baht $\rightarrow$ VAT 7% = 21 baht):**
- Dr. Output VAT Expense on Inventory Shortage (ภาษีขายจากสินค้าขาด - รายจ่ายต้องห้าม ม.65 ตรี (6)) 21
- Cr. Output VAT (ภาษีขาย - นำส่ง ภ.พ.30) 21

---

## 7. Common Root Causes of Inventory Mismatches

| Cause | Symptom | Corrective Action |
|---|---|---|
| Damaged or expired goods discarded without record | Book > Physical | Issue official scrap write-off voucher before disposing. |
| Internal staff usage or promotional samples | Book > Physical | Require an internal withdrawal slip (ใบเบิกใช้ภายใน) for every non-sale issue. |
| Receiving goods but waiting for tax invoice | Physical > Book | Log receipt immediately from the Delivery Note (ใบส่งของ); do not wait for the tax invoice. |
| Mixed units of measure (cartons vs. pieces) | Major factor errors | Mandate a single unit of measure in the card header. |
| Delayed or batch batch-posting | Discrepancies mid-month | Enforce daily posting or within the 3-day statutory window. |

---

## 8. Common Mistakes & Rationalization Table

| Common Rationalization / Mistake | Reality & Correct Treatment |
|---|---|
| *"We found an error from two weeks ago, so let's just edit that row in Excel."* | **Wrong.** Overwriting past entries destroys the audit trail. Post a distinct adjustment row with an `ADJ` document reference. |
| *"Stock shortage is small, so we can just lump it into Cost of Goods Sold."* | **Wrong.** Inventory shortages are a separate operating loss (ค่าใช้จ่ายอื่น), not COGS. Furthermore, unexplained shortages require Output VAT remittance under Sec. 77/1(8)(j). |
| *"We don't need a stock card because we only sell services."* | **Correct for pure services**, but any business selling goods, consumables, or maintaining spare parts must track inventory. |
| *"Stock cards and VAT Goods & Materials Reports are the same thing."* | **Different.** Stock cards are internal management records. The Goods & Materials Report is an official tax document mandated by Sec. 87(3) with rigid statutory compliance. |
| *"Calculate Output VAT on missing stock using cost price."* | **Wrong.** Section 79/3 requires Output VAT on deemed sales to be calculated based on **Market Value (ราคาตลาด)**, not historical cost. |
| *"Throwing away spoiled goods doesn't need tax paperwork."* | **Wrong.** To avoid deemed sale VAT on spoiled stock, businesses must follow the Revenue Department's formal destruction guidelines (แจ้งล่วงหน้า, มีผู้สอบบัญชีร่วมเป็นพยานตรวจทำลาย). |
