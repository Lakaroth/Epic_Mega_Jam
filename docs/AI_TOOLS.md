# AI and Automation Tools

This page lists only the tools that have actually been used so far. Tools planned in
[AGENTS.md](../AGENTS.md) are added here only once they are used.

| Tool | Used for | Used since | Distributed in the game? |
|---|---|---|---|
| **Claude Code** (Anthropic, Claude Opus model) | Planning, project setup, build configuration, C++ and documentation, and driving the Unreal Editor through MCP. The owner reviews and approves every step. | 2026-11-12 (Day 1) | No. It is a development tool. |
| **Ultimate Engine Copilot / Blueprint Generator Ultimate** (Unreal Engine plugin from Fab, v2.4.0) | Editor automation. Its MCP server lets Claude Code read and edit the live Unreal Editor (assets, animation blueprints, levels). | 2026-11-12 (Day 1) | **No.** It is used for development only and is enabled only in the jam project. Excluding it from the packaged build will be verified at the first packaging (PENDING). |
| **Tripo** (AI 3D generation) | Generated the hero's hat (mesh and textures), before the jam (2026-11-11), as part of the pre-jam character work. | Before the jam | Yes, as part of the hero character's hat (declared in ASSET_PROVENANCE.md). |

## How the agents work

- The owner gives direction and makes the decisions (scope, assets, licenses, publishing).
- Claude Code proposes and carries out small, testable steps. It reports what was actually
  done, and pushes to this repository only with explicit owner approval.
- Every AI-assisted step that matters is recorded in [DEVELOPMENT_LOG.md](DEVELOPMENT_LOG.md).
