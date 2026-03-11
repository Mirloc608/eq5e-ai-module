EQ‑5e AI Module
A Modular, Extensible World‑Simulation Engine for Foundry VTT
The EQ‑5e AI Module is a comprehensive, drop‑in artificial intelligence framework designed to bring a living, reactive, simulation‑driven world to your EQ‑5e Foundry VTT system.
It provides combat intelligence, social behavior, emotional modeling, memory, reputation, faction politics, kingdom simulation, dungeon ecosystems, monster ecology, weather, economy, and procedural generation — all in a modular, extensible format.

This module does not include any copyrighted EverQuest content.
Instead, it provides a generic, EQ‑flavored AI architecture that you can map to your own custom data.

📦 Module Overview
The AI system is divided into several drop‑in JSON packs:

File	Description
eq-ai-core.json	Core roles, personalities, awareness profiles
eq-ai-combat-packs.json	Combat tactics, class profiles, monster AI packs, behavior trees
eq-ai-social.json	Social behavior, emotions, memory, reputation, dialogue
eq-ai-factions-kingdoms.json	Factions, politics, diplomacy, kingdom simulation, warfare
eq-ai-world-sim.json	Economy, weather, event chains, zone ecology, settlement simulation
eq-ai-dungeons.json	Dungeon ecosystems, biome packs, procedural dungeon generator
eq-ai-npc-templates.json	Example NPC templates demonstrating full AI integration
Each file is fully modular — you can enable or disable entire layers depending on your campaign needs.

✨ Key Features
🧠 1. Combat AI
Role‑based behavior (tank, caster, healer, melee DPS, ranged DPS)

Class‑aware ability rotations

Monster species AI packs

Hierarchical behavior trees

Pack coordination, ambush logic, flanking, fear responses

🎭 2. Social AI
Idle loops, gossip clusters, patrol routes, rituals

Social personalities (friendly, stoic, skittish, hostile)

Social awareness (observant, oblivious, militant)

Dynamic dialogue based on emotion, faction, reputation, and events

🌡 3. Emotional State Engine
Calm, alert, afraid, angry, panicked, enraged

Emotional decay and escalation

Behavior overrides based on emotional state

🧠 4. Memory & Reputation
Short‑term, mid‑term, and long‑term memory

Personal reputation separate from faction standing

NPCs remember crimes, kindness, quests, and interactions

⚖️ 5. Crime & Justice
Crime detection (theft, assault, murder, trespassing)

Guard response logic (warn, arrest, attack)

Justice outcomes (fines, jail, execution)

🏘 6. Settlement Simulation
Jobs, needs, schedules, social networks

Work cycles, sleep cycles, festivals, panic events

Resource production and consumption

🌍 7. Zone Ecology
Wildlife behavior

Weather effects

Day/night cycles

Ambient events

Faction presence

🧬 8. Monster Ecology
Predator/prey relationships

Territorial behavior

Seasonal behavior

Species interactions

🕳️ 9. Dungeon Ecosystems
Food chains, lairs, patrols, hazards

Dynamic events (cave‑ins, spore blooms, boss awakenings)

Territorial logic and migration

🌋 10. Dungeon Biome Packs
Ice caverns, lava forges, fungal warrens, void rifts, etc.

Biome‑specific hazards, traps, species, events

👑 11. Kingdom Simulation
Economy, military, diplomacy, politics, stability

Internal factions (military, merchants, priests, rebels)

Succession crises, coups, rebellions

⚔️ 12. Kingdom Warfare Engine
Armies, battles, raids, sieges, ambushes

Terrain and weather modifiers

Morale, logistics, attrition

🔗 13. Event Chains
Multi‑stage dynamic events

Local, regional, and global arcs

Player‑triggered and simulation‑driven events

🧱 14. Procedural Dungeon Generator
Layout, rooms, corridors, special chambers

Ecosystem‑driven population

Biome integration

Trap and hazard generation

🧩 Integration
NPCs can be assigned AI via:

json
"aiProfile": {
  "role": "caster",
  "personality": "disciplined",
  "tacticProfile": "kite_and_burn",
  "classProfile": "wizard",
  "awareness": "observant"
}
Social AI:

json
"aiSocial": {
  "tactic": "patrol_route_guard",
  "personality": "stoic",
  "awareness": "observant",
  "scriptHooks": "default_social_hooks"
}
World simulation layers are automatically referenced by:

Zone tags

Faction tags

Kingdom tags

Dungeon biome tags

🛠 Customization
You can:

Add new roles, personalities, tactics

Create new monster species packs

Build custom dungeon biomes

Add new factions, kingdoms, political events

Extend dialogue packs

Override any behavior per NPC

Everything is JSON‑driven and designed for modular patching.

⚠️ Legal Note
This module contains no copyrighted EverQuest content.
It is a generic AI simulation framework designed to be compatible with EQ‑style gameplay when paired with your own custom data.

You are responsible for mapping your own NPCs, factions, zones, and dungeons.

📄 License
You can choose MIT, GPL, or a custom license depending on how open you want the system to be.

🚀 Roadmap
AI Narrative Director

AI Quest Generator

AI Monster Evolution System

AI Dungeon Mutation System

AI Kingdom History Generator

AI Weather‑Driven Encounter Director