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
| Source | Free Epic sample project for Unreal Engine 5.8 (Motion Matching locomotion). |
| License | Epic sample content for use in Unreal Engine projects. Exact license wording UNVERIFIED. |
| Use in game | Planned donor for Motion Matching: locomotion starts, stops, pivots, turn-in-place and the other clips the two packs above lack, plus the Pose Search setup. It is migrated into the jam project; we do not work inside the sample. |
| Status | Migration NOT performed yet as of 2026-11-12 08:12 CET. |
| Note | The migration must bring only Epic sample content. Unrelated pre-existing content from other owner projects must not be included. |

## 5. Ultimate Horse System — Hivemind (Fab)

| Field | Value |
|---|---|
| Creator | Hivemind (Fab publisher, owner-confirmed 2026-11-12) |
| Source | Fab Marketplace: https://www.fab.com/listings/0f1d9f24-9f5a-42dd-8934-5d6dbf1bc002 ("Ultimate Horse System (Horse, Horse Riding, Horse System, Mount, Rideable Horse)", category: Game Systems / Gameplay Features) |
| Status | **PURCHASED** by the owner on 2026-11-12, during the jam (owner-confirmed). |
| License | PENDING OWNER REVIEW. Verify whether the purchased entitlement is Fab Standard Personal, Professional or another license. |
| Acquired | 2026-11-12. Exact order date/time to be confirmed from the Fab receipt. |
| Added to project | Not yet, as of 2026-11-12 08:15 CET. |
| Pre-jam? | Third-party asset. It was not created by the team. |
| Use in game | Planned: horse, riding, mount/dismount and the horse drinking at the trough. |
| Compatibility | UE 5.8.4 support UNVERIFIED. Mount/dismount and rider alignment still need tests. |
| Redistribution | Not redistributed. Vendor code and assets stay private; shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |
| Open questions | Record the license tier and receipt; confirm the supported engine versions. |

---

## Development-only tools (NOT distributed)

| Tool | Creator / source | License | How it is used | Distributed in the game? |
|---|---|---|---|---|
| Ultimate Engine Copilot / Blueprint Generator Ultimate (Unreal Engine plugin, v2.4.0) | Fab Marketplace | Owner's Fab license | Editor automation during development, driven by Claude Code through the plugin's MCP server. It is enabled only in the jam project. | **No.** Used for development only. It must be disabled or excluded from the packaged build. Verification at the first packaged build is PENDING. |

See also [AI_TOOLS.md](AI_TOOLS.md).
