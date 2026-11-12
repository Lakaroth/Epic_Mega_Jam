# Work Routine

This is how the game is built during the jam: who decides, who does what, and how each step is checked and recorded.

## Roles
- **Owner (Elvis Morelli, solo developer):** sets the direction and makes every decision on scope, quality, assets, licenses and publishing. He tests the game hands-on.
- **Claude Code (AI coding agent):** inspects, proposes, implements and tests small steps, and keeps the record. It works in the owner's private project and drives the open Unreal Editor through the Ultimate Engine Copilot plugin (MCP).

## The loop for every step
1. **Read the state.** The agent reads [AGENTS.md](../AGENTS.md), the current log and the decisions.
2. **Inspect, read-only.** It looks at files, or at the live editor through MCP read queries, before changing anything.
3. **Propose.** It gives a short plan and flags license or rule concerns. The owner approves or redirects.
4. **Implement the smallest testable change.**
   - C++ is edited on disk and built with UnrealBuildTool. Structural C++ changes are built with the editor closed.
   - Editor assets (input, Blueprints, level setup) are created through structured MCP calls. The agent saves only the assets it created.
5. **Test.** The build must succeed. Then the agent runs a Play-in-Editor check with injected input and reads the log. Then the owner tests by hand with a gamepad. A step counts as accepted only after the owner's test.
6. **Record.**
   - Source code goes into a private local git repository (never published).
   - Public documentation records what happened, with real times (CET) and evidence: build results, test results, decisions, and rejections too.
7. **Publish documentation.** Only text documentation is staged, file by file. It is audited (file list, diff, secrets scan) and pushed only with the owner's explicit approval.

## Asset intake
- Every new asset gets a row in [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md) as soon as it enters the project: source link, license status, time added, pre-jam or not.
- Content taken from an existing local project is copied with its dependencies computed first. The owner's personal pre-jam content is excluded unless it is explicitly chosen and declared.
- Nothing is overwritten. Original file timestamps are kept as evidence.

## Never published
Unreal project files, assets, Blueprints, animations, plugins, binaries, builds, credentials, the owner's proprietary tools, and private footage.
