# Project Adapter

Use this file to map generic PCG building workflow to a concrete project.

## Fill-in Items
- PCG graph assets under `/Game/...` and owning map(s)
- Building module mesh sets and pivot conventions
- Lot, district, or biome tags used by filters
- Runtime generation trigger source (volume, player source, subsystem)
- Target output mode (ISM/HISM, actor spawn, dynamic mesh)
- Save/load and replication requirements for generated results

## Current Default
- Keep this skill generic by default.
- Add project-specific mappings here only when needed.
