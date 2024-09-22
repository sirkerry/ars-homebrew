# Advanced Roleplaying System Homebrew

A Foundry VTT module to share ARS data between worlds via compendia.

## Installation

1. Go to the Add-on Modules tab within the FoundryVTT Configuration and Setup page.
2. Click the `Install Module` button.
3. Paste the Module's [Manifest URL](https://github.com/sirkerry/ars-homebrew/releases/latest/download/module.json)
   into the `Manifest URL` field.
4. Click the `Install` button.

| WARNING: If you update this module, FoundryVTT will erase your compendia. |
| ------------------------------------------------------------------------- |

### Preventing Module Update

- Option 1 (easier): Locking your module:
  1. Go to the Add-on Modules tab within the FoundryVTT Configuration and Setup page.
  2. Find this module (ARS Homebrew) in the list, and click the padlock icon.
- Option 2: Updating your `module.json` file:
  1. Go to the Module's installation folder within foundry (`~/Data/modules/ars-homebrew`) and update the `module.json` file.
  2. Remove lines 108-109 (`download` and `manifest`) and save the file.
  3. Restart Foundry to reload the module.

### Unlock your Compendia!

_Remember_ that you need to unlock your compendia to be able to add things to them.

## Default Setup

This module comes with 14 Default compendia:

- `Actors (GM)` ([Actors](https://foundryvtt.com/article/actors/))
- `Actors (PC)` ([Actors](https://foundryvtt.com/article/actors/))
- `Adventures` ([Adventure](https://foundryvtt.com/article/adventure/))    
- `Card` ([Cards](https://foundryvtt.com/article/cards/))
- `Items (GM)` ([Items](https://foundryvtt.com/article/items/))
- `Items (PC)` ([Items](https://foundryvtt.com/article/items/))
- `Journals (GM)` ([JournalEntry](https://foundryvtt.com/article/journal/))
- `Journals (PC)` ([JournalEntry](https://foundryvtt.com/article/journal/))
- `Macros (GM)` ([Macros](https://foundryvtt.com/article/macros/))
- `Macros (PC)` ([Macros](https://foundryvtt.com/article/macros/))
- `Playlists` ([Playlists](https://foundryvtt.com/article/playlists/))
- `Scenes` ([Scenes](https://foundryvtt.com/article/scenes/))
- `Tables (GM)` ([RollTables](https://foundryvtt.com/article/roll-tables/))
- `Tables (PC)` ([RollTables](https://foundryvtt.com/article/roll-tables/))

## Customize

To change the default setup, edit the `module.json` file. All compendia are defined within the "packs" attribute beginning with line 18.

For example:

```json
{
  "packs": [
    {
      "name": "monsters",
      "system": "ars",
      "label": "Monsters",
      "path": "./packs/monsters.db",
      "module": "ars-homebrew",
      "type": "Actor"
    },
    {
      "name": "spells",
      "system": "ars",
      "label": "Spells",
      "path": "./packs/spells.db",
      "module": "ars-homebrew",
      "type": "Item"
    }
  ]
}
```

Note: There are no compendium Types for Classes, Abilities, Actions, and Spells in Foundry, so the `Item` type is generally used for these.

## Dependencies

- [ARS Game System](https://gitlab.com/foundryprojects/systems/advanced-roleplay-system) is required.

