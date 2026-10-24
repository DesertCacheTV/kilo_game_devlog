---
layout: page
title: Tools
permalink: /tools/
---

**TL;DR:** Not everything I build goes in the game. These are the little helper tools I make so that building the game takes less remembering and more making.
{: .tldr}

## Kilo Session

**Status: Working.** Used for a real game session on 2026-10-23.

Kilo Session is a small window that sits on my second screen. It does two jobs: getting a work session started, and closing one out properly at the end of the night.

### Why I needed it

Every time I sat down to work on Kilo Man Jar-O, I did the same warm-up from memory:

- open the game editor and wait for it to finish loading,
- open my AI helper,
- remind it of the project's rules, where we left off, and what I wanted to do tonight.

And at the end of the night there were three wrap-up jobs that only work in the right order: write down what we did, save a checkpoint of the project, then write the devlog post. When I got the order wrong, this devlog quietly ended up **a session behind**, because the post can only see work that has been saved.

Lots of small steps, every single time. Easy to forget one. So I made a button for it.

{% include figure.html src="/assets/img/kilo-session-window.webp" width="704" height="1140" alt="The Kilo Session window: a dark green panel with a status list of green and yellow dots, a 'Tonight I want to' box, a big green Start Session button, and three End of night buttons numbered Handoff, Checkpoint and Run devlog, all ticked off." caption="The real window after a session. Some private lines are blurred." %}

### How a session flows

<figure class="shot">
<svg viewBox="0 0 420 760" role="img" aria-labelledby="ks-flow-title ks-flow-desc" style="display:block;width:100%;max-width:440px;margin:0 auto;font-family:var(--sans)">
  <title id="ks-flow-title">How a Kilo Session flows</title>
  <desc id="ks-flow-desc">Start: click Start Session, the editor opens, the window waits until the editor is ready, the AI helper opens, the start note is copied in, and the work happens. End of night: 1 Handoff writes down what we did, 2 Checkpoint saves the project, 3 Run devlog drafts the post from the saved work, then I approve it and it goes live.</desc>
  <style>
    .ks-box { fill: var(--card); stroke: var(--ink); stroke-width: 2; }
    .ks-go { fill: #B3CF73; stroke: var(--ink); stroke-width: 2; }
    .ks-end { fill: var(--sun); stroke: var(--ink); stroke-width: 2; }
    .ks-t { fill: var(--ink); font-size: 16px; }
    .ks-dark { fill: #10140c; font-size: 16px; font-weight: 600; }
    .ks-head { fill: var(--loam-soft); font-size: 13px; letter-spacing: .08em; font-weight: 600; }
    .ks-line { stroke: var(--loam-soft); stroke-width: 2; fill: none; marker-end: url(#ks-arrow); }
    .ks-work { fill: var(--leaf-wash); stroke: var(--ink); stroke-width: 2; stroke-dasharray: 6 5; }
  </style>
  <defs><marker id="ks-arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" fill="var(--loam-soft)"/></marker></defs>
  <text class="ks-head" x="20" y="24">START OF SESSION</text>
  <rect class="ks-go" x="20" y="36" width="380" height="48" rx="10"/>
  <text class="ks-dark" x="210" y="66" text-anchor="middle">▶ Click Start Session</text>
  <path class="ks-line" d="M210 84 V104"/>
  <rect class="ks-box" x="20" y="106" width="380" height="44" rx="10"/>
  <text class="ks-t" x="210" y="134" text-anchor="middle">The game editor opens</text>
  <path class="ks-line" d="M210 150 V170"/>
  <rect class="ks-box" x="20" y="172" width="380" height="44" rx="10"/>
  <text class="ks-t" x="210" y="200" text-anchor="middle">Wait until the editor is really ready</text>
  <path class="ks-line" d="M210 216 V236"/>
  <rect class="ks-box" x="20" y="238" width="380" height="44" rx="10"/>
  <text class="ks-t" x="210" y="266" text-anchor="middle">Then the AI helper opens</text>
  <path class="ks-line" d="M210 282 V302"/>
  <rect class="ks-box" x="20" y="304" width="380" height="44" rx="10"/>
  <text class="ks-t" x="210" y="332" text-anchor="middle">Start note copied: paste, go</text>
  <path class="ks-line" d="M210 348 V368"/>
  <rect class="ks-work" x="20" y="370" width="380" height="56" rx="10"/>
  <text class="ks-t" x="210" y="404" text-anchor="middle" font-weight="600">Make the game</text>
  <path class="ks-line" d="M210 426 V456"/>
  <text class="ks-head" x="20" y="452">END OF NIGHT</text>
  <rect class="ks-end" x="20" y="464" width="380" height="52" rx="10"/>
  <text class="ks-dark" x="40" y="487">1  Handoff</text>
  <text class="ks-dark" x="40" y="507" style="font-weight:400;font-size:14px">write down what we did and what's next</text>
  <path class="ks-line" d="M210 516 V536"/>
  <rect class="ks-end" x="20" y="538" width="380" height="52" rx="10"/>
  <text class="ks-dark" x="40" y="561">2  Checkpoint</text>
  <text class="ks-dark" x="40" y="581" style="font-weight:400;font-size:14px">save the project so it can't be lost</text>
  <path class="ks-line" d="M210 590 V610"/>
  <rect class="ks-end" x="20" y="612" width="380" height="52" rx="10"/>
  <text class="ks-dark" x="40" y="635">3  Run devlog</text>
  <text class="ks-dark" x="40" y="655" style="font-weight:400;font-size:14px">draft the post from the saved work</text>
  <path class="ks-line" d="M210 664 V684"/>
  <rect class="ks-go" x="20" y="686" width="380" height="48" rx="10"/>
  <text class="ks-dark" x="210" y="716" text-anchor="middle">I say yes → it goes live here</text>
</svg>
<figcaption>Every step is one click. The window copies the right note for each step, and I paste it into the AI helper.</figcaption>
</figure>

### What the window shows

The top of the window is a status board that keeps itself up to date:

- **Green** means ready: the editor is open, its tools are answering, my helper is open, the last checkpoint is saved, and the devlog is caught up.
- **Yellow** means "look at this": unsaved work, an empty plan, or a devlog that's behind.
- **Red** means something's actually wrong, like the editor being open but not answering.

Under that, a box asks what I want to do tonight. Whatever I type goes straight into the start note, so the session begins with a plan instead of "so... where were we?"

### Why the order matters

<figure class="shot">
<svg viewBox="0 0 400 300" role="img" aria-labelledby="ks-order-title ks-order-desc" style="display:block;width:100%;max-width:460px;margin:0 auto;font-family:var(--sans)">
  <title id="ks-order-title">Why checkpoint comes before devlog</title>
  <desc id="ks-order-desc">Right order: tonight's work is saved in a checkpoint, then the devlog reads it, so the post includes tonight. Wrong order: the devlog runs before tonight's work is saved, so it only sees last time's work and the post ends up one session behind.</desc>
  <style>
    .ko-h { fill: var(--ink); font-size: 17px; font-weight: 600; }
    .ko-dim { fill: var(--loam-soft); font-size: 14px; }
    .ko-saved { fill: #B3CF73; stroke: var(--ink); stroke-width: 2; }
    .ko-read { fill: var(--sun); stroke: var(--ink); stroke-width: 2; }
    .ko-unsaved { fill: var(--card); stroke: var(--ink); stroke-width: 2; stroke-dasharray: 5 4; }
    .ko-track { stroke: var(--loam-soft); stroke-width: 3; }
    .ko-good { fill: var(--pickle); font-size: 16px; font-weight: 600; }
    .ko-bad { fill: var(--barn); font-size: 16px; font-weight: 600; }
  </style>
  <text class="ko-h" x="10" y="22">Right order: checkpoint, then devlog</text>
  <line class="ko-track" x1="30" y1="56" x2="370" y2="56"/>
  <circle class="ko-saved" cx="55" cy="56" r="14"/><text class="ko-dim" x="55" y="92" text-anchor="middle">last night</text>
  <circle class="ko-saved" cx="200" cy="56" r="14"/><text class="ko-dim" x="200" y="92" text-anchor="middle">tonight (saved)</text>
  <circle class="ko-read" cx="340" cy="56" r="18"/><text class="ko-dim" x="340" y="92" text-anchor="middle">devlog reads</text>
  <text class="ko-good" x="10" y="122">✓ The post includes tonight.</text>
  <text class="ko-h" x="10" y="176">Wrong order: devlog, then checkpoint</text>
  <line class="ko-track" x1="30" y1="210" x2="370" y2="210"/>
  <circle class="ko-saved" cx="55" cy="210" r="14"/><text class="ko-dim" x="55" y="246" text-anchor="middle">last night</text>
  <circle class="ko-read" cx="170" cy="210" r="18"/><text class="ko-dim" x="170" y="246" text-anchor="middle">devlog reads</text>
  <circle class="ko-unsaved" cx="320" cy="210" r="14"/><text class="ko-dim" x="320" y="246" text-anchor="middle">tonight (unsaved)</text>
  <text class="ko-bad" x="10" y="276">✗ The post is a night behind.</text>
</svg>
<figcaption>The devlog only reads saved checkpoints. That's why the End of night buttons are numbered.</figcaption>
</figure>

### Blooper of the day

On its very first real run, every light in the window was green, and my AI helper still swore the editor wasn't there. The helper had tried to connect earlier, before the editor was ready, gave up, and never tried again. Now the window opens the editor first, **waits until it's really ready**, and only then opens the helper. If the helper was already open, the window tells me to restart it.

Runner-up: the first version's text was so tiny I could barely read it. It now has **A−** and **A+** buttons and remembers my size.

### What I learned

- "Is the program open?" and "is the program ready?" are two different questions. The window now asks both.
- The best fix for forgetting steps is to stop needing to remember them.
- A tool for making the game is still a tool I play-test. It counts as working because I used it for a real session, not because it looked right on paper.

*Kilo Man Jar-O is a working title. Everything shown is work in progress.*
