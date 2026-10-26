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

```text
> คำนวณค่าเสื่อมราคาคอมพิวเตอร์โน้ตบุ๊กราคา 30,000 บาท อายุการใช้งาน 3 ปี ซื้อต้นเดือนเมษายนให้หน่อย
```

```text
> บริษัทซื้อรถยนต์นั่งราคา 1,500,000 บาท ช่วยเปรียบเทียบการลงบัญชี TAS 16 กับการหักค่าเสื่อมทางภาษีสรรพากรให้หน่อย
```

```text
> ช่วยทำตารางค่าเสื่อมราคาแบบยอดลดลงทวีคูณ (Double-declining) เครื่องจักร 100,000 บาท อายุ 5 ปี
```

---

## 📁 โครงสร้างโฟลเดอร์ (Repository Structure)

```text
ai-skills/
├── .gitignore
├── LICENSE
├── README.md
└── accounting-cal-asset-depreciation/
    └── SKILL.md                          # รายละเอียดทักษะ สูตร และเกณฑ์การคำนวณ
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
