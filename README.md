# Farming War - Story Project

## Overview
This project contains the story, characters, world-building, magic, and items for the **Farming War** novel. It is organized into structured folders for easy navigation and understanding.

## Folder Structure:
- **/project** - The main folder containing story and world-building content
  - **/worldbuilding** - Locations, magic, and lore of the world.
  - **/characters** - Information about characters, NPCs, and monsters.
  - **/magic** - Magic spells, abilities, and systems.
  - **/items** - Various items used in the story.
  - **/story** - The chapters of the story, organized by episodes.

## Steps for Creating New Content
1. Check the progress of the project in **project-status.md**.
2. Review the chapter structure in **/dev**.
3. Check the current episode and previous chapters in **/story**.
4. Verify the items, magic, and quests in **/items**, **/magic**, and **/quests**.
5. Review world-building information in **/worldbuilding**.
6. Plan and create documents for the next episode.

## Contribution
This is an ongoing solo project by the author. Please feel free to explore, provide suggestions, or use this repository for reference. 

## 🧠 Context for AI and Human Collaborators

- [context-ai.md](./context-ai.md) — for AI models (English)


# Farming War – GitHub Worldbuilding Project

> โปรเจกต์นี้เป็นโครงสร้างนิยายแฟนตาซี “Farming War”  
> ที่เน้นการล่ามอนสเตอร์, คราฟต์ของ, วางกลยุทธ์ และสร้างโลกแบบมีระบบ  
> จัดวางข้อมูลทั้งหมดด้วยโฟลเดอร์และ Markdown เพื่อรองรับนิยายระดับหลายร้อยตอน


# Farming War: โปรเจกต์เขียนนิยายแฟนตาซีเชิงระบบ

โปรเจกต์นี้คือระบบจัดการข้อมูลสำหรับนิยายเรื่อง **Farming War** ซึ่งเป็นนิยายแฟนตาซีที่เน้นการล่ามอนสเตอร์, การสร้างฟาร์ม, การค้า, การเมือง และการสร้างไอเท็มในโลกแฟนตาซียุคกลางชื่อว่า **ออร์เทีย (Orthia)**

ข้อมูลทั้งหมดใช้รูปแบบ Markdown text เพื่อความเรียบง่าย ค้นหาง่าย และรองรับการใช้งานบน Git ได้ในระยะยาว

---

## โครงสร้างโฟลเดอร์หลัก

```plaintext
project/
├── story/                  ← ตอนนิยาย แบ่งเป็น ep1/, ep2/, ep3/
├── characters/             ← ตัวละครหลัก แบ่งเป็น silent-fortune/, npc/, enemy/
├── monsters/               ← มอนสเตอร์ แบ่งตามระดับหรือพื้นที่ เช่น forest/, shadowrift/
├── worldbuilding/          ← ระบบโลก เช่น เวทมนตร์, ประเทศ, วัฒนธรรม
│   ├── locations/
│   ├── factions/
│   ├── magic-system/
│   ├── economy-and-politics/
│   ├── cultures/
│   └── maps/
├── items/                  ← รายการไอเท็มทั้งหมด (อยู่ระหว่างพัฒนา)
├── quests/                 ← ระบบเควสต์ แยกตามบท
├── teams/                  ← ทีม Silent Fortune และพันธมิตร
├── dev/                    ← ไฟล์วางแผนภายใน เช่น ep3-structure.md
└── templates/              ← แม่แบบ เช่น WSP-Character-Intro.md

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
