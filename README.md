# Dimension Door

A Dragon's Dogma 2 mod (REFramework Lua script) that adds a **Dimension Door** spell in the style of the
D&D one: aim at a spot up to 500 ft away, open a door of light next to you, walk through it and step out
at the destination.

- **Cast:** press **B** (keyboard), or **hold your Vocation Action button and give Go!** (gamepad; with the default
  controls that's **R1 + d-pad up**). The mod follows the game's own button mapping. Your character goes into the Mage's
  spell-casting animation and turns to where you aim. A beam goes from your eyes to where the camera
  points and stops at the first thing it hits (ground, a wall, a roof); sparks mark the spot. If it hits
  nothing it ends in the air 500 ft away.
- **Open the door:** press again (on gamepad, d-pad up alone works while aiming). The target is locked and a door of frost shimmer opens right next to you,
  toward the camera, even in the air at a roof edge. A matching door appears at the destination too (just
  for show).
- **Walk through it:** the camera flies to the destination, a door opens there, your character steps out of
  it toward the camera, and the camera swings back behind you. Press once more to close an open door; it also
  closes by itself after a minute.
- **Gamepad:** while the Vocation Action button is held, the d-pad doesn't give pawn commands (like holding the
  weapon-skill button switches the d-pad to item shortcuts).
- Free: no cost, no cooldown.

Everything you see is the game's own: Mystic Spearhand's Skydragon's Fangtooth sparks and sounds, the Frost
Boon shimmer (played from the game's own effect file, no frost weapon needed), and the Mage's casting animation. No game files are included or replaced.

Current version: **0.8.2**. Download it from [Releases](../../releases).

## Requirements

| What | Needed? | Why |
|---|---|---|
| Dragon's Dogma 2 (PC) | Required | Tested on dd2.exe 3.2.0.0 (Steam build 24831693). |
| [REFramework](https://github.com/praydog/REFramework) by praydog | **Required** | Loads the Lua script (`dinput8.dll` in the game folder). |
| **_ScriptCore** by SilverEzredes and alphaZomega | **Required** | Its raycast helper (`reframework/autorun/_SharedCore`) finds where the beam hits and where you land. Find it on Nexus Mods (Dragon's Dogma 2). You already have it if you use NickCore or UDD2P. |

## Install

1. Install REFramework and _ScriptCore.
2. Copy the `reframework` folder from this repository (or the release zip) into your Dragon's Dogma 2
   folder, next to `dd2.exe`, merging folders.
3. Start the game. Back up your saves before trying any new mod.

## Settings

Press **Insert** → *Script Generated UI* → **Dimension Door v0.8.2**:

- **Enabled**, **Key** (click to change), **Hold Vocation Action + Go!** (shows whether the button is seen as held)
- **Max range (ft)**, **Door stays open (s)**, **Door height offset (m)**
- **Casting animation while aiming**, **Arrival scene** (off = instant teleport), **Camera flight (s)**
- **Sounds**, **Default**

Settings are saved to `reframework/data/DimensionDoor.json`.

## Uninstall

Delete `reframework/autorun/DimensionDoor.lua` (and `reframework/data/DimensionDoor*.json`).

## Known limits

- After a long jump the game may not have loaded the ground yet; the mod catches you for 2 s if you start
  falling through it. Arriving lower than where you jumped in doesn't cause fall damage; falling after you
  arrive does.
- Aiming somewhere the game has no solid ground for (deep under the map, out of the world) makes the spell
  fizzle. A target in mid-air means you appear there and fall.
- While casting (and during the short release) your character doesn't react to anything else.
- The casting animation is made for a staff, so with other weapons the hands are posed for a staff.
- Single-player only. Your character only (pawns are not taken along unless you carry one).

## Credits

- **Capcom** for Dragon's Dogma 2. The effects, sounds and animations are the game's own, used by ID.
- **praydog** for [REFramework](https://github.com/praydog/REFramework).
- **SilverEzredes** and **alphaZomega** for _ScriptCore (raycasts).
- **Nickesponja** for UDD2P and its NickCore library: their scripts showed how to play effects, add animation
  banks, warp the player and read input.
- Built with AI assistance: [Claude Code](https://claude.com/claude-code) and the
  [universal-modder](https://github.com/rehan-remade/universal-modder) toolkit by rehan-remade.
