# Changelog - Birdtray-MATE

All notable changes to Birdtray-MATE will be documented in this file.

## [1.12.6] - 2026-08-28

### Added
- **Unread Folder Details Dialog**: Added an "Unread Folder Details..." entry to the right-click tray icon context menu. Clicking it opens a popup dialog detailing all monitored mailboxes, highlighting folders containing unread mail in red with exact counts and paths.

### Fixed
- **Instant File Watcher (inotify)**: Updated `unreadmonitor.cpp` to register `.msf` file paths directly with `QFileSystemWatcher`, enabling instant `IN_MODIFY` inotify updates when Thunderbird marks emails read or unread.
- **Zero Temp File Disk Overhead**: Replaced temporary file creation and copying in `morkparser.cpp` with direct read-only in-memory parsing, eliminating `/tmp/birdtray.XXXXXX` disk churn and file leakage.
