# base-unit-trait-attack-ends-turn

The `AttackEndsTurn` unit trait: a unit type with it ends its turn when it attacks.

A unit type with this trait uses up its remaining moves when it attacks.

For example: Civ1: Bomber.

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(AttackEndsTurn)`:

```ts
import AttackEndsTurn from '@civ-clone/base-unit-trait-attack-ends-turn/AttackEndsTurn';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, AttackEndsTurn));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
