---
layout: post
title: "A 10 cm Hero, a Mountain of Pickles, and 15 Hours of Building"
date: 2026-10-20
tags: [devlog, origin]
---

**TL;DR:** Kilo went from a blank project to a playable run (a tiny hero, an ant trail and a pickle jar at the finish) in under 15 hours.

Hi! Welcome to the first devlog for **Kilo** (working title).

## The idea

Kilo is about a tiny hero. He's 10 centimeters tall and weighs about a kilogram, and he runs through a giant garden toward a pickle jar the size of a mountain. Blades of grass tower like trees. Pebbles are boulders. A barn on the horizon is over a kilometer wide from where he stands. The goal is a game that feels calm and full of wonder, even while you're dodging flying pickles.

## How it plays

You run, jump and climb your way along a winding trail. You read what's ahead and pick your route: the main path, a side branch, or eventually a trap door into the tunnels underneath. A run to the jar takes about three minutes, and if you fall off, you're back at the start in under two seconds to try again.

## How it's being made

This is a small project with an unusual crew. I'm the designer and play-tester, and I make the final call on everything. Alongside me are two AI helpers. One of them works directly inside Unreal Engine 5.8, building Blueprints, materials and level pieces. The other plans each step, checks the work, keeps the project's history safe, and measures performance. While I'm at my day job, it keeps working and pings my phone whenever it needs a human decision. (More on that in [How Kilo is made]({{ "/how-kilo-is-made/" | relative_url }}).)

## What we've built so far

All of this happened in under 15 hours, starting from a blank project:

- **The hero.** A properly tiny character with his own camera and movement tuning. After a few rounds of tweaks, my note was simply: "feels really good."
- **A level builder.** Instead of hand-placing every piece of track, levels are assembled from a kit of segments: straightaways, bridges, vistas and hazard lanes. That means new levels can be tested quickly.
- **The Backyard: an ant trail.** The first biome is a narrow dirt trail with twigs and logs to hop over, plus wide-open "vista" stretches where you can stop and take in how huge everything is.
- **The full run loop.** Countdown, distance counter, finishing at the jar, failing by falling off, a results screen, and a near-instant retry.
- **A morning sky.** A low golden sun, drifting clouds, softened fog, and a big red barn in the distance.
- **Safety nets.** Every change is saved as a checkpoint, so if something breaks, we roll back instead of patching on top of a mess.

## Honest corner

I'm building on a laptop with integrated graphics, on purpose. If Kilo runs well here, it should run well on most people's PCs. Right now it doesn't hit that bar yet at max settings, and a performance pass is on the list.

## Next up

- Getting hurt and the retry screen
- **Underground tunnels** lit only by glowing mushrooms, a glowing worm guiding the way, and shafts of sunlight through holes in the ground
- Something to run *away* from
- Rain
- Better faraway scenery
- A storm that rolls in during your run (it works on paper, but not on screen yet)

Thanks for following along. There's a lot more pickle to come.

*Kilo is a working title. Everything shown is work in progress.*
