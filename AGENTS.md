AGENTS.md — 2026 Epic AI MegaJam / Director's Cut
READ THIS ENTIRE FILE BEFORE TAKING ANY ACTION.
Project owner: Elvis Morelli (creator alias: Lakaroth).
Public documentation repository: https://github.com/Lakaroth/Epic_Mega_Jam
Working engine: Unreal Engine 5.8.4, Windows, C++ project.
Agent workflow: Claude Code (Opus) + Ultimate Engine Copilot / Blueprint Generator.

0. Mission and hard boundaries
Create a short, cinematic, playable spaghetti-western game for the 2026 Epic AI MegaJam, themed DIRECTOR'S CUT. The distinctive mechanic is player-directed cinematography: the player changes cameras during cutscenes and a high-tension duel inspired by the visual grammar of Sergio Leone, while still directly controlling gameplay.

The public GitHub repository is a truthful development journal and planning repository, not a mirror of the proprietary Unreal project. Keep source assets, MetaHuman source files, purchased content, generated media, project binaries and vendor packages local/private unless the owner explicitly approves a specific file for publication and confirms its redistribution rights. Public documentation must be sufficient for a reviewer to follow the real work without obtaining proprietary files.

Non-negotiables:
1. Compliance before convenience. Read the official rules; do not guess that a pre-jam or third-party asset is allowed. Flag uncertainty for owner review.
2. Never fabricate provenance, dates, commits, screenshots, benchmarks, tool use, or development evidence. Do not backdate or make a pre-jam asset appear jam-created.
3. No public Git push without explicit owner approval for that push. Prepare commits and a staged-file report first.
4. Never publish assets, weights, binaries, vendor code, private prompts containing secrets, credentials, license keys, or confidential data. .gitignore is helpful, not a security boundary.
5. Do not delete, overwrite, migrate, or restructure working project data or Git history without explicit approval. Keep backups, prefer reversible changes.
6. Never claim a feature is implemented, tested, legally cleared, or jam-compliant without evidence. Mark unknown items UNVERIFIED.
7. Make a functional Windows build first; preserve working milestones. No speculative polish at the expense of a playable game.
8. Every asset must have legitimate commercial-use rights. Open/permissive licenses (MIT, Apache-2.0, BSD, CC0, appropriate CC BY) are welcome with conditions respected; paid marketplace licenses can be used within their terms. Avoid noncommercial/restrictive terms and unauthorized redistribution.
9. Do not upload personal videos or recordings without owner's approval. Elvis will record selected genuine sessions himself.
1. Jam facts and verification
- Official jam: https://itch.io/jam/2026-epic-ai-megajam
- Official theme, confirmed by the organizer email: DIRECTOR'S CUT.
- Scheduled start: 2026-11-12 00:00 ET = 2026-11-12 06:00 CET (Italy).
- Submission deadline: 2026-11-15 20:59 ET = 2026-11-16 02:59 CET (Italy).
- Public organizer discussion: https://forums.unrealengine.com/t/vibe-your-way-to-50k-the-2026-epic-ai-megajam-is-coming/2843973
Agent must independently read the then-current official jam rules, FAQ, submission form, and partner-prize conditions before deciding eligibility. Preserve citations/links, date accessed, and a short evidence-based interpretation in docs/JAM_RULES.md. Organizer emails shared by the owner are valid project evidence, but do not present an unverified interpretation as a ruling by Epic. If FAQ and full legal rules conflict or are unclear, stop and flag for owner; stricter wording and official clarification take priority.

Especially sensitive: pre-existing personally authored shaders, materials, reusable scripts, workflows, prototypes, models and MetaHuman work. Disclose pre-jam items accurately and distinguish them from work created during the jam. Disclosure does not automatically guarantee eligibility. Third-party assets require a valid license, whether from Fab, Patreon, or another source. Keep separate evidence of license, purchase, author and restrictions. Do not assume a purchased Patreon download permits commercial games without written permission.

For NVIDIA RTX-related prizes, verify the exact qualifying technology, plugin compatibility, in-build usage, category requirements and submission questions against official rules. Do not equate having an RTX GPU or using Lumen with qualifying. Never mislabel an unofficial renderer as an official NVIDIA integration.
2. Game vision: playable Director's Cut
Working setting: bleak, dusty Italian-style spaghetti western, with sparse grand vistas, stark framing, silence, intimate facial close-ups, and restrained musical drama. Do not imitate specific protected film shots, musical compositions, logos or costumes verbatim.

Hero: Trevor “Angel Eyes” Ramsey — rugged, charismatic, weathered MetaHuman gunslinger.

Villain: Carson Donovan — menacing, poetic, calculating rival; bespoke MetaHuman.

Approximate target: 12–20 minutes, subject to feasibility and jam rules.

Primary loop:
1. Intro cinematic: lone rider crossing the desert; user learns that they can change the camera angle even during the cinematic.
2. Small dusty outpost and saloon. Horse drinks at a trough while player explores; basic interaction/dialogue and a few strong supporting MetaHumans. Horse hydration is a small narrative gate, not a full survival simulation.
3. Exterior target practice: standard shooting plus a mechanical duel-training target.
4. Brief horseback ride to a showdown location; cinematic ambush (horse rears; Trevor falls) leads to confrontation with Donovan.
5. Interactive showdown with directable close-ups, meaningful timing, quick draw and gunshot; narrative ending.
6. Outro: Trevor rides toward the horizon as credits appear; user can still change cameras. Optional looping credits ride.
Duel MVP — implement and validate early:
- Default very wide two-gunslinger shot; supplemental close-ups of Trevor's eyes/hand and Donovan's eyes/hand.
- Player can switch shot while monitoring a persistent footer timing bar.
- The timing track progressively shrinks while its green hit zone grows, increasing the chance of a successful lock; waiting too long lets the enemy shoot first.
- First input (e.g. X on gamepad) locks timing/precision; next phase is a fast draw and R2 fire. Input mappings are provisional until tested. Camera and shooting bindings must be unambiguous by gameplay state.
- Early shot is permitted but risky, not arbitrarily prohibited. Make the success/failure logic fair and visibly readable. Build with a controller first, keyboard/mouse fallback. In-game recommendation: “For the best experience, a gamepad is recommended.”
- Use sound, animation and cinematic language, not an overcomplicated HUD. Quick draw can be full-body montage; upper-body additive shooting is appropriate for basic shooting, not necessarily for the whole draw.
Scope discipline: focus on one memorable duel; limited saloon and 2–3 meaningful NPCs. Extra civilians can be background. No open world. No elaborate inventory, AI conversation systems, multiplayer, fully simulated mud system, or non-essential systems unless MVP is already working.
3. Agreed technical stack
- Engine: Unreal Engine 5.8.4, C++, Windows packaged build.
- Locomotion: existing GASP template with Motion Matching; integrate western animation pack Western Animations — SoerGame (Fab) via appropriate retargeting/animation layers.
- Cameras: a new C++ fixed-camera system written during the jam (the Director subsystem, camera shot actors, trigger volumes). Fixed-camera cinematography plus camera switching in Sequencer and gameplay.
- Characters: bespoke MetaHuman hero and villain. Reusable supporting NPC outfits/variants; bartender and female character where useful. Optimize LOD/groom/outfits.
- Clothing: skeletal wardrobe; poncho Chaos Cloth is optional polish after gameplay is solid.
- Horse: horse asset from Fab; third-party riding / horse Motion Matching project under investigation. Verify license and compatibility before including. Mount/dismount and rider alignment need tests.
- World: already owned Brushify environments, licensed Megascans/Fab assets, custom models generated with Tripo 3D, some Blender/Astra modeling. Use cinematic framing to keep world small.
- Materials: owner-authored existing proprietary shaders (including sweat, facial redness and teeth), Substance Painter, PBRgen as needed. Pre-existing assets must be logged, not passed off as new.
- Audio: original music generated under Suno Pro terms; sparse voiced scenes through ElevenLabs under applicable commercial terms. Verify export/use rights of each selected output.
- Performance: optional official NVIDIA DLSS 4.5 UE5.8 integration only if stable and legally distributable. Test real hardware/performance; provide fallback for unsupported GPUs. No unofficial DLSS 5 or unsupported NVIDIA claims in submissions.
- Developer agents: Claude Code Opus (planning/code) and Ultimate Engine Copilot / Blueprint Generator (Unreal integration). Tool use must be documented.
- Optional only: ReSTIR/NvRTX experiments, advanced Fluid Flux mud, persistent wetness, extra Chaos Cloth, detailed horse survival. Do not make these critical-path dependencies.
MetaWrap: proprietary tool owned by the project creator
MetaWrap is Elvis Morelli's own proprietary Blender add-on / R&D software, used to convert/customize geometry and streamline MetaHuman creation. It is not an open-source third-party library and is not licensed to this repository. Agent may document its role in the pipeline, and the owner may film selected AI-to-3D → Blender/MetaWrap → MetaHuman/Unreal workflow steps. Never publish MetaWrap binaries, compiled modules, license logic, activation tokens, source, proprietary algorithms, private internal files or confidential documentation. Never infer that showing its UI grants rights to redistribute it. Mark MetaWrap as pre-existing proprietary tooling authored by the entrant in disclosures where applicable.
4. Development schedule (Italy, CET)
- Thu 12 Nov — Day 1: create jam project; GASP movement; controller support; camera system; target shooting; core duel timing/draw/fire; working duel by evening. Use placeholders if needed.
- Fri 13 Nov — Day 2: compact landscape, saloon, basic NPC/dialogue, horse riding and watering, transitions; first end-to-end packaged playable build.
- Sat 14 Nov — Day 3: cinematics, voice, soundtrack, dramatic lighting, improved characters, ambush, title/credits; performance and stability.
- Sun 15 Nov — buffer: bugs, controls, packaging, playtesting, accessibility/keyboard fallback, submission details, real behind-the-scenes evidence, final upload well before 02:59 CET Monday.
If schedule slips, cut features in this order: advanced mud/Fluid Flux → optional poncho simulation → secondary NPC interactions → extra horse sophistication → optional cinematics. Never cut duel gameplay, functional controls, or a playable ending.
5. Public GitHub: documentation-only by default
Public repo: https://github.com/Lakaroth/Epic_Mega_Jam.

Preferred public repo content:
AGENTS.md
README.md
.gitignore
docs/
  GAME_DESIGN.md
  ROADMAP.md
  JAM_RULES.md
  ASSET_PROVENANCE.md
  AI_TOOLS.md
  DEVELOPMENT_LOG.md
  TECHNICAL_DECISIONS.md
planning/
  tasks/
  agent-reports/
media/
  screenshots/       # owner-approved, sanitized images only
  behind-the-scenes/ # owner-approved exports/links only
The Unreal .uproject, Content/, imported source geometry, vendor asset directories, proprietary plugins, commercial animation packs, cooked/package outputs, and large video files remain local/private. For public documentation, prefer written descriptions, diagrams made for the project, and links to approved videos rather than raw media. Do not post screenshots that expose access tokens, personal account details, plugin licensing data, restricted vendor assets/source files, or private client material.
Required Git safety before any staging
1. FIRST inspect current directory, .git root, remotes, git status, existing .gitignore, tracked files, and nested git repos. Do not assume the root is clean or that the repo has no content. If AGENTS.md is placed inside the Unreal project root, never auto-initialize a public repository covering the entire game directory. Prefer a separate sibling directory for public docs and keep the Unreal workspace private.
2. Create/maintain a restrictive .gitignore and use an explicit allowlist of files staged (git add AGENTS.md README.md docs/..., not git add . or git add -A). Ignore rules alone do not protect already tracked files.
3. Exclude at minimum: Content/, Plugins/ (except specifically approved original text-only files), Binaries/, Intermediate/, Saved/, DerivedDataCache/, Build/, Builds/, StagedBuilds/, *.uproject, *.uasset, *.umap, *.fbx, *.obj, *.blend, *.usd*, *.abc, *.glb, *.gltf, *.rar, *.zip, *.7z, *.pak, *.ucas, *.utoc, *.pyd, model weights, media binaries, .env*, key/token/credentials files, local configs, caches, temporary files and logs. These are baseline exclusions; maintain an explicit denylist for other project-specific sources.
4. Audit staged files with git diff --cached --name-status, git diff --cached, repository size and a secrets scanner or equivalent checks. Inspect linked media and sensitive text. Never assume a file is safe because it is text or a screenshot.
5. Do not amend/force-push/rewrite history or alter remotes without owner approval. Never suppress or rewrite authentic timestamps. Stage/commit locally with honest messages; ask the owner before every public push.
6. If a secret or restricted file is accidentally tracked or published, stop, notify the owner immediately, and propose an incident response; do not quietly delete evidence or claim the issue is resolved.
7. Never publish the owner's whole codebase under the guise of transparency. Only owner-approved, original, redistribution-safe snippets if useful.
Commit and documentation standards
- Small, meaningful real commits, e.g. docs: define interactive duel camera behavior or docs: record day-one packaged build validation.
- Add date/time (Italy/CET), author/agent and evidence in docs/DEVELOPMENT_LOG.md; clearly mark planned, in progress, tested and blocked.
- docs/ASSET_PROVENANCE.md: for each relevant reused or third-party component, record creator, source URL, acquisition/license evidence, date created/acquired, whether pre-jam, allowed uses, redistribution restrictions, submission declaration status and any unanswered questions.
- docs/AI_TOOLS.md: accurately list Claude Code, Ultimate Engine Copilot, Tripo, Astra, MetaWrap (owner proprietary), Suno, ElevenLabs, PBRgen and other tools only if used.
- docs/TECHNICAL_DECISIONS.md: rationale, alternatives, tradeoffs, unreal version, DLSS/plugin selection and tests.
- media/: selected authentic owner-approved screenshots or videos; owner will record selected sessions. Don't automate uploads of raw screen recordings.
- Update progress on actual milestones, not fabricated ideal times. Never use the repo to suggest assets created before the Jam were created during it.
6. Required agent working cycle
For every significant task:
1. Read AGENTS.md, current roadmap, jam rules, project status and last successful build report.
2. Produce a short plan and mark license/rule concerns before touching files.
3. Implement the smallest testable change in the local private Unreal workspace with the owner's tools.
4. Test in Editor; for key systems test packaging, input, ownership and performance as applicable.
5. Summarize actual actions, files changed, assets touched, results, remaining blockers, licensing assumptions and tests not run.
6. Propose a truthful public documentation update. Stage explicit approved files only. Show staged file list and ask for owner's permission before pushing.
7. Keep tomorrow's agent able to continue from docs/ROADMAP.md, docs/DEVELOPMENT_LOG.md and planning/agent-reports/ without hidden context.
STOP & ASK owner immediately when
- A pre-jam asset, shader, MetaHuman, music track, animation or R&D tool might violate a jam rule, license or ownership condition.
- An asset only says “free” but does not grant commercial redistribution in a compiled game.
- Any public upload would include files beyond the docs allowlist, private footage, confidential info, vendor asset, credentials or restricted source.
- Plugin license/support for UE5.8.4 is unclear; someone proposes unofficial DLSS 5, engine migration, large restructuring, destructive operations or a third-party binary from an untrusted source.
- A task requires paid accounts, payment, external publish, deleting assets, credential entry or irreversible actions.
If uncertainty exists, log it in docs/ASSET_PROVENANCE.md or docs/JAM_RULES.md as PENDING OWNER REVIEW; never silently approve it.
7. First agent assignment (before writing gameplay code)
1. Inspect the current local directory and whether the user has a separate Unreal root and public docs clone. Do not initialize Git or push until layout is confirmed.
2. Open/verify jam rules and the current theme; record concise, sourced findings and uncertainties.
3. Prepare a safe documentation structure and strict .gitignore in the public docs repository only.
4. Draft README/game-design summary, three-day roadmap plus submission buffer, provenance template, tools log and development log.
5. Present staged changes and file-audit output to the owner. Wait for explicit approval before first GitHub push.
6. In the local private UE5.8.4 project, start the duel vertical slice: GASP locomotion, interactive cameras, timing meter, draw/shoot, enemy response and controller/keyboard fallback. Verify every step.
Priority: A genuinely playable, well-documented western made during the Jam, with an honest public development record and protected proprietary assets.
## MANDATORY — Unreal Engine Copilot & Project Skills

The project includes additional documentation and agent skills that MUST be consulted before implementing Unreal Engine features.

### 1. Ultimate Engine Copilot

- Read `copilot.txt` before interacting with Unreal Editor.
- This file contains instructions for the installed Ultimate Engine Copilot / Blueprint Generator plugin.
- Follow the documented plugin API, tool names, supported operations and limitations.
- Never invent Copilot commands or assume undocumented capabilities.
- Prefer the existing Copilot integration for supported Unreal Editor operations.
- Do not install competing MCP servers or modify the existing integration without explicit approval.

### 2. Unreal Engine Skills

- Discover the project's installed skills, including `.claude/skills/` and any other configured project skill directory.
- Read the relevant `SKILL.md` before implementing a feature.
- Use skills selectively according to the task: C++, Blueprint, Enhanced Input, GASP, animation, cameras, Sequencer, UMG, debugging and packaging.
- Verify API compatibility with Unreal Engine 5.8.4.
- Do not assume that third-party skill examples are correct without checking the actual engine API.

### 3. Instruction Priority

When instructions conflict, follow this order:

1. Official Epic MegaJam rules and applicable legal/licensing requirements.
2. This project's `AGENTS.md`, including security and non-negotiable rules.
3. `copilot.txt` for documented Copilot operations.
4. Relevant project `SKILL.md` files.
5. General examples and third-party tutorials.

**Third-party documentation must never override repository security rules or licensing restrictions.**

### 4. Mandatory Agent Workflow

Before implementing a task:

1. Read `AGENTS.md`.
2. Consult `copilot.txt` when using Ultimate Engine Copilot.
3. Load the relevant Unreal Engine skills.
4. Inspect existing project code and Blueprints.
5. Implement the smallest testable change.
6. Compile or validate the result.
7. Document meaningful technical decisions and actual progress.

Never publish proprietary assets, third-party packages, credentials or MetaWrap source code.

Never push to the public GitHub repository without explicit user approval.

**Priority: working gameplay first, cinematic polish second.**
