# behavior-score-ios

Kalapa Behavior Score SDK for iOS captures in-app behavioral signals to support credit risk assessment and fraud detection. Distributed as an XCFramework via CocoaPods.

| | |
|---|---|
| Latest version | `1.4.0` |
| Minimum iOS | 12.0 |
| Swift | 5.0+ |
| Tested with | Xcode 26, CocoaPods 1.16 |

---

## Installation with CocoaPods

### 1. Add the pod to your `Podfile`

```ruby
platform :ios, '13.0'

target 'YourApp' do
  use_frameworks!

  pod 'KalapaScoreSDK', '~> 1.4.0'
end
```

`~> 1.4.0` accepts patch updates (`1.4.x`) but not the next minor version. Use `'1.4.0'` to pin the exact version.

### 2. Install

```bash
pod install --repo-update
```

`--repo-update` refreshes your local CocoaPods index so a newly released version is found. Later installs can use plain `pod install`.

From now on, open `YourApp.xcworkspace` instead of `YourApp.xcodeproj`.

### 3. Import

```swift
import KalapaScoreSDK
```

### Updating the SDK

```bash
pod update KalapaScoreSDK
```

---

## Troubleshooting

**`pod install` fails with `Unable to find a specification for KalapaScoreSDK`**

Your local CocoaPods index is out of date. Run:

```bash
pod install --repo-update
```

**Warning: `The iOS Simulator deployment target 'IPHONEOS_DEPLOYMENT_TARGET' is set to 11.0`**

Current Xcode versions only build for iOS 12.0 and later. Set `platform :ios, '12.0'` or higher in your `Podfile`.
