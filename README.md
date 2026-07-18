# Titan Sandbox

A 2D kaiju physics sandbox in a single HTML file. An original titan — a
charcoal-hided theropod with ember-glowing bone fins — stomps through a hazy
old city of crumbling masonry. Grab him, fling him, blow things up, torch
buildings with his breath.

**Play it:** https://fabianb14.github.io/TitanSandbox/

## Features

- **Painted-sprite art, 100% generated in code** — every sprite (titan body
  parts, building facades, cars, sky, parallax skyline, lattice tower) is
  rendered to offscreen canvases at load time with layered gradients, speckle
  noise, and glow. No image files.
- **Seven original kaiju** — each is a single rigid physics body with a
  fully procedural animation rig: legs, arms, tail chain, head, and jaw are
  drawn kinematically (walk cycle, tail sway, head bob, jaw hinge), so poses
  always look deliberate. They stomp toward the nearest building, tumble as
  one piece when thrown or blasted, and right themselves like a toy.
  - **Titan** — charcoal theropod with ember-glowing bone fins and a fire
    breath.
  - **Goliath** — a giant fur-textured ape with long heavy arms and a
    concussive roar that blasts buildings apart with shockwaves.
  - **Ravok** — a giant horned serpent: cobra-raised forebody, flared hood,
    crimson-glowing spine fins, and a corrosive venom spit that arcs and
    melts masonry.
  - **Scorn** — a grotesque mutant saurian: near-black gnarled hide split by
    glowing magma fissures, oversized craggy fins, chaotic teeth, tiny
    withered arms, a huge tail, and a violet atomic beam. Keening screech.
  - **Meka** — a giant robot kaiju: riveted gunmetal armor with panel lines,
    a glowing reactor core, visor eye, beacon antenna, angular metal fins,
    and a cyan laser. Klaxon roar.
  - **Hydrax** (store unlock) — a golden three-headed dragon with wings and
    forked lightning that slams around its target. Cackling triple screech.
  - **Vanguard** (store unlock) — a hero mech in white armor with a gold
    V-crest, red intakes, and a rapid plasma rifle.
- **Ultimates** — every kaiju has a signature super-attack on a 25s
  cooldown (Ultimate tool, also used by the AI in fights): Overcharge Beam,
  Seismic Slam, Venom Deluge, Meltdown Nova, Sweep Laser, Skyfall Storm,
  and Missile Barrage.
- **Deployable military** — Tank, Heli, Jet Strike, and Ship tools let you
  drop the army in wherever you tap, alongside the automatic defense waves.
- **Coins & store** — earn coins for crushing buildings, clearing levels,
  winning kaiju fights, wrecking the military, and popping cars; spend them
  in the in-game store to unlock Hydrax and Vanguard (saved on-device).
- **Warships** — on water levels destroyers cruise the bay and shell the
  kaiju alongside the tanks, helicopters, and jets. Cars explode from hard
  impacts, blasts, and beam fire — with chain reactions.
- **Fight mode & HP** — hit Fight and the kaiju brawl: claw strikes,
  knockback, and ability duels. Every kaiju has 100 HP; explosions, beams,
  venom, hard impacts, and the military all deal damage. At zero HP they
  collapse, smoke, and fade away. Distinct roars per species (saurian
  bellow, ape grunts, serpent hiss).
- **The military fights back** — from level 2 onward tanks roll in and shell
  the kaiju, attack helicopters strafe with rockets, and jets scream past
  dropping bombs. All of them can be crushed, torched, swatted, or blown up.
- **Wild kaiju** — higher levels sometimes open with a hostile wild kaiju
  that attacks yours on sight; extra buildings appear with each cycle.
- **Crumbling buildings** — each building is a grid of individual physics
  bricks joined by breakable constraints; every brick renders its slice of the
  facade (windows, cornices, doorway), so debris looks architectural. Bricks
  char dark when burned, and settled rubble fades away to keep the streets
  clear.
- **Six levels** — Outskirts, Old Town, Downtown Dusk, Midnight Harbor
  (stars, moon, lit windows), Metropolis Dawn, and Open Bay — a waterfront
  level with buoyant water, splashes, and boats. Level the whole city and
  the next level rolls in automatically, growing harder each cycle.
- **Title screen & UI** — start menu with Start/Exit, collapsible scrolling
  tool panel, a top-right quick bar (Auto rampage, Fight, Store, Menu), and
  an attacker highlight: with Attack/Ultimate selected, the kaiju that will
  fire is marked with a pulsing ring and chevron in its beam color.
- **Auto rampage** — toggle Auto and your kaiju level the city themselves,
  mixing breath attacks and ultimates, clearing level after level.
- **Custom sprites (optional)** — drop PNGs into a `sprites/` folder named
  `<species>_<part>.png` (species: titan, ape, drax, scorn, mecha, hydrax,
  vang; parts: torso, head, jaw, arm, leg, tail0-2, wings) and the game
  swaps them in over the generated art at load, inheriting the animation
  rig. Only ship art you have the rights to.
- **Kaiju Forge** — the companion sprite studio at
  https://fabianb14.github.io/kaiju-forge/ ([repo](https://github.com/FabianB14/kaiju-forge))
  lets you paint or AI-generate parts on game-matched canvases, preview
  them on the live animation rig, and send them straight into the game
  with one tap (shared browser storage — both sites live on the same
  domain). It can also export a `sprites.zip` for the folder method above.
- **Tools** — Grab (drag & fling anything), three kaiju spawners (max 3 on
  screen), Building spawn, Bomb (3-second fuse ring, radial blast, screen
  shake, synthesized WebAudio boom), **A-Bomb** (falling warhead, screen-white
  flash, mushroom cloud, city-levelling blast radius), Breath/Roar (auto-aimed
  at the nearest block), Car spawn (kaiju bite and carry cars in their jaws),
  Reset. The breath is aimed: tap where you want the beam and hold-drag to
  sweep it. The Titan fires an atomic-blue beam, Ravok a crimson one, and
  Goliath a concussive shockwave roar.
- Works with mouse and touch, sized for tablets, and installable as an app
  (PWA manifest + service worker — open the site and use "Add to Home
  Screen" / the install prompt; it also works offline after the first
  visit).

## Running locally

Open `index.html` in a browser (Matter.js loads from cdnjs, so you need
internet access), or serve the folder with any static file server.

## Development

- `main` — default branch, deployed to GitHub Pages on every push via
  `.github/workflows/pages.yml`.
- `fabian-branch` — working branch for development.

## Legal

All art and all three creature designs are original. The game is inspired by
the kaiju genre generally (giant saurians, giant apes) and contains no
third-party characters, names, or likenesses.
