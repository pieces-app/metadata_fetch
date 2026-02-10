# Fork Changes Documentation

This document tracks all custom modifications, patches, and deviations from the upstream `jg-l/metadata_fetch` repository.

## Fork Information

- **Fork Repository**: `https://github.com/pieces-app/metadata_fetch`
- **Upstream Repository**: `https://github.com/jg-l/metadata_fetch`
- **Current Branch**: `master`
- **Fork Version**: `0.4.2`
- **Commits Ahead**: 7 (custom modifications)
- **Commits Behind**: 0 (fully synced)
- **Last Upstream Merge**: February 2026 -- merged `upstream/master` into `chore/unify-dependencies` (commit `fe209b2`)

## Custom Modifications

### 1. Remove String Validator Dependency
- **Commit**: `7027c6d`
- **Changes**:
  - Removed `string_validator` dependency
  - Updated URL validation logic in `metadata_fetch_base.dart` to use built-in Dart URL parsing
- **Files Modified**:
  - `lib/src/metadata_fetch_base.dart` (8 lines changed: 4 insertions, 4 deletions)
- **Reason**: Reduced dependency footprint; `string_validator` was unnecessary when Dart's `Uri.tryParse` suffices

### 2. Dependency Updates
- **Commits**: `845f195`, `4dbb396`, `151d95b`, `bfd1dd7`
- **Changes**: Updated dependencies for SDK compatibility across multiple iterations

### 3. IDE Configuration
- **Commit**: `8b1d270`
- **Changes**: Added `.iml` IDE project file

## Upstream Sync History

### February 2026 - Upstream Merge & Dependency Unification
- **Merge Commit**: `fe209b2` -- merged `upstream/master` into `chore/unify-dependencies`
- **Changes Merged**: 3 upstream commits (CHANGELOG and pubspec updates)
- **Conflicts Resolved**: `pubspec.yaml` (kept workspace resolution and SDK constraints)
- **Custom Changes Preserved**: `string_validator` removal intact, workspace `resolution: workspace` preserved
- **Version**: Bumped to `0.4.2`
- **Status**: Fully synced with upstream

## Upstream Sync Status

- **Current Gap**: 0 commits behind upstream/master (fully synced, February 2026)
- **Status**: Up to date. Monitor upstream for new commits (upstream is stale -- last push Sep 2024).

## Why This Fork Exists

1. **Dependency Reduction**: Removed unnecessary `string_validator` dependency
2. **SDK Compatibility**: Updated for newer Dart SDK versions

## Future Considerations

1. **Consider Dropping Fork**: Now fully synced. Could potentially use upstream if they accept the `string_validator` removal PR and bump SDK constraints. However, upstream is stale (last push Sep 2024, 0 recent activity).
2. **Upstream Contribution**: The string_validator removal is a clean improvement that could be contributed
3. **SDK Compatibility**: Upstream pub.dev SDK constraint is likely still old (`<3.0.0`). Fork is needed until upstream updates.

## Contact

For questions about this fork or to request changes, contact the Pieces development team.
