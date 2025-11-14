# APK Analysis with JADX-GUI

## Step-by-Step APK Analysis

### 1. Extract APK from Android
```cmd
# Find the package name
adb shell pm list packages | findstr injured

# Get APK path
adb shell pm path b3nac.injuredandroid

# Pull APK to PC
adb pull /data/app/~~XRKrOiGruWotykaIJ5g1kw==/b3nac.injuredandroid-8QGAHzKr_j5THs5XWoqoNA==/base.apk C:\Users\PC\Desktop\InjuredAndroid.apk
```

2. Analyze with JADX-GUI

    Open JADX-GUI

    File → Open → Select your APK

    Explore the decompiled code

3. Key Areas to Examine

    AndroidManifest.xml: App permissions and components

    MainActivity.java: App entry point

    String resources: Hardcoded values

    Network security config: SSL/TLS settings

4. Common Security Findings

    Hardcoded API keys

    Insecure data storage

    Weak encryption

    Exposed endpoints
