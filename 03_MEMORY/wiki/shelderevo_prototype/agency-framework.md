# Concept: S0-S4 Agency Framework

The **S0-S4 Framework** defines the levels of existence, autonomy, and relationship for creatures in Shelder Evolution. It moves away from simple NPC scripts toward a multi-layered model of "living" entities.

## Level S0: Persistence & Perpetuality

- **Definition**: The entity exists in the **Global Database** independently of any player's presence.
- **Mechanical Hook**: The creature continues its metabolic cycles and interactions in the background (`magpie-server` core).
- **Feeling**: The world is perpetual; things happen even when you are offline.

## Level S1: Instinct & Metabolism (Growth)

- **Definition**: The base biological layer.
- **Mechanical Hook**: Governs the **Fatigue-Stamina-Reserve** system. The creature has "instincts" (eat, rest, flee) that drive its idle behavior.
- **Growth**: As the creature survives, it builds its "Deck" of traits and capabilities.

## Level S2/S3: Agency & Intelligence

- **Definition**: The decision-making layer.
- **Mechanical Hook**: A combination of **State-driven Impulses** (hunger, fear) and **Experience-driven Morality** (derived from `exps`).
- **Emergence**: NPCs aren't just following paths; they are "Agents" making "Grey Decisions" based on their current needs and history.

## Level S4: Affinity & Rapport

- **Definition**: The bond between the Player and their adopted creature.
- **The "Team" Dynamic**:
  - **Loose Team**: High friction, "laggy" response to player influence, potential conflict.
  - **Tight Team**: High responsiveness, "shorthand" rapport, unlocking direct interface options like 'WASD' control.
- **Emergent UX**: Affinity is earned through shared experiences and survival, not just a numerical stat.

## Level S5: Interface & Console

- **Definition**: The meta-layer where the player interacts with the creature via the **Player Console** or CLI.

---
*Reference: [Biomass Economy](./biomass-economy.md), [Vitals System](./vitals-system.md)*
