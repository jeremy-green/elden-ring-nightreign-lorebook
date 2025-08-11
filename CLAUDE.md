# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the Elden Ring Nightreign lorebook collection - a curated set of 70 lorebook entries for the standalone co-op roguelike spinoff. The project contains production-ready JSON lorebooks for use with SillyTavern and similar AI roleplay platforms.

## Project Structure

```
elden-ring-nightreign-lorebook/
├── lorebooks/                          # Production-ready lorebook files
│   ├── nightreign_characters.json     # 16 entries - Nightfarers & NPCs
│   ├── nightreign_bosses_enemies.json # 19 entries - Nightlords & enemies
│   ├── nightreign_mechanics.json      # 14 entries - Game systems
│   ├── nightreign_locations.json      # 10 entries - Limveld areas
│   ├── nightreign_items.json          # 11 entries - Equipment & relics
│   └── nightreign_master_complete.json # 70 entries - Complete collection
└── Documentation/
    ├── README.md                       # Primary documentation
    ├── QUICK_START.md                  # Usage guide
    └── CONTRIBUTING.md                 # Contribution guidelines
```

## Validation Commands

### JSON Syntax Validation
```bash
# Validate all lorebook files
python3 -c "import json, glob; [print(f'✓ {f}: {len(json.load(open(f))[\"entries\"])} entries') for f in glob.glob('lorebooks/*.json')]"

# Verify total entry count (should be 70)
python3 -c "import json; print(f'Total entries: {sum([len(json.load(open(f))[\"entries\"]) for f in glob.glob(\"lorebooks/nightreign_*.json\") if \"master\" not in f])}')"
```

### Token Usage Analysis
```bash
# Estimate token usage per lorebook
python3 -c "import json; [print(f'{f.split(\"/\")[-1]}: ~{sum(len(e[\"content\"]) for e in json.load(open(f))[\"entries\"].values())//4} tokens') for f in glob.glob('lorebooks/*.json')]"
```

### Duplicate Detection
```bash
# Check for duplicate UIDs across files
python3 -c "import json, glob; uids = []; [uids.extend([(f, uid) for uid in json.load(open(f))['entries'].keys()]) for f in glob.glob('lorebooks/*.json')]; dupes = [x for x in uids if uids.count(x) > 1]; print('No duplicates' if not dupes else f'Duplicates found: {dupes}')"
```

## Lorebook Entry Structure

Standard SillyTavern World Info format:
```json
{
  "uid": "unique_integer_as_string",
  "key": ["primary_keyword", "alternate_keywords"],
  "content": "Rich markdown content with lore",
  "group": "Category_Name",
  "order": 100,
  "depth": 4,
  "probability": 100,
  "selective": true,
  "secondary_keys": [],
  "position": "before_char",
  "displayIndex": display_order
}
```

### Content Categories
- **Nightfarers** - 8 playable characters with abilities
- **NPCs** - Supporting characters (Solitary, Rime Witch)
- **Nightlords** - Boss entities and Everdark Sovereigns
- **Nightreign Mechanics** - Three-day cycle, Night's Tide
- **Nightreign Regions** - Limveld and corrupted landmarks
- **Nightreign Items** - Relics, currencies, equipment

## Working with Content

### Adding New Entries
1. Choose the appropriate category file
2. Use sequential UID numbering within each file
3. Include both formal names and common variations in keywords
4. Keep content canon-based (from official sources)
5. Optimize for 150-200 tokens per entry maximum
6. Update entry counts in README.md after changes

### Content Standards
- Rich atmospheric descriptions with environmental details
- Character entries must include abilities and personality
- Boss entries include combat mechanics and lore significance
- Location entries emphasize the parallel dimension aspects
- Use markdown formatting for structure and emphasis

### Token Optimization Guidelines
- Individual lorebooks: Target 600-800 active tokens
- Master lorebook: 2,000+ tokens (requires large context)
- Never load more than 3 lorebooks simultaneously
- Use specific keywords to minimize false triggers

## Testing

### SillyTavern Import Testing
1. Import lorebook into SillyTavern World Info
2. Configure: Scan Depth 4, Token Budget 800-1200
3. Test keyword triggers with sample prompts
4. Monitor actual token usage during roleplay

### Entry Validation Checklist
- [ ] Valid JSON syntax
- [ ] Unique UID within file
- [ ] Keywords include variations
- [ ] Content is canon-accurate
- [ ] Group name matches category
- [ ] Standard metadata (depth: 4, probability: 100)

## Important Notes

- This is a content repository with no build scripts or processing pipeline
- All lorebooks are production-ready and manually curated
- Content is based on official Elden Ring Nightreign sources
- The master_complete.json contains all 70 entries combined
- Entry counts in README.md must be updated when adding content
- Token estimates use the rough formula: characters/4 = tokens