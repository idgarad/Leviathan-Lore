# Calibration Reference Note

All ships listed in the calibration appendix (AX-004) are drawn from external franchises and serve solely as reference anchors for mass, volume, and performance calibration. None of these vessels are canon within Leviathan lore itself. They exist only to provide a consistent, external basis for calibrating Leviathan ships when those are defined and provide a 'best effort' to meet audience expectations.

# Design Philosophy: Physics and Engineering First

The CHJ FTL system is founded on a consistent, universal set of physical and mathematical laws. All ships, regardless of class or origin, interact with the same equations for drag, field coupling, and FTL compression. There are no arbitrary, ship-specific exceptions or narrative goalposts—outcomes are determined by the underlying math and physics. Environmental and systemic effects (such as local mass rating or rare spatial anomalies) are modeled as physical variables, not as special-case rules. This ensures the FTL lore remains internally consistent, predictable, and engineering-driven, with narrative consequences emerging from the system’s foundational logic.

# CX-013: Conventional Space, Hyperspace, and Jump Space

Document Status: Draft
Primary Layer: Modern Times
Subject Domain: Technology
Audience: Developers | Authors | Readers

## Abstract

This volume begins the dedicated FTL rewrite for Leviathan canon. It defines the three-part CHJ transit model: Conventional Space as ordinary reality, Hyperspace as ship-driven short-range transit enabled by exotic matter, and Jump Space as gate-mediated interstellar transit. It also records the current gate classes, the campaign doctrine under which the Imperial Survey Corps deploys starter gates and Houses are expected to upgrade them into durable infrastructure, the first mathematical basis for why space behaves like a resistive medium around FTL-capable vessels, the first baseline compression calibrations for H-Space and J-Space under a light-speed transit cap, and the initial engine-emitter architecture by which compressed exotic matter is activated, circulated, cooled, and turned into an Intrinsic Coupling Field. The companion calibration appendix AX-004 records the current external reference hull set used to normalize crewed-envelope mass comparisons.

## Diegetic Record

The empire does not cross the stars by a single miracle. It does so through three linked regimes of motion, each with its own limits and costs.

Conventional Space is the ordinary physical world. Ships launch, maneuver, fight, dock, mine, and die there. All normal inertia, fuel burden, travel time, and spatial geometry still matter in it. Nothing about the empire's FTL order abolishes the fact that a ship remains a machine moving through a material universe.

Yet C-Space is not entirely empty to the modern navigator. Exotic matter, abbreviated xM in most technical and naval shorthand, exists across all three domains at once: Conventional Space, Hyperspace, and Jump Space. A ship capable of FTL does not merely carry a fuel or catalyst. It carries a substance whose state must remain partially coherent across the CHJ stack.

In ordinary service, xM sits in tankage as a liquid. Activation does not turn it into a different substance, and it does not spare an engineer from the ordinary burden of hauling mass. Inert xM resists forced motion in C-Space just as active xM does. What activation changes is not the matter's identity, but whether it can be used to hold a transit field.

For that reason, the ship's FTL engines are not treated as burners in the old chemical sense. They are compression machines. They force stored xM into an active state, circulate it through the ship, and return it for reconditioning after field use. The competent engineer does not speak of having burned jump fuel. He speaks of having kept the loop alive. Loss exists, but only as leakage, fouling, and transient inefficiency.

The engines alone do not open Hyperspace. Active xM must be delivered to emitters, and the emitters generate the Intrinsic Coupling Field that actually wraps the hull. That is why serious ships spread emitter capacity across the frame, mix sizes when necessary, and insist on redundancy. A ship with insufficient field coverage has not merely lost performance. It has failed to become a coherent transit body at all.

Activation also leaves heat behind. xM retains that waste heat and cannot simply be turned around for another pass the instant the field drops. It must be cooled back below reuse temperature, and the ship stores that removed heat in dedicated thermal batteries assigned to the xM loop.

That recovery problem is uglier than ordinary thermal management. Because xM-bearing heat exchangers are themselves subject to CHJ drag, the empire does not favor delicate radiator farms on working FTL craft. It favors robust exchanger trunks and heat-pipe-like rejection systems whose efficiency is limited but survivable. The result is that repeat-jump cadence is governed as much by cooling architecture as by engine power.

That coherence is imperfect. The three domains do not agree cleanly about motion, position, or imposed change, and the energy of that disagreement has to go somewhere. In C-Space it appears as drag. This is why serious navigators describe space as behaving more like a fluid than a vacuum once an xM-bearing vessel is involved. A ship pushing too hard is not simply fighting its own inertia. It is also fighting the resistance generated by xM trying to reconcile three domains that do not want to move in exactly the same way.


If the imposed acceleration or turn rate is too violent, the hull may continue its motion while the xM field fails to remain fully coupled. In practical language, the ship begins to leave its exotic matter behind. In the event of such coherence loss, the ship simply drops out of H-Space back into Conventional Space—catastrophic outcomes are not typical. This mechanism will be further detailed in the section on interdiction. That is one of the core hard limits of the CHJ order. Local FTL capacity does not free a vessel from motion discipline. It makes disciplined motion more necessary.


Hyperspace is the first sanctioned fracture in that order. By using exotic matter, a ship may shift into H-Space and perform a short-distance transit that would be impossible in purely conventional motion. Importantly, FTL travel in both H-Space and J-Space is always locally limited to light speed. The apparent superluminal effect arises because space itself is compressed in these domains—the ship never exceeds the local speed of light, but the effective distance is reduced by the compression ratio. This is not the empire's answer to interstellar freedom. It is a local transit method. In current doctrine its theoretical ceiling is roughly one light-year, and practical use is usually much shorter. H-Space therefore serves local repositioning, system-scale movement, and close stellar hops rather than the ordinary long-haul movement of an interstellar civilization.

Jump Space is the second and greater fracture. It is not normally entered by shipboard effort alone. It is accessed through stargates: fixed transit works that open J-Space routes between anchored points in the imperial network. The modern gate stack recognizes four classes: light, medium, heavy, and advanced. These classes are not merely engineering labels. They define how much mass can be moved, what tier of corridor is being served, and what sort of traffic the surrounding political order can sustain.

Campaign doctrine follows from that structure. At the start of a new campaign, the Imperial Survey Corps installs starter light, medium, and heavy gates to make the opened territory barely traversable. Those starter gates are intentionally limited in how much mass they can move at one time. The frontier is opened, but not comfortingly. Houses are then expected to turn access into infrastructure by upgrading those gates to regular capacity. In practice, this means the empire uses transit scarcity as both a developmental bottleneck and a political test.

This is why the frontier feels harsh even when the empire arrives with gates already in place. The ISC does not deliver a finished arterial network. It delivers the minimum structure needed to force a campaign to become real. The House that cannot widen the corridor cannot truly hold the territory behind it.

## Analytical Breakdown

### Layer Function

- Modern Times: This is the primary present-day transit doctrine through which the empire moves freight, fleets, settlers, and authority.
- Ancient History: Older ruins, dead gates, and broken corridors remain legible only because modern transit doctrine distinguishes local movement from anchored network movement.
- Hyborean Era: Lost or legendary FTL systems can now be described as distinct from the modern CHJ order rather than collapsing all transit into one blurred miracle.
- Eldritch Layer: Anomalous transit failures, hostile geometries, and impossible routes remain dangerous partly because modern institutions have a baseline model they expect reality to obey.

### Origins

The modern transit order rests on a functional separation. Ships require their own limited local FTL capacity so they can maneuver meaningfully within a star system or across very short interstellar gaps. Civilizations require something more stable for empire-scale logistics. The CHJ model is the present answer to that divide: H-Space for local reach, J-Space for infrastructural reach.

### Development

The current FTL framework includes the following established features.

- Conventional Space remains the baseline domain in which ordinary motion, combat, logistics, and orbital mechanics occur.
- Hyperspace transit requires exotic matter.
- Exotic matter is abbreviated xM in current technical shorthand.
- xM exists across Conventional Space, Hyperspace, and Jump Space simultaneously rather than belonging to only one of them.
- xM remains xM whether inert in tankage or active in circulation; activation state does not change its resistance to forced motion in C-Space.
- Disagreement between the CHJ domains creates effective drag in C-Space and gives high-performance navigation a fluid-dynamics character.
- H-Space is a short-range mode whose theoretical limit is about one light-year.
- Ships remain locally capped at light speed while in H-Space and J-Space; apparent FTL comes from traversing compressed path length rather than from attaining superluminal local velocity.
- H-Space and J-Space use distinct compression ratios rather than sharing one common FTL multiplier.
- FTL engines activate xM by compression and are sized by required xM throughput rather than by one-pass fuel burn.
- Active xM is recirculated and reconditioned after field use with transient loss below `0.01%` per circulation cycle.
- xM retains waste heat after field use and must be cooled below `50 C` before the same working mass can be reused.
- Dedicated thermal batteries absorb xM waste heat during turnaround, and xM-bearing heat exchangers rely on robust heat-pipe-like rejection systems rather than delicate high-area radiators.
- Emitters generate the Intrinsic Coupling Field, and current author-side sizing uses real-world diesel generators as stand-ins for emitter physical scale and field output.
- The first emitter anchor is `1 kW -> 2 m` of nominal spherical ICF diameter for a single emitter class, subject to later recalibration.
- Spin-up time is the time required to activate enough xM flow and prime enough emitters to achieve full field coverage with redundancy; ships may mix emitter sizes.
- Consecutive jumps without honoring cooldown are limited by the amount of cool buffered xM carried aboard, and carrying more xM increases C-Space drag.
- Jump Space transit is normally accessed through stargates rather than by free shipboard projection.
- The current gate classes are light, medium, heavy, and advanced.
- Standard campaign opening doctrine uses starter light, medium, and heavy gates rather than full-capacity network infrastructure.
- Houses are expected to upgrade starter gates into regular-capacity gates as part of the developmental burden of a campaign.
- Existing campaign geography still maps light gates to intra-sector movement, medium gates to inter-sector movement within a region, and heavy gates to inter-region movement.

### Local Mass Rating

Current transit vocabulary also requires a system-scale mass term. Local Mass Rating, abbreviated LMR, is the combined mass of a solar system's central star and its total planetary mass.

This term exists so later transit doctrine can speak consistently about the mass context of a local system without reducing the problem to the star alone or treating inhabited orbital architecture as though it exists in a negligible environment.

For current CHJ doctrine, higher Local Mass Rating reduces local CHJ misalignment. A more massive system gives the three domains a stronger common gravitational reference, so the same xM-bearing ship experiences less CHJ disagreement there than it would in a lighter system.

Let the local mass factor be written as:

mu_L = LMR / LMR_Sol

where `LMR_Sol` is the Local Mass Rating of the Sol system and therefore the current calibration baseline. If `mu_L = 2`, then a ship under otherwise identical conditions experiences half the CHJ drag it would in Sol.

### Transit Compression Calibration

The current rewrite also fixes a shared structural rule for both H-Space and J-Space: ships do not exceed light speed inside the transit domain itself. What appears to be faster-than-light travel in Conventional Space is instead the result of moving through a compressed route.

Let the real-space route length be `D_real` and the route length inside a transit domain be `D_dom`. Define compression ratio as:

chi = D_real / D_dom

so that:

D_dom = D_real / chi

If a ship is operating at the domain velocity ceiling `v_dom = c`, then transit time becomes:

t = D_real / (chi * c)

The important present claim is that `chi_H` and `chi_J` are not the same quantity. H-Space and J-Space are distinct compression regimes.

For H-Space, the current Sol-baseline calibration target is a nominal Earth-to-Mars hop in about ten seconds. Using the radial separation between 1.000 AU and 1.524 AU as the present nominal route gives:

- `D_EM,Sol = 0.524 AU ~= 78,389,284 km`
- `t_H,target ~= 10 s`
- `chi_H,Sol = D_EM,Sol / (c * t_H,target) ~= 26.147851`

The present practical reading is therefore that Sol-baseline H-Space compresses a nominal Earth-to-Mars route by about `26.15:1`.

For J-Space, the current baseline corridor target is about one light-year per second. Since light traverses one light-second in one second, that implies:

- `chi_J = 1 ly / 1 ls = 31,557,600`

The present practical reading is therefore that ordinary J-Space corridor travel uses a compression ratio of about `31,557,600:1`.

H-Space is therefore a comparatively shallow compression regime suitable for local and near-local movement, while J-Space is an extreme corridor-compression regime appropriate to networked interstellar transit.

### Activation and Intrinsic Coupling Architecture

xM does not become a new substance when activated. It remains exotic matter in both inert and active states. In ordinary tankage it behaves as a liquid. Activation changes whether it can participate in field generation, not whether it contributes to CHJ resistance in C-Space.

FTL engines are therefore modeled as compression activators rather than propellant burners. Their real-world stand-ins are diesel engines sized for the necessary xM flow requirement, ranging from very small cylinder counts on light craft to extremely large multi-bank or plant-scale machinery on capital hulls and fixed installations.

Emitters are separate hardware. They take circulating active xM and generate the Intrinsic Coupling Field, or ICF, that encloses the hull and permits H-Space entry. Current author-side sizing uses real-world diesel generators as stand-ins for emitter classes. Generator `kW` is treated as a proxy for emitter physical scale and ICF capacity, not as the ship's literal electrical demand.

Let:

- `Q_act` be the net engine activation throughput of field-ready xM.
- `epsilon_cyc` be the transient xM loss fraction per circulation cycle.
- `T_reuse` be the maximum permissible xM temperature for immediate reuse.
- `B_th` be the thermal-battery capacity dedicated to the xM loop.
- `Q_cool` be the effective cooling rate of the ship's xM heat-rejection system.
- `A_ship` be the ship's effective heat-rejection area available to the xM loop.
- `M_buf` be the mass of cooled xM reserve available for immediate repeat operations.
- `M_hot` be the xM working mass that exits a typical jump above reuse temperature.
- `M_norm` be the ship's normalized crewed-service mass when cross-hull thermal comparison is being made.
- `sigma_jump` be the relative severity of a jump, with `sigma_jump = 1` for the current Sol-baseline Earth-to-Mars H-Space hop.
- `P_i` be the stand-in generator rating of emitter `i`.
- `C_req` be the minimum field coverage needed to envelop the hull.
- `C_eff` be the installed effective coverage after mixed emitter geometry, overlap, and placement losses are accounted for.
- `R_red` be the redundancy factor required by the design doctrine of the ship.
- `b_inf` be the current first-pass FTL infrastructure bin assigned to the ship.
- `P_cyl` be the installed emitter-support rating assigned to one compression cylinder or banked cylinder block.
- `q_cyl` be the activation throughput of one duty compression cylinder.
- `chi_pipe(b_inf)` be the first-pass piping-volume multiplier attached to infrastructure bin `b_inf`.
- `rho_act,wet` be the first-pass effective active xM mass density occupying wetted emitters and reinforced lines during spin-up.

Current first-pass calibration fixes:

- `epsilon_cyc < 10^-4`, meaning less than `0.01%` xM loss per circulation cycle.
- `T_reuse < 50 C`, meaning xM must be cooled below fifty degrees Celsius before immediate reuse.
- `R_red = 2` for emitters, meaning current emitter doctrine assumes dual redundancy.
- the Falcon anchor fixes the smallest emitter as a flat `22 in x 22 in` square panel, so `s_emit,1 = 0.5588 m` and `A_emit,1 = 0.312257 m^2`.
- the Falcon anchor also fixes `t_panel = 4 in = 0.1016 m` and `h_manifold = 18 in = 0.4572 m`, giving `h_stack = 0.5588 m` total installed depth.
- the derived Falcon package law is `nu_e = A_emit,1 * h_stack = 0.174489 m^3/kW`, meaning installed emitter hardware volume scales linearly with class rating under the current panel-stack model.
- `phi_g(P_i)` follows the current full-load diesel-generator stand-in curve for emitter feed demand when estimating xM throughput-equivalent working mass:
	- `P_i <= 10 kW -> 0.35 kg/kWh`
	- `10 < P_i <= 100 kW -> 0.28 kg/kWh`
	- `100 < P_i <= 1,000 kW -> 0.24 kg/kWh`
	- `1,000 < P_i <= 10,000 kW -> 0.21 kg/kWh`
	- `P_i > 10,000 kW -> 0.19 kg/kWh`
- `P_i = 1 kW` corresponds to a nominal `2 m` diameter spherical ICF coverage zone for the first emitter anchor.
- emitter bubble diameter now scales with class size as `d_i = 2 * sqrt(P_i / 1 kW) m`, so larger emitters project proportionally larger ICF spheres.
- current first-pass cooling law assumes `Q_cool ~= q_A * A_ship`, meaning effective xM heat rejection scales linearly with available ship surface area under the present drag-limited exchanger model.
- current first-pass jump-friction law assumes `H_jump,fric ~= k_H * sigma_jump * (M_norm)^n_H`, meaning retained jump heat rises with normalized ship mass but not linearly per ton.
- current thermal anchors fix `n_H ~= 0.730583`, `k_H ~= 1.319889 kJ / t^n_H`, and `q_A ~= 3.23425 * 10^-4 kW/m^2` for the standard Sol-baseline Earth-to-Mars hop.
- a typical jump on a Falcon-scale small hull implies `t_cool ~= 180 s`, while the same standard hop on an SDF-1-scale heavy hull implies `t_cool ~= 360 s` under the current first-pass thermal law.
- current first-pass wet-line priming density assumes `rho_act,wet ~= 0.03 kg/m^3` inside saturated emitters and reinforced trunks.
- current first-pass cylinder activation law assumes `q_cyl ~= gamma_c * P_cyl`, with `gamma_c ~= 2 * 10^-4 kg/(s * kW)` for duty cylinders.

After field use, the xM loop first dumps retained heat into dedicated thermal batteries and only then rejects it outward through drag-tolerant exchanger trunks. Because those exchangers must survive as xM-bearing structures in a CHJ-active ship, they behave more like armored heat pipes than like delicate radiator wings. Their effective cooling rate is therefore materially limited.

Spin-up completes only when both of the following are true:

- enough active xM has been activated and circulated to feed the installed emitters at field-start condition
- `C_eff >= R_red * C_req`

To first order, spin-up time may be tracked symbolically as:

`t_spin ~= M_prime / Q_act`

where `M_prime` is the active xM inventory needed to fill lines, prime the installed emitters, and close a full-coverage field. Mixed emitter sizes and redundancy increase `M_prime` even when nominal hull coverage alone would already be satisfied.

Because route geometry is solved before H-Space injection, first-pass spin-up sizing assumes the engine already knows the planned transit duration. The same law therefore scales from a short local hop to a near-ceiling `1 ly` H-Space run by evaluating `M_jump,eq` and `M_engine,start` for the actual route rather than only for the standard ten-second calibration hop.

Current first-pass doctrine also rejects remote xM tank farms inside a maneuvering hull. xM resists forced motion under linear acceleration and under rotational motion alike, so any reserve intended for immediate jump use must stay inside reinforced engine-side accumulators, cylinder jackets, and armored manifold plenums. The FTL engine therefore remains the primary point of failure for bad maneuvering, containment damage, or spin-up faults.

For whole-drive sizing, current first-pass infrastructure bins are keyed to installed total emitter rating `P_tot` as follows:

| Infrastructure Bin | Installed Total Emitter Rating | Nominal Reinforced Main Trunk Bore | `chi_pipe` | Cylinder Redundancy Doctrine |
| --- | --- | ---: | ---: | --- |
| Tiny | `P_tot < 10 kW` | `25 mm` | `0.20` | `N+1` |
| Small | `10 <= P_tot < 10,000 kW` | `50 mm` | `0.25` | `N+1` |
| Medium | `10,000 <= P_tot < 250,000 kW` | `100 mm` | `0.35` | `N+1` |
| Large | `250,000 <= P_tot < 2,000,000 kW` | `250 mm` | `0.50` | `N+1` |
| Huge | `2,000,000 <= P_tot < 10,000,000 kW` | `500 mm` | `0.70` | `N+2` |
| Capital | `10,000,000 <= P_tot < 100,000,000 kW` | `1.0 m` | `1.00` | `N+2` |
| Titanic | `P_tot >= 100,000,000 kW` | `2.5 m` | `1.50` | `N+2` |

These bins describe the whole active plant, not just one part. Under the current user-directed anchor, Falcon-scale system components are therefore treated as `small`, while `tiny` is reserved for sub-Falcon auxiliaries such as probes, service craft, emergency drives, or other edge-case installations below the current locked smallest-shipboard anchor.

For individual emitter hardware, current first-pass class bins are keyed to the rating of one emitter `P_i`:

| Emitter Bin | Single-Emitter Rating |
| --- | --- |
| Tiny | `P_i < 1 kW` |
| Small | `1 <= P_i < 100 kW` |
| Medium | `100 <= P_i < 1,000 kW` |
| Large | `1,000 <= P_i < 10,000 kW` |
| Huge | `10,000 <= P_i < 20,000 kW` |
| Capital | `20,000 <= P_i < 100,000 kW` |
| Titanic | `P_i >= 100,000 kW` |

That mapping keeps the Falcon anchor in the `small` emitter tier and places the current `20,000 kW` backbone panel at the low end of the `capital` emitter tier rather than at the end of the whole ladder.

Above the present ship-scale capital tiers, the first explicit titanic emitter classes are:

| Titanic Emitter Class | Bubble Diameter | Panel Face Side | Package Volume | Current Reading |
| --- | ---: | ---: | ---: | --- |
| `100,000 kW` | `632.456 m` | `176.706 m` | `17,448.947 m^3` | District-scale bank for titans, yard blocks, and industrial complexes |
| `1,000,000 kW` | `2,000.000 m` | `558.800 m` | `174,489.474 m^3` | Largest practical single emitter bank for titans, industrial districts, and worldship cluster nodes |

Current working emitter palette is therefore `1`, `100`, `1,000`, `10,000`, `20,000`, `100,000`, and `1,000,000 kW`. Titanic emitter banks are reserved for `titanic` plants, fixed yards, industrial complexes, titans, and worldships. They are not treated as practical hardware for merely `capital` plants, and current doctrine does not introduce any larger singular emitter class above the titanic tier.

FTL engines are now treated as standardized platforms that accept cylinder suites rather than as one indivisible magic drive. The current first-pass cylinder ladder is:

| Cylinder Class | `P_cyl` Support Rating | `q_cyl` Duty Throughput | Current Reading |
| --- | ---: | ---: | --- |
| Tiny | `25 kW` | `0.005 kg/s` | Smallest practical shipboard priming cylinder |
| Small | `250 kW` | `0.05 kg/s` | Utility and cutter-scale activator |
| Medium | `2,500 kW` | `0.5 kg/s` | Light freighter and courier activator |
| Large | `25,000 kW` | `5 kg/s` | Escort and corvette activator |
| Huge | `250,000 kW` | `50 kg/s` | Fleet combatant and carrier activator |
| Capital | `2,500,000 kW` | `500 kg/s` | Major capital-hull activator |
| Titanic | `250,000,000 kW` | `50,000 kg/s` | Largest practical banked cylinder block; worldships use clustered titanic blocks rather than any larger singular unit |

Current first-pass FTL hull classes are frame and systems bands rather than mission labels. They describe structural volume, plant envelope, and emitter support, not the specific job the ship is performing. The broader setting can still use `drone`, `interceptor`, `fighter`, and `bomber` as smallcraft descriptors, but those frames sit below the current minimum envelope for shipboard xM activation machinery and are therefore outside the present FTL ladder. The smallest current FTL-capable frame is `bantam`, used for tug, tender, and close-yard utility work.

When AX-004 normalization is being applied, let first-pass normalized gross marketed tonnage be:

`M_gross,norm ~= rho_ref * V_env`

where `rho_ref` is the current AX-004 reference density and `V_env` is the ship's outer service-envelope volume. Let the corresponding gross-tonnage index be:

`Theta_g ~= log10(M_gross,norm / 1 t)`

Current marketing doctrine reads `Theta_g` on broad logarithmic weight bands first and frame class second. That means multiple frame classes can live inside one marketed tonnage band, while later mount-point families and internal-module ceilings still differentiate them. Two ships of similar gross tonnage can therefore remain different classes because one is built as a freighter frame, another as a carrier frame, and a third as a dreadnaught frame.

| Hull Frame Class | Typical Plant Band | Largest Practical Cylinder Class | Largest Practical Backbone Emitter Bin | Current Reading |
| --- | --- | --- | --- | --- |
| Bantam | Small | Small | Small | Smallest practical FTL tug, tender, and yard-utility frame |
| Cutter | Small | Small | Medium | Short-service utility and patrol frame |
| Scout | Small | Medium | Large | Long-range light frame built around endurance and sensors |
| Clipper | Small | Medium | Large | Fast courier or packet frame, often civilian |
| Corvette | Medium | Large | Large | First compact warship frame with a dedicated engineering spine |
| Transport | Small-Medium | Medium | Large | General-service hull for passengers, tenders, or mixed cargo |
| Freighter | Medium | Large | Large | Broad-beam cargo frame whose mission may still be civilian or military support |
| Frigate | Medium | Large | Huge | Escort frame with a full naval engineering deck |
| Destroyer | Large | Huge | Huge | First sustained fleet-combat frame |
| Cruiser | Large | Huge | Capital | Long-service line frame for multirole heavy work |
| Carrier | Medium-Huge | Huge | Capital | Volume-dominant frame built around internal bays and service decks |
| Battlecruiser | Huge | Huge | Capital | Fast heavy line frame that trades some density for reach |
| Battleship | Huge | Huge | Capital | Dense heavy line frame built around direct combat endurance |
| Capital | Huge-Capital | Capital | Capital | Umbrella for first-rank heavy frames once plant scale matters more than silhouette |
| Industrial Complex | Capital-Titanic | Titanic | Titanic | Mobile factory-habitat or yard-block frame whose output matters more than maneuver grace |
| Dreadnaught | Capital | Capital | Capital | Overbuilt first-rank war frame above the ordinary capital band |
| Titan | Titanic | Titanic | Titanic | City-ship or sector-flagship frame that demands true titanic hardware |
| Worldship | Titanic | Titanic | Titanic | Habitat-world or fortress-world frame at the mobile upper limit, built from clustered titanic plant districts rather than super-titanic one-piece hardware |

Density family is now treated as a second descriptor layered over frame class rather than as a replacement for it. The current first-pass planning bands are:

| Density Family | Planning Density | Current Reading |
| --- | ---: | --- |
| Light | `0.75 * rho_ref = 0.072096 t/m^3` | Hollow service hulls, carriers, explorers, and other frames dominated by internal void, habitat, or bay volume |
| Medium | `1.00 * rho_ref = 0.096128 t/m^3` | Neutral default when no stronger structural cue is available |
| Heavy | `1.25 * rho_ref = 0.120160 t/m^3` | Armor-dense combatants, industrial bricks, and machinery-heavy frames |

When a density family is being used for estimation, let:

`M_family ~= rho_family * V_env`

`V_family ~= M_pub / rho_family`

Density family prefixes frame class in the expected plain-language way: `light bantam`, `medium cruiser`, `heavy carrier`, and so on. These planning bands do not force every source-published ship to equal its assigned target density exactly. `rho_ref` remains the repo's neutral continuity constant, while density family is the author-side read of how hollow or compact the frame really is. SDF-1 is therefore still treated as a light-density dreadnaught despite being the ship that currently fixes `rho_ref`, because the vessel is structurally dominated by internal city volume and large service voids.

Later external mounts and internal module ceilings should key off frame class and dedicated size families such as `light`, `medium`, and `heavy`, not off gross tonnage alone. A ship can therefore mount `small heavy` weapon families or carry a different internal-module count than another ship in the same marketed tonnage band if the two hulls use different frames.

When published mass and published dimensions disagree sharply enough that both cannot be preserved honestly, documented dimensions win. Preserve the envelope, then revise the inferred mass or the assumed density family instead of forcing the hull shape to bend around an unreliable mass figure.

Current worldship doctrine now caps out at the `titanic` component tier. The limiting factor is not only field physics but maintainability: emitter banks, cylinder blocks, exchanger trunks, and their service parts must still be manufacturable, movable, and replaceable through real internal corridors, cargo ways, drydock apertures, and orbital freight systems. A worldship therefore scales by clustering many titanic infrastructure districts behind one coordinated field architecture rather than by inventing a larger singular part class above titanic.

Current first-pass spin-up law therefore treats wet-line priming as:

`V_pipe,tot ~= chi_pipe(b_inf) * V_emit,tot`

`M_prime ~= M_engine,start + rho_act,wet * (V_emit,tot + V_pipe,tot)`

`Q_act ~= sum(q_cyl,j)`

`t_spin ~= M_prime / Q_act`

where `Q_act` is quoted from duty cylinders only. Redundant cylinders exist so the drive still meets the published spin-up figure after the loss of one cylinder on `N+1` plants or two cylinders on `N+2` plants. On truly titanic installations, a quoted "cylinder" should be read as a banked cylinder block rather than as one literal monolithic bore.

For naive coverage passes that ignore complex hull geometry, let the hull be treated as a rectangular box with surface area:

`A_box = 2 * (L * W + L * H + W * H)`

Under the current emitter law, nominal ICF diameter scales with emitter class as:

`d_i = 2 * sqrt(P_i / 1 kW)`

Under the current emitter geometry law, panel face area scales as:

`A_emit,i = A_emit,1 * (P_i / 1 kW)`

and the square panel face side length is:

`s_emit,i = s_emit,1 * sqrt(P_i / 1 kW)`

The current first-pass emitter stack retains the Falcon anchor depth:

`h_stack = t_panel + h_manifold = 0.5588 m`

so physical package volume scales as:

`V_emit,i = nu_e * P_i`

Let the coverage patch assigned to emitter `i` be:

`A_patch,i = pi * (d_i / 2)^2`

where `d_i` is the nominal ICF sphere diameter of that emitter class. The minimum emitter count before explicit redundancy and placement penalties is then:

`N_emit,min = ceil(A_box / A_patch,i)`

Under the current bubble law, this reduces to:

`A_patch,i = pi * P_i`

when `P_i` is written in `kW`.

The installed emitter count under current dual-redundant doctrine is then:

`N_emit = ceil((R_red * A_box) / A_patch,i)`

and the installed total emitter rating becomes:

`P_tot = sum(P_i)`

The installed total emitter package volume becomes:

`V_emit,tot = sum(V_emit,i)`

This first-pass law keeps coverage per `kW` roughly constant across emitter classes while still encouraging larger emitters on large hulls, because larger classes sharply reduce part count and also benefit from the improving `phi_g(P_i)` feed curve. It also blocks small craft from casually mounting capital emitters, because emitter face span now grows with class rating even before service clearance, armored coffering, manifold trunks, and maintenance access are added.

Current practical doctrine therefore expects mixed emitter suites rather than one universal emitter class per hull. Large backbone emitters should cover the broad regular faces of the envelope, while smaller contour emitters close irregular geometry, local coverage gaps, and redundancy pockets so the installation does not waste large areas of hull envelope on oversized panels where they do not fit cleanly.

Until loop turnover time is calibrated separately, the first-pass xM demand for a jump may be tracked as an integrated throughput-equivalent mass:

`M_jump,eq ~= (t_jump / 3600) * sum(phi_g(P_i) * P_i)`

where each `P_i` is in `kW`, `t_jump` is in seconds, and `phi_g(P_i)` is in `kg/kWh`.

If a ship uses only one emitter class, this reduces to:

`M_jump,eq ~= phi_g(P_i) * P_tot * (t_jump / 3600)`

This deliberately makes very small emitter suites less feed-efficient than large industrial emitter classes. In current author-side calibration, swarms of tiny emitters buy geometric flexibility at the cost of worse xM throughput-equivalent efficiency.

The corresponding first-pass CHJ friction heat retained in the working xM mass and exchanger loop after a representative jump may be tracked as:

`H_jump,fric ~= k_H * sigma_jump * (M_norm)^n_H`

where `M_norm` is in `t`, `sigma_jump = 1` for the standard Sol-baseline Earth-to-Mars hop, and current first-pass calibration fixes `n_H ~= 0.730583`.

The effective heat added per ton therefore falls with ship scale as:

`h_eff(M_norm) ~= H_jump,fric / M_norm ~= k_H * (M_norm)^(n_H - 1)`

Under the current area-limited cooling law, effective cooling rate may be tracked as:

`Q_cool ~= q_A * A_ship`

where `A_ship` is the effective ship surface area available to the drag-tolerant xM heat-rejection architecture.

To first order, cooldown time may be tracked symbolically as:

`t_cool ~= H_jump,fric / Q_cool ~= (k_H * sigma_jump * (M_norm)^n_H) / (q_A * A_ship)`

This makes repeat-jump cadence primarily a hull-and-route property under the current first-pass law rather than a direct function of emitter class alone. Emitter class still governs xM throughput-equivalent working mass and installation geometry, but the dominant retained jump heat is currently treated as CHJ friction against carried ship mass.

If immediate repeat jumps are attempted without waiting for cooldown, the first-order buffer limit may be tracked as:

`N_chain <= 1 + floor(M_buf / M_hot)`

where `N_chain` is the maximum number of consecutive jumps possible before cooldown becomes mandatory. Carrying more buffered xM can raise `N_chain`, but it also raises `m_xM` and therefore the ship's C-Space drag burden.

Because diesel-generator fuel-supply curves are being used as stand-ins for emitter feed demand, the installed emitter suite can be back-solved into required xM throughput and therefore into the likely number and scale of FTL engines the ship must carry.

### xM Coupling Model

The first mathematical task of the CHJ rewrite is to define why xM changes ordinary ship handling.

Let the domain-state terms for a ship's carried xM be written as:

- Psi_C: the xM state projected in Conventional Space.
- Psi_H: the xM state projected in Hyperspace.
- Psi_J: the xM state projected in Jump Space.

Let CHJ disagreement be defined symbolically as:

Delta_CHJ = w_CH * |Psi_C - Psi_H| + w_CJ * |Psi_C - Psi_J| + w_HJ * |Psi_H - Psi_J|

where the w terms are weighting constants chosen by later engineering doctrine.

Let the effective local disagreement be written as:

Delta_eff = Delta_CHJ / mu_L

where `mu_L` is the system's Local Mass Rating relative to Sol. The important present claim is structural rather than numeric: larger disagreement means greater resistance to forced motion in C-Space, but higher LMR suppresses that disagreement.

Let xM drag in Conventional Space be written as:

F_drag = k_d * m_xM * Delta_eff * v^2

where:

- F_drag is the effective resistive force created by xM disagreement.
- k_d is the drag coefficient for the local field geometry and drive regime.
- m_xM is the ship's carried exotic-matter mass or effective xM load.
- Delta_eff is the locally suppressed CHJ disagreement after LMR is taken into account.
- v is the ship's C-Space velocity relative to the surrounding frame.

Under this rule, a system with twice Sol's Local Mass Rating produces half the CHJ drag at the same ship state and velocity.

This does not mean all ships move through vacuum as though they were submerged in atmosphere. It means that once xM is carried aboard, whether inert in tankage or active in circulation, large changes in motion generate a resistive term that scales more like fluid handling than like ideal freefall, and that the strength of that term varies by system.

The danger state is not velocity alone, but stress on xM coupling. Define coupling stress as:

S_c = (m_xM / C_bind) * (a + lambda_t * r * omega^2)

where:

- S_c is the total coupling stress imposed on the ship-xM relationship.
- C_bind is the xM binding capacity of the vessel, lattice, and containment architecture.
- a is linear acceleration.
- lambda_t is the turn-stress weighting constant.
- r is the effective distance from the vessel's turning center to the relevant xM mass distribution.
- omega is angular velocity.

The term r * omega^2 is the turning contribution. A hard turn is dangerous for the same reason a hard burn is dangerous: the hull is trying to force a change in motion faster than the xM can remain coherently dragged across CHJ.

Define the first safe-navigation boundary as:

- If S_c < 1, nominal xM coupling is maintained.
- If S_c = 1, the vessel is at the redline of stable xM retention.
- If S_c > 1, the vessel enters partial-decoupling risk, in which the ship's hull motion begins to outrun some fraction of its carried xM state.

This is the mathematical basis for the common spacer statement that careless pilots try to leave their jump behind.

### Present Understanding

The current imperial transit order rests on several working assumptions.

- H-Space is a local or near-local mobility tool, not a substitute for the gate network.
- H-Space and J-Space are compressed-path transit domains rather than raw superluminal-velocity states.
- Exotic matter is therefore a strategic transit resource even before one reaches the gate question.
- xM is not just a consumable input; it is the tri-domain coupling medium that makes CHJ transit physically consequential in ordinary maneuver.
- Activation changes whether xM can feed an ICF emitter loop, not whether the ship suffers xM-related C-Space drag.
- FTL engines are throughput-scaled activation machinery, while emitters and their redundancy determine whether a hull can actually close a stable transit field.
- Emitter class size now changes throughput-equivalent xM demand, because very small emitter classes are less feed-efficient than larger industrial ones under the current diesel stand-in curve.
- Emitter redundancy is now fixed at dual coverage, and emitter bubble diameter scales upward with class size rather than remaining flat.
- Emitter class size now also changes installation geometry, because radiator-like panel face span grows with class even under the current shallow-stack package law.
- Practical emitter architecture is now mixed-suite by default: large backbone panels handle broad hull coverage, while smaller contour panels reduce wasted envelope area and close awkward local geometry.
- Current first-pass infrastructure bins now sort complete FTL plants from `tiny` through `titanic`, with Falcon-scale hardware anchored in `small` and true titan or worldship machinery reserved for `titanic` plants.
- Current hull classes are now frame bands rather than mission labels, so civilian and military ships can share one structural class without sharing one mission.
- Thermal batteries, exchanger limits, and xM cooling thresholds now place a hard cadence limit on repeat jumps.
- Immediate-use xM reserve is now engine-local by doctrine: there is no general-purpose central xM tank that can safely shrug off the translational and rotational loads of a maneuvering CHJ-active hull.
- C-Space handling of xM-bearing ships is limited by drag and coupling stress rather than by Newtonian inertia alone.
- Sudden burns and violent turns are constrained by the risk of partial xM decoupling.
- Local Mass Rating provides the current shorthand for the combined mass context of a system's star and planetary bodies when later transit and infrastructure doctrine needs a system-scale reference term.
- Higher LMR suppresses CHJ misalignment, so identical ships do not share one universal cruise ceiling across all systems.
- Sol-baseline H-Space compression is currently about `26.15:1` for a nominal Earth-to-Mars hop, while ordinary J-Space corridor compression is about `31,557,600:1`.
- Current thermal calibration treats cooling as surface-limited and retained jump heat as a sublinear function of normalized ship mass.
- A typical Falcon-scale standard jump currently implies about `180 s` of cooldown before the same working xM mass can be reused, while an SDF-1-scale heavy hull currently anchors at about `360 s`.
- Interstellar civilization at scale depends on anchored J-Space infrastructure rather than on every ship simply jumping where it pleases.
- Campaign scarcity is partly a transit problem by design because ISC starter gates open access without solving mass throughput.
- House success in frontier space depends not only on conquest and settlement, but on the ability to widen and stabilize the transit corridors that keep those holdings alive.
- Advanced gates exist above the light-medium-heavy campaign stack, but their exact deployment doctrine is not yet fully fixed in the current rewrite.

## Material Implications

- The distinction between H-Space and J-Space keeps local maneuver, strategic movement, and imperial logistics from collapsing into a single overpowered travel mode.
- Distinct H-Space and J-Space compression ratios prevent local shipboard transit from collapsing into gate-equivalent strategic mobility.
- Gate control remains one of the central levers of sovereignty because J-Space access is infrastructural rather than purely shipboard.
- Exotic matter becomes a meaningful industrial, military, and political resource because even local FTL depends on it.
- Engine rooms and xM plumbing scale with circulation throughput and priming demand rather than with one-pass fuel consumption.
- Engine rooms become armored xM citadels rather than mere pump spaces, because immediate reserve, cylinder banks, and wet-line mass are intentionally concentrated there.
- Emitter placement, overlap, and redundancy become core naval-architecture questions because field coverage determines whether the ship can complete spin-up at all.
- Larger emitter classes are now structurally favored as backbone hardware on capital hulls because they collapse component count without materially increasing total field power under the current bubble law.
- Mixed emitter suites are now favored in practical installations, because they let large hulls exploit big backbone panels without wasting envelope area on oversized hardware where local contour closure needs smaller units.
- Titanic emitter banks above `20,000 kW` now give titans, industrial districts, and worldship cluster nodes a real megastructure backbone tier without requiring any super-titanic one-piece hardware class.
- Frame class, plant class, and mission are now partially decoupled, which lets a civilian hull ride a bomber, clipper, freighter, or even destroyer frame without changing the underlying engineering class.
- Small ships can no longer be treated as though they can mount arbitrarily large emitter classes without paying obvious geometry costs in hull surface area and internal manifold layout.
- Thermal batteries and drag-tolerant heat exchangers become just as important as engine throughput, because repeat-jump cadence is limited by cooling rather than by simple willingness to burn harder.
- Larger hulls now gain limited thermal economy of scale under the current first-pass law, because CHJ friction heat rises with normalized mass more slowly than linearly while cooling still tracks available surface area.
- Ship handling, pursuit doctrine, and combat maneuver all inherit hard limits from xM drag and coupling stress.
- Every system alters attainable C-Space cruise behavior because local stellar-plus-planetary mass changes CHJ drag.
- Additional xM reserve can buy more immediate jump attempts, but only by increasing the drag burden the ship carries between them.
- The light-speed cap inside H-Space and J-Space means Leviathan FTL is fundamentally geometric compression, not hidden infinite acceleration.
- Piloting culture becomes more conservative and technical because reckless acceleration is not merely inefficient; it risks field separation.
- Starter gate doctrine gives campaign openings a built-in freight bottleneck that supports frontier scarcity, smuggling, contested upgrades, and House competition.
- The empire can appear technologically powerful without making distance meaningless, because the ability to open a corridor is not the same as the ability to move unlimited mass through it.

## Cross-References

- CX-000
- CX-003
- CX-006
- CX-012
- AX-003
- AX-004

## Author Notes

Purpose: This volume begins replacing the repo's standing FTL deferral with explicit canon.

Reasoning: The current codex already assumes stargates, campaign opening infrastructure, and the Imperial Eye, but it intentionally deferred the actual transit model. This FTL pass extends the CHJ framework by defining xM as a tri-domain substance whose imperfect CHJ coherence produces real drag and coupling limits in C-Space. It also fixes the current interpretation of H-Space and J-Space as compressed-path transit domains whose apparent faster-than-light performance does not require ships to exceed light speed inside those domains, and it establishes the first engine-emitter chain by which inert liquid xM is activated, circulated, cooled, and used to generate an Intrinsic Coupling Field. That keeps the setting's FTL exception physically expensive instead of making maneuver doctrine decorative.

Layer Function Checkpoints:
- Modern Times: Defines the empire's current transit grammar.
- Ancient History: Creates a baseline against which older gate ruins and lost transit systems can later be contrasted.
- Hyborean Era: Keeps mythic transit inheritance distinct from the modern imperial network.
- Eldritch Layer: Gives anomalous transit phenomena a stable normal model to violate.

Math And Constraint Checks: If H-Space tops out at about one light-year in theory, ordinary interstellar civilization cannot bypass gate infrastructure simply by scaling ship drives upward. If ships remain capped at `c` inside both H-Space and J-Space, then Leviathan FTL must be modeled as metric compression rather than raw superluminal velocity. A nominal Earth-to-Mars Sol hop in about ten seconds requires H-Space compression of about `26.15:1`, while J-Space at about one light-year per second requires compression of about `31,557,600:1`. Those values are distinct enough that H-Space cannot be treated as a weak form of J-Space or J-Space as merely a faster H-Space cruise mode. If xM resists forced motion in C-Space whether inert or active, then ships pay the mass-handling burden of carrying xM even before they spin up for transit. If xM must be cooled below `50 C` before reuse, cooling capacity scales with effective ship surface area, and retained standard-jump friction heat scales as `(M_norm)^0.730583`, then repeat-jump doctrine becomes a thermal-management problem rather than a simple engine-output problem. Under the current first-pass anchors, that law gives a Falcon-scale standard jump about `180 s` of cooldown and an SDF-1-scale heavy hull about `360 s`. If greater immediate jump reserve is bought by carrying more cooled buffered xM, then the ship's drag burden also rises because `m_xM` rises with it. If the current emitter anchor is `1 kW -> 2 m` of nominal ICF sphere diameter and transient circulation loss is below `0.01%` per cycle, then later ship-design passes can start estimating emitter count, engine throughput, spin-up time, and repeat-jump cadence from real-world diesel generator and engine classes without pretending those proxies are literal shipboard electrical loads. If xM exists across CHJ simultaneously and creates drag proportional to disagreement, later fleet and ship-design volumes need coherent assumptions about acceleration envelopes, turn-rate limits, containment geometry, failure behavior, and thermal soak under overload. If Local Mass Rating suppresses CHJ disagreement inversely relative to Sol, then local system environment must become part of any honest speed, drag, and routing model. A system with twice Sol's LMR produces half the CHJ drag under otherwise identical conditions, which means later speed tables cannot be treated as universal constants divorced from stellar environment. If starter gates intentionally restrict mass throughput, later campaign, freight, and military volumes need realistic assumptions about queueing, upgrade cost, transit priority, and strategic delay. If exotic matter is required even for local FTL, later volumes need coherent assumptions about sourcing, storage, transport safety, and denial strategy.

Terminology Check: Local Mass Rating, abbreviated LMR, is now fixed as the combined mass of a solar system's central star and total planetary mass. It is also the current system-scale modifier on CHJ alignment, with Sol used as the baseline reference case.

FTL Hand-Waves: This volume now fixes the CHJ structure, xM's tri-domain role, the first symbolic drag and coupling framework, the baseline distinction between H-Space and J-Space compression, the first engine-emitter activation loop, the basic xM thermal-recovery rule, the first hull-frame ladder, and the existence of gate classes, but it does not yet define full route tables, exotic-matter production chains, exact zoning laws for clustered titanic worldship infrastructure, calibrated engineering constants, detailed thermal-battery classes, advanced-gate doctrine, Imperial Eye class identity, or wormhole behavior.

Open Questions: What normal practical H-Space range is common in fleet and civilian service as distinct from the one-light-year theoretical ceiling; how much H-Space compression varies by drive quality, field stability, route geometry, and Local Mass Rating beyond the current Sol-baseline calibration; how clustered titanic infrastructure should be zoned across industrial complexes and worldships while keeping every major part maintainable and transportable; what redundancy doctrine different ship classes should carry beyond the current first-pass `N+1` and `N+2` plant rules; how thermal-battery capacity and exchanger rate should scale by hull class; how exotic matter is produced, refined, stored, and rationed; what the calibrated values of k_d, the CHJ weighting terms, C_bind, and lambda_t should be for ordinary ship classes; what exact mass and throughput thresholds distinguish starter gates from regular-capacity gates; what doctrine separates advanced gates from heavy gates; whether the Imperial Eye is an advanced gate or a distinct super-category; how interdiction, navigation failure, hostile route denial, xM separation damage, and thermal overload behavior work under CHJ.