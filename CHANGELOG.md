# Changelog

All notable changes to this project will be documented in this file.

## [1.0.3] - 2025-12-02

### Added

- **GitHub Integration**: Added a "New" button to the "Connect to GitHub" screen, allowing users to quickly create a new repository in the browser. The list automatically refreshes upon returning to the app.
- **Auto-Commit Progress**: The Project Overview now displays real-time progress (Staging, Diffing, Generating Message, Committing, Pushing) next to the Push button during auto-commits.
- **Path Truncation**: Project paths in the dashboard are now intelligently truncated for better readability.

### Changed

- **Auto-Commit Service**: Enhanced the service to broadcast granular status updates for better UI feedback.

## [1.0.2] - 2025-12-02

### Added

- **Version Display**: Added the current application version number (e.g., v1.0.2) to the bottom of the sidebar for easy verification.
- **Update Settings**: Added a toggle in Settings > General to enable/disable automatic update checks on startup.
- **Diff Stats**: Added visual diff statistics (insertions/deletions) next to files in the changes list with color-coding (Green for additions, Red for deletions).
- **Auto-Commit Controls**: Added a cancel button to the auto-commit banner and disabled the push button while an operation is in progress.
- **Dynamic Installer**: The Windows installer now automatically includes the version number in its filename (e.g., `Velocity_Setup_v1.0.2.exe`).

### Fixed

- **UI Blurriness**: Resolved an issue where the UI would become blurry on Windows during hot reloads.
- **Onboarding Flash**: Fixed a bug where the onboarding screen would briefly flash on startup for existing users.
- **Push Logic**: Fixed an issue where the push button would stop immediately if there were no changes to commit but local commits needed pushing.

## [1.0.1] - 2025-12-02

### Added

- **Update Notification**: Added a feature to check for updates on startup.
  - Checks GitHub Releases for newer versions.
  - Displays a non-intrusive toast notification if an update is available.
  - Includes a "Download" button to open the release page.
  - Uses a custom SVG icon for the notification.

## [1.0.0] - 2025-12-02

### Added

- Initial release of Velocity.
- Dashboard with GitHub integration.
- Settings management.
- "Gentle Nudge" feature for commit reminders.
- Custom window title bar and semantic theme colors.
- Toastification for notifications.
