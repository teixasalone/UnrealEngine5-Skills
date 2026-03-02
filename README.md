# UnrealEngine5-Skills

A practical Codex skill pack for Unreal Engine **5.6/5.7** projects.

This repository provides reusable skill workflows to help with:

- Blueprint feature implementation
- Gameplay C++ development
- UI (UMG/Slate) tasks
- Save/Load and replication
- Debugging and validation
- Performance and packaging checks
- Architecture and module-boundary design

## Skill List

- `ue5-auto-assistant`: default entry and intent-based routing
- `ue5-module-router`: module name/alias based routing
- `ue5-architecture`: module layout, Build.cs, ownership boundaries
- `ue5-blueprint-workflow`: Blueprint graph edits and input-event workflows
- `ue5-cpp-gameplay`: gameplay C++ patterns for UE5.6/5.7
- `ue5-debug-validation`: issue triage and validation workflow
- `ue5-performance-packaging`: runtime perf and pre-package checks
- `ue5-save-load-replication`: SaveGame and multiplayer sync workflow
- `ue5-ui-umg-slate`: UMG/Slate implementation guidance
- `ue5-world-interaction`: pickups, spawners, overlap/trace interaction logic

## Quick Start

1. Start with `ue5-auto-assistant`.
2. If module names appear, route with `ue5-module-router`.
3. Execute the selected target skill workflow.

More details are in [skills/README.md](./skills/README.md).

## Validation

Run:

```powershell
python .\skills\scripts\validate_skills.py
```

Expected output: `Validation OK`

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).

