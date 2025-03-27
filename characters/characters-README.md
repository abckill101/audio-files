---

<!--
type: character-index
structure: grouped-by-role-and-episode
auto-parsable: true
source-path: characters/
-->

---



# สารบัญตัวละคร (Characters Index) – Farming War

เอกสารนี้รวบรวมตัวละครทั้งหมดในนิยาย *Farming War* แบ่งตามกลุ่มบทบาท ได้แก่:  
- ทีมหลัก (Silent Fortune)  
- ตัวละครจากโลกจริง (Player)  
- ตัวละครสำคัญของเรื่อง (NPC)  
- ฝ่ายศัตรู (Enemy)  
- เวอร์ชันพิเศษตามตอน (Story-Based)

## คู่มือการพัฒนาระบบตัวละคร (Character System Guide)

เอกสารนี้ใช้กำหนดมาตรฐานในการจัดเก็บข้อมูลตัวละครทั้งหมดในโปรเจกต์ *Farming War* เพื่อให้สามารถสั่งงานและใช้งานได้โดยอัตโนมัติผ่านระบบ AI ทั้งในปัจจุบันและรุ่นถัดไป

---

### 1. โครงสร้างไฟล์ตัวละคร

- เก็บไว้ภายใต้โฟลเดอร์ `characters/`
- แบ่งตามบทบาทหลัก ได้แก่:
  - `silent-fortune/` → สมาชิกทีมหลักของไคลน์
  - `npc/` → ตัวละครโลก Orthia ที่ไม่ใช่ผู้เล่น
  - `enemy/` → ศัตรู, บอส, ฝ่ายตรงข้าม
  - `player/` → ตัวละครจากโลกจริง (ต่างโลก)
  - `story/epX/` → เวอร์ชันพิเศษตามตอน เช่น alt, transformed, hidden

---

### 2. การตั้งชื่อไฟล์ตัวละคร

ใช้รูปแบบ:

ตัวอย่าง:
- `serena-whiteford.md`
- `kanokwan-sarisa.md`
- `maria-luna-alt.md`
- `kline-fendrix-ep3.md`

---

### 3. โครงสร้างภายในไฟล์ตัวละคร

ใช้มาตรฐาน `WSP-Character-Intro` เช่น:

```markdown
# ชื่อเต็ม: (ไทย + อังกฤษ)

## อายุ:
## รูปร่างหน้าตา:
## บุคลิกและนิสัย:
## บทบาท:
## หมายเหตุ:

สามารถขยายหัวข้อ เช่น ประวัติ, ความสามารถเฉพาะ, ความสัมพันธ์, พัฒนาการ

การอ้างอิงและอัปเดตใน characters-README.md
เมื่อมีตัวละครใหม่:

ใส่ไฟล์ .md ในโฟลเดอร์ที่ถูกต้อง

เพิ่มลิงก์ไฟล์ไว้ใน characters-README.md ตามหมวดที่ถูกต้อง

ถ้ามีเวอร์ชัน EP หรือ alt → เพิ่มไว้ในหมวด “Story-Based” พร้อมระบุ EP

ให้ commit ด้วยข้อความเช่น:

เพิ่มตัวละครใหม่: seril-wenston.md ใน silent-fortune

การทำให้ AI เข้าถึงได้อัตโนมัติ
characters-README.md ควรมี metadata block ด้านบน:

<!--
type: character-index
structure: grouped-by-role-and-episode
auto-parsable: true
source-path: characters/
-->

คำแนะนำเพิ่มเติม
ตัวละครที่มีหลายเวอร์ชัน (alt, ep) ให้แยกไฟล์ ไม่เขียนรวม

ควรจัดลิงก์เรียงตามตัวอักษรภายในแต่ละหมวดเพื่อการค้นหาง่าย

หากตัวละครมีบทในหลาย EP ให้เพิ่มไฟล์เวอร์ชัน EP ใหม่ หรืออัปเดตหมายเหตุอย่างชัดเจน

ประโยชน์ต่อระบบ AI
ระบบสามารถ:

สร้างความสัมพันธ์ระหว่างตัวละคร

แนะนำฉาก/เนื้อเรื่องตามบทบาท

วิเคราะห์พัฒนาการข้าม EP

ค้นหาเวอร์ชันเฉพาะได้ทันที (เช่น “Maria Luna เวอร์ชัน alt”)

ระบบสามารถเชื่อมโยงกับเวทมนตร์ เควส และ Worldbuilding อัตโนมัติ
หากแต่ละไฟล์มี keyword และหัวข้อที่สม่ำเสมอ

---

หากต้องการให้ผมช่วย generate เทมเพลตไฟล์ `.md` สำหรับตัวละครใหม่ พร้อมหัวข้อครบถ้วนในโครงสร้างนี้ แจ้งได้เลยครับ!

---

## 1. Silent Fortune (ทีมหลัก)
- [aila-vendarin.md](silent-fortune/aila-vendarin.md)
- [arvel-feldman.md](silent-fortune/arvel-feldman.md)
- [aviana-orelia.md](silent-fortune/aviana-orelia.md)
- [beren-stonecook.md](silent-fortune/beren-stonecook.md)
- [finn-wildcard.md](silent-fortune/finn-wildcard.md)
- [graf-bloodbrand.md](silent-fortune/graf-bloodbrand.md)
- [isaac-nocturne.md](silent-fortune/isaac-nocturne.md)
- [kael-thorne.md](silent-fortune/kael-thorne.md)
- [kline-fendrix.md](silent-fortune/kline-fendrix.md)
- [lucia-blackwood.md](silent-fortune/lucia-blackwood.md)
- [lyla-fortune.md](silent-fortune/lyla-fortune.md)
- [maria_luna.md](silent-fortune/maria_luna.md)
- [orphea-stringheart.md](silent-fortune/orphea-stringheart.md)
- [rudy-gearwright.md](silent-fortune/rudy-gearwright.md)
- [serena-whiteford.md](silent-fortune/serena-whiteford.md)
- [seril-wenston.md](silent-fortune/seril-wenston.md)

---

## 2. Player (ตัวละครจากโลกจริง)
- [kanokwan-sarisa.md](player/kanokwan-sarisa.md)

---

## 3. NPC (ตัวละครสำคัญของโลก Orthia)
- [elrys-memory.md](npc/elrys-memory.md)
- [marek-kozlowski.md](npc/marek-kozlowski.md)
- [thuren-boundary.md](npc/thuren-boundary.md)
- [verel-drystrom.md](npc/verel-drystrom.md)

---

## 4. Enemy (ฝ่ายศัตรู)
- [nigel-darkraven.md](enemy/nigel-darkraven.md)
- [rex-flameheart.md](enemy/rex-flameheart.md)
- [victor-falkner.md](enemy/victor-falkner.md)
- [zargos_werth.md](enemy/zargos_werth.md)

---

## 5. Story-Based / Alternate Characters

### EP2
- [echo-phantom-prototype.md](story/ep2/echo-phantom-prototype.md)
- [guardian-of-reflection.md](story/ep2/guardian-of-reflection.md)
- [isaac-nocturne-alt.md](story/ep2/isaac-nocturne-alt.md)
- [maria-luna-alt.md](story/ep2/maria-luna-alt.md)

### EP3
- [kline-fendrix-ep3.md](story/ep3/kline-fendrix-ep3.md)

---

## หมายเหตุ

- ตัวละครที่มีเวอร์ชัน "alt" หรือ "เฉพาะ EP" จะถูกจัดแยกชัดเจนภายใต้ `story/epX/`  
- AI สามารถใช้ข้อมูลนี้เพื่อ:  
  - สร้างความสัมพันธ์ระหว่างตัวละคร  
  - กำหนดบทบาทในแต่ละตอน  
  - ตรวจสอบพัฒนาการของตัวละครข้ามตอน  
- ชื่อลิงก์ไฟล์ทั้งหมดสอดคล้องกับชื่อไฟล์ใน repo  
- ใช้ร่วมกับระบบ `WSP-Character-Intro` และ worldbuilding ได้โดยตรง
