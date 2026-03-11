⚡ QUICKSTART.md (Updated)
markdown
# EQ‑5e AI Module – Quickstart Guide

## 1. Install the Module

1. Open **Foundry VTT → Add-on Modules → Install Module**.
2. Paste the manifest URL:

https://raw.githubusercontent.com/Mirloc608/eq5e-ai-module/main/module.json (raw.githubusercontent.com in Bing)

Code

3. Install and enable **EQ‑5e AI Module** in your world.

---

## 2. Enable the AI Compendiums

The module provides the following packs:

- EQ AI Core  
- EQ AI Combat Packs  
- EQ AI Social  
- EQ AI Factions & Kingdoms  
- EQ AI World Simulation  
- EQ AI Dungeons  
- EQ AI NPC Templates  

You may use them as compendiums or import them into your world.

---

## 3. Add Combat AI to an NPC

Add this to an NPC’s flags or system data:

```json
"aiProfile": {
"role": "caster",
"personality": "disciplined",
"tacticProfile": "kite_and_burn",
"classProfile": "wizard",
"awareness": "observant"
}
4. Add Social AI
json
"aiSocial": {
  "tactic": "patrol_route_guard",
  "personality": "stoic",
  "awareness": "observant",
  "scriptHooks": "default_social_hooks"
}
5. Tag Zones with Ecology Profiles
Scenes can be tagged with:

json
"ecologyProfile": "forest_ecology"
This activates wildlife, weather, and ambient behavior.

6. Start Small
Recommended first steps:

Assign AI to 2–3 NPCs

Enable one zone ecology

Enable one dungeon ecosystem

Add emotional + memory systems

Then expand into kingdoms, warfare, and world simulation.
