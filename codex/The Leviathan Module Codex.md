# The Leviathan Module Codex

## Purpose
This codex defines the philosophy, standards, and catalog structure for all ship modules in the Leviathan setting. It documents the modular system approach, standardizes module slot types, and catalogs the high-level ship systems and their module configurations.

---

## Module Philosophy
- All ships are constructed with standardized external mounts and internal system slots, as defined by USO regulations.
- Modules are discrete components that can be installed in these slots to customize or upgrade ship capabilities.
- Tradeoffs are enforced by slot count, slot type (power/size), and system compatibility.

---

## Updated Module Slot Types (Skill-Aligned)

To align with the skill system, module slots are categorized as follows:
- **Standard Module Slot:** For general upgrades and baseline improvements (mirrors baseline skills).
- **Precision Module Slot:** For specialized enhancements and focused capabilities (mirrors spec-line skills).
- **Efficiency Module Slot:** For upgrades that improve resource use, endurance, or operational cost (mirrors efficiency-line skills).

Modules are designed and cataloged according to these bins, and each system specifies its available slot mix.

---

## High-Level Ship Systems & Default Module Slot Configurations

| System                        | Standard Slots | Precision Slots | Efficiency Slots | Notes                                   |
|-------------------------------|---------------|----------------|------------------|-----------------------------------------|
| Mainframe                     | 2             | 3              | 1                | Core system, interfaces with other      |
| Navigation                    | 1             | 4              | 2                |                                         |
| Targeting                     | 3             | 3              | 3                |                                         |
| Primary Sensor Array          | 2             | 2              | 2                |                                         |
| Secondary Sensor Array        | 2             | 2              | 2                |                                         |
| Power Plant                   | 4             | 2              | 3                |                                         |
| Primary Thrusters             | 2             | 2              | 2                |                                         |
| Maneuvering Thrusters         | 2             | 2              | 2                |                                         |
| Thermal Management            | 3             | 3              | 4                | Includes batteries, exchangers          |
| FTL Control (incl. emitters)  | 2             | 2              | 2                |                                         |
| Environment Control System    | 2             | 2              | 2                |                                         |
| Weapons Array                 | 2             | 3              | 3                | Per-weapon management by mounting       |
| Shields (with emitters)       | 1             | 2              | 3                |                                         |
| Armor                         | 1             | 3              | 2                |                                         |
| Hull Integrity System         | 1             | 1              | 1                |                                         |
| Logistics Control             | 4             | 4              | 4                | Inventory and crew management           |
| Stellar Cartography           | 2             | 4              | 2                | Maps                                    |
| Communications                | 4             | 2              | 2                | Includes mission management             |
| Engineering Bay / Fabrication | 2             | 2              | 2                | Repairs, upgrades, manufacturing        |
| Hangar Bay / Docking Control  | 1             | 4              | 2                | Shuttles, drones, boarding ops          |
| Security System               | 1             | 4              | 2                | Internal sensors, lockdowns, anti-board |
| Medical Bay / Life Support    | 1             | 2              | 2                | Advanced medical, stasis                |
| Data Storage / Archives       | 1             | 2              | 2                | Mission logs, sensor data               |
| AI/Expert System Management   | 1             | 2              | 2                | Autonomous ops, decision support        |
| Command & Control             | 1             | 3              | 2                | Fleet/tactical integration              |
| Waste Management / Recycling  | 1             | 2              | 4                |                                         |
| Propellant Management         | 1             | 2              | 2                | Fuel, reaction mass, consumables        |
| Emergency Systems             | 3             | 2              | 2                | Fire suppression, escape pods, damage   |
| Specialized Equipment Control | 3             | 2              | 2                | Modular/science/mission-specific        |

---

## Example Module Entries

### Lithium Stabilizer (Thermal Battery Module)
- **Slot Type:** Standard Module
- **System Compatibility:** Thermal Battery (any size band, must match system size)
- **Effect:** Increases battery capacity by 10%.
- **Drawback:** Reduces outflow transfer rate by 9% per rank in the 'Thermal Management' skill.
- **Special:** Use of this module negates any Logistic Officer bonuses (officers are treated as bridge modules, but are personnel-based).

### Xelon Nullifier (Thermal Battery Module, Rare)
- **Slot Type:** Precision Module
- **System Compatibility:** Thermal Battery (any size band, must match system size)
- **Effect:** Allows thermal deletion at a ratio of 50:1 (for every 50 MJ of power provided, 1 MJ of heat is deleted).
- **Limit:** Can delete up to 500 MJ of heat before the module is depleted and must be replaced or recharged.
- **Drawback:** Use of a Xelon Nullifier prohibits FTL priming for 10 minutes due to system interference.
- **Rarity:** Rare

### Highpass Compression Fittings (FTL Drive Module)
- **Slot Type:** Efficiency Module
- **System Compatibility:** FTL Drive (any size band, must match system size)
- **Effect:** Doubles the maximum pressure the FTL system can support, reducing spin-up times by 25%.
- **Drawback:** None
- **Notes:** This module is highly sought after for rapid deployment and tactical maneuvering.

---

## Canonical High-Level Ship Systems

The following systems are recognized as actively managed, modular shipboard systems. Each supports module slots and/or officer assignment, and is managed via the Standard Management Interface protocol:

- Mainframe (core system)
- Navigation
- Targeting
- Primary Sensor Array
- Secondary Sensor Array
- Power Plant
- Primary Thrusters
- Maneuvering Thrusters
- Thermal Management
- FTL Control (including FTL emitters)
- Environment Control System (ECS)
- Weapons Array (per-weapon management by mounting)
- Shields (with shield emitters)
- Armor
- Hull Integrity System
- Logistics Control (inventory and crew management)
- Stellar Cartography (maps)
- Communications (including mission management)
- Engineering Bay / Fabrication
- Hangar Bay / Docking Control
- Security System (internal sensors, lockdowns, anti-boarding)
- Medical Bay / Life Support Augmentation
- Data Storage / Archives
- AI/Expert System Management
- Command & Control (fleet/tactical integration)
- Waste Management / Recycling
- Propellant Management
- Emergency Systems (fire suppression, damage control)
- Specialized Equipment Controls (for modular/science/mission-specific systems)

---

## Module Rarity and Consumable Behavior

As a balance mechanism, rare and powerful modules often behave as consumables:
- These modules may be discarded after use or require substantial work and resources to recharge or refurbish.
- Recharging or reactivating such modules is intentionally costly, limiting their use to critical situations or strategic planning.
- This design ensures that high-impact modules remain valuable and do not undermine core system balance.

---

## Cataloging Modules
- Each module entry should specify:
  - Compatible slot type(s)
  - Power/size requirements
  - System compatibility
  - Effects and tradeoffs

---

## Future Expansion
- As new systems or module types are introduced, update this codex to maintain consistency and clarity across the catalog.
