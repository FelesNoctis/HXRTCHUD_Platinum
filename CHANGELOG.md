# Changelog

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