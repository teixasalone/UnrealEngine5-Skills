# PCG Building Graph Patterns

## Pattern 1: Lot To Building Footprint
- Input lot points or splines.
- Filter invalid areas by slope, bounds, and exclusion tags.
- Derive footprint transforms for each accepted lot.

## Pattern 2: Vertical Stack
- Convert each footprint into floor-level points.
- Apply floor count rules by district tag or density tier.
- Offset transforms per floor height and pivot convention.

## Pattern 3: Facade Dressing
- Use side/corner classification from footprint edges.
- Sample facade modules by rule set and weighted randomness.
- Add conditional meshes (balcony, signage, trim) via tags.

## Pattern 4: Rooftop Pass
- Add rooftop modules only for top floor points.
- Validate clearance before large rooftop props.
- Keep rooftop spawn optional by style preset.

## Pattern 5: Output Selection
- Prefer Static Mesh Spawner with ISM/HISM for high counts.
- Use Spawn Actor only for interactive or stateful building parts.
- Keep output split by layer for easier debug and culling.
