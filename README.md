# qb-factory Script

The **qb-factory** script is a crafting and selling system for the **QBCore Framework**. It allows players with the **factory job** to craft items, sell goods, and utilize custom stash systems. Designed with flexibility and customization in mind, it offers configurable crafting recipes, crafting tables, stash locations, and other features.

---

## Features

- **Crafting System**:
  - Craft various items with defined recipes and success percentages.
  - Items require specific ingredients, time, and player XP levels to craft.
  - Supports crafting tables with individual configurations and recipes.

- **XP System** (Optional):
  - Players gain XP upon successful or failed crafting.
  - Configurable XP values, levels, and level multipliers.

- **Blips and Markers**:
  - Configurable crafting blips and floor markers.

- **Stash System**:
  - Custom stashes for fruits, vegetables, meats, and packed goods.
  - Configurable stash weight and slots.

- **Target Zones**:
  - Interact with crafting tables and stashes using target zones defined by **st-target**.

- **Highly Configurable**:
  - Easily adjust settings such as crafting locations, item recipes, XP system, and blips through the `config.lua` file.

---

## Installation

### Requirements

- **QBCore Framework**
- **okokTextUI** (Optional, for optimized UI notifications)
- **st-target** (For target zones)

### Steps

1. **Download and Install**:
   - Place the `qb-factory` folder into your server's **resources** directory.

2. **Add to Server Config**:
   - Add `ensure qb-factory` to your `server.cfg` file.

3. **Dependencies**:
   - Ensure `st-target` and `qb-core` are correctly installed and configured.

4. **Configure**:
   - Open `config.lua` and adjust the settings to your preference:
     - Toggle options such as `UseOkokTextUI`, `ShowBlips`, `UseXP`, etc.
     - Configure crafting recipes and tables.
     - Adjust stash locations and settings.

---

## Configuration

### `config.lua` Key Settings

### Crafting Tables Example
```lua
Config.UseOkokTextUI = true  -- Use okokTextUI for optimized notifications.
Config.Key = 38              -- Interaction key (Default: [E]).
Config.HideMinimap = true    -- Hide minimap when crafting menu is open.
Config.ShowBlips = false     -- Toggle crafting blips on the map.
Config.UseXP = false         -- Enable or disable XP system.

```lua
Config.CraftingTables = {
    {
        coordinates = vector3(1228.15, -3305.0, 5.5),
        radius = 0.5,
        tableName = 'Sack Table',
        crafts = {
            {
                item = 'advancedlockpick',
                amount = 1,
                recipe = {
                    {'plastic', 1, true},
                    {'lockpick', 1, true},
                },
                successCraftPercentage = 75,
                time = 3,
                xpPerCraft = 15,
                job = { 'factory' },
            },
        },
    },
}
```
### Stash Example
```lua
AddEventHandler("qb-factory:Client:Stash01", function()
    local other = {}
    other.maxweight = 40000000 -- Stash weight.
    other.slots = 50          -- Stash slots.
    TriggerServerEvent("inventory:server:OpenInventory", "stash", "Fruits_Stash", other)
    TriggerEvent("inventory:client:SetCurrentStash", "Fruits_Stash")
end)
```
### Depedency
- `qb-core`
- `okokTextUI`
- `qb-target`


## Usage

### Crafting
1. Approach a crafting table location.
2. Press the interaction key (default: **[E]**).
3. Select the item you want to craft from the menu.
4. Ensure you have the required materials in your inventory.

### Stash Interaction
1. Approach a stash location.
2. Press the interaction key (default: **[E]**).
3. Access the stash to store or retrieve items.

## Adding New Items or Recipes
1. Open `config.lua`.
2. Add a new entry under `Config.Crafting` for crafting tables or `Config.itemNames` for new items.
3. Reload the resource or restart the server.

## Commands & Events

### Events
- `qb-factory:Client:Stash01` - Opens the Fruits Stash.
- `qb-factory:Client:Stash02` - Opens the Vegetables Stash.
- `qb-factory:Client:Stash03` - Opens the Meat Aliments Stash.
- `qb-factory:Client:Stash04` - Opens the Packed Fruits Stash.
- `qb-factory:Client:Stash05` - Opens the Packed Vegetables Stash.

## Notes
- Ensure the factory job is added to your QBCore job configuration.
- If using the XP system, adjust `MaxLevel`, `StartEXP`, and `LevelMultiplier` according to your server's progression style.
- Test crafting recipes and stash interactions after configuration to ensure they work as intended.

## Support
For issues or questions, contact me on GitHub or open an issue in the [GitHub repository](https://github.com/louairgh) for additional assistance.
