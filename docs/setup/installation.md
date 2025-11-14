# Installation Guide

## Step 1: Install Java JDK 11

### Download JDK
1. Visit [Oracle JDK 11 Downloads](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
2. Create a free Oracle account if required
3. Download `jdk-11.0.x_windows-x64_bin.exe`
4. Run the installer as Administrator

### Verify Installation
```cmd
java -version
```

### Expected output
```
java version "11.0.x" 2024-XX-XX LTS
Java(TM) SE Runtime Environment 18.9
```


# Installation Guide

## Step 1: Install Java JDK 11
Download from: https://www.oracle.com/java/technologies/javase-jdk11-downloads.html
Run installer as Administrator
Verify: `java -version`

## Step 2: Install JADX-GUI
Download from: https://github.com/skylot/jadx/releases/tag/v1.2.0
Extract to C:\jadx\
Test: Run C:\jadx\bin\jadx-gui.bat

## Step 3: Install ADB Tools
Download from: https://developer.android.com/studio/releases/platform-tools
Extract to C:\Windows\platform-tools\
Verify: `adb version`
Fix PATH if needed: `set PATH=%PATH%;C:\Windows\platform-tools`

## Step 4: Install Docker Desktop
Download from: https://www.docker.com/products/docker-desktop
Run installer as Administrator
Verify: `docker --version`

## Step 5: Pull Android Image
`docker pull budtmo/docker-android:emulator_12.0`
Verify: `docker images`

## Step 6: Run Android Container
`docker run -d -p 6080:6080 -p 5555:5555 -e EMULATOR_DEVICE="Samsung Galaxy S10" -e WEB_VNC=true --device /dev/kvm --name android-container budtmo/docker-android:emulator_12.0`
Verify: `docker ps`

## Step 7: Access Android Emulator
Open browser to: `http://localhost:6080`
Click "Connect"
Wait 3-5 minutes for boot

## Step 8: Connect ADB
`adb connect localhost:5555`
`adb devices`

## Step 9: Test Android System
`adb shell getprop ro.build.version.release`
`adb shell ls /sdcard/`

