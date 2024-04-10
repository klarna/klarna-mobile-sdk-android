# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.6.16] - 2024-04-10
- Fixed class conflict issues due to obfuscation.
- Fixed conflicting FileProvider class manifest merger issue.

## [2.6.15] - 2024-04-04
- Added NA and OC region support for Sign in with Klarna.
- Added native support for sharing/opening file contents.
- Card scanning results are wiped from memory after usage in the scanning module.
- Minor bug fixes and improvements.

## [2.6.14] - 2024-02-29
- Bug fixes and stability improvements.

## [2.6.13] - 2024-02-08
- Updated development and build JDK to JDK 11 and AGP to AGP 7.
- Resolved an issue preventing Sign in with Klarna integration when using a non-AppCompat theme.
- Deleted several internal APIs that were mistakenly exposed in earlier versions.
- Implemented several internal improvements and optimizations to enhance performance and reliability.

## [2.6.12] - 2024-01-09
- Set the default variant of the SDK to basic.
- Implemented minor internal security fixes and improvements.

## [2.6.11] - 2023-12-18
- Fixed javascript code execution vulnerability.
- Added URL validations for SDK WebViews.
- Improved Sign in with Klarna Redirects with a separate Activity.
- Updated SDK User-Agents.
- Improved Activity referencing for view operations.
- Improved SDK monitoring.

## [2.6.10] - 2023-11-03
- Added system browser fallback support for Sign in with Klarna.
- Fixed On-site Messaging link click area.
- Changed default autoFinalize value to null for KlarnaPaymentView.

## [2.6.9] - 2023-09-05
- Changed the `launchMode` attribute for `KlarnaCustomTabActivity` from `singleTop` to `singleTask`
- Minor internal improvements.

## [2.6.8] - 2023-08-22
- Changed Sign in with Klarna button logo layout.
- Added support for loading indicator for Sign in with Klarna button.
- Improved performance by caching for Sign in with Klarna logins.
- Fixed text scaling issues for native buttons.
- Added support for skipping load calls in legacy tokenize flows.
- Added permission support for hybrid integrations.

## [2.6.7] - 2023-08-09
- Card scanning results are wiped from memory after usage.
- KlarnaPaymentView is made visible also on authorize call.

## [2.6.6] - 2023-07-27
- Fixed a proguard issue for fullscreen dialogs.

## [2.6.5] - 2023-07-06
- Fixed proguard issues for public Sign in with Klarna classes.
- Fixed an issue with cancelling dialogs with the back button.

## [2.6.4] - 2023-06-21
- Internal Browser now uses dialog fragments instead of an Activity.
- Fixed user cancel false-positives for Sign in with Klarna. 
- Fixed proguard issues for internal Sign in with Klarna data classes.

## [2.6.3] - 2023-05-26
- Fixed blank pages reporting error from background.
- Updated assets.
- Improved monitoring for application lifecycle.

## [2.6.2] - 2023-05-09
- Added support for permission handling in Separate Fullscreen.
- Fixed redirect URI validation for Sign in With Klarna.
- Removed max width and height limits for KlarnaSignInButton.

## [2.6.1] - 2023-04-21
- Fixed initial validation errors for KlarnaSignInButton.
- Internal optimization and improvements for Sign In With Klarna.

## [2.6.0] - 2023-04-11
- Added Sign in with Klarna integration.

## [2.5.2] - 2023-02-21
- Renamed internal assets of the SDK to fix conflicts with host applications.

## [2.5.1] - 2023-01-30
- Fixed OkHttp header encoding issues.
- Optimized internal OkHttpClient usage.

## [2.5.0] - 2023-01-19
- Added Klarna Express Button integration.

## [2.4.3] - 2023-01-13
- Bug fixes and stability improvements.

## [2.4.2] - 2022-12-19
- Use English locale in the SDK's internal string functions instead of device's/app's locale configuration.

## [2.4.1] - 2022-11-29
- Updated SDK assets for Klarna Payments.

## [2.4.0] - 2022-11-21
- Added support for Klarna Checkout in Standalone, Hybrid and WebView integrations.
- Added `KlarnaCheckoutView` extends `KlarnaSingleComponent` and `KlarnaStandaloneComponent`.

## [2.3.2] - 2022-10-26
- Improved handling of files and links.
- Removed network security config file.
- Improved debugging capabilities during development.
- Minor internal improvements.

## [2.3.1] - 2022-10-03
- Fixed fullscreen height issue with quick authorize calls for One Klarna payment flows.

## [2.3.0] - 2022-09-23
- Added `KlarnaComponent`. General class that envelops any Klarna Component, regardless of integration. 
- Added `KlarnaMultiComponent`. Components conforming to this interface protocol may render multiple products at once.
- Added `KlarnaStandaloneComponent`. For components that host and own their content. 
- Added `KlarnaSingleComponent`. Components conforming to this protocol render a single Klarna product at a time.
- Added `KlarnaEventHandler` interface. Provides methods that will notify events happening to a product in a Klarna component.
- Added `KlarnaStandaloneWebView` class.
- Added `KlarnaEnvironment` enum class.
- Added `KlarnaProduct` enum class.
- Added `KlarnaProductEvent` data class.
- Added `KlarnaOSMRegion` enum class.
- Added `KlarnaOSMTheme` enum class.
- Added public constructor to `KlarnaProductOptions` data class.

### Klarna Payments
- `KlarnaPaymentView` extends `KlarnaSingleComponent` and `KlarnaStandaloneComponent`.

### Hybrid
- `KlarnaHybridSDK` extends `KlarnaMultiComponent`.

### OSM
- `KlarnaOSMView` extends `KlarnaStandaloneComponent` and `KlarnaSingleComponent`.
#### Deprecations
- `KlarnaOSMEnvironment` is deprecated. Use `KlarnaEnvironment` instead.
- `KlarnaOSMRegion` is deprecated. Use `KlarnaRegion` instead.
- `KlarnaOSMTheme` is deprecated. Use `KlarnaTheme` instead.

### Post Purchase
- `KlarnaPostPurchaseSDK` extends `KlarnaSingleComponent` and `KlarnaComponent`.
#### Deprecations
- `KlarnaPostPurchaseEnvironment` is deprecated. Use `KlarnaEnvironment` instead.
- `KlarnaPostPurchaseRegion` is deprecated. Use `KlarnaRegion` instead.

## [2.2.1] - 2022-08-19
- KlarnaOSMView has been made an open class.

## [2.2.0] - 2022-07-13
- Added Post Purchase standalone integration.

## [2.1.8] - 2022-06-02
- Added checks for WebView availability on the device.
- Allow verbose logs in debug mode.

## [2.1.7] - 2022-05-04
- Added support for opening Custom Tabs.

## [2.1.6] - 2022-03-23
- Added support for "One Klarna" payment flow.
- Minor bug fixes and improvements.

## [2.1.5] - 2022-02-11
- Updated application lifecycle implementation.
- Disabled some proguard optimizations.
- Changed proguard rules to apply obfuscation in consumer builds for some core parts.

## [2.1.4] - 2022-02-10
- Updated consumer proguard rules to prevent detected obfuscation issues.

## [2.1.3] - 2022-01-24
- Fixed an issue with opening external apps from internal browser.

## [2.1.2] - 2022-01-18
- Fixed an issue caused by render process crash in WebViews.

## [2.1.1] - 2021-12-03
- Fixed an issue while creating an instance of the SDK in background thread.

## [2.1.0] - 2021-11-12
- Improved support for 3DSecure flows in new markets.
- Added "returnURL" to the `KlarnaPaymentView` constructor parameters. [Read more.](https://docs.klarna.com/in-app/inapp-android-overview/klarna-payments-native/)
- Deprecated `KlarnaHybridSDKCallback` and added separate callbacks for events and fullscreen transitions. [Read more.](https://docs.klarna.com/in-app/inapp-android-overview/hybrid/)
- Internal optimization and improvements.

## [2.0.44] - 2021-07-23
- Change hardware requirements to be optional.

## [2.0.43] - 2021-07-13
- Improve transition animation to/from full screen content.
- Added support to open Klarna App in Android API level 30.

## [2.0.42] - 2021-06-28
- Improve internal parts using random integers and UUIDs.
- Fix string resources with special characters.

## [2.0.41] - 2021-06-14
- Replaced the default SDK variant to include all features just like the full variant. SDK variant supporting limited features with a smaller size will be the basic variant starting with this version.

## [2.0.40] - 2021-06-01
- Permissions & WebRTC support.
- Improved fullscreen implementation.

## [2.0.39] - 2021-05-25
- Reduce singletons for less memory usage.
- Improve internal error handling.

## [2.0.38] - 2021-05-12
- Support JS Bridge caching.
- Internal optimization and improvements.

## [2.0.37] - 2021-04-23
- Support for alternative resource endpoints

## [2.0.36] - 2021-04-15
- Fullscreen keyboard improvements.
- Updated analytic events.

## [2.0.35] - 2021-03-22
- Revert WebRTC support and fullscreen improvements.

## [2.0.34] - 2021-03-11
- :warning: **This version has some functionality issues**: Please use a newer version of the SDK. Future releases with new features will be cautiously checked to prevent these warnings.
- WebRTC support.
- Improved fullscreen implementation.

## [2.0.33] - 2021-02-18
- Internal optimizations.
- Fix obfuscation errors.

## [2.0.32] - 2021-01-13
- Internal optimizations.
- Updated SDK resources to prevent conflicts.
- Migrated dependencies to AndroidX.

## [2.0.31] - 2020-12-08
- Internal optimizations and stability improvements.

## [2.0.30] - 2020-12-03
- Overall stability improvements.

## [2.0.29] - 2020-11-04
- Fixed an issue with Post Purchase in Hybrid integration.
- Overall stability improvements.

## [2.0.28] - 2020-10-21
- Fix compile-time errors for some dependencies.

## [2.0.27] - 2020-10-20
- Minor stability improvements and bug fixes.

## [2.0.26] - 2020-10-19
- Overall stability improvements and bug fixes.

## [2.0.25] - 2020-09-03
- Upgraded the target Android SDK version to 30
- Enabled the file access for web views on Android SDK version 30 and above

## [2.0.24] - 2020-08-12
- Basic support for static On site marketing - beta version

## [2.0.23] - 2020-07-29
- Added callback API for merchant events from Klarna components inside a WebView.

## [2.0.22] - 2020-07-14
- Improved API for Java applications.
- Fixed an issue with base64 encoding.
- Improved thread safety for WebView implementations.

## [2.0.21] - 2020-06-17
- Fixed an issue with internal browser URL parameter and navigation.

## [2.0.20] - 2020-06-05
- Fixed an issue when the payment view was having blank white space.

## [2.0.19] - 2020-05-27
- Full artifact with card scan.
- Default/basic artifact without card scan.

## [2.0.18] - 2020-05-22
- Removed `READ_PHONE_STATE` permission usage and requirement.

## [2.0.17] - 2020-05-14
- Fixed an issue with the `Context` instance being used to move or create separate web views.

## [2.0.16] - 2020-04-09
- Fixed an issue with showing an error message inside the web view without hiding it.

## [2.0.15] - 2020-03-20
- Fix issue with showing fullscreen, primarily affecting post purchase widgets.

## [2.0.14] - 2020-02-21
- Overall performance and error handling improvements.

## [2.0.13] - 2020-02-17
- Fixed a crash with `JSONException` in `WrapperManager` when initializing the SDK.

## [2.0.12] - 2020-01-30
- Fixed a Proguard issue that would cause the payment view to not load.

## [2.0.11] - 2020-01-28
- Internal optimizations.

## [2.0.10] - 2020-01-14
- Enabled cookies for internal web views.

## [2.0.9] - 2019-12-19
- Renamed internal assets to avoid merchant app conflicts.

## [2.0.8] - 2019-12-05
- Improvements of internal web view identification towards Klarna components.

## [2.0.7] - 2019-11-27
- Fix rare crash with `NullPointerException` when invalid message is sent to the SDK.

## [2.0.6] - 2019-11-20
- Fix rare crash on certain Android devices with `JSONException` in `ConfigManager` when initializing the SDK.
- Improved link handling in fullscreen web views.
