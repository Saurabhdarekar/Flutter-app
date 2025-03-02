# flutter_blue_app

A Flutter application that uses the `flutter_bluetooth_serial` package.

## Table of Contents
- [Overview](#overview)
- [Running the Application](#running-the-application)
- [Building the APK](#building-the-apk)
- [Setting Up Android SDK (macOS)](#setting-up-android-sdk-macos)
- [Setting Up Android SDK (Windows)](#setting-up-android-sdk-windows)
- [Getting Started](#getting-started)
- [Additional Resources](#additional-resources)

## Overview

This project is a starting point for a Flutter application that integrates Bluetooth functionality using the `flutter_bluetooth_serial` package.

## Running the Application

1. **Add the Bluetooth Package Dependency**  
   In your project directory, run:
   ```bash
   flutter pub add flutter_bluetooth_serial:^0.4.0
   ```

2. **Get Dependencies**  
   Fetch the package:
   ```bash
   flutter pub get
   ```

3. **Create Necessary Files**  
   If needed, generate missing files:
   ```bash
   flutter create .
   ```

4. **Run the App**  
   Launch the application:
   ```bash
   flutter run
   ```

## Building the APK

1. **Set Up the Android SDK**  
   Follow the setup instructions below for your operating system.

2. **Clean and Build**  
   Once the SDK is configured, run:
   ```bash
   flutter clean
   flutter build apk --release
   ```

## Setting Up Android SDK (macOS)

### 1. Install Android Command-Line Tools
Open Terminal and install via Homebrew:
```bash
brew install android-commandlinetools
```

### 2. Create the Android SDK Directory
```bash
mkdir -p ~/Library/Android/sdk
```

### 3. Install Essential SDK Packages
```bash
sdkmanager --sdk_root=$HOME/Library/Android/sdk "platform-tools" "platforms;android-34" "build-tools;34.0.0" "cmdline-tools;latest"
```

### 4. Configure Environment Variables

#### For zsh (Default on macOS Catalina & later)
Edit your `~/.zshrc`:
```bash
nano ~/.zshrc
```
Add these lines at the end:
```bash
export ANDROID_HOME=$HOME/Library/Android/sdk
export ANDROID_SDK_ROOT=$HOME/Library/Android/sdk
export PATH=$ANDROID_HOME/emulator:$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$ANDROID_HOME/platform-tools:$PATH
```
Save and apply:
```bash
source ~/.zshrc
```

#### For bash
Edit your `~/.bashrc`:
```bash
nano ~/.bashrc
```
Add the same environment variables, then apply:
```bash
source ~/.bashrc
```

### 5. Verify the Installation
Check if Flutter detects the Android SDK:
```bash
flutter doctor
```
Resolve any issues that appear.

### 6. Run the Flutter Project
```bash
flutter run
```

## Setting Up Android SDK (Windows)

### 1. Install Android Command-Line Tools
1. Download the [Android Command Line Tools](https://developer.android.com/studio#command-tools).
2. Extract the downloaded ZIP to `C:\Android\cmdline-tools`.
3. Rename the extracted folder to `latest` so that your path becomes:
   ```
   C:\Android\cmdline-tools\latest
   ```

### 2. Install Essential SDK Packages
Open **Command Prompt** as Administrator, then run:
```batch
cd C:\Android\cmdline-tools\latest\bin
sdkmanager "platform-tools" "platforms;android-34" "build-tools;34.0.0" "cmdline-tools;latest"
```

### 3. Configure Environment Variables
1. Open **Start Menu** and search for **Environment Variables**. Click on **Edit the system environment variables**.
2. In the **System Properties** window, click **Environment Variables**.
3. Under **User variables**, add:
   - `ANDROID_HOME` = `C:\Android`
   - `ANDROID_SDK_ROOT` = `C:\Android`
4. Edit the **Path** variable and add:
   - `C:\Android\platform-tools`
   - `C:\Android\cmdline-tools\latest\bin`
   - `C:\Android\build-tools\34.0.0`

### 4. Verify the Installation
Restart **Command Prompt** and run:
```batch
flutter doctor
```
Address any missing dependencies as reported.

### 5. Run the Flutter Project
```batch
flutter run
```

## Getting Started

This project is a great starting point for your Flutter application. If you're new to Flutter, check out these resources:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

## Additional Resources

For more help with Flutter development, visit the [Flutter documentation](https://docs.flutter.dev/), which provides tutorials, samples, and a full API reference.

