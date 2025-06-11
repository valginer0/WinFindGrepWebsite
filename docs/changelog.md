# Changelog

All notable changes to WinFindGrep will be documented in this file.

## [v1.1.0] - 2025-06-11

### Added
- Asynchronous search engine (**async/await**) keeps UI responsive on large directory trees and network drives.
- New **Modified** column shows each file’s last-write timestamp in results.

### Changed
- Various performance optimizations: removed superfluous thread hops, switched to line-by-line streaming, compile one Regex per file, and throttled progress events to minimize UI lag.

### Fixed
- Replace-in-Files now works with the async pipeline and respects the new timestamp field.
- Searches automatically skip inaccessible folders/files instead of aborting.

### Tests
- Unit tests upgraded to async and coverage extended for new functionality.

## [v1.0.0] - 2025-06-04

First stable release of WinFindGrep, a Windows desktop application for searching and replacing text across multiple directories.

### Features
- Multi-directory text search with file filtering (default: *.txt)
- Advanced search options including regex and case sensitivity
- Replace functionality for bulk text updates
- Self-contained executable with no dependencies
