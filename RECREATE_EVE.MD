# RECREATE_EVE: EVE Online Ships in USO Building Code

This document provides the technical translation of the *EVE Online* mainline fleet into the **USO Unified Starship Building Codes (CX-999)** and **Volume-Normalized Mass (AX-004)** standards. 

## Conversion Methodology
1. **Scale-Up Factor (1.41x):** To support human crews and USO-standard habitability, all EVE hull lengths are multiplied by **1.41** ($L_{USO} = L_{EVE} \times 1.41$). This results in a 2.82x increase in displacement volume ($V_{env}$) compared to the capsule-pilot original.
2. **Density Family:** EVE hulls are treated as **Heavy** (0.1202 t/m³) for combatants and **Medium** (0.0961 t/m³) for logistics/carriers.
3. **Resultant ICS Ratio:** Scaling by 1.41x creates a habitable void of approximately **0.65** ($V_{ics} / V_{env}$). This provides the necessary volume for the SCU spine, life support, and maintenance crawlspaces required by CX-999.
4. **Class Scaling:** Benchmarked against the Falcon ($k=1.0, L=34.75m$).
5. **Shields/Thermal:** Calibrated per **CX-015** and **AX-004**.

---

## Summary Comparison Table (USO 1.41x Scale)

| Hull Class | Representative | $L_{USO}$ (m) | $k$ | $M_{norm}$ (t) | SCUs | FTL Spin-up | Max Crew |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Frigate** | Rifter | 62 | 1.78 | 3,390 | 28 | 12s | 224 |
| **Destroyer** | Thrasher | 226 | 6.50 | 51,800 | 430 | 16s | 3,440 |
| **Cruiser** | Thorax | 395 | 11.37 | 86,400 | 720 | 21s | 5,760 |
| **Battlecruiser** | Hurricane | 649 | 18.68 | 433,000 | 3,600 | 26s | 28,800 |
| **Battleship** | Abaddon | 1,600 | 46.04 | 7.6M | 63,650 | 32s | 509,200 |
| **Carrier** | Archon | 3,384 | 97.38 | 27.5M | 230,000 | 42s | 1.84M |
| **Titan** | Avatar | 19,300 | 555.4 | 786M | 8.2M | 52s | 65.6M |

---

## 1. Frigate Class (USO Class II: Light Crewed)

#### Executioner (Amarr) / Incursus (Gallente) / Merlin (Caldari) / Rifter (Minmatar)
*   **Linear Scale Factor ($k$):** 1.78 ($L = 62m$)
*   **Normalized Mass ($M_{norm}$):** 3,390 t (Heavy Family)
*   **Habitability (ICS):**
    *   **SCU Count:** 28 SCUs
    *   **Crew Capacity:** 224 (Emergency) / 8 - 15 (Standard)
*   **Engineering Plant:**
    *   **Power:** 4x Small CDAPs (Total Output: 40 MW)
    *   **FTL Propulsion:** 1x Small FTL Engine ($t_{spin} \approx 12s$)
    *   **Thermal Battery ($B_{th}$):** 8,000 MJ
    *   **Active Rejection ($Q_{cool}$):** 1.2 MW
*   **Combat Architecture:**
    *   **Shield Efficiency ($\eta_{shield}$):** 2.38
    *   **Instantaneous Absorption ($IAL$):** 900 MJ
    *   **Max Sustained Tank ($MST$):** 19 MW
    *   **Armor MST (Hardness):** 60 MJ

---

## 2. Destroyer Class (USO Class III: Escort)

#### Thrasher / Coercer / Cormorant / Catalyst
*   **Linear Scale Factor ($k$):** 6.50 ($L = 226m$)
*   **Normalized Mass ($M_{norm}$):** 51,800 t (Heavy Family)
*   **Habitability (ICS):**
    *   **SCU Count:** 430 SCUs
    *   **Crew Capacity:** 3,440 (Emergency) / 120 (Standard)
*   **Engineering Plant:**
    *   **Power:** 6x Medium CDAPs (Total Output: 480 MW)
    *   **FTL Propulsion:** 2x Small FTL Engines ($t_{spin} \approx 16s$)
    *   **Thermal Battery ($B_{th}$):** 120,000 MJ
    *   **Active Rejection ($Q_{cool}$):** 16 MW
*   **Combat Architecture:**
    *   **Shield Efficiency ($\eta_{shield}$):** 1.42
    *   **Instantaneous Absorption ($IAL$):** 46,000 MJ
    *   **Max Sustained Tank ($MST$):** 920 MW
    *   **Armor MST (Hardness):** 115 MJ

---

## 3. Cruiser Class (USO Class III: Medium Hull)

#### Omen / Thorax / Caracal / Rupture
*   **Linear Scale Factor ($k$):** 11.37 ($L = 395m$)
*   **Normalized Mass ($M_{norm}$):** 86,400 t (Heavy Family)
*   **Habitability (ICS):**
    *   **SCU Count:** 720 SCUs
    *   **Crew Capacity:** 5,760 (Emergency) / 400 (Standard)
*   **Engineering Plant:**
    *   **Power:** 4x Large CDAPs (Total Output: 5.0 GW)
    *   **FTL Propulsion:** 2x Medium FTL Engines ($t_{spin} \approx 21s$)
    *   **Thermal Battery ($B_{th}$):** 210,000 MJ
    *   **Active Rejection ($Q_{cool}$):** 85 MW
*   **Combat Architecture:**
    *   **Shield Efficiency ($\eta_{shield}$):** 1.14
    *   **Instantaneous Absorption ($IAL$):** 240,000 MJ
    *   **Max Sustained Tank ($MST$):** 4,800 MW
    *   **Armor MST (Hardness):** 310 MJ

---

## 4. Battlecruiser Class (USO Class IV: Heavy Hull)

#### Harbinger / Myrmidon / Drake / Hurricane
*   **Linear Scale Factor ($k$):** 18.68 ($L = 649m$)
*   **Normalized Mass ($M_{norm}$):** 433,000 t (Heavy Family)
*   **Habitability (ICS):**
    *   **SCU Count:** 3,600 SCUs
    *   **Crew Capacity:** 28,800 (Emergency) / 1,500 (Standard)
*   **Engineering Plant:**
    *   **Power:** 6x Large CDAPs (Total Output: 7.5 GW)
    *   **FTL Propulsion:** 2x Large FTL Engines ($t_{spin} \approx 26s$)
    *   **Thermal Battery ($B_{th}$):** 1.1 TJ
    *   **Active Rejection ($Q_{cool}$):** 230 MW
*   **Combat Architecture:**
    *   **Shield Efficiency ($\eta_{shield}$):** 0.93
    *   **Instantaneous Absorption ($IAL$):** 1.1M MJ
    *   **Max Sustained Tank ($MST$):** 22,000 MW
    *   **Armor MST (Hardness):** 480 MJ

---

## 5. Battleship Class (USO Class IV: Heavy Hull)

#### Abaddon / Megathron / Rokh / Tempest
*   **Linear Scale Factor ($k$):** 46.04 ($L = 1,600m$)
*   **Normalized Mass ($M_{norm}$):** 7.6M t (Heavy Family)
*   **Habitability (ICS):**
    *   **SCU Count:** 63,650 SCUs
    *   **Crew Capacity:** 509,200 (Emergency) / 5,000 (Standard)
*   **Engineering Plant:**
    *   **Power:** 8x Large CDAPs (Total Output: 10 TW)
    *   **FTL Propulsion:** 4x Huge FTL Engines ($t_{spin} \approx 32s$)
    *   **Thermal Battery ($B_{th}$):** 19 TJ
    *   **Active Rejection ($Q_{cool}$):** 1.4 GW
*   **Combat Architecture:**
    *   **Shield Efficiency ($\eta_{shield}$):** 0.65
    *   **Instantaneous Absorption ($IAL$):** 1.6M MJ
    *   **Max Sustained Tank ($MST$):** 32,000 MW
    *   **Armor MST (Hardness):** 820 MJ

---

## 6. Capital Class (USO Class V: Capital Hull)

#### Archon (Carrier) / Naglfar (Dreadnought)
*   **Linear Scale Factor ($k$):** 97.4 ($L = 3,384m$)
*   **Normalized Mass ($M_{norm}$):** 27.5M t (Medium Family)
*   **Habitability (ICS):**
    *   **SCU Count:** 230,000 SCUs
    *   **Crew Capacity:** 1.84M (Emergency) / 12,000 (Standard)
*   **Engineering Plant:**
    *   **Power:** 8x Huge CDAPs (Total Output: 80 GW)
    *   **FTL Propulsion:** 4x Huge FTL Engines ($t_{spin} \approx 42s$)
    *   **Thermal Battery ($B_{th}$):** 65 TJ
    *   **Active Rejection ($Q_{cool}$):** 6.2 GW
*   **Combat Architecture:**
    *   **Shield Efficiency ($\eta_{shield}$):** 0.48
    *   **Instantaneous Absorption ($IAL$):** 29 TJ
    *   **Max Sustained Tank ($MST$):** 580,000 MW
    *   **Armor MST (Hardness):** 1.2 GJ

---

## 7. Supercapital Class (USO Class VI: Megastructure)

#### Avatar / Erebus / Ragnarok / Leviathan
*   **Linear Scale Factor ($k$):** 555.4 ($L = 19.3 km$)
*   **Normalized Mass ($M_{norm}$):** 786M t (Titanic Family)
*   **Habitability (ICS):**
    *   **SCU Count:** 8.2M SCUs
    *   **Crew Capacity:** 65.6M (Emergency) / 450,000 (Standard)
*   **Engineering Plant:**
    *   **Power:** 16x Titanic CDAP Banks (Total Output: 1.2 TW)
    *   **FTL Propulsion:** 8x Titanic FTL Cluster-Engines ($t_{spin} \approx 52s$)
    *   **Thermal Battery ($B_{th}$):** 1.8 PJ
    *   **Active Rejection ($Q_{cool}$):** 210 GW
*   **Combat Architecture:**
    *   **Shield Efficiency ($\eta_{shield}$):** 0.24
    *   **Instantaneous Absorption ($IAL$):** 140 TJ
    *   **Max Sustained Tank ($MST$):** 2.8 TW
    *   **Armor MST (Hardness):** 4.4 GJ

---