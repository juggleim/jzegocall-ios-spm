# JZegoCall iOS (Swift Package)

This repository distributes JZegoCall, the Zego call plugin for the JuggleIM iOS SDK, through Swift Package Manager.
SDK source code and issues live in [imsdk-ios](https://github.com/juggleim/imsdk-ios).

## Installation

In Xcode: **File > Add Package Dependencies…**, enter the repository URL:

```
https://github.com/Juggleim/jzegocall-ios-spm
```

Choose **Up to Next Major Version** from `1.10.1` and add the `JZegoCall` library to your app target.
It brings in JuggleIM and Zego SDK automatically.

Or in `Package.swift`:

```swift
dependencies: [
    .package(url: "https://github.com/Juggleim/jzegocall-ios-spm", from: "1.10.1")
],
targets: [
    .target(name: "YourApp", dependencies: [
        .product(name: "JZegoCall", package: "jzegocall-ios-spm")
    ])
]
```

JZegoCall 1.10.1 works with JuggleIM 1.10.1 or later within the same major version (below 2.0.0), and requires ZegoExpressEngine 3.22.0 (github.com/zegolibrary/express-video-ios).
If your app also depends on `juggleim-ios-spm` directly, any version in that range works, so JuggleIM can be upgraded without changing this package.

Requirements: iOS 12.0 or later.

## Usage

JuggleIM loads the Zego engine automatically once JZegoCall is linked into your app; no import is needed.

## License

Copyright © JuggleIM. See [LICENSE](./LICENSE).
