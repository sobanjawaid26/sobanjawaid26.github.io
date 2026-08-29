# Cluviqo — App Store and Release Copy

## App metadata

- Name: Cluviqo
- Subtitle: Private password reminders
- Promotional text: Remember passwords without storing them. Build layered clues that only make sense to you, reveal one at a time, and keep everything offline on your device.
- Keywords: password,clue,reminder,memory,hint,offline,private,secure,recall,local
- Tagline: Clues that only make sense to you

## App Store description

Remember the clue, not the password.

Cluviqo is a private password-reminder utility that helps you create personally meaningful clues—without intentionally storing your actual passwords. It is not a password manager: it does not generate, autofill, verify, or connect to accounts.

Create up to five layered hints for each service, then reveal them one at a time only when you need help. Organize clues by category, mark favorites, archive old entries, search locally, and schedule optional review reminders.

Designed for privacy:

- No account or internet connection required
- No analytics, advertising, or tracking
- Username hints and clue layers encrypted locally with AES-GCM
- Encryption key protected by the iOS Keychain
- Optional Face ID, Touch ID, or device-passcode protection
- App-switcher cover and active screen-recording protection
- Local notifications only; no remote push service

Your clues stay on the original device. They do not sync, transfer through backups, or go to the developer. If the device is lost, damaged, erased, or replaced, the developer cannot recover them.

Important: Never enter your actual password. Cluviqo is a reminder, not a credential vault.

## Release notes — Version 1.0

Welcome to Cluviqo. Create layered private clues, organize them by category, reveal hints one at a time, review clues on a schedule, and optionally protect access with Face ID, Touch ID, or your device passcode. Everything stays local to the original device.

## TestFlight description

Test the complete local-only clue workflow: onboarding, creating and editing clues, layered reveal and automatic concealment, favorites, search and filters, archiving and restoration, review reminders, authentication, quick lock, app-switcher privacy, screen-recording protection, light/dark appearance, Dynamic Type, VoiceOver, rotation, and iPad layouts. Never enter a real password or sensitive credential while testing.

## App Review notes

Cluviqo is a local-only password-reminder utility. It helps users store personally meaningful encrypted clues rather than actual passwords. No account or network connection is required.

Username hints and clue text are encrypted locally using AES-GCM with a key protected by the iOS Keychain. The app does not collect or transmit user data. Device authentication is optional and supports Face ID, Touch ID, or the device passcode through Apple’s device-owner authentication interface.

Review reminders use local notifications; no remote push service is used. Screen Recording Protection conceals content while iOS reports active recording or screen sharing. The app does not claim that ordinary screenshots can be prevented.

The binary declares `ITSAppUsesNonExemptEncryption = YES` conservatively. The account holder will answer Apple’s export-compliance questions and provide any requested documentation; no exemption is claimed here.

## Screenshot captions

1. Keep every hint hidden until you need it.
2. Build up to five clues that only make sense to you.
3. Reveal one hint at a time—never the password itself.
4. Find clues by name, category, favorite, or recent activity.
5. Protect access with iOS device authentication.
6. Choose when revealed clues conceal themselves again.

## Onboarding copy

1. **Remember the clue, not the password.** Build personal reminders that help you reconstruct what you already know. Never enter an actual password.
2. **Stays on this device.** Your clues are stored locally, encrypted where sensitive, and never sent to us. They do not sync or restore to another device.
3. **Add device protection.** Optionally require Face ID, Touch ID, or your device passcode whenever Cluviqo locks.
4. Actions: **Enable Authentication** / **Not Now**

## Permission explanations

- Notifications: Allow Cluviqo to schedule private, on-device reminders to review whether your clues still help. No remote push service or device token is used.
- Face ID purpose string: Face ID protects your private clues.

## Security and encryption overview

Cluviqo encrypts username hints and clue layers locally using Apple CryptoKit, AES-GCM, and a random 256-bit symmetric key. The key is stored using `kSecAttrAccessibleWhenUnlockedThisDeviceOnly`; it is usable only while the device is unlocked and does not migrate through backup. Account names and organizational metadata stay local but are not encrypted. App storage is excluded from backups to avoid restoring ciphertext without its original-device key.

The app has no application networking, third-party SDKs, analytics, crash-reporting service, advertising, tracking, external AI, cloud database, CloudKit, or remote notifications. Password-like text detection, search, encryption, and decryption run locally.

## Data retention and deletion statement

Clues remain on the original device until the user deletes them or removes app data. Individual clues can be archived, restored, or permanently deleted; all app data can also be deleted. Permanent deletion is irreversible. Removing a clue removes its local review reminder. The developer cannot view, decrypt, restore, or recover app data.

## Backup and device-transfer warning

Cluviqo data is intentionally excluded from iCloud and computer backups. Clues do not synchronize or transfer to a replacement device. If this device is lost, damaged, erased, or replaced, your clues cannot be recovered—even by the developer. Recreate any clues you still need on the new device.

## Accessibility statement

Cluviqo is built with native SwiftUI components and provides accessibility labels for important controls, including Settings, filters, manual lock, unlock, category selection, favorite controls, hint removal, and quick close. Accessibility feedback is welcome through support. Users should never include real passwords or clue text in a report.

## Support response templates

### Authentication issue

Confirm that your device has a passcode configured and that Face ID or Touch ID is enrolled if you want to use biometrics. Cluviqo uses iOS device-owner authentication, and passcode fallback remains available. Please share your device model, iOS version, and exact error wording—never your password or clue text.

### Missing clues or new device

Cluviqo stores clues only on the original device and excludes them from backups. They do not sync or restore to a replacement device, and the developer does not have a copy or encryption key. Unfortunately, lost or deleted clues cannot be recovered.

### Notification issue

Open iOS Settings, select Cluviqo, and confirm notifications are allowed. Review reminders are local and will not be delivered when permission is denied. Archiving or deleting a clue removes its reminder.

### Screen protection question

Screen Recording Protection covers app content while iOS reports an active recording or screen-sharing session. iOS reports an ordinary screenshot only after capture, so Cluviqo cannot guarantee screenshot blocking.
