 <!--
type: monster-index
format: markdown-list
fields: name, rank, filename
structure: grouped-by-rank
source: monsters/
auto-parsable: true
-->

 # สารบัญมอนสเตอร์ (Monsters Index)

## วิธีการอัปเดตรายชื่อมอนสเตอร์

เพื่อให้ระบบมอนสเตอร์ในโลกออร์เทียสามารถอ้างอิงได้อย่างถูกต้องและอัตโนมัติ โปรดปฏิบัติตามขั้นตอนต่อไปนี้เมื่อมีการเพิ่มหรือแก้ไขมอนสเตอร์:

### 1. สร้างไฟล์ใหม่
- ตั้งชื่อไฟล์ด้วยรูปแบบ: `[ชื่อมอนสเตอร์]-rank-[ระดับ].md`
  - ตัวอย่าง: `sky-whale-rank-d.md`, `flame-phoenix-rank-a.md`
- ถ้าเป็นเวอร์ชันพิเศษ ให้ต่อท้ายด้วย:
  - `-variant`, `-alpha`, `-mutated`, `-prime`, `-echo` หรืออื่น ๆ ที่อธิบายลักษณะได้ชัดเจน
  - ตัวอย่าง: `shadow-cat-variant-rank-c.md`

### 2. วางไฟล์ไว้ในโฟลเดอร์ `monsters/`
- ไม่ต้องแยกโฟลเดอร์ย่อยตาม Rank
- ให้ทุกไฟล์อยู่ใน `monsters/` เดียวกันเพื่อความสะดวกในการค้นหาและจัดการ

### 3. เพิ่มชื่อไฟล์ในสารบัญ
- เปิดไฟล์ `monsters-README.md`
- ไปยังหัวข้อ Rank ที่เหมาะสม (Rank D, C, B, A หรือ พิเศษ)
- เพิ่มบรรทัดใหม่ในรูปแบบ:

### 4. ตรวจสอบลำดับตัวอักษร
- เรียงลำดับชื่อภายในแต่ละ Rank จาก A ถึง Z
- เพื่อให้ง่ายต่อการค้นหาและบำรุงรักษา

### 5. Commit การเปลี่ยนแปลง
- เขียนข้อความ commit ให้สื่อความหมาย เช่น:
- `เพิ่มมอนสเตอร์ใหม่: sky-whale-rank-d.md`
- `อัปเดตสารบัญ monsters-README.md`

### หมายเหตุ
- หากมีมอนสเตอร์ที่ยังไม่กำหนด Rank สามารถใช้ `rank-x` ชั่วคราวได้ เช่น `monster-name-rank-x.md`
- ควรอัปเดต README ทุกครั้งหลังมีการเพิ่มไฟล์ เพื่อให้ AI และผู้ร่วมพัฒนาเข้าถึงข้อมูลได้ทันที

มอนสเตอร์ทั้งหมดในโลกออร์เทีย จัดเรียงตามระดับ (Rank) และชื่อไฟล์

---

## Rank A
- [flame-phoenix-rank-a.md](flame-phoenix-rank-a.md)
- [sea-serpent-rank-a.md](sea-serpent-rank-a.md)
- [tempest-lord-rank-a.md](tempest-lord-rank-a.md)

---

## Rank B
- [asmolith-rank-b.md](asmolith-rank-b.md)
- [astral-hawk-rank-b.md](astral-hawk-rank-b.md)
- [crystal-tornado-rank-b.md](crystal-tornado-rank-b.md)
- [desert-medusa-rank-b.md](desert-medusa-rank-b.md)
- [hexsels-rank-b.md](hexsels-rank-b.md)
- [illusio-rank-b.md](illusio-rank-b.md)
- [luminaklein-rank-b.md](luminaklein-rank-b.md)
- [magnus-mana-rank-b.md](magnus-mana-rank-b.md)
- [mist-kirin-rank-b.md](mist-kirin-rank-b.md)
- [paladin-soul-rank-b.md](paladin-soul-rank-b.md)
- [phoenix-fighter-rank-b.md](phoenix-fighter-rank-b.md)
- [venomous-eye-rank-b.md](venomous-eye-rank-b.md)

---

## Rank C
- [ancient-mossbear-rank-c.md](ancient-mossbear-rank-c.md)
- [arcane-mosslurker-rank-c.md](arcane-mosslurker-rank-c.md)
- [blackbloom-vine-rank-c.md](blackbloom-vine-rank-c.md)
- [blackflora-weaver-rank-c.md](blackflora-weaver-rank-c.md)
- [bloom-avenger-rank-c.md](bloom-avenger-rank-c.md)
- [blueroot-bear-rank-c.md](blueroot-bear-rank-c.md)
- [chronbee-of-venomdew-rank-c.md](chronbee-of-venomdew-rank-c.md)
- [crestling-rank-c.md](crestling-rank-c.md)
- [crystal-muse-rank-c.md](crystal-muse-rank-c.md)
- [crystal-rockworm-rank-c.md](crystal-rockworm-rank-c.md)
- [crystallink-rank-c.md](crystallink-rank-c.md)
- [crystalroot-maw-rank-c.md](crystalroot-maw-rank-c.md)
- [crystol-rank-c.md](crystol-rank-c.md)
- [ember-sylph-rank-c.md](ember-sylph-rank-c.md)
- [felthena-rank-c.md](felthena-rank-c.md)
- [flame-lurker-rank-c.md](flame-lurker-rank-c.md)
- [florrentree-rank-c.md](florrentree-rank-c.md)
- [forest-golem-rank-c.md](forest-golem-rank-c.md)
- [lumeneer-mirage-rank-c.md](lumeneer-mirage-rank-c.md)
- [mimic-harmony-rank-c.md](mimic-harmony-rank-c.md)
- [mist-hunter-rank-c.md](mist-hunter-rank-c.md)
- [mistfang-serpent-rank-c.md](mistfang-serpent-rank-c.md)
- [mosswolf-rank-c.md](mosswolf-rank-c.md)
- [shade-of-raka-rank-c.md](shade-of-raka-rank-c.md)
- [shadow-cat-rank-c.md](shadow-cat-rank-c.md)
- [shadow-crawler-rank-c.md](shadow-crawler-rank-c.md)
- [silvershadow-luma-rank-c.md](silvershadow-luma-rank-c.md)
- [sorenmoth-rank-c.md](sorenmoth-rank-c.md)
- [soulroot-creeper-rank-c.md](soulroot-creeper-rank-c.md)
- [stinestinger-rank-c.md](stinestinger-rank-c.md)
- [thornlurker-rank-c.md](thornlurker-rank-c.md)
- [voidmoth-rank-c.md](voidmoth-rank-c.md)
- [warp-spore-rank-c.md](warp-spore-rank-c.md)
- [whispering-fox-rank-c.md](whispering-fox-rank-c.md)
- [whisperwood-rank-c.md](whisperwood-rank-c.md)
- [witherbloom-rank-c.md](witherbloom-rank-c.md)

---

## Rank D
- [blaze-bee-rank-d.md](blaze-bee-rank-d.md)
- [boom-mushroom-rank-d.md](boom-mushroom-rank-d.md)
- [electric-frog-rank-d.md](electric-frog-rank-d.md)
- [fire-lizard-rank-d.md](fire-lizard-rank-d.md)
- [flame-slime-rank-d.md](flame-slime-rank-d.md)
- [frost-serpent-rank-d.md](frost-serpent-rank-d.md)
- [giant-cockroach-rank-d.md](giant-cockroach-rank-d.md)
- [moonlight-sprite-rank-d.md](moonlight-sprite-rank-d.md)
- [rock-turtle-rank-d.md](rock-turtle-rank-d.md)
- [shadow-rat-rank-d.md](shadow-rat-rank-d.md)
- [shadowmoth-rank-d.md](shadowmoth-rank-d.md)
- [sky-whale-rank-d.md](sky-whale-rank-d.md)
- [snow-wolf-rank-d.md](snow-wolf-rank-d.md)
- [thunderbird-rank-d.md](thunderbird-rank-d.md)
- [toxic-dragonfly-rank-d.md](toxic-dragonfly-rank-d.md)
- [venom-spider-rank-d.md](venom-spider-rank-d.md)

---

## อื่น ๆ
- [monster-name-rank-x.md](monster-name-rank-x.md) *(ไฟล์เทมเพลตหรือยังไม่กำหนด Rank)*