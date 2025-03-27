
# ระบบจัดการตอน (Story Management System) – Farming War

เอกสารนี้ใช้สำหรับจัดการโครงสร้างตอนทั้งหมดในโปรเจกต์นิยาย *Farming War*  
รวมถึงแนวทางการเขียน การจัดเก็บไฟล์ การใช้ schema และการเชื่อมโยงกับระบบ AI context

---

## 📁 โฟลเดอร์ย่อยของ `story/`

| โฟลเดอร์ | เนื้อหา |
|----------|---------|
| `ep1/`   | ตอนที่ 1–5 (บทนำเรื่อง) |
| `ep2/`   | ตอนที่ 6–10 |
| `ep3/`   | ตอนที่ 11–15 |
| `ep4/`   | ตอนที่ 16–20 |

---

## 📄 ไฟล์ที่เกี่ยวข้อง

| ไฟล์ | คำอธิบาย |
|------|----------|
| `farming-war-main-plot.md` | สรุปโครงเรื่องหลัก |
| `validate-schema-episode-readme.yaml` | Schema สำหรับตรวจ metadata ของตอน |

---

## ✅ มาตรฐานการเขียน README ตอน

ให้แต่ละ EP มีไฟล์ `epX-YY-README.md` โดยมี metadata ดังนี้:

```yaml
---
episode_id: ep4-18
title: ตัวแปรที่ไม่ควรมีอยู่
chapter: บทที่ 4: เงาที่กลับมาพร้อมผู้ตื่นรู้
page: full
type: episode
status: draft
main_characters:
  - klein
  - echo-phantom-prototype
setting: inner-seal-node
related_spells:
  - fragment-echo
  - corrupted-seal-feedback
theme:
  - instability
  - fragment-chaos
  - experimental-magic
created: 2025-03-24
modified: 2025-03-27
author: abckill101
---
```

---

## 🔗 เชื่อมโยงระบบ

- ระบบจะใช้ `structure-index.yaml` สำหรับจัดหมวดตอน
- README แต่ละตอนต้องผ่านการตรวจสอบกับ `validate-schema-episode-readme.yaml`
- สามารถใช้คำสั่ง `@@ep epX-YY` เพื่อเรียกข้อมูลตอนใดก็ได้

---

## 🧠 สำหรับนักเขียน

- สามารถเพิ่มตอนใหม่โดยใช้ `structure-template.md`
- หากไม่แน่ใจให้พิมพ์: **“@@ep create ep4-21”** แล้ว AI จะช่วยร่าง metadata ให้

---

## 📌 หมายเหตุ

- โปรดตรวจสอบว่าไฟล์ README ทุกไฟล์มี metadata block ครบถ้วน
- หากมีหลายเวอร์ชันในตอนเดียว เช่น split 1of5, 2of5 → ใส่ไว้ในโฟลเดอร์ `epX/` และใช้ README ตรงกลางควบคุม

