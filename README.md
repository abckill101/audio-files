# 📚 Farming War – GitHub Worldbuilding Project

> โปรเจกต์นี้เป็นโครงสร้างนิยายแฟนตาซี “Farming War”  
> ที่เน้นการล่ามอนสเตอร์, คราฟต์ของ, วางกลยุทธ์ และสร้างโลกแบบมีระบบ  
> จัดวางข้อมูลทั้งหมดด้วยโฟลเดอร์และ Markdown เพื่อรองรับนิยายระดับหลายร้อยตอน

---

## 🗂 โครงสร้างหลักของโปรเจกต์

### 📁 `story/`
- เก็บเนื้อหานิยายแต่ละตอน
- แบ่งตาม Episode เช่น `ep1/`, `ep2/`
- ตัวอย่าง: `ep01-01.md`, `ep01-02-1of5.md`

### 📁 `characters/`
- ข้อมูลตัวละครทั้งหมดในเรื่อง
- ใช้โครงสร้าง `WSP-Character-Intro`

### 📁 `monsters/`
- รายชื่อมอนสเตอร์ทุกระดับ
- แบ่งตามโซน เช่น `forest/`, `ep1/`, `shadowrift/`

### 📁 `worldbuilding/`
- ศูนย์รวมข้อมูลโลก “ออร์เทีย (Orthia)”
- แยกเป็นหมวดหมู่:
  - `locations/` – เมือง, ดันเจี้ยน
  - `factions/` – องค์กร, สมาคม, กลุ่มอำนาจ
  - `magic-system/` – ระบบเวท
  - `economy-and-politics/` – เศรษฐกิจ, การเมือง
  - `cultures/` – ภาษา, ประเพณี
  - `maps/` – แผนที่ / โครงสร้างโลก

### 📁 `quests/`
- ระบบภารกิจและเควส แยกตามบท
- ตัวอย่าง: `quests/ep1/`

### 📁 `items/` *(ถ้ามี)*
- ข้อมูลอาวุธ, ชุดเกราะ, วัตถุดิบ, ไอเท็มหายาก
- ระดับไอเท็ม: Common, Rare, Epic, Legendary

### 📁 `teams/`
- ข้อมูลทีม Silent Fortune และพันธมิตร

---

## 🧭 วิธีใช้งานโปรเจกต์นี้

- สามารถเปิดไฟล์ `.md` ใน GitHub หรือ Obsidian
- ใช้ README ของแต่ละโฟลเดอร์เป็นเมนูแนะนำ
- รองรับการเชื่อมกับ AI / ChatGPT เพื่อช่วยเขียน, ขยาย หรือวิเคราะห์เนื้อหา

---

## ✨ เป้าหมายระยะยาว

- นิยาย 500 ตอน แบ่งเป็น 100 บท
- ขยายระบบ worldbuilding ครบทุกด้าน
- วางรากฐานสำหรับเกม, Webtoon หรือ Visual Novel

> สร้างโดย abckill101 ✍  
> ระบบจัดการโดย GitHub + Markdown + ChatGPT 🧠
