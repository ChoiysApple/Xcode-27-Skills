---
description: "Xcode 27.1 beta release guidance, compatibility notes, and beta-era verification checklist."
name: xcode-27-1-beta
---
# Xcode 27.1 Beta

Use this skill when a task targets Xcode 27.1 beta, Swift 6.4, or the iOS/iPadOS 27.1 SDK. It captures the beta-specific environment requirements, compatibility notes, and verification guidance that complement the framework-focused skills in this repository.

## Scope

- Xcode 27.1 beta includes Swift 6.4 and SDKs for iOS 27.1, iPadOS 27.1, tvOS 27, watchOS 27, macOS 27, and visionOS 27.
- Xcode 27.1 beta requires macOS Tahoe 26.6 or later.
- On-device debugging supports iOS 17 and later, tvOS 17 and later, watchOS 10 and later, and visionOS.
- Use the existing `swiftui-whats-new-27` skill for SwiftUI APIs introduced by the OS 27 SDKs; this skill is for Xcode 27.1 beta tooling and compatibility context.

## Workflow

1. Confirm the selected developer directory is the intended Xcode 27.1 beta installation with `xcodebuild -version`.
2. Export the installed built-in skills after selecting that Xcode:
   `xcrun agent skills export --replace-existing <destination>`
3. Prefer the narrowest relevant skill for source changes, then use this skill for Xcode 27.1 beta environment constraints.
4. For Mac Catalyst builds that use iOS 27.1-only APIs, isolate those APIs with `#if !targetEnvironment(macCatalyst)` in Swift or `#if !TARGET_OS_MACCATALYST` in Objective-C.
5. Validate on the intended simulator/device runtime; the first Simulator launch can take several minutes in this beta.

## Beta cautions

- iOS 27.1-specific APIs can produce Mac Catalyst compile errors when the same target is built for Mac Catalyst.
- Projects targeting iOS 27.1 may not expose a Mac Catalyst run destination; use a Mac Catalyst 27.0 minimum deployment as the documented workaround when appropriate.
- The iPhone Duo Simulator has beta limitations, including unavailable StandBy and limited app-extension debugging.

See [release-notes.md](references/release-notes.md) for the source-linked summary.
