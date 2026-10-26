---
name: accounting-inventory-management
description: Use when designing or auditing inventory management systems (การบริหารสินค้าคงคลัง), calculating Economic Order Quantity (EOQ), establishing Safety Stock and Reorder Points (ROP), classifying stock using ABC analysis, evaluating Inventory Turnover Ratio and Days Sales of Inventory (DSI), and applying Thai accounting standards (TAS 2 / TFRS for NPAEs Chapter 8 prohibiting LIFO).
---

# Inventory Management & Costing (การบริหารสินค้าคงคลังและต้นทุน)

## Overview

Inventory is cash converted into physical goods. Managing inventory involves balancing two opposing risks:
1. **Holding too much inventory (เงินจม):** Traps working capital, incurs holding and warehousing costs, and increases the risk of obsolescence, spoilage, or shrinkage.
2. **Holding too little inventory (ของขาดสต๊อก):** Causes stockouts, lost sales revenue, customer dissatisfaction, and rush-order delivery premiums.

Inventory is classified into three categories depending on the business model:
- **Raw Materials (วัตถุดิบ):** Direct inputs for manufacturing.
- **Work in Process (งานระหว่างทำ / WIP):** Semi-finished goods currently in production.
- **Finished Goods (สินค้าสำเร็จรูป):** Completed goods ready for sale to customers.

---

## 1. Inventory Replenishment Models

### 1.1 Economic Order Quantity (EOQ - ปริมาณการสั่งซื้อที่ประหยัดที่สุด)
EOQ identifies the optimal order quantity ($Q^*$) that minimizes the total cost of ordering and holding inventory:

$$\text{EOQ} = \sqrt{\frac{2 \times D \times S}{H}}$$

- $D$ = Annual demand (ความต้องการสินค้าต่อปี in units)
- $S$ = Fixed ordering cost per order (ต้นทุนการสั่งซื้อต่อครั้ง in baht)
- $H$ = Annual holding/carrying cost per unit (ต้นทุนการเก็บรักษาต่อหน่วยต่อปี in baht)

**Derivative Calculations:**
- **Annual Orders ($N$):** $N = \frac{D}{\text{EOQ}}$
- **Cycle Time ($T$):** $T = \frac{365}{N}$ days between purchase orders.

*Worked Example:*
- $D = 1,200$ units/year, $S = 500$ baht/order, $H = 10$ baht/unit/year.
- $\text{EOQ} = \sqrt{\frac{2 \times 1,200 \times 500}{10}} = \sqrt{120,000} \approx \mathbf{346} \text{ units/order}$.
- Annual orders $N = \frac{1,200}{346} \approx \mathbf{3.47} \text{ orders/year}$.
- Order every $T = \frac{365}{3.47} \approx \mathbf{105} \text{ days}$ (approximately every 3.5 months).

---

### 1.2 Safety Stock (สต๊อกสำรองเพื่อความปลอดภัย)
Buffer inventory held to protect against supplier lead-time delays or sudden demand surges:

$$\text{Safety Stock} = (\text{Max Daily Sales} - \text{Average Daily Sales}) \times \text{Lead Time (days)}$$

*Worked Example:*
- Average daily sales = 10 units, Peak daily sales = 15 units, Supplier lead time = 7 days.
- $\text{Safety Stock} = (15 - 10) \times 7 = 5 \times 7 = \mathbf{35} \text{ units}$.

---

### 1.3 Reorder Point (ROP - จุดสั่งซื้อซ้ำ)
The inventory level that automatically triggers issuing a new Purchase Order:

$$\text{ROP} = (\text{Average Daily Sales} \times \text{Lead Time}) + \text{Safety Stock}$$

*Worked Example (Continuing above):*
- $\text{ROP} = (10 \times 7) + 35 = 70 + 35 = \mathbf{105} \text{ units}$.
- *Action:* The moment physical + on-order balance reaches 105 units, Purchasing must immediately release the PO.

---

## 2. ABC Inventory Classification (Pareto Principle: 80/20 Rule)

Stratifies inventory into three categories based on annual consumption value, directing management effort where impact is greatest:

| Category | % of Total SKUs | % of Total Annual Value | Control Strategy |
|:---:|:---:|:---:|---|
| **Class A** | **15% – 20%** | **70% – 80%** | **Tightest Control:** Daily/weekly perpetual tracking, frequent cycle counting, rigorous safety stock calculation, strategic vendor partnerships. |
| **Class B** | **30% – 35%** | **15% – 20%** | **Moderate Control:** Automated replenishment using standard EOQ and ROP, quarterly stock counts. |
| **Class C** | **45% – 50%** | **5% – 10%** | **Simplified Control:** Low unit cost bulk items (screws, packaging, staples). Managed via 2-Bin system, reordered in bulk, counted semi-annually or annually. |

---

## 3. Financial Efficiency Metrics

### 3.1 Inventory Turnover Ratio (อัตราการหมุนเวียนสินค้าคงคลัง)
Measures how many times inventory is sold and replaced over a defined period (usually 1 year):

$$\text{Inventory Turnover Ratio} = \frac{\text{Cost of Goods Sold (COGS)}}{\text{Average Inventory}}$$
$$\text{Average Inventory} = \frac{\text{Beginning Inventory} + \text{Ending Inventory}}{2}$$

### 3.2 Days Sales of Inventory (DSI / Days Inventory Outstanding)
The average number of days it takes for inventory to turn into sales:

$$\text{DSI} = \frac{365}{\text{Inventory Turnover Ratio}} = \frac{\text{Average Inventory} \times 365}{\text{COGS}}$$

*Worked Example:*
- COGS = 3,000,000 baht. Beginning stock = 600,000 baht, Ending stock = 400,000 baht.
- Average Inventory = $\frac{600,000 + 400,000}{2} = 500,000$ baht.
- $\text{Inventory Turnover} = \frac{3,000,000}{500,000} = \mathbf{6.0} \text{ turns/year}$.
- $\text{DSI} = \frac{365}{6.0} \approx \mathbf{60.8} \text{ days}$ (stock turns over every 2 months).

### Benchmark Guidelines:
- **Fast-Moving Consumer Goods (FMCG):** 8 – 14 turns/year (25 – 45 days)
- **General E-Commerce / Retail:** 6 – 10 turns/year (36 – 60 days)
- **Manufacturing / Machinery:** 4 – 8 turns/year (45 – 90 days)

---

## 4. Thai Accounting & Tax Compliance (TAS 2 & TFRS for NPAEs)

### 4.1 Permitted Costing Methods
Under Thai Accounting Standards (TAS 2 / TFRS for NPAEs Chapter 8):
1. **FIFO (First-In, First-Out: วิธีเข้าก่อน-ออกก่อน):** Assumes oldest inventory is sold first.
2. **Weighted Average Cost (วิธีถัวเฉลี่ยถ่วงน้ำหนัก / ถัวเฉลี่ยเคลื่อนที่):** Unit cost is averaged across available inventory.
3. **Specific Identification (วิธีราคาเจาะจง):** Strictly for non-interchangeable, segregated projects or high-value items (e.g., custom machinery, real estate).

### 4.2 Strict Prohibition of LIFO (Last-In, First-Out)
> **LIFO is strictly prohibited** under Thai Accounting Standards and the Thai Revenue Code (มาตรา 65 ทวิ (6)).
- **Why LIFO is banned:**
  1. *Physical unreality:* Companies sell oldest stock first to avoid expiration/obsolescence.
  2. *Distorted balance sheet:* Balance sheet inventory is valued at outdated historical costs.
  3. *Tax avoidance:* In inflationary periods, LIFO artificially inflates COGS and understates taxable profit.

### 4.3 Lower of Cost and Net Realizable Value (LCNRV)
At each balance sheet date, inventory must be measured at the lower of historical cost and Net Realizable Value (NRV = Estimated Selling Price less Completion and Selling Costs).
- If $\text{NRV} < \text{Cost}$, write down inventory:
  - **Dr.** Loss on Devaluation of Inventory (ขาดทุนจากการลดมูลค่าสินค้า - งบกำไรขาดทุน)
  - **Cr.** Allowance for Inventory Devaluation (ค่าเผื่อมูลค่าสินค้าลดลง - บัญชีปรับลดยอดสินค้า)

---

## 5. Common Mistakes & Rationalization Table

| Common Rationalization / Mistake | Reality & Correct Treatment |
|---|---|
| *"Suppliers offer a 10% volume discount, so let's buy a 2-year supply."* | **Flawed Trade-off.** Excessive bulk orders inflate holding costs, increase damage/expiration risks, and drain cash flow far exceeding the 10% discount. Run EOQ with discount analysis first. |
| *"We don't need a formal safety stock; we just order when we run low."* | **Frequent Stockouts.** Without calculated safety stock based on supplier lead times, demand spikes cause lost sales and emergency freight surcharges. |
| *"We count all 2,000 SKUs every month."* | **Operational Waste.** Use ABC Analysis: Count Class A items monthly, Class B quarterly, and Class C annually. |
| *"High Inventory Turnover is always positive."* | **Warning Sign if Too High.** Extremely high turnover (> 25 turns) often signals chronically inadequate stock, causing frequent stockouts and lost revenue. |
| *"We can use LIFO for management reports because raw material prices rose."* | **Prohibited.** Thai GAAP and the Revenue Code require FIFO or Weighted Average. Maintain consistency across management and statutory books. |
