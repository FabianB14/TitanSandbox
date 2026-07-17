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
- **Ragdoll titan** — a 10-part physics ragdoll (torso, head, hinged jaw,
  arms, legs, 3 tail segments) with a balance "muscle" controller: he stands
  upright, stomps toward the nearest building, ragdolls when thrown or
  blasted, then staggers back up.
- **Crumbling buildings** — each building is a grid of individual physics
  bricks joined by breakable constraints; every brick renders its slice of the
  facade (windows, cornices, doorway), so debris looks architectural. Bricks
  char dark when burned. Buildings crumble progressively and never despawn.
- **Tools** — Grab (drag & fling anything), Titan spawn (max 3), Building
  spawn, Bomb (3-second fuse ring, radial blast, screen shake, synthesized
  WebAudio boom), Breath (auto-aimed ember beam: particle stream, cone force,
  joint-melting, charring), Car spawn (he can bite and carry cars in his
  jaws), Reset.
- Works with mouse and touch. No build step, no backend — one static file.

## Running locally

Open `index.html` in a browser (Matter.js loads from cdnjs, so you need
internet access), or serve the folder with any static file server.

## Development

- `main` — default branch, deployed to GitHub Pages on every push via
  `.github/workflows/pages.yml`.
- `fabian-branch` — working branch for development.

## Legal

All art and the creature design are original. The game is inspired by the
kaiju genre generally and contains no third-party characters, names, or
likenesses.
