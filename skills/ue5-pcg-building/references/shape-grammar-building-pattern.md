# Shape Grammar Building Pattern

## Use Cases
- Rule-driven facade variation with deterministic output.
- District style switching without rebuilding full graphs.
- Fast iteration on floor and facade composition rules.

## Rule Design Checklist
- Define atomic modules first: base, mid, corner, top, roof.
- Keep grammar symbols readable and style-scoped.
- Isolate random choices behind explicit seeded selectors.
- Add hard constraints for min/max height and facade continuity.

## Integration Pattern
- Generate candidate points/transforms in PCG graph.
- Apply shape grammar stage for module sequence decisions.
- Emit final symbol-resolved meshes to output spawner.
- Record style/seed metadata tags for debug and replay.

## Common Pitfalls
- Mixing unit scales across module sets.
- Unstable rule order causing non-deterministic variation.
- Overly deep grammar chains causing heavy runtime cost.
