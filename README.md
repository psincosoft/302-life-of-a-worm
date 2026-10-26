# 302: Life of a Worm

A simulation of *C. elegans* on the MEGA65.

Up to 32 animals live in a dish. Each runs its own nervous system: the 302 neurons and the
6,107 connections of the real worm, mapped neuron by neuron (Cook et al. 2019). Backing away
from a touch comes from that wiring, not from a rule. Their lives follow published biology,
only 600 to 5,600 times faster than in a lab dish at 20 °C. The predators, *Pristionchus
pacificus*, run the head wiring mapped in their own species (Cook et al. 2025).

A simulation with a little game added: you choose the dish and its warmth, feed, lay eggs of
five strains, touch the animals, bleach the dish and keep a lab notebook. The pages in the
program say what is real and what is simplified.

## Run

Needs a MEGA65.

1. Download `302.D81` from the [latest release](https://github.com/psincosoft/302-life-of-a-worm/releases/latest)
   and copy it to the SD card.
2. `MOUNT "302.D81"`
3. `LOAD"*",8,1`, then `RUN`

On the title, SPACE or fire opens the dish chooser; I or H opens the instructions.

## What is in it

- Ten dishes, from the round dish to mazes; warmth from 15 to 25 °C; a feeder with five levels.
- Five strains of worm: N2, him-5, daf-2, mec-4 and fog-2. Mating, dauers, ageing, and a
  predator that bites.
- A panel showing the selected animal's neurons and muscles as they fire, and a lab notebook
  with the population over the last 64 days.
- Two engines in 6502 machine code, one for the dish's life and every nervous system, one for
  the drawing; BASIC 65 around them; attic RAM for the pages, the dishes and the predators'
  wiring. With a full dish the MEGA65 computes 9,664 neurons.

## Tested on

A MEGA65 (R6A) in PAL, core 890-sdcard-native build #32, ROM 920422. The program handles NTSC,
but it has not been tested there.

## Credits

302: Life of a Worm 1.0, 2026, by Dawid Blachowski, with Claude, Anthropic's AI.
psinco. A Software Atelier from Luxembourg.

- The worms' wiring: Cook et al. 2019, *Whole-animal connectomes of both Caenorhabditis
  elegans sexes*, Nature 571: 63–71, read with OpenWorm's
  [C. elegans Connectome Toolbox](https://github.com/openworm/ConnectomeToolbox) (MIT).
- Their transmitters: Wang et al. 2024, eLife 95402.
- The signs of their synapses: predicted with
  [WormNeuroAtlas](https://github.com/francescorandi/wormneuroatlas) by Francesco Randi
  (GPL 3 or later); only its predictions are used.
- The predators' head wiring: Cook et al. 2025, Science,
  [doi:10.1126/science.adx2143](https://doi.org/10.1126/science.adx2143); synapse tables from
  [the authors' repository](https://github.com/stevenjcook/cook_et_al_2024_pristionchus) (MIT).
- The logo's font: Poppins Bold (Indian Type Foundry), SIL Open Font License 1.1.

## Terms

302: Life of a Worm is free. You may download it, play it, show it, film it, and share the
disk image unchanged and free of charge. It is not for sale. See [LICENSE](LICENSE).

The disk includes data from third parties under the MIT licence; their notices are in
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt) and on the disk (`TYPE "LICENCES"`).
