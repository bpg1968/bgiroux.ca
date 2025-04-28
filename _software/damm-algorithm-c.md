---
title: "Damm Algorithm CLI Tool (C)"
description: "A lightweight C program to compute and validate check digits using the Damm algorithm, based on H. Michael Damm's 2004 dissertation."
date: 2025-04-27
categories: [software]
layout: project
---

# Damm Algorithm CLI Tool (C)

I've been fascinated by check digit algorithms ever since I wrote an ISBN check digit validator for a high school programming project back in the 1980s. There are many types of check digit systems, but the Damm algorithm has always stood out for its elegant structure and strong error detection properties.

This small command-line tool implements the [Damm algorithm](https://en.wikipedia.org/wiki/Damm_algorithm) in C for Linux systems.  
It allows users to compute a check digit for a given number or validate an existing number with its check digit.

The implementation uses the **quasigroup table** published in H. Michael Damm’s 2004 dissertation, [*Totally Antisymmetric Quasigroups*](http://archiv.ub.uni-marburg.de/diss/z2004/0516/pdf/dhmd.pdf) — the same table most commonly referenced in documentation and examples, including the [Wikipedia entry](https://en.wikipedia.org/wiki/Damm_algorithm#Example).

It’s important to note that the choice of quasigroup table matters:  
Different tables will typically produce different check digits. A check digit generated using one table will usually not validate against another, making this approach uniquely table-specific compared to many other check digit algorithms.

This implementation offers strong error detection capabilities. It catches all single-digit errors as well as adjacent digit transpositions — even when the check digit itself is involved. Thanks to the structure of the quasigroup table (where all diagonal elements are zero), there's no need for a separate table of inverses.

The system generates only digits (0–9) as possible check digits, eliminating the need for special characters like the "X" used in ISBN-10 schemes.

Leading zeros are treated consistently: numbers like `123`, `0123`, and `00123` all produce the same check digit, preserving data integrity across formatting variations.

Additionally, this implementation is designed to detect all common phonetic errors in English — such as confusing `13` with `30`, `14` with `40`, ..., `19` with `90` and similar pairs — making it even more robust for real-world transcription scenarios.

This project was developed partly for fun, partly out of personal curiosity, and partly as a way to revisit C programming at a low level.

## Features

- **Compute Check Digits:** Quickly generate the correct Damm check digit for any number.
- **Validate Numbers:** Validate a number's Damm check digit.
- **Simple Command-Line Interface:** Minimalist, efficient, and fast.
- **Built for Linux:** Written in standard C using GCC.

## Examples

**Generate a check digit:**
```sh
$ damm 38425
384253
```

**Check a valid number:**
```sh
$ damm -c 384253
```
*no output*

**Check an invalid number:**
```sh
$ damm --check 384254
Error: Invalid check digit.
```
---

[View the GitHub Repository →](https://github.com/bpg1968/damm---C)

