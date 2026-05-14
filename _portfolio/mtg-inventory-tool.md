---
title: "MTG Inventory Tool"
collection: portfolio
permalink: /portfolio/mtg-inventory-tool/
excerpt: "A full-stack inventory and valuation system for complex, variant-heavy collectible goods with searchable records, auditable transactions, and decision-ready reporting."
date: 2026-03-30
author_profile: true
link: "https://github.com/monsonbo2/MtG_Inventory_Tool"
---

<span class="project-meta">Python • SQLite • FastAPI • React • TypeScript • data modeling</span>

This project started from a practical problem: keeping track of a collectible inventory where many items look similar, but still need to be treated as meaningfully different. For Magic: The Gathering cards, that means handling printings, finishes, language, condition, storage location, ownership history, and pricing data without collapsing important distinctions.

The result is a full-stack inventory and valuation system for complex, variant-heavy goods. It translates messy product, pricing, and ownership data into searchable inventory records, auditable transactions, and usable valuation reports.

## What It Does

- Imports catalog, identifier, and pricing data from Scryfall and MTGJSON into SQLite.
- Supports one or more inventories instead of a single flat collection.
- Tracks owned printings with condition, finish, language, quantity, notes, tags, location, and acquisition details.
- Produces valuations and reports from imported price snapshots.
- Supports transactional mutation flows, grouped bulk mutations, inventory transfer and duplication, CSV and deck import/export, and per-edit audit logging.
- Provides a React/TypeScript/Vite frontend for inventory selection, card search and add flows, inline item editing, and recent audit activity.

## Why I Built It This Way

I wanted something more rigorous than a spreadsheet and more practical than a simple card catalog. The data model is built around the idea that identity can be hierarchical and context-sensitive: some differences matter for valuation or organization, while others matter for substitution or personal use.

That made the project a good systems problem, not just a card database. The platform now supports a local-first SQLite workflow for offline personal use and a hosted single-host shared-service model with authenticated, role-scoped inventory access.

## Technical Shape

- Backend ingestion workflows for Scryfall/MTGJSON data, SQLite schema and migrations, inventory-domain services, pricing, valuation, reporting, CSV import/export, deck import/export, and audit history.
- FastAPI service layer with documented API contracts, role-scoped inventory access, grouped bulk mutations, transfer and duplication workflows, import preview and commit flows, and snapshot-based recovery support.
- Frontend built with React, TypeScript, and Vite against a contract-driven HTTP boundary.

## What It Shows About My Work

- I enjoy translating messy real-world categories into durable systems.
- I care about usability, auditability, and operational fit, not just correctness.
- I like building tools that are extensible enough to handle future complexity without becoming fragile.
- I am comfortable working across data modeling, backend service design, API contracts, frontend workflows, and documentation.

## Where It Can Grow

The same approach could extend beyond trading cards to any inventory domain with overlapping variants, bundle relationships, and condition-sensitive value.
