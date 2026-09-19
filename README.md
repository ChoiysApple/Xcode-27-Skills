# Xcode-27-Skills

A personal archive of built-in coding skills exported from Xcode 27 and maintained for Xcode 27.1 beta.

> **Note**
> This archive began with skills from the first Xcode 27 beta and now includes Xcode 27.1 beta guidance.

## Contents

- `xcode-skills/swiftui-whats-new-27` — SwiftUI APIs, behavior changes, and deprecations introduced by the OS 27 SDKs.
- `xcode-skills/swiftui-specialist` — SwiftUI architecture, data flow, localization, accessibility, and soft-deprecation guidance.
- `xcode-skills/uikit-app-modernization` — UIKit modernization for scene lifecycle, safe areas, orientation, and screen APIs.
- `xcode-skills/audit-xcode-security-settings` — Xcode build-setting and security-hardening audits.
- `xcode-skills/c-bounds-safety` — C bounds-safety adoption and debugging guidance.
- `xcode-skills/test-modernizer` — XCTest to Swift Testing modernization.
- `xcode-skills/device-interaction` — Device and Simulator interaction verification.
- `xcode-skills/xcode-27-1-beta` — Xcode 27.1 beta toolchain, compatibility, and verification notes.

## Updating the archive

Select the Xcode 27.1 beta installation, then export its built-in skills into this repository:

```sh
sudo xcode-select -s "/Applications/Xcode 27.1 beta.app/Contents/Developer"
xcrun agent skills export --replace-existing ./xcode-skills
```

Review the generated diff, preserve the repository's README inventory, and commit the export on a versioned branch. The `xcode-27-1-beta` skill includes the Apple release-note context that is not part of the generic framework skills.

## Source

The archive is based on skills shipped with Xcode and Apple Developer documentation. Beta-specific notes are summarized from the [Xcode 27.1 beta release notes](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_1-release-notes).
