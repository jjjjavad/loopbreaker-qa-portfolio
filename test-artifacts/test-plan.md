# Risk-based test plan

| Priority | Risk | Approach |
|---|---|---|
| P1 | Falling or thawing before the room is ready | Stage solved boundaries. Walk through the real exits at three network profiles. Delay readiness and check retry and cancellation. |
| P1 | Broken echo support or unsolvable chambers | Walk all twelve routes with real recordings and validated requests. Cover plate persistence, route switching, lifts, handovers, and the ending. Compare margins with design targets. |
| P1 | Lost progress or changed checkpoint during replay | Test independent profiles, completion before exit, replay access, and simulated reconnect. Run the core flow on the current build. |
| P1 | Controller unable to operate game | Use Studio's Controller Emulator for menu focus, valve hold and release. Check trigger deduplication and cancellation with fixtures. Schedule a physical-device pass. |
| P2 | Players cannot find replay or help | Inspect title and pause entry points, all row labels, and deliberate hint reveal in compact layouts. |

## Manual Studio retest

1. Use the isolated profile backend. Select **Begin Shift**. Observe loading, the intro, timer zero, then restoration of camera and controls.
2. In Chamber 01, record a sustained coolant hold. Loop, reach ignition, wait for coolant and tap once. Before exiting, verify chamber completion and checkpoint 02.
3. Pause and open **Chambers**. Verify one Replay row, eleven unfinished rows, and a separate Continue action. Replay Chamber 01 with zero echoes, repair it again, and walk through its exit. Verify the browser returns and Continue still points to 02.
4. In Studio's Controller Emulator, D-pad to Chambers, select with A and return with B. During play, approach coolant, hold RT and release. Observe the accepted hold and cleanup.
5. Record the exact build and environment for each run. Use PASS for an observed match, FAIL for a measured miss, and NOT RUN when execution evidence is unavailable.

[Case ledger](test-cases.csv)
