# VS Reimagined

**An unofficial remaster of *Vagrant Story* (Square, 2000) for PC.**

VS Reimagined starts from rood-boi, a native PC port that runs the game's decompiled
code with a modern path-traced renderer, and takes it towards a full remaster:
- new 4K artwork and raised stone relief;
- full voice acting;
- Merlose fighting at Ashley's side;
- modern menus, a bigger inventory and dozens of quality-of-life options;
- fixes for crashes found over many hours of streamed playthroughs.

Not affiliated with or endorsed by Square Enix.

**Source code release: coming later.** Follow development on YouTube:
[HDRcade](https://www.youtube.com/@HDRcade)

## What's different

| | PS1 original | rood-boi (the port this builds on) | **VS Reimagined** |
|---|---|---|---|
| **Engine** | PlayStation | Native PC code, Vulkan, path-traced lighting, 4K, widescreen | The same, plus [the fixes below](#fixes) for crashes and bugs that show up in a full playthrough |
| **Artwork** | Original textures | Original textures; HD packs supported | **4K reimagined texture pack**: over 2,000 textures, hand-corrected, original faces kept; stays HD through menus, targeting and spells |
| **Scenery** | Flat | Flat | **Raised stone relief** through tessellation *(in development)* |
| **Voices** | Text only | Text only | **Full voice acting**: over 1,100 lines, plus the narration screens |
| **Companion** | None | Merlose joins you (Two's A Riot) | **Merlose in the modern menus**: her gear, her items marked, behaviour modes (Aggressive, Balanced, Healer, No casting) on a key or R3 |
| **Inventory** | Original limits | Original limits | **Three times the equipment space**; saves stay compatible with the original |
| **Combat** | Original | Quick weapon swap | **Chain assist** toggle (L3), **fast casting** (hold R2) |
| **Progress** | None | None | **Achievements** for bosses and endings |
| **Options** | None | Graphics and camera options | **Cheats page**: damage multiplier, Never zero, Risk, weapon growth, No wear, Workshop anywhere, Infinite HP, Pause AI |
| **Presentation** | Original | 16:9 option | Widescreen with 4:3 kept for cutscenes or menus if you like, your own title screen and intro images, room-start quick reload (F10), HD on/off toggle (F8) |

## Fixes

A native port runs the game's code in ways the PlayStation never did. Some problems only
appear many hours in, so VS Reimagined is tested by playing it through on stream, and every
crash found gets fixed. Fixed so far:

**Crashes**
- Leaving a room after one of the numbered blocks has vanished (the Iron Maiden block
  puzzles)
- A character linked to an empty slot, a few frames after entering a room
- A character standing off the room's floor map
- An enemy chasing or facing a character that is no longer there (groups of goblins)
- Old text left in hidden dialogue boxes, with modern text on (a doorway early in a New Game)
- An enemy turning towards a character whose model is gone (the ogres in the Limestone
  Quarry)
- A sound requested before its sound bank is loaded (the title screen's demo)

**Gameplay**
- The Giant Crab's Aqua Bubble and the Wyvern's Fire Breath had no animation and did no
  damage
- With Merlose in the party, a Ghost could take on her body instead of its own

**Graphics**
- Ghosts' inner bodies drawn in the right order and opacity, as on the PlayStation
- HD textures no longer drop back to the originals in menus, while targeting or during spells
- Broken images in HD texture packs are skipped instead of drawn (the burning manor's
  colours)

**Menus**
- The modern Data screen said "No room on the card" for every slot, so you couldn't save from it

More are being worked on.

## Coming next
- A launcher: pick your disc image, choose settings and packs, play.
- Raised relief across more of Leá Monde.
- The source code release.

## What it is not
No game data is included or will be. You will need your own copy of the game.

## Licences
- **Code:** CC0, like the projects it builds on. The bundled third-party libraries
  (SDL 3, Dear ImGui and others) keep their own licences.
- **Voice recordings** (`voice/`): © 2026 HDRcade, all rights reserved. You may use them,
  unmodified, with VS Reimagined, including in your videos and streams of it. Any other use,
  redistribution, modification or voice training needs written permission. See
  `voice/LICENSE.txt`. The words spoken are from *Vagrant Story* © Square Enix; the licence
  covers only the recordings.
- **Texture and relief pack** (separate download): the reworked 4K textures, normal and
  material maps, masks, height fields and tessellation profiles. © 2026 HDRcade, all rights
  reserved. You may use it, unmodified, with VS Reimagined, including in your videos and
  streams of it.
  Use with other ports or emulators, redistribution, modification or AI training needs
  written permission. See `LICENSE.txt` in `vagrant-story-reimagined-textures` and in every pack
  download. The original artwork is © Square Enix; the licence covers only the work added
  for VS Reimagined.

## Support
VS Reimagined is and will stay free. If you'd like to support my work:
[Patreon](https://patreon.com/HDRcade) · [Ko-fi](https://ko-fi.com/hdrcade)

## Credits
- [rood-reverse](https://github.com/ser-pounce/rood-reverse), the decompilation, started by
  ser-pounce
- rood-boi, noprompt's native PC port
- Daemeous's rood-boi fork and Two's A Riot (Merlose as a companion)
- eremtsov's QoL mod (the quick weapon swap)
