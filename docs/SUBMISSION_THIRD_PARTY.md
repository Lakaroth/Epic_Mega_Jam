# Third-party animations and Fab packs — submission declaration

**Game:** Director's Cut (2026 Epic AI MegaJam), by Elvis Morelli (Lakaroth).
**Status as of:** 2026-11-12, 17:40 CET. The final version must match the submitted build: only packs that ship in the build stay in the list.

None of the content below was made by the entrant. Each pack is used under the license from its source and ships only inside the compiled game. No source files are redistributed: the public repository holds text documentation only.

Full records, with evidence and open questions, are in [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md).

---

## 1. Animations

| Pack | Creator | Source | How obtained | Use in the game | Status |
|---|---|---|---|---|---|
| Game Animation Sample (GASP), version 5.8 | Epic Games | Epic's free sample project, unmodified 5.8 download | Free sample content | Player movement: Motion Matching locomotion, traversal over small obstacles, the character and animation blueprints. Our changes are listed in the development log. | **In use** |
| Western Animations | SoerGame | [Fab listing](https://www.fab.com/listings/6ff33fd3-f834-41f6-bf97-a0df10372304) | Purchased on Fab (date: PENDING, from the receipt) | Planned: duel (hand near holster, quick draw, firing, deaths), saloon idles (sitting at tables and at the bar), hat gestures. | In the project, **not yet in gameplay** |
| Eating and Drinking Animation Pack | Animaster Studio | [Fab listing](https://www.fab.com/listings/df3a9824-4cc8-425d-b986-10bfe4d5575a) | Purchased on Fab **during the jam**, 2026-11-12 | Planned: saloon life (drinking and eating at tables and at the bar, toasts, serving). | In the project (~14:03 CET), **not yet in gameplay** |

## 2. Other Fab packs

| Pack | Creator | Source | How obtained | Use in the game | Status |
|---|---|---|---|---|---|
| Ultimate Horse System | Hivemind | [Fab listing](https://www.fab.com/listings/0f1d9f24-9f5a-42dd-8934-5d6dbf1bc002) | Purchased on Fab **during the jam**, 2026-11-12 | Planned: the horse, riding, mount and dismount, the horse drinking at the trough. | In the project, **not yet in gameplay** |
| HS_WeaponPack_03 (western weapons) | PENDING (to be read from the listing) | [Fab listing](https://www.fab.com/listings/05c6741c-5233-4367-9c0d-67b49c8aa745) | Free on Fab, added **during the jam**, 2026-11-12 | Planned: revolvers, ammunition and weapon props for the duel and target practice. | In the project, **not yet in gameplay** |
| Saloon Interior | Quixel Megascans | [Fab listing](https://www.fab.com/listings/57991a62-f98f-4c6a-9b94-a74ec12f242e) | Acquired by the owner **before the jam** (pre-existing; license PENDING VERIFICATION) | Planned: the demo's saloon interior (bar, stools, tables, signs, decorations). | In the project (2026-11-12), **not yet in gameplay** |
| Ezio Tears – Crying System | Ezz Eldin Medhat | [Fab listing](https://www.fab.com/listings/a16ff48e-2e40-46d6-8147-430b6e6b69e3) | Purchased and paid on Fab **during the jam**, 2026-11-12 (confirmed by the owner; Fab Standard License) | Planned: tears on the MetaHuman actors in the duel and close-ups (installed and connected by the owner; no AI agent opens it: "Allows usage with AI: No"). | **Not yet in the project** |
| Casual Shirt – MetaHuman Clothes – Parametric Outfit | Cindy | [Fab listing](https://www.fab.com/listings/006666c2-ba60-43e6-a61a-7398a44f33c1) | Bought on Fab **during the jam** (owner's decision 2026-11-13; receipt date PENDING) | Planned: the new Trevor's shirt (fitted by the owner in MetaHuman Creator; no AI agent opens it: "Allows usage with AI: No"). | **Not yet in the project** |
| Dirty and Muddy Terrain Pack | 32cm | [Fab listing](https://www.fab.com/listings/f4622b3a-7cfb-4755-9ede-3f3c75642576) | Bought on Fab **during the jam**, 2026-11-13 (receipt PENDING) | Planned: mud and dirt ground materials for the exterior (8 seamless PBR textures; "Allows usage with AI: No", see ASSET_PROVENANCE §17). | **Not yet in the project** |
| "Click" (sound) | NenadSimic | [Freesound 157539](https://freesound.org/people/nenadsimic/sounds/157539/) | Free download, **CC0**, during the jam (2026-11-13) | The camera-change click. | **In use** |
| UE5 Rigged Hand, Male, White 40 | 3D Scan Store | [Store page](https://www.3dscanstore.com/unreal-engine-rigged-hands/ue5-rigged-hand-male-white-40) | Purchased **during the jam** (2026-11-13; license terms PENDING from the receipt) | Trevor's forearms and hands, adapted by the owner to the MetaHuman skeleton. | In the project (2026-11-13), on Trevor |
| African Slate Quarry | Quixel Megascans | [Fab listing](https://www.fab.com/listings/578d0ceb-5ccb-425f-abd5-e791a21551b6) | Free on Fab; acquisition date and license tier PENDING (owner's Fab Library) | Planned: rocks, ground and dressing of the desert level around the saloon. | In the project (2026-11-12, 22:59 CET), **not yet in gameplay** |

## 3. Epic Games engine content

| Content | Use | License |
|---|---|---|
| UE5 mannequins and template animation content (also bundled inside some packs above) | Placeholder bodies under the MetaHuman characters | Unreal Engine EULA |
| MetaHuman framework and the GASP mannequin-to-MetaHuman runtime retarget | The hero MetaHuman follows the GASP character's pose | Unreal Engine EULA / MetaHuman terms |

## 4. Tried during development and removed — not in the build, not declared as used

| Pack | Creator | Source | What happened |
|---|---|---|---|
| Free Animation Pack | Gamma Studio | [Fab listing](https://www.fab.com/listings/8de31c5d-93bc-4bd4-9606-ca789ce91b99) | A slower-walk test (12:20–12:40 CET) was rejected by the owner and fully removed. |
| FREE Motion Matching Walk Dance Card | Quantum Stage – Swiss Mocap Animations (Mocap ATLAS) | [Fab listing](https://www.fab.com/listings/1da7ad14-de22-426d-8ca0-7d467e43fc49) | A walk A/B test (12:55–13:10 CET) was rejected by the owner and fully removed. If it is used later: credit "Quantum Stage / Mocap ATLAS". |

---

## To complete before submission

- [ ] **Owner:** license tier and receipt date from the Fab Library for each purchased pack: SoerGame and Hivemind first, then Animaster Studio. (Ezio Tears: purchase date confirmed by the owner, 2026-11-12.)
- [ ] Fab Library entitlement for HS_WeaponPack_03 (free).
- [ ] Ezio Tears: test in PIE and in a packaged Windows build.
- [ ] Saloon Interior (Quixel Megascans, pre-existing): verify the historical acquisition license and date in the owner's Library.
- [ ] Creator name of HS_WeaponPack_03.
- [ ] African Slate Quarry (Quixel Megascans, free): acquisition date and license tier from the owner's Fab Library; add it to the form text below once it is in gameplay.
- [ ] Remove the rows for packs that do not ship. Packs that are not used are not migrated into the final project.
- [ ] Update each "Use in the game" cell to what the final build really uses.

## Text for the submission form (draft)

> Third-party content (not made by the entrant, used under each source's license, shipped only inside the compiled game):
> Game Animation Sample 5.8 by Epic Games (player locomotion and traversal); Western Animations by SoerGame (Fab); Eating and Drinking Animation Pack by Animaster Studio (Fab, bought during the jam); Ultimate Horse System by Hivemind (Fab, bought during the jam); Saloon Interior by Quixel Megascans (Fab, acquired before the jam); Ezio Tears – Crying System by Ezz Eldin Medhat (Fab, bought during the jam); HS_WeaponPack_03 (Fab, free); UE5 mannequins and MetaHuman framework by Epic Games.

This draft lists every pack currently planned. Before submitting, cut it to the packs that ship.
