# Asset Provenance — Director's Cut (2026 Epic AI MegaJam)

This is a record of every third-party and pre-existing component used in the private Unreal project.
**It is the list of items to declare in the jam submission.** The final declaration covers the assets actually used in the submitted build. It will be cross-checked against the clean migration of the final maps.
Only text is published here. Source assets, Blueprints, animations, plugins and packaged third-party project files are **never** published in this repository.

Status legend: **VERIFIED** (evidence on file) · **PENDING OWNER REVIEW** · **UNVERIFIED**.
Exact license evidence (Fab Library entitlement / receipt) must be recorded for each asset before final submission.

---

## 1. Gamma Studio — Free Animation Pack (Fab)

| Field | Value |
|---|---|
| Creator | Gamma Studio (owner-confirmed, 2026-11-12) |
| Source | Fab Marketplace: https://www.fab.com/listings/8de31c5d-93bc-4bd4-9606-ca789ce91b99 |
| Status | Free (claimed on Fab). |
| License | Fab Standard License; commercial use permitted (owner-confirmed, 2026-11-12). Fab Library entitlement evidence to be recorded before final submission. |
| Acquired | PENDING OWNER REVIEW (date the pack was added to the owner's Fab library) |
| Added to project | 2026-11-12 ~08:07 CET (file timestamps in `/Game/SampleAnimationPack`) |
| Pre-jam? | Third-party asset. It was not created by the team. |
| Contents used | 24 motion-capture sequences at 120 fps on the UE5 Mannequin skeleton: 12 male unarmed clips (idle, gesture, 4-direction walk loops, 90° turn-in-place, injured idle/walk, walk transitions), 12 female rifle walk/aim clips and 2 door-kick clips. The pack also ships demo content with the UE5 Manny/Quinn mannequins and the Third Person template animation blueprint (Epic content). |
| Use in game | Planned: third-party locomotion animations added to the player's Motion Matching database (together with Game Animation Sample data, see §4), on Manny first and later retargeted to MetaHumans. Nothing is integrated yet as of 2026-11-12 08:12 CET. |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |
| Open questions | Record the Fab Library entitlement evidence. |

## 2. Western Animations — SoerGame (Fab)

| Field | Value |
|---|---|
| Creator | SoerGame (Fab publisher, owner-confirmed 2026-11-12) |
| Source | Fab Marketplace: https://www.fab.com/listings/6ff33fd3-f834-41f6-bf97-a0df10372304 |
| Status | **PURCHASED** by the owner (owner-confirmed, 2026-11-12). |
| License | PENDING OWNER REVIEW. Verify the purchased license tier in the Fab Library. |
| Acquired | Purchase date PENDING (from the Fab receipt). |
| Added to project | 2026-11-12 ~08:09 CET (file timestamps in `/Game/WesternAnimations`) |
| Pre-jam? | Third-party asset. It was not created by the team. |
| Contents used | 52 western animation sequences: quick-draw shots, duel deaths, hand-near-holster idles, revolver fanning, spin and reload, horseback riding and shooting, saloon/bartender/table idles, hat gestures. The pack also ships demo mannequin content: Manny/Quinn and locomotion, pistol, rifle, death and hit-react animations. These appear to be Epic UE5 template content (UNVERIFIED). |
| Use in game | Duel (holster idle, quick draw, fire, death), saloon NPC idles, horse riding placeholder. |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |
| Open questions | Record the license tier and the purchase date from the Fab Library/receipt. |

## 3. Epic Games content (UE5 Mannequin, template content)

| Field | Value |
|---|---|
| Creator | Epic Games |
| Source | Bundled with Unreal Engine templates; copies are included inside the two packs above. |
| License | Unreal Engine EULA (use in Unreal Engine projects). |
| Use in game | Placeholder player and NPC mesh (Manny) until the MetaHumans are ready. |
| Submission declaration | To be listed as engine/template content. |

## 4. Game Animation Sample Project (GASP) — Epic Games

| Field | Value |
|---|---|
| Creator | Epic Games |
| Source | Free Epic sample project (Motion Matching locomotion). It was copied from the owner's local copy of the sample, installed before the jam (2026-01-14) and upgraded to UE 5.8. |
| License | Epic sample content for use in Unreal Engine projects. Exact license wording UNVERIFIED. |
| Use in game | Player locomotion: the sample's CMC character, animation blueprint, Motion Matching databases and choosers, traversal (small obstacles) and input, used as-is. Unused sets (e.g. sprint, crouch) will be pruned before the clean migration. |
| Status | **Imported 2026-11-12 08:54 CET**: 1,263 packages (~1.25 GB), copied at their original paths with original timestamps. A further 167 packages (34 MB: foley sounds, aim offsets, a few locomotion clips) that the first dependency scan had missed were added at 09:42 CET, for **1,430 packages** in total. The exact file list is kept locally. |
| Excluded on purpose | The owner's pre-jam personal content in that local project (a custom Mover-based character, the owner's own MetaHuman and outfits), and the sample's alternate display characters (Echo, Paragon, UE4/UE5 mannequins, sample MetaHumans), which are not needed. |
| Note | 9 of the 1,263 copied files (UEFN mannequin materials, meshes, rig, textures) carry January 2026 modification dates later than the sample install, from the owner's pre-jam project. They are most likely engine re-saves during the 5.8 upgrade. Content changes are UNVERIFIED; declare if any owner edit is confirmed. |

## 5. Ultimate Horse System — Hivemind (Fab)

| Field | Value |
|---|---|
| Creator | Hivemind (Fab publisher, owner-confirmed 2026-11-12) |
| Source | Fab Marketplace: https://www.fab.com/listings/0f1d9f24-9f5a-42dd-8934-5d6dbf1bc002 ("Ultimate Horse System (Horse, Horse Riding, Horse System, Mount, Rideable Horse)", category: Game Systems / Gameplay Features) |
| Status | **PURCHASED** by the owner on 2026-11-12, during the jam (owner-confirmed). |
| License | PENDING OWNER REVIEW. Verify whether the purchased entitlement is Fab Standard Personal, Professional or another license. |
| Acquired | 2026-11-12. Exact order date/time to be confirmed from the Fab receipt. |
| Added to project | 2026-11-12 ~08:24 CET (file timestamps in `/Game/UltimateHorsePack`). Content only, no code plugin. |
| Pre-jam? | Third-party asset. It was not created by the team. |
| Use in game | Planned: horse, riding, mount/dismount and the horse drinking at the trough. |
| Compatibility | UE 5.8.4 support UNVERIFIED. Mount/dismount and rider alignment still need tests. |
| Redistribution | Not redistributed. Vendor code and assets stay private; shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |
| Open questions | Record the license tier and receipt; confirm the supported engine versions. |

## 6. Western weapon pack "HS_WeaponPack_03" (Fab)

| Field | Value |
|---|---|
| Creator | UNVERIFIED (to be read from the Fab listing). |
| Source | Fab Marketplace: https://www.fab.com/listings/05c6741c-5233-4367-9c0d-67b49c8aa745 |
| Status | **Free** (owner-confirmed, 2026-11-12). |
| License | PENDING OWNER REVIEW. Record the license shown in the Fab Library. |
| Acquired | 2026-11-12, during the jam. |
| Added to project | 2026-11-12 ~08:53 CET (file timestamps in `/Game/HS_WeaponPack_03`). |
| Contents | Revolvers (skeletal and static meshes), shoulder stock, powder flask, bullets, weapon holder board, materials and textures, demo map. |
| Use in game | Planned: Trevor's and Donovan's revolvers, ammunition and props for the duel and target practice. |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |
| Open questions | Creator name and license from the listing. |

---

## Pre-jam items to declare (summary)

The jam page asks entrants to "Declare any prompts, scripts, or assets you made before the jam" (see [JAM_RULES.md](JAM_RULES.md)). Current list:

| Item | Made / obtained | Status in the game |
|---|---|---|
| Game Animation Sample content (Epic) | Installed in the owner's local sample project on 2026-01-14 and upgraded to UE 5.8 before the jam. Imported into the jam project on 2026-11-12. | Third-party (Epic) locomotion content, used as-is. 9 files carry pre-jam re-save dates (see §4). |
| Owner's fixed-camera prototype (Blueprint) | January 2026 | Design reference only. The logic is re-implemented in C++ during the jam; no assets copied. |
| Agent rulebook ([AGENTS.md](../AGENTS.md)) | Written by the owner; creation date PENDING OWNER CONFIRMATION (local file saved 2026-11-12 07:38 CET). | Prompt/instructions for the agents, not game content. |
| Copilot plugin agent guide (private text file) | Written by the owner in August 2026. | Prompt/tooling instructions, not game content. Not published (it covers other private projects). |
| Tool setup: Ultimate Engine Copilot plugin and its MCP connection; a third-party Unreal Engine skills package for Claude Code | Set up before or at the jam start. | Tools only, allowed by the FAQ ("set up your tools, agents, and MCP ahead of time"). |
| SoerGame Western Animations (Fab, purchased) | Purchase date PENDING (Fab receipt). | Third-party asset (§2). |

## Pre-jam owner work used as reference only

| Item | Created | How it is used | Copied into the jam project? |
|---|---|---|---|
| Owner's fixed-camera prototype (UE 5.7, Blueprint, separate personal project) | Before the jam (January 2026) | Design reference for the fixed-camera behaviour: trigger-based camera switching and soft tracking. | **No.** No assets or code were copied. The jam camera system was written from scratch in C++ on 2026-11-12 (see TECHNICAL_DECISIONS TD-007). Declare as pre-jam design reference. |

---

## Development-only tools (NOT distributed)

| Tool | Creator / source | License | How it is used | Distributed in the game? |
|---|---|---|---|---|
| Ultimate Engine Copilot / Blueprint Generator Ultimate (Unreal Engine plugin, v2.4.0) | Fab Marketplace | Owner's Fab license | Editor automation during development, driven by Claude Code through the plugin's MCP server. It is enabled only in the jam project. | **No.** Used for development only. It must be disabled or excluded from the packaged build. Verification at the first packaged build is PENDING. |

See also [AI_TOOLS.md](AI_TOOLS.md).
