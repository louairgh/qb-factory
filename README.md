# **qb-factoryjob**

A customizable factory job script for **QBCore** framework. This resource allows players to work in a factory, craft items, manage stashes, and gain XP to level up their crafting skills.

---

## **Features**
- **Crafting System**: Players can craft items using recipes and gain XP for successful crafts.
- **XP and Leveling**: Players level up by gaining XP, with configurable max levels and XP multipliers.
- **Stash Management**: Multiple stashes for storing raw materials, finished products, and tools.
- **qb-target Integration**: Easy-to-use target system for interacting with stashes and crafting tables.
- **Customizable Configurations**: Easily configure stashes, crafting recipes, XP settings, and more.

---

## **Dependencies**
- [**qb-core**](https://github.com/qbcore-framework/qb-core): Core framework for QBCore.
- [**qb-target**](https://github.com/qbcore-framework/qb-target): For interaction with stashes and crafting tables.
- [**qb-inventory**](https://github.com/qbcore-framework/qb-inventory): For managing stashes and items.

---

## **Installation**
1. Download the `st-factoryjob` resource and place it in your `resources` folder.
2. Add the following line to your `server.cfg`:
   ```lua
   ensure st-factoryjob
   ```
3. Ensure all dependencies (qb-core, qb-target, qb-inventory) are installed and running.

---

## **Configuration**
### **General Configuration**
Edit the `shared/Config.lua` file to customize:
- **XP System**: Enable/disable XP, set max levels, and configure XP multipliers.
- **Crafting Recipes**: Define recipes for crafting items.
- **Job Restrictions**: Set which jobs can access the factory.

### **Stash Configuration**
Edit the `shared/Config.Stashes.lua` file to customize:
- **Stash Locations**: Define coordinates, sizes, and labels for each stash.
- **Stash Properties**: Set max weight and slots for each stash.

---

## **Usage**
### **Accessing Stashes**
- Players can interact with stashes using the qb-target system.
- Each stash is labeled and can be accessed by players with the factory job.

### **Crafting Items**
- Players can craft items at designated crafting tables.
- Successful crafts reward XP, which contributes to leveling up.

### **XP and Leveling**
- Players gain XP for successful crafts.
- XP requirements for each level are configurable in `Config.lua`.

---

## **Commands**
- **Set XP**: Admins can set a player's XP using the `/setcraftxp` command.
- **Set Level**: Admins can set a player's level using the `/setcraftlevel` command.

---

## **File Structure**
```
st-factoryjob/
│
├── fxmanifest.lua
├── shared/
│   ├── Config.lua          # General configuration
│   └── Config.Stashes.lua  # Stash-specific configuration
├── client/
│   ├── main.lua            # Main client logic
│   └── target.lua          # Target integration for stashes
├── server/
│   └── main.lua            # Main server logic
└── README.md               # Documentation
```

---

## **Support**
For support, questions, or feature requests, please open an issue on the GitHub repository.

---

## **License**
This resource is licensed under the MIT License. See the LICENSE file for more details.

---

## **Credits**
Developed by [Louai].

Enjoy using **st-factoryjob**! 🚀

---

## **Screenshots (Comming Soon)**
---

## **Changelog**
### v1.0.0
- Initial release of `st-factoryjob`.
- Added crafting system, XP leveling, and stash management.
- Integrated qb-target for seamless interactions.
