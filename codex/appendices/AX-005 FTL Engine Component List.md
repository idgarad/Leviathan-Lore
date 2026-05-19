**Component List:**
-
---

**Cylinder Safety Margin:**
All FTL engine classes assume a safety margin between each cylinder equal to one quarter (1/4) of the cylinder's diameter. This margin is included in the total engine length calculation for each class, ensuring safe operation, maintenance access, and thermal isolation between cylinders.

- xM 4-port intake manifold (size-dependent, with overpressure vent)
- 2 xM intake manifold sensor arrays
- xM buffer tank (size-dependent, 10× total primary cylinder capacity)
	- Primary mounting block (size-dependent, distributes xM lag resistance to hull)
	- Upper mounting block (size-dependent, distributes xM lag resistance to hull)
	- 4 DSCS (Damped Structural Coupling Struts) interfacing with the upper mounting block (shock absorbers for xM resistance and sudden motion)
	- 4 DSCS (Damped Structural Coupling Struts) interfacing with the lower mounting block (shock absorbers for xM resistance and sudden motion)
		- DSCS operate in two modes: powered and unpowered. In powered mode, they use force field technology to convert ship power (in megawatts) into kinetic-to-heat conversion, dissipating sudden forces as heat. This conversion is not 100% efficient; currently, only 20% of the absorbed kinetic force is converted to heat (partial conversion).
- Mounting bolts (and, for large sizes, full welding of mounting block to hull)
- Primary & secondary engine control modules
- 6 block sensor arrays
- Primary & secondary wiring harnesses (size-dependent)
- Coolant intake & return manifolds (size-dependent)
- Coolant intake pressure control valve (size-dependent)
- 2 coolant intake & 2 coolant return manifold sensor arrays
- 1 high energy sensor array
- Duty and spare cylinders (size-dependent, quantity and volume per class)
- Compression actuators with high energy couplers (size-dependent, per cylinder)
- Upper cylinder control bar & 2 sensors (size-dependent)
- Heavy containment shroud (size-dependent)
- Outer containment shell with windows (size-dependent, cylinders are translucent)

---

**Mounting Note:**
All mounting bolts, welds, and hull interface gaskets for each FTL engine class are sized to withstand the maximum resistive coupling force (CHJ Drag) at cruise speed. This creates a trade-off: higher engine counts provide more anchor points for speed, but the increased xM inventory burden reduces maneuverability and G-load limits.

---

**Coupling Forces and Dynamics:**
The force applied to an individual FTL engine mounting block is the sum of the engine's internal xM inertia and its share of the total ship drag:

    F_total = (m_xM,engine × a_ship) + (F_drag_total / N_engines)

where $F_{drag\_total}$ is defined by the CHJ Drag Law in AX-004.

Mount yield strength sets the limit for safe performance. Tactical configurations (N+ engines) optimize for spin-up time, while performance configurations (minimal engines) optimize for G-load tolerance and cruise efficiency.

---

## Tiny FTL Engine (Sub-Falcon, shuttle, drone)

**Dimensions:** ~0.61 m (L) × 0.32 m (W) × 0.32 m (H)  
*Includes 1/4 diameter safety margin between cylinders*
**Estimated Dry Mass:** 120 kg

**xM Output per Cycle:** ~2 L (~2.4 kg)
**Maximum Cylinder Capacity:** 10 L (2 × 5 L)

**Component List:**
- xM 4-port intake manifold (Tiny, with overpressure vent)
- 2 xM intake manifold sensor arrays
- xM buffer tank (Tiny, 10× cylinder capacity, ~10 L)
	- Primary mounting block (Tiny, ~30 kg)
	- Upper mounting block (Tiny, ~30 kg)
	- 4 DSCS (Damped Structural Coupling Struts, Tiny, shock absorbers for xM resistance and sudden motion, upper block)
	- 4 DSCS (Damped Structural Coupling Struts, Tiny, shock absorbers for xM resistance and sudden motion, lower block)
		- DSCS operate in two modes: powered and unpowered. In powered mode, they use force field technology to convert ship power (in megawatts) into kinetic-to-heat conversion, dissipating sudden forces as heat.
- Mounting bolts
- Primary & secondary engine control modules
- 6 block sensor arrays
- Primary & secondary wiring harnesses (Tiny)
- Coolant intake & return manifolds (Tiny)
- Coolant intake pressure control valve (Tiny)
- 2 coolant intake & 2 coolant return manifold sensor arrays
- 1 high energy sensor array
- 1 duty cylinder (Tiny, 2–5 L), 1 spare
- 2 compression actuators with high energy couplers (Tiny)
- Upper cylinder control bar & 2 sensors (Tiny)
- Heavy containment shroud (Tiny)
	- Outer containment shell with windows (Tiny)
	- Maintenance terminal

---

## Small FTL Engine (Falcon, light freighter, corvette)

**Dimensions:** ~0.79 m (L) × 0.41 m (W) × 0.41 m (H)  
*Includes 1/4 diameter safety margin between cylinders*
**Estimated Dry Mass:** 350 kg

**xM Output per Cycle:** ~8 L (~9.6 kg)
**Maximum Cylinder Capacity:** 20 L (2 × 10 L)

**Component List:**
- xM 4-port intake manifold (Small, with overpressure vent)
- 2 xM intake manifold sensor arrays
- xM buffer tank (Small, ~40–60 L)
	- Primary mounting block (Small, ~80 kg)
	- Upper mounting block (Small, ~80 kg)
	- 4 DSCS (Damped Structural Coupling Struts, Small, shock absorbers for xM resistance and sudden motion, upper block)
	- 4 DSCS (Damped Structural Coupling Struts, Small, shock absorbers for xM resistance and sudden motion, lower block)
		- DSCS operate in two modes: powered and unpowered. In powered mode, they use force field technology to convert ship power (in megawatts) into kinetic-to-heat conversion, dissipating sudden forces as heat.
- Mounting bolts
- Primary & secondary engine control modules
- 6 block sensor arrays
- Primary & secondary wiring harnesses (Small)
- Coolant intake & return manifolds (Small)
- Coolant intake pressure control valve (Small)
- 2 coolant intake & 2 coolant return manifold sensor arrays
- 1 duty + 1 spare cylinder (Small, 5–10 L each)
- 2 compression actuators with high energy couplers (Small)
- Upper cylinder control bar & 2 sensors (Small)
- Heavy containment shroud (Small)
	- Outer containment shell with windows (Small)
	- Maintenance terminal

---

## Medium FTL Engine (Transport, research, small warship)

**Dimensions:** ~3.92 m (L) × 0.65 m (W) × 0.65 m (H)  
*Includes 1/4 diameter safety margin between cylinders*
**Estimated Dry Mass:** 900 kg

**xM Output per Cycle:** ~30 L (~36 kg)
**Maximum Cylinder Capacity:** 240 L (6 × 40 L)

**Component List:**
- xM 4-port intake manifold (Medium, with overpressure vent)
- 2 xM intake manifold sensor arrays
- xM buffer tank (Medium, ~200–400 L)
	- Primary mounting block (Medium, ~200 kg)
	- Upper mounting block (Medium, ~200 kg)
	- 4 DSCS (Damped Structural Coupling Struts, Medium, shock absorbers for xM resistance and sudden motion, upper block)
	- 4 DSCS (Damped Structural Coupling Struts, Medium, shock absorbers for xM resistance and sudden motion, lower block)
		- DSCS operate in two modes: powered and unpowered. In powered mode, they use force field technology to convert ship power (in megawatts) into kinetic-to-heat conversion, dissipating sudden forces as heat.
- Mounting bolts
- Primary & secondary engine control modules
- 6 block sensor arrays
- Primary & secondary wiring harnesses (Medium)
- Coolant intake & return manifolds (Medium)
- Coolant intake pressure control valve (Medium)
- 2 coolant intake & 2 coolant return manifold sensor arrays
- 2–4 duty + 1–2 spare cylinders (Medium, 10–40 L each)
- Compression actuators with high energy couplers (Medium, per cylinder)
- Upper cylinder control bar & 2 sensors (Medium)
- Heavy containment shroud (Medium)
	- Outer containment shell with windows (Medium)
	- Maintenance terminal

---

## Large FTL Engine (Carrier, heavy warship, capital)

**Dimensions:** ~7.83 m (L) × 0.87 m (W) × 0.87 m (H)  
*Includes 1/4 diameter safety margin between cylinders*
**Estimated Dry Mass:** 2,500 kg

**xM Output per Cycle:** ~120 L (~144 kg)
**Maximum Cylinder Capacity:** 800 L (8 × 100 L)

**Component List:**
- xM 4-port intake manifold (Large, with overpressure vent)
- 2 xM intake manifold sensor arrays
- xM buffer tank (Large, ~1,000–2,000 L)
	- Primary mounting block (Large, ~600 kg)
	- Upper mounting block (Large, ~600 kg)
	- 4 DSCS (Damped Structural Coupling Struts, Large, shock absorbers for xM resistance and sudden motion, upper block)
	- 4 DSCS (Damped Structural Coupling Struts, Large, shock absorbers for xM resistance and sudden motion, lower block)
		- DSCS operate in two modes: powered and unpowered. In powered mode, they use force field technology to convert ship power (in megawatts) into kinetic-to-heat conversion, dissipating sudden forces as heat.
- Mounting bolts (plus full welding of primary mounting block to hull required)
- Primary & secondary engine control modules
- 6 block sensor arrays
- Primary & secondary wiring harnesses (Large)
- Coolant intake & return manifolds (Large)
- Coolant intake pressure control valve (Large)
- 2 coolant intake & 2 coolant return manifold sensor arrays
- 4–6 duty + 2 spare cylinders (Large, 40–100 L each)
- Compression actuators with high energy couplers (Large, per cylinder)
- Upper cylinder control bar & 2 sensors (Large)
- Heavy containment shroud (Large)
	- Outer containment shell with windows (Large)
	- Maintenance terminal
	- Secondary maintenance terminal (mounted to upper catwalk)
	- Upper catwalk for maintenance access (first class requiring this feature)

---

## Huge FTL Engine (Supercarrier, dreadnaught)

**Dimensions:** ~21.57 m (L) × 1.26 m (W) × 1.26 m (H)  
*Includes 1/4 diameter safety margin between cylinders*
**Estimated Dry Mass:** 7,000 kg

**xM Output per Cycle:** ~500 L (~600 kg)
**Maximum Cylinder Capacity:** 4,800 L (16 × 300 L)

**Component List:**
- xM 4-port intake manifold (Huge, with overpressure vent)
- 2 xM intake manifold sensor arrays
- xM buffer tank (Huge, ~5,000–10,000 L)
	- Primary mounting block (Huge, ~1,800 kg)
	- Upper mounting block (Huge, ~1,800 kg)
	- 4 DSCS (Damped Structural Coupling Struts, Huge, shock absorbers for xM resistance and sudden motion, upper block)
	- 4 DSCS (Damped Structural Coupling Struts, Huge, shock absorbers for xM resistance and sudden motion, lower block)
		- DSCS operate in two modes: powered and unpowered. In powered mode, they use force field technology to convert ship power (in megawatts) into kinetic-to-heat conversion, dissipating sudden forces as heat.
- Mounting bolts (plus full welding of primary mounting block to hull required)
- Primary & secondary engine control modules
- 6 block sensor arrays
- Primary & secondary wiring harnesses (Huge)
- Coolant intake & return manifolds (Huge)
- Coolant intake pressure control valve (Huge)
- 2 coolant intake & 2 coolant return manifold sensor arrays
- 8–12 duty + 3–4 spare cylinders (Huge, 100–300 L each)
- Compression actuators with high energy couplers (Huge, per cylinder)
- Upper cylinder control bar & 2 sensors (Huge)
- Heavy containment shroud (Huge)
	- Outer containment shell with windows (Huge)
	- Maintenance terminal
	- Secondary maintenance terminal (mounted to upper catwalk)
	- Upper catwalk for maintenance access

---

## Titanic FTL Engine (Megastructure, worldship)

**Dimensions:** ~38.90 m (L) × 1.71 m (W) × 1.71 m (H)  
*Includes 1/4 diameter safety margin between cylinders*
**Estimated Dry Mass:** 30,000 kg

**xM Output per Cycle:** ~2,000 L (~2,400 kg)
**Maximum Cylinder Capacity:** 22,000 L (22 × 1,000 L)

**Component List:**
- xM 4-port intake manifold (Titanic, with overpressure vent)
- 2 xM intake manifold sensor arrays
- xM buffer tank (Titanic, ~50,000–100,000 L)
	- Primary mounting block (Titanic, ~8,000 kg)
	- Upper mounting block (Titanic, ~8,000 kg)
	- 4 DSCS (Damped Structural Coupling Struts, Titanic, shock absorbers for xM resistance and sudden motion, upper block)
	- 4 DSCS (Damped Structural Coupling Struts, Titanic, shock absorbers for xM resistance and sudden motion, lower block)
		- DSCS operate in two modes: powered and unpowered. In powered mode, they use force field technology to convert ship power (in megawatts) into kinetic-to-heat conversion, dissipating sudden forces as heat.
- Mounting bolts (plus full welding of primary mounting block to hull required)
- Primary & secondary engine control modules
- 6 block sensor arrays
- Primary & secondary wiring harnesses (Titanic)
- Coolant intake & return manifolds (Titanic)
- Coolant intake pressure control valve (Titanic)
- 2 coolant intake & 2 coolant return manifold sensor arrays
- 16+ duty + 6+ spare cylinders (Titanic, 300–1,000 L each)
- Compression actuators with high energy couplers (Titanic, per cylinder)
- Upper cylinder control bar & 2 sensors (Titanic)
- Heavy containment shroud (Titanic)
	- Outer containment shell with windows (Titanic)
	- Maintenance terminal
	- Secondary maintenance terminal (mounted to upper catwalk)
	- Upper catwalk for maintenance access

---

## Estimated FTL Engine Power Requirements (Spin-Up)

The following table provides estimated FTL engine spin-up energy requirements for each engine class, based on the Falcon-derived scaling law of **600 MJ per kg of xM processed** (see AX-004). Values are for a single engine's standard spin-up cycle.

| Engine Class | Approx. Wet-Line Prime Mass (kg) | Spin-Up Energy (MJ) | Spin-Up Energy (GJ) |
|-------------|-------------------------------|---------------------|---------------------|
| Tiny        | 0.02                          | 12                  | 0.012               |
| Small       | 0.26                          | 156                 | 0.156               |
| Medium      | 84.7                          | 50,820              | 50.8                |
| Large       | 1,517                         | 910,200             | 910.2               |
| Huge        | 4,734                         | 2,840,400           | 2,840               |
| Titanic     | 1,163,262                     | 697,957,200         | 697,957             |

**Notes:**
- Wet-line prime mass values are estimated from AX-004 and may be refined as calibration improves.
- Total ship spin-up energy = (number of engines) × (per-engine value).
- For SDF-1 (4 huge engines): total spin-up energy ≈ 11,360 MJ (11.36 GJ).
- These values represent the energy required to prime the FTL engine for a standard jump, not idle or cruise operation.
- Use the formula: $E_{\text{spin-up}} = 600~\text{MJ} \times M_{\text{prime}}$ for any engine.

---

## Estimated FTL Engine Idle Power Draw (Total xM Inventory)

Idle (standby/containment) power draw for each FTL engine class is now calculated using the total xM inventory in the engine (cylinders + buffer tank), not just the wet-line prime mass. This better reflects the containment and readiness burden for all active xM within the engine system.

**Formula:**
- $P_{\text{idle}} = 15~\text{kW} \times M_{\text{xM,total}}$
- Where $M_{\text{xM,total}}$ is the total xM mass in the engine (cylinders + buffer tank), in kg.

**Example Idle Draws (per engine):**
| Engine Class | Cylinder Capacity (kg) | Buffer Tank (kg) | Total xM (kg) | Idle Power Draw (kW) |
|--------------|-----------------------|------------------|---------------|---------------------|
| Tiny         | 2.4                   | 24               | 26.4          | 396                 |
| Small        | 9.6                   | 48               | 57.6          | 864                 |
| Medium       | 36                    | 360              | 396           | 5,940               |
| Large        | 144                   | 1,440            | 1,584         | 23,760              |
| Huge         | 600                   | 6,000            | 6,600         | 99,000              |
| Titanic      | 2,400                 | 24,000           | 26,400        | 396,000             |

**Notes:**
- Buffer tank is assumed to be 10× cylinder capacity for all classes (see component lists).
- Idle draw is now significantly higher, reflecting the containment burden for all xM present in the engine.
- Adjust $M_{\text{xM,total}}$ as needed for specific ship/engine fits.
- Total ship idle draw = (number of engines) × (per-engine value).

---

## FTL Engine Waste Heat (Idle and Peak)

The following table provides estimated waste heat output for each FTL engine class, both at idle and during peak (spin-up) operation. This waste heat is separate from xM friction/thermal loads and must be managed by the ship’s coolant system.

| Engine Class | Idle Power Draw (kW) | Idle Waste Heat (kW) | Spin-Up Power (MW) | Peak Waste Heat (MW) |
|--------------|----------------------|----------------------|--------------------|---------------------|
| Tiny         | 396                  | 396                  | 0.012              | 0.012               |
| Small        | 864                  | 864                  | 0.156              | 0.156               |
| Medium       | 5,940                | 5,940                | 50.8               | 50.8                |
| Large        | 23,760               | 23,760               | 910.2              | 910.2               |
| Huge         | 99,000               | 99,000               | 2,840              | 2,840               |
| Titanic      | 396,000              | 396,000              | 697,957            | 697,957             |

**Notes:**
- Idle waste heat equals idle power draw (all input power becomes heat at idle).
- Peak waste heat equals spin-up power input (all input energy is eventually dissipated as heat during spin-up).
- The ship’s coolant system must be sized to handle these loads in addition to any xM friction/thermal loads.
- Values are per engine; total ship waste heat = (number of engines) × (per-engine value).

---

## Update: Idle Power Draw Now Based on Total xM Inventory

**Revision:** Idle (standby/containment) power draw for each FTL engine class is now calculated using the total xM inventory in the engine (cylinders + buffer tank), not just the wet-line prime mass. This better reflects the containment and readiness burden for all active xM within the engine system.

**Formula:**
- $P_{\text{idle}} = 15~\text{kW} \times M_{\text{xM,total}}$
- Where $M_{\text{xM,total}}$ is the total xM mass in the engine (cylinders + buffer tank), in kg.

**Example Idle Draws (per engine):**
| Engine Class | Cylinder Capacity (kg) | Buffer Tank (kg) | Total xM (kg) | Idle Power Draw (kW) |
|--------------|-----------------------|------------------|---------------|---------------------|
| Tiny         | 2.4                   | 24               | 26.4          | 396                 |
| Small        | 9.6                   | 48               | 57.6          | 864                 |
| Medium       | 36                    | 360              | 396           | 5,940               |
| Large        | 144                   | 1,440            | 1,584         | 23,760              |
| Huge         | 600                   | 6,000            | 6,600         | 99,000              |
| Titanic      | 2,400                 | 24,000           | 26,400        | 396,000             |

**Notes:**
- Buffer tank is assumed to be 10× cylinder capacity for all classes (see component lists).
- Idle draw is now significantly higher, reflecting the containment burden for all xM present in the engine.
- Adjust $M_{\text{xM,total}}$ as needed for specific ship/engine fits.
- Total ship idle draw = (number of engines) × (per-engine value).

---

## Update: FTL Engine Waste Heat Efficiency

**Revision:**
- Idle waste heat: 85% of idle power draw (15% is not immediately dissipated as heat, e.g., stored or used for non-thermal work).
- Spin-up/peak waste heat: 75% of spin-up power input (25% is used for useful work, e.g., xM compression/containment).

| Engine Class | Idle Power Draw (kW) | Idle Waste Heat (kW, 85%) | Spin-Up Power (MW) | Peak Waste Heat (MW, 75%) |
|--------------|----------------------|---------------------------|--------------------|--------------------------|
| Tiny         | 396                  | 337                       | 0.012              | 0.009                    |
| Small        | 864                  | 734                       | 0.156              | 0.117                    |
| Medium       | 5,940                | 5,049                     | 50.8               | 38.1                     |
| Large        | 23,760               | 20,196                    | 910.2              | 682.7                    |
| Huge         | 99,000               | 84,150                    | 2,840              | 2,130                    |
| Titanic      | 396,000              | 336,600                   | 697,957            | 523,468                  |

**Notes:**
- Idle waste heat = 85% of idle power draw.
- Peak waste heat = 75% of spin-up power input.
- The rest is assumed to be used for useful work or stored in non-thermal forms.
- Values are per engine; total ship waste heat = (number of engines) × (per-engine value).
- The ship’s coolant system must be sized for these loads in addition to xM friction/thermal loads.
