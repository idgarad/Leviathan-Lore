# AX-004: Reference Hull Set and Volume-Normalized Mass Calibration

**Document Status:** Final Refactor (Gemini-AX-004)  
**Primary Layer:** Modern Times  
**Subject Domain:** Technical Calibration  
**Audience:** Developers | Authors | Readers  
**Refactor Pass:** Gemini Pass 1
## Abstract

## Canonical Power System: CDAP Integration

All FTL power calculations in this appendix are now anchored to the Compact Dimensional Acceleration Pack (CDAP) system (see AX-006). CDAPs are modular, scalable power units with output, mass, and efficiency scaling by ship class. The canonical scaling law is:

- Output per CDAP: $10\,\text{MW} \times k^3$ (where $k$ is the linear scale factor relative to Falcon)
- Typical quantity per ship class: 4–8 units (see AX-006 for table)
- Total output per class: see table below

| Ship/Engine Class | CDAP Bin | Single CDAP Output (MW) | Typical Quantity | Total Output (MW) |
|-------------------|----------|------------------------|------------------|-------------------|
| Tiny              | Tiny     | 2                      | 4                | 8                 |
| Small (Falcon)    | Small    | 10                     | 6                | 60                |
| Medium            | Medium   | 80                     | 6                | 480               |
| Large             | Large    | 1,250                  | 6                | 7,500             |
| Huge              | Huge     | 10,000                 | 8                | 80,000            |
| Titanic/Titan     | Titan    | 80,000                 | 8                | 640,000           |

All FTL engine power requirements, spin-up, idle, and waste heat values are now expressed as a percentage of available CDAP output for each class. This ensures all reference ships are self-consistent and physically plausible within the Leviathan setting.

This appendix establishes the universal calibration baseline for Leviathan ship engineering. It defines the **Volume-Normalized Mass (VNM)** method to reconcile inconsistent fictional data, sets the material properties for the **Dura-Steel** structural baseline, and records the **CHJ Dynamics** governing drag and force-coupling scaling. This document serves as the "Master Anchor" for all ship-handling and FTL-infrastructure calculations within the repository.

## Diegetic Record: "USO Standards"

The Union for Space Operations (USO) does not merely provide the labor that keeps the empire moving; it dictates the material conditions under which that movement is permitted. While the Imperial Survey Corps oversees the survey sectors and the gates that bridge them, the docking bays, maintenance gantries, and reconditioning pits remain the domain of the Union. To the USO, a ship is a workplace, and an improperly anchored FTL engine or a volatile xM inventory is a lethal liability to every union hand aboard and every facility in the vicinity. Consequently, the USO enforces rigid engineering standards for all vessels operating within Imperial Space. Any hull found with compromised mounting hardware, insufficient cooling capacity, or activation loads that exceed its structural yield limits faces immediate interdiction. Compliance is the non-negotiable price of entry to the docking network; non-compliant ships run the risk of having their permissions revoked and finding themselves excluded from all USO facilities.

## Analytical Breakdown

### Module 1: Volume-Normalized Mass (VNM)

The project's primary axiom is that **Math Holds**. Because published mass figures for external reference ships are inconsistent, we normalize all ships to a standard density baseline ($ \rho_{ref} $) using the **SDF-1 Macross** as our primary anchor.

#### 1.1 The Reference Density
The reference density is derived from the SDF-1 Macross at standard displacement:
- **SDF-1 Dimensions:** $1,210\,\text{m} \times 496\,\text{m} \times 312\,\text{m}$
- **SDF-1 Envelope Volume ($ V_{env} $):** $187,249,920\,\text{m}^3$
- **SDF-1 Published Mass:** $18,000,000\,\text{t}$
- **Reference Density ($\rho_{ref}$):** $\mathbf{0.096128\,\text{t/m}^3}$

#### 1.2 Density Families
Density Families are descriptive outcomes of a ship's internal configuration (Phase 2 Design). They describe the final mass-to-volume ratio after the ESH has been fitted with a custom spine and modules:
| Family | Density ($\rho$) | Logic |
| :--- | :--- | :--- |
| **Light** | $0.0721\,\text{t/m}^3$ | Hollow hulls, carriers, habitat-heavy explorers. |
| **Medium** | $0.0961\,\text{t/m}^3$ | Standard multi-role vessels (Default). |
| **Heavy** | $0.1202\,\text{t/m}^3$ | Armor-dense combatants, industrial mining bricks. |
| **Titanic** | $0.0961\,\text{t/m}^3$ | Megastructures (Normalized to medium for scale). |

#### 1.3 Scaling Procedures for External Franchises
To reconcile ships designed for non-human or capsule-based operation (where internal void space is negligible), the following scaling laws apply:

1. **EVE Online (Capsuleer Standard):** All EVE Online hulls shall be scaled by a linear factor of **1.41** ($\sqrt{2}$) to provide the internal volume required for USO-standard habitability and manual engineering access. 
   - **Volumetric Increase:** $1.41^3 \approx 2.82$. 
   - **ICS Ratio:** The resulting scale creates an internal distribution of roughly 35% machinery and 65% habitable void, aligning these hulls with the **Light to Medium** Density Families defined in Chapter 7 of CX-999.

---

### Module 2: Material and Structural Baseline

FTL engine mounts are the primary failure point under high-G maneuvers or xM-induced drag. We define "Dura-Steel" as the calibration baseline for these mounts.

#### 2.1 Dura-Steel Properties
- **Tensile/Compressive Yield Strength:** $155\,\text{MPa}$
- **Shear Strength:** $93\,\text{MPa}$
- **Thermal Limit:** Retains $>90\%$ strength up to $1,200\,\text{K}$.

#### 2.2 Damped Structural Coupling Struts (DSCS)
Engine mounting relies on DSCS area scaling.
- **Mounting Block Area:** $0.8 \times (\text{Engine Width} \times \text{Engine Height})$
- **Strut Interface Area ($ A_{DSCS} $):** $4\%$ of Mounting Block Area.

---

### Module 3: CHJ Dynamics (Drag and Force-Coupling)

Space behaves as a resistive fluid to any vessel carrying exotic matter.

#### 3.1 CHJ Drag Law
The resistive force ($ F_{drag} $) in Conventional Space is:
$$ F_{drag} = \frac{k_d \cdot M \cdot v^2}{\mu_L} $$
Where:
- $ k_d $: Drag Coefficient (**$ 1.37 \times 10^{-7} $**, Falcon-derived).
- $ M $: **Effective Coupled Mass** ($M_{hull} + m_{xM,inventory}$ in kg).
- $ v $: Velocity in m/s.
- $ \mu_L $: Local Mass Rating (**LMR**) relative to Sol ($\mu_L = 1$ in Sol).

#### 3.2 Coupling Load Normalization and Scaling
To prevent capital ships from maneuvering like interceptors, the peak resistive load capacity of the xM (the drag force anchored by the engine housing) decreases in density as volume increases.
$$ F_{max} = T_{norm,0} \cdot V_F^\alpha \cdot V^{1-\alpha} $$
Where:
- $ T_{norm,0} $: $885\,\text{N/m}^3$ (Falcon Baseline Resistive Load Density).
- $ V_F $: $6,998.4\,\text{m}^3$ (Falcon Volume).
- $ \alpha $: **$0.75$** (Sublinear Scaling Exponent).

#### 3.3 The Structural Ceiling: Configuration Scaling
The cruise speed of a vessel is usually capped by the mechanical integrity of the engine mounts (DSCS, bolts, and blocks) acting as the anchor for the contained xM against domain drag. The engine itself functions as a high-pressure pump to circulate xM; however, it is the mounting that bears the physical load of the xM's resistance to motion. Furthermore, imperial doctrine targets a **1-minute cap on wet-prime timing** for operational readiness, which dictates the minimum number of engines a hull must carry.

**Example: SDF-1 Macross Scaling**
Theoretical Activation Capacity (Unbounded): **79.6 MN**

| Configuration | Total Mount Area ($A_{DSCS}$) | Plant Yield Limit | Max Cruise (Sol) |
| :--- | :--- | :--- | :--- | :--- |
| **Single Engine** | $0.0508\,\text{m}^2$ | $7.87\,\text{MN}$ | $56\,\text{m/s}$ | $\sim 3.2$ Minutes |
| **Quad Engine (Std)** | $0.2032\,\text{m}^2$ | $31.5\,\text{MN}$ | $113\,\text{m/s}$ | **$47$ Seconds** |

- **Falcon Cruise Target:** **$300\,\text{m/s}$** (xM Volume/Capacity Limited).

---

### Module 4: Thermal Architecture

Cooldown cadence is governed by the ship's ability to reject heat during discharge through drag-tolerant exchanger trunks.

#### 4.1 Retained Jump Friction
$$ H_{jump,fric} = \frac{k_H \cdot \sigma_{jump} \cdot M_{norm}^{n_H}}{\mu_L} $$
Where:
- $ n_H = 0.730583 $ (Sublinear Mass Exponent).
- $ k_H = 1.319889\,\text{kJ/t}^{n_H} $.
- $ \sigma_{jump} = 1 $ (Standard Earth-to-Mars jump).

#### 4.2 Cooling Law
$$ Q_{cool} = q_A \cdot A_{ship} $$
- $ q_A = 3.23425 \times 10^{-4}\,\text{kW/m}^2 $.
- $A_{ship}$ represents the effective area of the external radiator trunks.

### Module 4.3: Thermal Calibration Table

| Ship Class | Scale ($k$) | $V_{bat} (4 \times V_{eng})$ | Heavy Max ($P_{H,max}$) | Light Max ($P_{L,max}$) | Input Flux ($\phi_q$) | $Q_{cool}$ ($k^2$) | $t_{cool}$ (s) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Tiny** | 0.46 | $0.80 \text{ m}^3$ | 0.38 MW | 0.04 MW | 0.44 MW/m² | 0.15 MW | 153 |
| **Small (Falcon)** | 1.00 | $8.00 \text{ m}^3$ | 2.08 MW | 0.20 MW | 0.52 MW/m² | 0.69 MW | 181 |
| **Medium** | 2.71 | $159 \text{ m}^3$ | 18.3 MW | 1.83 MW | 0.62 MW/m² | 5.05 MW | 217 |
| **Large** | 9.97 | $7,928 \text{ m}^3$ | 317 MW | 31.7 MW | 0.80 MW/m² | 68.5 MW | 278 |
| **Huge** | 32.9 | $284,800 \text{ m}^3$ | 3,975 MW | 397 MW | 0.92 MW/m² | 747 MW | 319 |
| **Titanic** | 84.1 | $4.76 \times 10^6 \text{ m}^3$ | 30,833 MW | 3,083 MW | 1.09 MW/m² | 4,880 MW | 379 |

*Notes: $P_{H,ship}$ (Black) and $P_{L,ship}$ (White) represent the aggregate ship-level thermal input capacities. $P_{L,ship}$ handles the constant-flow ECS network, which carries heat from life support, energy shields, and armor; it is calibrated to 10% of $P_{H,ship}$ for standard hulls. These capacities are achieved by installing multiple modular thermal battery units (Models WW, BB, or WB) and their associated heat exchangers.*

*Notes: $V_{eng}$ (Falcon) is anchored at $2.0\text{ m}^3$. $V_{bat}$ is fixed at 4x the class-equivalent FTL engine volume. Thermal density remains a constant $250\text{ MJ/m}^3$ across all classes.*

See CX-016 for a detailed breakdown of Thermal Batteries and Heat Exchangers.
---

### Module 5: Exotic Matter (xM) Properties

We use real-world materials as "Physical Stand-ins" for xM modeling.

| Property | Stand-in Material | Value |
| :--- | :--- | :--- |
| **Density/Viscosity** | Diesel Fuel | $850\,\text{kg/m}^3$ |
| **Specific Heat** | Liquid Lithium | $3.58\,\text{kJ/kg/K}$ |
| **Melting Point** | - | $-20^\circ\text{C}$ (Freezes in vacuum) |
| **Boiling Point** | - | $1,342^\circ\text{C}$ |

**Operational Energy:** Spin-up requires **$600\,\text{MJ}$** per kg of xM processed. This is a rough estimate per kg of xM to simplify the energy requirements for various FTL engine sizes.

---

### Module 6: Reference Hull Corpus

### FTL Engine Power Consumption as Percentage of CDAP Output

| Ship | Engine Class | FTL Engines | Total CDAP Output (MW) | Spin-Up Power per Engine (MW) | Total Spin-Up Power (MW) | Spin-Up % of Output | Idle Power per Engine (kW, per FTL engine) | Total Idle Power (kW, all FTL engines) | Idle % of Output |
|------|--------------|---------|------------------------|-------------------------------|-------------------------|---------------------|-------------------------------------------|----------------------------------------|------------------|
| Falcon | Small | 1 | 60 | 0.156 | 0.156 | 0.26% | 864 | 0.864 | 0.0014% |
| Discovery One | Medium | 1 | 480 | 50.8 | 50.8 | 10.6% | 5,940 | 5.94 | 0.0012% |
| Serenity | Medium | 2 | 480 | 50.8 | 101.6 | 21.2% | 5,940 | 11.88 | 0.0025% |
| White Base | Large | 3 | 7,500 | 910.2 | 2,730.6 | 36.4% | 23,760 | 71.28 | 0.00095% |
| SDF-1 (Quad) | Huge | 4 | 80,000 | 2,840 | 11,360 | 14.2% | 99,000 | 396,000 | 0.495% |
| Venator SD | Huge | 4 | 80,000 | 2,840 | 11,360 | 14.2% | 99,000 | 396,000 | 0.495% |
| Spirit of Fire | Huge | 12 | 80,000 | 2,840 | 34,080 | 42.6% | 99,000 | 1,188,000 | 1.485% |
| Infinity (UNSC) | Huge | 52 | 80,000 | 2,840 | 147,680 | 184.6% | 99,000 | 5,148,000 | 6.435% |
| Supremacy | Titanic | 2 | 1,400,000 | 697,957 | 1,395,914 | 99.7% | 396,000 | 792,000 | 0.057% |
| Death Star | Titanic | 22 | 15,000,000 | 697,957 | 13,959,140 | 93.1% | 396,000 | 8,712,000 | 0.058% |

*Spin-up power is a transient load; idle power is continuous. Most ships operate well below CDAP peak output. For megastructures like Supremacy and Death Star, the number and/or scale of CDAPs must be increased so that total output meets or exceeds the required spin-up power for a 1-minute cycle. The table above reflects the minimum CDAP output needed for these ships to meet operational doctrine.*

The following table records the eighteen ships used to anchor the current calibration. Engine counts are determined by the greater of: (a) the activation throughput required to meet the **1-minute wet-prime cap**, or (b) the number of anchor points required to achieve a viable Sol-baseline cruise speed under the **Structural Ceiling**.

| **Ship** | **$M_{norm}$ ($t$)** | **Engine Config** | **Spin-Up** | **Yield Limit** | **Max Cruise (Sol)** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Millennium Falcon** | $505$ | 1x Small | $5$ s | $6.20$ MN | $300$ m/s |
| **Enterprise-D** | $419,000$ | 3x Large | $38$ s | $11.25$ MN | $145$ m/s |
| **Discovery One** | $3,823$ | 1x Medium | $56$ s | $2.10$ MN | $134$ m/s |
| **Serenity** | $9,837$ | 2x Medium | $42$ s | $4.20$ MN | $215$ m/s |
| **White Base** | $474,308$ | 3x Large | $25$ s | $11.25$ MN | $132$ m/s |
| **SDF-1 (Single-Eng)** | $18 \times 10^6$ | 1x Huge | $47$ s | $7.87$ MN | $56$ m/s |
| **SDF-1 (Quad-Eng)** | $18 \times 10^6$ | 4x Huge | $12$ s | $31.48$ MN | **$113$ m/s** |
| **Venator SD** | $16 \times 10^6$ | 4x Huge | $11$ s | $31.48$ MN | $119$ m/s |
| **Spirit of Fire** | $141 \times 10^6$ | 12x Huge | $17$ s | $94.44$ MN | $70$ m/s |
| **Infinity (UNSC)** | $474 \times 10^6$ | 52x Huge | $11$ s | $409.24$ MN | $79$ m/s |
| **Supremacy (Mega)** | $306 \times 10^9$ | 2x Titanic | $30$ s | $29.00$ MN | $0.8$ m/s |
| **Death Star** | $206 \times 10^{12}$ | 20x Titanic | $32$ s | $290.00$ MN | $0.1$ m/s |

*Note: The Enterprise-D is calibrated as a **Light Density Family** explorer ($V_{ics}/V_{env} \approx 0.50$). With an envelope volume of $5.82 \times 10^6 \text{ m}^3$, it supports a theoretical maximum of **4,490 SCUs**.*

*Spin-up calculations use the duty cylinder counts specified in AX-005 for each class (e.g., 1 for Small, 3 for Medium, 4 for Large, 8 for Huge, 16 for Titanic).*

---

### Module 7: Safety and Catastrophic Failure

#### 7.1 The Position Imprint Rule
xM encodes its galactic-relative position upon activation. Reusing already-active xM after a jump results in a "Galactic Position Mismatch."

#### 7.2 Relativistic Collision Analysis (SDF-1 Example)
A failure to discharge xM on the SDF-1 resulting in a head-on collision between the "Position Imprinted" xM and the hull releases:
$$ E_{total} \approx (M_{xM} + M_{ship}) c^2 $$
- **Result:** $1.62 \times 10^{27}\,\text{Joules}$
- **Scale:** **387 Trillion Megatons of TNT.**
- **Consequence:** Atmospheric ignition, moon fragmentation, or planetary surface vaporization.

---

## Material Implications

- **Agility vs. Mass:** The drag coefficient ($k_d$) coupled with volume-normalized mass ensures large ships feel their size. Agile smugglers exist because they have high coupling-load-per-volume, not because they ignore physics.
- **Structural Speed Limits:** Speed is not just a function of engine capacity or xM volume; it is a function of the mechanical interface’s ability to anchor the engine against the resistive drag of the xM.
- **Strategic Cooldown:** The cooldown cadence prevents "Rapid Fire Jumps," forcing tactical pause and infrastructure reliance (Gates).

## Cross-References
- **CX-013:** CHJ Physics baseline.
- **AX-005:** Engine component specifications.

## Author Notes
- **Refactor Logic:** This version of AX-004 removes duplicate calibration tables and merges redundant structural notes into clear "Modules."
- **LMR Integration:** The LMR variable is now formally integrated into the drag and friction equations, allowing for environmental speed variations.
- **Supremacy/Death Star Check:** These megastructures are treated as "Titanic" frames. The math holds—they are essentially mobile geographical features with immense cooldowns.

---
*ISC-004-REF: "The stars do not care for your name, only your displacement."*