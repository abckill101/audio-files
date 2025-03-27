---

<!--
type: magic-index
structure: grouped-by-episode-class-and-usage
auto-parsable: true
source-path: worldbuilding/magic/
-->

---
# สารบัญเวทมนตร์ (Magic Index) – Farming War

เอกสารนี้รวบรวมเวทมนตร์ทั้งหมดที่ปรากฏในนิยาย *Farming War* จัดเรียงแบบ 3 ชั้น เพื่อให้ AI และนักเขียนเข้าถึงข้อมูลได้รวดเร็วและตรงประเด็น

## คู่มือการพัฒนาเวทมนตร์ (Magic Development Guide)

เอกสารนี้ใช้กำหนดมาตรฐานและแนวทางการจัดเก็บเวทมนตร์ทั้งหมดในโปรเจกต์ *Farming War* เพื่อให้สามารถใช้งานและอ้างอิงได้อย่างเป็นระบบ ทั้งโดยมนุษย์และ AI รุ่นถัดไป

---

### 1. โครงสร้างโฟลเดอร์

- เวทมนตร์ทั้งหมดเก็บไว้ใน `magic/`
- แบ่งตามตอนที่ปรากฏ โดยใช้โฟลเดอร์ย่อย:
  - `magic/ep2/`
  - `magic/ep3/`
  - `magic/ep4/`  
- ทุกไฟล์ควรมีนามสกุล `.md` และใช้ **ตัวพิมพ์เล็กทั้งหมด**

---

### 2. การตั้งชื่อไฟล์เวท

ใช้รูปแบบ:


ตัวอย่าง:
- `mirror-seal-ep2.md`
- `echo-pulse-ep3.md`
- `inheritance-link-ep4.md`

---

### 3. โครงสร้างเนื้อหาในไฟล์เวท

ควรประกอบด้วยหัวข้อหลักดังนี้:

```markdown
# ชื่อเวท (ภาษาไทย + ภาษาอังกฤษ)

**ระดับเวท:** (พื้นฐาน / กลาง / สูง / โบราณ / ต้องปลดล็อก)  
**คลาสเวท:** (เวทสะท้อน / เวทผนึก / ความทรงจำ / ก่อกวน ฯลฯ)  
**ประเภทการใช้งาน:** (โจมตี / ป้องกัน / สนับสนุน / ฟื้นฟู / ฟังก์ชันพิเศษ)

## คำอธิบายโดยรวม
(อธิบายว่าเวทนี้คืออะไร มีที่มา/บทบาทอย่างไรในเรื่อง)

## วิธีใช้งาน
(วิธีร่าย / เงื่อนไข / ข้อจำกัด)

## ผลกระทบ
(ผลลัพธ์เมื่อสำเร็จ เช่น ความเสียหาย การบัฟ การเดบัฟ ฯลฯ)

## ความสัมพันธ์กับระบบอื่น
(เกี่ยวข้องกับ Seal Network, Echo, หรือพลังความทรงจำหรือไม่)

## ปรากฏครั้งแรกใน
(ระบุตอน เช่น EP3-14)

## หมายเหตุเพิ่มเติม
(ใช้เฉพาะบางสถานการณ์? มีผลข้างเคียง? ใช้เฉพาะตัวละคร?)

การ commit หรือบันทึกการเปลี่ยนแปลง

เพิ่มเวทใหม่: seal-resonance-ep3.md
อัปเดตหมวดคลาสเวท: memory-disruption-field

หมายเหตุ
ทุกเวทควรถูกอ้างอิงใน magic-README.md เสมอ เพื่อให้ระบบสารบัญของ AI สมบูรณ์

หากเวทมีการเปลี่ยนแปลงผลลัพธ์หรือชื่อ ควรเขียนเวอร์ชันใหม่แล้ว deprecate เวอร์ชันเก่าอย่างชัดเจน


---

คู่มือนี้จะช่วยให้ทั้งคุณและ AI รุ่นถัดไปสามารถ “ขยายระบบเวท” ได้เรื่อย ๆ แบบไม่สับสนเลยครับ!  
หากอยากได้เวอร์ชัน `.md` พร้อมจัดโครงสร้างจริง แจ้งได้เลย!

---

## I. แยกตามตอน (Episode)

### EP2
- [echo-pulse-ep2.md](ep2/echo-pulse-ep2.md)
- [feral-reflection-ep2.md](ep2/feral-reflection-ep2.md)
- [mirror-seal-ep2.md](ep2/mirror-seal-ep2.md)

### EP3
- [echo-inheritance.md](ep3/echo-inheritance.md)
- [echo-pulse-ep3.md](ep3/echo-pulse-ep3.md)
- [fragment-echo-ep3.md](ep3/fragment-echo-ep3.md)
- [memory-chain-ep3.md](ep3/memory-chain-ep3.md)
- [mirror-seal-ep3.md](ep3/mirror-seal-ep3.md)
- [new-seal-theory-ep3.md](ep3/new-seal-theory-ep3.md)
- [seal-resonance-ep3.md](ep3/seal-resonance-ep3.md)
- [seal-resonance-fragment.md](ep3/seal-resonance-fragment.md)
- [unknown-reaction-ep3.md](ep3/unknown-reaction-ep3.md)

### EP4
- [echo-fusion.md](ep4/echo-fusion.md)
- [inheritance-link.md](ep4/inheritance-link.md)
- [memory-disruption-field.md](ep4/memory-disruption-field.md)

---

## II. แยกตามคลาสของเวท (Class of Magic)

### A. เวทสะท้อน (Echo-Type)
- echo-pulse-ep2, echo-pulse-ep3, echo-inheritance, fragment-echo-ep3, echo-fusion

### B. เวทผนึก (Seal-Type)
- mirror-seal-ep2, mirror-seal-ep3, new-seal-theory, seal-resonance, seal-resonance-fragment

### C. เวทความทรงจำ / จิต (Memory & Mind)
- memory-chain, inheritance-link, memory-disruption-field

### D. เวทก่อกวน / ปฏิกิริยา
- feral-reflection, unknown-reaction

---

## III. แยกตามรูปแบบการใช้งาน (Usage Type)

### 1. เวทโจมตี (Offensive Magic)
- [feral-reflection-ep2.md](ep2/feral-reflection-ep2.md) – ปลุกพลังจากเงาธรรมชาติ
- [echo-pulse-ep3.md](ep3/echo-pulse-ep3.md) – ความถี่โจมตีจากเสียงสะท้อน

### 2. เวทป้องกัน (Defensive Magic)
- [mirror-seal-ep2.md](ep2/mirror-seal-ep2.md)
- [mirror-seal-ep3.md](ep3/mirror-seal-ep3.md)
- [seal-resonance-ep3.md](ep3/seal-resonance-ep3.md)

### 3. เวทสนับสนุน (Supportive Magic)
- [memory-chain-ep3.md](ep3/memory-chain-ep3.md) – เชื่อมความทรงจำในทีม
- [inheritance-link.md](ep4/inheritance-link.md) – สานพลังผู้สืบทอด
- [echo-inheritance.md](ep3/echo-inheritance.md) – สะท้อนความสามารถข้ามรุ่น

### 4. เวทฟื้นฟู / บัฟ (Recovery / Buff)
- [echo-fusion.md](ep4/echo-fusion.md) – รวมพลังเสียงเพื่อฟื้นคืนกำลัง

### 5. เวทก่อกวน / ขัดขวาง (Disruption / Debuff)
- [memory-disruption-field.md](ep4/memory-disruption-field.md)
- [unknown-reaction-ep3.md](ep3/unknown-reaction-ep3.md)

### 6. เวทฟังก์ชันพิเศษ (Utility / Unique Function)
- [new-seal-theory-ep3.md](ep3/new-seal-theory-ep3.md)
- [seal-resonance-fragment.md](ep3/seal-resonance-fragment.md)
- [fragment-echo-ep3.md](ep3/fragment-echo-ep3.md)

---

## หมายเหตุ
- เวทหลายชนิดอาจอยู่ได้มากกว่า 1 ประเภท เช่น สนับสนุนและฟังก์ชันพิเศษ
- การระบุ usage ช่วยให้ AI สร้าง encounter หรือระบบต่อสู้ได้ตรงประเภทมากขึ้น
- โปรดเพิ่มลิงก์ทั้งใน EP, Class และ Usage ทุกครั้งเมื่อมีเวทใหม่
