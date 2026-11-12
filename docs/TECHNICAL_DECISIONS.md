# Technical Decisions

Each entry gives the decision, the date and time (CET), the reason, and the alternatives considered.

## TD-001 — Private Unreal project, public docs-only repository
- **When:** 2026-11-12, Day 1 morning.
- **Decision:** The game is a private local Unreal Engine 5.8.4 C++ project. This public repository holds only documentation.
- **Why:** The project uses purchased and third-party assets that may not be redistributed, plus the owner's proprietary tools. The public record still has to be truthful and complete.

## TD-002 — New C++ project; Game Animation Sample as a donor only
- **When:** 2026-11-12, 07:53 CET.
- **Decision:** Start from a new Blank C++ project. Epic's Game Animation Sample is used only as a donor: the needed content is migrated in, and we do not work inside the sample.
- **Why:** Clean provenance and a small project.
- **Alternative rejected:** building the game directly inside the sample project, which would carry a lot of unused content.

## TD-003 — Player: UE5 Manny first, MetaHumans later
- **When:** 2026-11-12, Day 1 morning.
- **Decision:** Gameplay is built and tested on the UE5 Mannequin (Manny). The bespoke MetaHumans replace it later through animation retargeting.
- **Why:** Gameplay does not wait for the character work.

## TD-004 — Locomotion: Motion Matching
- **When:** 2026-11-12, ~08:10 CET (owner decision).
- **Decision:** Player locomotion uses Motion Matching (Pose Search). The database combines Epic's Game Animation Sample clips (starts, stops, pivots, turn-in-place, runs) with the third-party animation packs listed in [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md).
- **Why:** The owner wants fluid, modern movement, not stiff or dated state-machine motion.
- **Alternative rejected:** a classic animation blueprint with blend spaces using only the free pack. It is simpler, but its 24 walk-only clips have no starts, stops or runs.
- **Movement component:** Character Movement Component (CMC), not the Mover plugin.
- **Update ~08:45 CET:** an interim placeholder (our own C++ character on the template blend-space animation blueprint) was built and tested, then rejected by the owner because of foot sliding and a dated look. Since then, the Game Animation Sample's own CMC character is used **as-is**: animation blueprint, Motion Matching databases, choosers and traversal for small obstacles. We add layers around it (cameras, controller) instead of replacing it. Walk is the default and run is optional; sprint is not used.

## TD-005 — Editor automation is development-only
- **When:** 2026-11-12, 07:58 CET.
- **Decision:** Ultimate Engine Copilot is enabled only in the jam project and is used only during development, through its MCP server with Claude Code. It is not part of the shipped game.
- **To verify:** that it is excluded from the first packaged build (PENDING).

## TD-006 — Sandbox project now, clean migration later
- **When:** 2026-11-12, ~08:15 CET (owner decision).
- **Decision:** The current Unreal project is an experimental sandbox where content is added quickly. Once the build works, the final maps and game mode are migrated into a clean project, which brings only the assets actually used. The migration list is cross-checked against [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md).
- **Rules that keep the migration safe:** project assets live under one root folder; C++ never hard-codes asset paths; the clean project reuses the same C++ module; code plugins are installed separately; the editor automation plugin stays disabled there. The migration is planned at the first working packaged build, not at the deadline.

## TD-007 — The Director: one authority for the live camera
- **When:** 2026-11-12, ~08:25 CET.
- **Decision:** Fixed cinematic camera shots are placed actors. A single world subsystem (the Director) decides which shot is on air. Requests come from the player (camera buttons) now, and from camera zones and sequences later. This is the core of the "Director's Cut" mechanic.
- **Movement:** player input is relative to the live shot. When the camera cuts while the stick is held, the previous camera's frame is kept until the stick is released or turned past 45°. This prevents the classic fixed-camera problem where the character swerves on every cut.
- **Reference:** the owner's pre-jam fixed-camera prototype was used as a design reference only. The jam implementation was written from scratch in C++; see [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md).
- **Update ~08:57 CET:** camera-relative movement now lives in the player controller. It sets the control rotation from the live fixed camera, keeping the previous direction across cuts while the stick is held. Any pawn that moves relative to its control rotation (including the sample character, unchanged) therefore walks relative to the fixed camera. The first camera-switching behaviour was rejected by the owner; switching will be rebuilt following the owner's design: plane-crossing trigger volumes with hysteresis, smooth blends, soft tracking, focus on the character, and volumes visible in the editor.

## TD-008 — Build size budget: under 1 GB zipped
- **When:** 2026-11-12, ~09:05 CET, after reading the jam page (see [JAM_RULES.md](JAM_RULES.md)).
- **Constraint:** the desktop submission .zip must be under 1 GB.
- **Consequences:**
  - Prune unused Motion Matching sets (e.g. sprint, crouch) before the final build.
  - Do not ship the sample's alternate display characters.
  - Budget the MetaHumans (LODs, grooms, texture sizes), the horse and the environment.
  - Measure the packaged size at every packaged build, starting with the first one.

## TD-009 — Game Animation Sample 5.8, unmodified download
- **When:** 2026-11-12, ~10:20 CET.
- **Decision:** The sample content in the project is Epic's unmodified 5.8 download. The first import, taken from the owner's older local copy of the sample, was removed and replaced.
- **Why:** The 5.8 version has newer traversal and locomotion data, and an unmodified source gives a clean provenance. Our changes are made inside the jam project and logged.
- **Alternative rejected:** keeping the first import and patching it.

## TD-010 — Hero MetaHuman as a visual on the sample character
- **When:** 2026-11-12, ~11:10 CET.
- **Decision:** Movement stays on the sample's mannequin character, which is hidden. The MetaHuman hero is attached as its visual and copies its pose every frame through the sample's runtime retarget (mannequin to MetaHuman).
- **Why:** The Motion Matching data, traversal and foot placement keep working exactly as tested, and any MetaHuman can be swapped in without retargeting the animation library.
- **Consequences:** The hero is kept at full detail, animates even off-screen (fixed cameras cut while it is out of frame), and updates after the mannequin it copies from.

## TD-011 — Head attention: C++ component plus anim instance
- **When:** 2026-11-12, ~11:55 CET.
- **Decision:** Points of interest are level actors with a range sphere visible in the editor. A component on the character picks the point to look at and computes a smoothed head turn within human neck limits. The hero's anim blueprint (a C++ anim instance) spreads that turn over neck_01, neck_02 and head after the retarget.
- **Why:** Values can be tuned in the editor (range, priority, limits, speed). It works with any MetaHuman, does not change the sample's animation blueprint, and the animation owns the head during traversal.
