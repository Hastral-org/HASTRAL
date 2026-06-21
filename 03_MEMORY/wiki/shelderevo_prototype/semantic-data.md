# Architecture: Semantic Data Units (Exps, Keys, Symbols)

Shelder Evolution uses a specialized data architecture to manage lore, mechanics, and memory in a way that is both machine-readable (for the HIVE) and narratively significant.

## 1. Exps (Experiences)

**Exps** are the primary data structures for "Sentient Memory."

- **Function**: They are handed between entities and systems to gather and deliver data.
- **Narrative Role**: They represent the individual experiences of a creature. For example, an `exp` might store the data of a specific hunt, which then influences the creature's future "Agency" (S3).
- **Technical Role**: Act as "Packets" of state that can be easily serialized and synchronized.

## 2. Keys (Semantic Units)

**Keys** are identifiers used to attach or unlock meaning within other components.

- **Function**: They function like tags or flags that trigger specific behaviors or lore reveals.
- **Example**: A `Key` might be "Aquatic_Predator," which unlocks specific evolutionary cards in the CCG layer when certain conditions are met.

## 3. Symbols (Semantic Archetypes)

**Symbols** are the highest level of abstraction, designed for the CCG (Collectible Card Game) mechanics.

- **Function**: They synthesize the "most common denominator" traits into a single card representation.
- **Visual Role**: When a player looks at their "Creature Deck," they are looking at a collection of `Symbols` that abstract the complex biological state of the Shelder into understandable game terms.

## 4. Contexts (Quick Configurations)

**Contexts** are semantic groupings used for the rapid setup of scenarios involving the units above.

- **Buffering**: They ensure that related Entities, Exps, Keys, and Symbols are buffered in the **HIVE** together, reducing latency during complex world events.
- **Meta-Role**: They can double as "Semantic Metakeys," defining the "Vibe" or "Rulebook" of a specific location or event.

## 5. The Data Cycle

1. **Event** generates an **Exp**.
2. **Exp** is processed by the **HIVE**.
3. **HIVE** updates the Entity's **Keys** based on the Exp.
4. **Symbols** (Cards) are updated to reflect the new state of the Entity's Keys.

---
*Reference: [HIVE & MAGPIE Architecture](./hive-architecture.md), [S0-S4 Agency Framework](./agency-framework.md)*
