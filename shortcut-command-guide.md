
<!--
type: shortcut-command-guide
version: 1.0
auto-parsable: true
-->

# คู่มือคำสั่งสั้นระบบ @@ สำหรับโปรเจกต์ Farming War

คำสั่งในรูปแบบ `@@` นี้ถูกออกแบบมาเพื่อให้สามารถเรียกดูข้อมูลเฉพาะเจาะจงจากระบบ worldbuilding, characters, magic, quests และ context ได้อย่างรวดเร็ว  
เหมาะสำหรับนักเขียน นักพัฒนา หรือระบบ AI ที่ต้องการเรียกใช้งานแบบ Zero-Shot

---

## รูปแบบคำสั่ง

```
@@[หมวด] [ชื่อ/รหัสเป้าหมาย]
```

---

## รายการคำสั่งที่รองรับ

### `@@help`
- แสดงคำสั่งทั้งหมดที่สามารถใช้งานได้

### `@@char` หรือ `@@character`
- ใช้เรียกข้อมูลตัวละครจาก `characters-index.yaml`
- ตัวอย่าง:
  - `@@char maria-luna`
  - `@@char kline-fendrix`

### `@@magic`
- ใช้เรียกข้อมูลเวทมนตร์จาก `magic-index.yaml`
- ตัวอย่าง:
  - `@@magic echo-pulse`
  - `@@magic seal-resonance`

### `@@quest`
- ใช้เรียกข้อมูลเควสจาก `quest-index.yaml`
- ตัวอย่าง:
  - `@@quest shadow-patrol`
  - `@@quest blaze-bee-scout`

### `@@item`
- เรียกดูข้อมูลไอเท็ม (สำหรับระบบอนาคต)

### `@@ep`
- เรียก metadata ของตอน เช่น `ep4-16`
- ตัวอย่าง:
  - `@@ep ep3-15`

### `@@world`
- ใช้เรียกข้อมูลด้าน worldbuilding
- ตัวอย่าง:
  - `@@world seal-network`
  - `@@world stone-inscription-plaza`

### `@@context`
- เรียกดูข้อมูล context system
- ตัวอย่าง:
  - `@@context checklist`
  - `@@context missing`

### `@@dev`
- เรียกดูแผนงานที่กำลังพัฒนา หรือเนื้อหาที่อยู่ใน dev/

### `@@story`
- เข้าถึงเนื้อหานิยายจากโฟลเดอร์ `story/`
- ตัวอย่าง:
  - `@@story ep4-18`

---

## หมายเหตุ
- คำสั่งนี้จะถูกเชื่อมกับ `context-ai-index.yaml` โดยตรง
- ใช้งานได้ทันทีในระบบ AI หรือใน prompt ของ ChatGPT
- สามารถต่อยอดเป็น autocomplete หรือ interface อื่น ๆ ได้

หากต้องการเพิ่มคำสั่งใหม่ → อัปเดตที่ `shortcut-command-guide.yaml`
