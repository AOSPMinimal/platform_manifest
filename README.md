# AOSP Minimal Manifest #

#StayMinimal

## Credits: ##
- [**AOSP**](https://android.googlesource.com)
- [**LineageOS**](https://github.com/LineageOS)
- [**StormBreaker**](https://github.com/stormbreaker-project)

### Get started: ###

**Download the source code**
```bash
# Initialize local repository
repo init -u https://github.com/AOSPMinimal/platform_manifest -b aosp-12

# Initializa a shallow local repository "useful for saving space"
repo init -u https://github.com/AOSPMinimal/platform_manifest -b aosp-12 --depth=1

# Sync
repo sync -c --force-sync --no-tags --no-clone-bundle -j$(nproc --all) --optimized-fetch --prune
```

**Build the rom**
```bash
. build/envsetup.sh
lunch aosp_($Device)-userdebug
make bacon
```
