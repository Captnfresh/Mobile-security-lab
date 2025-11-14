# Security Testing Methodology

## Mobile App Security Assessment

### 1. Static Analysis (Code Review)
- **Decompile APK** with JADX-GUI
- **Review AndroidManifest.xml** for permissions
- **Search for hardcoded secrets** (API keys, passwords)
- **Check certificate pinning** implementation
- **Review crypto implementations**

### 2. Dynamic Analysis (Runtime)
- **Monitor network traffic**
- **Test input validation**
- **Check for data leakage**
- **Test authentication bypass**

### 3. Using Injured Android App
The Injured Android app contains multiple CTF flags:
- **Flag One**: Hardcoded strings
- **Flag Two**: Insecure data storage
- **Flag Three**: Component exposure
- Continue through all 17 flags

### 4. Common Vulnerabilities to Find
- Insecure data storage
- Hardcoded credentials
- Weak SSL/TLS configurations
- Exposed app components
- Input validation issues
