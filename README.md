# 🌙 Elden Ring Nightreign Lorebook Collection for SillyTavern

A comprehensive lorebook collection for Elden Ring Nightreign roleplay and storytelling in SillyTavern, featuring 70 meticulously crafted entries covering the standalone co-op roguelike game.

> **Looking for the main game?** Check out our [Elden Ring Lorebook Collection](https://github.com/jeremy-green/elden-ring-lorebook) with 1,200+ entries for the base game and DLC.

## ✨ Features

- **70 Curated Entries** covering all Nightfarers, Nightlords, and mechanics
- **Roguelike Focus** optimized for expedition-based storytelling
- **Co-op Emphasis** with team synergy information
- **Complete Coverage** through August 2025 updates including Everdark Sovereigns
- **Token Optimized** with smart categorization to prevent bloat

## 📦 Quick Start

### Installation
1. Download the lorebook files you need from the `lorebooks/` folder
2. In SillyTavern, go to World Info → Import
3. Select the downloaded JSON file(s)
4. Configure settings (see below)

### Recommended Settings
```
Search Depth: 3-4 messages
Token Budget: 600-800 per lorebook
Recursive Scanning: ON
Case Sensitive: OFF
```

## 📚 Available Lorebooks

| File | Entries | Description | Best For |
|------|---------|-------------|----------|
| **nightreign_master_complete.json** | 70 | Everything in one file (use with caution) | Large context models |
| **nightreign_characters.json** | 16 | All 8 Nightfarers + NPCs | Character interactions |
| **nightreign_bosses_enemies.json** | 19 | Nightlords + Everdark Sovereigns | Boss encounters |
| **nightreign_mechanics.json** | 14 | Game systems, endings, Night's Tide | Understanding mechanics |
| **nightreign_locations.json** | 10 | Limveld areas and landmarks | Exploration RP |
| **nightreign_items.json** | 11 | Relics, equipment, currencies | Loot and progression |

## 🎮 Usage Examples

### Three-Day Expedition
Load: `nightreign_characters` + `nightreign_bosses_enemies` + `nightreign_mechanics`

### Nightfarer Team Dynamics
Load: `nightreign_characters` + `nightreign_items` + `nightreign_locations`

### Boss Hunt Focus
Load: `nightreign_bosses_enemies` + `nightreign_mechanics`

### Character Backstory
Load: `nightreign_characters` + `nightreign_locations`

## 💡 Tips

- **Never load more than 3 lorebooks** simultaneously
- **The master file** should only be used with 8k+ context models
- **Switch lorebooks** as your expedition progresses through days
- **Remember:** This is a roguelike, not a souls-like

## 🔧 Token Management

Each split lorebook uses 600-800 tokens when active. The complete version can use 2000+ tokens and requires models with large context windows.

## 📊 What's Included

### Characters
- ✅ All 8 playable Nightfarers with unique abilities
- ✅ NPC allies and the Priestess/Duchess
- ✅ Character personalities and synergies
- ✅ Remembrance quest information

### Bosses & Enemies
- ✅ All Nightlords including Morgott and Gladius
- ✅ Heolstor, the Night Aspect (final boss)
- ✅ 5 Everdark Sovereign variants
- ✅ Shadow enemies and Tide Spawn

### Game Systems
- ✅ Three-day expedition structure
- ✅ Night's Tide shrinking map mechanic
- ✅ Co-op revival system
- ✅ Three endings (Dawn, Endless Night, New Night)

### Content Updates
- ✅ Everdark Sovereign rotation system
- ✅ Sovereign Sigils and rewards
- ✅ Duo Mode information
- ✅ Post-launch content through August 2025

## ⚠️ Important Note

**Keep these separate from main Elden Ring lorebooks!** Nightreign uses fundamentally different mechanics:
- Roguelike vs Souls-like
- 3-player co-op vs solo focus
- Expeditions vs open exploration
- Nightfarers vs Tarnished

## 🤝 Contributing

Found an error or want to add new content? We welcome contributions!

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on:
- Adding new entries
- Reporting issues
- Updating for new patches
- Maintaining canon accuracy

## ⚖️ License

MIT License - Free for any use

## ⚠️ Disclaimer

This is a fan-made project for the Elden Ring Nightreign community. It is not affiliated with, endorsed by, or connected to FromSoftware or Bandai Namco Entertainment.

## 🙏 Acknowledgments

- FromSoftware for creating Elden Ring Nightreign
- The Nightreign community for exploration and discovery
- Contributors who help keep this updated
- SillyTavern developers for the amazing platform

---

*"As Night Falls, We Rise"*

**Version**: 1.1.0  
**Last Updated**: August 2025  
**Total Entries**: 70  
**Game Version**: 1.3.0 (Everdark Sovereigns Update)