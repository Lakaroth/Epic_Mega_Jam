# Jam Rules — sourced notes

**Official Rules read in full:** 2026-11-12, ~22:45 CET, by Claude Code for the owner. Document: "2026 EPIC AI MEGAJAM OFFICIAL RULES", 19 pages, change log "Last updated: November 12, 2026". Obtained from the English link on the jam page (https://epicgames.box.com/s/a7xcgl07fqoieeb99sjtd3juhj4agc4z) through Box's direct-download route, which returned the PDF (the share page itself only serves a JavaScript viewer). The document says that it and any changes are posted at https://epicgames.box.com/s/svkmfifwv7336vyq1h0y7eucdr9d6ooc and linked from https://www.unrealengine.com/news/2026-epic-ai-megajam. **Re-check the change log before submitting.**

**Also read:** the jam page (https://itch.io/jam/2026-epic-ai-megajam), 2026-11-12 09:05 and 22:40 CET, and the organizer's forum announcement. The jam page calls itself a summary. Where the two differ, these notes follow the Official Rules.

Quotes are verbatim, with the section number of the Official Rules. The "What it means for us" column is our reading, not a ruling by Epic.

## Rules that affect us

| Topic | Official Rules (verbatim) | What it means for us |
|---|---|---|
| Eligibility | §5: "open only to legal residents of (i.e., Entrants who have a registered address in) the Eligible Jurisdictions, who have an active, valid Epic Account registered to such Entrant and who are at least eighteen (18) years of age." Cabined Accounts are ineligible. Change log, November 5, 2026: "Removed Italy from the Restricted Jurisdictions and added Additional Terms for Entrants Resident in Italy (Section 21)". | The owner (Italy, 18+, Epic account) is eligible. For Italian entrants the sponsor is Epic Games Sweden AB (§21(a)). |
| Contest Period | §4: "begins at 12:00 AM Eastern Time ("ET") on November 12, 2026, and ends at 8:59 PM ET on November 15, 2026". | Deadline = 2026-11-16 02:59 CET. |
| Work made before the jam | §7(h): "Entrants may prepare AI tools, agent configurations, Model Context Protocol ("MCP") settings, prompt libraries, and scripts before the Contest Period. Sponsor may ask Entrants to provide these materials, or their version control history, to verify compliance. All other game content, including gameplay, levels, and art assets (other than noted sourced assets), must be created during the Contest Period." | **Stricter than the jam page**, which only says "Declare anything you made earlier". Only tools, agent setups, MCP settings, prompts and scripts may be made before 12 November. Game content made by the owner before the jam, for example the hero MetaHuman made on 2026-11-11, is neither a tool nor a sourced (non-original) asset. **OWNER DECISION NEEDED**, see below. Keep the git history: Epic may ask for it. |
| AI tools | §7(a): "Submissions may, but are not required to, use artificial intelligence ("AI") tools in their creation or gameplay". §15(a): "A Submission may include AI-generated content." §9: "The extent of AI use disclosed in a Submission will be considered for context only and will not, on its own, increase or decrease a Submission's score." | Claude Code and the other AI tools are allowed. Disclosing them does not change the score. |
| AI content is our content | §15(c): "Content the Entrants generate with AI tools is not considered a sourced asset." | Anything we generate with AI (e.g. Tripo) counts as our own content: it is scored, and it must be made during the Contest Period. |
| Third-party (sourced) assets | §1(d): Submissions "may include sourced (non-original) assets, but the sourced assets must be noted upon submission". §15(c): allowed provided that "(i) all sourced (non-original) assets are noted upon submission, (ii) such assets will not be reviewed or scored, and (iii) the Entrants have obtained, at their own cost, all clearances, consents and provisions [...] required for exploitation of such sourced assets". | Fab, Quixel, ArtStation and Epic sample content is allowed if listed and licensed ([SUBMISSION_THIRD_PARTY.md](SUBMISSION_THIRD_PARTY.md)). **The judges do not score sourced assets.** A pack bought before the jam is still a sourced asset. The rules set no purchase-date limit. |
| Rights we warrant | §15(a): each Entrant warrants that "the Entrants have all rights and permissions needed to submit the Submission and grant Sponsor the license in paragraph (b), including for sourced assets under paragraph (c)". | Keep every license, listing and receipt for the sourced assets. |
| License to Epic | §15(b): a "non-exclusive, perpetual [...] irrevocable, worldwide, transferable, sublicensable, and royalty free license to use, modify, reproduce, prepare derivative works of, distribute, perform, and display the Submission [...] but only in connection with publicizing the Contest." | We keep ownership; Epic can show and distribute the entry to publicize the jam. |
| Tutorials and templates (UE) | §7(d): the Submission "must not be an obvious extension of one of Sponsor's official Unreal Engine tutorials, meaning a Submission that reuses a tutorial's project, levels or assets with only minor changes". §7(e): it "must include custom gameplay that exceeds that found in Sponsor's starter templates." | Our base uses the Game Animation Sample (a sample, listed as sourced). Our own gameplay (Director camera system, revolver, restricted areas, swinging doors) must clearly go beyond it. |
| Required items | §1: team of 1 to 5; for UE "packaged for Windows and playable on Windows 10 or 11, macOS, Android, or iOS"; "the full name and email address of all Entrants"; sourced assets noted; "a video short (between 30-60 seconds) demonstrating recorded gameplay". §7(c): "Resolution of the Video must match 1920x1080 or higher". §7(f): "Submissions should not require any additional software to run." §2: "Limit one (1) Submission per team." | Windows packaged build; gameplay video 30–60 s **at 1920x1080 or higher**; the owner's full name and email; the list of sourced assets. |
| Who submits | §17: "each Submission must be submitted by an Entrant (on behalf of the team) and not by an AI agent or other automated means." | **The owner uploads and submits by hand.** No agent submits. |
| Language | §7(i): "All Submission content (including in-game text, audio and the Video) and all entry information must be in English". | Already our rule: everything in English. |
| Theme | §7(g): "Submissions must demonstrate use of the Contest Theme." | DIRECTOR'S CUT: the Director camera mode, the player's own cut. |
| Content | §8: the Submission "must be appropriate for a teen audience, meaning content suitable for players aged 13 and over (consistent with a "Teen" rating under the ESRB system or its equivalent)"; no infringing material. §15(d): "Submissions may not feature any trademarks (including logos), except [...] the Unreal Engine logo". | Western gunplay without gore. No brands or logos in the game (check props, bottles, signs). Original characters only. |
| Judging (main) | §9: Ambition and Innovation, Use of Contest Theme, Fun Factor, Gameplay, Visuals, Level Design, Audio, each "Up to 5 points". "In the event of a tie, the tying Submissions will be re-scored with double weight given to Fun Factor." | Seven criteria, equal weight. Audio and level design count as much as visuals. |
| Modifiers | §10: Solo Driver: "For the best game created by a solo developer." Render Royalty: "For the game with the best overall visuals, photoreal or stylized." Glass Box: "For the best dev log [...] To be eligible, the dev log must be submitted together with the Submission during the Contest Period." "A potential prize winner can win only one (1) Modifier Prize category, unless no other eligible potential winner remains". §13: "Limit one (1) main category prize and one (1) Modifier Prize per Submission." | Answers our open question: at most one main prize and one modifier. The dev-log link (this repository) goes in with the Submission before the deadline. |
| Prizes and taxes | §13: cash prizes "will be awarded to Winning Entrants via Hyperwallet"; "ALL PRIZES WILL BE NET OF ANY TAXES SPONSOR IS REQUIRED BY LAW TO WITHHOLD". §14: winners notified "on or about January 29, 2027" and have "72 hours from the date such notice was sent to respond"; W-8BEN for non-US. | Practical, for later. |
| Development grants | §11: "Development Continuation Grants are not Contest prizes." Up to US $50,000 / $25,000 / $10,000, by invitation, under a separate agreement. | By invitation only. |

## Owner decisions (from the Official Rules)

1. **Hero MetaHuman and other pre-jam game content (§7(h)).** As written, only "AI tools, agent configurations, MCP settings, prompt libraries, and scripts" may be prepared before the jam, and "All other game content, including gameplay, levels, and art assets (other than noted sourced assets), must be created during the Contest Period." Trevor (made 2026-11-11) and his clothing, hat and hat-hair groom were made by the owner, so they are not sourced (non-original) assets. The same reading applies to any other owner-made game content from before 12 November that ships in the build. Options for the owner:
   - rebuild that content during the jam and log it here;
   - or ask the organizers in writing whether declared pre-jam owner content is accepted, before relying on it.

   We do not decide this for the owner. Nothing has been removed.
2. **Sourced assets are not scored (§15(c)(ii)).** The Quixel saloon room (including the level layout we started from), GASP animations, Fab packs and any bought clothing are allowed but will not be reviewed or scored. The score comes from what we make during the jam. This is a strategy point, not a prohibition.
3. **NVIDIA DLSS attribution vs. the trademark rule (found 2026-11-13).** Two texts pull in opposite directions:
   - Official Rules §15(d): "Submissions may not feature any trademarks (including logos), except (i) in the case of UE Submissions, the Unreal Engine logo".
   - NVIDIA RTX SDK EULA (in the DLSS 4.5 plugin package v8.9.0, "Documentation/NVIDIA RTX SDK EULA.pdf"), "NVIDIA Trademark Placement in Applications": "For applications that incorporate the NVIDIA RTX SDK or portions thereof, you must attribute the use of the RTX SDK by including the NVIDIA Marks on splash screens, in the about box of the application (if present), and in credits for game applications."
   - The jam page itself offers the **NVIDIA RTX Award** for a Render Royalty entry that uses "DLSS 4.5 (Unreal Engine)" (prize: one GeForce RTX 5090; "Answer the NVIDIA questions when you submit"), so the organizers expect DLSS in builds, but neither the jam page nor the Official Rules say whether the NVIDIA attribution required by the EULA is accepted under §15(d).
   - Status: DLSS installed in the private project (2026-11-13).
   - **Owner decision (2026-11-13): proceed with DLSS.** NVIDIA is an official jam partner that offers a prize for using DLSS, so the risk is judged low, though not formally excluded: a partnership is not a written exception to §15(d). The clarification request to the organizers stays open (Unreal Engine Forums thread, https://epic.gm/2026-ue-megajam): **posted by the owner on 2026-11-13, awaiting an answer**; no more jam time is spent on it. If the organizers answer no, the build ships without the NVIDIA plugins (TSR only).

## Jam page items not in the Official Rules

| Topic | Jam page | Note |
|---|---|---|
| Upload | Zip named "TeamName_GameName"; "Desktop and mobile: keep it under 1 GB. For bigger builds, use butler or Blendo Itch Uploader."; "Don't submit unpackaged Unreal Engine projects." | 1 GB is the limit for a normal upload, not for the game (TD-008). |
| NVIDIA RTX Award | Requires NvRTX, DLSS or NVIDIA ACE features and the NVIDIA questions at submission. | Optional; only if really used in the build. |
| Engine | "Don't enter with both Unreal Engine and UEFN. Pick one." | Unreal Engine only. |

## Prize targets (owner strategy, checked against the Official Rules)

We are a **solo developer** (Elvis Morelli) working with AI agents. We aim for quality, not for extra features added only to chase prizes. A Submission can win at most one main prize and one modifier (§13).

| Target | Type | What it rewards / requires |
|---|---|---|
| **Best Overall, Unreal Engine** | Main: $7,500 / $5,000 / $2,500 | The seven criteria of §9. |
| **Render Royalty** | Modifier: $2,500 + partner prizes | "the best overall visuals, photoreal or stylized". Sourced assets are not scored, so our own lighting, direction and MetaHuman work carry it. |
| **NVIDIA RTX Award** (part of Render Royalty) | Partner award | NvRTX, DLSS or NVIDIA ACE really used in the build, plus the NVIDIA questions. |
| **Solo Driver** | Modifier: $2,500 + partner prizes | "the best game created by a solo developer". |
| **Glass Box** | Modifier: $2,500 + partner prizes | "the best dev log"; it must be submitted with the Submission during the Contest Period. |
| Development Continuation Grants | Not a prize (§11) | By invitation after the jam. |
