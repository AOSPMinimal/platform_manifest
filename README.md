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
lunch ($Device)-userdebug
make bacon
```

#### Warning ####
As this rom is born to be an experiment, i don't like to see someone buildbotting this and saying "WhY tHiS rOm DoEsN't BoOt ??, AuDiO/dIsPlAy/MeDiA Is DeAd SuR, hOw I cAn FiX iT ??, and similar", is just because you have nothing to do 

Mostly is because of some changes i've hardcoded to work with my device

```bash
- Make sure to adapt this for your device https://github.com/AOSPMinimal/platform_vendor_aosp/commit/020786113b0adb857902b3b8b29c0499d4967f7d

- also https://github.com/AOSPMinimal/platform_vendor_qcom_opensource_power/blob/aosp-12/Android.mk#L34

- also drop project pathmap on your hals "like https://github.com/ItsVixano/hardware_qcom-caf/commit/3278ed4a4d3646238702404816377abfa27ed91c"

- and **USE PREBUILT KERNEL AND HEADERS**
```

Also, i won't recruit any maintainers so don't spam me if you want to maintain this rom "Officially"
