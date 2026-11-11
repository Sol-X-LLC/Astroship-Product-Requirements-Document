# Astroship
An iPhone Duo multiplayer grid-based battle game for friends, family, and enemies. 
<br><br>


<img width="1024" height="1024" alt="astroship-app-icon" src="https://github.com/user-attachments/assets/b84363ac-5d18-49e3-89e1-95950c1d05e9" />

## Product Requirement Document Table of Contents:
### 1	[Document Purpose](#sec-1-document-purpose)
### 1.1	[Requirement Identifiers](#sec-1-1-requirement-identifiers)
### 2	[Introduction](#sec-2-introduction)
### 2.1	[Hardware Block Diagram](#sec-2-1-hardware-block-diagram)
### 2.2	[Principle Functionality Explained](#sec-2-2-principle-functionality)
### 3	[Functional Requirements](#sec-3-functional-requirements)
### 3.1	[Electrical Requirements (ELEC-###)](#sec-3-1-electrical)
### 3.2	[Mechanical Requirements (MECH-###)](#sec-3-2-mechanical)
### 3.3	[Software Requirements (SOFT-###)](#sec-3-3-software)
### 3.4	[Interface Requirements (INTE-###)](#sec-3-4-interface)
### 4	[Non-Functional Requirements](#sec-4-non-functional)
### 4.1	[System Attributes Requirements (SYSA-###)](#sec-4-1-system-attributes)
### 4.2	[Project Management Requirements (PROJ-###)](#sec-4-2-project-management)
### 4.3	[Regulatory / Approbation Requirements (REGU-###)](#sec-4-3-regulatory)
### 4.4	[Certifications Requirements (CERT-###)](#sec-4-4-certifications)
### 5	[Reference & Support Documents](#sec-5-reference-documents)
<br><br>


## Revision History

Table 0 – Document version history <br>
|Version |Date       |Author(s)     |Notes                                                                              |
|--------|-----------|--------------|-----------------------------------------------------------------------------------|
|A	     |2026-10-13 |Blaze Sanders |Initial document with skeleton based on Table of Contents                          |
|B       |2026-10-30 |Blaze Sanders |First public open source version with new Sol-X assets and Swift code              |
|C       |2026-11-08 |Meta Muse     |Added SOFT-006 to SOFT-025 on AI-Requirements branch merged to main by Blaze S     |
|D       |2026-11-09 |Blaze Sanders |Rewrote ELEC Requirements branch & added hyperlinks to Table of Contents entries   |
|E       |2026-11-11 |Blaze Sanders |Rewrote INTE-001 and INTE-002 to be testable and added INTE-003–INTE-012 on the AI-Interface-Requirements branch |

<br><br>  


## Abbreviations & Terminology

Table 1 – Local document acronyms and initialisms <br>
|Term	   |Definition                                                                                                    |
|--------|--------------------------------------------------------------------------------------------------------------|
|SKU     | Stock Keeping Unit, See https://en.wikipedia.org/wiki/Stock_keeping_unit                                     |

<br><br>


<a id="sec-1-document-purpose" name="sec-1-document-purpose"></a>
### 1	Document Purpose 
This document defines both the business and engineering requirements for Astroship, a multiplayer grid-based battle game.

<a id="sec-1-1-requirement-identifiers" name="sec-1-1-requirement-identifiers"></a>
#### 1.1	Requirement Identifier 
Each requirement has a unique identifier according to the following structure: Domain-<Number>[Tag]{Author} (e.g. SYSA-001[QC]{Blaze S} = System Attribute #1 regarding Quality Control authored by Blaze Sanders). 

Where Domain will be one of the following: CERT (certification), ELEC (electrical), MECH (mechanical), INTE (external interface), PROJ (project management), REGU (regulatory), SOFT (software), SYSA (system attribute). <br>

Where Tag may be one of the following short (< 10 characters preferred) tags to make database searching and filtering easier: Power, Interface, Strength, Bandwidth, Quantity, Cost, Location, Schedule, UX (User Experience), UI (User Interface), Color, Material, Sourcing, Safety, Security, API (Application Programing Interface), Testing, Logs, QC (Quality Control), QA (Quality Assurance), OS (Operating System), OTA (Over The Air updates), Process, Performance, ADD_NEW_TAGS_HERE. <br>

Where Author is a first name and first letter of the last name of the human that wrote the requirement. This wil not be used to blame the author, but instead be used to ask the author what their thinking and base assumptions where when writing the requirment. [SOURCE](https://www.goodreads.com/quotes/11819361-1-question-every-requirement-each-should-come-with-the-name)

All units shall be metric International System of Units (SI), with imperial units added only for convenience for weight. If a numerical value is not labeled, assume SI units are being used. <br>

In expressing requirements, the following terminology will be used:
* shall means “is required to” and thus used to define exact must have requirements
* will means “it is true that” and thus used in statements of fact
* may means “is permitted to” and thus is used to allow flexibility to save time or money
* note is used for informational context and is not required to implement the specification 
<br><br>


<a id="sec-2-introduction" name="sec-2-introduction"></a>
### 2	Introduction
Source code for all Apple OS can be found at https://github.com/Sol-X-LLC/Astroship-Apple-Apps 
Any source code in this repo is only for small scale testing and as example documentation.

Kickstarter Price: $4.00 per iPhone with local multiplayer (no online feature)
Release Price: $0 with $4.69 upgrade to Astroship Pro for online multiplayer via a two week trial
Jan 2028 Price: $8 per year 

TestFlight Beta: Coming Dec 12, 2026
* v2026.0: Minimally Viable Product with basis graphic, audio, and local single player game play loop.
* v2026.1: Online play enabled with Game Center integration and accessibility features 

Kickstarter Campaign: Coming Jan 12, 2027
* ATP.fm podcast ad running Jan 14, 2027
* Release daily post on Kickstarter for 30 days using prewritten blog
* Release business model poll Jan 29 to get feedback on $8/year subscription 
  
App Store Public Release: Coming April 14, 2026
* v2027.X: TODO
<br><br>


<a id="sec-2-1-hardware-block-diagram" name="sec-2-1-hardware-block-diagram"></a>
### 2.1	Hardware Block Diagram
TODO
<br><br>


<a id="sec-2-2-principle-functionality" name="sec-2-2-principle-functionality"></a>
### 2.2	Principle Functionality Explained
TODO
<br><br>


<a id="sec-3-functional-requirements" name="sec-3-functional-requirements"></a>
### 3	Functional Requirements
Functional requirements define observable and measurable behavior expected from the Engineering Development Rack. Every functional requirement should be objectively testable and include a method of validation, acceptance criteria, and traceability to supporting test documentation when applicable. Whenever possible, requirements shall be written to support automated verification and long-term regression testing.

<a id="sec-3-1-electrical" name="sec-3-1-electrical"></a>
### 3.1	Electrical Requirements (ELEC-###)
ELEC-001[Power]{Blaze S}: Astroship shall draw less than 5 Watts (W) total device power during solo off line play and less than 7 Watts (W) during local or online multiplayer play, measured on an iPhone target (MECH-001) at 50% display brightness using Xcode Instruments Energy Log. The 5 W and 7 W limits are initial estimates from published third-party measurements of heavier 3D games on iPhone 15-17 Pro Max (4-6 W) and shall be confirmed or corrected by the measurement in ELEC-002 before the v2026.0 TestFlight.

ELEC-002[Testing]{Blaze S}: The power limits in ELEC-001 shall be measured on each iPhone target device (MECH-001) using Xcode Instruments Energy Log over a full 30-minute match, before the v2026.0 TestFlight on Dec 12, 2026. If a measured value differs from the ELEC-001 estimate, the measured value shall replace it.

ELEC-003[Power]{Blaze S}: Astroship v2026.0 shall not hold the cellular or Wi-Fi radio active during local solo play. The radio shall only be used for online play (SOFT-003, 0.5 Mbps) and Game Center sign-in (SYSA-004).

ELEC-004[Power]{Blaze S}: Astroship v2026.0 on iPhone Duo shall drive both displays only during active gameplay (fleet pane and hunt pane). Menus, the lobby, and settings shall use a single display to reduce power draw.

ELEC-005[Power]{Blaze S}: Astroship v2026.0 starry backgrounds and UI shall use predominantly dark pixels to reduce OLED display power on iPhone targets (MECH-001).

ELEC-006[Performance]{Blaze S}: Astroship v2026.0 shall keep sustained processor and graphics load within the thermal envelope of the target devices (MECH-001), so a full match completes without forced performance reduction or thermal shutdown.

ELEC-007[UX]{Blaze S}: Astroship v2026.1 shall remain fully playable by finger touch when the Apple Pencil (USB-C) is not connected or its battery is depleted, and shall not require the Pencil to be charging during play.

ELEC-008[Power]{Blaze S}: Astroship v2026.0 on mains-powered targets (4K Apple TV, Mac running macOS 27 or higher) shall run on mains power and shall not require battery-backed operation; no battery power budget applies to those targets.

ELEC-009[Power]{Blaze S}: Astroship v2028.0 backend power is the hosting provider's responsibility: the SYSA-005 backend shall run on a 32 GB RAM Linux Virtual Private Server (VPS), so Astroship shall specify only the virtual machine and no physical rack hardware (no quantities, make, model, or serial number).

ELEC-010[UX]{Blaze S}: Astroship v2026.0 shall respect the device's system power management: it shall not prevent auto-lock or Low Power Mode, and a match in progress shall be preserved when the device locks or the app backgrounds so it can resume after charging.

ELEC-011[Power]{Blaze S}: Astroship v2026.0 shall support play while the device charges over USB-C and shall not require a charger wattage beyond the device's own USB-C charging specification.

<a id="sec-3-2-mechanical" name="sec-3-2-mechanical"></a>
### 3.2	Mechanical Requirements (MECH-###)
MECH-001[Performance]{Blaze S}: Astroship v2026.0 (or higher) shall be optimized run on any iPhone Duo, any 4K Apple TV, any Mac running MacOS 27 (or higher) or any iPhone (6.3 inches or larger).

MECH-002[UX]{Blaze S}: Astroship v2026.1 (or higher) may support [Apple Pencil (USB-C)](https://www.apple.com/xc/product/MUWA3AM/A).

MECH-003[Color]{Blaze S}: Sol-X LLC shall sell a custom vinyl wrapper for the [Apple Pencil (USB-C)](https://www.apple.com/xc/product/MUWA3AM/A) at www.astroship.store starting Dec 2026 from [Decal Girl website](https://www.decalgirl.com/products/custom-apple-pencil-skin?variant=51649275953523&country=US&currency=USD&gad_campaignid=23527328328&gbraid=0AAAAAD_rqzbW1dad77YBtB_bFoUCcg4tq)
<br><br>


<a id="sec-3-3-software" name="sec-3-3-software"></a>
### 3.3	Software Requirements (SOFT-###)
SOFT-001[Process]{Blaze S}: All Astroship Swift code shall be open source forever and accept pull requests until at least v2027.0 as developer social outreach tool.

SOFT-002[UX]{TODO}: Astroship v2026.0 shall have a single player local game mode with a very basic AI opponent.

SOFT-003[UX]{Blaze S}: Astroship v2026.1 shall allow two humans play against each other anywhere on or above Earth using a 0.5 Mbps or faster WiFi or cellular connection.

SOFT-004[UX]{Blaze S}: Astroship v2026.2 (or higher) shall have a single player local game mode that uses an on device Apple Foundation model.

SOFT-005[Logs]{Blaze S}: Software tools utilized should preserve historical test data with added user comments to maintain sufficient audit information to allow engineering investigation of failures occurring during qualification activities.

SOFT-006[API]{Blaze S}: Astroship v2026.0 shall implement the AI opponent as a `GameAI` protocol with `nextShot(on: GameState, rng:) -> GridPoint`, so each AI strategy is interchangeable and independently testable.

SOFT-007[UX]{Blaze S}: Astroship v2026.0 shall use CrissCrossAI as the default solo opponent. CrissCrossAI shall hunt with a [checkerboard search pattern](https://youtu.be/26P1KyvrmjI?si=w-XaKHwjMoptaFk9&t=745) and, on a hit, target adjacent unshot cells until the ship is sunk, then resume hunting. 

SOFT-008[UX]{Blaze S}: Astroship v2026.0 shall include DumbScanAI as the simplest AI strategy, choosing shots at random with no targeting memory, for debugging and to fulfill SOFT-002.

SOFT-009[UX]{Blaze S}: Astroship v2026.0 shall expose a single AI difficulty `skillLevel` slider from 0 to 10 to player, default 5, with 0 reserved for debugging and 1 the minimum shown to the player. The solo setup shall display the chosen strategy name and skill level before the match starts.

SOFT-010[Testing]{Blaze S}: Astroship v2026.0 AI decisions shall be deterministic given a seeded random number generator: the same game state and seed shall always produce the same AI shot, so solo matches are reproducible in tests.

SOFT-011[API]{Blaze S}: Astroship v2026.0 AI shots and placements shall go through the same `GameState` validation as human moves (in bounds, unshot, correct turn, 7-ship cap). An invalid AI move shall throw and change nothing.

SOFT-012[Security]{Blaze S}: Astroship v2026.0 AI shall never use hidden information: it may only use its own shot history and revealed results (hit, miss, sunk), never the opponent's unrevealed ship cells, even though the `GameState` passed to it contains both grids.

SOFT-013[UX]{Blaze S}: Astroship v2026.0 AI shall place all 7 ships before the battle starts, each with exact cells matching its length (2–5) in an I, X, T, or Y footprint, inside the 14x10x4 board with no overlapping cells.

SOFT-015[Performance]{Blaze S}: Astroship v2026.0 AI shall fire exactly once per turn and only when it is its turn, and AI shot selection shall run off the main thread so the board stays responsive while the AI thinks.

SOFT-016[OS]{Blaze S}: Astroship v2026.2 (or higher) shall implement the on-device Apple Foundation Model AI as a `LocalFoundationModelAI` conforming to the same `GameAI` protocol, as a drop-in replacement for CrissCrossAI with no server dependency.

SOFT-017[OS]{Blaze S}: Astroship v2026.x shall not use a server-side model AI; a server-seide AI shall only be considered with SYSA-005 in v2028.0 or later.

SOFT-018[UX]{Blaze S}: Astroship v2027.0 (or lower) AI personalities (AiCarey, AiBlaze) shall be trained on Blaze & Carey human game play saves in a SQLite file.

SOFT-019[UX]{Blaze S}: Astroship v2026.0 shall unlock friend invites on solo victories.

SOFT-020[Testing]{Blaze S}: Astroship v2026.0 AI shall be covered by XCTest under SYSA-001: determinism with a seeded RNG, shot legality (in bounds, unshot, on turn) for DumbScanAI and CrissCrossAI, and completion of full solo games (win and loss).

SOFT-021[Logs]{Blaze S}: Astroship v2026.0 solo match results shall be recorded as `MatchRecord` history (AI strategy, skill level, outcome, shot count) with test data preserved for audit under SOFT-005.

SOFT-022[UX]{Blaze S}: Astroship v2026.1 AI turns shall use the same accessibility encoding as human turns under INTE-001: every AI shot and its result shall be shown by shape and VoiceOver label, never colour alone, with visual-only alerts and no audio-only cues.

SOFT-023[UX]{Blaze S}: Astroship may support a 2D-only game mode for standard iPhones (not iPhone Duo's), in which the AI shall play on the 14x10 board with depth fixed at 0.

SOFT-024[UX]{Blaze S}: Astroship v2026.x AI shall not use the radar move until its semantics are defined (Phase 2 decision), and shall not fire at radar- or empty-revealed cells, which `GameState` rejects as already fired.

SOFT-025[Cost]{Blaze S}: Astroship v2026.0 basic AI opponents (DumbScanAI and CrissCrossAI) shall be available in the free game and shall not be gated by Astroship Pro, which gates online multiplayer and levels only.
<br><br>


<a id="sec-3-4-interface" name="sec-3-4-interface"></a>
### 3.4	Interface Requirements (INTE-###)
INTE-001[UX]{Blaze S}: Astroship v2026.1 shall let colorblind and deaf people play the full game. It shall be satisfied by INTE-003 (shape and label encoding), INTE-004 (VoiceOver labels), INTE-005 (visual-only alerts), and INTE-006 (Dynamic Type, Reduce Motion, high-contrast mode).

INTE-002[UX]{Blaze S}: Astroship v2027.X (or higher) shall let blind people play the full game using Siri AI voice commands, by satisfying INTE-009 (VoiceCommand seam) and INTE-010 (voice placement, shots, and results). The v2026.x releases shall only carry the VoiceCommand seam, not the voice interface itself.

INTE-003[UX]{Blaze S}: Astroship v2026.1 shall distinguish every cell state by shape and text label, never by colour alone: fog "F", empty "·", ship as an outline shape, hit "X", miss "O", radar "R" (CellState).

INTE-004[UX]{Blaze S}: Astroship v2026.1 shall give every grid cell a VoiceOver label naming its position and state (for example "Row 3, Column 4, hit"), and every interactive control a VoiceOver label and hint. VoiceOver label coverage for every CellState shall be tested under SYSA-001.

INTE-005[UX]{Blaze S}: Astroship v2026.1 shall convey all game information visually: anything announced by audio shall also be shown on screen, with visual-only alerts and no audio-only cues, so deaf players miss nothing.

INTE-006[OS]{Blaze S}: Astroship v2026.1 shall respect the system's Dynamic Type, Reduce Motion, and high-contrast mode settings.

INTE-007[UI]{Blaze S}: Astroship v2026.1 shall accept finger touch and Apple Pencil (USB-C) interchangeably for placing ships and calling shots (MECH-002).

INTE-008[UI]{Blaze S}: Astroship v2026.0 on iPhone Duo shall present two panes in landscape — one for my fleet, one for the hunt — with the SwiftUI grid laid over the 1.4:1 starry backgrounds, never baked into them.

INTE-009[API]{Blaze S}: Astroship v2026.1 shall keep a VoiceCommand seam in the view model, so the Siri voice interface (INTE-010) can be added without rewriting BattleView.

INTE-010[UX]{Blaze S}: Astroship v2027.X (or higher) shall let blind people place ships, call shots, and hear results (hit, miss, sunk, turn, winner) by voice using Siri AI.

INTE-011[UX]{Blaze S}: Astroship v2026.0 shall sign the player in to Game Center through GameKit's in-app prompt, and the lobby shall show the authentication status with a Try again control when sign-in fails. Debug builds shall use a sandbox tester account, never a real Apple ID.

INTE-012[UX]{Blaze S}: Astroship v2026.1 shall offer Find Opponent automatch in the lobby, disabled until the player is authenticated, and shall show the match status and handle disconnects.
<br><br>


<a id="sec-4-non-functional" name="sec-4-non-functional"></a>
### 4	Non-Functional Requirements
Non-Functional requirements are quality constraints that the system must satisfy according to the project contract. They are also called non-behavioral requirements. They deal with issues like: Portability, Security, Maintainability, Reliability, Scalability, Performance, and Reusability.

<a id="sec-4-1-system-attributes" name="sec-4-1-system-attributes"></a>
### 4.1	System Attributes Requirements (SYSA-###)
SYSA-001[Testing]{Blaze S}: Astroship integration and unit tests shall provide test reports demonstrating requirement validation (not verification) with strict acceptance criteria outlined the following TODO (3) requirements: INTE-001, INTE-002, and SOFT-005.  

SYSA-002[QA]{Blaze S}: Astroship shall use calendar version number (e.g. v2026.1, v2027.42) in all public and internal releases.

SYSA-003[Process]{Blaze S}: All external libraries use shall be on the approved vendor list (AVL) as defined here (TelemetryDeck).

SYSA-004[Logs]{TODO}: Astroship shall use Apple's "Game Center" backend to handle ranking, small profiles, single sign on.

SYSA-005[Logs]{Blaze S}: Astroship v2028.0 (or higher) may use a 32 GB RAM Linux Virtual Private Server (VPS) and opensource Python FastAPI backend to enable cross platform play with Android or the web and more detailed gameplay level analytics, and anti-cheat (that runs well on all Linux Desktop distros released after Jan 2022) to sync multiplayer matches and allow long term support of game even if Sol-X goes out of business. 

SYSA-006[Quality]{Blaze S}: Astroship v2027.X (or lower) shall never place ads anywhere on the screen.
<br><br>


<a id="sec-4-2-project-management" name="sec-4-2-project-management"></a>
### 4.2	Project Management Requirements (PROJ-###)
PROJ-001[Process]{Blaze S}: The Astroship product shall use GitHub Issues and Linear to track feature development.

PROJ-002[Schedule]{Blaze S}: All hardware purchases shall have a lead time of less then 7 days and use two-day or faster shipping to reduce down time. 

PROJ-003[Process]{Blaze S}: All product communication shall be through the "Astroship Duo" iMessage & WhatsApp groups with yellow app icon.

PROJ-004[Quality]{Blaze S}: All Astroship product engineering, branding and marketing decision shall be made by Blaze Sanders the 100% owner of Sol-X LLC.

PROJ-005[Quality]{Blaze S}: All Astroship UX designs choices shall be reviewed by Carey before public release using Figma and GitHub Issues.
<br><br>


<a id="sec-4-3-regulatory" name="sec-4-3-regulatory"></a>
### 4.3	Regulatory / Approbation Requirements (REGU-###)
REGU-001[Process]{Blaze S}: Astroship v2026.1 (or higher) shall be a product of Sol-X LLC sold via www.astroship.store and the iOS, TVOS, VisionOS Apple App Stores. 

REGU-002[Safety]{Blaze S}: Evidence of compliance may include reports, certifications, declarations, laboratory test records, safety analyses, or manufacturer documentation.
<br><br>


<a id="sec-4-4-certifications" name="sec-4-4-certifications"></a>
### 4.4	Certifications Requirements (CERT-###)
CERT-001[Process]{Blaze S}: TODO
<br><br>


<a id="sec-5-reference-documents" name="sec-5-reference-documents"></a>
### 5	Reference & Support Documents 
1. How to [create tables in Markdown](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-tables)
2. To view SQLite database TODO.db or MySQL database TODO) use the following SQL statements:
* SELECT * FROM  "Requirements" WHERE "note" LIKE '%See%' ORDER BY "id" ASC LIMIT 300 OFFSET 0;
3. [Game Music Design](https://kierannolan.com/bitbas/)
4. [Astroship Private iCloud Drive](https://www.icloud.com/iclouddrive/0c3x8qLlcmu7eYAt8mL6EOcxw)
