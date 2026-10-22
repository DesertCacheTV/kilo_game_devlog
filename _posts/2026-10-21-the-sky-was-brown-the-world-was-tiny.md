---
layout: post
title: "The Sky Was Brown, the World Was Tiny"
date: 2026-10-21 23:00:00
tags: [devlog, lighting, terrain, flowers]
image: /assets/img/kilo-sky-fixed.jpg
image_alt: "A big red barn and a pickle jar under a blue sky with soft white clouds, seen through tree branches."
---
**TL;DR:** The sky was wearing the ground's paint, and the faraway hills were squashed to a quarter of their size. Both are fixed now. The light is warmer, the air is clearer, and Kilo Man briefly ended up underneath his own trail.
{: .tldr}

Today was a day of "oh, *that's* why it looked weird" moments. Those are the good ones.

## The sky was brown {% include status.html s="Fixed" %}

The sky looked off for days. It was tan. Kind of brown. Not very morning.

Then we dug through our own change history and found it. When we added the hills, the paint for the *ground* ended up on the big sky ball by mistake. The sky was literally wearing the ground's clothes.

We put the real sky back. Blue, with soft clouds. Much better.

{% include figure.html src="/assets/img/kilo-sky-fixed.jpg" alt="A big red barn and a pickle jar under a blue sky with soft white clouds, seen through tree branches." caption="The right sky, back where it belongs." width="1251" height="670" %}

## Warmer light, clearer air {% include status.html s="Working" %}

We made the sun a little warmer, like early morning light. We also thinned the fog, so you can see the jar and the barn from far down the trail.

I ran through it myself. It looks much more real. Everything feels like a morning in a giant garden.

{% include figure.html src="/assets/img/kilo-track-clear-air.jpg" alt="A pickle jar in front of red barn doors in warm light, seen from ground level." caption="The jar from ground level. Warmer sun, thinner fog." width="1251" height="670" %}

## The faraway hills were squashed {% include status.html s="In progress" %}

The hills and mountains behind the trail had been squashed to a quarter of the size they were designed to be. The flat strip of ground along the trail ended way too early. After that, the trail was running *inside* a hill.

We set the hills back to their full size. It's a big change. The world finally looks like a giant place, seen from a very small hero.

{% include figure.html src="/assets/img/kilo-terrain-too-small.jpg" alt="A small island of hills under a tan sky, seen from far above." caption="Before: a small island under a brown sky." width="1251" height="670" %}

{% include figure.html src="/assets/img/kilo-terrain-full-size.jpg" alt="A wide bowl of hills and mountains with the barn and big trees in the middle." caption="After: a wide bowl of hills, with the barn in the middle. (Seen from way up, outside the sky.)" width="1251" height="670" %}

## Blooper of the day

We also lowered the ground well below the trail, so that falling off really feels like a fall. Then, in one test, Kilo Man ended up on the ground *under* the trail. He looked up, and there it was: the trail, hanging in the air like a long plank of grass.

It's a rare look at how the trail is built a few pieces at a time. We think he fell off, then wandered around afterwards. We'll check. For now, enjoy the view.

{% include figure.html src="/assets/img/kilo-hero-under-the-path.jpg" alt="Looking up from the ground at the dirt trail hanging in the air, with a giant wheelbarrow and a red barn beside it." caption="Kilo Man's-eye view of his own trail." width="1251" height="769" %}

## Flowers, on a slider {% include status.html s="In progress" %}

We're making a flower patch that grows as you drag a slider. More slider, more flowers. We want to scatter them in the faraway background.

It works in the editor. But when we stretch it, the flowers float in the air or vanish. So that's the bug we're chasing next.

## Still cooking

- **A rounder, earthier trail.** The path pieces should feel like a dug-out dirt groove, with a rounded half-pipe shape.
- **A part-by-part art pass.** Leaves, trunks, petals, stalks, roots and pebbles, each one looked at on its own, so they all share one style.
- **A fog dial.** A simple control so we can tune the fog by hand.

*Kilo Man Jar-O is a working title. Everything shown is work in progress.*
