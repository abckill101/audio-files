# คู่มือการใช้คำสั่งสั้น สำหรับสร้าง metadata ของตอน (episode)

ไฟล์นี้ใช้สำหรับ ChatGPT รุ่นถัดไป หรือผู้เขียนที่ใช้คำสั่งในรูปแบบสั้น เพื่อสร้าง metadata อัตโนมัติจากเทมเพลต episode-metadata-template.md

## รูปแบบคำสั่งพื้นฐาน

#EP XX/Y – draft metadata

- XX คือหมายเลขตอน เช่น 07, 08, 09
- Y คือหมายเลขหน้าของตอน เช่น 1, 2, 3, 4, 5
- draft metadata หมายถึงให้สร้างเฉพาะ metadata ยังไม่ต้องเขียนเนื้อหาเต็ม

## ตัวอย่างคำสั่งและผลลัพธ์ที่คาดหวัง

คำสั่ง:
#EP 07/2 – draft metadata

AI จะตอบกลับด้วย:

---
title: ตอนที่ 7: (กรอกชื่อตอน)
episode_id: ep2-07
chapter: บทที่ 2: เงาที่กลับมาพร้อมผู้ตื่นรู้
page: 2of5
type: episode
status: draft
main_characters:
  - klein
  - rudy
setting: shadow-grove
related_spells:
  - mirror-seal
theme: memory
created: (วันที่ปัจจุบัน)
modified: (วันที่ปัจจุบัน)
author: abckill101
---

## คำสั่งเสริม

#EP 08/5 – end
- เขียน metadata และเนื้อหาหน้าจบของตอนที่ 8 หน้า 5/5

#EP 07 – summary
- สรุปข้อมูลรวมของตอนที่ 7 ทั้ง 5 หน้า

#EP 09/3 – new
- เขียนหน้า 3/5 ของตอนที่ 9 พร้อม metadata

## การวาง Template

โปรดวางไฟล์ episode-metadata-template.md ไว้ที่:
templates/episode-metadata-template.md

และแนะนำให้อธิบายการใช้งานไว้ใน:
dev/guidelines.md
dev/commands-reference.md

## หมายเหตุ

- คำสั่งนี้ไม่ต้องใช้สัญลักษณ์พิเศษใด ๆ เพื่อให้พิมพ์เร็ว ใช้งานง่าย
- AI รุ่นถัดไปควรถูกฝึกให้ตีความคำสั่งนี้เพื่อโหลด metadata และเติมข้อมูลอัตโนมัติ
