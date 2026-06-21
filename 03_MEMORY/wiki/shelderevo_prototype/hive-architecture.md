# Architecture: The HIVE & MAGPIE Server

The **M.A.G.P.I.E.** (Modular Agentic Governance & Persistent Intelligence Engine) Server is the "AI Overlady" of the Shelder Evolution ecosystem. It manages the persistent world, entity agency, and the centralized knowledge base.

## 1. The MAGPIE Server

The server is a Node.js application that serves as the authoritative source of truth for the game world.

- **Role**: Oversees entity cycles, processes asynchronous events, and handles the `better-sqlite3` database connections.
- **Lore Integration**: Within the game world, MAGPIE is an ancient AI overseeing the Sanriku zone, making the server's technical role a part of the meta-narrative.

## 2. The HIVE System

The **HIVE** is the runtime memory and buffering system within the server.

- **Purpose**: Dedicated to managing active entities and buffering the components (Exps, Keys, Symbols) necessary for them to run smoothly.
- **Efficiency**: Instead of querying the database for every minor interaction, the HIVE keeps "Hot" entities and their contexts (`contexts`) in memory.
- **Persistence**: The HIVE periodically flushes its state to the `metastate` table in the SQLite database.

## 3. Distributed Persistence

While the HIVE is centralized in the MAGPIE Server, the state is synchronized across the community using:

- **Local SQLite DBs**: For immediate player-side performance.
- **Discord Sync-Layer**: For global community events and cross-player state persistence.

## 4. Entity Management

Entities in the HIVE are not just "Objects"; they are "Subjects" with properties and the ability to interact.

- **Physical Entities**: Creatures, items, environmental objects.
- **Abstract Entities**: Geomarkers, events, and triggers that exist in the world coordinates but lack a "Body."

---
*Reference: [S0-S4 Agency Framework](./agency-framework.md), [Discord Sync Persistence](../../../.github/skills/discord-sync-persistence/SKILL.md)*
