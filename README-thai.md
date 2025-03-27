
<!--
context-index: context-ai-index.yaml
template-index: templates/template-index.yaml
validate-schemas: schemas/
auto-parsable: true
project-type: worldbuilding+novel+ai
version: 1.0
-->

# Farming War – ภาพรวมโปรเจกต์

โครงการนี้คือระบบจัดเก็บโลกนิยาย **Farming War** อย่างเป็นระบบ  
รองรับการใช้งานร่วมกับ AI สำหรับช่วยเขียนนิยาย ตรวจสอบโครงเรื่อง และสร้างเนื้อหาโดยอัตโนมัติ

---

## 🗂 โครงสร้างโปรเจกต์หลัก

- `story/` – เนื้อหาตอนหลัก แบ่งตามบท (EP)
- `characters/` – ข้อมูลตัวละคร แบ่งตามกลุ่ม (ทีม, NPC, ศัตรู, เวอร์ชันพิเศษ)
- `magic/` – ระบบเวทมนตร์ แยกตาม EP และคลาสของเวท
- `quests/` – เควส ภารกิจย่อยต่าง ๆ พร้อมจัดอันดับ
- `worldbuilding/` – ข้อมูลฉาก, เผ่า, เศรษฐกิจ, ระบบเวท
- `monsters/` – มอนสเตอร์ แยกตาม Rank
- `templates/` – แม่แบบการเขียน (ตัวละคร, เควส, เวท ฯลฯ)
- `schemas/` – ไฟล์ตรวจโครงสร้าง (schema) สำหรับแต่ละหมวด
- `dev/` – แผนการพัฒนา และเอกสารเบื้องหลัง
- `context-ai-index.yaml` – ไฟล์กลางเชื่อมโยงทุกระบบ
- `context-ai-checklist.yaml` – เช็คลิสต์ตรวจความพร้อมระบบ AI

---

## ✅ การใช้งานร่วมกับ AI

ภายในโฟลเดอร์นี้ได้จัดระบบไว้เพื่อให้ AI ทำงานได้อย่างแม่นยำ เช่น

- ไฟล์ README พร้อม metadata block
- มี index ไฟล์แยกชัดเจน: magic, characters, quests
- เชื่อมโยงกับ template และ schema
- โครงสร้างไฟล์ predictable และมี anchor
- AI สามารถสร้าง ตรวจ และอ้างอิงข้อมูลได้โดยอัตโนมัติ

AI สามารถเริ่มทำงานจาก `context-ai-index.yaml` ได้ทันที

---

## 🔄 วิธีอัปเดตระบบ

1. เพิ่มเนื้อหาใหม่ตาม template ที่เกี่ยวข้อง (ใน `templates/`)
2. เพิ่มใน index ที่เกี่ยวข้อง เช่น `characters-index.yaml`
3. ใส่ metadata block และ anchor ใน README ทุกไฟล์
4. ตรวจความถูกต้องด้วย schema ที่เกี่ยวข้อง (ใน `schemas/`)

---

## 🔗 ไฟล์สำคัญในระบบ

- [`context-ai-index.yaml`](context-ai-index.yaml)
- [`context-ai-checklist.yaml`](context-ai-checklist.yaml)
- [`characters-index.yaml`](characters-index.yaml)
- [`magic-index.yaml`](magic-index.yaml)
- [`quest-index.yaml`](quest-index.yaml)
- [`validate-schema-character.yaml`](schemas/validate-schema-character.yaml)
- [`validate-schema-magic.yaml`](schemas/validate-schema-magic.yaml)
- [`validate-schema-quest.yaml`](schemas/validate-schema-quest.yaml)

---

เอกสารนี้พัฒนาอย่างต่อเนื่องเพื่อรองรับระบบ worldbuilding ที่ใช้ AI ขับเคลื่อนอย่างเต็มรูปแบบ
