---
title: "MTG Inventory Tool"
collection: portfolio
permalink: /portfolio/mtg-inventory-tool/
excerpt: "A local-first Python and SQLite workflow for handling collectible inventory with print-level identity, condition, and valuation."
date: 2026-03-30
author_profile: true
link: "https://github.com/monsonbo2/MtG_Inventory_Tool"
---

<span class="project-meta">Python • SQLite • CLI design • data modeling</span>

This project started from a practical problem: keeping track of a collectible inventory where many items look similar, but still need to be treated as meaningfully different. For Magic: The Gathering cards, that means handling printings, finishes, language, condition, storage location, and pricing data without collapsing important distinctions.

## What It Does

- Imports catalog and pricing data from Scryfall and MTGJSON into a local SQLite-backed workflow.
- Supports one or more personal inventories instead of a single flat collection.
- Tracks owned printings with condition, finish, language, quantity, notes, tags, and location.
- Produces valuations and reports from imported price snapshots.

## Why I Built It This Way

I wanted something more rigorous than a spreadsheet and more practical than a simple card catalog. The data model is built around the idea that identity can be hierarchical and context-sensitive: some differences matter for valuation or organization, while others matter for substitution or personal use. That made it a good design problem as well as a useful tool.

## What It Shows About My Work

- I enjoy translating messy real-world categories into durable systems.
- I care about usability, not just correctness.
- I like building tools that are extensible enough to handle future complexity without becoming fragile.

## Where It Can Grow

The same approach could extend beyond trading cards to any inventory domain with overlapping variants, bundle relationships, and condition-sensitive value.
