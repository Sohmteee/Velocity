<!-- markdownlint-disable MD024 -->
# Changelog

All notable changes to this project will be documented in this file.

## [1.1.0] - 2025-12-09

### Added

- **Commit History Browser**: New full-screen view to browse your entire commit history.
  - Search commits by message, author, or hash.
  - View detailed commit information with expandable file diffs.
  - Paginated list for smooth browsing of large repositories.
  - "View all" button in Project Overview for quick access.
- **Profile Screen**: New dedicated profile screen (replaces dialog).
  - User avatar, name, email with Pro badge.
  - Subscription card showing plan type (Monthly/Yearly) and next billing date.
  - GitHub stats (repositories, followers, following).
- **Notifications Screen**: New full-screen notifications view (replaces dialog).
  - Notification icon moved to home page header.
  - Mark all as read functionality.
  - Click notification to view full details in dialog and auto-mark as read.
- **Pro Payment Verification**: Auto-polling payment verification flow.
  - Automatic polling for Pro activation after payment.
  - Shows verification dialog with countdown while waiting for confirmation.
- **Commit Avatars**: GitHub profile pictures now displayed for commit authors.

### Improved

- **Faster Git Operations**: Git commands are now up to 30x faster.
  - Opening projects, staging files, and viewing status is now nearly instant.
  - Significantly reduced loading times for large repositories.
- **Payment Processing**: Upgraded to Flutterwave for more reliable payment handling.
  - Support for both local (NGN) and international (USD) payments.
  - Improved subscription management experience.
- **Automatic Branch Publishing**: Pushing a new branch automatically publishes it to GitHub.
- **Navigation**: Profile and Notifications are now dashboard tabs instead of dialogs.

### Fixed

- **Staged Changes Display**: Fixed a bug where unstaged changes were incorrectly shown as staged.
- **Untracked Files**: Untracked files now correctly appear in the changes list and can be staged.
- **Payment Verification Timer**: Fixed the countdown timer continuing after successful payment.

## [1.1.0] - 2025-12-04

### Added

- **Pro Features**: Introduced a comprehensive pro subscription model.
  - **Pro Dialog**: A detailed comparison view of Free vs. Pro plans.
  - **Upsell Card**: A non-intrusive card in the sidebar encouraging users to upgrade.
  - **Upgrade Flow**: Secure upgrade process that enforces user authentication.
- **Authentication System**: Full GitHub OAuth integration.
  - **Login Screen**: A branded login screen with "Sign in with GitHub".
  - **User Profile**: Sidebar widget displaying user avatar, name, and plan status.
  - **Logout Confirmation**: A safety dialog to prevent accidental logouts.
  - **Custom Auth Page**: A beautifully styled HTML success page for the local auth server.
- **Feedback System**: A robust in-app feedback mechanism.
  - **Feedback Dialog**: Allows users to report bugs or request features.
  - **Screenshot Support**: Users can now attach screenshots to their feedback.
  - **Metadata Collection**: Automatically captures OS, app version, and build number for better debugging.
- **UI Refinements**:
  - **Visual Polish**: Enhanced buttons and icons with the primary brand color and GitHub branding.
- **Analytics & Usage Tracking**:
  - **Session Tracking**: Logs session start and end times to Firestore.
  - **Daily Usage**: Tracks total daily usage duration.
  - **Heartbeat Sync**: Optimized "heartbeat" mechanism to sync data every 5 minutes with minimal database costs.
- **Productivity Features**:
  - **Uncommitted Changes Indicator**: Added a visual dot indicator in the sidebar for projects with uncommitted changes.
  - **Pro Sync**: Pro status changes in Settings are now instantly synced to the cloud.
- **UX Improvements**:
  - **Loading States**: Added "Signing in..." loading state to the Login screen.
  - **Streamlined Auth**: Improved the "Connect to GitHub" flow to prevent redundant sign-in prompts.

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
