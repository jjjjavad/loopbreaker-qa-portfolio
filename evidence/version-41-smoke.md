# Version 41 smoke · November 23, 2026

Roblox Studio local Play from the connected published place, version 41 in Edit. The profile store was Studio's isolated in-memory backend.

| Check | Observed result |
|---|---|
| Fresh title | Title loaded with checkpoint 01, all twelve chambers in the free access range, no paywall, and the avatar pinned before entry. |
| Begin Shift and intro | Clicked the title button. Observed LOADING, then INTRO at cycle one and elapsed zero with the character anchored and scriptable camera. Natural completion returned control and the Custom camera. |
| Campaign Chamber 01 | A driver walked the actual route, recorded a sustained coolant hold, looped and tapped ignition once. Repair secured in cycle two. The isolated profile reported one completion and checkpoint 02 before exit. The run took 24.33 seconds from driver start. |
| Desktop replay browser | P opened Pause. The Chambers button opened the browser with all twelve rows, one completed replay action, eleven locked replay rows and Continue · 02. |
| Replay entry | Clicked the completed row. Chamber 01 loaded at cycle one, elapsed zero, zero echoes, valve released, and checkpoint 02. |
| Replay exit | Repaired again using the same driver, then walked the physical exit. A direct route met room geometry. A walk through navigable waypoints returned to the browser. Chamber 01 was still completed and checkpoint remained 02. |
| Controller handler fixture | The real Replay row was eligible for controller focus. A synthetic gamepad handler fixture counted one use, one release and one Back dispatch despite duplicate trigger Begin input. |

The current-build controller input attempt did not switch Studio to preferred Gamepad input. Native controller menu navigation is therefore NOT RUN on v41. The [v35 emulator run](archived-runs.md#november-10--gamepad) provides the previous end-to-end input evidence.

The game driver used normal colliding movement and accepted requests. Its hooks observed state and drove controls during Play. The run ended by stopping Play, discarding the test profile and runtime observers.
