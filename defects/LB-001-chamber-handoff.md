# LB-001 · Character falls after a chamber exit

**P1 · Progress blocker · Fix verified in Studio**

## Reproduction

On the affected published build, complete a chamber and walk through its exit. Observe the interval between unloading the old room and gaining control at the destination. The reported result was jitter and an occasional fall. The expected result is a stable spawn on the destination floor with the new cycle starting after the room is ready.

Inspection found that the server removed the previous room and teleported the character without client readiness acknowledgement. Two client reset paths also repositioned the avatar. The original live report did not capture the floor arrival time, so the exact timing of the live failure remains unmeasured.

## Fix and retest

Freeze the avatar and simulation before unloading the old room. Stream the destination and require a client acknowledgement for the matching room revision and required parts. Verify the floor server-side and position the player once. If readiness times out, keep the avatar frozen and offer retry or return to title.

On November 6, **341 fixtures passed with zero falls**. Each used a real colliding avatar and the production exit with a staged solved room. This covered all 11 boundaries at three Studio network profiles. Across 9,576 loading observations, the avatar remained anchored and the timer and recorder stayed idle. Delayed readiness, timeout, retry, respawn, and stale messages were checked. The fix was published as v12.

A related interaction change separated immediate input feedback from server acceptance. One routing acknowledgement took **431.48 ms** under packet loss, missing the latency target. Live Roblox transitions and latency remain open.

[Per-crossing results](../evidence/transitions.csv) · [Methods and timing](../evidence/archived-runs.md)
