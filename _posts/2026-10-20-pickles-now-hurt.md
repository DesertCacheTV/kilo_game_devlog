---
layout: post
title: "Ouch! Pickles Now Hurt (and the World Got Bigger)"
date: 2026-10-20 23:00:00
tags: [devlog, combat, terrain]
image: /assets/img/kilo-wheelbarrow-barn.webp
image_alt: "A low view of a wooden wheelbarrow full of giant pickles in front of a red barn."
---
**TL;DR:** Kilo Man can get hurt now. Three pickle hits and the run is over. Behind the trail, a whole landscape of hills and mountains is starting to take shape.
{: .tldr}

## Three hits and you're pickled

Until today, the only way to lose was to fall off the trail. Now the garden fights back a little.

- **Kilo Man has 3 HP**, shown in the top corner of the screen.
- **Each pickle hit costs 1 HP**, with a squish and a small "oof".
- **At zero, the run ends** on the same results screen as falling off, and Retry puts you back at full health.
- **The pickle shooters stop** as soon as the run ends, so nothing pelts you on the results screen.

All of that has been play-tested. The squish and "oof" sounds are placeholders for now, and real ones come later.

{% include figure.html src="/assets/img/kilo-hp-tall-grass.webp" width="1280" height="710" loading="eager" alt="Kilo Man, seen from behind, walking down a path between towering blades of grass toward a giant glowing pickle jar. The screen shows HP 3/3 in the top left and 610.8 m at the top." caption="The new HP readout in the top left, deep in the tall grass. The number at the top is how far you've run." %}

## Pickles on the back burner

Here's a lesson from play-testing: the flying pickles were too small and too fast to dodge. Getting hit by something you can't react to doesn't feel fair. It just feels random.

So the pickle shooters are switched off for now (not deleted). A different hazard is planned, something you can see coming and actually outrun.

{% include figure.html src="/assets/img/kilo-hp-wheelbarrow.webp" width="1280" height="630" alt="Kilo Man standing on a brown tiled path, facing a huge wooden wheelbarrow loaded with pickles, with grass growing through it. A red barn and sandy hills are behind, and HP 3/3 shows in the top left." caption="A wheelbarrow of pickles parked by the barn. From 10 cm up, it's the size of a house." %}

## A bigger world behind the trail

The garden needed a horizon, so tonight we started on an **8 km background landscape**. It stays flat under the track, rolls into hills, and ends in a ring of mountains.

It's made with a small homemade tool. You paint a rough greyscale sketch, where black means flat, grey means hills and white means mountains, and the tool turns it into terrain. The track always stays flat, so the hills never poke up through your path.

To keep it light on modest PCs, the landscape doesn't use any texture images. Its colors blend from grass to rock to snow based on how steep the ground is.

**Honest corner:** the landscape's position was corrected tonight, but I haven't fully play-checked it yet. Treat it as "still cooking".

{% include figure.html src="/assets/img/kilo-background-landscape.webp" width="1280" height="712" alt="An editor view along the trail: little cone trees and grey rocks line the track, with the pickle wheelbarrow, the giant jar and the red barn ahead. A bumpy sandy ridge rises behind them, outlined in orange." caption="The new background landscape rising behind the track. It's outlined in orange because it's selected in the editor." %}

## Next up

- Sculpting the landscape by hand in the editor
- A new hazard to replace the flying pickles
- More terrain work, plus a few other changes

Thanks for following along. Mind the pickles.

*Kilo Man Jar-O is a working title. Everything shown is work in progress.*
