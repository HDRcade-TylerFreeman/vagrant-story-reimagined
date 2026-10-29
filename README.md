# VS Reimagined

**An unofficial remaster of *Vagrant Story* (Square, 2000) for PC. Vagrant Story Reimagined: Echoes of Leá Monde**

VS Reimagined starts from rood-boi, a native PC port that runs the game's decompiled
code with a modern path-traced renderer, and takes it towards a full remaster:
- new 4K artwork and raised stone relief;
- full voice acting, with Ashley remarking on the world as you play;
- Merlose fighting at Ashley's side;
- modern menus, a Bestiary, a bigger inventory and dozens of quality-of-life options;
- a lantern, embers and other subtle effects lit by the path tracer;
- fixes for crashes found over many hours of streamed playthroughs.

None of this would be possible without the rood-reverse decompilation, rood-boi and
Daemeous's fork: see [Credits and thanks](#credits-and-thanks).

Not affiliated with or endorsed by Square Enix.

**Source code release: coming later.** Follow development on YouTube:
[HDRcade](https://www.youtube.com/@HDRcade)

## What's different

| | PS1 original | rood-boi and Daemeous's fork (what this builds on) | **VS Reimagined** |
|---|---|---|---|
| **Engine** | PlayStation | Native PC code, Vulkan, path-traced lighting, 4K, widescreen | The same, plus [the fixes below](#fixes) for crashes and bugs that show up in a full playthrough |
| **Artwork** | Original textures | Original textures; HD packs supported | **4K reimagined texture pack**: over 2,000 textures, hand-corrected, original faces kept; stays HD through menus, targeting and spells |
| **Scenery** | Flat | Flat | **Raised stone relief** through tessellation, with separate strength for walls, floors and props and an F11 before/after toggle *(spreading to more rooms)* |
| **Voices** | Text only | Text only | **Full voice acting**: over 1,100 lines, plus the narration screens dubbed "Echoes of Leá Monde". **Ashley's remarks**: 143 lines on his Risk, wounds and ailments, new areas, bosses, each key and sigil he finds |
| **Bestiary** | None | None | **A Bestiary tab**: every creature and character you meet, with its lore, stats, weaknesses and a rotating 3D model, each entry read by a narrator |
| **Companion** | None | Merlose joins you (Two's A Riot) | **Merlose in the modern menus**: her gear, her items marked, behaviour modes (Aggressive, Balanced, Healer, No casting, or No action: she just follows and enemies leave her be) |
| **Inventory** | Original limits | Original limits | **Three times the equipment space**; saves stay compatible with the original |
| **Combat** | Original | Quick weapon swap | **Chain assist** toggle, **fast casting** (hold R2), and a **quick menu** (L3) for Merlose's mode, accessories, the lantern, the camera and more |
| **Effects** | Original | Path-traced lighting | **Ashley's lantern**, a path-traced light that casts his shadow; **subtle HD effects**: a Risk aura, embers rising from braziers and hearths, dust in the light. All optional, Remaster mode only |
| **Progress** | None | None | **Achievements** for bosses, keys and sigils, the endings and a complete Bestiary |
| **Options** | None | Graphics and camera options | **Cheats page**: damage multiplier, Never zero, Risk, weapon growth, No wear, Workshop anywhere, Infinite HP, Pause AI, healing at Circles of Magic. Separate music, sound effect and voice volumes |
| **Presentation** | Original | 16:9 option | **Remaster, HD or Original** presentation at a switch. **30, 60 or 120 fps** (30 for frame generation tools). Over-the-shoulder camera. Widescreen with 4:3 kept for cutscenes or menus if you like, your own title screen and intro images, room-start quick reload (F10), HD on/off toggle (F8) |

## Fixes

A native port runs the game's code in ways the PlayStation never did. Some problems only
appear many hours in, so VS Reimagined is tested by playing it through on stream, and every
crash found gets fixed. Fixed so far:

**Crashes**
- Leaving a room after one of the numbered blocks has vanished.
- A character linked to an empty slot, a few frames after entering a room.
- A character standing off the room's floor map.
- An enemy chasing or facing a character that is no longer there.
- Old text left in hidden dialogue boxes, with modern text on.
- An enemy turning towards a character whose model is gone.
- A sound requested before its sound bank is loaded.

**Gameplay**
- The Giant Crab's Aqua Bubble and the Wyvern's Fire Breath had no animation and did no
  damage. Likely fixed other enemies as well.
- With Merlose in the party, a Ghost could take on her body instead of its own.
- Late in a playthrough, potions and grimoires in the modern Items menu could stick on
  "Loading..." and could not be used.

**Graphics**
- Ghosts' inner bodies drawn in the right order and opacity, as on the PlayStation.
- HD textures no longer drop back to the originals in menus, while targeting or during spells.
- Broken images in HD texture packs are skipped instead of drawn (the burning manor's
  colours).
- The idle demo's narration screens left the game showing through at the sides in widescreen.
- A cutscene camera standing against a door (Hardin at the burning manor) showed nothing but
  the door; it now frames him as the PlayStation did.

**Menus**
- The modern Data screen said "No room on the card" for every slot, so you couldn't save from it.

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

## Credits and thanks

VS Reimagined stands on some remarkable work. Please check out and support these projects:

- **[rood-reverse](https://github.com/ser-pounce/rood-reverse)** by
  [ser-pounce](https://github.com/ser-pounce): the decompilation that turned *Vagrant Story* back
  into readable C that rebuilds the original game byte for byte. No native port could exist
  without it. [Lil' Sassy](https://github.com/lil-sassy) is one of its most prolific
  contributors.
- **[rood-boi](https://github.com/noprompt/rood-boi)** by [noprompt](https://github.com/noprompt):
  the native PC port this is built on, and a huge achievement in its own right. Its features
  include:
  - rendering from native meshes on Vulkan, with ray-traced shadows and path-traced lighting;
  - a live lighting editor;
  - the modern menus, widescreen and much more.
- **[Daemeous's rood-boi fork](https://github.com/Daemeous/rood-boi)** by
  [Daemeous](https://github.com/Daemeous): Two's A Riot, which brings Merlose along as your
  companion, plus HD texture pack support and ready-made player builds.
- **[eremtsov's Vagrant Story QoL mod](https://github.com/eremtsov/rood-reverse)**: the quick
  weapon swap.
- **[Andrew Kuhar](https://andrewkuhar.com)**'s
  [Vagrant Story UI Remaster](https://andrewkuhar.com/blog/the-phantom-pain/) design, which
  inspired rood-boi's modern menus.
- **[Kenney](https://kenney.nl)**'s [Input Prompts](https://kenney.nl/assets/input-prompts) for
  the button icons.
