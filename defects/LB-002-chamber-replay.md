# LB-002 · Solved chambers missing from title and pause menus

**P2 · Returning-player workflow blocked · Fix verified in Studio**

## Reproduction

On v13, load a profile with a completed chamber. Check the title menu, then enter play and pause on desktop. Both menus lacked **Chambers** even though the replay browser and completion flags existed.

Expected behavior: open the browser from title or pause, replay a completed room with empty echoes, and keep **Continue** pointed at the campaign checkpoint. Unfinished rooms stay locked for replay.

## Fix and retest

Restore the two browser entry points, fit the menu to its visible actions, correct browser dimensions on first open, and enable vertical scrolling. Reuse the existing completion flags and server access checks.

On v17, profiles with 0, 3, and 12 completions exposed exactly 0, 3, and 12 replay actions. Unfinished-room requests were rejected. An ordinary Chamber 01 route advanced the checkpoint to 02 before exit. The replay started empty and returned to the browser with checkpoint 02 and one completion. The focused v41 run repeated the repair and replay on an isolated profile. Actual Roblox leave/rejoin remains open.

[Archived replay checks](../evidence/archived-runs.md) · [Current-build smoke](../evidence/version-41-smoke.md)
