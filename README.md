# FARMING WAR – README (TH/EN)

## สารบัญ / Table of Contents

1. [ภาพรวมโปรเจกต์ / Project Overview](#1-ภาพรวมโปรเจกต์--project-overview)
2. [ระบบตัวละคร / Character System](#2-ระบบตัวละคร--character-system)
3. [ระบบโลกและเศรษฐกิจ / Worldbuilding & Economy](#3-ระบบโลกและเศรษฐกิจ--worldbuilding--economy)
4. [มอนสเตอร์ / Monster System](#4-มอนสเตอร์--monster-system)
5. [โครงสร้างการเขียนตอน / Episode Writing Format](#5-โครงสร้างการเขียนตอน--episode-writing-format)
6. [ระบบเวท Echo และ Seal / Magic System](#6-ระบบเวท-echo-และ-seal--magic-system-echo--seal)
7. [ทีม Silent Fortune / Silent Fortune Team](#7-ทีม-silent-fortune--silent-fortune-team)
8. [คนต่างโลก / The Outworlder (Kanokwan Sarisa)](#8-คนต่างโลก--the-outworlder-kanokwan-sarisa)
9. [เทมเพลตและเมทาดาทา / Templates & Metadata](#9-เทมเพลตและเมทาดาทา--templates--metadata)
10. [กลยุทธ์การเล่าเรื่อง / Foreshadowing & Cross-Episode Strategy](#10-กลยุทธ์การเล่าเรื่อง--foreshadowing--cross-episode-strategy)
11. [ระบบเควส / Quest System](#11-ระบบเควส--quest-system)
12. [เศษเวทและ anomaly / Fragments & Anomalies](#12-เศษเวทและ-anomaly--fragments--anomalies)
13. [GitHub Workflow](#13-github-workflow)
14. [การเชื่อมโยงข้ามบท / Cross-Episode Strategy](#14-กลยุทธ์การเชื่อมโยงข้ามบท--cross-episode-strategy)
15. [วิสัยทัศน์และสรุปภาพรวม / Vision & Final Summary](#15-วิสัยทัศน์และสรุปภาพรวม--vision--final-summary)

---

# FARMING WAR – Structure Overview (โครงสร้างโปรเจกต์แบบละเอียด)

```
FARMING-WAR/
├── .github/
│   └── workflows/                 # GitHub Actions, CI/CD
│
├── characters/                   # ตัวละครทั้งหมด
│   ├── silent-fortune/           # ทีมหลักของไคลน์
│   ├── npc/                      # ตัวละครสนับสนุน, นักวิจัย, ผู้เฝ้าผนึก
│   ├── enemy/                    # ฝ่ายศัตรู, บอส, ผู้ใช้เวทเงา
│   └── player/                   # คนต่างโลก เช่น Kanokwan Sarisa
│
├── context-ai/                   # สำหรับ AI ใช้เชื่อมโยงและอ่านบริบท
│   ├── characters-index.yaml
│   ├── magic-index.yaml
│   ├── echo-network-map.md
│   └── timeline.md
│
├── items/                        # ระบบไอเท็มทั้งหมด
│   ├── weapons/                  # อาวุธ เช่น seal-breaker-lance.md
│   ├── accessories/              # เครื่องประดับ
│   ├── materials/                # วัตถุดิบ เช่น fragment-dust.md
│   └── schematics/               # แบบพิมพ์การคราฟต์
│
├── magic/                        # เวทมนตร์ทุกระบบ
│   ├── ep1/                      # เวทเฉพาะตอน
│   ├── epX/                      # เวทเฉพาะบทอื่น ๆ
│   └── core/                     # เวทระบบหลัก เช่น echo-pulse.md
│
├── monsters/                     # ข้อมูลมอนสเตอร์ทั้งหมด
│   ├── rank-d/
│   ├── rank-c/
│   ├── rank-b/
│   ├── rank-a/
│   └── rank-x/                   # มอนสเตอร์พิเศษระดับสุดท้าย
│
├── project/                      # ไฟล์จัดการโครงสร้าง นิยามภารกิจ Dev
│   ├── dev-roadmap.md
│   ├── structure-spec.md
│   └── deployment-checklist.md
│
├── quests/                       # ภารกิจและเงื่อนไขต่าง ๆ
│   ├── main-quests/
│   └── side-quests/
│
├── story/                        # ตอนนิยายหลัก (แบ่งบท/พาร์ท)
│   ├── ep1/
│   │   ├── ep1-01/
│   │   │   ├── ep1-01-1of5.md
│   │   │   └── ep1-01-README.md
│   │   └── ep1-05/
│   ├── ep2/
│   └── epX/
│
├── structure-dev/                # โครงต้นแบบ ระบบทดสอบ แนวคิดใหม่
│   ├── magic-prototype.md
│   ├── team-meta-structure.md
│   └── expansion-plans.md
│
├── teams/                        # การจัดกลุ่มตัวละคร, พันธมิตร, ฝ่าย
│   ├── silent-fortune-team.md
│   └── others/
│
├── templates/                    # แม่แบบทุกหมวด
│   ├── character-template.md
│   ├── episode-metadata-template.md
│   ├── item-template.md
│   ├── location-template.md
│   ├── magic-template.md
│   └── quest-template.md
│
├── worldbuilding/                # ข้อมูลโลก Orthia
│   ├── locations/
│   │   ├── ep1/
│   │   └── epX/
│   ├── anomaly/
│   ├── quests/
│   ├── factions/
│   └── economy/
│       ├── global-trade-network.md
│       ├── monster-drop-market.md
│       └── orthia-currency.md

---

# PROJECT SUMMARY – FARMING WAR (TH/EN)

> *เอกสารนี้สรุปข้อมูลโปรเจกต์นิยาย "Farming War" อย่างเป็นระบบ*  
> *This document summarizes the novel project "Farming War" in a structured format.*

---

## 1. ภาพรวมโปรเจกต์ / Project Overview

**ชื่อโปรเจกต์:** Farming War  
**แนวเรื่อง:** แฟนตาซี, การบริหารทรัพยากร, ฟาร์ม, ล่ามอนสเตอร์, การเมือง, ระบบเศรษฐกิจ  
**จำนวนเป้าหมาย:** 100 บท (500 ตอน), ตอนละ ~5 พาร์ท (~60 บรรทัดต่อพาร์ท)  
**โลก:** ออร์เทีย (Orthia) – โลกแฟนตาซีที่เต็มไปด้วยเวทโบราณและระบบผนึก

**Project Name:** Farming War  
**Genres:** Fantasy, resource management, farming, monster hunting, politics, economy  
**Target Volume:** 100 Episodes (500 chapters), each ~5 parts (~60 lines/part)  
**World:** Orthia – A fantasy world shaped by ancient magic and sealed systems

---

## 2. ระบบตัวละคร / Character System

ตัวละครแบ่งเป็น 4 กลุ่มหลัก:
- `silent-fortune/` – ทีมของพระเอก
- `npc/` – ตัวละครท้องถิ่น
- `enemy/` – ฝ่ายตรงข้ามหรือมอนสเตอร์
- `player/` – คนต่างโลก (มีเพียง 1 คนเท่านั้น: Kanokwan Sarisa)

Characters are categorized into 4 groups:
- `silent-fortune/` – Protagonist's team
- `npc/` – Local world characters
- `enemy/` – Opponents or monsters
- `player/` – Outworlder (only 1 exists: Kanokwan Sarisa)

**Template มาตรฐาน:** WSP-Character-Intro  
ประกอบด้วยชื่อ, อายุ, บุคลิก, บทบาท และหมายเหตุ

**Standard Template:** WSP-Character-Intro  
Includes name, age, traits, role, and notes.

---

## 3. ระบบโลกและเศรษฐกิจ / Worldbuilding & Economy

**Orthia** เป็นโลกแฟนตาซีไม่มีเทคโนโลยีล้ำยุค  
แผนที่โลกประกอบด้วยเมืองหลัก, เขตเวทเก่า, anomaly, ป่าลึก และโซนอุตสาหกรรมเวท

**Orthia** is a fantasy world with no modern tech.  
The map includes major cities, ancient magic zones, anomalies, deep forests, and arcane industries.

ระบบเศรษฐกิจ:
- ใช้สกุลเงินกลาง
- ตลาดผูกกับทรัพยากรจากมอนสเตอร์
- ราคาเปลี่ยนตามความต้องการและความเสี่ยงในการหา

Economy System:
- Uses a central currency
- Market linked to monster-derived resources
- Prices vary by demand and risk

---

## 4. มอนสเตอร์ / Monster System

มอนสเตอร์แบ่งตามแรงค์:
- D: ฝึกฝนทั่วไป
- C: มีความสามารถเฉพาะ ต้องใช้ทีม
- B: ระดับเมือง
- A: ระดับรัฐ
- X: นอกระบบ, anomaly

Monsters are ranked:
- D: Basic training
- C: Tactical, requires teams
- B: City-level threats
- A: National-level threats
- X: Out-of-system anomaly types

Metadata ของมอนสเตอร์แต่ละตัวประกอบด้วย: ชื่อ, ประเภท, สกิล, เขต, วิธีรับมือ, ไอเท็มดรอป

Monster metadata includes: name, type, skills, region, tactics, drops

---

## 5. โครงสร้างการเขียนตอน / Episode Writing Format

นิยาย 1 บท = 5 ตอน  
1 ตอน = 5 พาร์ท (epX-Y-1of5.md ถึง 5of5.md)  
แต่ละพาร์ทยาว ~60 บรรทัด

One episode group = 5 chapters  
Each chapter = 5 parts (epX-Y-1of5.md to 5of5.md)  
Each part ~60 lines

### โครงสร้าง Markdown มาตรฐาน:
```markdown
#EP X/Y

- ตอนที่ X: [ชื่อตอน]
- บทที่ Y: [ชื่อบทหลัก]
- หมายเหตุ: [บริบทสำคัญของตอน]

[เนื้อหานิยาย]

---

[END] ตอนที่ X – [ชื่อตอน] | ต่อ: EP X+1
```

### ตัวอย่าง / Example:
```markdown
#EP 21/5

- ตอนที่ 21: เสียงแรกจากอีกฟากของเงา  
- บทที่ 5: เสียงแรกจากอีกฟากของเงา  
- หมายเหตุ: ทีม Silent Fortune ฟื้นตัวและพบเสียงสะท้อนใหม่ในป่า

แสงจากวงเวทหกชั้นค่อย ๆ สลายตัวไปพร้อมกับไอหมอกเย็น...

---

[END] ตอนที่ 21 – เสียงแรกจากอีกฟากของเงา | ต่อ: EP22
```

---

## 6. ระบบเวท Echo และ Seal / Magic System (Echo & Seal)

ระบบเวทมนตร์ของโลก Orthia แบ่งเป็น 2 แกนหลัก:

### 6.1 Echo System (ระบบเสียงสะท้อน)
- พลังเวทที่เกิดจาก “ข้อมูลของอดีตหรือสิ่งที่ถูกลืม”
- ไม่สามารถสร้างเอง แต่สามารถ “รับรู้หรือดึงมาใช้” ได้
- ตอบสนองเฉพาะผู้ที่มีคุณสมบัติเข้ากัน เช่น ไคลน์, Kanokwan

**ตัวอย่างเวท Echo:**
- Echo Pulse – ตรวจจับรอยรั่วของผนึก
- Fragment Echo – เศษความทรงจำที่รั่วออกมา
- Echo Fusion – รวมเสียงจากหลายแหล่งเพื่อปลุกพลัง

### 6.2 Seal Network (เครือข่ายผนึก)
- โครงข่ายเวทที่ปกป้องความลับและพลังเวทเก่า
- กระจายอยู่ทั่วโลก เช่น Stone Inscription Plaza, Inner Seal Core
- หากผนึกเสียหาย อาจเกิด anomaly หรือปล่อยเศษเวท

**ตัวอย่างเวทผนึก:**
- Mirror Seal – ผนึกสะท้อนข้อมูล
- Seal Resonance – การสั่นพ้องของผนึก
- New Seal Theory – ทฤษฎีใหม่ที่เจาะเครือข่ายผนึกได้

---

## 7. ทีม Silent Fortune / Silent Fortune Team

ทีมหลักของพระเอก "ไคลน์ เฟนดริกซ์" ประกอบด้วยสมาชิกสูงสุด 16 คน  
เป็นทีมกึ่งทหารกึ่งนักผจญภัย ที่โตจากการล่ามอนสเตอร์และสร้างไอเท็ม

**Silent Fortune คือ:**
- ทีมอิสระ ไม่ขึ้นกับกิลด์ใด
- พึ่งพากันด้วยบทบาทเฉพาะ ไม่ใช้ระบบคลาสตายตัว
- แยกทีมย่อยได้ตามภารกิจ: scouting, assault, support

**สมาชิกตัวอย่าง:**
- ไคลน์ (Klein) – ผู้นำ, นักวางแผน
- ลาร่า – นักเจรจา, วิเคราะห์ตลาด
- แรมมอส – แทงค์กึ่งเวท

ทุกคนพัฒนาโดยใช้ “ไอเท็มและข้อมูล” ไม่ใช่พลังภายใน

---

## 8. คนต่างโลก / The Outworlder (Kanokwan Sarisa)

**ชื่อ:** กนกวรรณ สาริษา (Kanokwan Sarisa)  
**ชื่อเล่น:** นก  
**สถานะ:** คนไทยจากโลกปัจจุบัน (มีเพียงคนเดียวในโลก Orthia)  
**ความจำ:** ครบถ้วนจากโลกเดิม

**บทบาทในเรื่อง:**
- เข้ามาในโลก Orthia โดยไม่ทราบสาเหตุ  
- มีปฏิกิริยากับเวท Echo และระบบผนึกไวผิดปกติ  
- ทำให้ anomaly หลายจุดเริ่มเคลื่อนไหว

**ไม่ใช่ตัวเอก** แต่เป็นจุดเปลี่ยนของเรื่อง  
มีข้อมูลที่ระบบเวทของโลกนี้ไม่สามารถตีความได้

---

## 9. เทมเพลตและเมทาดาทา / Templates & Metadata

เพื่อให้เนื้อหาของโปรเจกต์มีความเป็นระบบ ใช้งานร่วมกับ AI และนักเขียนได้ง่าย  
จำเป็นต้องมี **template** และ **metadata** ที่ชัดเจนในทุกหมวด

**ตัวอย่าง Template ที่ใช้:**

- `episode-metadata-template.md`:  
  ใช้สรุปเนื้อหาตอน เช่น ชื่อตอน, ตัวละคร, เวท, สถานที่, เควส

- `WSP-Character-Intro`:  
  ใช้เขียนตัวละครทุกตัว (ชื่อ, อายุ, บุคลิก, บทบาท ฯลฯ)

- `magic-template.md`:  
  สำหรับเวท – ระบุชื่อเวท, ประเภท, เงื่อนไข, ผลกระทบ และตอนที่ใช้

**Metadata ตัวอย่าง (YAML):**
```yaml
episode: ep4-18
title: ตัวแปรที่ไม่ควรมีอยู่
characters:
  - klein
  - kanokwan
magic:
  - fragment-echo
  - echo-pulse
location: echo-depth
quest: investigate-fracture
```

---

## 10. กลยุทธ์การเล่าเรื่อง / Foreshadowing & Cross-Episode Strategy

เพื่อให้เรื่องร้อยเรียงต่อเนื่อง มีแรงดึงและไม่หลุดธีม  
ระบบการ “วางเบาะแสล่วงหน้า” (Foreshadowing) และ “เชื่อมโยงข้ามตอน” จึงมีความสำคัญ

### เทคนิคที่ใช้:
- วางข้อมูลหรือประโยคเล็ก ๆ ที่ยังไม่อธิบายในตอนนั้น  
- ใช้เสียง Echo หรือ anomaly เป็นตัวเล่าเรื่องแทนคำอธิบาย  
- เฉลยในตอนหลัง โดยย้อนกลับไปเชื่อมตอนเก่าได้อย่างมีเหตุผล

**ตัวอย่าง:**
- Fragment Echo ใน EP3-13 ถูกเฉลยว่าเกี่ยวข้องกับเหตุการณ์ใน EP6-25  
- คำพูดของตัวละครที่เคยพูดไว้ “เล่น ๆ” กลายเป็นเงื่อนไขเวทในตอนหลัง

### สำหรับ AI:
- ตรวจสอบ README อย่างน้อย 3 ตอนก่อนหน้า  
- ค้นหาเบาะแสหรือข้อมูลที่ยังไม่ถูกปิดประเด็น  
- หากจะวางเบาะแสใหม่ ให้บันทึกไว้ใน metadata `foreshadow: true`

---

## 11. ระบบเควส / Quest System

เควสคือกลไกหลักที่ขับเคลื่อนทีม Silent Fortune ไปยังพื้นที่ใหม่  
และเปิดโอกาสให้ค้นพบ anomaly, Echo หรือพลังที่ไม่ได้บันทึกไว้ในระบบ

### ประเภทเควส:
- Gathering – เก็บวัตถุดิบ
- Hunting – ล่ามอนสเตอร์เป้าหมาย
- Escort – คุ้มกัน NPC หรือวัตถุ
- Investigation – สำรวจ anomaly หรือเศษเวท
- Faction/War – ภารกิจสงครามหรือสายลับระหว่างองค์กร

### ความพิเศษ:
- เควสระดับสูงจะไม่มีรางวัลแจ้งล่วงหน้า  
- ต้องเสี่ยงแลกกับข้อมูล, fragment, หรือเวทต้นฉบับ

**Metadata ตัวอย่าง:**
```yaml
quests:
  - name: Investigate the Dissonant Chamber
    type: investigation
    location: echo-depth
    required_by: ep4-18
    result: Echo-born Entity Triggered
```

---

## 12. เศษเวทและ anomaly / Fragments & Anomalies

### 12.1 Fragment System (ระบบเศษเวท)
- Fragment คือเศษของพลังเวทหรือข้อมูลเวทที่หลุดออกจากระบบผนึก
- แบ่งเป็น:
  - Fragment Echo – เสียงหรือคลื่นข้อมูลจากอดีต
  - Fragment Seal – เศษผนึกที่ยังมีพลัง
  - Fragment Entity – สิ่งมีชีวิตที่ก่อตัวจากเศษเวท

### ลักษณะการใช้งาน:
- ใช้ปลดล็อกเวท, เปิดเผยข้อมูลที่หายไป, หรือเปิดทางใหม่
- ไม่สามารถควบคุมตรง ๆ ได้ แต่ตอบสนองกับ “เสียง” หรือ “คลื่นพลัง”

### 12.2 Anomaly (จุดแปรปรวนพลังงาน)
- เขตผิดปกติที่เกิดจาก Fragment หรือผนึกที่แตก
- ส่งผลต่อพื้นที่/มิติ/เวลา และทำให้เวทบางประเภทล้มเหลว
- AI ต้องอ้างอิง anomaly เหล่านี้เมื่อเขียนตอนที่มีผลกระทบเวทใหญ่

**ตัวอย่างการปรากฏในเนื้อเรื่อง:**
- EP3-13: Fragment Echo โผล่รอบจุดผนึก
- EP4-17: ทางเดินใหม่ปรากฏจากเสียงสะท้อนที่ไม่มีในแผนที่
- EP4-18: Fragment Entity ปรากฏกลาง anomaly

---

## 13. GitHub Workflow

เพื่อให้โปรเจกต์นิยายทำงานร่วมกับ AI และนักเขียนหลายคนได้  
จึงกำหนด Workflow ที่ชัดเจนในการเขียน อัปเดต และเชื่อมโยงข้อมูล

### 13.1 โฟลเดอร์หลัก
- `story/epX/` – ตอนนิยาย
- `magic/epX/` – เวทที่ใช้ในแต่ละบท
- `characters/` – ตัวละครแยกตามกลุ่ม
- `worldbuilding/` – สถานที่, factions, economy
- `templates/` – Template การเขียน README และ metadata

### 13.2 ขั้นตอนเขียนตอนใหม่
1. ตรวจ `epX-README.md` และตอนล่าสุด
2. ใช้ `episode-metadata-template.md` สร้าง README ตอน
3. เขียนตอนใหม่ `epX-Y-1of5.md` ถึง `5of5.md`
4. เชื่อมโยงเวท/ตัวละคร/เควส/สถานที่ใน README
5. อัปเดต `characters-README.md`, `magic-README.md` ฯลฯ
6. Commit พร้อมข้อความสื่อความเข้าใจ เช่น `Add EP4-18 (complete)`

---

## 14. กลยุทธ์เบาะแสล่วงหน้า / Hidden Clues Strategy

### เป้าหมาย
- สร้างการรอคอยที่มีน้ำหนัก
- ทำให้ผู้อ่าน “กลับไปอ่านตอนก่อนหน้า” เมื่อเบาะแสเฉลย
- ทำให้ AI เชื่อมโยงข้อมูลข้ามบทได้อย่างมีระบบ

### เทคนิคการวางเบาะแส
- ใช้ Fragment หรือ anomaly เป็นตัวเล่าแทนคำบรรยาย
- วางภาพ/เสียง/ประโยค ที่มีความหมายในตอนหลัง
- หลีกเลี่ยงการเฉลยทันที ค่อย ๆ ปลดผ่าน Echo หรือ Seal

**Metadata ตัวอย่าง:**
```yaml
foreshadow: true
hint_type: echo-anomaly
appears_in: ep3-13
resolved_in: ep6-25
```

---

## 15. วิสัยทัศน์และ Roadmap / Vision & Roadmap (500 ตอน)

โปรเจกต์ "Farming War" วางแผนโครงสร้างยาว 500 ตอน  
แบ่งเป็น 100 บท (EP1–EP100) โดยมีธีมหลักในแต่ละช่วงชัดเจน

| ตอนที่ (EP) | ธีมหลัก | คำอธิบาย |
|-------------|----------|-----------|
| EP1–10 | จุดเริ่มต้นของการล่า | สร้างทีม ฟาร์ม ทดสอบระบบ |
| EP11–20 | ผนึกและเสียงสะท้อน | เผชิญเวท Echo และเงาโบราณ |
| EP21–40 | ขยายพลังและพันธมิตร | สู้กับกลุ่มภายนอก, พัฒนาอาวุธ |
| EP41–60 | เศษเวทและข้อมูลที่หายไป | เปิดเผย anomaly และสู้กับระบบ |
| EP61–80 | สงครามผนึก | ระบบผนึกทั่วโลกเริ่มสั่นคลอน |
| EP81–99 | วิกฤตระดับทวีป | ความจริงของโลกเริ่มเปิดเผย |
| EP100 | จุดเปลี่ยนของโลก | ตัดสินชะตา Echo และระบบเวททั้งมวล |

---

## การทำงานร่วมของ AI และนักเขียน / AI & Writer Collaboration

### สำหรับ AI
- ใช้ `context-ai.md`, `characters-index.yaml`, `magic-README.md` เป็นจุดเริ่มต้น
- อ้างอิง `epX-Y-README.md` ก่อนเขียนตอน
- หากมีข้อมูลไม่พอ: แจ้งเตือนก่อนแต่ง

### สำหรับนักเขียน
- สร้างไฟล์ใหม่ตามโครงสร้าง Markdown ที่กำหนด
- ทุกไฟล์ใหม่ต้องเชื่อมโยงผ่าน README หรือ index
- เน้น “ระบบ” ไม่เน้น “อารมณ์ล้น”

---

## โฟลเดอร์เสริมที่ควรจัดทำ / Recommended Folder Additions

| โฟลเดอร์ | ใช้สำหรับ |
|----------|------------|
| `worldbuilding/anomaly/` | anomaly แต่ละจุด, สภาพเวทผิดปกติ |
| `worldbuilding/quests/` | เก็บภารกิจทุกเควสที่เกิดขึ้น |
| `characters/player/kanokwan-sarisa.md` | ตัวละครคนต่างโลก |
| `magic/core/` | เวทระดับแกน เช่น Echo Pulse, Seal Origin |

---

## ปิดท้าย / Final Note

> *Farming War* ไม่ใช่แค่นิยาย แต่คือระบบแฟนตาซีที่ออกแบบให้เติบโตจากการเชื่อมโยงข้อมูล  
> หากทุกไฟล์ถูกจัดการอย่างมีโครงสร้าง โลกนี้จะพัฒนาอย่างต่อเนื่องโดยไม่ต้องพึ่ง “ตัวละครที่โกง”

---

[END] README.md 5/15

---

## 16. Echo System (ระบบเสียงสะท้อน) – เชิงลึก / Deep Echo System

ระบบ Echo ไม่ใช่เวทโจมตีหรือสนับสนุนโดยตรง  
แต่เป็นระบบที่ “ดึงข้อมูลจากอดีตหรืออนาคตที่ผิดเพี้ยน” มาส่งผลในปัจจุบัน

### ประเภทของ Echo:
- **Echo Pulse:** คลื่นเสียงที่ใช้ตรวจจับโครงสร้างเวท
- **Fragment Echo:** เศษข้อมูลที่ล่องลอยอยู่ใน anomaly
- **Echo Fusion:** การรวมคลื่นจากหลายต้นกำเนิดให้เกิดพลังใหม่
- **Inheritance Link:** การเชื่อมโยงข้อมูลเวทระหว่างผู้ใช้กับโครงสร้างเก่า

### กลไกการทำงาน:
- Echo จะแสดงผลเมื่ออยู่ในเขตที่มี “ความไม่เสถียรของผนึก”
- ยิ่งใช้บ่อย ยิ่งเกิดผลข้างเคียง เช่น ความทรงจำย้อนกลับ, สูญเสียการควบคุมเวท

---

## 17. Seal Network (เครือข่ายผนึก) – เชิงลึก / Advanced Seal Network

เครือข่ายผนึกคือระบบ “เก็บกักข้อมูล, พลัง, หรือความจริง”  
ใช้ควบคุมโครงสร้างของโลกเวทมนตร์

### โครงสร้างผนึก:
- จุดศูนย์กลาง: Core Node
- จุดสื่อสาร: Resonant Node
- จุดควบคุม Echo: Reflection Node

### อันตรายจากการแตะต้อง:
- หากเปิดผนึกโดยไม่มี “ความสอดคล้องทางเสียง” จะเกิดการย้อนสะท้อน  
- ผนึกบางจุด “หลอกข้อมูล” หรือสร้าง Echo ปลอม

---

## 18. การเชื่อมโยง Echo กับ Seal

เมื่อ Echo สัมผัสกับผนึกโดยตรง จะเกิด:
- **Data Leak:** ข้อมูลเวทในอดีตรั่วไหล
- **Anomaly Growth:** anomaly ขยายตัว
- **Memory Activation:** ความทรงจำที่ถูกผนึกตื่นขึ้น

**ตัวอย่างในเนื้อเรื่อง:**
- EP4-18: Fragment Echo กระตุ้นระบบผนึกให้เกิดการต่อต้าน
- EP4-20: ไคลน์ได้รับการยอมรับจาก “เสียง” ในระบบผนึกเก่า

---

## 19. ทีม Silent Fortune – เชิงลึก / Silent Fortune – Deep Profile

ทีม Silent Fortune เป็นแกนหลักของเนื้อเรื่อง  
เติบโตจากการฟาร์ม, ล่า, และรับมือ anomaly โดยไม่พึ่งพาพลังเหนือธรรมชาติ

### 19.1 รูปแบบการทำงานในทีม
- ไม่มีระบบคลาสตายตัว → ทุกคนปรับตามไอเท็มที่มี
- แบ่งบทบาทแบบยืดหยุ่น เช่น แทงค์ล้ำหน้า, นักเวทลอบสังหาร
- ใช้ระบบ “ผู้เชี่ยวชาญเชิงสถานการณ์” (เช่น ผู้เปิดผนึก, นักประเมินเศษเวท)

### 19.2 การพัฒนา
- อิงจากประสบการณ์และทรัพยากร ไม่ใช่เลเวล
- ทุกไอเท็มและข้อมูลที่ได้รับมา “ต้องแลก” ด้วยความเสี่ยง

---

## 20. ตัวอย่างความสัมพันธ์ภายในทีม

| สมาชิก | ความสัมพันธ์ | หมายเหตุ |
|--------|----------------|----------|
| ไคลน์ – ลาร่า | ผู้นำ – ที่ปรึกษา | ความไว้ใจสูง, ปะทะคารมบ่อย |
| ลาร่า – แรมมอส | นักวิเคราะห์ – ผู้ลงมือ | แรมมอสรับคำแนะนำลาร่ามากกว่าคำสั่งไคลน์ |
| ไคลน์ – นก (Kanokwan) | สงสัย – เปิดใจ | ไคลน์เริ่มเปิดรับข้อมูลจากต่างโลก |

---

## 21. ระบบย่อยในทีม / Subsystems in the Team

- **หน่วย Scout:** เคลื่อนไหวเร็ว ใช้ตรวจ anomaly
- **หน่วย Frontline:** รับมือมอนสเตอร์ระดับ B ขึ้นไป
- **หน่วย Data / Seal:** วิเคราะห์ข้อมูลผนึก, แปล fragment

ทุกภารกิจใช้ทีมผสม (ไม่ตายตัว)  
แต่ละคนจะมี “ค่าเชื่อมั่น” (trust metric) ที่กำหนดการตัดสินใจร่วมกัน

---

## 22. เอกสารอ้างอิงภายใน

- `characters/silent-fortune/*.md` – โปรไฟล์สมาชิกแต่ละคน  
- `story/epX/epX-Y-README.md` – ตอนที่มีความสัมพันธ์เด่นชัด  
- `templates/episode-metadata-template.md` – ระบุการมีส่วนร่วมของแต่ละตัวละคร

---

## 23. คนต่างโลก – Kanokwan Sarisa / The Outworlder

โลก Orthia มีเพียง "หนึ่งคน" ที่ไม่ได้เกิดในโลกนี้  
นั่นคือ **Kanokwan Sarisa (กนกวรรณ สาริษา)** หรือชื่อเล่นว่า “นก”

---

## 24. ข้อมูลพื้นฐาน / Basic Information

| รายการ | รายละเอียด |
|--------|-------------|
| ชื่อเต็ม | กนกวรรณ สาริษา (Kanokwan Sarisa) |
| ชื่อเล่น | นก |
| ภูมิลำเนา | ประเทศไทย (โลกเดิม) |
| ความจำ | มีครบถ้วนก่อนเข้าสู่โลกนี้ |
| สถานะ | คนเดียวจากต่างโลกใน Orthia |

---

## 25. บทบาทในเนื้อเรื่อง / Role in the Story

- ปรากฏตัวครั้งแรกใน EP4-17 ในเขต anomaly
- มีปฏิกิริยาแรงกับ Echo และ Seal โดยไม่ต้องฝึกเวท
- ปลุกข้อมูลที่ผนึกไว้อย่างไม่ตั้งใจ
- เป็นคนเดียวที่เข้าใจ “มุมมองโลกจริง” เมื่อเทียบกับระบบเวทใน Orthia

---

## 26. จุดเด่นและจุดอ่อน

### จุดเด่น
- เข้าใจโครงสร้างระบบโดยไม่ต้องมีพลังเวท
- คิดนอกกรอบจากระบบของ Orthia ได้
- มีภูมิต้านทานจาก anomaly ในระดับหนึ่ง

### จุดอ่อน
- ไม่มีไอเท็มหรือพลังต่อสู้โดยตรง
- การเคลื่อนไหวของเธออาจทำให้ผนึกผิดเพี้ยน

---

## 27. ความสัมพันธ์กับทีม Silent Fortune

- เริ่มต้นจากความไม่ไว้วางใจ (ไคลน์ระวังตัว)  
- ลาร่าเห็นว่าเธอคือ "ตัวแปรจากนอกระบบ"  
- กลายเป็นผู้ให้เบาะแสกับ Echo ที่ทีมเข้าถึงไม่ได้

> เธอไม่ใช่ตัวเอก แต่คือกุญแจสำคัญของการเปิดเผย “โครงสร้างความจริงของโลก”

---

## 28. เอกสารที่เกี่ยวข้อง

- `characters/player/kanokwan-sarisa.md` – (ต้องจัดทำแยก)  
- `story/ep4/ep4-17-README.md` ถึง `ep4-20-README.md` – บทหลักของเธอ  
- `magic/ep4/echo-fusion.md`, `inheritance-link.md` – เวทที่เกี่ยวข้อง  
- `worldbuilding/anomaly/` – พื้นที่ที่เธอมีอิทธิพล

---

## 29. การวางเบาะแสล่วงหน้า / Foreshadowing Strategy

การวางเบาะแสล่วงหน้าเป็นหนึ่งในแกนหลักของการเล่าเรื่องใน Farming War  
เพื่อให้ข้อมูลในอดีตหรือคำพูดบางประโยค กลับมามีความหมายในตอนหลัง

---

## 30. จุดประสงค์ของการวางเบาะแส / Purpose

- สร้างความรู้สึกต่อเนื่องทางเนื้อเรื่อง  
- ทำให้ผู้อ่านอยาก “กลับไปอ่านตอนเก่า”  
- สร้างน้ำหนักให้กับเหตุการณ์สำคัญในตอนที่เฉลย

---

## 31. เทคนิคที่ใช้ / Techniques

### เทคนิคฝั่งนักเขียน
- ใส่ “คำที่ดูเหมือนธรรมดา” แต่มีความหมายลึก
- แทรก anomaly โดยไม่มีคำอธิบายทันที
- ใช้บรรยากาศหรือสิ่งแวดล้อมให้เป็นตัวใบ้

### เทคนิคฝั่ง AI
- ตรวจสอบ README อย่างน้อย 3 ตอนก่อนหน้า  
- ดึงคำพูด ตัวละคร หรือ Echo ที่ยังไม่มีคำอธิบาย  
- วาง metadata: `foreshadow: true`

---

## 32. ตัวอย่างการวางเบาะแส

| ตอนแรกพบ | ตอนที่เฉลย | รายละเอียด |
|-----------|-------------|-------------|
| EP3-13 | EP6-25 | เสียงในป่าไม่มีที่มา กลายเป็น Fragment Echo ที่ตอบสนอง Echo Fusion |
| EP4-17 | EP5-23 | สิ่งที่ Kanokwan สัมผัส กลายเป็นผนึกชนิดใหม่ |

---

## 33. Metadata ตัวอย่าง / Sample Metadata

```yaml
foreshadow: true
hint_type: fragment-echo
appears_in: ep4-17
resolved_in: ep5-23
character: kanokwan
```

เบาะแสเหล่านี้จะช่วยให้โครงเรื่องมีมิติ  
และช่วยให้นักเขียน/AI สามารถสร้างการเชื่อมโยงระยะยาวได้อย่างมั่นคง

---

## 34. ระบบเควส / Quest System

เควสคือโครงสร้างหลักที่เชื่อมการผจญภัย, การฟาร์ม, และการเปิดเผยข้อมูลในโลก Orthia

---

## 35. ประเภทเควส / Quest Types

| ประเภท | รายละเอียด | ตัวอย่าง |
|--------|-------------|----------|
| Gathering | เก็บวัตถุดิบจากธรรมชาติหรือมอนสเตอร์ | เก็บ Crystal Root 10 ชิ้น |
| Hunting | ล่ามอนสเตอร์เป้าหมาย | จัดการ Twinclaw Drake |
| Escort | คุ้มกัน NPC หรือวัตถุสำคัญ | ส่งหินผนึกไปยัง Stone Node |
| Investigation | สำรวจ anomaly หรือ fragment | ตรวจสอบเสียงที่ผิดเพี้ยนในป่า |
| Faction | สงครามหรือเควสเฉพาะกลุ่ม | ช่วยฝ่ายต่อต้าน Seal Network |

---

## 36. ความพิเศษของเควส

- เควสบางภารกิจ **ไม่มีรางวัลชัดเจน** ล่วงหน้า  
- ต้องอาศัยการตัดสินใจบน “ข้อมูลไม่ครบถ้วน”  
- การล้มเหลวอาจเปิดเผย fragment, anomaly หรือ Echo สำคัญ

---

## 37. การจัดการเควสในเนื้อเรื่อง

### Metadata ตัวอย่าง:
```yaml
quests:
  - name: Investigate the Dissonant Chamber
    type: investigation
    location: echo-depth
    required_by: ep4-18
    result: Echo-born Entity Triggered
```

### จุดที่ควรเขียนลง README:
- ใส่ใน `epX-Y-README.md` สำหรับตอนที่เกี่ยวข้อง  
- ลิงก์เควสกับตัวละคร, เวท, สถานที่ที่เกี่ยวข้อง  
- ระบุผลกระทบ เช่น เปิดทางใหม่, anomaly โผล่, NPC เสียหาย

---

## 38. เควสที่ไม่มีในระบบกลาง

- บาง anomaly “เรียก” เควสด้วยตัวเอง  
- Kanokwan หรือ Klein อาจ “กระตุ้นเควส” โดยไม่ผ่านระบบเมือง  
- ต้องจดบันทึกเควสแบบนี้แยกใน `worldbuilding/quests/` (ควรสร้างโฟลเดอร์นี้)

---

## 39. ระบบเศษเวทและ Anomaly / Fragment System & Anomalies

---

## 40. Fragment System (ระบบเศษเวท)

**Fragment** คือเศษของพลังเวทหรือข้อมูลที่ "หลุด" จากระบบผนึก  
มักเกิดจากการใช้เวทผิดเงื่อนไข หรือ anomaly สะสมพลังงานมากเกินไป

### ประเภทของ Fragment:
- **Fragment Echo:** เสียงหรือคลื่นข้อมูลที่ผิดเพี้ยน
- **Fragment Seal:** ชิ้นส่วนผนึกที่ยังคงพลังงาน
- **Fragment Entity:** สิ่งมีชีวิตที่ก่อตัวจาก fragment หลายประเภทรวมกัน

---

## 41. Anomaly (จุดแปรปรวน)

- เป็น “พื้นที่ผิดปกติ” ที่ระบบผนึกควบคุมไม่ได้อีกต่อไป  
- มีผลกับพลังเวท, เวลา, เส้นทาง และความจำของผู้เข้าใกล้  
- บาง anomaly ทำให้ Echo เก่า “พูดออกมาเอง”

### ตัวอย่าง anomaly:
- เขตผนึกหายไป (Seal Collapse Zone)  
- เสียงแฝงในเวทพื้นฐาน (Echoed Cast)  
- ความทรงจำที่ไม่ควรมี (Anomalous Memory)

---

## 42. กลไกการเกิด Anomaly

- ระบบผนึกมี “จุดต้านทาน” (Threshold) หากถูกกดดันมากเกินจะเกิดการแตก  
- เมื่อเสียงจาก Echo ไม่ตรงกับข้อมูลในผนึก → anomaly จะเริ่มขยายตัว  
- Fragment Entity อาจโผล่ออกมาและทำให้ผนึกอื่นรอบข้างเสียสมดุล

---

## 43. การใช้ anomaly ในการเขียนตอน

- anomaly ไม่ควรเป็นแค่ “พื้นที่แปลก” แต่เป็นจุดเปลี่ยนโครงสร้าง  
- สามารถใช้วางเบาะแส, กระตุ้น Echo, เปิดบทใหม่  
- ต้องบรรยายอย่างมีจังหวะ ไม่เฉลยทั้งหมดในฉากเดียว

---

## 44. เอกสารที่ควรสร้างเพิ่มเติม

- `worldbuilding/anomaly/README.md` – สรุป anomaly แต่ละจุด  
- `magic/fragment/` – เวทที่เกี่ยวข้องกับ fragment โดยตรง  
- `characters/npc/[ผู้วิจัย anomaly].md` – ตัวละครผู้ศึกษาหรือได้รับผลจาก anomaly

---

## 45. GitHub Workflow – สำหรับทีมเขียนและ AI / GitHub Workflow for Writers & AI

การจัดโครงสร้าง GitHub อย่างเป็นระบบ  
ช่วยให้โปรเจกต์ "Farming War" ดำเนินต่อได้โดยไม่มีข้อมูลสูญหาย

---

## 46. ขั้นตอนการเขียนตอนใหม่ / Writing New Episodes

1. ตรวจสอบ `story/epX/` ว่าถึงตอนใดแล้ว  
2. สร้าง `epX-Y-README.md` ตาม `episode-metadata-template.md`  
3. เขียนพาร์ทเนื้อหา `epX-Y-1of5.md` ถึง `epX-Y-5of5.md`  
4. ลิงก์ไฟล์กับ:
   - ตัวละคร → `characters/*.md`
   - เวท → `magic/*.md`
   - เควส → `worldbuilding/quests/`
   - สถานที่ → `worldbuilding/locations/`

5. อัปเดต README หลักของแต่ละหมวด
6. Commit พร้อมชื่อที่สื่อความเข้าใจ เช่น `Add EP5-22 (part 3 of 5)`

---

## 47. โครงสร้างโฟลเดอร์ที่ควรใช้

| โฟลเดอร์ | ใช้สำหรับ |
|----------|------------|
| `story/epX/` | เนื้อหานิยายแบ่งตามตอน |
| `characters/` | ข้อมูลตัวละครทุกกลุ่ม |
| `magic/` | เวทและระบบพลัง |
| `worldbuilding/` | สถานที่, anomaly, เศรษฐกิจ |
| `templates/` | แม่แบบ metadata |
| `context-ai/` | ข้อมูลภาพรวมของโปรเจกต์สำหรับ AI |

---

## 48. การทำงานของ AI ที่เหมาะสม

- ใช้ YAML index และ README ก่อนเขียนทุกครั้ง  
- ถ้าต้องเขียนตอนใหม่ → ตรวจ context จากตอนก่อนหน้า 2–3 ตอน  
- ไม่สร้างเวทหรือตัวละครใหม่โดยไม่มี template  
- แจ้งเตือนก่อนทุกครั้งหากพบ anomaly หรือข้อมูลไม่สอดคล้อง

---

## 49. ตัวอย่าง Metadata สำหรับตอน

```yaml
episode: ep5-22
title: เงาที่ไม่เคยถูกบันทึก
characters:
  - klein
  - echo-entity-alpha
magic:
  - seal-resonance
  - fragment-sequence
quests:
  - investigate-echo-anomaly
foreshadow: true
location: forbidden-echo-core
```

---

## 50. กลยุทธ์การเชื่อมโยงข้ามบท / Cross-Episode Strategy

การเล่าเรื่องใน Farming War ต้องสามารถ “เชื่อมโยงจากบทเก่าไปบทใหม่” ได้อย่างมีเหตุผล  
เพื่อให้การเปิดเผยข้อมูล, เงื่อนไขเวท, และพัฒนาการตัวละครมีความต่อเนื่อง

---

## 51. จุดประสงค์ของการเชื่อมโยง

- ป้องกันการเล่าเรื่องแบบขาดตอนหรือข้ามประเด็น  
- ทำให้การกลับมาอ่านย้อนหลังมีความหมาย  
- ช่วยให้ AI หรือนักเขียนใหม่ “เข้าใจระบบในระยะยาว”

---

## 52. ประเภทของการเชื่อมโยง

| ประเภท | ตัวอย่าง | เชื่อมโยงจาก |
|--------|----------|----------------|
| ไอเท็ม | Fragment Echo สีทอง | EP3 → EP6 |
| คำพูด | “หากเสียงเงียบลงเมื่อไร เราจะรู้...” | EP4 → EP5 |
| สถานที่ | เขตเวทต้องห้ามลึก | EP3 → EP7 |
| การกระทำ | การไม่ฆ่ามอนสเตอร์ | EP2 → EP8 |

---

## 53. แนวทางการวางเชิงโครงสร้าง

### สำหรับนักเขียน:
- ทำสรุปเบาะแสสำคัญของแต่ละบทไว้ใน `epX-README.md`
- ใช้ anomaly หรือ fragment เป็น “จุดตั้งคำถาม” ไม่เฉลยทันที
- เชื่อมโยงด้วยเหตุการณ์ซ้ำหรือเวทที่มีลักษณะผิดปกติ

### สำหรับ AI:
- ก่อนเขียนตอนใหม่ ให้ไล่ย้อน context อย่างน้อย 3 ตอน  
- ค้นหาข้อมูลที่ยัง “ไม่มีคำตอบ” แล้ววางเงื่อนหรือต่อยอด  
- ใส่ metadata กำกับการเชื่อมโยง เช่น `resolved_in`, `appears_in`

---

## 54. Metadata สำหรับการเชื่อมโยงข้ามบท

```yaml
connection:
  appears_in: ep4-18
  resolved_in: ep6-25
  item: fragment-echo
  hint: anomaly-triggered-vision
  character: klein
```

---

การเชื่อมโยงแบบนี้จะทำให้ “ข้อมูลกลายเป็นพลังหลักของเรื่อง”  
และช่วยสร้างเส้นเรื่องที่พัฒนาต่อเนื่องไปจนถึง EP100 ได้อย่างมีชั้นเชิง

---

## 55. วิสัยทัศน์ระยะยาวและสรุปภาพรวม / Long-Term Vision & Final Summary

Farming War เป็นนิยายที่ออกแบบจากระบบขึ้นมาก่อน  
ทุกสิ่งที่เกิดขึ้นในเนื้อเรื่องต้องมี “รากฐานจากข้อมูล” ที่มีการจัดการไว้ใน GitHub

---

## 56. โครงสร้างหลักของโปรเจกต์ (รีวิว)

| ระบบ | จุดเด่น | ใช้ไฟล์ไหน |
|------|---------|------------|
| ตัวละคร | แบ่ง 4 กลุ่ม, ใช้ template | characters/*.md |
| เวทมนตร์ | Echo + Seal เป็นระบบหลัก | magic/epX/*.md |
| เศรษฐกิจ | ผูกกับการฟาร์ม, สินค้า, ความเสี่ยง | worldbuilding/economy.md |
| anomaly | พื้นที่ปั่นป่วน, ปลดล็อกข้อมูล | worldbuilding/anomaly/*.md |
| เควส | ขับเคลื่อนเรื่อง, สร้างทางเลือก | worldbuilding/quests/*.md |

---

## 57. Roadmap การเติบโตของโปรเจกต์

- EP1–10: วางฐานทีม ฟาร์ม ระบบไอเท็ม  
- EP11–40: เริ่มปะทะ Echo และกลุ่มที่เกี่ยวข้องกับผนึก  
- EP41–80: สงครามทรัพยากร, ระบบผนึกแตกเป็นวงกว้าง  
- EP81–99: เผยข้อมูลโลกที่ถูกซ่อนไว้  
- EP100: จุดเปลี่ยนของระบบเวททั้งโลก

---

## 58. การทำงานร่วมกันระหว่าง AI กับนักเขียน

### สำหรับ AI:
- ใช้ context จาก README และ metadata ก่อนแต่งตอนใหม่  
- ระบุให้ชัดว่าอิงจากตอนใด ใช้ตัวละคร/เวท/เควสใด  
- อย่าแต่งข้อมูลใหม่หากไม่มีรากฐานในระบบ

### สำหรับนักเขียน:
- บันทึกทุกข้อมูลใหม่แยกไฟล์ชัดเจน  
- อ้างอิงทุกเวท/เควส/ตัวละครผ่าน README  
- ใช้ template เพื่อให้ AI และนักเขียนอื่นเข้าใจตรงกัน

---

## 59. ปิดท้าย

> *Farming War ไม่ใช่เพียงนิยายแอ็กชันแฟนตาซี  
> แต่คือการทดลองเล่าเรื่องที่ให้ข้อมูลและโครงสร้างเป็นผู้กำหนดโชคชะตา*

ถ้าโลกนี้จะเปลี่ยนแปลง... มันต้องเกิดจากข้อมูลที่ “ไม่เคยถูกบันทึกไว้ในแผนที่ใด”

[END] README.md 15/15
