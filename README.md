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
- **Three original kaiju** — each is a single rigid physics body with a
  fully procedural animation rig: legs, arms, tail chain, head, and jaw are
  drawn kinematically (walk cycle, tail sway, head bob, jaw hinge), so poses
  always look deliberate. They stomp toward the nearest building, tumble as
  one piece when thrown or blasted, and right themselves like a toy.
  - **Titan** — charcoal theropod with ember-glowing bone fins and a fire
    breath.
  - **Goliath** — a giant fur-textured ape with long heavy arms and a
    concussive roar that blasts buildings apart with shockwaves.
  - **Ravok** — a moss-green horned saurian with crimson-glowing fins and a
    searing crimson breath.
- **Crumbling buildings** — each building is a grid of individual physics
  bricks joined by breakable constraints; every brick renders its slice of the
  facade (windows, cornices, doorway), so debris looks architectural. Bricks
  char dark when burned. Buildings crumble progressively and never despawn.
- **Tools** — Grab (drag & fling anything), three kaiju spawners (max 3 on
  screen), Building spawn, Bomb (3-second fuse ring, radial blast, screen
  shake, synthesized WebAudio boom), **A-Bomb** (falling warhead, screen-white
  flash, mushroom cloud, city-levelling blast radius), Breath/Roar (auto-aimed
  at the nearest block), Car spawn (kaiju bite and carry cars in their jaws),
  Reset.
- Works with mouse and touch. No build step, no backend — one static file.

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
