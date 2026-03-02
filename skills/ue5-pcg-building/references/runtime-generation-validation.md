# Runtime Generation Validation

## Functional Checks
- Verify generation source moves correctly and updates target bounds.
- Verify graph regenerates only required cells or regions.
- Verify seed and style settings produce reproducible output.

## Performance Checks
- Measure generation spikes in PIE and standalone.
- Confirm high-count outputs use instance-based rendering.
- Limit per-update spawned element count to avoid frame hitches.

## World Integration Checks
- Validate navigation behavior for generated collision.
- Validate streaming boundaries with World Partition.
- Validate interaction actors are spawned only where needed.

## Safety Checks
- Ensure runtime path does not call editor-only logic.
- Ensure cleanup path removes stale generated instances.
- Ensure save/load or network authority rules are explicit.
