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

Code

---

# 🧠 **DEVELOPER_GUIDE.md (Updated)**

```markdown
# EQ‑5e AI Module – Developer Guide

## 1. Philosophy

The AI system is:

- Modular  
- Data-driven  
- Extensible  
- EQ-flavored but not tied to copyrighted content  
- Designed for simulation-first gameplay  

---

## 2. Extending Combat AI

### Add a new tactic

Edit `packs/eq-ai-combat-packs.json`:

```json
{
  "name": "hit_and_run",
  "system": {
    "positioning": "ranged",
    "priority": ["burst_damage", "retreat", "reposition"]
  }
}
3. Extending Monster AI
Add a species pack:

json
{
  "name": "monster_ai_pack_bat",
  "system": {
    "species": "bat",
    "instincts": { "swarm": true },
    "combatBehavior": {
      "openers": ["sonic_shriek"],
      "coreLoop": ["bite", "dive"],
      "finishers": ["swarm_overwhelm"]
    }
  }
}
4. Extending Social AI
Add a personality:

json
{
  "name": "jovial",
  "system": {
    "greetingStyle": "warm",
    "gossipLikelihood": 0.9
  }
}
5. Extending World Simulation
Add a new ecology:

json
{
  "name": "desert_ecology",
  "system": {
    "wildlife": { "scorpions": { "spawnRate": "medium" } },
    "weatherEffects": { "sandstorm": ["reduce_visibility"] }
  }
}
6. Versioning
Use semantic versioning

Update CHANGELOG.md

Tag releases in GitHub

Keep JSON packs append-only when possible

7. Integration Notes
Use flags.eq5e-ai.* for storing AI data

Keep all logic data-driven

Use examples/ as a sandbox
