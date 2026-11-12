# Jam Rules — sourced notes

**Accessed:** 2026-11-12, ~09:05 CET, by Claude Code for the owner.
**Sources read:** the jam page (https://itch.io/jam/2026-epic-ai-megajam) and the organizer's forum announcement (https://forums.unrealengine.com/t/vibe-your-way-to-50k-the-2026-epic-ai-megajam-is-coming/2843973).
**Not read yet:** the full **Official Rules** document linked from the jam page (https://epicgames.box.com/s/a7xcgl07fqoieeb99sjtd3juhj4agc4z, which redirects to epicgames.ent.box.com). Box serves it through a JavaScript viewer: two automated attempts (09:05 and 17:40 CET) received only an empty page, so no clause has been read. The jam page itself says it is a summary and that the Official Rules must be read before entering. **PENDING OWNER REVIEW — highest priority:** the owner reads the Official Rules in a browser and confirms or corrects the points below, in particular whether pre-jam work that is declared (the hero MetaHuman, the owner's proprietary tools and shaders) is allowed and judged.

Quotes are verbatim from the jam page unless noted. The "What it means for us" column is our interpretation, not a ruling by Epic.

| Topic | What the page says | What it means for us |
|---|---|---|
| Theme | Announced at the kickoff livestream. | **DIRECTOR'S CUT**, confirmed to the owner by organizer email. |
| Dates | "November 12–15, 2026". Upload "before November 15, 5:59 PM PST / 8:59 PM EST." "Late submissions will be disqualified." | Deadline = **2026-11-16 02:59 CET**. Target the final upload well before it. |
| AI tools | "Use any AI tools you like: coding agents, asset generation, audio, writing, anything." "There's no limit on agents." | Claude Code and the Copilot plugin are allowed. We still list them (see [AI_TOOLS.md](AI_TOOLS.md)). |
| Pre-jam work | "Don't start building your game before November 12. Declare anything you made earlier." FAQ: set up tools, agents and MCP ahead of time is fine; "Declare any prompts, scripts, or assets you made before the jam." | The game project was created on 2026-11-12 at 07:53 CET. Everything made before the jam is declared in [ASSET_PROVENANCE.md](ASSET_PROVENANCE.md) ("Pre-jam items to declare"). |
| Third-party assets | "Use assets you didn't make, such as from Fab, as long as you have the right license. List them in your submission." | Every Fab and Epic asset is listed with its source, license status and the time it was added. |
| Submission | Packaged build (Windows 10/11 among the options); "Don't submit unpackaged Unreal Engine projects."; .zip named "TeamName_GameName"; "Desktop and mobile: keep it under 1 GB. For bigger builds, use butler or Blendo Itch Uploader."; "Upload it to your own itch.io account, then submit to this jam."; gameplay video link (30–60 s); optional dev log link; optional "Tools you used". | 1 GB is the limit for a normal upload, **not a limit on the game**: a bigger build is uploaded with butler (itch.io's uploader). The page sets no maximum for butler uploads. We do not cut quality (MetaHumans, textures) to fit 1 GB; see TECHNICAL_DECISIONS TD-008. We need a Windows packaged build and a short gameplay video. |
| Dev log | "Dev log link (optional, but required for the Glass Box modifier)". Glass Box = "Best dev log showing how you built your game". | This repository is our dev log. Keep it truthful and timestamped. |
| Solo | "Solo Driver": "Best game built by a solo developer". | The owner is a solo developer. |
| NVIDIA prize | Requires at least one feature from NvRTX, DLSS 4.5 (Unreal Engine) or NVIDIA ACE, plus answering the NVIDIA questions. "Eligibility restrictions apply." | Optional. Only claim it if an official integration is really used in the build. |
| Engine choice | "Don't enter with both Unreal Engine and UEFN. Pick one." | Unreal Engine only. |
| Content | "No content that breaks the Official Rules, including other people's IP and inappropriate content." | Original western characters only. Do not copy film shots, music, logos or costumes. |
| Eligibility | 18+ with an active Epic Games account. Organizer staff stated on the forum that entrants from Italy are eligible if they meet the other requirements. | Confirm in the Official Rules (Section 5). |

## Open questions (PENDING OWNER REVIEW)
- Read the Official Rules: platform requirement, accepted engine version for desktop builds, where declarations go, and the disqualification list.
- In the Official Rules, check what they say about work made before the jam. Declaring a pre-existing asset does not by itself make it allowed or judged. This matters for the hero MetaHuman (made 2026-11-11) and for the owner's proprietary tools and shaders.
- Where in the submission form do pre-jam declarations and the asset list go? This is not stated on the page.

## Prize targets (owner strategy, checked against the jam page)

We are a **solo developer** (Elvis Morelli) working with AI agents. We aim for quality, not for extra features added only to chase prizes.

| Target | Type on the jam page | What it rewards / requires |
|---|---|---|
| **Best Overall, Unreal Engine** | Main category: $7,500 / $5,000 / $2,500 | The best game overall. |
| **Render Royalty** | Modifier: $2,500 + partner prizes | "Best visuals, photoreal or stylized". Our focus: MetaHuman close-ups, lighting, interactive direction. |
| **NVIDIA RTX Award** (part of Render Royalty) | Partner award: one GeForce RTX 5090 | Must really use NvRTX, **DLSS 4.5 (Unreal Engine)** or NVIDIA ACE in the build, and answer the NVIDIA questions at submission. Optional; only if an official integration is stable. |
| **Solo Driver** | Modifier: $2,500 + partner prizes | "Best game built by a solo developer". |
| **Glass Box** | Modifier: $2,500 + AMD prize | "Best dev log showing how you built your game". This repository is our dev log. |
| Development Continuation Grants | Separate: up to $50,000 / $25,000 / $10,000 | For "standout" entries. The page does not say how they are chosen. |

**Corrections to our earlier assumptions:**
- Render Royalty is a **modifier** category, not a main category.
- The jam page does **not** state a limit such as "one main category and one modifier per submission". It may be in the Official Rules: **PENDING OWNER REVIEW**. We do not assume prizes can or cannot be combined.
