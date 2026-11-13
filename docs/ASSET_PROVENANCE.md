# Asset Provenance — Director's Cut (2026 Epic AI MegaJam)

This is a record of every third-party and pre-existing component used in the private Unreal project.
**It is the list of items to declare in the jam submission.** The final declaration covers the assets actually used in the submitted build. It will be cross-checked against the clean migration of the final maps.
Entries marked **Tried and removed — not in the build** (§1, §7) are kept only as a record of what was tested; they are not part of the declaration.
Submission-ready summary of the animations and Fab packs: [SUBMISSION_THIRD_PARTY.md](SUBMISSION_THIRD_PARTY.md).
Only text is published here. Source assets, Blueprints, animations, plugins and packaged third-party project files are **never** published in this repository.

Status legend: **VERIFIED** (evidence on file) · **PENDING OWNER REVIEW** · **UNVERIFIED**.
Exact license evidence (Fab Library entitlement / receipt) must be recorded for each asset before final submission.

---

## 1. Gamma Studio — Free Animation Pack (Fab) — Tried and removed, not in the build

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
| Use in game | **Not used in the game** as of 2026-11-12 12:45 CET. A test (12:20–12:40 CET) retargeted its 4 male unarmed walk loops to the sample's UEFN mannequin skeleton and added them to the walk Motion Matching database for a slower walk. The owner rejected the result, and everything from that test was removed (clips, retargeter, database entries, speed changes). |
| Redistribution | Not redistributed. Not in the build: the pack stays in the private sandbox project and is not migrated. |
| Submission declaration | **Not declared as used** (not in the build). Record only. |

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
| Source | Free Epic sample project (Motion Matching locomotion), **version 5.8, unmodified**, copied from the Epic Games Launcher download cache on the owner's machine (the launcher refreshed it on 2026-11-12 at 10:16 CET, when the owner created a new 5.8 sample project). |
| License | Epic sample content for use in Unreal Engine projects. Exact license wording UNVERIFIED. |
| Use in game | Player locomotion: the sample's CMC character, animation blueprint, Motion Matching databases and choosers, traversal (small obstacles) and input. Our changes are listed in the development log (walk as the default, no jump, speeds, no sprint, traversal picks without the spinning hurdle variants, input bindings). Unused sets (e.g. sprint, crouch) will be pruned before the clean migration. |
| Status | **Current content imported 2026-11-12 ~10:20 CET**: 1,417 packages (~1.24 GB) from the unmodified 5.8 download, at their original paths, plus 366 packages at ~11:08 CET for MetaHuman support (below). The exact file lists are kept locally. |
| Earlier import (replaced) | From 08:54 to ~10:20 CET the project used a first import (1,430 packages) taken from the owner's older local copy of the same sample. At ~10:20 it was removed from the project and replaced by the unmodified 5.8 download above; it is kept only as an offline backup outside the project. A disk check at 12:33 CET found no leftover file from that first import. |
| Excluded on purpose | The sample's alternate display characters (Echo, Paragon, UE4/UE5 mannequins), its sample game mode and physics obstacle props, which are not needed. |
| MetaHuman support | 2026-11-12 ~11:08 CET: the sample's generic runtime retarget (mannequin to MetaHuman), the shared MetaHuman files and Epic's sample MetaHuman "Kellan" (used only to test the pipeline) were imported from the same unmodified 5.8 download. |

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
| Use in game | Planned: horse, riding, mount/dismount and the horse drinking at the trough. Since 2026-11-13: the opening scene (the pack's realistic horse, western saddle, horse idle and rider mount idle), being blocked out. |
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

## 7. Quantum Stage — FREE Motion Matching Walk Dance Card (Fab) — Tried and removed, not in the build

| Field | Value |
|---|---|
| Creator | Quantum Stage – Swiss Mocap Animations (Mocap ATLAS) |
| Source | Fab Marketplace: https://www.fab.com/listings/1da7ad14-de22-426d-8ca0-7d467e43fc49 |
| Status | Free. |
| License | The Fab listing shows no license terms. The owner reports that Quantum Stage confirmed by email that the dataset may be used. Email date: PENDING. |
| Added to project | 2026-11-12 ~12:33 CET (`/Game/QS_MM_Sample`). |
| Pre-jam? | Third-party asset. It was not created by the team. |
| Contents | One 42 s motion-capture walk take (forward walk with left and right turns of 45°, 90°, 135° and 180°) for the UE5 Mannequin and MetaHuman skeletons, demo meshes, a demo map and a sequence. |
| Use in game | **Not used in the game** as of 2026-11-12 13:10 CET. An owner A/B test (12:55–13:10 CET) retargeted the take to the Game Animation Sample's mannequin skeleton and swapped it in for the sample's walk; the owner rejected it, and every asset made for the test was removed. The pack itself is still in the private sandbox project and will not be migrated unless used. |
| Credit | If used: credit **Quantum Stage / Mocap ATLAS** in the game and in the submission, and note the creator's email confirmation. |
| Redistribution | Not redistributed. No source files in this repository. |
| Submission declaration | **Not declared as used** (not in the build). Record only. |

## 8. Props made with Tripo during the jam (owner)

Props generated by the owner with the Tripo AI 3D tool during the jam, imported as glTF and made game-ready in the project (texture size cap, compression, names, simple collision, Nanite) with a project script.

| Prop | Made | Tool and prompt | In-game textures | Status |
|---|---|---|---|---|
| Chair (`SM_Chair`) | 2026-11-12, ~13:20 CET | Tripo. Prompt: PENDING (owner to record). | 512 px (source kept in the editor) | Placed in the blockout level. |
| Table (`SM_Table`) | 2026-11-12, ~13:35 CET | Tripo. Prompt: PENDING (owner to record). | 512 px (1024 px source kept in the editor) | Placed in the blockout level. |

### Trevor's gunbelt and holster (owner, made during the jam)

| Asset | Made | Source file | In the project |
|---|---|---|---|
| Gunbelt (`SK_Trevor_Gunbelt`) | By the owner on 2026-11-12, during the jam (owner, 2026-11-12). | `SK_Belt_LOD0.fbx`, exported 2026-11-12 12:25 CET | `/Game/_Game/_Characters/Trevor/Gear/Gunbelt/` |
| Holster (`SK_Trevor_Holster`) | By the owner on 2026-11-12, during the jam (owner, 2026-11-12). | `SK_Holster_LOD0.fbx`, exported 2026-11-12 12:25 CET | `/Game/_Game/_Characters/Trevor/Gear/Holster/` |

## 9. Eating and Drinking Animation Pack — Animaster Studio (Fab)

| Field | Value |
|---|---|
| Creator | Animaster Studio (Fab seller, from the listing) |
| Source | Fab Marketplace: https://www.fab.com/listings/df3a9824-4cc8-425d-b986-10bfe4d5575a |
| Status | **PURCHASED** by the owner during the jam (owner, 2026-11-12). |
| License | PENDING OWNER REVIEW. Record the license tier from the Fab Library or receipt. The listing says "Generated with AI: No". |
| Acquired | 2026-11-12, during the jam (exact time from the Fab receipt PENDING). |
| Added to project | 2026-11-12 ~14:03 CET (file timestamps in `/Game/Eating_Drinking_Anim_anim`, 313 files). |
| Pre-jam? | No. It is a third-party asset bought during the jam. It was not created by the team. |
| Contents | 40 in-place animations on the Epic skeleton (Manny/Quinn), UE 5.3+: eating and drinking while standing, sitting or walking; pouring; raising a cup for a toast; serving with a tray; after-meal reactions; getting up after eating. There are no chair pull/push animations and no meshes. |
| Planned use | Saloon life: drinking and eating at tables and at the bar, toasts, the bartender serving. Retarget to the sample's character skeleton is needed. |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |

## 10. Revolver sound effects (third-party, downloaded during the jam)

| Sound in the game | Source file (owner's download, 2026-11-12) | Source / license | Edit in the project |
|---|---|---|---|
| `SW_Revolver_Draw` (draw) | `drawgun.wav` (15:37 CET) | PENDING OWNER REVIEW: origin and license not yet recorded. | Leading silence and tail cut (0.40 s); played 1.25x faster. |
| `SW_Revolver_Cock` (hammer click after the draw) | `freesound_community-pistol-hammer-cocking-back-4-39887.mp3` (15:51) | Pixabay sound effects (owner-confirmed 2026-11-12, found through https://pixabay.com/sound-effects/search/revolvers/), uploader "freesound_community", id 39887. Pixabay Content License. | Leading silence cut (0.38 s). |
| `SW_Revolver_Shot` (shot) | `freesound_community-single-pistol-gunshot-33-37187.mp3` (15:51) | As above (id 37187). | Trimmed to 1.26 s, faded tail, gain 0.85 (the source is clipped). |
| `SW_Revolver_Spin` (cylinder spin, kept for later scenes) | `freesound_community-revolver-spin-96947.mp3` (15:50) | As above (id 96947). | Trimmed to 2.89 s. |

Pixabay Content License, as summarised in Pixabay's FAQ and Terms (read 2026-11-12, https://pixabay.com/service/license/): free for commercial use, including inside a game; no attribution required (suggested credit: "by freesound_community via Pixabay"); the files must not be sold or distributed on their own. Our use: only inside the compiled game; the source files are not published. Planned credit line: "Sound effects by freesound_community via Pixabay".

## 11. Saloon Interior — Quixel Megascans (Fab)

| Field | Value |
|---|---|
| Creator | Quixel Megascans (Epic Games; Fab seller "Quixel Megascans"). |
| Source | Fab Marketplace (current listing): https://www.fab.com/listings/57991a62-f98f-4c6a-9b94-a74ec12f242e |
| Status | **PRE-EXISTING third-party asset.** Acquired by the owner years before the jam (owner, 2026-11-12). Not made by the team. |
| License | Owner's statement: previously acquired Quixel assets keep their original licensing rights. The exact historical acquisition license is **PENDING VERIFICATION** in the owner's Fab/Quixel Library. The current listing shows "Generated with AI: No" and "Allows usage with AI: Yes"; it shows no named license ("License terms: -"). |
| Acquired | Before the jam (years earlier, owner). Exact date PENDING VERIFICATION (Library). |
| Added to project | Yes, by the owner via Fab, present on 2026-11-12 (evening): folder `/Game/Scene_Saloon`, showcase map `Historic_Saloon`. Private jam project only. |
| Pre-jam? | Yes: pre-existing third-party content, declared in the pre-jam summary below. |
| Contents | From the listing: a modular saloon interior set of 73 assets (bar, bar stools, tables, vintage signs, decorations). FBX meshes with JPG textures (1K, 2K, 4K or 8K); a showcase scene for Unreal Engine 5.4-5.6. The listing gives no polygon counts. |
| Planned use | The demo's saloon interior. |
| Redistribution | Not redistributed. The source assets are not published; they ship only inside the compiled game build. |
| Submission declaration | To be declared as a pre-existing third-party asset. Status: PENDING. |

## 12. Ezio Tears – Crying System (Fab)

| Field | Value |
|---|---|
| Creator | Ezz Eldin Medhat (Fab publisher, from the listing). The description is branded "Ezio Production Studio". |
| Source | Fab Marketplace: https://www.fab.com/listings/a16ff48e-2e40-46d6-8147-430b6e6b69e3 |
| Status | **PURCHASED AND PAID** by the owner on 2026-11-12, during the Epic AI MegaJam (**confirmed by the owner**, 2026-11-12). |
| License | Fab Standard License (owner's review, 2026-11-12): commercial use in a game and modification allowed. Purchase date confirmed by the owner (2026-11-12); license tier to be re-checked in the Fab Library. The listing says "Generated with AI: No" and "Allows usage with AI: No". |
| Acquired | 2026-11-12, during the jam: purchase and payment confirmed by the owner. Approximate time ~16:30 CET (exact time from the Fab receipt not recorded). |
| Added to project | Not yet (2026-11-12). The owner installs it and connects it to Trevor by hand. |
| Pre-jam? | No. It is a third-party asset bought during the jam. It was not created by the team. |
| Contents | From the listing and the developer's guide (owner, 2026-11-12): a procedural crying system for MetaHuman characters (UE 5.8.4, MetaHuman 5.8, Win64; uses the ProceduralMeshComponent plugin). Tears form on the lower eyelids, run down the animated face and leave wet, reflective trails; simulation in Play and a cache for Sequencer. |
| Planned use | Tears on the MetaHuman actors in the duel and close-ups. |
| "Allows usage with AI: No" | A restriction on using the content as input to generative AI, separate from the commercial license. Project rule: **no AI agent opens, reads, analyses or rewrites this pack's files or source.** The owner installs, connects and edits it by hand; our code may only call its documented public functions. |
| Build check | To test in PIE and in a packaged Windows build. |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |

## 13. African Slate Quarry — Quixel Megascans (Fab)

| Field | Value |
|---|---|
| Creator | Quixel Megascans (Epic Games). |
| Source | Fab Marketplace: https://www.fab.com/listings/578d0ceb-5ccb-425f-abd5-e791a21551b6 (free listing). |
| Status | Third-party asset, not made by the team. |
| License | The listing shows "Allows usage with AI: Yes" (checked 2026-11-12). License tier and acquisition date are **PENDING OWNER CONFIRMATION** (Fab Library). |
| Acquired | PENDING OWNER CONFIRMATION (Fab Library). |
| Added to project | 2026-11-12, 22:59 CET (file creation times in the Content manifest, see "Content snapshots" below): folder `/Game/Scene_QuarrySlate` (396 files: meshes, materials, the showcase map `Quarry_Slate`). Private jam project only. |
| Planned use | Rocks, ground and dressing for the game's single desert level around the saloon (owner's direction, 2026-11-12). The pack's showcase frame meshes are not used. |
| Redistribution | Not redistributed. The source assets are not published; they ship only inside the compiled game build. |
| Submission declaration | To be declared as a sourced asset (Official Rules §15(c)). Status: PENDING. |

## 14. NVIDIA DLSS 4.5 plugins for Unreal Engine (NVIDIA)

| Field | Value |
|---|---|
| Creator | NVIDIA Corporation. |
| Source | NVIDIA developer site, https://developer.nvidia.com/rtx/dlss/get-started : "UE 5.8 DLSS Plugin", file `2026.10.16_UE5.8_DLSS4.5Plugin_v8.9.0.zip` (plugin 8.9.0, Streamline SDK 2.14.16, NGX SDK 310.9.16). Downloaded by the owner on 2026-11-13. |
| License | "NVIDIA RTX SDKs LICENSE", shipped with the plugin (`Plugins/DLSS/Source/ThirdParty/NGX/LICENSE.txt`, read in full 2026-11-13); it supersedes the older "NVIDIA RTX SDK EULA" PDF (v. February 2021) in the package's Documentation folder. Streamline SDK headers: MIT license (NVIDIA). Distribution of the runtime parts inside a game is allowed under the license's distribution requirements. The NVIDIA attribution conflicts with Official Rules §15(d); see [JAM_RULES.md](JAM_RULES.md), Owner decisions §3. |
| Obligations (verified 2026-11-13) | 1. **Attribution** (Supplement §7.1(b)): "For applications that incorporate the DLSS SDK or NGX SDK or portions thereof, you must attribute the use of the applicable SDK and include the NVIDIA Marks on splash screens, in the about box of the application (if present), and in credits for game applications." "NVIDIA Marks" = "NVIDIA RTX™" (§7.2(c)). 2. **Approval of each use of the Marks** (§7.2(c)): follow NVIDIA's style guidelines and "submit a sample of each proposed use of NVIDIA's Marks at least two (2) weeks prior to the desired implementation"; no answer within ten business days = not approved. Cannot be met before the jam deadline; the owner emails the samples to nvidia-rtx-license-questions@nvidia.com on 2026-11-13. 3. **No endorsement claim** (§4(c)): do not suggest the game is sponsored or endorsed by NVIDIA; no promotional NVIDIA logo beyond the required attribution (owner, 2026-11-13). 4. **Third-party notices** (DLSS Programming Guide §4.2.3): ship the copyright and license texts of guide §9.5-9.6 with the game: `Legal/THIRD_PARTY_NOTICES.txt` in the private project (also holds the Streamline MIT notice). 5. **Release DLLs only** (guide §4.2): the development DLSS DLLs (on-screen notices) must not ship; the plugin uses the release binaries by default (`r.NGX.BinarySearchOrder 0`), to check in the packaged build. 6. **Notification before commercial release** (Supplement §4, https://developer.nvidia.com/sw-notification): not triggered by a free jam entry; required if the game is released commercially later. 7. **Press releases** (§7.1(c)) must reference the NVIDIA RTX SDK and NVIDIA, if any are issued. |
| Prepared attribution text | Splash card (text only, no logo): "NVIDIA DLSS · NVIDIA RTX™". Credits: "NVIDIA DLSS and NVIDIA Streamline — NVIDIA RTX™ technology by NVIDIA Corporation." Both pending NVIDIA's approval (item 2) and the organizers' answer on §15(d). |
| Added to project | 2026-11-13, project-local `Plugins/` (not in git): DLSS, StreamlineNGXCommon, StreamlineCore, StreamlineReflex, StreamlineDLSSG, DLSSMoviePipelineSupport. Not installed: NIS, StreamlineDeepDVC, the deprecated Streamline plugin. |
| Planned use | DLSS Super Resolution / DLAA / Ray Reconstruction and Frame Generation with Reflex on NVIDIA RTX GPUs; TSR stays the fallback on other GPUs. Candidate for the jam's NVIDIA RTX Award ("DLSS 4.5 (Unreal Engine)"). |
| Redistribution | Only the plugin's runtime binaries inside the compiled build. Not published otherwise. |
| Submission declaration | Declare as a third-party SDK, and answer the NVIDIA questions if DLSS ships. Status: PENDING (owner decision on attribution). |

## 15. Casual Shirt – MetaHuman Clothes – Parametric Outfit (Fab)

| Field | Value |
|---|---|
| Creator | Cindy (Fab seller). |
| Source | Fab Marketplace: https://www.fab.com/listings/006666c2-ba60-43e6-a61a-7398a44f33c1 (EUR 9.04 before taxes, read 2026-11-13). |
| Status | **Owner's decision to use it: 2026-11-13, ~09:05 CET** (for the new Trevor's shirt). Purchase date and license tier: PENDING (Fab receipt). |
| Listing facts | Parametric shirt for MetaHuman Creator ("fits onto any body shape in MetaHumanCreator"; listed body types: tall / medium build, man and woman). MetaHuman skeleton. Static mesh in FBX plus cloth and outfit assets (`CA_`, `OA_`, a Dataflow graph). Folder note mentions UE 5.6 / 5.7. "Generated with AI: No". **"Allows usage with AI: No"**. "License terms": not shown on the listing. |
| AI rule | **Owner's decision (2026-11-13):** the "NoAI" flag forbids using the content to train AI; using it in the game is allowed, and the agents may work with it in the project. No training takes place. |
| Note | The listing ships cloth-simulation assets; the owner's rule is no Chaos Cloth in the game, so it is used as a skinned garment if the outfit allows it (owner to check). |
| Pre-jam? | No. Third-party asset obtained during the jam. Sourced asset: noted, not scored (§15(c) of the Official Rules). |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |

## 16. UE5 Rigged Hand, Male, White 40 — 3D Scan Store

| Field | Value |
|---|---|
| Creator | 3D Scan Store. |
| Source | https://www.3dscanstore.com/unreal-engine-rigged-hands/ue5-rigged-hand-male-white-40 (the site refuses automated reading; listing details and license not read by the agent). |
| Status | **Purchased by the owner during the jam** (recorded 2026-11-13, ~10:30 CET). Price, license name and terms: PENDING (owner's receipt and the store's license). |
| Use in game | Trevor's forearms and hands. The owner adapted them into `SK_West_Hero_Hands` (MetaHuman body skeleton, all 9,308 vertices skinned, fingers included; owner's 2K base colour, normal and specular maps), imported 2026-11-13. The matching arm geometry was removed from a copy of the MetaHuman body (`SKM_MHC_Hero_Western_BodyMesh_NoArms`) so the two never overlap; the seam sits under the shirt. |
| Pre-jam? | No. Third-party asset bought during the jam. Sourced asset: noted, not scored (§15(c)). |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset. Status: PENDING. |

## 17. Dirty and Muddy Terrain Pack (Fab)

| Field | Value |
|---|---|
| Creator | 32cm (Fab seller). |
| Source | Fab Marketplace: https://www.fab.com/listings/f4622b3a-7cfb-4755-9ede-3f3c75642576 (EUR 4.51 before taxes, read 2026-11-13). |
| Status | **Purchased by the owner during the jam** (recorded 2026-11-13, ~12:15 CET). License tier and receipt: PENDING (Fab receipt). |
| Listing facts | "8 different seamless PBR textures": soil, mud, gravel, puddles and dirt. Format: "Unreal Engine" (no engine version listed). "Generated with AI: No". **"Allows usage with AI: No"**. "License terms": not shown on the listing. |
| AI rule | Same flag as the Casual Shirt (§15). The owner's reading recorded there (the flag forbids using the content to train AI; using it in the game is allowed) is applied here. No training takes place. |
| Use in game | Planned: ground materials (mud and dirt) for the exterior. Not yet in the project. |
| Pre-jam? | No. Third-party asset bought during the jam. Sourced asset: noted, not scored (§15(c) of the Official Rules). |
| Redistribution | Not redistributed. Shipped only inside the compiled game build. |
| Submission declaration | To be declared as a third-party asset if it ships. Status: PENDING. |

## 18. "Click" by NenadSimic (Freesound, CC0)

| Field | Value |
|---|---|
| Creator | NenadSimic (Freesound user). |
| Source | https://freesound.org/people/nenadsimic/sounds/157539/ (read 2026-11-13). |
| License | **Creative Commons 0** (public domain dedication): commercial use allowed, no attribution required. Credited anyway in the third-party list. |
| Use in game | The camera-change click (D-pad camera cuts), `/Game/_Game/_Audio/UI/SW_UI_CameraCut`. Chosen by the owner on 2026-11-13. |
| Pre-jam? | No. Third-party asset obtained during the jam. Sourced asset: noted, not scored (§15(c)). |
| Redistribution | Shipped only inside the compiled game build. |

## 19. Typefaces: IM Fell English SC, EB Garamond, Courier Prime (SIL Open Font License)

| Field | Value |
|---|---|
| Fonts and authors | **IM Fell English SC**: Copyright (c) 2010, Igino Marini. **EB Garamond**: Copyright 2017 The EB Garamond Project Authors (Georg Duffner, Octavio Pardo). **Courier Prime**: Copyright 2015 The Courier Prime Project Authors (Quote-Unquote Apps). |
| Source | Google Fonts repository on GitHub (`google/fonts`, folders `ofl/imfellenglishsc`, `ofl/ebgaramond`, `ofl/courierprime`), downloaded during the jam on 2026-11-13 (~12:47 CET), each with its `OFL.txt`. |
| License | **SIL Open Font License 1.1**: free to use, embed and bundle with software, including commercial software. The copyright notice and the license text must ship with the fonts; the fonts may not be sold on their own; a modified font may not use a Reserved Font Name. The fonts are not modified. |
| Use in game | HUD and UI type, chosen by the owner on 2026-11-13: IM Fell English SC for titles and labels (in use: the "Camera Cuts" label), EB Garamond for body text and subtitles, Courier Prime for small technical text (both imported, planned for the menus and subtitles). Assets in `/Game/_Game/_UI/Fonts`. |
| Pre-jam? | No. Third-party assets obtained during the jam. Sourced assets: noted, not scored (§15(c)). |
| Redistribution | Embedded in the compiled game build only. **To do for the build:** add the three `OFL.txt` files (copyright and license) to the build's third-party notices. |

## 20. "Revolver Loading - Remington 1875" by Guy_Personface (Freesound, CC0)

| Field | Value |
|---|---|
| Creator | Guy_Personface (Freesound user). |
| Source | https://freesound.org/people/Guy_Personface/sounds/795317/ (read 2026-11-13). Unedited 32-bit recording, 7.6 s, stereo, 48 kHz, uploaded 2025-03-24. |
| License | **Creative Commons 0** (public domain dedication): commercial use allowed, no attribution required. Credited anyway in the third-party list. |
| Use in game | Two short cuts, normalized and made mono (the 3 MB original is not in the project): a round going into the cylinder (`SW_Reload_Round`, 0.28 s) and the light clicks of the gate (`SW_Reload_Gate`, 0.40 s), for the revolver reload. Chosen by the owner on 2026-11-13. |
| Pre-jam? | No. Third-party asset obtained during the jam (2026-11-13). Sourced asset: noted, not scored (§15(c)). |
| Redistribution | Shipped only inside the compiled game build. |

## 21. "revolvercock1.wav" by Dredile (Freesound, CC0)

| Field | Value |
|---|---|
| Creator | Dredile (Freesound user). |
| Source | https://freesound.org/people/Dredile/sounds/111676/ (read 2026-11-13). "Cocking an old revolver." 0.67 s, mono, 44.1 kHz, uploaded 2011-01-07. |
| License | **Creative Commons 0** (public domain dedication): commercial use allowed, no attribution required. Credited anyway in the third-party list. |
| Use in game | The hammer being cocked (`SW_Revolver_HammerCock`, silence trimmed, 0.38 s). Chosen by the owner on 2026-11-13 to replace the earlier cock sound. |
| Pre-jam? | No. Third-party asset obtained during the jam (2026-11-13). Sourced asset: noted, not scored (§15(c)). |
| Redistribution | Shipped only inside the compiled game build. |

---

## Content snapshots (made-during-the-jam evidence)

The project's `Content/` folder (binary assets) is not in version control. To show when each asset appeared or changed (Official Rules §7(h) and §7(j)), the private project keeps a tracked manifest of every file under `Content/`: path, size, creation time, modification time and SHA-256. It is regenerated and committed at the end of each jam day by `Tools/Provenance/content_manifest.py`. Only the manifest's own SHA-256 is published here; the file list itself stays private. Ezio Tears folders are skipped unread (§12).

| Snapshot | Files | Size | Manifest SHA-256 | Private commit |
|---|---|---|---|---|
| 2026-11-13 07:56 CET | 4702 | 16.36 GB | `8c06dece711a313c61dc87708227063913f6429e08107255858633dd5fc9b5cc` | 6c4b4b8 |

---

## Pre-jam items to declare (summary)

The jam page asks entrants to "Declare any prompts, scripts, or assets you made before the jam" (see [JAM_RULES.md](JAM_RULES.md)). Current list:

| Item | Made / obtained | Status in the game |
|---|---|---|
| Game Animation Sample content (Epic) | Third-party Epic content, not made by the owner. The copy in the project is the unmodified 5.8 download (see §4). An earlier import from the owner's older local copy of the sample was used from 08:54 to ~10:20 CET on 2026-11-12 and then replaced. | Used as-is with the changes listed in the development log. |
| Agent rulebook ([AGENTS.md](../AGENTS.md)) | Written by the owner; creation date PENDING OWNER CONFIRMATION (local file saved 2026-11-12 07:38 CET). | Prompt/instructions for the agents, not game content. |
| Copilot plugin agent guide (private text file) | Written by the owner in August 2026. | Prompt/tooling instructions, not game content. Not published (it covers other private projects). |
| Tool setup: Ultimate Engine Copilot plugin and its MCP connection; a third-party Unreal Engine skills package for Claude Code | Set up before or at the jam start. | Tools only, allowed by the FAQ ("set up your tools, agents, and MCP ahead of time"). |
| SoerGame Western Animations (Fab, purchased) | Purchase date PENDING (Fab receipt). | Third-party asset (§2). |
| Animaster Studio Eating and Drinking Animation Pack (Fab, purchased) | Bought by the owner during the jam, 2026-11-12 ~14:05 CET. Not pre-jam; listed here so the submission declares it. | Third-party asset (§9). Not yet in the project. |
| Saloon Interior — Quixel Megascans (Fab) | Acquired by the owner years before the jam. Exact acquisition date and license PENDING VERIFICATION (Library). | Pre-existing third-party asset (§11). In the project since 2026-11-12. |
| Ezio Tears – Crying System (Fab, purchased) | Bought and paid by the owner during the jam, 2026-11-12 ~16:30 CET (confirmed by the owner). Not pre-jam; listed here so the submission declares it. | Third-party asset (§12). Not yet in the project. |
| **Trevor "Angel Eyes" Ramsey** (hero MetaHuman) | Created by the owner on 2026-11-11, the day before the jam. Built with MetaHuman Creator and the owner's proprietary MetaWrap tool. Clothing (shirt, trousers) made by the owner; the hat was made with the Tripo AI tool (see AI_TOOLS.md). Hat-hair groom made by the owner. | Pre-jam owner work, imported into the jam project on 2026-11-12 (~11:20 CET, optimized version). Declared as pre-jam. **Official Rules §7(h)** allow only tools, agent setups, MCP settings, prompts and scripts to be made before the jam; other game content must be made during it unless it is a sourced (non-original) asset. OWNER DECISION PENDING: see [JAM_RULES.md](JAM_RULES.md), "Owner decisions". **2026-11-13 (owner):** this pre-jam version is only a placeholder for tests. The owner is creating a new Trevor during the jam, as a new MetaHuman Character asset; the placeholder is to be replaced by it. |

---

## Development-only tools (NOT distributed)

| Tool | Creator / source | License | How it is used | Distributed in the game? |
|---|---|---|---|---|
| Ultimate Engine Copilot / Blueprint Generator Ultimate (Unreal Engine plugin, v2.4.0) | Fab Marketplace | Owner's Fab license | Editor automation during development, driven by Claude Code through the plugin's MCP server. It is enabled only in the jam project. | **No.** Used for development only. It must be disabled or excluded from the packaged build. Verification at the first packaged build is PENDING. |

See also [AI_TOOLS.md](AI_TOOLS.md).
