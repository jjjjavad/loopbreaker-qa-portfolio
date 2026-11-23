# LB-003 · Controller input does not operate menus or machines

**P1 · Supported input unavailable · Fix verified in the v35 Studio Controller Emulator**

## Reproduction

On the affected console build, try to move title focus to **Chambers**, select it, and return. In play, approach a coolant valve and press the use trigger. The reported result was unresponsive controller buttons. Inspection of v30 found keyboard and pointer bindings for the affected gameplay actions and missing menu focus initialization.

Expected behavior: navigate with the D-pad, select with A/Cross, return or pause with B/Circle, and use RT/R2 at the machine. Releasing the trigger ends a hold.

## Fix and retest

Add bindings through the existing interaction hooks, initialize focus on visible menus, scroll offscreen selections into view, and display controller prompts. Deduplicate analog and digital trigger reports and cancel held input on disconnect.

In the v35 Studio Controller Emulator, D-pad reached Chambers, A opened it, B returned to title, and B/A paused and resumed during play. An emulated trigger at the valve produced a server-accepted hold and rising coolant pressure. Handler fixtures verified threshold, release, cancellation, loop input, and held resume. A full controller-only solve and physical-console coverage remain open.

[Archived emulator results](../evidence/archived-runs.md) · [Current-build smoke](../evidence/version-41-smoke.md)
