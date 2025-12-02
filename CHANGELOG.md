<!-- markdownlint-disable MD024 -->
# Changelog

All notable changes to this project will be documented in this file.

## [1.0.2] - 2025-12-02

### Added

- **Version Display**: Added the current application version number (e.g., v1.0.2) to the bottom of the sidebar for easy verification.
- **Update Settings**: Added a toggle in Settings > General to enable/disable automatic update checks on startup.
- **Diff Stats**: Added visual diff statistics (insertions/deletions) next to files in the changes list with color-coding (Green for additions, Red for deletions).
- **Auto-Commit Controls**: Added a cancel button to the auto-commit banner and disabled the push button while an operation is in progress.

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
