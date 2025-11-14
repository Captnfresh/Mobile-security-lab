# ADB (Android Debug Bridge)

## What is ADB?
ADB is a command-line tool that lets your PC communicate with Android devices.

## Purpose in Mobile Security
- Extract APK files from devices/emulators
- Install/uninstall apps
- Access Android shell commands
- Transfer files between PC and Android

## Key Commands for Security
```cmd
adb devices                          # List connected devices
adb connect localhost:5555          # Connect to emulator
adb shell pm list packages          # List installed apps
adb shell pm path <package>         # Find APK location
adb pull /path/to/apk ./            # Extract APK to PC
adb install app.apk                 # Install APK
