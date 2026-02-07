# Fork Changes Documentation

This document tracks all custom modifications, patches, and deviations from the upstream `jg-l/metadata_fetch` repository.

## Fork Information

- **Fork Repository**: `https://github.com/pieces-app/metadata_fetch`
- **Upstream Repository**: `https://github.com/jg-l/metadata_fetch`
- **Current Branch**: `master`
- **Fork Version**: `0.4.1`
- **Commits Ahead**: 7
- **Commits Behind**: 3
- **Last Upstream Merge**: Fork created from upstream

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

## Upstream Sync Status

- **Current Gap**: 3 commits behind upstream/master
- **Complexity**: LOW -- our changes are minimal
- **Priority**: LOW -- small gap, stable package

### Recommended Sync Approach
1. Fetch upstream master
2. Merge -- should be straightforward with 3 commits behind
3. Verify string_validator removal is still intact
4. Test metadata fetching functionality

## Why This Fork Exists

1. **Dependency Reduction**: Removed unnecessary `string_validator` dependency
2. **SDK Compatibility**: Updated for newer Dart SDK versions

## Future Considerations

1. **Consider Dropping Fork**: Only 3 commits behind with minimal changes; may be possible to use upstream directly
2. **Upstream Contribution**: The string_validator removal is a clean improvement that could be contributed

## Contact

For questions about this fork or to request changes, contact the Pieces development team.
