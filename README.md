
# SendBird SyncManager for Android

[![Platform](https://img.shields.io/badge/platform-android-orange.svg)](https://github.com/sendbird/sendbird-syncmanager-android)
[![Languages](https://img.shields.io/badge/language-java-orange.svg)](https://github.com/sendbird/sendbird-syncmanager-android)
[![Maven](https://img.shields.io/badge/maven-v1.1.18-green.svg)](https://github.com/sendbird/sendbird-syncmanager-android/tree/master/com/sendbird/sdk/sendbird-syncmanager/1.1.18)
[![Commercial License](https://img.shields.io/badge/license-Commercial-brightgreen.svg)](https://github.com/sendbird/sendbird-syncmanager-android/blob/master/LICENSE.md)

SendBird SyncManager is chat data sync management add-on for SendBird. SyncManager offers an event-based data management framework so that each view would listen data event in event handler in order to update the view. And it stores the data into SQLite which implements local caching for faster loading.

## Requirements

- SendBird SyncManager works on Android 4.0+ (API level 14), Java 7+ and [SendBird Android SDK](https://github.com/sendbird/SendBird-SDK-Android) 3.0.96+.

## Install using Gradle

```
repositories {
    maven { url "https://raw.githubusercontent.com/sendbird/sendbird-syncmanager-android/master/" }
}
dependencies {
    // SyncManager
    implementation 'com.sendbird.sdk:sendbird-syncmanager:1.1.21'

    // SendBird
    implementation 'com.sendbird.sdk:sendbird-android-sdk:3.0.129'
}
```

## How it works

- For more information, please refer to [SyncManager Document](https://docs.sendbird.com/android/sync_manager_getting_started).

## Sample

- We provide sample project to understand `SyncManager` further. Check out [SyncManager sample](https://github.com/sendbird/SendBird-Android/tree/master/syncmanager).
