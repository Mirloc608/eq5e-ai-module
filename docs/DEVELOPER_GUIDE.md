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
