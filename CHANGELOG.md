<!-- markdownlint-disable MD024 -->
# Changelog

All notable changes to this project will be documented in this file.

## [1.1.1] - 2025-12-11

### Fixed

- **Payment Redirect**: Fixed payment callback redirect URL to use the proper landing page instead of a placeholder.
- **Recent Commits**: Initial commit now appears in recent commits after linking a new project to GitHub.

## [1.1.0] - 2025-12-09

### Added

- **Commit History Browser**: New full-screen view to browse your entire commit history.
  - Search commits by message, author, or hash.
  - View detailed commit information with expandable file diffs.
  - Paginated list for smooth browsing of large repositories.
  - "View all" button in Project Overview for quick access.
- **Keyboard Shortcuts**: Customizable shortcuts for common Git actions.
  - Stage All, Commit, Push, Undo Commit, Stash, Unstash, and Close Tab.
  - Configure your own key combinations in Settings.
- **Profile Screen**: New dedicated profile screen.
  - User avatar, name, email with Pro badge.
  - Subscription card showing plan type (Monthly/Yearly) and next billing date.
  - GitHub stats (repositories, followers, following).
- **Notifications Screen**: New full-screen notifications view.
  - Notification icon moved to home page header.
  - Mark all as read functionality.
  - Click notification to view full details in dialog and auto-mark as read.
- **Pro Features**: Comprehensive pro subscription model.
  - Pro comparison dialog showing Free vs. Pro plans.
  - Non-intrusive upsell card in the sidebar.
  - Secure upgrade process with authentication.
- **Authentication System**: Full GitHub OAuth integration.
  - Branded login screen with "Sign in with GitHub".
  - Sidebar widget displaying user avatar, name, and plan status.
  - Logout confirmation dialog.
- **Feedback System**: In-app feedback mechanism.
  - Report bugs or request features directly from the app.
  - Attach screenshots to your feedback.
- **Commit Avatars**: GitHub profile pictures now displayed for commit authors.
- **Uncommitted Changes Indicator**: Visual dot in sidebar for projects with uncommitted changes.

### Improved

- **Faster Git Operations**: Git commands are now up to 30x faster.
  - Opening projects, staging files, and viewing status is now nearly instant.
  - Significantly reduced loading times for large repositories.
- **Payment Processing**: Upgraded to Flutterwave for more reliable payment handling.
  - Support for both local (NGN) and international (USD) payments.
  - Improved subscription management experience.
- **Automatic Branch Publishing**: Pushing a new branch automatically publishes it to GitHub.
- **Navigation**: Profile and Notifications are now dashboard tabs instead of dialogs.
- **Connect to GitHub Flow**: Streamlined flow to prevent redundant sign-in prompts.

### Fixed

- **Staged Changes Display**: Fixed a bug where unstaged changes were incorrectly shown as staged.
- **Untracked Files**: Untracked files now correctly appear in the changes list and can be staged.
- **Payment Verification Timer**: Fixed the countdown timer continuing after successful payment.

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
