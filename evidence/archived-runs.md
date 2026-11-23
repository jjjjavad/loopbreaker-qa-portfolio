# Archived QA runs

## November 6 · Online reliability update

The connected revision was later published as **v12**. Fixtures staged the solved state and approach, then walked a colliding avatar through the production exit. Elapsed time measures exit to playable destination.

| Studio network profile | Crossings | Falls | Mean exit-to-playing |
|---|---:|---:|---:|
| 0 ms base RTT, including 11 initial crossings | 121 | 0 | 0.430 s |
| 100 ms base RTT | 110 | 0 | 0.648 s |
| 250 ms base RTT, 25 ms jitter and 0.5% loss per direction | 110 | 0 | 1.044 s |

**9,576** loading observations had zero early releases. E-valve feedback reached its next UI update within **1.212 ms** on the host. An acknowledgement for a routing action reached **431.48 ms** under simulated loss, exceeding measured RTT plus 100 ms. These measurements describe this Studio session. [Crossing records](transitions.csv)

## November 4 · Twelve-chamber regression

The hint-rework development build passed all twelve routes using colliding Humanoid walking and validated device requests. The driver created real tracks and never teleported along the puzzle routes.

- Chamber 08 completed at **25.95 s** with **8.9 s** of stable transfer.
- Chamber 10 completed at **38.70 s**, with **3.1 s** of coolant overlap and **13.3 s** of support remaining.
- Chamber 11 completed at **55.30 s**, leaving **4.70 s** versus the **5.00 s** target.
- Chamber 12 secured isolation at **51.20 s** with the feed still connected and reached the ending at **61 s**.

[Per-chamber results](walkthroughs.csv)

## November 8 · Replay and persistence

Published fix **v17**. A Studio ordinary-route run completed Chamber 01 in **24.87 s total** and recorded one completion with checkpoint 02. A fresh replay completed the repair and physically exited back to the browser with checkpoint 02. Profiles with 0, 3, and 12 completions exposed the matching count of replay actions.

The isolated-backend suite passed **31 checks** across profile independence, save flush, authorization, retained unlocks, new service instances, and simulated reconnect. Desktop and two phone landscape sizes were inspected. Touch Back and confirmation worked in emulation. The last-row visibility check used a set scroll offset after host gestures proved unreliable.

## November 10 · Gamepad

Published fix **v35**. In Studio Controller Emulator, D-pad reached Chambers, A opened it, B returned, B paused play, and A resumed. An emulated RT hold reached server acceptance and increased coolant pressure. Handler fixtures exercised trigger deduplication, release, cancellation, and held resume. Controller Skip and a full controller solve were outside the verified scope.

## November 18 · Free campaign

Published **v41** granted access to all twelve chambers in four account fixtures with zero Marketplace calls. Fresh Studio startup showed no purchase panel. Roblox metadata reported all chambers free, and the former game pass was independently verified off sale. Campaign checkpoints and completed replay remain separate.
