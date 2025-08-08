# Contributing to Elden Ring Nightreign Lorebook

Thank you for your interest in improving the Nightreign lorebook collection! As this is a rapidly evolving game with regular updates, community contributions are essential.

## How to Contribute

### Reporting Issues
- Verify information against current game version (post-August 2025)
- Check if the issue exists in latest release
- Provide specific entry name and file
- Include source (patch notes, in-game text, official announcements)

### Adding Content
New entries must:
1. Be from verified Nightreign sources only
2. Follow the existing JSON format exactly
3. Include appropriate keywords for AI triggering
4. Avoid duplicating existing entries
5. Distinguish from base Elden Ring content

### JSON Format
```json
{
  "uid": [unique_number],
  "key": ["primary_keyword", "alternate_name"],
  "content": "**Name**\\nType: Category | Additional Info\\nDescription here...",
  "group": "Nightfarers|Nightlords|Mechanics|Items|Locations",
  "order": 100,
  "depth": 4
}
```

### Pull Request Process
1. Fork the repository
2. Create a feature branch (`git checkout -b add-gladius-nightlord`)
3. Make your changes
4. Test in SillyTavern
5. Update entry count in README if needed
6. Commit with clear message
7. Push and open PR

### Nightreign-Specific Sources
Acceptable:
- In-game Nightreign text and dialogue
- Official patch notes and announcements
- Network test information (marked as such)
- Everdark Sovereign event details

Not acceptable:
- Base Elden Ring lore (use main repo)
- Speculation without marking
- Leaked/datamined content
- Fan theories as fact

### Content Guidelines
- Mark expedition-specific mechanics clearly
- Include synergies between Nightfarers
- Note which content requires unlocking
- Specify Everdark vs standard versions
- Include three-day cycle context

## Testing
Before submitting:
1. Validate JSON syntax
2. Import to SillyTavern successfully
3. Check token usage (aim for <100 per entry)
4. Verify keywords trigger appropriately

## Questions?
Open an issue labeled "question" for clarification.

Thank you for helping the Nightreign community!