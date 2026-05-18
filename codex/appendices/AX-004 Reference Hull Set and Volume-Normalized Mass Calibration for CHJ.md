---
### Reference FTL System Plumbing Diagram (Calibration Standard)

The following diagram represents the canonical calibration plumbing for an FTL system, using a bus architecture for xM flow and emitter priming. This model is used as the baseline for all FTL engine, emitter, and piping calculations in this appendix:

```
[FTL Engine]
	|
	v
[Main Supply Bus]
	|
	+---------------------> [Emitters]
	|                           |
	|                           v
	|                   [Hot Return Line]
	|                           |
	|                  [Thermal Management]
	|                           |
	+----------------------> [Discharge Module]
								 |
								 v
							[FTL Engine]
```

**Flow Description:**
- The FTL engine primes and fills the main supply bus with active xM.
- Emitters branch off the bus and are primed from it.
- After priming, any unused xM in the bus is drained to the discharge module.
- When the FTL event occurs, emitters fire and send hot xM to thermal management.
- Thermal management cools the xM, which is then dumped into the discharge module.
- The discharge module is the only return path to the FTL engine, completing the loop.

This reference system is the basis for all subsequent FTL engine, cylinder, and piping scaling in this appendix.
# AX-004: Reference Hull Set and Volume-Normalized Mass Calibration for CHJ

Document Status: Draft
Primary Layer: Modern Times
Subject Domain: Technical Appendix
Audience: Developers | Authors | Readers

## Abstract

This appendix records the reference hull set currently used to calibrate the CHJ rewrite. It fixes SDF-1 Macross as the calibration ship, defines the outer-envelope volume method used to normalize incompatible fictional mass figures, separates full-envelope anchors from partial-data anchors, and records the current eighteen-ship comparison corpus.

## Diegetic Record

Shipwrights who survive long enough to matter learn a simple embarrassment: most arguments about tonnage are really arguments about prestige. Admirals call a hull light because they wish it were agile. Yard lords call it heavy because they wish it were feared. Neither answer is useful when the question is what kind of inhabited machine the CHJ stack is actually being asked to drag.

The imperial technical habit is therefore to begin with the operating envelope. A warship, freighter, or exploratory ark is first treated as a crewed service volume with length, beam, depth, and population burden. Wedges, rings, flight pods, fins, cavities, and ornamental voids matter later. The first question is how much organized hull-space is being moved, supplied, pressurized, and kept coherent under xM load.

This discipline is especially important when foreign or hypothetical hulls are compared against one another. Their published mass figures are rarely written to the same standard. Some are closer to dry structural weight, some to loaded displacement, and some to pure dramatic rhetoric. A comparative corpus is only usable if the same simplifying violence is applied to every ship in it.

For that reason, the present calibration pass uses a conservative outer-envelope method. Hulls with published length, width, and height are allowed to drive the comparison set. Hulls with only partial geometry, crew, or mass data are retained as sanity checks, role checks, and scale checks, but they are not permitted to falsify the mass-normalization baseline by pretending to be more complete than they are.

## Analytical Breakdown

### Layer Function

- Modern Times: This appendix supports the present FTL rewrite by giving CHJ ship handling and throughput discussions a stable external comparison set.
- Ancient History: The method provides a disciplined way to compare rediscovered or poorly documented hulls without mistaking legend for measurement.
- Hyborean Era: Mythic megastructures and lost warships can later be slotted into the same calibration grammar once even partial dimensions are known.
- Eldritch Layer: Impossible geometries remain legible as violations because there is now a declared baseline for what ordinary crewed hull envelopes look like.

### Calibration Rules

- This appendix is an author-side calibration instrument for Leviathan canon, not a claim that the listed comparison ships exist diegetically inside the setting.
- SDF-1 Macross is the calibration ship for the current pass, per standing project instruction.
- The operative comparison volume is the outer hull envelope: `V_env = L * W * H`.
- Published apparent density is recorded as `rho_app = M_pub / V_env` when both published mass and full envelope dimensions are available.
- Normalized mass is recorded as `M_norm = rho_ref * V_env`.
- The current reference density is `rho_ref = 18,000,000 t / (1,210 m * 496 m * 312 m) = 0.096128 t/m^3`, using SDF-1 Macross standard displacement.
- Current first-pass density-family planning bands are `rho_light = 0.75 * rho_ref = 0.072096 t/m^3`, `rho_medium = rho_ref = 0.096128 t/m^3`, and `rho_heavy = 1.25 * rho_ref = 0.120160 t/m^3`.
- When published mass and published dimensions conflict hard enough that both cannot be kept honestly, documented dimensions win. Preserve the envelope first, then infer replacement mass through `rho_ref` or through the chosen density family.
- Initial ship-handling targets are recorded here as provisional Conventional Space cruise targets for later CHJ drag and throughput fitting.
- Current cruise-speed targets assume the Sol system as the local mass baseline, so `LMR / LMR_Sol = 1` unless otherwise noted.
- All normalized masses assume active crewed-service condition rather than stripped hulk mass, museum condition, or empty ferry state.
- Bounding-envelope bias is accepted intentionally. The purpose of this method is consistent comparison across franchises, not exact real-world naval architecture.
- Full-envelope anchors may drive calibration. Partial-data anchors may pressure-test scale and role assumptions, but they do not set the normalization constant.

### Initial Cruise-Speed Targets

| Ship | Target Cruise Speed | Calibration Role | Current Reading |
| --- | ---: | --- | --- |
| SDF-1 Macross | 108 m/s | First heavy-hull cruise target | Treat the SDF-1 as a very large warship whose ordinary cruise behavior remains deliberately slow in Conventional Space. |
| Millennium Falcon | about 300 m/s | First fast light-hull cruise target | Treat the Falcon as a small high-performance service hull whose ordinary cruise behavior materially exceeds the SDF-1 baseline. |

**Note:** These cruise-speed targets assume 100% constant thrust is available and applied throughout cruise. Real-world or diegetic operational profiles may involve variable thrust, coasting, or other constraints that reduce average speed below these calibration values.

- These are calibration targets, not yet final derived outputs.
- They should be read as present C-Space cruise benchmarks used to constrain later CHJ drag, handling, and ship-class fitting.
- They are Sol-baseline targets rather than universal speeds, because Local Mass Rating changes effective CHJ drag from system to system.
- The point of the pair is comparative discipline: an enormous fleet fortress should not cruise like a smuggler, and a smuggler should not be crushed down to capital-ship behavior.
- A system with twice Sol's Local Mass Rating halves CHJ drag under otherwise identical conditions, so the attainable cruise speed for the same ship must be recalculated per system rather than copied blindly from the Sol baseline.
- Later calibration work should explain whether a ship's cruise target is being limited primarily by xM drag envelope, hull stress tolerance, fuel economy, traffic doctrine, or some combination of the four.

### Initial Jump-Cooldown Targets

| Hull Scale | Target Cooldown After Typical Jump | Calibration Role | Current Reading |
| --- | ---: | --- | --- |
| Falcon-scale small hull | about 3 minutes | First small-hull thermal recovery anchor | Treat this as the expected xM cooldown window after a typical jump before the same working xM mass can be reused immediately. |
| SDF-1-scale heavy hull | about 6 minutes | First capital-hull thermal recovery anchor | Treat this as the present heavy-hull calibration anchor for the same standard Sol-baseline Earth-to-Mars jump. |

- These are calibration targets, not yet a universal cooldown law for all hulls and routes.
- Immediate repeat jumps above this cadence require additional cooled xM buffer aboard the ship rather than wishful thinking.
- Additional buffered xM improves jump chaining, but it also raises carried xM mass and therefore the ship's C-Space drag burden.
- Current first-pass thermal law assumes effective cooling capacity scales linearly with usable ship surface area, while retained standard-jump CHJ friction heat scales with normalized ship mass by a sublinear exponent.
- Later calibration work should still relate cooldown to thermal-battery capacity, heat-pipe exchanger limits, non-standard jump severity, and any emitter-side inefficiency not captured by the present friction law.

### Current Thermal Friction Calibration

- The present first-pass cooling law is `Q_cool = q_A * A_ship`, where `A_ship` is the effective ship surface area available to the xM heat-rejection architecture.
- The present first-pass standard-jump friction law is `H_jump,fric = k_H * sigma_jump * (M_norm)^n_H`, with `sigma_jump = 1` for the current Sol-baseline Earth-to-Mars H-Space hop.
- For current thermal calibration only, Falcon is treated as a shallow circular hull using published length `34.75 m` as diameter and published height `7.8 m` as hull depth, because the ship is roughly circular in planform and the appendix does not yet carry a cleaner full envelope for it.
- This first-pass Falcon thermal approximation gives `A_F = 2,748.363 m^2`, `V_F = 7,397.655 m^3`, and `M_F,norm = 711.122 t`.
- Anchoring Falcon at `160 kJ` retained friction heat and `180 s` cooldown plus SDF-1 at `360 s` fixes `n_H = 0.730583`, `k_H = 1.319889 kJ / t^n_H`, and `q_A = 3.23425 x 10^-4 kW/m^2`.
- Under this law, total jump friction heat still rises with normalized hull mass, but the effective heat added per ton falls with scale. Larger hulls therefore run hotter in absolute terms while gaining some thermal economy of scale.

### Falcon Smallest Emitter Anchor

- Falcon currently anchors the smallest emitter class as a dual-redundant suite of `16` total emitters, with `8` required for minimum field closure.
- Each smallest emitter is modeled as a flat square surface panel `22 in x 22 in`, with `4 in` panel thickness and `18 in` rear manifold depth.
- This fixes `s_emit,1 = 0.5588 m`, `A_emit,1 = 0.312257 m^2`, `h_stack = 0.5588 m`, and `V_emit,1 = 0.174489 m^3` for the current first-pass emitter geometry law.

### Current Comparative FTL Specs

- The current comparative FTL spec table now carries exact-coverage worked mixed-suite fits for every current full-envelope sample hull.
- Current practical doctrine expects mixed emitter suites: large backbone panels should cover broad regular hull faces, while smaller contour panels should close irregular geometry, redundancy pockets, and remaining local gaps so envelope area is not wasted on oversized emitters.
- The standard jump basis for the table is the current Sol-baseline Earth-to-Mars H-Space hop, so `t_jump = 10 s`.
- `xM Processed Per Standard Jump` means `M_jump,eq`, the throughput-equivalent working xM mass circulated through the active loop during that representative jump. It is not a statement of full onboard xM inventory.
- `Minimum Engine xM Reserve At Start` means `M_engine,start = 10 * M_jump,eq`, the current sanity-check assumption for immediately available engine-side working xM before any external refill. It is not a statement of full strategic xM tankage carried elsewhere aboard the ship.
- `CHJ Friction Heat Per Standard Jump` means the retained thermal load assigned to the xM loop under the current mass-friction law, not the full onboard ship heat budget.
- For those worked rows, installed rating is the exact dual-redundant coverage requirement under the current bubble law, decomposed into the largest practical backbone panels first and then into smaller contour panels down to the current `1 kW` floor.
- Falcon is still listed from its explicit `16` emitter anchor for field hardware and from the current shallow circular thermal approximation for cooldown scaling, because the appendix still does not carry a cleaner full envelope for that hull.

| Ship | Spec Basis | Installed Emitters | Installed Rating | xM Processed Per Standard Jump | Minimum Engine xM Reserve At Start | CHJ Friction Heat Per Standard Jump | Standard Jump Cooldown | Total Emitter Face Area | Total Installed Emitter Volume | Current Reading |
| --- | --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| SDF-1 Macross | Exact-coverage mixed suite: `72 x 20,000 kW + 1 x 1,000 kW + 8 x 100 kW + 58 x 1 kW` | 139 | 1,441,858 kW | 761.345 kg | 7,613.453 kg | 263,703 kJ | 360 s | 450,230.888 m^2 | 251,588.586 m^3 | First heavy-hull cooldown anchor and current capital mixed-suite fit; current standard hop still recycles in about six minutes while the exact-coverage installation eliminates leftover envelope waste. |
| UNSC Spirit of Fire | Exact-coverage mixed suite: `283 x 20,000 kW + 8 x 1,000 kW + 8 x 100 kW + 25 x 1 kW` | 324 | 5,668,825 kW | 2,993.202 kg | 29,932.021 kg | 1,190,892 kJ | 414 s | 1,770,132.782 m^2 | 989,148.494 m^3 | Current carrier-scale mixed fit; still a huge installation, but no longer trapped in the false all-`1 kW` emitter swarm. |
| UNSC Infinity | Exact-coverage mixed suite: `734 x 20,000 kW + 1 x 10,000 kW + 4 x 1,000 kW + 9 x 100 kW + 80 x 1 kW` | 828 | 14,694,980 kW | 7,757.056 kg | 77,570.556 kg | 2,880,893 kJ | 386 s | 4,588,616.836 m^2 | 2,564,114.668 m^3 | Current heavy-warship mixed fit; the 20 MW backbone dominates while smaller contour closures eliminate the remaining exact-coverage gaps. |
| White Base | Exact-coverage mixed suite: `6 x 20,000 kW + 2 x 1,000 kW + 5 x 100 kW + 54 x 1 kW` | 67 | 122,554 kW | 65.108 kg | 651.081 kg | 18,508 kJ | 297 s | 38,268.398 m^2 | 21,384.344 m^3 | Current small-carrier mixed fit; contour closures keep the hull out of the all-small-emitter trap without changing its hull-driven thermal cadence. |
| Discovery One | Exact-coverage mixed suite: `6 x 1,000 kW + 3 x 100 kW + 73 x 1 kW` | 82 | 6,373 kW | 4.304 kg | 43.043 kg | 547 kJ | 169 s | 1,990.017 m^2 | 1,112.019 m^3 | Current research-hull mixed fit; 1 MW panels remain the highest practical backbone tier under the present class palette. |
| Serenity | Exact-coverage mixed suite: `9 x 1,000 kW + 5 x 100 kW + 24 x 1 kW` | 38 | 9,524 kW | 6.412 kg | 64.122 kg | 1,091 kJ | 225 s | 2,973.940 m^2 | 1,661.835 m^3 | Current light irregular-hull mixed fit; it stays in the same general light-craft turnaround band as Falcon while cutting both part count and working xM burden. |
| Venator-class Star Destroyer | Exact-coverage mixed suite: `68 x 20,000 kW + 8 x 1,000 kW + 2 x 100 kW + 95 x 1 kW` | 173 | 1,368,295 kW | 723.359 kg | 7,233.590 kg | 242,534 kJ | 349 s | 427,260.294 m^2 | 238,752.641 m^3 | Current fleet-carrier mixed fit; the 20 MW backbone handles the broad hull faces while smaller contour closures cleanly finish the remainder. |
| Mega-class Star Destroyer Supremacy | Exact-coverage mixed suite: `1,393 x 1,000,000 kW + 5 x 100,000 kW + 2 x 20,000 kW + 7 x 1,000 kW + 4 x 100 kW + 88 x 1 kW` | 1,499 | 1,393,547,488 kW | 735,484.508 kg | 7,354,845.078 kg | 325,065,929 kJ | 459 s | 435,145,571.121 m^2 | 243,158,925.964 m^3 | Current titanic mixed fit; the titanic backbone collapses the megastructure count from `69,776` emitters to `1,499` while preserving exact coverage and keeping the plant honestly in the titanic band. |
| Millennium Falcon | Explicit Falcon anchor: `16 x 1 kW` emitters, `8` required | 16 | 16 kW | 0.015556 kg | 0.155560 kg | 160 kJ | 180 s | 4.996 m^2 | 2.792 m^3 | Explicit smallest-emitter anchor and first small-hull cooldown anchor under the current law. |

### Current First-Pass Infrastructure Binning and Spin-Up

- CX-013 now bins whole-drive infrastructure by installed total emitter rating rather than by hull genre alone, and it separately bins single-emitter hardware by per-emitter class rating.
- Under that pass, Falcon's locked `16 x 1 kW` installation is explicitly treated as `small` infrastructure and as `small` emitter hardware rather than as a `tiny` edge case.
- Standard-jump spin-up below uses the current first-pass priming law `M_prime = M_engine,start + rho_act,wet * (V_emit,tot + V_pipe,tot)` with `rho_act,wet = 0.03 kg/m^3`, `V_pipe,tot = chi_pipe * V_emit,tot`, and duty-cylinder-only `Q_act`.
- The listed times are therefore comparison-grade startup figures for the current `10 s` Sol-baseline Earth-to-Mars hop, not final manufacturer brochures.

| Ship | Backbone Emitter Bin | FTL Infrastructure Bin | First-Pass Cylinder Suite | Duty Activation Throughput | Approx. Wet-Line Prime Mass | Approx. Standard Jump Spin-Up | Current Reading |
| --- | --- | --- | --- | ---: | ---: | ---: | --- |
| Millennium Falcon | Small | Small | `1 duty + 1 spare tiny cylinder` | `0.005 kg/s` | `0.260 kg` | `52.0 s` | Falcon now fixes the lower edge of the `small` plant band; `tiny` remains reserved for sub-Falcon auxiliaries. |
| Discovery One | Large | Small | `3 duty + 1 spare medium cylinders` | `1.5 kg/s` | `84.744 kg` | `56.5 s` | Small-hull infrastructure can still carry a `large` emitter backbone once the plant and the individual emitter tiers are treated separately. |
| Serenity | Large | Small | `4 duty + 1 spare medium cylinders` | `2.0 kg/s` | `126.441 kg` | `63.2 s` | The irregular freighter stays in the `small` plant band even though its practical backbone emitter tier is already `large`. |
| White Base | Capital | Medium | `5 duty + 1 spare large cylinders` | `25 kg/s` | `1,517.147 kg` | `60.7 s` | Carrier geometry pushes the ship into a `capital` emitter backbone before total plant size leaves the `medium` band. |
| Venator-class Star Destroyer | Capital | Large | `6 duty + 1 spare huge cylinders` | `300 kg/s` | `17,977.459 kg` | `59.9 s` | This is the first clean fleet-carrier `large` plant fit under the current cylinder ladder. |
| SDF-1 Macross | Capital | Large | `6 duty + 1 spare huge cylinders` | `300 kg/s` | `18,934.939 kg` | `63.1 s` | The heavy-hull calibration anchor now also reads as a `large` plant with a `capital` emitter backbone. |
| UNSC Spirit of Fire | Capital | Huge | `3 duty + 2 spare capital cylinders` | `1,500 kg/s` | `80,378.594 kg` | `53.6 s` | This is the first clean `N+2` heavy-carrier fit under the current platform doctrine. |
| UNSC Infinity | Capital | Capital | `6 duty + 2 spare capital cylinders` | `3,000 kg/s` | `231,417.436 kg` | `77.1 s` | The current large warship upper band now lands in a true `capital` plant rather than merely a `large` one. |
| Mega-class Star Destroyer Supremacy | Titanic | Titanic | `6 duty + 2 spare titanic cylinder banks` | `300,000 kg/s` | `25,591,764.525 kg` | `85.3 s` | This is the first clean titanic-on-titanic fit in the sample set: the plant and the emitter backbone now agree that the hull is a megastructure. |

### Current First-Pass Hull Frame Readings

- CX-013 now treats these names as hull-frame classes rather than as mission labels.
- Drone through bomber remain valid smallcraft descriptors in the setting, but they now sit below the current minimum shipboard FTL envelope and are ignored by the present FTL frame ladder.
- A civilian ship can therefore ride a bantam, clipper, transport, freighter, or even destroyer frame without becoming a military mission type by definition.
- Gross-tonnage marketing bands are intentionally broader than frame classes, so multiple frames can share one weight group and later diverge by mount-point families and internal-module ceilings.
- The readings below are Leviathan-side frame matches for the comparison corpus, not retroactive franchise renamings inside the source settings.

| Ship | Likely Leviathan Hull Frame | FTL Infrastructure Bin | Backbone Emitter Bin | Current Reading |
| --- | --- | --- | --- | --- |
| Millennium Falcon | Clipper | Small | Small | Fast packet or courier anchor at the lower edge of the `small` plant band |
| Discovery One | Scout | Small | Large | Long-range research hull with scout endurance and an oversized small-hull emitter backbone |
| Serenity | Transport | Small | Large | Civilian transport frame using a `small` plant with a `large` emitter backbone |
| White Base | Carrier | Medium | Capital | Lower-band carrier anchor |
| Venator-class Star Destroyer | Carrier | Large | Capital | Fleet carrier anchor |
| SDF-1 Macross | Dreadnaught | Large | Capital | Overbuilt heavy war frame with carrier-scale internal volume |
| UNSC Spirit of Fire | Carrier | Huge | Capital | Heavy carrier anchor |
| Enterprise (NX-01) | Scout | Small | Large | Early interstellar explorer anchor |
| USS Enterprise (NCC-1701) | Cruiser | Small | Large | Mid-scale cruiser-side explorer anchor |
| USS Enterprise (NCC-1701-D) | Cruiser | Medium | Capital | Flagship explorer-combatant anchor |
| USS Enterprise (NCC-1701-E) | Cruiser | Medium | Capital | Heavy late-era cruiser-side explorer anchor |
| Battlestar Galactica (TRS) | Dreadnaught | Large | Capital | Heavy war frame with carrier volume |
| Imperial-class Star Destroyer | Battleship | Large | Capital | Wedge battleship anchor |
| Resurgent-class Star Destroyer | Battlecruiser | Huge | Capital | Late-era heavy line-hull anchor |
| Xyston-class Star Destroyer | Battleship | Huge | Capital | Heavy line-battle anchor |
| Death Star | Worldship | Titanic | Titanic | Worldship-scale anchor |
| UNSC Infinity | Capital | Capital | Capital | Upper heavy-warship anchor where plant scale matters more than silhouette |
| Mega-class Star Destroyer Supremacy | Titan | Titanic | Titanic | Titan anchor; current doctrine now separates it cleanly from the larger Death Star worldship anchor |

### Current First-Pass Gross-Tonnage Marketing Groups

- Current Leviathan-side marketing now reads normalized gross tonnage `M_gross,norm = rho_ref * V_env` on broad logarithmic bands rather than on one linear tonnage ladder.
- These weight groups are not frame identities. They are market shorthand for how much ship is being bought, crewed, maintained, or freighted before frame-specific mount and module limits are considered.
- Because of that split, two ships can share one marketed tonnage group and still land in different frame classes.

| Gross-Tonnage Group | Normalized Gross Tonnage | Current Anchor Ships | Current Reading |
| --- | --- | --- | --- |
| Bantam-weight | `10^2 <= M_gross,norm < 10^4 t` | Millennium Falcon, Discovery One, Serenity | Lowest current FTL market band and future home of bantam tug or tender frames |
| Light-hull | `10^4 <= M_gross,norm < 10^6 t` | White Base, Enterprise (NX-01), USS Enterprise (NCC-1701) | Lower service-capital and small-carrier band |
| Medium-hull | `10^6 <= M_gross,norm < 10^8 t` | Venator-class Star Destroyer, SDF-1 Macross, USS Enterprise (NCC-1701-D), USS Enterprise (NCC-1701-E), Battlestar Galactica (TRS), Imperial-class Star Destroyer | Major line-hull and fleet-carrier band |
| Heavy-hull | `10^8 <= M_gross,norm < 10^10 t` | UNSC Spirit of Fire, UNSC Infinity, Resurgent-class Star Destroyer, Xyston-class Star Destroyer | First-rank heavy ship band where plant scale starts to dominate marketing |
| Titanic-hull | `M_gross,norm >= 10^10 t` | Mega-class Star Destroyer Supremacy, Death Star | Megastructure band; worldships remain clustered titanic systems rather than any larger singular hardware tier |

### Current First-Pass Density Families

- Density family is an author-side planning modifier applied on top of frame class and gross-tonnage group, not a replacement for either.
- A ship can therefore be marketed and discussed as `light bantam`, `medium bantam`, or `heavy bantam` without changing its underlying frame identity.
- These bands are estimation tools for missing data. They do not force every published source ship to land numerically on its chosen family target after crude envelope-boxing and cross-franchise cleanup.

| Density Family | Planning Density | Current Example Readings | Current Reading |
| --- | ---: | --- | --- |
| Light | `0.072096 t/m^3` | SDF-1 Macross, Trek Enterprise line, many explorer and carrier hulls | Favor large internal service voids, bay volume, or habitat space |
| Medium | `0.096128 t/m^3` | Neutral default family when role and construction cues do not strongly point elsewhere | Use for first-pass normalization when no better cue is available |
| Heavy | `0.120160 t/m^3` | Battlestar Galactica, dense line combatants, machinery-heavy industrial hulls | Favor armor, machinery, ammunition, or industrial plant density |

- When dimensions are known but mass is poor or contradictory, use `M_family = rho_family * V_env`.
- When mass is known but dimensions are missing, use `V_family = M_pub / rho_family`, then back out provisional envelope dimensions from the chosen shape assumption.
- SDF-1 remains the current `rho_ref` anchor for continuity, but it is now also treated as a light-density dreadnaught in engineering reading because the ship is dominated by large hollow internal volume.

### Current Missing Hull Frame References

- The current corpus now has direct or working anchors for `clipper`, `scout`, `transport`, `carrier`, `dreadnaught`, `capital`, `titan`, and `worldship`.
- Drone through bomber are intentionally excluded from this gap table because current doctrine treats them as below the minimum shipboard FTL envelope.
- Eve Online is now the first candidate pool for many of the remaining unfilled middle bands, with the current pass preferring Amarr hulls wherever a clean analogue exists, while Death Star is fixed as the current worldship anchor.
- When EVE hulls are imported into Leviathan as crewed-service references, their published capsuleer-optimized forms should be scaled up by at least `2x` in linear dimensions before frame and gross-tonnage assignment. In first order that implies about `8x` envelope volume and normalized gross tonnage relative to the published one-pilot shell.
- The Trek Enterprise line is now treated as cruiser-side rather than corvette- or frigate-side when it is used as a Leviathan comparison source.

| Hull Frame Class | Current Reference Status | Suggested Candidate Pool | Current Gap Reading |
| --- | --- | --- | --- |
| Bantam | Missing | User-side `Rifter` sanity check, then Amarr `Sentinel` or `Crucifier` after crewed upscale | User-directed tugboat and yard-tender baseline; should become the smallest practical FTL utility frame |
| Cutter | Missing | Amarr `Magnate` or `Inquisitor` after crewed upscale | Need a compact service hull between bantam and clipper |
| Corvette | Missing | Amarr `Punisher` or `Tormentor` after crewed upscale | Need the first compact FTL combatant and escort spine |
| Freighter | Missing | Amarr `Sigil`, `Bestower`, `Prorator`, `Impel`, or `Providence` after crewed upscale | Need a broad-beam cargo anchor distinct from transport |
| Frigate | Missing | Amarr `Coercer` or `Dragoon` after crewed upscale | Need a clean escort baseline distinct from cruiser-scale explorers |
| Destroyer | Missing | Amarr `Omen`, `Maller`, `Arbitrator`, or `Augoror` after crewed upscale | Need a full-envelope heavy escort or line-combat anchor |
| Cruiser | Anchored | USS Enterprise (NCC-1701-D) | Multi-era cruiser-side explorer anchors now established |
| Battlecruiser | Anchored | Resurgent-class Star Destroyer | Heavy line-hull anchor established |
| Battleship | Anchored | Imperial-class Star Destroyer | Wedge battleship anchor established |
| Industrial Complex | Missing | No clean Amarr analogue in the current verified pool; keep the gap open after the Amarr pass | Need a mobile yard, factory-habitat, or convoy-foundry reference |

### Pending Partial-Data FTL Spec Rows

- The remaining partial-data anchors stay in the comparison corpus, but they cannot yet receive a credible derived emitter count without importing geometry the appendix does not actually have.
- Keeping these rows visible is still useful, because it separates missing source geometry from actual CHJ doctrine.

| Ship | Current Anchor Status | Blocking Data Gap | Interim Reading |
| --- | --- | --- | --- |

### Current FTL Spec Sanity Check

- The current main table now carries an exact-coverage mixed-suite pass for every full-envelope sample hull, so the comparison no longer pretends that practical ship fits remain on the all-`1 kW` diagnostic baseline.
- The old all-`1 kW` baseline still survives where it is useful: in the SDF single-class comparison below, which remains the clean diagnostic view of class scaling under fixed hull geometry.
- Under the current class palette, the mixed-suite pass drops full-envelope emitter counts from `6,373 to 1,393,547,488` on the all-`1 kW` baseline down to `16 to 1,499` across the current derivable set, and it cuts throughput-equivalent standard-jump xM demand by about `30.5 to 45.7%` across the same sample set.
- The new first-pass infrastructure ladder now sorts the same full-envelope sample from `small` through `titanic`, with Falcon explicitly anchoring `small` and `tiny` left below the current locked shipboard corpus.
- The new hull-frame ladder is structural rather than mission-bound. A ship can be civilian, industrial, or military while still riding the same bomber, transport, freighter, carrier, or titan frame.
- The Supremacy row is still behaving correctly as a stress test, but it is no longer a part-count pathology. Under the titanic emitter extension its exact-coverage fit drops from `69,776` emitters to `1,499` while preserving installed rating, thermal load, and plant bin.
- Under the current engine-local reserve and wet-line priming law, approximate standard-jump spin-up now lands in roughly the `52 to 85 s` band across the fitted sample set.
- Supremacy now confirms the opposite lesson: megastructures need both `titanic` plants and `titanic` emitters, and once both tiers exist the doctrine stops visibly fighting the hull.
- Falcon remains the only partial-data anchor with a real locked FTL installation, because it is carrying an explicit emitter count and the current first-pass thermal model now also carries an explicit shallow-circular cooling approximation for it.
- Cooldown scaling is no longer undefined in first pass. Under the current law, standard-jump cooldown depends on normalized hull mass raised to a sublinear exponent and on available ship surface area.
- The new thermal model also decouples retained jump heat from emitter class in first order. Emitter class still changes xM throughput-equivalent working mass and installation burden, but the dominant retained heat is now treated as CHJ friction against hull mass.
- The working selection rule is now mixed-suite by default: large hulls should use the biggest practical backbone emitters they can fit cleanly, then use smaller contour emitters wherever local geometry or redundancy zoning would otherwise waste envelope area.
- Under the current `10 * M_jump,eq` startup assumption, immediately available engine-side working xM spans from about `0.155560 kg` on Falcon to about `13,548,378.356 kg` on Supremacy. That spread is a direct signal that reserve doctrine and emitter-class doctrine cannot stay decoupled forever.

### SDF-1 Dual-Redundant Emitter Comparison

- Naive box surface area: `2,264,864 m^2` using `2 * (L * W + L * H + W * H)` for a `1,210 x 496 x 312 m` envelope.
- Current emitter doctrine fixes `R_red = 2`, so every listed suite assumes dual redundancy rather than bare closure.
- Current bubble law is `d_i = 2 * sqrt(P_i / 1 kW) m`, which makes coverage patch scale linearly with class rating.
- Current emitter package law is a Falcon-derived radiator panel stack: panel face area scales linearly with class, stack depth stays at the Falcon anchor `0.5588 m`, and `V_emit = 0.174489 m^3/kW * P_i`.
- This diagnostic comparison still stops at `20,000 kW`, because the new `100,000` and `1,000,000 kW` titanic emitter banks are reserved for titanic plants and are not treated as practical hardware for the SDF-1 `large` plant anchor.

| Emitter Class | Bubble Diameter | Panel Face Side | Panel Face Area | Stack Depth | Package Volume Per Emitter | Installed Emitters at Dual Redundancy | Total Emitter Face Area | Total Installed Emitter Volume | Total Emitter Rating | `phi_g` | xM Throughput-Equivalent Per Jump | CHJ Friction Heat Per Jump |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| 1 kW | 2.000 m | 0.559 m | 0.312 m^2 | 0.559 m | 0.174 m^3 | 1,441,858 | 450,230.888 m^2 | 251,589.020 m^3 | 1,441,858 kW | 0.35 kg/kWh | 1,401.806 kg | 263,703 kJ |
| 100 kW | 20.000 m | 5.588 m | 31.226 m^2 | 0.559 m | 17.449 m^3 | 14,419 | 450,244.003 m^2 | 251,596.349 m^3 | 1,441,900 kW | 0.28 kg/kWh | 1,121.478 kg | 263,703 kJ |
| 1,000 kW | 63.246 m | 17.671 m | 312.257 m^2 | 0.559 m | 174.489 m^3 | 1,442 | 450,275.228 m^2 | 251,613.798 m^3 | 1,442,000 kW | 0.24 kg/kWh | 961.333 kg | 263,703 kJ |
| 10,000 kW | 200.000 m | 55.880 m | 3,122.574 m^2 | 0.559 m | 1,744.895 m^3 | 145 | 452,773.288 m^2 | 253,009.713 m^3 | 1,450,000 kW | 0.21 kg/kWh | 845.833 kg | 263,703 kJ |
| 20,000 kW | 282.843 m | 79.026 m | 6,245.149 m^2 | 0.559 m | 3,489.789 m^3 | 73 | 455,895.862 m^2 | 254,754.608 m^3 | 1,460,000 kW | 0.19 kg/kWh | 770.556 kg | 263,703 kJ |

- This remains a naive surface-area pass, not a finished emitter-placement design.
- Because the current bubble law makes coverage patch scale linearly with `kW`, total installed emitter rating stays near `1.44 GW` across the compared single-class suites.
- Because the Falcon panel law also scales linearly with `kW`, total installed emitter face area stays near `450,000 to 456,000 m^2` and total installed emitter volume stays near `0.252 to 0.255 million m^3` across the same suites.
- Larger emitter classes are still favored because they collapse part count and ride down the size-based feed-demand curve at the same time.
- The geometry law now makes that preference physically legible: a single `20,000 kW` emitter presents a `79.026 m` square radiator face over a `0.559 m` stack and occupies `3,489.789 m^3`, which is a serious capital-hull installation rather than a casual light-craft upgrade.
- The listed xM quantities remain throughput-equivalent working masses for the 10 second Sol-baseline Earth-to-Mars hop, not final statements of total onboard xM inventory.
- Under the current thermal-friction law, retained standard-jump heat is treated as a hull-mass effect rather than an emitter-power effect, so all single-class rows share the same SDF thermal load and differ mainly in xM working mass, part count, and installation geometry.
- Mixed suites are now the expected practical doctrine once explicit redundancy zoning, overlap penalties, and real layout constraints are introduced. The single-class rows remain useful as comparison bounds rather than as preferred final installations.

### Worked Mixed-Suite Anchor Fits

- These remain useful anchor illustrations inside the now-complete full-envelope mixed-suite pass, not finished yard blueprints.
- Falcon remains the locked smallest-emitter anchor, so Serenity is still used here as the light irregular-hull worked example rather than retroactively replacing the Falcon anchor.
- Because both coverage patch and panel package scale linearly with installed `kW`, exact-coverage mixed suites hold total installed face area and total package volume at the same values shown in the main comparative table while sharply reducing emitter count and xM demand relative to the all-`1 kW` diagnostic baseline.

| Ship | Backbone Suite | Contour Suite | Total Emitters | Installed Rating | xM Processed Per Standard Jump | Minimum Engine xM Reserve At Start | CHJ Friction Heat Per Standard Jump | Standard Jump Cooldown | Total Emitter Face Area | Total Installed Emitter Volume | Current Reading |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| SDF-1 Macross | `72 x 20,000 kW` | `1 x 1,000 kW + 8 x 100 kW + 58 x 1 kW` | 139 | 1,441,858 kW | 761.345 kg | 7,613.453 kg | 263,703 kJ | 360 s | 450,230.888 m^2 | 251,588.586 m^3 | Current exact-coverage capital anchor; the 20 MW backbone handles the broad faces while the smaller contour tiers close the remaining coverage to the current `1 kW` floor. |
| Serenity | `9 x 1,000 kW` | `5 x 100 kW + 24 x 1 kW` | 38 | 9,524 kW | 6.412 kg | 64.122 kg | 1,091 kJ | 225 s | 2,973.940 m^2 | 1,661.835 m^3 | Current exact-coverage light-hull anchor; 1 MW panels stay within the ship's scale while smaller contour tiers close the irregular remainder without wasting envelope area. |

- SDF-1 needs about `4,529,728 m^2` of dual-redundant nominal coverage in the current box pass. The current exact-coverage mixed suite provides about `4,529,730.500 m^2`, cuts installed emitter count from `1,441,858` to `139`, and lowers throughput-equivalent standard-jump xM from `1,401.806 kg` to `761.345 kg` while leaving hull-driven jump heat and cooldown unchanged.
- Serenity needs about `29,920 m^2` of dual-redundant nominal coverage in the current box pass. The current exact-coverage mixed suite provides about `29,920.528 m^2`, cuts installed emitter count from `9,524` to `38`, and lowers throughput-equivalent standard-jump xM from `9.259 kg` to `6.412 kg` while leaving hull-driven jump heat and cooldown unchanged.
- These remain comparison-grade fits rather than final placement drawings. Real hull zoning, armored coffering, service clearances, and overlap penalties can still move the exact class mix.


### Full-Envelope Anchors

| Ship | Franchise | Dimensions (m) | Envelope Volume (m^3) | Published Mass (t) | Published rho_app (t/m^3) | Normalized Mass at rho_ref (t) | Density Family | Crew or Population Note | Current Use |
| --- | --- | --- | ---: | ---: | ---: | ---: | --- | --- | --- |
| SDF-1 Macross | Macross | 1,210 x 496 x 312 | 187,249,920 | 18,000,000 | 0.096128 | 13,502,234 | Light | Published complement varies by pre-refit and post-refit context | Calibration anchor |
| UNSC Spirit of Fire | Halo | 2,500 x 856 x 689 | 1,474,460,000 | 44,000,000 | 0.029841 | 141,737,203 | Light | 11,350 total personnel | Mass-light military carrier cross-check |
| UNSC Infinity | Halo | 5,694.2 x 833.3 x 1,041.2 | 4,940,469,906.63 | 907,000,000 | 0.183586 | 474,918,538 | Heavy | 17,151 pre-refit; 18,262 post-refit, excluding Spartans | Heavy warship upper-band cross-check |
| White Base | Mobile Suit Gundam | 262 x 202.5 x 93 | 4,934,115 | 68,000 | 0.013782 | 474,308 | Light | Published crew not fixed in the current source pass | Small carrier lower-band cross-check |
| Discovery One | 2001: A Space Odyssey | 140.1 x 16.7 x 17 | 39,774.39 | 5,440 | 0.136771 | 3,823 | Medium | Deep-space expedition hull | Deep-space research hull cross-check |
| Serenity | Firefly | 82 x 52 x 24 | 102,336 | - | - | 9,837 | Light | 18 passengers cited in the current source pass | Small civilian service hull |
| Venator-class Star Destroyer | Star Wars | 1,137 x 548 x 268 | 166,984,368 | - | - | 16,051,909 | Medium | Population volume 7,400 | Fleet carrier geometry anchor |
| Mega-class Star Destroyer Supremacy | Star Wars | 13,234 x 60,543 x 3,975 | 3,184,873,596,450 | - | - | 306,156,204,158 | Titanic | Population volume 2,225,000 | Megastructure stress-test hull |
| Enterprise (NX-01) | Star Trek | 225 x 135.8 x 33.3 | 1,014,160 | - | - | 97,529 | Medium | Crew 83 (standard complement) | Early interstellar explorer, promoted to full-envelope anchor (medium-density family; primitive military architecture) |
| USS Enterprise (NCC-1701) | Star Trek | 288.6 x 127 x 85 | 3,116,199 | 190,000 | 0.06096 | 299,653 | Medium | Crew 430 (standard complement); Height: 85 m (midpoint of 70–100 m) | promoted to full-envelope anchor (medium-density family) |
| USS Enterprise (NCC-1701-D) | Star Trek | 641 x 470 x 151 | 45,497,570 | 4,960,000 | 0.1090 | 3,277,393 | Light | Crew and passengers: 1,012; Decks: 42 | promoted to full-envelope anchor (light-density family) |
| USS Enterprise (NCC-1701-E) | Star Trek | 685.3 x 250.6 x 88.2 | 15,140,234 | 3,205,000 | 0.2118 | 1,091,563 | Light | Decks: 24 | promoted to full-envelope anchor (light-density family) |
| Battlestar Galactica (TRS) | Battlestar Galactica | 1,438.6 x 536.8 x 183.3 | 141,654,234 | - | - | 17,027,234 | Heavy | Crew: ~2,800 | promoted to full-envelope anchor (heavy-density family) |
| Imperial-class Star Destroyer | Star Wars | 1,600.52 x 985.17 x 455.40 | 717,667,964 | 40,000,000 | 0.05574 | 68,999,964 | Medium | Crew: 9,235 officers, 27,850 enlisted, 9,700 stormtroopers | promoted to full-envelope anchor (medium-density family) |
| Millennium Falcon | Star Wars | 35 x 25.6 x 7.8 | 6,998.4 | - | - | 505 | Light | Crew: 2–4, passengers: 6–30 | Small freighter, promoted to full-envelope anchor (light-density family) |
| Resurgent-class Star Destroyer | Star Wars | 2,915.81 x 1,483.5 x 496.89 | 2,151,963,964 | - | - | 206,885,964 | Medium | Crew: 19,000 officers, 55,000 enlisted, 8,000+ stormtroopers | Large late-era battleship-carrier, promoted to full-envelope anchor (medium-density family) |
| Xyston-class Star Destroyer | Star Wars | 2,406 x 1,480 x 682 | 2,426,894,560 | - | - | 233,234,000 | Medium | Population volume 29,585 | promoted to full-envelope anchor (medium-density family) |
| Death Star | Star Wars | Diameter 160,000 (sphere) | 2,144,660,584,850 | - | - | 206,162,000,000 | Titanic | Staffing and population vary by source | Spherical battlestation-worldship, promoted to full-envelope anchor (titanic-density family) |

### Partial-Data Anchors

| Ship | Franchise | Current Published Data Held In This Pass | Current Use |
| --- | --- | --- | --- |

### Current Calibration Reading

- The current calibration constant is `rho_ref = 0.096128 t/m^3`, fixed by SDF-1 Macross standard displacement.
- The current corpus stands at 18 ships: 18 full-envelope anchors and 0 partial-data anchors.
- The first explicit cruise-speed targets now fixed in the appendix are Sol-baseline values: 108 m/s for SDF-1 Macross and about 300 m/s for Millennium Falcon.
- The first explicit thermal-recovery targets now fixed in the appendix are about `3 minutes` on a Falcon-scale small hull and about `6 minutes` on an SDF-1-scale heavy hull for the standard Sol-baseline Earth-to-Mars hop.
- AX-004 now carries a first-pass comparative FTL spec table for the current sample set: every current full-envelope row now uses an exact-coverage worked mixed-suite fit, Falcon uses its explicit `16` emitter anchor, every current row quotes a minimum startup engine reserve of `10 * M_jump,eq`, and the remaining partial-data anchors stay pending until their geometry improves.
- AX-004 now also carries a first-pass gross-tonnage marketing pass keyed to `M_gross,norm = rho_ref * V_env` and read logarithmically, so broad marketed weight groups can coexist with more specific frame classes.
- AX-004 now also carries first-pass light, medium, and heavy density families at `0.75`, `1.00`, and `1.25` times `rho_ref`, plus a dimension-first rule when published mass and envelope data disagree.
- AX-004 now also carries a first-pass thermal law: effective cooling scales linearly with ship surface area, retained standard-jump CHJ friction heat scales with normalized ship mass by `n_H = 0.730583`, and the anchor pair of Falcon and SDF-1 fixes the shared coefficients.
- Under current dual-redundant doctrine and the current bubble law, the SDF-1 naive emitter pass requires on the order of `1.44 GW` of installed emitter rating regardless of single-class choice, with larger emitter classes mainly reducing part count and xM demand.
- Under current dual-redundant doctrine, the current bubble law, and the Falcon-derived panel emitter law, the SDF-1 naive emitter pass requires on the order of `1.44 GW` of installed emitter rating, about `450,000 to 456,000 m^2` of emitter face area, and about `0.252 to 0.255 million m^3` of installed emitter volume regardless of single-class choice.
- The same comparative FTL spec table now supports the working emitter-selection rule: practical ships should use mixed suites so large backbone panels handle broad hull coverage while smaller contour panels reduce wasted envelope area and close geometry that oversized emitters would fit poorly.
- AX-004 now carries exact-coverage worked mixed-suite fits across the full-envelope sample set, with SDF-1 Macross and Serenity retained as the clearest anchor examples for capital and light irregular hulls.
- Under the current thermal-friction law, the standard-jump SDF-1 heat load is about `263,703 kJ` and the corresponding cooldown is about `360 s` regardless of single-class emitter choice in the naive pass.
- On the current curve, a fully dual-redundant all-`1 kW` SDF-1 suite still implies about `1,401.806 kg` of throughput-equivalent xM per standard jump and therefore about `14,018.064 kg` of minimum startup engine reserve, while moving to very large emitter classes can push that same jump closer to `770.556 kg` and about `7,705.556 kg` of startup reserve without materially changing retained thermal friction heat.
- The exact-coverage full-envelope mixed-suite pass keeps that same thermal-law behavior while reducing emitter counts from `6,373 to 1,393,547,488` down to `38 to 1,499` across the exact-coverage mixed-suite rows, while Falcon remains on its explicit `16` emitter anchor, and it cuts throughput-equivalent standard-jump xM by about `30.5 to 45.7%` across the current sample set.
- The current mass-known full-envelope sample spans `0.013782 t/m^3` to `0.183586 t/m^3` in published apparent density.
- The unweighted mean of that same sample is `0.092022 t/m^3`, which keeps the SDF-1 baseline near the center of the currently usable measured set rather than at an obvious edge case.
- Published franchise masses therefore remain valuable as spread checks, but not as a clean shared baseline.
- The normalized gross-tonnage anchors now run from about `711.122 t` on Millennium Falcon through about `3.06156 * 10^11 t` on Supremacy, while a `160 km` spherical Death Star lands at about `2.06162 * 10^14 t` under the same reference-density reading.
- The present corpus is intentionally mixed across carrier hulls, line warships, exploratory vessels, civilian service hulls, megastructural command ships, and now an explicit worldship-scale anchor so later CHJ doctrine is not tuned only to one fictional navy's habits.
- The present corpus is still thin through much of the bantam-to-battleship middle, especially where future mount-point and internal-module doctrine will need cleaner frame anchors.
- The current middle-band acquisition queue now leans Amarr-first for EVE imports, with a standing rule that capsuleer hulls should be upscaled to crewed-service dimensions before they are marketed by Leviathan gross tonnage.
- The new density-family layer now gives the project a cleaner way to interpolate missing volume from known mass or missing mass from known volume without pretending every fictional universe publishes compatible displacement logic.
- Under the current reading, SDF-1 and the Trek Enterprise line are treated as light-density service hulls, while Battlestar Galactica is the clearest current heavy-density warship cue in the partial-data tier.
- The Trek Enterprise line is now being read as cruiser-side in the candidate queue rather than as a corvette or frigate solution.
- Under the current cap, any future worldship reference should demonstrate clustered titanic infrastructure rather than a notional hardware tier above titanic.
- The Star Trek Enterprise lineage is now retained explicitly in the partial-data tier so the corpus preserves a multi-era exploration-hull baseline even before exact beam, height, and tonnage lines are cleaned up.
- The Supremacy row is useful precisely because it is unreasonable. It pressures the upper bound of any later throughput and handling model, even though its raw envelope should not be mistaken for true solid material volume.


## xM Stand-In Physical Properties

For all engineering calculations in this appendix, the following real-world substances are used as stand-ins for the physical properties of active xM (exotic matter):

- **Density and Viscosity:**
	- *Diesel fuel* is used as the reference for xM density and viscosity.
		- Typical density: 0.82–0.85 g/cm³ (820–850 kg/m³)
		- Viscosity: Use standard diesel values for hydraulic and flow modeling.

- **Thermal Capacity (Specific Heat):**
	- *Liquid lithium* is used as the reference for xM thermal properties.
		- Specific heat capacity: $c_{xM} \approx 3.58$ kJ/kg/K (at ~500 K)
		- Use this value for all calculations involving heat absorption, temperature rise, and cooldown modeling.

These stand-ins are chosen for their industrial relevance:

If later project work establishes different canonical values for xM properties, this section should be updated accordingly.

---
**To-Do:**
We still need to establish and solve for cylinder volumes. Specifically, we must solve for the wet priming time as a function of engine size and cylinder counts. This calculation is pending and should be addressed in a future revision of this appendix.

## xM Phase Transitions (Stand-In: Liquid Lithium)


For the purposes of engineering and thermal modeling, xM is assumed to have phase transitions as follows:

- **Melting point (solid → liquid):** −20°C (−4°F) or lower (xM remains liquid at all human-habitable temperatures)
- **Boiling point (liquid → gas):** 1,342°C (2,448°F) (as per liquid lithium stand-in)

**Operational Range:**
- Below −20°C: xM is solid (rare in normal operation; avoid subcooling)
- −20°C to 1,342°C: xM is liquid (normal operating range for FTL system and all habitable environments)
- Above 1,342°C: xM is gaseous (abnormal, emergency, or failure state)

This ensures xM is always liquid in shipboard and planetary environments, while retaining the high boiling point of liquid lithium for thermal modeling. If later project work establishes different canonical values for xM, update this section accordingly.

### Operational Hazard: xM Solidification in Space

Because xM has a melting point of −20°C (−4°F), any xM that leaks into deep space (ambient temperature ~−270°C) will rapidly freeze into a solid. This creates several operational and safety hazards:

- Leaked xM can solidify on hull surfaces, in vents, or around external piping, potentially clogging or damaging equipment.
- Solid xM may form hazardous debris, complicating recovery, cleanup, or salvage operations.
- Maintenance protocols must account for the risk of solidified xM in exposed environments, especially during EVA or hull repairs.

This behavior should be considered in all engineering, safety, and emergency procedures involving xM handling and containment.

---
## Material Implications

## FTL System Architecture (Summary)


### Why Discharge and Reactivate xM?

Active xM must be discharged and reactivated after each jump because its CHJ coherency is fixed at the moment of activation, binding it to the ship’s position and local spacetime. If reused after a jump, the xM’s imprint disagrees with the ship’s new position. In H-Space, this causes the active xM to be displaced to its old location and then accelerate toward the ship’s current position at the speed of light, carrying the density and mass of diesel fuel.

The resulting collision between the xM and the ship is so violent—given the relativistic speed, mass, and the known phase transition temperatures of xM—that both the ship and the xM are instantly reduced to high-temperature plasma and debris. The FTL jump technically resolves, but the ship is destroyed: its remains and the xM plasma are ejected from H-Space almost instantly at the point of loss of field (e.g., the intermediate stop). The xM plasma, along with any debris carried along, continues to the intended destination, where it arrives as a destructive burst of plasma and wreckage. This is not merely a failed jump, but a catastrophic event with both the ship and its xM violently annihilated in the process.

This model ensures that the no-reuse rule is a direct, catastrophic consequence of the underlying math and physics of CHJ coherency and galactic-relative imprinting. (See CX-013 for full rationale.)

Note: Future engineering may require tracking discharge time as a function of xM volume and system design.

The standard FTL system architecture is as follows (see CX-013 for full diagram and flow):

- **FTL Engine(s):** Activate and pressurize xM, feeding the Active xM Network (AXN).
- **Active xM Network (AXN):** Distributes active xM to emitters and the Discharge Module.
- **Emitters:** Generate the Intrinsic Coupling Field; connect to the HURL (Hot Unused Return Line) network.
- **HURL:** Carries heated, unused xM to a heat exchanger or thermal battery.
- **Heat Exchanger / Thermal Battery:** Removes waste heat; cooled xM is routed to the Discharge Module.
- **Discharge Module:** Collects xM from both the AXN and the cooling path, returning it to the FTL engine(s).

This closed-loop system ensures efficient cycling, cooling, and reactivation of xM, with clear separation between the main active loop and the hot return/cooling path. All modules are critical for safe, repeatable FTL operation.

- Later CHJ engineering constants should be discussed against normalized mass classes when cross-franchise comparison matters more than franchise-native technobabble.
- xM drag and coupling stress should be thought of as acting on an inhabited service hull, not merely on a romanticized dry structural number.
- Early speed fitting now has a declared spread between very heavy capital-hull cruise behavior and very fast light-hull cruise behavior.
- That early speed fitting is environment-dependent, because each system's Local Mass Rating alters the drag a ship must overcome.
- Early jump-cadence fitting now includes explicit thermal recovery anchors for Falcon-scale small craft and SDF-1-scale heavy hulls.
- Early emitter fitting now includes a dual-redundant SDF-1 comparison pass built from naive hull surface area rather than bespoke geometry.
- Current thermal fitting now treats retained jump heat as CHJ friction against normalized hull mass and cooling capacity as surface-limited, giving larger hulls some thermal economy of scale without making them thermally free.
- Large carriers and city-ships can now be compared to survey or freighter hulls without pretending their published universes measure mass the same way.
- Small civilian hulls remain necessary in the corpus so the CHJ rewrite does not silently become a doctrine written only for battleships.
- Partial-data anchors preserve useful role and scale diversity without forcing the project to invent false beam, height, or tonnage figures.

## Catastrophic Energy Release: SDF-1/xM Relativistic Collision

If a ship like the SDF-1 attempts to reuse active xM for a second jump (e.g., Earth→Mars, then Mars→Jupiter), the resulting relativistic collision between the xM and the ship releases an extraordinary amount of energy.

- **xM processed per jump:** $m_{xM} = 761.345$ kg
- **SDF-1 published mass:** $m_{ship} = 18,000,000,000$ kg

The total available energy for a head-on relativistic collision is:

$$
E_{total} \approx (m_{xM} + m_{ship}) c^2
$$

Where $c = 3 \times 10^8$ m/s. Plugging in the values:

$$
E_{total} \approx (761.345 + 18,000,000,000) \times (3 \times 10^8)^2 \\
E_{total} \approx 1.62 \times 10^{27} \text{ J}
$$

This is equivalent to about **387 trillion megatons of TNT** ($1 \text{ megaton TNT} = 4.184 \times 10^{15}$ J).

#### Planetary Consequences

For perspective, this energy is many orders of magnitude greater than the Chicxulub impactor (dinosaur extinction event, $\sim$100 million megatons) or the total energy output of the Sun in a few seconds. If the destination is near a planet like Jupiter or one of its moons, the impact would:

- Vaporize the ship, xM, and any nearby matter into plasma
- Create a fireball and shockwave visible across the solar system
- Potentially devastate or even disrupt a moon if the impact is close enough
- Deposit enough energy to alter local planetary atmospheres or cause secondary effects (e.g., moon fragmentation, atmospheric ignition)

Such an event would be catastrophic on a planetary or even system-wide scale, making the no-reuse rule for xM not just a safety protocol, but a fundamental requirement for the survival of ships, crews, and inhabited worlds.

**Perspective:** The gravitational binding energy of Earth—the energy required to disperse the entire planet into space—is about $2.24 \times 10^{32}$ joules. The energy released in this collision ($1.62 \times 10^{27}$ joules) is less than Earth's total binding energy, but still enough to vaporize the surface, shatter the crust, and render any terrestrial planet or moon uninhabitable. For smaller bodies, this could be planet-destroying; for gas giants, it would cause catastrophic atmospheric and structural effects.
## Cross-References

- CX-000
- CX-010
- CX-013

## Author Notes

Purpose: This appendix gives the FTL rewrite a disciplined external comparison set so later Leviathan ship classes, gate thresholds, and drag envelopes are not improvised from one franchise's internal assumptions.

Reasoning: The project rule is that math holds, but fictional ship masses are published under incompatible conventions. The user therefore directed that mass be normalized by volume averages while assuming all ships are crewed, and selected SDF-1 Macross as the calibration ship. This appendix implements that instruction by using a shared outer-envelope volume rule, fixing SDF-1 as the density anchor, and separating complete geometry rows from partial-data rows rather than pretending all sources are equally good.

Layer Function Checkpoints:
- Modern Times: Supports the current CHJ rewrite with a technical comparison corpus.
- Ancient History: Provides a repeatable way to compare rediscovered hulls whose records are incomplete.
- Hyborean Era: Prepares a grammar for later comparison of legendary or precursor vessels.
- Eldritch Layer: Establishes a normal hull-envelope baseline that anomalous craft can later violate.

Math And Constraint Checks: The current normalization constant is `0.096128 t/m^3`. The presently usable mass-known full-envelope sample ranges from `0.013782 t/m^3` to `0.2118 t/m^3`. Later Leviathan design work should state clearly whether it is using published source mass, SDF-normalized mass, or fully diegetic Leviathan mass.

Speed Target Checks: The current first-pass cruise targets now deliberately separate a very large fortress-carrier baseline from a very small fast freighter baseline: SDF-1 Macross at `108 m/s` and Millennium Falcon at `about 300 m/s`. Those are Sol-baseline figures rather than universal truths.

FTL Hand-Waves: This appendix does not yet translate normalized masses into thrust constants, drag coefficients, gate throughput tonnages, or ship-class redlines. It only stabilizes the comparison corpus used to discuss those later quantities.

Open Questions: Whether later passes should introduce shape coefficients for wedges, rings, and podded carriers; whether civilian, naval, and megastructural hulls should eventually receive separate density bands; whether Yamato should join the promotion queue; whether later calibration should privilege median density, mean density, or class-specific density families over the present SDF-first baseline.