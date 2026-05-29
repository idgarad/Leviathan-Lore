
## Command Directives and Autopilot Patterns

Command directives given to the navigation system are high-level instructions, not manual piloting. For example:
- "Orbit target 6 at 13km range, approach pattern gamma-6. At target range, switch to orbital pattern Gamma-4."

These directives are interpreted by the autopilot, which works in conjunction with the CDS and CAS to plot and execute the maneuver while avoiding all INCs and hazards.

**Pattern Types:**
- **Gamma Patterns:** Spirals designed to maximize transversal speed relative to the target (difficult to hit, evasive approach/orbit).
- **Alpha Patterns:** Straight-line approaches with a zig-zag component (direct, aggressive, but less evasive).
- **Beta Patterns:** Arc-shaped approaches, balancing minimal approach time with moderate transversal speed (compromise between speed and safety).

The navigation and autopilot systems handle all course adjustments, orientation, and collision avoidance required to execute these patterns, freeing the crew to focus on tactical decisions rather than manual control.

## Helm Adjustments and Manual Overrides

The helm officer's primary role is to make real-time adjustments to the variables used by the autopilot's navigation patterns. For example, the helm may increase turn speed by 10%, tighten or loosen spiral radii, or adjust approach velocity. These changes are input as variable modifications, which the autopilot then incorporates into its course calculations.

Manual overrides are available, but they are not instantaneous. Any direct manual command (such as a thruster firing or emergency maneuver) must be translated by the navigation system into a safe, executable sequence. This translation process introduces a delay of several seconds, as the system computes a collision-free and structurally safe thruster firing pattern. As a result, even "manual" control is mediated by the ship's safety and navigation logic.

## Published Transit and Exclusion Corridors

Due to the complexity and density of interstellar traffic, many systems maintain published transit corridors—predefined safe routes for navigation between major destinations (such as between star gates, stations, or planetary orbits).

- **Transit Corridors:** These are officially designated, continuously monitored paths that ships are encouraged (or required) to use for routine travel. They are optimized for safety, efficiency, and traffic flow.
- **Exclusion Corridors:** Certain regions are permanently or temporarily marked as exclusion corridors, where navigation is prohibited. Examples include the direct path between two active star gates, military exclusion zones, or areas with known hazards.
- The navigation system automatically incorporates these published corridors and exclusions into course plotting, ensuring compliance and safety.
# CX-017: Navigation

## Collision Detection System (CDS) and Collision Avoidance System (CAS)

The Collision Detection System (CDS) is a layered safety and navigation architecture. It integrates:
- Shipboard sensor data
- Navigation beacon signals from the local system
- Privileged, secure transponder information from all vessels (including cloaked ships)

The CDS uses this data to construct a real-time map of valid navigation corridors and Invalid Navigation Corridors (INC). All ship transponders continuously broadcast their general collision bounds and position on a non-crew-inspectable frequency. This information is only accessible to the CDS and CAS systems.

### System Roles: CDS vs. CAS

- The Collision Detection System (CDS) is a planning system: it analyzes sensor data and navigation information to proactively map valid and invalid corridors, supporting safe route planning and course plotting.
- The Collision Avoidance System (CAS) is a reactive system: it monitors for imminent hazards and takes immediate action to prevent collisions, overriding helm or autopilot as needed.

**INC Handling:**
- When a potential collision risk is detected (ship, debris, transient object, etc.), the CDS marks the affected region as an Invalid Navigation Corridor (INC).
- The nature of the INC is never revealed to the crew. The navigation interface simply reports that a given location or path is not a valid navigation destination.
- This preserves operational security and neutrality: the crew cannot distinguish between a ship, debris, or any other hazard—only that the path is blocked.

The Collision Avoidance System (CAS) uses the same data to actively prevent course plotting or autopilot engagement into any INC, ensuring safe navigation without revealing the underlying cause of the restriction.

## Directive Navigation and Course Plotting

Navigation in Leviathan vessels is not fly-by-wire or joystick piloting. The complexity and mass of the ship preclude manual control. Instead, navigation is directive:

- The helmsman or navigation officer provides a destination using:
	- Relative coordinates (e.g., B160, P40, R220: bearing, vertical offset, range)
	- Object references (e.g., "target 6, R30")
	- Grid coordinates (e.g., 0, -145, 22)
- The navigation system then plots a course to the specified location, automatically utilizing the CDS to avoid all INC (Invalid Navigation Corridor) regions.
- The plotted transit corridor includes a buffer zone (typically a cylinder about 8 km in diameter) to ensure safe passage.
- Tactical playbooks (e.g., "Attack Pattern Alpha-9") are often used to define complex maneuvers, with the helmsman primarily adjusting ship orientation rather than direct trajectory.

## Collision Avoidance System (CAS) and Helm Override

The CAS is the active safety system responsible for preventing collisions. It leverages shields, tractor/repulsor beams, and thrusters to ensure the vessel never enters a collision state:
- CAS will override helm or autopilot control as needed to prevent impact.
- There is no "ramming speed" option for captains or helmsmen; CAS will simply not allow a deliberate collision.
- The system's sole function is to maintain safe separation from all detected hazards, regardless of crew intent.
# CX-017: Navigation

*This volume is reserved for the formal definition and mechanics of navigation systems, protocols, and doctrine in the Leviathan setting.*

---

*Content to be provided.*
