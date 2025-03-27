
# คู่มือการพัฒนา: magic-index.yaml

ไฟล์ `magic-index.yaml` ใช้สำหรับจัดเก็บข้อมูลเวทมนตร์ในรูปแบบที่ AI สามารถใช้งานได้อัตโนมัติ  
รองรับการค้นหา ตรวจสอบ และเชื่อมโยงกับระบบอื่นในนิยาย *Farming War*

---

## ✅ metadata ด้านบนไฟล์

```yaml
metadata:
  type: magic-index
  auto-parsable: true
  source-path: worldbuilding/magic/
```

---

## ✅ โครงสร้างแต่ละเวท (ใน `magic:`)

| ฟิลด์ | บังคับ | คำอธิบาย |
|-------|--------|-----------|
| `id` | ✅ | slug ของเวท เช่น `echo-pulse` |
| `name` | ✅ | ชื่อเวท เช่น `Echo Pulse` |
| `file` | ✅ | path ไปยังไฟล์ Markdown |
| `ep` | ✅ | EP ที่เวทปรากฏครั้งแรก |
| `class` | ✅ | ประเภทของเวท เช่น `seal`, `echo` |
| `spell_level` | ✅ | ระดับของเวท เช่น `basic`, `advanced`, `forbidden` |
| `description` | ✅ | คำอธิบายย่อ |
| `element` | ❌ | ธาตุ เช่น `light`, `dark`, `void` |
| `origin` | ❌ | แหล่งกำเนิด เช่น `ancient-seal`, `player` |
| `keywords` | ❌ | tag เช่น `area`, `disrupt` |
| `status` | ❌ | `active`, `experimental`, `disabled` |

---

## ✅ ตัวอย่าง

```yaml
- id: echo-pulse
  name: Echo Pulse
  file: ep3/echo-pulse.md
  ep: 3
  class: echo
  spell_level: advanced
  description: เวทสะท้อนที่แทรกสัญญาณเวทกลับไปยังต้นทาง
  element: void
  origin: seal-network
  keywords: [reflection, disrupt]
  status: active
```

---

## ✅ การเชื่อมโยง

- ใช้ร่วมกับ `magic-template.md`
- ใช้ตรวจด้วย `validate-schema-magic.yaml`
- แนะนำใส่ anchor ใน `magic-README.md`:
  ```markdown
  <!-- magic-index-source: magic-index.yaml -->
  ```

---

## ✅ ตัวอย่างคำสั่งที่ AI จะใช้:

- “เวททั้งหมดใน EP4”
- “เวทที่เป็นคลาส seal”
- “เวทระดับ forbidden”
- “เติม class ให้เวทที่ยังว่าง”

---

## ✅ ตำแหน่งที่ควรวางไฟล์

```
worldbuilding/magic/magic-index.yaml
```

ไฟล์นี้คือหัวใจของระบบเวท ที่เชื่อมโยงทุกองค์ประกอบเข้าด้วยกัน ✨
