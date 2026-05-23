# The Leviathan Module Codex

## I. Module Philosophy & Standards
This codex defines the standards and catalog structure for all ship modules in the Leviathan setting per USO regulations.

---

### 1.1 General Principles
- Modules are discrete components that can be installed in slots to customize or upgrade ship capabilities.
- Tradeoffs are enforced by slot count, slot type, and system compatibility.
- All installed modules must integrate with the **Standard Management Interface (SMI)** for mainframe oversight.

### 1.2 Module Slot Types (Skill-Aligned)
To align with the Imperial Pilot Skill System, module slots are categorized into three functional bins:
- **Standard Module Slot:** For general upgrades and baseline improvements (mirrors baseline skills).
- **Precision Module Slot:** For specialized enhancements and focused capabilities (mirrors spec-line skills).
- **Efficiency Module Slot:** For upgrades that improve resource use, endurance, or operational cost (mirrors efficiency-line skills).

---

## II. Facility Grouping & System Consolidation
Per **CX-999 Section 102.0B**, all ship systems must be consolidated into certified facilities. This grouping ensures redundancy and standardizes the ship's Interior Conditioned Space (ICS).

### 2.1 Facility Group I: Command Center (Bridge)
*Core intelligence and tactical oversight.*
| System | Std | Prec | Eff |
| :--- | :---: | :---: | :---: |
| Mainframe* | 2 | 3 | 1 |
| Navigation* | 1 | 4 | 2 |
| Targeting* | 3 | 3 | 3 |
| Weapons Array* | 2 | 3 | 3 |
| Logistics Control* | 4 | 4 | 4 |
| Stellar Cartography* | 2 | 4 | 2 |
| Communications* | 4 | 2 | 2 |
| Command & Control* | 1 | 3 | 2 |
| Data Storage / Archives | 1 | 2 | 2 |
| AI/Expert System Management | 1 | 2 | 2 |

### 2.2 Facility Group II: Primary Engine Bay
*FTL activation and primary propulsion.*
| System | Std | Prec | Eff |
| :--- | :---: | :---: | :---: |
| Primary Thrusters | 2 | 2 | 2 |
| FTL Control | 2 | 2 | 2 |
| Propellant Management | 1 | 2 | 2 |

### 2.3 Facility Group III: Power & Thermal Facilities
*CDAP Generation and PCM Heat Sinks.*
| System | Std | Prec | Eff |
| :--- | :---: | :---: | :---: |
| Power Plant (Facility) | 4 | 2 | 3 |
| Thermal Management (Center) | 3 | 3 | 4 |

### 2.4 Facility Group IV: Environmental & Medical (Redundant)
*Redundant life support and biological maintenance.*
| System | Std | Prec | Eff |
| :--- | :---: | :---: | :---: |
| Environment Control (ECS) | 2 | 2 | 2 |
| Medical Bay / Life Support | 1 | 2 | 2 |
| Waste Management / Recycling | 1 | 2 | 4 |

### 2.5 Facility Group V: Auxiliary Engineering & Technical Bays
*Maneuvering, fabrication, and structural defense.*
| System | Std | Prec | Eff |
| :--- | :---: | :---: | :---: |
| Maneuvering Thrusters | 2 | 2 | 2 |
| Engineering / Fabrication | 2 | 2 | 2 |
| Hull Integrity System | 1 | 1 | 1 |
| Emergency Systems | 3 | 2 | 2 |
| Sensor Arrays (Pri/Sec) | 2/2 | 2/2 | 2/2 |
| Shields | 1 | 2 | 3 |
| Armor (Monitoring) | 1 | 3 | 2 |
| Hangar / Security / Specialized | - | - | - |

---

## III. Volumetric Validation (The "Fit" Check)
Per **CX-999 Section 102.14**, all Facility Groups must be expressed in whole SCU increments ($W \times L \times H$). Designers must calculate these dimensions using the following constraints:

1. **Component Footprint:** The facility must physically accommodate the dimensions of its clustered systems (e.g., FTL Engine length/width from **AX-005**).
2. **USO Service Clearance:** Per **CX-999 Chapter X.1**, a minimum of 1.0m of unobstructed clearance must be maintained on all primary service sides of major components.
3. **Linear Span Requirements:** 
    - **Huge Engines (21.57m):** Require a minimum longitudinal span of 2 SCUs (36m).
    - **Titanic Engines (38.90m):** Require a minimum longitudinal span of 3 SCUs (54m).
4. **Trim Allowance:** Per **CX-999 Section 102.11**, the standard 25% trim consumption applies. If the physical components and clearances exceed 75% of the gross SCU volume, the facility must be expanded to the next whole SCU increment.

### Example Calculation: Medium-Class Primary Engine Bay
- **Clustered Systems:** 2x Medium FTL Engines, Propellant Management, Primary Thruster Emitters.
- **Max Component Length:** 3.92m (Medium Engine).
- **Required Clearance:** 1.0m surrounding each engine.
- **VNM Proxy:** A 1x1x1 SCU bay (648 $m^3$) provides sufficient volume, but a 1x2x1 (1296 $m^3$) configuration is often preferred to allow for high-pressure propellant manifolds and thruster gimbal clearance.

---

## IV. Module Classification & Behavior

### 4.1 Rarity and Consumable Behavior
As a balance mechanism, rare and powerful modules often behave as consumables:
- High-impact modules may be discarded after use or require substantial resources to recharge.
- Recharging is intentionally costly, limiting use to critical strategic planning.

### 4.2 Module Rarity Tiers
1. **Common:** Mass-produced, reliable baseline components.
2. **Specialized:** Performance-tuned modules for specific roles.
3. **Rare:** Advanced technology, often containing experimental or restricted components (e.g., Xelon tech).

---

## V. Sample Module Catalog

### Lithium Stabilizer (Thermal Battery Module)
- **Slot Type:** Standard Module
- **System Compatibility:** Thermal Battery (any size band, must match system size)
- **Effect:** Increases battery capacity by 10%.
- **Drawback:** Reduces outflow transfer rate by 9% per rank in the 'Thermal Management' skill.
- **Notes:** Standard issue for long-range scouts. Negates Logistic Officer bonuses.

### Xelon Nullifier (Thermal Battery Module, Rare)
- **Slot Type:** Precision Module
- **System Compatibility:** Thermal Battery (any size band, must match system size)
- **Effect:** Thermal deletion at a ratio of 50:1 (50 MJ power : 1 MJ heat).
- **Limit:** Can delete up to 500 MJ of heat before the module is depleted and must be replaced or recharged.
- **Drawback:** Use of a Xelon Nullifier prohibits FTL priming for 10 minutes due to system interference.
- **Rarity:** Rare

### Highpass Compression Fittings (FTL Drive Module)
- **Slot Type:** Efficiency Module
- **System Compatibility:** FTL Drive (any size band, must match system size)
- **Effect:** Doubles the maximum pressure the FTL system can support, reducing spin-up times by 25%.
- **Drawback:** None
- **Notes:** Essential for tactical extraction vessels.

---

## VI. Administrative & Future Growth
- **Update Protocol:** As new systems are introduced, they must be assigned to a Facility Group and mapped to standard slot counts.
- **SMI Compliance:** All future modules must provide a data-handshake for the Mainframe log per **CX-999 Chapter 6**.

<!--
[PROMPT_SUGGESTION]Should we add a section for 'External Mount' modules specifically for the ESH Heavy/Medium/Light mounts? [/PROMPT_SUGGESTION]
[PROMPT_SUGGESTION]Can you define a module for the 'Propellant Management' system that improves xM circulation efficiency? [/PROMPT_SUGGESTION]
-->
