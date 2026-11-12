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

### Next
- **PLANNED:** migrate the needed Game Animation Sample content (Epic) into the jam project.
- **PLANNED:** C++ player character (Character Movement Component, Enhanced Input, Xbox gamepad first), with Manny as the placeholder.
- **PLANNED:** Motion Matching setup with the Game Animation Sample data plus the third-party clips.
- **PLANNED:** read the official jam rules and record sourced findings in `docs/JAM_RULES.md`. Not done yet.
- **PLANNED:** duel vertical slice (cameras, timing bar, draw, fire). This is the Day 1 target.
