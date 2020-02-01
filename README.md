# aosp-10

Scripts that build aosp 10 for xperia devices using linux kernel 4.9 or 4.14 and including opengapps.

Please be aware that these scripts are not appropriate for a developer aosp tree that contains
changes but should only be used on clean trees, since the script will do things like:
- delete files
- git hard resets
- git checkouts

For general build instructions how to setup and build aosp for xperia see:
https://developer.sony.com/develop/open-devices/guides/aosp-build-instructions

The scripts need to be adjusted for your build via setting these variables accordingly:
```
SOURCE=~/android/source
APK_DIR=~/android/apk
LUNCH_CHOICE=aosp_g8441-userdebug
PLATFORM=yoshino
DEVICE=lilac
```

For opengapps it is required to obtain the SetupWizard manually and provide it in APK_DIR.
The apk can be obtained from a pixel 10 image e.g. from coral:
https://developers.google.com/android/images

To download and extract the apk from the image use e.g. `extract-apks.sh` from this repository.
