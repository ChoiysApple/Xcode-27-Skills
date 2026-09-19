# Xcode 27.1 Beta Release Notes

Source: [Apple — Xcode 27.1 Beta Release Notes](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_1-release-notes)

## Toolchain

- Swift 6.4.
- iOS 27.1 and iPadOS 27.1 SDKs.
- tvOS 27, watchOS 27, macOS 27, and visionOS 27 SDKs.
- Requires macOS Tahoe 26.6 or later.

## Compatibility and known issues

### Mac Catalyst

Projects using APIs specific to iOS 27.1 can fail to compile for Mac Catalyst. Isolate those APIs with `#if !targetEnvironment(macCatalyst)` in Swift or `#if !TARGET_OS_MACCATALYST` in Objective-C.

Projects targeting iOS 27.1 may not show a Mac Catalyst run destination. Apple documents using a Mac Catalyst 27.0 minimum deployment as a workaround.

### Previews

The canvas overrides picker includes a Display group for previewing content on an alternative device display.

### Simulator

The initial Simulator launch may take several minutes. StandBy is unavailable in the iPhone Duo Simulator runtime, and most app extensions cannot be run or debugged there.
