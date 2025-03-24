# factions/ - ข้อมูลองค์กรในจักรวาล

โฟลเดอร์นี้ใช้สำหรับบันทึกข้อมูลของ “องค์กร” หรือ “ฝ่าย” ในโลกของ *Farming War*

## วิธีใช้งาน

- แต่ละองค์กรให้สร้างเป็นไฟล์ `.md` 1 ไฟล์
- ควรตั้งชื่อไฟล์ด้วย format: `ชื่อองค์กรในภาษาอังกฤษ แบบ kebab-case.md`
  - เช่น: `arcane-order.md`, `rogue-scholars.md`
- ทุกไฟล์ควรมี Metadata เช่น:

```yaml
---
title: ชื่อองค์กร (ไทย และ อังกฤษ)
faction_id: ชื่อย่อ เช่น arcane-order
type: faction
status: active | inactive | unknown
leaders:
  - ชื่อตัวละคร (เช่น zargos-werth)
tags:
  - magic-faction
  - political-group
related_episodes:
  - ep2-09
  - ep2-10
created: YYYY-MM-DD
modified: YYYY-MM-DD
author: abckill101
---
```

## ความสำคัญ

องค์กรต่าง ๆ มีผลต่อโครงสร้างพลัง การเมือง และเวทต้องห้ามในเรื่อง  
การจัดแยกไว้ที่นี่ช่วยให้สามารถเชื่อมโยงกับตัวละคร, สถานที่, เวทมนตร์ และเนื้อเรื่องหลักได้ง่าย

## ตัวอย่างที่มีอยู่

- [Arcane Order](arcane-order.md)  
  สมาคมเวทกลาง ผู้ควบคุมกฎเวทและข้อมูลเวทต้องห้าม
