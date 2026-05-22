## CDAP Volume as Proportion of Vessel Size

**Method:**
- CDAP unit volume scales with $k^3$ (linear scale factor relative to Falcon).
- Vessel internal volume is estimated from reference hulls (see AX-004).
- Total CDAP volume = unit volume × quantity.
- Proportion = (total CDAP volume) / (vessel internal volume).

| Ship/Engine Class | CDAP Bin | Unit Volume (m³) | Quantity | Total CDAP Volume (m³) | Vessel Volume (m³) | CDAP % of Vessel |
|-------------------|----------|------------------|----------|------------------------|--------------------|------------------|
| Tiny              | Tiny     | 0.0096           | 4        | 0.0384                 | 1,000              | 0.004%           |
| Small (Falcon)    | Small    | 0.048            | 6        | 0.288                  | 6,998              | 0.004%           |
| Medium            | Medium   | 0.384            | 6        | 2.304                  | 50,000             | 0.005%           |
| Large             | Large    | 7.68             | 6        | 46.08                  | 1,000,000          | 0.005%           |
| Huge              | Huge     | 61.44            | 8        | 491.52                 | 10,000,000         | 0.005%           |
| Titanic/Titan     | Titan    | 614.4            | 8        | 4,915.2                | 187,249,920        | 0.003%           |

*Unit volumes are scaled from Falcon (0.048 m³) by $k^3$ for each class. Vessel volumes are estimated from AX-004 reference hulls. CDAPs occupy less than 0.01% of vessel internal volume in all classes, ensuring negligible impact on habitable or cargo space.*
## CDAP Binning and Quantity Scaling by Ship/Engine Class

**Binning and Quantity Rule:**
- CDAPs are binned by ship/engine class: Tiny, Small, Medium, Large, Huge, Titan.
- Each ship class typically installs 4–8 CDAPs per main engine block, with more for larger ships or higher redundancy.
- The number of CDAPs is set by dividing total required power by single-CDAP output, then rounding up to the next even number for redundancy and operational margin.

| Ship/Engine Class | CDAP Bin | Single CDAP Output (MW) | Typical Quantity | Total Output (MW) |
|-------------------|----------|------------------------|------------------|-------------------|
| Tiny              | Tiny     | 2                      | 4                | 8                 |
| Small (Falcon)    | Small    | 10                     | 6                | 60                |
| Medium            | Medium   | 80                     | 6                | 480               |
| Large             | Large    | 1,250                  | 6                | 7,500             |
| Huge              | Huge     | 10,000                 | 8                | 80,000            |
| Titanic/Titan     | Titan    | 80,000                 | 8                | 640,000           |

*Quantities are chosen for redundancy and operational margin (always even, typically 6–8 per block). Total output is single CDAP output × quantity.*
# AX-006: Power System Calibration Appendix

This appendix collects all canonical calibration data, scaling laws, and reference values for power generation, storage, and distribution in the Leviathan setting. It serves as the technical anchor for CX-014 and related codex volumes.

## [Section Placeholder]
- Calibration details and tables will be moved here as the CDAP system is further defined.

## Example: Millennium Falcon CDAP Power Calibration

- **Primary Power Bank:** 6 CDAP units (Compact Dimensional Acceleration Packs)
- **Hot Fail-Over Spares:** 2 CDAP units
- **Operational Notes:**
    - All 6 primary CDAPs operate in parallel to supply the Falcon’s full power demand under normal and peak loads.
    - The 2 spare units are kept in hot fail-over, ready to instantly replace any failed primary unit.
    - CDAPs are self-regulating and will shut down if cooling fails; restart requires external jump-start power.
- **Self-Regulation and Idle State:** CDAP units automatically adjust their output to match the power drawn by connected systems. When demand is low, they enter a very low power idle state, maintaining only minimal activity to avoid full shutdown. This feature is critical: once stopped, a CDAP requires a massive external power source to restart. For this reason, CDAPs are always kept in idle state during sale, purchase, or transport, never fully deactivated.
- **Performance Decay:** CDAP unit output gradually decays over time due to thermal and operational effects. As output drops below required thresholds, it is standard practice to bring a spare (hot fail-over) unit online to maintain full power delivery. This ensures continuous, reliable operation even as individual units age or degrade.
- **Calibration Anchor:** The Falcon’s CDAP configuration serves as the baseline for small-ship power scaling in the Leviathan setting.
- **Standardized Size and Universality:** All CDAP units are manufactured to a single, standardized function and interface, but can be produced in a range of physical sizes to suit different ship classes and installation requirements. Larger CDAPs provide proportionally greater power output, allowing capital ships and worldships to use fewer, larger units, while small craft use compact versions. The core dimensional relationships of CHJ space still govern the minimum and maximum viable sizes, but within those bounds, CDAPs can be scaled to meet operational needs.
- **Banking and Installation (Revised):** CDAPs may be installed individually or in banks, with total ship power determined by the number and size of units installed. Banks can be arranged in 3D arrays as needed, similar to battery arrays, but the size of each CDAP may vary by application.
- **Small CDAP Output Calibration (Revised):** Each small CDAP unit is now rated for approximately **10 MW** peak output. This aligns with common sci-fi ship power scales and provides a more robust baseline for shipboard systems. For the Millennium Falcon (6 units), this yields a total peak output of 60 MW, with additional margin from hot fail-over spares.
- **Weight:** Each small CDAP unit weighs approximately **100 kg**. This makes manual handling a two-person job, though specialized loaders or exosuits are typically used for installation and removal. The substantial weight reflects the dense, high-energy components and robust containment required for safe operation.
- **Waste Heat and Efficiency:**
    - At peak output, a small CDAP generates waste heat equal to 75% of its 10 MW output (**7.5 MW** per unit).
    - At idle, CDAPs are extremely efficient, drawing as little as **100 W**—just enough to power status indicators and a small integrated computer. Idle waste heat is negligible and easily managed by passive cooling.
    - This ultra-low idle draw allows CDAPs to be safely stored, transported, or even purchased at retail without special infrastructure, provided they are never fully shut down.
- **Physical Size Reference:** For setting flavor and visual consistency, each small CDAP unit is approximately the size and form factor of a Ghostbusters proton pack—roughly 0.6 m tall, 0.4 m wide, and 0.2 m deep. This makes them compact enough for modular installation, maintenance, and dramatic on-screen presence, while still conveying advanced, high-density technology.
See CX-016 for details on Thermal Batteries and Heat Exchangers, which manage CDAP waste heat.

---
*This appendix is a work in progress and will be expanded as power system calibration is refined.*

## CDAP Scaling Law and Example Classes

**Scaling Assumptions:**
- CDAP units maintain constant density and dimensional ratios (geometry is fixed by CHJ constraints).
- Power output and mass scale with volume ($k^3$), where $k$ is the linear scaling factor relative to the Falcon unit.
- Efficiency increases with size: waste heat fraction decreases as $f_{waste} = f_{waste,0} \cdot k^{-\alpha}$, with $\alpha \approx 0.2$ (empirical, adjustable).

**Scaling Laws:**
- $\text{Output} = 10\,\text{MW} \times k^3$
- $\text{Mass} = 100\,\text{kg} \times k^3$
- $f_{waste} = 0.75 \times k^{-0.2}$
- $\text{Waste Heat} = \text{Output} \times f_{waste}$

**Example CDAP Classes:**

| Class   | Linear Scale ($k$) | Output (MW) | Mass (kg) | Waste Heat Fraction | Waste Heat (MW) |
|---------|--------------------|-------------|-----------|---------------------|-----------------|
| Falcon  | 1                  | 10          | 100       | 0.75                | 7.5             |
| Large   | 5                  | 1,250       | 12,500    | 0.57                | 712             |
| Titan   | 20                 | 80,000      | 800,000   | 0.42                | 33,600          |

*Waste heat fraction for Large: $0.75 \times 5^{-0.2} \approx 0.57$; for Titan: $0.75 \times 20^{-0.2} \approx 0.42$.*

**Interpretation:**
- As CDAPs get larger, they become more efficient (less waste heat per MW output).
- Mass and output scale with volume.
- Dimensional ratios and density are constant, so installation and handling scale predictably.
