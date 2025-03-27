
<!--
context-index: context-ai-index.yaml
template-index: templates/template-index.yaml
validate-schemas: schemas/
auto-parsable: true
project-type: worldbuilding+novel+ai
version: 1.0
-->

# Farming War – Project Overview

This repository contains the structured worldbuilding system, characters, quests, magic system, and serialized episodes for the novel **Farming War**.  
It is designed to support advanced AI-based tools for writing, validation, auto-generation, and creative collaboration.

---

## 🗂 Project Structure (โครงสร้างหลักของโปรเจกต์)

- `story/` – Main episodes, chapters, and serialized content
- `characters/` – Character profiles grouped by team, NPC, enemy, etc.
- `magic/` – Magic spells categorized by EP and class
- `quests/` – Quest system and side missions
- `worldbuilding/` – Locations, factions, economy, etc.
- `monsters/` – Bestiary grouped by rank
- `templates/` – Authoring templates (character, magic, quest, structure)
- `schemas/` – Schema validation files for each type
- `dev/` – Development plans, internal notes, draft structure
- `context-ai-index.yaml` – Master file for AI context linking
- `context-ai-checklist.yaml` – Progress tracker for AI-ready content

---

## ✅ AI Context Usage (การทำให้ AI เข้าใจโครงสร้างนี้ได้)

This repository includes:

- ✔️ AI-parsable README files with metadata anchors
- ✔️ Index YAML files (magic, quest, character, structure)
- ✔️ Anchors to templates and schema validation
- ✔️ Predictable file/folder structure
- ✔️ Cross-reference capabilities between characters, spells, and quests

With `context-ai-index.yaml`, AI can traverse the whole world model from any entry point.

---

## 🔄 Update Process (การอัปเดต)

- Add new content using appropriate templates under `templates/`
- Update relevant index files: e.g. `characters-index.yaml`
- Ensure metadata block and anchors are present in all README files
- Validate with corresponding schema in `schemas/`

---

## 🔗 Index & Metadata Files

- [`context-ai-index.yaml`](context-ai-index.yaml)
- [`context-ai-checklist.yaml`](context-ai-checklist.yaml)
- [`characters-index.yaml`](characters-index.yaml)
- [`magic-index.yaml`](magic-index.yaml)
- [`quest-index.yaml`](quest-index.yaml)
- [`validate-schema-character.yaml`](schemas/validate-schema-character.yaml)
- [`validate-schema-magic.yaml`](schemas/validate-schema-magic.yaml)
- [`validate-schema-quest.yaml`](schemas/validate-schema-quest.yaml)

---

This repository is actively developed and AI-augmented for long-term worldbuilding and storytelling.

