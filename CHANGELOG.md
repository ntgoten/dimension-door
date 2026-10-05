# Changelog

## 0.8.1
- Gamepad combo follows the game's controls: hold the **Vocation Action** button and give **Go!** (default
  R1 + d-pad up) instead of a fixed L1. Pawn commands are blocked while the Vocation Action is held; no learning
  step any more.
- While aiming, Go! alone locks the target; the held button is tracked through the cast, so closing the door
  with the combo works while still holding it.

## 0.8.0
First public release.
- Beam from the eyes to the camera aim (up to 500 ft), stops at the first surface; sparks mark the target.
- Mage casting animation while aiming, release animation when the target is locked.
- Frost-shimmer door next to you toward the camera, also in the air; closes after 60 s or on a key press.
- Arrival scene: camera flight, door at the destination, walk-out toward the camera, camera hand-back.
- Keyboard B or gamepad L1 + d-pad up; pawn commands blocked while L1 is held (learned automatically).
- Aim checks both thin rays and terrain spheres (a ray through a hill no longer puts the target behind it).
- A second, visual-only door appears at the destination while the door is open.
- Landings must be reachable from open air (no more landing inside rocks); a fall guard catches falling through
  ground that hasn't loaded yet; no fall damage from the height you jumped into the door at.
- Safety: a mid-air landing with ground above it is moved up onto that surface; nothing below fizzles.
