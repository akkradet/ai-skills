# ai-skills

> **My Claude Code skills collection** — รวมคอลเลกชัน Custom Skills สำหรับ **Claude Code** และ AI Coding Assistants ใช้งานง่าย ติดตั้งได้ทันที

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-6366f1.svg)](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code)

---

## 📌 สารบัญ (Table of Contents)
- [เกี่ยวกับ Repository](#-เกี่ยวกับ-repository)
- [รายการ Skills ที่มีในคลัง (Available Skills)](#-รายการ-skills-ที่มีในคลัง-available-skills)
- [วิธีการติดตั้ง (Installation)](#-วิธีการติดตั้ง-installation)
  - [วิธีที่ 1: ติดตั้งแบบ Global (แนะนำ - ใช้ได้ทุกโปรเจกต์)](#วิธีที่-1-ติดตั้งแบบ-global-แนะนำ---ใช้ได้ทุกโปรเจกต์)
  - [วิธีที่ 2: ติดตั้งเฉพาะโปรเจกต์ (Project Level)](#วิธีที่-2-ติดตั้งเฉพาะโปรเจกต์-project-level)
  - [วิธีที่ 3: ก๊อปปี้เฉพาะบาง Skill ที่ต้องการ](#วิธีที่-3-ก๊อปปี้เฉพาะบาง-skill-ที่ต้องการ)
- [วิธีทดสอบการใช้งาน (Usage)](#-วิธีทดสอบการใช้งาน-usage)
- [โครงสร้างโฟลเดอร์ (Repository Structure)](#-โครงสร้างโฟลเดอร์-repository-structure)
- [การเพิ่ม Skill ใหม่ (How to Add New Skill)](#-การเพิ่ม-skill-ใหม่-how-to-add-new-skill)
- [License](#license)

---

## 📖 เกี่ยวกับ Repository

Repository นี้รวบรวม **Custom Skills** สำหรับ AI Coding Assistant โดยเฉพาะ **Claude Code** เพื่อช่วยเพิ่มความสามารถเฉพาะทางให้กับ AI เช่น การคำนวณทางบัญชีและภาษี, การจัดการงานเฉพาะทาง และ Workflow อัตโนมัติต่างๆ

แต่ละ Skill จะบรรจุอยู่ในโฟลเดอร์ของตัวเอง พร้อมไฟล์ `SKILL.md` ที่มีคำแนะนำ กฎเกณฑ์ ตารางอ้างอิง และตัวอย่างการคำนวณที่ชัดเจน

---

## 🛠️ รายการ Skills ที่มีในคลัง (Available Skills)

| Skill Name | คำอธิบายสั้นๆ | ความสามารถหลัก |
|---|---|---|
| [`accounting-cal-asset-depreciation`](accounting-cal-asset-depreciation/) | คำนวณค่าเสื่อมราคาสินทรัพย์ตามมาตรฐานบัญชีและภาษีไทย | • รองรับ 4 วิธีหลัก: เส้นตรง (Straight-line), ยอดลดลงทวีคูณ (Double-declining), ผลรวมจำนวนปี (Sum-of-years-digits), ตามหน่วยผลิต (Units-of-production)<br>• รองรับการซื้อสินทรัพย์ระหว่างปี (Prorated)<br>• เทียบค่าเสื่อมราคาทางบัญชี (TAS 16) vs ทางภาษีสรรพากร (เพดานราคารถยนต์นั่ง 1 ล้านบาท, อัตราสูงสุดตามกฎหมาย) |
| [`accounting-deposit-vat`](accounting-deposit-vat/) | บันทึกบัญชีเงินมัดจำ เงินประกัน และภาษีมูลค่าเพิ่ม | • จุดรับรู้ภาษีมูลค่าเพิ่ม (Tax Point) ตามมาตรา 78/78/1 และการออกใบกำกับภาษีทันทีที่รับเงินมัดจำ<br>• การหักภาษี ณ ที่จ่าย (WHT) สำหรับมัดจำบริการ vs มัดจำสินค้า<br>• บันทึกบัญชีฝั่งผู้รับ (หนี้สิน) และฝั่งผู้จ่าย (สินทรัพย์) พร้อมการออกบิลหักลบมัดจำตอนส่งมอบงานเพื่อป้องกันคิด VAT ซ้ำซ้อน<br>• ข้อยกเว้นเงินประกันการเช่า/ประกันความเสียหายตามคำสั่ง ป.73/2541 และการบันทึกบัญชีกรณีริบมัดจำ |
| [`accounting-stock-card`](accounting-stock-card/) | จัดทำและตรวจสอบบัตรคุมสินค้า (Stock Card) | • คุมสต๊อกสินค้าเข้า-ออก-คงเหลือตามลำดับเอกสารและหน่วยนับเดียว<br>• คำนวณต้นทุนขายและสินค้าคงเหลือแบบ FIFO, ถัวเฉลี่ยถ่วงน้ำหนัก (Moving Average), และเฉพาะเจาะจง<br>• จัดการผลต่างการตรวจนับสต๊อก (ของขาด/เกิน) และจุดสั่งซื้อซ้ำ (Reorder Point) |
| [`accounting-vat-income-tax-reconciliation`](accounting-vat-income-tax-reconciliation/) | กระทบยอด ภ.พ.30 กับรายได้ในงบการเงิน และ ภ.ง.ด.50 | • กระทบยอดฐานภาษีขาย 12 เดือน กับรายได้ในงบกำไรขาดทุน<br>• สูตรคำนวณภาษีขายรวม VAT ด้วย $7/107$ และการจัดการบิลเงินสด<br>• หาสาเหตุผลต่าง: ดอกเบี้ยรับ, กำไรอัตราแลกเปลี่ยน, ใบลดหนี้ข้ามงวด, ยอดขายอัตรา 0% / ยกเว้นภาษี<br>• แนวทางปรับปรุงรายการบัญชีและการยื่น ภ.พ.30 เพิ่มเติมพร้อมเบี้ยปรับ/เงินเพิ่ม |

---

## 🚀 วิธีการติดตั้ง (Installation)

เลือกวิธีติดตั้งที่สะดวกได้ตามต้องการ:

### วิธีที่ 1: ติดตั้งแบบ Global (แนะนำ - ใช้ได้ทุกโปรเจกต์)

โคลน Repository นี้ไปไว้ที่โฟลเดอร์ Skills กลางของ Claude Code เพื่อให้เรียกใช้ได้ตลอดเวลาในทุก Workspace:

#### 🪟 Windows (เปิด PowerShell):
```powershell
# สร้างโฟลเดอร์ .claude/skills หากยังไม่มี
New-Item -ItemType Directory -Force -Path "$HOME\.claude\skills"

# โคลน repository ลงในโฟลเดอร์ skills
git clone https://github.com/akkradet/ai-skills.git "$HOME\.claude\skills\ai-skills"
```

#### 🍎 macOS / 🐧 Linux (Terminal):
```bash
# สร้างโฟลเดอร์ .claude/skills หากยังไม่มี
mkdir -p ~/.claude/skills

# โคลน repository ลงในโฟลเดอร์ skills
git clone https://github.com/akkradet/ai-skills.git ~/.claude/skills/ai-skills
```

---

### วิธีที่ 2: ติดตั้งเฉพาะโปรเจกต์ (Project Level)

หากต้องการให้ Skills ใช้งานได้เฉพาะในโปรเจกต์ใดโปรเจกต์หนึ่ง:

```bash
# นำทางไปยังโฟลเดอร์โปรเจกต์ของคุณ
cd /path/to/your-project

# ดึง skills เข้ามาไว้ในโฟลเดอร์ .claude/skills
git clone https://github.com/akkradet/ai-skills.git .claude/skills/ai-skills
```

---

### วิธีที่ 3: ก๊อปปี้เฉพาะบาง Skill ที่ต้องการ

หากต้องการหยิบไปใช้เพียงโฟลเดอร์เดียว เช่น `accounting-cal-asset-depreciation`:

1. ดาวน์โหลดหรือคัดลอกโฟลเดอร์ `accounting-cal-asset-depreciation`
2. นำไปวางใน:
   - **Global:** `~/.claude/skills/accounting-cal-asset-depreciation`
   - **หรือ Local Project:** `<โฟลเดอร์โปรเจกต์>/.claude/skills/accounting-cal-asset-depreciation`

---

## 💬 วิธีทดสอบการใช้งาน (Usage)

เมื่อติดตั้งเสร็จแล้ว สามารถเปิดใช้งาน **Claude Code** และพิมพ์สอบถามได้ทันที Claude จะเรียกใช้งาน Skill ที่เกี่ยวข้องโดยอัตโนมัติ เช่น:

**ตัวอย่างคำถามเกี่ยวกับค่าเสื่อมราคา:**
```text
> คำนวณค่าเสื่อมราคาคอมพิวเตอร์โน้ตบุ๊กราคา 30,000 บาท อายุการใช้งาน 3 ปี ซื้อต้นเดือนเมษายนให้หน่อย
```
```text
> บริษัทซื้อรถยนต์นั่งราคา 1,500,000 บาท ช่วยเปรียบเทียบการลงบัญชี TAS 16 กับการหักค่าเสื่อมทางภาษีสรรพากรให้หน่อย
```

**ตัวอย่างคำถามเกี่ยวกับกระทบยอด ภ.พ.30 / ภาษี:**
```text
> ช่วยทำกระดาษทำการกระทบยอด ภ.พ.30 12 เดือนกับงบกำไรขาดทุน รายได้รวม 16,988,000 บาท มีดอกเบี้ยรับและกำไรจากอัตราแลกเปลี่ยน
```
```text
> ยอดขายรวม VAT ได้รับมา 12,840,000 บาท ต้องถอดภาษีขายด้วยสูตรไหน และบันทึกบัญชีอย่างไร
```

**ตัวอย่างคำถามเกี่ยวกับเงินมัดจำ เงินประกัน และภาษีมูลค่าเพิ่ม:**
```text
> รับเงินมัดจำค่าจ้างทำของ 30% ต้องออกใบกำกับภาษีทันทีไหม หัก ณ ที่จ่ายเท่าไร และบันทึกบัญชีอย่างไร
```
```text
> เรียกเก็บเงินประกันสัญญาเช่าสำนักงาน 2 เดือน ต้องคิด VAT 7% ไหม และถ้าลูกค้ายกเลิกสัญญาแล้วริบมัดจำต้องเสียภาษีอย่างไร
```

**ตัวอย่างคำถามเกี่ยวกับบัตรคุมสินค้า (Stock Card):**
```text
> ช่วยทำตาราง Stock Card สินค้าราคาปรับขึ้น เปรียบเทียบต้นทุนขายและสินค้าคงเหลือปลายงวดระหว่างวิธี FIFO กับถัวเฉลี่ยเคลื่อนที่
```
```text
> สิ้นเดือนตรวจนับสต๊อกแล้วพบสินค้าขาดหายไป 2 ชิ้น ต้องลงบัตรคุมสินค้าอย่างไร และต้องเสียภาษีขายตาม ม.77/1(8)(จ) หรือไม่
```

---

## 📁 โครงสร้างโฟลเดอร์ (Repository Structure)

```text
ai-skills/
├── .gitignore
├── LICENSE
├── README.md
├── accounting-cal-asset-depreciation/
│   └── SKILL.md                          # รายละเอียดการคำนวณค่าเสื่อมราคาสินทรัพย์
├── accounting-deposit-vat/
│   └── SKILL.md                          # รายละเอียดการบันทึกบัญชีเงินมัดจำ เงินประกัน และภาษีมูลค่าเพิ่ม
├── accounting-stock-card/
│   └── SKILL.md                          # รายละเอียดการจัดทำบัตรคุมสินค้า (Stock Card)
└── accounting-vat-income-tax-reconciliation/
    └── SKILL.md                          # รายละเอียดการกระทบยอด ภ.พ.30 กับบัญชีและภาษีเงินได้
```

---

## ➕ การเพิ่ม Skill ใหม่ (How to Add New Skill)

หากต้องการสร้างหรือเพิ่ม Skill ใหม่ ให้ทำตามโครงสร้างมาตรฐานดังนี้:

1. สร้างโฟลเดอร์ใหม่ตามชื่อ Skill เช่น `my-new-skill/`
2. สร้างไฟล์ `SKILL.md` ภายในโฟลเดอร์ โดยมี Frontmatter ด้านบนสุด:

```markdown
---
name: my-new-skill
description: อธิบายว่า Skill นี้ใช้ทำอะไร และควรเรียกใช้เมื่อใด
---

# My New Skill Title

## Overview
คำอธิบายภาพรวมและบริบท

## Instructions & Rules
กฎเกณฑ์และขั้นตอนการทำงาน
```

3. Commit และ Push ขึ้น Repository ได้ทันที!

---

## 📄 License

แจกจ่ายภายใต้ [MIT License](LICENSE) สามารถนำไปใช้งาน ปรับแต่ง และพัฒนาต่อยอดได้อย่างอิสระ
