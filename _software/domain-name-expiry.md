---
title: "Domain Name Expiry Script (Shell)"
description: "A simple but flexible shell script to check domain expiration dates, enhanced with colour-coded output and command-line options."
date: 2025-04-27
categories: [software]
github: https://github.com/bpg1968/Domain-Name-Expiry
layout: project
---

# Domain Name Expiry Script (Shell)

What started as an idea for a **macro-like script** — just to automate a few `whois` and `grep` commands — turned into something much more useful.

At first, I planned to simply loop over an array of domain names and display their expiration dates. But then I thought it might be even more flexible to read domain names from a file instead. Thanks to the help of AI, it became easy (and fun) to keep adding features: colour-coded output, command-line options, and even the ability to check just a single domain directly.

This project is shared in the hopes that someone else might find it useful too.

## Features

- **Flexible Input:** Read domain names from a default file (`~/.domains.txt`), a custom file, or provide a single domain on the command line.
- **Colour-Coded Output:**  
  - **Green** — Domain is available  
  - **Red** — Domain has expired  
  - **Yellow/Orange** — Domain expires within 3 months  
  - **White** — Domain is valid for more than 3 months
- **Respectful Querying:** 1-second delay between lookups to avoid overwhelming `whois` servers.
- **Graceful Error Handling:** Friendly messages if the input file is missing or invalid.
- **Simple Installation:** Just clone the repo, make the script executable, and run.

## How It Works

The script uses standard Linux utilities like `whois`, `grep`, `tput`, and `date` to fetch and format expiration information in a human-readable way. Colour formatting makes it easy to quickly spot domains that are about to expire.

It's lightweight, fast, and designed for real-world daily use.

