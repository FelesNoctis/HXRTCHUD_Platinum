# Changelog

## DEV

- **General:**
  - Newly scripted "manual" powerup tracking system implemented for those that have obscured duration control.
  - Stamina module scripting now references a CVAR that may be used for additional customization at a later date.

- **Bottom-Left Panels:**
  - **Mugshot** panel border tweaks to allow Invul to fill in the corners when the player doesn't have Berserk.

- **Mod Updates:**
  - Brutal Doom Platinum v3.1:
    - Nuke availability panel now only appears if you've found a weapon that utilizes it, similar to how the BDv21/CE HUD operates.

- **Mod Support:**
  - Brutal Doom Black Edition v3.36
    - Known Issue: Some powerups may repeat their countdown as they can stack their duration, but due to using an "handler" actor with no TID controlling the total duration by user variable, I can't access it with ACS. ZScript may be able to do so, but that's out of scope for the project at this time.

## v0.65

- **General:**
  - Mod control scripts have been entirely overhauled due to reaching the limit of level-scope vars that were allowed. All control vars are now constants (#define and #libdefine).

- **Mod Updates:**
  - Faspons:
    - Ammo counter changed from ammo1 to ammo2, because hurr durr how did we miss this before?

## v0.61

- **Bottom-Right Panels:**
  - **Ammo Tally** display of throwables will now fade to grey when the player is out of ammo for the throwable item, instead of staying orange.

- **Mod Support:**
  - Meatgrinder v2-C
  - Meatgrinder MrChoriCheeseEdition update 1

## v0.60

- **Mod Updates:**
  - Brutal Doom Platinum v3.1:
    - Haste Powerup's timer updated
    - Haste's infinite ammo property now takes control of the Current Ammo window for its affected weapons!
    - Railgun ammo tracking updated
    - Unmaker Mode: Corrected missing 6-digit functionality for expanded displays
    - Unmaker Mode: Low Motion is now implemented, locking numbers and bars

## v0.57

- **Mod Updates:**
  - ZioMcCall's Brutal Wolfenstein v6.0:
    - Gewehr 43 support added.
    - Leichenfaust 1943 support added.

## v0.56

- **Top-Left Panels:**
  - **KIS Panel** can now be configured for 4, 5, or 6 digits, to handle INSANE numbers of things.

- **Mod Updates:**
  - Brutal Doom 64 v2.5_r31:
    - Corrected mod detection script to include changed indicators.
    - Updated support for 64SMGTactical and 64RocketLauncherTactical, which unfortunately isn't backwards compatible due to how the Rocket Launcher changed.
    - Updated weapon icons for rifle and laser to respond to BD64's visual customization. New rocket launcher skin has no unique icon yet.
  - Brutal Doom Platinum v3.0:
    - Grenades now use the same "low ammo" indicators as weapon mags.
    - Added support for G-Chan's Vorpal Blade.
  - ZioMcCall's Brutal Wolfenstein v5.8:
    - Panzerfaust support added.
    - Vertical mag ammo bar now correctly tracks magazine ammo.
    - Refactored "low ammo" thresholds for Gatling Gun (clip 200, low 50) and Flammenwerfer (max 20, low 5).
    - Throwing Axe reserve ammo visibility improved as it's an on-demand weapon.

## v0.55

- **Bottom-Left Panels:**
  - **Artifact Pieces** panel added for use with any mod that uses the 3-step weapon powerup system.

- **Settings:**
  - **Mod-Specific** settings section added. Right now this only contains the toggle to force WolfenDoom layout.

- **Mod Support:**
  - Doom 4 Vanilla 3.2.1
  - Doom 64: Retribution v1.5
  - Faspons (REL: MAR 13 2020) & (DEV: MAR 16 2020)
  - Kriegsland 1: Blutorden v2.4 (ZScript & Orig)
  - Kriegsland 2: Untergrund v1.4 (ZScript & Orig)
  - Lt. Typhon V6
  - Omni-Wolf v1.2
  - Supercharge v2.9 (with backwards support for v2.8)
  - Weasel Presents: NAZIS V2
  - WolfenDoom Enhanced
  - WolfenDoom V2
  - ZioMcCall's Brutal Wolfenstein v5.5

## v0.30

- **General:**
  - Major version change would have happened in 0.21, but the connection to BDv21 was just too good, so you get it here instead.
  - Master Presence token added (HXSYS_HUDACTIVE) to allow reliable detection of the HUD by other mods.

- **Bottom-Right Panels:**
  - **Keys Bar** positioning and sizes have been adjusted for oversized keys, such as Doom64 keys, for supported mods

- **Mod Support:**
  - Beautiful Doom 7.1.6
  - Brutal Doom 64 v2.5
  - Doom CE 3.1.3: Doom64
  - Doom CE 3.1.3: PSX
  - Supercharge v2.8

## v0.21

- **General:**
  - All mod- (also vanilla-) specific scripts have been pulled out of the shared file and now each have their own.
  - Every mod supported will have its own script, even if it would still use vanilla tokens. This allows for quick changes in the future, and also cuts back on loops constantly running over logic checks.
  - Due to both of the above, mod existence logic checks have been swapped to look for their token before running a loop, so they run once on map load and then never again if their mod isn't active.

- **Bottom-Right Panels:**
  - **Keys Bar** now uses DrawKeysBar function. This means the HUD now uses the default icon assigned to a key, but is much more flexible regarding mod support
  - **Keys Bar** is now a panel that can toggle between 1x6 and 3x8 layouts, for when maps have crazy numbers of keys

- **Mod Support:**
  - Brutal Doom v21
  - Brutal Doom Community Expansion
  - Brutal Doom Platinum v3.0: Updated support to have generic fallbacks for BDPv2.0's addon weapons until full support is confirmed

## v0.20

- **Mod Support:**
  - Brutal Doom Platinum v3.0

## v0.12

- **General:**
  - More extensive mod compatibility has been created, and parts of the SBARINFO file are being converted to this system.  
  This is likely an ongoing process, continuing into the future as I find more efficient ways to handle mod support.

- **Top-Left Panels:**
  - Togglable "extended" version of the KIS tally, for those occasional maps that need 5 digits

- **Bottom-Center Panels:**
  - New stamina bar. Appears when needed, sticks for roughly 3 seconds after completely refilling, then disappears
  - **Inventory Bar** updated to reposition above stamina bar when both are active

- **Bottom-Left Panels:**
  - RIP female mugshots for mods that support the swap. Apparently the flag for getting it to display isn't supported by Zandronum.

- **Bottom-Right Panels:**
  - **Arms Bar** now always shows all ten (1-0) digits. This is to simplify mod support, but may be subject to change

- **Mod Support:**
  - Brutal Doom Platinum v2.0
  - Led's Generic Weapon Mod

## v0.11

- **Bottom-Left Panels:**
  - Air Supply bar is now on a toggle, default "false", due to Zandronum not supporting "IfWaterLevel"

## v0.10

- **General:**
  - **HUD Customization:** Top-Left, Bottom-Left, Top-Right, Bottom-Right panel toggles added
  - **Inventory Bar:** Implemented at 5 slots, centered at bottom of screen
  - **Visual Style:** Interpolated a bunch of things for nice smooth motion
  - **Visual Style:** Standardized border transparencies
  - **Weapon Icons:** "alticonfirst" flag added to hopefully catch more mod-added cases

- **Bottom-Left Panels:**
  - Swapped Armor and Berserk panels
  - Berserk will now only appear when active
  - Removed Armor Save % bar, relocated as a panel above armor image
  - Removed Air Supply/Rage bar, relocated to conditionally display left and right of the mugshot
  - Health and Armor Total bar recognizes values 101-200 and renders a second bar

- **Mod Support:**
  - _BDLite:_ Keys should now display correctly
  - _SmoothDoom:_ Mugshot handling for unique death animation

## v0.03

- **Mod Support:**  
  - BDLite + all "official" addons

## v0.02

- **General:**
  - Modular Ammo Tally panel for ease of future mod support
  - ACS-based cvar handler to allow for a reactive HUD

- **Mod Support:**
  - PerK's Smooth Weapons Enhanced
  - SmoothDoom 2.0

## v0.01

Stuff and things. I'll fill this in later. Maybe. There's a lot.
