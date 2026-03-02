---
name: ue5-pcg-building
description: UE5.6/UE5.7 PCG building generation workflow for modular buildings, blockouts, facade rules, and runtime generation. Use when requests involve Procedural Content Generation (PCG), Shape Grammar, lot-based building spawn, deterministic random seeds, density/filter pipelines, or converting designer constraints into reusable PCG graphs.
---

# Quick Start
- Define generation target: blockout towers, modular facades, or full lot-based building sets.
- Define input data: lot splines, points, tags, seed, and per-zone constraints.
- Define output type: Static Mesh instances, spawned actors, or dynamic mesh output.

# Workflow
- Build PCG graph stages: input collection, filtering, transform generation, and output spawn.
- Keep deterministic random behavior with explicit seed inputs and stable point ordering.
- Use Shape Grammar for facade and floor stacking patterns when rule-based structure is required.
- Split graph into reusable subgraphs for footprint, vertical stacking, facade dressing, and rooftop pass.
- Add validation pass for collision, navigation impact, and overlap rejection before final spawn.

# Constraints
- Keep the main pipeline compatible with both UE5.6 and UE5.7 unless a version-specific note is required.
- Prefer ISM/HISM style output for large counts; avoid spawning heavyweight actors for every small part.
- Keep runtime generation bounds explicit to avoid uncontrolled world-wide regeneration.
- Avoid hidden dependency on editor-only data when runtime generation is expected.

# Failure Handling
- If no buildings spawn, verify input points/splines and spatial bounds first.
- If generated meshes overlap, add slope/clearance filters and occupancy checks before output.
- If runtime generation hitches, reduce graph complexity per cell and batch expensive operations.
- If results are non-reproducible, lock seed source and normalize upstream point sets.

# Escalation
- Escalate when architecture requires custom C++ PCG elements or engine plugin extension.
- Escalate when city-scale generation must be integrated with World Partition streaming policy.
- Escalate when generated layout must be synchronized with save/load or multiplayer authority rules.
