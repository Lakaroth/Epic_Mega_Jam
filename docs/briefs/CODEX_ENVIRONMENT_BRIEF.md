# Brief for Codex: western environment kit (Director's Cut)

**Project:** Director's Cut, a spaghetti-western game for the 2026 Epic AI MegaJam (solo developer: the owner).
**Your workspace:** a separate Unreal Engine **5.8** project on the laptop. Your output will be **migrated** into the main game project, so the conventions below are mandatory.
**Your scope:** environment art and props only. Gameplay, characters, animation, cameras and C++ are done in the main project. Do not build them.

---

## 1. The game, in short (what your work must serve)

- **Third person with fixed cinematic cameras**, Resident Evil style: each area is seen from placed cameras, usually high in a corner, focal length 18–35 mm.
  - **Facades are seen mostly from the front and at an angle.** Put the detail where cameras look, and keep the backs simple.
  - **Inside the frame, depth sells the shot:** foreground props, the street in the middle, buildings and far mesas behind.
- **Day 1 target: the duel on Main Street at high noon.** That is your first priority.
- **Hero:** about 180 cm tall. The player walks and runs, and **vaults** obstacles of **50 cm and 100 cm**. A horse is planned, about 160 cm at the withers.
- **Look:** Sergio Leone westerns. A dusty, sun-bleached frontier town, warm light, hard shadows, heat haze, weathered wood.

## 2. Deliverables, in priority order

### P1. Main Street kit (the duel)
1. **Street ground:** a dirt road with wagon ruts and hoof prints, using a tiling material plus decals.
   - Street about **60 m long and 12 m wide**.
2. **Building facades:** modular western "false front" buildings. Include at least:
   - a **saloon** with a swinging-door opening;
   - a **sheriff's office**;
   - a **general store**;
   - a **bank**.
   - 1–2 storeys, about **350 cm** per storey.
   - Module widths of **400 / 600 / 800 cm** on a 100 cm grid.
   - Doors at least **140 cm** wide and **240 cm** high, so the character can walk through.
3. **Boardwalk** in front of the buildings:
   - **400 cm** segments, **20–30 cm** high (walkable step);
   - step pieces;
   - posts and porch-roof (awning) pieces.
4. **Clock or bell tower** at one end of the street, so the duel can play at noon.

### P2. Props
Use real-world size, and keep each object's pivot at its base. Approximate sizes:

| Prop | Size |
|---|---|
| Barrel | 90 cm tall |
| Crates | 50 cm and 100 cm cubes |
| Water trough (horse drinking) | about 250 × 60 × 60 cm |
| Hitching rail | about 250 × 100 cm |
| Wanted-poster board | — |
| Lantern on a post | about 250 cm |
| Bench | — |
| Tumbleweed | — |
| Saloon chair and table | — |
| Wagon (optional) | — |
| Well (optional) | — |

### P3. Obstacles you can vault
- **Exact heights of 50 cm and 100 cm:** crates, a low fence, a low adobe wall, a stacked-barrel group.
- Model them only. The vault logic is added in the main project.
- Keep their top edges straight and clean.

### P4. Background
- Mesa and butte silhouettes, rocks, saguaro cacti, distant hills.
- Low poly, for the far distance, to close off the fixed-camera frames.

### P5. Light and atmosphere presets
- **High noon** and **sunset**, made with Sky Atmosphere, a Directional Light, Exponential Height Fog, Volumetric Clouds and a Post Process Volume:
  - warm grade;
  - strong contrast;
  - light film grain;
  - vignette.
- **Lumen only. No baked lighting.**
- Deliver each preset as a sublevel or a Level Instance, and write down the values.

## 3. Mandatory technical conventions

| Topic | Rule |
|---|---|
| Root folder | Everything under `/Game/_Game/_Environment/Western/` (subfolders `Meshes/`, `Materials/`, `Textures/`, `Decals/`, `Maps/`, `Presets/`). Nothing outside it. |
| Naming | `SM_` static mesh, `M_` material, `MI_` material instance, `T_` texture (suffixes `_D` base colour, `_N` normal, `_ORM` occlusion/roughness/metallic), `DI_`/`MI_` decal, `LV_` level. English names, no spaces. Example: `SM_WST_Barrel_A`. |
| Units and scale | Centimetres, real-world size, **pivot at the bottom centre** (modules: bottom-left corner on the 100 cm grid). |
| Collision | Simple collision on everything, either boxes or convex hulls. No "use complex as simple". |
| Geometry | Nanite on for meshes over about 5k triangles. Keep small props light. |
| Materials | A few **master materials** (weathered wood, plaster/adobe, rusty metal, ground) and their instances, with tint and wear parameters. Reuse them; do not make one material per prop. |
| Textures | **2K max** for hero assets, 1K for small props, packed `ORM` maps. |
| Budget | Your whole delivery must stay **under 300 MB on disk**. Keep the game lean; a final zip over 1 GB is uploaded with butler (jam page). |
| Engine content | Do not edit engine or Starter Content assets. Do not reference Starter Content. |
| Project settings | Keep 5.8 defaults (Lumen, Virtual Shadow Maps). Do not add plugins without telling the owner. |

## 4. Jam rules you must respect

- **Make everything during the jam** (from 12 November 2026, 06:00 CET).
  - Do not use anything made before the jam unless the owner approves it and it is declared.
- **Third-party assets** (Fab, Megascans or other) are allowed only with their **source and license recorded**. Prefer your own work.
- **AI is allowed, but it must be recorded.** For every AI tool you use (including image or 3D generators), record:
  - the tool;
  - what it made;
  - a short summary of the prompt.
- Do not copy content from other projects on the laptop.

## 5. Handover (needed for migration)

1. **Showcase map:** `LV_WST_Showcase` with every piece placed and labelled, plus a sample duel-street layout `LV_WST_MainStreet`.
2. **`README_WESTERN_KIT.md`** in the project root with:
   - **Asset table:** name, what it is, size in cm, triangle count, texture sizes, material used.
   - **Work log:** time (CET), what was done, tool used, and the prompt summary for any AI step.
   - **Provenance:** for every asset, "made in jam with ..." or "third party: source and license".
   - **Total disk size** of `/Game/_Game/_Environment/Western/`.
3. **Migration test:** use Asset Actions > Migrate on the `Western` folder into an empty 5.8 project, and confirm that it opens with no missing references.

## 6. Done checklist

- [ ] P1 complete and shown in `LV_WST_MainStreet`.
- [ ] Names, folders, pivots and scale follow section 3.
- [ ] Simple collision on every mesh.
- [ ] Under 300 MB; textures at 2K or less.
- [ ] README with the asset table, work log, provenance and size.
- [ ] Migration test passed with no missing references.
