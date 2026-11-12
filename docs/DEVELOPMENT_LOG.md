# Development Log

All times are Italy time (CET). Status tags: **DONE** · **IN PROGRESS** · **PLANNED** · **BLOCKED**.
Times come from file timestamps, editor logs and local git commits whenever possible.
The words "about" or "~" mark times that are approximate.

## Day 1 — Thursday 2026-11-12

The jam started at 06:00 CET (00:00 ET).

| Time (CET) | Who | What | Status |
|---|---|---|---|
| 07:38 | Owner | Agent rulebook ([AGENTS.md](../AGENTS.md)) placed in the local workspace. | DONE |
| ~07:46 | Owner + Claude Code | Local workspace prepared. This public docs repository was cloned (empty). The Unreal Engine skill set for Claude Code was installed locally. | DONE |
| 07:53 | Owner | New **Blank C++ project created in Unreal Engine 5.8.4** (private). | DONE |
| 07:57 | Claude Code | Private local git created for the Unreal project. It tracks only source, config and the project file, and has no remote. | DONE |
| 07:58 | Claude Code | Project configured: the plugin set needed for Motion Matching locomotion (Epic plugins) is enabled, and the Ultimate Engine Copilot plugin is enabled **for this project only**. The editor target was built with UnrealBuildTool. | DONE |
| 08:00 | Owner | Unreal Editor opened on the jam project. The Copilot plugin loaded, and Claude Code was connected to the editor through the plugin's MCP server. | DONE |
| ~08:05 | Claude Code | MCP connection checked with read-only queries: current folder and the level's lighting actors. | DONE |
| 08:07 | Owner | Added **Gamma Studio — Free Animation Pack** (Fab) to the project. | DONE |
| 08:09 | Owner | Added **Western Animations — SoerGame** (Fab) to the project. | DONE |
| ~08:10 | Claude Code | Checked the free pack in the editor. Its 24 clips are on the UE5 Mannequin skeleton, but walk-only clips are too few for Motion Matching on their own. | DONE |
| ~08:10 | Owner | **Decision:** keep Motion Matching. Take starts, turns and the missing locomotion clips from Epic's Game Animation Sample. See [TECHNICAL_DECISIONS.md](TECHNICAL_DECISIONS.md). | DONE |
| ~08:11 | Owner | Purchased **Ultimate Horse System — Hivemind** (Fab) for the horse. It is not yet added to the project. | DONE |
| 08:12 | Claude Code | First public documentation: README, AGENTS.md, asset provenance (submission declaration list), AI tools, technical decisions, this log. | DONE |
| ~08:15 | Owner | Fab listing URLs and purchase status recorded for the three third-party packs. **Decision:** the current project is an experimental sandbox; once the build works, only the assets actually used are migrated into a clean project (TD-006). | DONE |
| 08:17 | Owner | Created the project folder root (`_Game`) and the **DebugRoom** test level, set as the editor and game default map. | DONE |
| ~08:24 | Owner | Added **Ultimate Horse System — Hivemind** (Fab, purchased) to the project. | DONE |
| ~08:25 | Claude Code | Wrote the first gameplay C++: player character (walk/jog, limited turn rate, camera-relative movement with "sticky" input across camera cuts), placed cinematic camera shots, the Director that decides which shot is live, player controller and game mode (TD-007). | DONE |
| 08:28–08:31 | Owner + Claude Code | Owner closed the editor; Claude Code built the editor target with UnrealBuildTool (succeeded) and committed the source to the private local repository. | DONE |
| 08:33–08:37 | Claude Code | Through the Copilot MCP server: created the input assets (gamepad + keyboard), the Blueprint subclasses (UE5 Manny placeholder), and three test camera shots in DebugRoom. Play-in-Editor test with injected input: walk follows the live camera; holding the stick through a camera cut keeps the previous direction; a new press adopts the new camera; jog reaches 340 cm/s. No errors from project code in the log. | TESTED (automated input) |
| ~08:45 | Owner | Hands-on review. **Rejected** the interim locomotion (C++ character with the template animation blueprint): feet slide and it looks dated. Also rejected the first camera-switching behaviour. **Decision:** use Epic's Game Animation Sample character as-is for locomotion (Motion Matching, traversal over small obstacles). Rebuild the camera system in C++ following the owner's own pre-jam fixed-camera design (re-implemented, declared). | DONE (rejection recorded) |
| 08:46–08:53 | Claude Code | Read-only dependency analysis of the owner's local copy of the Game Animation Sample (installed before the jam). The full dependency set was 5.3 GB, including the owner's personal pre-jam content and alternate display characters we do not need. The owner approved a reduced set of about 1.25 GB without them. | DONE |
| 08:53 | Owner | Added a free western weapon pack from Fab (revolvers, ammunition, props). | DONE |
| 08:54 | Claude Code | With the editor closed, imported 1,263 Game Animation Sample packages at their original paths. No file was overwritten, and original timestamps were kept. The exact import list is kept in the private project. | DONE |
| ~08:57 | Claude Code | Player controller: camera-relative control for any pawn. The fixed camera's direction drives the control rotation that the sample character already uses, keeping the previous camera's direction across cuts while the stick is held. The editor target build succeeded. | BUILT, not tested yet |
| 09:02–09:10 | Claude Code | Read the public jam page and the organizer's forum post and wrote [JAM_RULES.md](JAM_RULES.md). The Official Rules document did not load for the agent and is pending the owner's reading. Documented the [work routine](WORKFLOW.md). | DONE |
| 09:12–09:30 | Claude Code | Through MCP, set up the sample character in DebugRoom with the Director's fixed cameras. Two sample Blueprints still pointed at the excluded sample game mode (skin switching, pawn cycling); those calls were removed so they compile. Walk is the default, run is on L3, sprint is unmapped, and the gamepad bumpers are left free for the camera. Play-in-Editor with injected input: walk 200 cm/s in the camera's direction, run 500 cm/s, direction kept across a camera cut while the stick is held. Three test obstacles placed (50 cm, 1 m, 1.5 m). | TESTED (automated input) |
| ~09:30 | Claude Code | The traversal did not trigger. Cause found: the sample's data-driven console variables (foot placement, locomotion setup and others) and two plugins (GameplayStateTree, MotionTrajectory) were missing from the project config. Added both; build succeeded. | DONE |
| ~09:40 | Owner + Claude Code | After the restart the owner saw 234 load errors. Cause: a bug in the agent's dependency scanner, which missed names that end with a number or contain "+". Fixed the scanner and copied the 167 missing sample files (34 MB, no overwrites, no excluded content). Checked that no saved asset had kept an empty reference. | DONE |
| ~09:56–10:00 | Claude Code | After the restart the load log is clean (no missing packages). Traversal verified in Play-in-Editor: in this sample version it is triggered by the Jump action (Cross/A, Space), not by the separate Traverse action; the character hurdled the 50 cm block and landed on the far side. | TESTED (automated input) |
| ~10:00 | Owner | Hands-on test of the sample locomotion and traversal with the gamepad. | IN PROGRESS |

### Next
- **PLANNED:** set up the Game Animation Sample character in DebugRoom (walk as the default, run optional, no sprint), then test it in Play-in-Editor and with the owner.
- **PLANNED:** rebuild the fixed-camera system in C++ (plane-crossing triggers with hysteresis, smooth blends, soft tracking, focus on the character, trigger volumes visible in the editor).
- **PENDING OWNER REVIEW:** read the Official Rules.
- **PLANNED:** duel vertical slice (cameras, timing bar, draw, fire). This is the Day 1 target.
