## Setup

- Get an API Key at [https://cloud.google.com/maps-platform/](https://cloud.google.com/maps-platform/)

- Enable Maps SDK for Android, Maps SDK for iOS, and Directions API.

- Add your API Key to the specified files

`android/app/src/main/AndroidManifest.xml`

```xml
<manifest ...
  <application ...
    <meta-data android:name="com.google.android.geo.API_KEY"
               android:value="AIzaSyBeOyY9O2d-W3GzzGcEiUJf1dD5GqJRfjs"/>
```

`ios/Runner/AppDelegate.swift`

```swift
import UIKit
import Flutter
import GoogleMaps

@UIApplicationMain
@objc class AppDelegate: FlutterAppDelegate {
  override func application(
    _ application: UIApplication,
    didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
  ) -> Bool {
    GMSServices.provideAPIKey("AIzaSyBeOyY9O2d-W3GzzGcEiUJf1dD5GqJRfjs")
    GeneratedPluginRegistrant.register(with: self)
    return super.application(application, didFinishLaunchingWithOptions: launchOptions)
  }
}
```

`lib/.env.dart`

```
const String googleAPIKey = 'AIzaSyBeOyY9O2d-W3GzzGcEiUJf1dD5GqJRfjs';
```
