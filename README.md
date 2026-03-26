# VRaze

**VRaze** is a VR port of **Raze** for Android-based VR headsets. Originally forked from **RazeXR 1.0.0** (based on Raze 1.7), VRaze expands on that foundation with new features, fixes, and ongoing active development.

## FEATURES (as of 1.9.5)
- `BUILT-IN 3D WEAPONS` for Duke Nukem 3D, Blood, Shadow Warrior, Redneck Rampage, Rides Again, Exhumed/Powerslave, NAM, and WW2GI.
- `BUILT-IN-CUSTOM 3D WEAPON OFFSET MENU`. Let's the player adjust the position, scale, and orientation of 3D Weapons from within VRaze.
- `BUILT-IN GAME SWITCHER`. Let's the player switch games from within VRaze. No companion app / launcher needed.
- `BUILT-IN MOD LOADER`. Let's the player activate mods from within VRaze. No companion app / launcher needed.
- `MULTI-MOD SUPPORT`. *Experimental*. Replaces def overrides with def accumulation and conflict specific overrides based on FIFO load order priority. First selected mod is applied first (lowest priority), second selected mod is applied next (overriding only conflicting definitions with first mod, higher priority), third selected mod is applied next (overriding only conflicting definitions with first and second mods, even higher priority), etc.
- `WEAPON SELECT SHORTCUTS`. Let's the player quickly switch weapons with preset button combinations.
- `IN-GAME VR CONTROLS AND WEAPON SHORTCUTS REFERENCE MENUS`. Let's the player quickly reference all the default VR Controls and Weapon Shortcuts.
- `CHEAT MENU`. Let's the player enable god mode, toggle clipping, grant all weapons/keys/items, and skip/warp to different levels.
- `TWO-HAND GRIP MODE TOGGLE`. Let's the player aim with both controllers.
- `CONTROLLER SWITCH ACTIVATION TOGGLE`. Let's the player activate switches based on position/rotation of the controller instead of the players view.
- `DOOM-STYLE SPRITE ROTATION TOGGLE`. Makes sprites rotate to face the player instead of rotating in lockstep with the players view.
- `HAIR TRIGGLE TOGGLE`. Let's the player reduce trigger activation threshold from 50% to 10%.

## GENERAL FIXES (as of 1.9.5)
- Fixed search paths and game detection. Supported games should be properly found and in-game names/episodes should be properly displayed.
- Fixed Clear Bind button. Right Grip + B will now properly clear any bind.
- Increased voxel limit from 1024 to 2048.
- Fixed Save/Load screen panel size.
- Fixed ANR loop on first run after fresh install.
- Pushed WW2GI to separate thread at launch to fix ANR loop under certain conditions.
- Increased file copy buffer size.
- `ALL` Fixed player view contaminating 6dof crosshair position.
- `ALL` Fixed viewscreens. Now display the live feed from their attached/selected camera properly.
- `ALL` Fixed misaligned 6dof crosshair. Now centered where aiming instead of foot-aligned.
- `ALL` Fixed display lag with mirrors.
- `BLOOD` Fixed HUD progress bar being rendered separately per eye. Now displays properly in stereo.
- `BLOOD` Raised HUD progress bar slightly.
- `BLOOD` Added detection for official expansion Marrow (part of game list now).
- `BLOOD` Added detection for official expansion Death With (part of game list now).
- `BLOOD` Set CD Audio default to On.
- `BLOOD` Fixed music fallback. If CD Audio is on and CD music files are not found it will now play midi music instead of nothing.
- `BLOOD/SW` Fixed 6dof crosshair lag.
- `BLOOD/SW/EX` Removed baked in barrel offsets.
- `DUKE` Fixed Pipe Bomb behavior. Now correctly explodes when damaged instead of turning invisible.
- `DUKE` Fixed Pipe Bomb firing angle. Now throws where the player is aiming instead of looking.
- `DUKE` Removed view lock while frozen.
- `DUKE` Fixed Protozoid Slimer eating behavior. Eaten enemies should no longer turn invisible and become unstoppable. Now they die like they're supposed to.
- `DUKE` Fixed Protector Drones not being able to trigger certain sector warps. They should be able to follow the player into our out of water now.
- `EX` Fixed HUD messages font being too large and messages getting cut off.
- `EX` Fixed Grenade throwing behavior. Holding the trigger longer should make the grenade throw farther.
- `EX` Removed pitch clamp while aiming.
- `EX` Fixed Ramses not appearing during scripted sequences.
- `EX` Removed view lock during scripted Ramses sequences.
- `EX` Fixed firing angle of Flamethrower and Cobra Staff.
- `NAM` Removed fake scope overlay from Sniper Rifle.
- `NAM/WW2GI` Increased size and brightness of crosshair.
- `NAM/WW2GI` Fixed Sniper Rifle missing impact effects.
- `NAM/WW2GI` Fixed Sniper Rifle accuracy.
- `NAM/WW2GI` Fixed Sniper Rifle damage.
- `RR/RA` Removed excessive and disorienting pushback/shake mechanics when firing certain weapons.
- `RR/RA` Removed forced forward lunge when using the Bowling Ball.
- `RA/SW` Removed view lock during vehicle sections.
- `RA/SW` Removed crosshair lock during vehicle sections.
- `RA/SW` Fixed player controls when in vehicles.
- `SW` Fixed player view shifting when activating viewscreens via sector trigger.
- `SW` Fixed rendering angle, controls, alignment, and 6dof crosshair when riding a sector object.
- `WW2GI` Fixed TNT placement behavior.
- `WW2GI` Fixed Grenades not being throwable.

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
| Duke Nukem 3D                     | DUKE3D.GRP, DUKEDC.GRP, VACATION.GRP, NWINTER.GRP, DUKEZONE2.GRP *(fixed version)*, WORLDORDER.GRP *(script extracted version)*, WORLDTOUR.ZIP *(zipped World Tour folder)* |
| Exhumed / Powerslave              | BOOK.MOV, STUFF.DAT, CD music files |
| NAM                               | NAM.GRP, GAME.CON |
| Redneck Rampage + Route 66        | REDNECK.GRP, *Route 66 files*: All *66*.ANM/.ART/.CON/.VOC files, all .MAP files, ASYAMB.VOC, G_BITE.VOC, G_SIT.VOC, NEON.VOC *(can be zipped as `route66.zip`)*, CD music files |
| Redneck Rampage Rides Again       | REDNECK.GRP/RIDES.GRP/RIDESAGAIN.GRP *(name may vary)*, CD music files |
| Shadow Warrior + Expansions       | SW.GRP, TD.GRP/TWINDRAG.GRP *(name may vary)*, WT.GRP, CD music files |
| WW2GI + Platoon Leader            | WW2GI.GRP, PLATOONL.DAT, PLATOONL.DEF |

