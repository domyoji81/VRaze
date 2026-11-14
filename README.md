# VRaze

**VRaze** is a sourceport for playing Build Engine games (Duke Nukem 3D, Blood, Shadow Warrior, etc.) in Virtual Reality on Android-Based headsets.

## FEATURES (as of Alpha 1.20.2)
- `BUILT-IN 3D WEAPONS` for Duke Nukem 3D, Blood, Shadow Warrior, Redneck Rampage, Rides Again, Exhumed/Powerslave, NAM, WW2GI and Witchaven.
- `BUILT-IN-CUSTOM 3D WEAPON OFFSET MENU`. Let's the player adjust the position, scale, and orientation of 3D Weapons from within VRaze.
- `BUILT-IN GAME SWITCHER`. Let's the player switch games from within VRaze. No companion app / launcher needed.
- `BUILT-IN MOD LOADER`. Let's the player activate mods from within VRaze. No companion app / launcher needed.
- `MULTI-MOD SUPPORT`. Replaces def overrides with def accumulation and conflict specific overrides based on FIFO load order priority. First selected mod is applied first (lowest priority), second selected mod is applied next (overriding only conflicting definitions with first mod, higher priority), third selected mod is applied next (overriding only conflicting definitions with first and second mods, even higher priority), etc.
- `MULTIPLAYER` for Duke Nukem 3D. Up to 16 player Dukematch (vs real opponents or AI controlled bots or both), adapted from NetDuke32, with custom usermap support. Playable via `Direct` TCP/IP connection or via integrated `NukemNet` IRC Relay.
- `REAL VR MELEE COMBAT` for Witchaven. Physically swing weapons at enemies to do damage. Supports dual wielding (independently controlled weapons in each hand).
- `MUTATORS` for Witchaven. A variety of toggleable game modifiers, such as respawning weapons, automap key markers, weather effects, enhanced gore, and more.
- `WEAPON SELECT SHORTCUTS`. Let's the player quickly switch weapons with preset button combinations.
- `WEAPON WHEEL` for Duke Nukem 3D, Blood, Shadow Warrior, Redneck Rampage, Rides Again, Powerslave, WW2GI, Platoon Leader, NAM, and Witchaven. Let's the player bring up a radial menu on the HUD for weapon swapping as an alternative to the weapon select shortcuts and weapon cycling. Slows game speed while open.
- `ITEM WHEEL` for Duke Nukem 3D, Blood, Shadow Warrior, Redneck Rampage, Rides Again, Powerslave, WW2GI, Platoon Leader, NAM, and Witchaven. Let's the player bring up a radial menu on the HUD for item usage as an alternative to item cycling. Slows the game down while open.
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
| Witchaven                         | VRaze/raze/witchaven/     |
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
| Witchaven                         | JOESND, SONGS, TILES000.ART-TILES010.ART, LEVEL1.MAP-LEVEL25.MAP, PALETTE.DAT, LOOKUP.DAT, TABLES.DAT, MENUPAL.DAT, INTRO.SMK |
