---
title: "Conway's Game of Life (Java)"
description: "A Java Swing-based simulation of Conway’s Game of Life, built with a clean MVC structure — and a little help from AI."
date: 2025-04-27
categories: [java]
tags: [java, swing, mvc, game-of-life, cellular-automata]
---

# Conway's Game of Life (Java)

Like many Computer Science students, I was once assigned a **Conway’s Game of Life** project during my studies. It’s a common assignment in programming courses because it combines simple rules with surprisingly complex and emergent behaviour — an excellent exercise in modelling logic, state management, and algorithmic thinking.

However, the project you see here is **not** the one I submitted back then.  
This version was created many years later — mostly for fun — and with the help of AI.

I built it as a way to:
- Brush up on the **Model-View-Controller (MVC)** architecture, which I wanted to understand more deeply in practice.
- Reacquaint myself with **Java Swing**, a library I hadn't touched in years (and, truth be told, I’ve always preferred writing the "guts" of a project over designing graphical interfaces).
- Experiment with how well AI could assist in coding — and I must say, I was impressed by how effective it was.

## Features

- **Graphical Visualization:** Displays a grid of cells using Java Swing, with black for "alive" and white for "dead."
- **MVC Architecture:** Separates the core logic, user interface, and control flow cleanly for better organization.
- **Randomized Start:** Each simulation begins with a randomized grid, evolving according to Conway’s rules.
- **Adjustable Speed:** Easily tweak the simulation speed through Swing’s built-in **Timer**.

## How It Works

The Game of Life operates based on a few simple rules:

- A live cell with two or three live neighbours survives.
- A live cell with fewer than two live neighbours dies (underpopulation).
- A live cell with more than three live neighbours dies (overpopulation).
- A dead cell with exactly three live neighbours becomes alive (reproduction).

Although the rules are simple, the patterns that emerge over time can be fascinatingly complex and often surprising.

