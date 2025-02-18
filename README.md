# **qb-factoryjob**

A fully customizable factory job script for the **QBCore** framework, allowing players to craft items, manage stashes, gain XP, and level up their crafting skills.

---

## **Features**
- 🛠 **Advanced Crafting System**: Craft items using custom recipes and earn XP.
- 📈 **XP & Leveling System**: Configurable XP multipliers and max levels.
- 📦 **Stash Management**: Store raw materials, tools, and finished products in different stashes.
- 🎯 **qb-target Integration**: Easily interact with stashes and crafting stations.
- ⚙️ **Highly Configurable**: Customize crafting, XP settings, job restrictions, and stash properties.

---

## **Dependencies**
- [**qb-core**](https://github.com/qbcore-framework/qb-core) - Core framework.
- [**qb-target**](https://github.com/qbcore-framework/qb-target) - Interaction system.
- [**qb-inventory**](https://github.com/qbcore-framework/qb-inventory) - Inventory management.

---

## **Installation**
1. Download `qb-factoryjob` and place it in the `resources` folder.
2. Add this line to `server.cfg`:
   ```lua
   ensure qb-factoryjob
   ```
3. Ensure all dependencies are installed and running.

---

## **Configuration**
### 🔧 **General Settings** (shared/Config.lua)
- **XP System**: Enable/disable XP, configure max levels, and XP gains.
- **Crafting Recipes**: Define item recipes and crafting costs.
- **Job Restrictions**: Specify job roles that can access the factory.

### 📍 **Stash Settings** (shared/Config.Stashes.lua)
- **Stash Locations**: Define stash coordinates, sizes, and labels.
- **Storage Limits**: Set max weight and slots per stash.

---

## **Usage**
### 📦 **Managing Stashes**
- Use `qb-target` to interact with stashes.
- Only factory workers can access specific storage areas.

### 🔨 **Crafting Items**
- Use crafting tables to create items.
- Successful crafts grant XP, contributing to level progression.

### 🎓 **XP & Leveling**
- Players earn XP per craft.
- Leveling system settings are configurable in `Config.lua`.

---

## **Admin Commands**
- `/setcraftxp [player] [amount]` - Set XP for a player.
- `/setcraftlevel [player] [level]` - Adjust a player's crafting level.

---

## **File Structure**
```
qb-factoryjob/
│
├── fxmanifest.lua
├── shared/
│   ├── Config.lua         # General settings
│   └── Config.Stashes.lua # Stash-specific settings
├── client/
│   ├── main.lua           # Client logic
│   └── target.lua         # qb-target interactions
├── server/
│   └── main.lua           # Server logic
└── README.md              # Documentation
```

---

## **Support & Contributions**
For issues, feature requests, or contributions, please open a GitHub issue.

---

## **License**
This resource is licensed under MIT License. See the `LICENSE` file for details.

---

## **Screenshots (Coming Soon)**

---

## **Changelog**
### 🆕 v1.0.0
- Initial release.
- Added crafting system, XP leveling, and stash management.
- Integrated qb-target for seamless interactions.
