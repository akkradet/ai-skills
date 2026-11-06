---
name: accounting-purchase-order
description: Use when drafting, reviewing, or approving a Purchase Order (ใบสั่งซื้อ, PO) for goods or services, designing a PO template or numbering scheme, laying out the purchasing flow (PR ใบขอซื้อ → PO → GR ใบรับสินค้า → invoice → payment), deciding whether a PO is legally binding under the Civil and Commercial Code, whether it carries VAT or stamp duty (อากรแสตมป์ for จ้างทำของ), what to record in the books when a PO is issued (nothing until delivery or invoice), handling PO deposits, partial deliveries, price changes, cancellations, or matching a PO against an invoice. Also use when someone asks how a PO differs from a quotation, PR, invoice, or tax invoice, or wants a PO checklist for a small business, even if they only say "PO" or "ใบสั่งซื้อ".
---

# Purchase Order (ใบสั่งซื้อ / PO)

## Overview

A **Purchase Order (ใบสั่งซื้อ, PO)** is the document a buyer issues to a seller to confirm what it wants to buy: the items or services, quantities, agreed prices, delivery date and place, and payment terms. It is usually the buyer's reply to an accepted quotation (ใบเสนอราคา) and the first document that leaves the buyer's company in the purchasing cycle.

Keep three facts in mind, because most questions about POs turn on them:

1. **A PO is a commercial and evidential document, not a tax document.** It does not give the buyer input VAT (ภาษีซื้อ), and it does not replace a tax invoice (ใบกำกับภาษี) or receipt.
2. **Issuing a PO creates no journal entry.** Nothing has been received and nothing is owed yet. The liability arises when goods are delivered or the service is performed and the invoice arrives.
3. **No law requires every business to issue POs.** POs exist for internal control: budget approval, proof of what was agreed, and the basis for matching invoices before payment.

---

## 1. Where the PO sits in the purchasing cycle

```
[Requesting dept]        [Approver]          [Purchasing]           [Supplier]
 PR ใบขอซื้อ  ──────►  approve budget ──►  PO ใบสั่งซื้อ  ───────►  accepts / confirms
 (internal)                                (external, numbered)        │
                                                                       ▼
[Accounting]  ◄── 3-way match ◄── Invoice / Tax invoice ◄── Delivery + GR ใบรับสินค้า
  pay (and withhold tax for services)        (supplier)            (warehouse inspects vs PO)
```

| Step | Document | Issued by | Purpose |
|---|---|---|---|
| 1. State the need | **PR – Purchase Requisition (ใบขอซื้อ)** | Requesting department | Internal request: item, quantity, needed-by date, budget code |
| 2. Approve | Approval on PR (or in system) | Supervisor / owner per authority matrix | Confirms need and budget before any commitment |
| 3. Order | **PO – Purchase Order (ใบสั่งซื้อ)** | Purchasing | External commitment to the supplier |
| 4. Confirm | Signed PO copy / Order confirmation | Supplier | Acceptance – this is when the agreement forms |
| 5. Receive | **GR – Goods Receipt (ใบรับสินค้า)**, or ใบตรวจรับงาน for services | Warehouse / user dept | Records what actually arrived and its condition, checked against the PO |
| 6. Bill | Invoice / Tax invoice (ใบแจ้งหนี้ / ใบกำกับภาษี), Billing note (ใบวางบิล) | Supplier | Creates the payable and, with a valid tax invoice, the input VAT |
| 7. Pay | Payment voucher, WHT certificate (50 ทวิ) for services | Accounting / Finance | Pays only after PO–GR–invoice match |

For 3-way matching tolerances, AP aging, and payment entries, use the `accounting-accounts-payable` skill. For the wider document map (QT → PO → DO → TI → BN → RC), see `accounting-business-accounting-documents`.

---

## 2. What a complete PO contains

The test for a good PO: the supplier can read it once and prepare the goods without phoning back, and accounting can later match it to an invoice line by line.

| Section | Fields | Why it matters |
|---|---|---|
| **Header** | PO number (running, unique), issue date, reference (quotation no. / PR no. / contract no.) | The PO number is the key that links PR, GR, invoice, and payment. A missing number makes matching and audit trails impossible. |
| **Buyer** | Company name, head office/branch (สำนักงานใหญ่/สาขาที่), address, tax ID (เลขประจำตัวผู้เสียภาษี 13 หลัก), contact | The supplier copies these onto the tax invoice. Wrong branch or tax ID here becomes a defective tax invoice later, and input VAT on a defective tax invoice cannot be claimed. |
| **Supplier** | Name, address, tax ID, branch, contact, vendor code | Confirms you are ordering from an approved vendor. |
| **Lines** | Item code, description/spec, quantity, unit, unit price, discount, amount before VAT | Itemize every line. A lump-sum PO cannot be checked against a partial delivery or an invoice. |
| **Totals** | Subtotal, discount, amount before VAT (มูลค่าที่คำนวณภาษี), VAT 7%, grand total (จำนวนเงินทั้งสิ้น) | State clearly whether prices include or exclude VAT. |
| **Terms** | Delivery date, delivery place (branch/warehouse), shipping/Incoterms, payment terms (e.g. Net 30, end of month), payment channel, deposit if any, warranty, penalty for late delivery (ค่าปรับ) | Disputes usually come from terms that were never written: who pays freight, what "end of month" means, late delivery. |
| **Approval** | Prepared by, approved by (per authority limit), dates; supplier acceptance signature and date | Law does not require a signature, but the signatures prove internal approval and supplier acceptance. |

### Sample PO line and totals

| # | Code | Description | Qty | Unit | Unit price | Disc. | Amount |
|---|---|---|---|---|---|---|---|
| 1 | P00005 | โต๊ะทำงาน (office desk) 120×60 cm | 20 | ตัว | 2,000.00 | 0.00 | 40,000.00 |

- Amount before VAT: 40,000.00
- VAT 7%: 2,800.00
- **Grand total: 42,800.00**

Numbering: use one running sequence per company (or per branch) with a prefix and period, e.g. `PO-202606-00001`. Never reuse the number of a cancelled PO. Mark it **CANCELLED** and keep it, so the sequence stays unbroken for audit.

---

## 3. Legal status

- **Contract formation.** Under the Civil and Commercial Code, a contract forms when an offer is met by a matching acceptance. The parties reach agreement when the supplier accepts the PO, by signing it, confirming it in writing or email, or delivering against it. Use the article numbers in `accounting-business-accounting-documents` (ม.354 for offers, ม.366 for agreement on all points). If the supplier changes price, quantity, or date in its confirmation, that is a counter-offer, not an acceptance. Issue a revised PO.
- **Sale of movables of 20,000 baht or more** (ป.พ.พ. ม.456 วรรคสาม): you cannot sue to enforce the sale unless there is written evidence signed by the party to be held liable, a deposit was paid, or there was partial performance. A PO signed by the buyer and an acceptance signed by the supplier give both sides that evidence. Electronic signatures and email confirmations count under the Electronic Transactions Act B.E. 2544.
- **Before acceptance**, the buyer can usually withdraw or amend the PO. **After acceptance**, a cancellation without cause can make the buyer liable for damages, so write the cancellation and change terms into the PO itself.
- If you need a firm opinion on whether a dispute is enforceable, refer the user to a lawyer. This skill is for document practice, not litigation advice.

---

## 4. Tax treatment

### 4.1 VAT
- A PO is **not** a tax invoice. The buyer claims input VAT only from a valid **tax invoice** (Revenue Code ม.82/4, ม.86/4). VAT shown on a PO is just a price quote.
- **Tax point for goods** (ม.78(1)): delivery, transfer of ownership, payment, or issue of a tax invoice, whichever comes first. **Tax point for services** (ม.78/1(1)): payment. A PO alone never triggers a tax point.
- **Deposit or advance payment on a PO:** payment triggers the tax point for the deposited amount. The supplier must issue a tax invoice for the deposit, and the buyer can claim that input VAT. For the deposit mechanics and the final-invoice deduction, use `accounting-deposit-vat`.
- **Import POs:** for goods, VAT is paid to Customs at import, and the import entry (ใบขนสินค้าขาเข้า) plus the Customs receipt is the input VAT document. For services bought from abroad, the buyer self-assesses VAT on ภ.พ.36 when it pays.

### 4.2 Withholding tax
Goods purchases carry no withholding tax. For a services PO, or the service part of a mixed PO (e.g. installation, transport), withhold at payment, not at PO issue. The usual rate is 3% for services and contracting, 1% for transport, and 5% for rent. Split goods and services on separate PO lines so the WHT base is clear. See `tax-withholding-tax-guide`.

### 4.3 Stamp duty (อากรแสตมป์)
- A PO for a straight **purchase of goods (ซื้อขาย)** is not an instrument listed in the stamp duty schedule, so no stamp duty applies.
- A PO for **hire of work (จ้างทำของ, instrument type 4)** is a different case. This covers work defined by a result: custom fabrication, molds or tooling made to your design, construction, repairs, printing, software development. Once the supplier accepts it, the PO is the hire-of-work contract. The rate is **1 baht per 1,000 baht or fraction** of the contract value. The contractor (ผู้รับจ้าง) is liable. Pay by affixing stamps or through e-Stamp; e-Stamp is required for electronic instruments.
- An unstamped instrument cannot be used as evidence in a civil case (Revenue Code ม.118) until it is stamped and the surcharge is paid. This is the main practical reason to care.
- Whether a "made-to-order goods" PO is a sale or hire of work depends on the substance: who supplies the materials and whether the result is built to the buyer's specification. When this is unclear, flag it and suggest confirming with the Revenue Department or a tax adviser rather than asserting an answer.

---

## 5. Accounting entries

| Event | Entry |
|---|---|
| PO issued / accepted | **No journal entry.** Optionally record the commitment off-book (open-PO report or budget encumbrance) so management sees committed spend. |
| Deposit paid on PO (e.g. 30% of 40,000 + VAT) | Dr. Advance to supplier (เงินมัดจำจ่าย/เงินจ่ายล่วงหน้า) 12,000 · Dr. Input VAT (ภาษีซื้อ) 840 · Cr. Bank 12,840 |
| Goods received with tax invoice (credit purchase) | Dr. Inventory / Asset / Expense 40,000 · Dr. Input VAT 2,800 · Cr. Accounts payable (เจ้าหนี้การค้า) 42,800 |
| Goods received, invoice not yet received at period end | Dr. Inventory 40,000 · Cr. Goods received not invoiced / Accrued payable (เจ้าหนี้ค้างรับใบแจ้งหนี้) 40,000. Do not book input VAT until the tax invoice arrives. |
| Deposit applied on final invoice | Dr. Inventory 40,000 · Dr. Input VAT (on balance) 1,960 · Cr. Advance to supplier 12,000 · Cr. Accounts payable 29,960 |

Classify the debit by what was bought, not by the fact that it came through a PO. Fixed assets go to the asset account and the fixed asset register (`accounting-fixed-asset-management`). Stock goes to inventory and the stock card (`accounting-stock-card`).

---

## 6. Common situations

| Situation | What to do |
|---|---|
| **Partial delivery** | Receive a GR per delivery and match each invoice to the GR quantity, not the PO total. Keep the PO open until it is fully received or closed short. |
| **Supplier invoices a different price** | Hold payment. Pay the PO price, or get an approved PO revision. Do not let the invoice silently override the PO. |
| **Extra charges** (freight, packing) **not on the PO** | Treat them as a price variance that needs approval. Next time, write who bears freight on the PO. |
| **Quantity over-delivered** | Accept up to the PO quantity, or return the excess. If you keep it, issue a PO amendment first. |
| **Change after acceptance** | Issue a revision (`PO-202606-00001 Rev.1`) that both sides sign. Keep the original. |
| **Cancellation** | Cancel in writing, get the supplier's acknowledgment, and mark the PO CANCELLED in the register. If a deposit was paid, see `accounting-deposit-vat` for refunds and forfeiture. |
| **Recurring supplies** | Use a **blanket PO** with an agreed price and period, plus call-off releases against it. |
| **Small shop, one supplier, few orders a month** | A full PR/PO process may be overkill. A confirmed quotation or a simple order form with a running number is enough. Introduce POs once you have several buyers, branches, or suppliers. |

---

## 7. Internal control checklist

- [ ] Every purchase above the set threshold has an approved PR/PO **before** ordering. "Retro POs" raised after the invoice defeat the control.
- [ ] An approval matrix sets limits by amount (e.g. department head < 50,000; manager < 500,000; director above).
- [ ] Segregate duties: whoever requests, approves, orders, receives, and pays are not the same person.
- [ ] Order only from vendors in the approved vendor master. Check bank account changes independently.
- [ ] PO prices match the quotation. Typos like 90 instead of 100 are a common source of disputes.
- [ ] Delivery date, place, and payment terms are written on the PO.
- [ ] Check for duplicate POs (same vendor, item, amount) before issuing.
- [ ] Review the open-PO report monthly. Close stale POs.
- [ ] Retain POs as supporting documents: at least **5 years** from the accounting period close (พ.ร.บ.การบัญชี พ.ศ. 2543 ม.14). VAT registrants should also keep them for 5 years under Revenue Code ม.87/3, which an officer can extend to 7. Many firms keep 7–10 years.

---

## 8. Common mistakes

1. **Booking an expense or payable when the PO is issued.** Nothing has been received. Record the purchase at delivery or invoice.
2. **Claiming input VAT from a PO or a deposit request.** Only a tax invoice supports input VAT.
3. **Lump-sum POs.** One line that says "office furniture 42,800" cannot be matched to partial deliveries or itemized invoices.
4. **Wrong buyer tax ID or branch on the PO.** This flows into a defective tax invoice.
5. **No PO number, or reused numbers.** These break the audit trail.
6. **Ignoring stamp duty on hire-of-work POs.** The PO then can't be used as court evidence until it is stamped and the surcharge is paid.
7. **Treating the supplier's modified confirmation as acceptance.** It is a counter-offer. Revise the PO.

---

## How to respond

- **Drafting a PO:** produce a filled template as a markdown table, or as Excel/Google Sheets columns if asked. Include header, buyer/supplier, itemized lines, totals with VAT computed, terms, and signature blocks. Flag any missing information (tax ID, branch, delivery terms) instead of inventing it.
- **Reviewing a PO:** go through Section 2 and Section 7, list each defect with its consequence, and suggest the fix.
- **Accounting or tax questions:** state plainly that issuing a PO alone creates no entry, no VAT, and no WHT, then show the entries at the event that does trigger them.
- Answer in the user's language. Use Thai terms with English in parentheses for document names.
