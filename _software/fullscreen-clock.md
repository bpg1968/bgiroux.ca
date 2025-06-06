---
title: Fullscreen Clock
date: 2025-06-05
description: A fullscreen digital clock for Linux, written in C using SDL2, with date display and mirrored reflection mode for a unique real-world use case.
prog_lang: C
summary: A fullscreen digital clock for Linux with date display and optional mirror mode — built in C with SDL2 for a clean, minimalist experience.
labels: [clock, sdl2, linux, c, fullscreen]
layout: software
language: en-CA
github: https://github.com/bpg1968/Fullscreen-Clock
---

This project was inspired by Nayuki’s excellent
[Full screen clock](https://www.nayuki.io/page/full-screen-clock-javascript)
written in JavaScript.
I used that version for a long time,
but eventually I wanted to tweak a few things
—
like adding the date below the time
and flipping the screen to show a mirror image.

So, I wrote my own fullscreen clock in JavaScript,
using Nayuki’s as a reference and starting point.

That version worked well,
but I was never quite satisfied with the fact that
it had to run in a browser window.
I wanted a **standalone desktop application**
—
clean, minimal, and fullscreen with no window decorations.
So I rewrote it in C, with the help of AI,
using the [SDL2](https://www.libsdl.org/) library.
I'm quite happy with the result.

## Features

* **Fullscreen with no window decorations
  (no border, title bar, or close button):**
  Ideal for distraction-free display.
* **Large, clear time display:** Uses 24-hour format (HH:MM).
* **Date display below the time:** e.g., "Saturday, April 5".
* **Mirror mode:** Press `[Space]` to flip the screen horizontally.
* **Quit easily:**
  Press `[Esc]` or `[Q]` to exit
  (important since the window has no close button).

## Why Mirror Mode?

When I’m relaxing in my recliner,
I often set my laptop on a table beside me.
From that angle,
I can see the screen’s reflection
in the glass doors of the cabinet below the TV.

By flipping the clock display into mirror mode,
I can **read the time clearly in that reflection**.
It’s a quirky but genuinely useful feature — and one I use often.

## Input Lag (and why it happens)

The clock updates once per second.
After drawing the time and date,
the program calls `SDL_Delay(1000)`,
which **pauses execution for one second** to reduce CPU usage.
This means it also only checks for keyboard input once per second
—
which can make it feel slightly unresponsive when you press a key.

