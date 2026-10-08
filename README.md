# VRaze

**VRaze** is a sourceport for playing Build Engine games (Duke Nukem 3D, Blood, Shadow Warrior, etc.) in Virtual Reality on Android-Based headsets.

> **Please read the GPLv2 Experimental / Internal Test Build Notice at the bottom of this document before downloading or attempting to use any experimental binary contained in this repository.**

## FEATURES (as of Alpha 1.14.0)
- `BUILT-IN 3D WEAPONS` for Duke Nukem 3D, Blood, Shadow Warrior, Redneck Rampage, Rides Again, Exhumed/Powerslave, NAM, and WW2GI.
- `BUILT-IN-CUSTOM 3D WEAPON OFFSET MENU`. Let's the player adjust the position, scale, and orientation of 3D Weapons from within VRaze.
- `BUILT-IN GAME SWITCHER`. Let's the player switch games from within VRaze. No companion app / launcher needed.
- `BUILT-IN MOD LOADER`. Let's the player activate mods from within VRaze. No companion app / launcher needed.
- `MULTI-MOD SUPPORT`. Replaces def overrides with def accumulation and conflict specific overrides based on FIFO load order priority. First selected mod is applied first (lowest priority), second selected mod is applied next (overriding only conflicting definitions with first mod, higher priority), third selected mod is applied next (overriding only conflicting definitions with first and second mods, even higher priority), etc.
- `MULTIPLAYER` for Duke Nukem 3D. Up to 16 player Dukematch (vs real opponents or AI controlled bots or both), adapted from NetDuke32, with custom usermap support. Playable via `Direct` TCP/IP connection or via integrated `NukemNet` IRC Relay.
- `WEAPON SELECT SHORTCUTS`. Let's the player quickly switch weapons with preset button combinations.
- `WEAPON WHEEL` for Duke Nukem 3D, Blood, Shadow Warrior, Redneck Rampage, Rides Again, Powerslave, WW2GI, Platoon Leader, and NAM. Let's the player bring up a radial menu on the HUD for weapon swapping as an alternative to the weapon select shortcuts and weapon cycling. Slows game speed while open.
- `ITEM WHEEL` for Duke Nukem 3D, Blood, Shadow Warrior, Redneck Rampage, Rides Again, Powerslave, WW2GI, Platoon Leader, and NAM. Let's the player bring up a radial menu on the HUD for item usage as an alternative to item cycling. Slows the game down while open.
- `IN-GAME VR CONTROLS AND WEAPON SHORTCUTS REFERENCE MENUS`. Let's the player quickly reference all the default VR Controls and Weapon Shortcuts.
- `CHEAT MENU`. Let's the player enable god mode, toggle clipping, grant all weapons/keys/items, and skip/warp to different levels.
- `TWO-HAND GRIP MODE TOGGLE`. Let's the player aim with both controllers.
- `CONTROLLER SWITCH ACTIVATION TOGGLE`. Let's the player activate switches based on position/rotation of the controller instead of the players view.
- `DOOM-STYLE SPRITE ROTATION TOGGLE`. Makes sprites rotate to face the player instead of rotating in lockstep with the players view.
- `HAIR TRIGGLE TOGGLE`. Let's the player reduce trigger activation threshold from 50% to 10%.
- `REBUILT OPENGL ES BACKEND`. Provides a massive performance increase over the original OpenGL backend.
- `NEW MESHING SYSTEM`. Enables full greedy voxel meshing, pre-loading meshes on app-start, and a mesh cache (saved between app instances) for increased performance.

## INSTALLATION INSTRUCTIONS
1. If upgrading from a previous version, uninstall VRaze from your headset first, then navigate to the /VRaze/ folder on your headset and delete `raze.pk3` and `commandline.txt`.
2. Install VRaze (if using Sidequest, click on the icon near the top right that has an arrow facing down and select the VRaze-xxxx.apk).
3. When done installing, make sure VRaze has read/write permissions. You can do this with Sidequest by clicking on the "Currently installed apps" icon near the top right (it's a 3x3 square grid). Then scroll down the list until you see "com.vraze" and click the gear icon to the right of it. A window will pop up, scroll down and look at the bottom right. Toggle READ_EXTERNAL_STORAGE and WRITE_EXTERNAL_STORAGE to on (the pip should be on the right side).
4. In your headset under the unknown sources apps, run VRaze. If this is your first time using VRaze you need to make sure all your game files are placed in the appropriate game folders.

Place game data in the following directories:
| Game                              | Path                      |
|:----------------------------------|:--------------------------|
| Duke Nukem 3D + Expansions        | VRaze/raze/duke/          |
| Blood + Expansions                | VRaze/raze/blood/         |
| Shadow Warrior + Expansions       | VRaze/raze/shadowwarrior/ |
| Redneck Rampage + Route 66        | VRaze/raze/rampage/       |
| Redneck Rampage Rides Again       | VRaze/raze/ridesagain/    |
| Exhumed / Powerslave              | VRaze/raze/exhumed/       |
| NAM                               | VRaze/raze/nam/           |
| WW2GI + Platoon Leader            | VRaze/raze/ww2gi/         |
| Mods                              | VRaze/raze/mods/          |

## SUPPORTED GAME FILES
| Game                              | Files          |
|:----------------------------------|:---------------|
| Blood + Expansions                | BLOOD.INI, BLOOD.RFF, GUI.RFF, SOUNDS.RFF, SURFACE.DAT, TILES000.ART–TILES017.ART, VOXEL.DAT, GTI.SMK, GTI.WAV, LOGO.SMK, LOGO811M.WAV, CS1.SMK, CS1822M.WAV, CS2.SMK, CS2822M.WAV, CS3.SMK, CS3822M.WAV, CS4.SMK, CS4822M.WAV, CS5.SMK, CS5822M.WAV, CS6.SMK, CS6822M.WAV, *Cryptic Passage files:* All .MAP files, CPART07.AR_, CPART15.AR_, CRYPTIC.INI, CRYPTIC.SMK, CRYPTIC.WAV *(can be zipped as `cryptic.zip`)*, MARROW.ZIP *(can be any name)*, DEATHWISH.ZIP *(can be any name)*, CD music files<br/><br/>*Note: ogv movie format not yet supported* |
| Duke Nukem 3D + Expansions        | DUKE3D.GRP, DUKEDC.GRP, VACATION.GRP, NWINTER.GRP, DUKEZONE2.GRP *(fixed version)*, WORLDORDER.GRP *(script extracted version)*, WORLDTOUR.ZIP *(zipped World Tour folder)* |
| Exhumed / Powerslave              | BOOK.MOV, STUFF.DAT, CD music files |
| NAM                               | NAM.GRP, GAME.CON |
| Redneck Rampage + Route 66        | REDNECK.GRP, *Route 66 files*: All *66*.ANM/.ART/.CON/.VOC files, all .MAP files, ASYAMB.VOC, G_BITE.VOC, G_SIT.VOC, NEON.VOC *(can be zipped as `route66.zip`)*, CD music files |
| Redneck Rampage Rides Again       | REDNECK.GRP/RIDES.GRP/RIDESAGAIN.GRP *(name may vary)*, CD music files |
| Shadow Warrior + Expansions       | SW.GRP, TD.GRP/TWINDRAG.GRP *(name may vary)*, WT.GRP, CD music files |
| WW2GI + Platoon Leader            | WW2GI.GRP, PLATOONL.DAT, PLATOONL.DEF |


# GPLv2 Experimental / Internal Test Build Notice

> **Please read this notice before downloading or attempting to use any experimental binary contained in this repository.**

---

## 1. Nature and Purpose of This Repository

This repository contains development materials for **VRaze**, a project based on software distributed under the GNU General Public License, version 2 ("GPLv2").

From time to time, **The VRaze Team** may make experimental development binaries available in this public-facing repository for the purposes of **internal development, quality assurance, multiplayer/network testing, debugging, and other pre-release testing**.

Such experimental binaries are **not public releases of VRaze** and should not be treated as stable, finished, or generally available versions of the software.

The purpose of making an experimental binary temporarily accessible through this repository is to facilitate testing by specifically selected members of **The VRaze Team's** development and testing team, including team members who are located remotely and therefore cannot participate in local testing.

---

## 2. Authorized Testers Only

An experimental binary identified as an **Internal Test Build**, **Experimental Build**, **Test Build**, **Alpha**, or similar designation is intended solely for specifically authorized members of **The VRaze Team's** development/testing group.

**The VRaze Team expressly requests that members of the general public do not download, execute, copy, redistribute, or otherwise use an experimental test binary unless they have been specifically authorized to participate in that particular test.**

The existence of a download link or other technical means by which an unauthorized person might obtain an experimental binary should not be interpreted as an invitation or authorization for that person to obtain or use it.

If you are not an authorized tester, please do not download or use the experimental binary.

---

## 3. Access Controls

Where appropriate, experimental binaries may additionally be protected by technical access controls.

For example, an experimental binary may require a password or other authorization credential before it can execute. Such credentials are distributed only to specifically selected members of **The VRaze Team's** development/testing group.

The purpose of these measures is to reinforce the distinction between an **internal development/test artifact** and a public release.

An individual who obtains an experimental binary despite the notices and access controls above, but who has not been authorized to participate in the test, has not thereby been granted authorization by **The VRaze Team** to use or redistribute that binary.

**The VRaze Team does not authorize or invite unauthorized acquisition, execution, copying, or redistribution of these experimental builds.**

---

## 4. Internal Development and Testing

**The VRaze Team** understands the GNU General Public License and associated FSF guidance to distinguish between private/internal development and the distribution of copies outside the relevant organization or development group.

The Free Software Foundation's GPL FAQ discusses the situation in which an organization makes and uses multiple copies internally and states that such internal use is not considered distribution in the same manner as transferring copies to other organizations or individuals.

See:

- [GNU GPL FAQ — "Is making and using multiple copies within one organization or company 'distribution'?"](https://www.gnu.org/licenses/old-licenses/gpl-2.0-faq.html#InternalDistribution)

**The VRaze Team's** development team consists of persons organized for the purpose of developing, maintaining, testing, and improving **VRaze**. Team members may work locally or remotely.

Accordingly, **The VRaze Team** considers an experimental binary supplied to an authorized member of its development/testing group for the purpose of participating in **VRaze's** internal development and testing activities to be an **internal development/test artifact**, rather than a public release of that version.

**The VRaze Team does not consider the physical location of an authorized team member, by itself, to transform an internal development activity into a public release.**

**The VRaze Team** recognizes, however, that the ultimate legal characterization of a particular transfer may depend upon applicable copyright law and the specific facts and circumstances involved.

This notice is therefore intended to explain **The VRaze Team's** good-faith interpretation and practices, rather than to assert that this interpretation is an authoritative statement of copyright law.

---

## 5. Meaning of "Organization"

Neither GPLv2 nor the above FSF FAQ states that an "organization" must be a corporation, company, incorporated association, or other formally incorporated legal entity.

**The VRaze Team** therefore understands the ordinary meaning of "organization" to be relevant: a group of persons organized for a particular purpose.

**VRaze** is maintained and developed by a group of persons organized for the purpose of developing and maintaining **VRaze**. Individuals may subsequently be admitted to that group for particular development, testing, quality-assurance, or other project-related purposes.

**The VRaze Team's** position is that an authorized individual who has been specifically admitted to the development/testing group and receives an experimental binary solely to perform that group's internal testing activities should not automatically be characterized as an unrelated third-party recipient merely because that individual is geographically remote.

**The VRaze Team** recognizes, however, that the absence of a formal incorporation requirement does not, by itself, establish the legal characterization of every particular transfer. The actual relationship between the parties, the purpose of the transfer, and applicable copyright law may all be relevant.

---

## 6. Experimental Binaries Are Not Public Releases

Experimental binaries may contain:

- incomplete features;
- untested code;
- temporary implementations;
- debugging facilities;
- experimental networking or multiplayer functionality;
- known or unknown defects;
- code that is subsequently modified or discarded; and

The experimental binary is not intended to constitute a new public release corresponding to the latest source tree merely because the binary happens to be temporarily accessible through this repository.

---

## 7. Corresponding Source and GPLv2 §3

**The VRaze Team** recognizes that GPLv2 §3 imposes source-code obligations when covered object code is distributed in the circumstances described by that section.

The official GPLv2 text provides several mechanisms for satisfying those obligations, including conveying the complete corresponding machine-readable source code or, in circumstances permitted by §3, using an applicable written-offer mechanism.

See:

- [GNU General Public License, version 2 — Section 3](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html#section3)

**The VRaze Team's** position is that a genuinely internal experimental build that is not distributed outside the relevant development organization/group is not equivalent to a public binary release requiring immediate publication of the corresponding source merely because the binary exists.

Once development of all planned features and debugging is complete and **VRaze** is ready for public release, **The VRaze Team** intends to make the corresponding source available in accordance with the applicable GPLv2 requirements.

Nothing in this notice is intended to waive, restrict, or supersede any rights granted by GPLv2.

---

## 8. Unauthorized Acquisition Is Not Authorization

**The VRaze Team** makes a distinction between:

1. **The VRaze Team intentionally providing a copy to an authorized member of its development/testing group**, and
2. **An unauthorized person independently obtaining a copy despite The VRaze Team's explicit instructions and any technical access controls.**

**The VRaze Team** does not intentionally distribute experimental test builds to members of the general public merely by making an internal development artifact temporarily accessible through a public-facing repository.

The FSF's GPL FAQ also addresses the concept of unauthorized acquisition of an unpublished GPL-covered work, including the example of a person obtaining a copy without the copyright holder's authorization. The FAQ distinguishes such unauthorized acquisition from intentional distribution by the copyright holder.

See:

- [GNU GPL FAQ — Official FSF FAQ](https://www.gnu.org/licenses/old-licenses/gpl-2.0-faq.html)

Accordingly, an unauthorized person who deliberately ignores this notice and obtains an experimental binary does not thereby become an authorized tester, nor does such conduct constitute authorization by **The VRaze Team**.

---

## 9. No Additional Restriction of GPL Rights

Nothing in this notice is intended to impose additional contractual restrictions upon a person who has legitimately received a copy of GPL-covered software in circumstances where the GPL grants that person rights to copy, modify, or redistribute the software.

The **"authorized testers only"** designation describes **The VRaze Team's** intended recipients and the circumstances under which **The VRaze Team** is providing an experimental development artifact. It is not intended to modify the rights that GPLv2 grants to a legitimate recipient where those rights otherwise apply.

In particular, this notice should not be interpreted as an attempt to replace GPLv2 with a proprietary **"no redistribution"** license.

---

## 10. Temporary Nature of Experimental Builds

Experimental binaries may be removed, replaced, or superseded at any time.

A test build may remain available only for the duration of the relevant testing period.

The absence of a corresponding source tree for an experimental binary should therefore not be interpreted as an assertion that **The VRaze Team** has permanently released a binary-only version of the modified GPL-covered work.

---

## 11. Relevant Official References

The following official GNU/FSF resources are relevant to the issues discussed above:

- [GNU General Public License, version 2 — Full License Text](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)
- [GNU GPL FAQ — Official FSF FAQ](https://www.gnu.org/licenses/old-licenses/gpl-2.0-faq.html)
- [GNU GPL FAQ — Internal Distribution / Multiple Copies Within an Organization](https://www.gnu.org/licenses/old-licenses/gpl-2.0-faq.html#InternalDistribution)

> **Important:** This notice expresses **The VRaze Team's** understanding and good-faith interpretation of GPLv2 and related FSF guidance. It is not a substitute for advice from a qualified attorney familiar with software copyright and open-source licensing.
