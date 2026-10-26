---
name: accounting-cal-asset-depreciation
description: Use when calculating depreciation (ค่าเสื่อมราคา) of fixed assets, choosing between straight-line, double-declining, sum-of-the-years-digits or units-of-production methods, setting salvage value (มูลค่าซาก), depreciating an asset bought mid-year, computing accumulated depreciation or book value, or looking up Thai tax depreciation rates (อัตราสรรพากร) versus accounting depreciation.
---

# Asset Depreciation Calculation (ค่าเสื่อมราคาสินทรัพย์)

## Overview

Depreciation spreads the depreciable cost of a fixed asset over its useful life. Depreciable amount = cost − salvage value. Accounting follows TAS 16; tax follows Thai Revenue Department rules. **These two are calculated separately** and reconciled later.

## Inputs to Collect

| Input | Notes |
|-------|-------|
| Cost (ต้นทุน) | Purchase price plus costs to bring asset to working condition |
| Salvage value (มูลค่าซาก) | Expected sale value at end of life. Review at least each year-end (TAS 16). Setting it to 1 baht is common practice but needs a reasoned basis |
| Useful life (อายุการใช้งาน) | Years, or total units for units-of-production |
| Start date | Needed for mid-year purchases |
| Method | See table below |

## Choosing a Method

| Method | Formula | Use when |
|--------|---------|----------|
| Straight-line (เส้นตรง) | (Cost − Salvage) ÷ Life | Default for most assets; SMEs mostly use this |
| Double-declining (ยอดลดลงทวีคูณ) | Opening book value × (2 ÷ Life) | Asset loses value fast early (vehicles, computers) |
| Sum-of-years-digits (ผลรวมจำนวนปี) | (Cost − Salvage) × (remaining years ÷ sum of years) | Asset wear is uneven, declining each year |
| Units of production (ตามจำนวนผลผลิต) | (Cost − Salvage) ÷ total units × units this period | Machines measured by output |

Sum of years = n(n+1)/2 (for 5 years: 15).

## Procedure

1. Confirm cost, salvage, life, and start date.
2. Compute depreciable amount = cost − salvage.
3. Apply the chosen method for each year (or month).
4. If purchased mid-year, prorate the first year: annual amount × months used ÷ 12. Count the purchase month as used when the asset is put into service.
5. Track accumulated depreciation; book value = cost − accumulated depreciation. Book value must never fall below salvage.
6. Record the journal entry each period.

## Double-Declining: Rules

- Rate = 2 ÷ life (5 years → 40%).
- Apply the rate to opening book value each year.
- Stop at salvage. In the final year, depreciate whatever remains above salvage (the source article does this for a zero-salvage example).

## Journal Entry

| Account | Dr | Cr |
|---------|----|----|
| Depreciation expense (ค่าเสื่อมราคา) | X | |
| Accumulated depreciation (ค่าเสื่อมราคาสะสม, contra asset) | | X |

## Tax Depreciation (ค่าเสื่อมราคาทางภาษี)

- Use maximum rates from the Revenue Department tables. Accounting may use a different rate, but the tax deduction is capped at the statutory rate.
- Reference rates as stated in the source article (verify against current Royal Decrees before filing):

| Asset | Max rate/year | Life |
|-------|---------------|------|
| Permanent buildings | 5% | 20 years |
| Temporary buildings | 100% | 1 year |
| Machinery and equipment | 20% | 5 years |
| Trucks and vans | 20% | 5 years |
| Passenger cars | 20% | 5 years (cost cap 1,000,000 baht for tax) |
| Computers and software | 33.33% | 3 years |
| Office furniture and equipment | 20% | 5 years |

- Passenger cars: tax deduction is based on at most 1,000,000 baht of cost even if the purchase price is higher. Accounting uses the full cost; the difference is added back in corporate income tax.
- **Verify before relying on these:** that tax depreciation uses straight-line only, and whether tax depreciation applies the rate to full cost rather than cost minus salvage. Confirm the current rates and any temporary measures (such as first-year extra allowances) with the Revenue Department or an accountant.

## Worked Examples (checked)

**Straight-line.** Printer: cost 50,000, salvage 5,000, life 5 years.
(50,000 − 5,000) ÷ 5 = **9,000 per year**.

**Double-declining.** Cost 100,000, life 5 years, rate 40%, zero salvage.

| Year | Opening BV | Depreciation | Closing BV |
|------|-----------|--------------|------------|
| 1 | 100,000 | 40,000 | 60,000 |
| 2 | 60,000 | 24,000 | 36,000 |
| 3 | 36,000 | 14,400 | 21,600 |
| 4 | 21,600 | 8,640 | 12,960 |
| 5 | 12,960 | 12,960 (remainder) | 0 |

**Sum-of-years-digits.** Cost 50,000, salvage 5,000, life 5 years (depreciable 45,000, sum 15).

| Year | Fraction | Depreciation |
|------|----------|--------------|
| 1 | 5/15 | 15,000 |
| 2 | 4/15 | 12,000 |
| 3 | 3/15 | 9,000 |
| 4 | 2/15 | 6,000 |
| 5 | 1/15 | 3,000 |

**Units of production.** Machine cost 200,000, salvage 20,000, total output 100,000 units, this year 25,000 units.
Rate = 180,000 ÷ 100,000 = 1.80/unit; this year = 1.80 × 25,000 = **45,000**.

**Mid-year purchase.** Machine bought in April, annual depreciation 60,000 (straight-line).
First year: 60,000 × 9 ÷ 12 = **45,000** (April–December). Following years: full 60,000.

**Notebook computer.** Cost 30,000, salvage 1 baht, 3 years.
(30,000 − 1) ÷ 3 = 9,999.67 per year, usually rounded to **10,000**. Monthly ≈ 833. Round consistently and make the final year absorb the rounding difference so total depreciation equals depreciable amount.

**Car, accounting vs tax.** Cost 1,500,000, salvage 1 baht, 5 years.
Accounting: ≈ 300,000 per year. Tax (cost capped at 1,000,000): ≈ 200,000 per year. Difference 100,000 per year is added back for tax.

**Book value.** Computer cost 30,000, two years of 10,000 depreciation: accumulated 20,000, book value **10,000**.

## Common Mistakes

- Forgetting to subtract salvage value from cost before dividing.
- Taking a full year's depreciation in the year of a mid-year purchase.
- Using tax rates or tax caps in the accounting books (or the reverse).
- Setting salvage to 1 baht without a reasoned basis.
- Letting double-declining book value drop below salvage.
- Using the 40% first-year allowance or other temporary rates without confirming they still apply.
- Rounding so the total depreciated does not equal the depreciable amount.

## Disclaimer

This skill gives calculation methods and reference figures. It is not tax or legal advice. For tax filings, confirm current Revenue Department rates and rules, and consult an accountant when the amounts are material.
