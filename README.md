# [Sendbird](https://sendbird.com) SyncManager for Android

[![Platform](https://img.shields.io/badge/platform-android-orange.svg)](https://github.com/sendbird/sendbird-syncmanager-android)
[![Languages](https://img.shields.io/badge/language-java-orange.svg)](https://github.com/sendbird/sendbird-syncmanager-android)
[![Maven](https://img.shields.io/badge/maven-v1.1.31-green.svg)](https://github.com/sendbird/sendbird-syncmanager-android/tree/master/com/sendbird/sdk/sendbird-syncmanager/1.1.31)
[![Commercial License](https://img.shields.io/badge/license-Commercial-brightgreen.svg)](https://github.com/sendbird/sendbird-syncmanager-android/blob/master/LICENSE.md)

## Table of contents

  1. [Introduction](#introduction)
  1. [Before getting started](#before-getting-started)
  1. [Getting started](#getting-started)

<br />

## Introduction

**Sendbird SyncManager** for Android is a [Chat SDK](https://github.com/sendbird/SendBird-SDK-Android) add-on that optimizes the user caching experience by interlinking the synchronization of the local data storage with the chat data in Sendbird server through an event-driven structure.

### How it works

SyncManager leverages local caching and synchronizes the chat data between the local storage and Sendbird server. By handling the operations in an event-driven structure, the add-on provides a simplified Chat SDK integration and a better user experience. 

### Operations

- **Background sync** occurs whenever there is a connection and automatically stores data fetched from Sendbird server into the local cache. 
- **Real time sync** occurs all the time; it identifies, stores, and delivers the real-time events received from WebSocket connection. 
- **Offline mode** ensures your client app is operational during offline mode, meaning that even without background sync, the view can display cached data. 

### More about Sendbird SyncManager for Android

Find out more about Sendbird SyncManager for Android on [SyncManager for Android doc](https://sendbird.com/docs/syncmanager/v1/android/getting-started/about-syncmanager). If you have any comments or questions regarding bugs and feature requests, visit [Sendbird community](https://community.sendbird.com). 

<br />

## Before getting started

This section shows the prerequisites you need to check to use Sendbird SyncManager for Android.

### Requirements 

The minimum requirements for SyncManager for Android are:

- `Android 4.0 (API level 14) or higher`
- `Java 8 or higher`
- `Sendbird Chat SDK for Android 3.0.158 or higher` (3.0.158 is embedded in SyncManager 1.1.31. If you want to use a higher version, you can directly declare a dependency on the higher version.)


<br />

## Getting started

This section gives you information you need to get started with Sendbird SyncManager for Android. 

### Try the sample app

Download the sample app to test the core features of SyncManager for Android. 

- https://github.com/sendbird/SendBird-Android/tree/master/syncmanager

> **Note**: The fastest way to test our SyncManager is to build your chat app on top of our sample app. Make sure to change the application ID of the sample app to your own. Go to the [Create a Sendbird application from your dashboard section](#step-1-create-a-sendbird-application-from-your-dashboard) to learn more.

### Step 1: Create a Sendbird application from your dashboard

A Sendbird application comprises everything required in a chat service including users, message, and channels. To create an application:

1. Go to the Sendbird Dashboard and enter your email and password, and create a new account. You can also sign up with a Google account.
2. When prompted by the setup wizard, enter your organization information to manage Sendbird applications.
3. Lastly, when your dashboard home appears after completing setup, click **Create +** at the top-right corner.

Regardless of the platform, only one Sendbird application can be integrated per app; however, the application supports communication across all Sendbird’s provided platforms without any additional setup. 

> **Note**: All the data is limited to the scope of a single application, thus users in different Sendbird applications are unable to chat with each other. 

### Step 2: Download SyncManager for Android

Sendbird SyncManager currently supports iOS, Android, and JavaScript SDKs. You can download SyncManager for Android from our repository on GitHub.

### Step 3: Install SyncManager for Android

Installing the SyncManager SDK is simple if you're familiar with using external libraries or SDKs. First, add the following code to your **root** `build.gradle` file:

```gradle
allprojects {
    repositories {
        ...
        maven { url "https://repo.sendbird.com/public/maven" }
    }
}
```

>**Note**: Make sure the above code block isn't added to your module `bundle.gradle` file.

Then, add the dependency to the project's top-level `build.gradle` file.

```gradle
dependencies {
    // SyncManager SDK for Android (Latest, embeds Sendbird Chat SDK 3.0.158)
    implementation 'com.sendbird.sdk:sendbird-syncmanager:1.1.31'

    // Chat SDK for Android (If you want to use higher version than the version embedded in the SyncManager)
    implementation 'com.sendbird.sdk:sendbird-android-sdk:3.0.160'
}
```

> **Note**: SyncManager SDK versions `1.1.30` or lower can be downloaded from JCenter until February 1, 2022. SDK versions higher than `1.1.30` will be available on Sendbird's remote repository.
