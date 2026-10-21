---
layout: post
title: "How the Trail Builds Itself"
date: 2026-10-21 09:00:00
tags: [devlog, tech, level-design]
---
**TL;DR:** Kilo Man's trail isn't built by hand. Each level is a little recipe, and the game snaps the trail together from a kit of pieces, building just ahead of you and tidying up behind.
{: .tldr}

Here's a peek behind the grass at how the levels actually work.

## A kit of trail pieces

Instead of placing every bit of path by hand, Kilo Man Jar-O has a **kit of trail pieces**, kind of like model train track. Right now the Backyard kit has:

- **Ant trail:** a narrow dirt path, about 1.2 m wide, walled in by towering blades of grass.
- **Twigs:** the same trail with twigs across it to hop over.
- **Vista:** a raised stretch where the grass gets short, so you can stop and see how huge everything is.
- **Straight** and **bridge** pieces from the very first version of the game.

Every piece has the same kind of "plug" at each end, so any piece can snap onto any other. Each one also carries a few simple notes: how long it is, how often it should show up, and how far into a run it's allowed to appear. That's how some pieces get kept out of the very start of a run.

## Each level is a recipe

A level isn't a big hand-made map. It's a short recipe that says:

- which **biome** to use (right now that's the Backyard),
- **how long** the trail is (the prototype is about 690 m),
- **how often** to give you a breather vista,
- and a **seed number**.

The seed is the secret ingredient. The same seed always builds the same trail, so a level stays the same every time you play it, and you can learn its twists and get faster. Change the number and you get a whole new trail from the same pieces. It's a tiny tool that makes a lot of garden.

{% include figure.html src="/assets/img/trail-builder-diagram.svg" width="1200" height="380" alt="A diagram of the trail as a row of pieces: straight, twigs, bridge and vista, snapped end to end. Kilo Man stands on one piece. The pieces about 72 meters ahead of him are built, and pieces 36 meters behind him have been cleared away." caption="The trail is built a few pieces at a time, right where Kilo Man needs it." %}

## Only building what you can see

Here's the part I'm proudest of. The game doesn't build the whole trail at once. While you run, it:

- builds the pieces **about 72 m ahead** of you,
- clears away pieces once they're **36 m behind** you,
- and checks about **five times a second**.

So at any moment, only a short stretch of trail actually exists. That keeps the game light, which matters a lot because it's being built on a laptop with integrated graphics. If it runs well there, it should run well on most PCs.

When you fall and hit Retry, the builder resets and rebuilds the start of the trail right away, so you're back running in under two seconds.

## What's still cooking

- **Forks in the road:** pieces with two exits, so you can pick your own route.
- **Trap doors and tunnels:** drop below the garden, then take a ramp back up.
- **More biomes,** each with its own kit of pieces.

The game already has names set aside for the underground pieces, but none of them are built yet. More screenshots of the trail pieces are coming soon.

Big gardens get built one small piece at a time. Turns out the same goes for trails.

*Kilo Man Jar-O is a working title. Everything shown is work in progress.*
