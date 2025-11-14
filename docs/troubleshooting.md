**YES! HERE'S THE COMPLETE TROUBLESHOOTING.MD IN ONE MARKDOWN BLOCK:**

```
# Troubleshooting Guide

## Common Errors & Solutions

### Docker Errors

#### Error: KVM Device Missing
```
docker: Error response from daemon: error gathering device information while adding custom device "/dev/kvm": no such file or directory
```
**Solution:** Remove `--device /dev/kvm` from the docker run command or use Android 12 image

#### Error: Container Name Conflict
```
Conflict. The container name "/android-container" is already in use
```
**Solution:** 
```cmd
docker rm -f android-container
```

#### Error: Container Created But Not Running
Container shows `STATUS: Created` but not `Up`
**Solution:** Check Docker Desktop is running, restart Docker

### ADB Errors

#### Error: ADB Not Recognized
```
'adb' is not recognized as an internal or external command
```
**Solution:** 
```cmd
set PATH=%PATH%;C:\Windows\platform-tools
```

#### Error: ADB Connection Failed
```
failed to connect to localhost:5555
```
**Solution:** Wait 3-5 minutes for Android to boot inside container

#### Error: Multiple Devices
```
adb.exe: more than one device/emulator
```
**Solution:** 
```cmd
adb -s localhost:5555 shell [command]
```

### Virtualization Errors

#### Error: KVM Not Supported
```
INFO: Your CPU does not support KVM extensions
```
**Solution:** Enable virtualization in BIOS or use Android 12 without KVM

#### Error: Virtualization Disabled
```
VirtualizationFirmwareEnabled: FALSE
```
**Solution:** Enter BIOS → Enable Intel VT-x/AMD-V → Save & Restart

### Android Boot Errors

#### Error: Device Service Crashed
```
WARN exited: device (exit status 1; not expected)
```
**Solution:** Android OS crashed - try different Android version or remove KVM flag

#### Error: ADB Device Offline
```
localhost:5555  offline
```
**Solution:** Android not fully booted - wait longer or check container logs

## Pro Tips
- Start the lab early - troubleshooting takes time
- Use Android 12 instead of Android 11
- Allocate more RAM with `-m 4g` if needed
- Physical Android phone works 100% if Docker fails
```


