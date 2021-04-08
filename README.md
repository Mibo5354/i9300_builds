# LineageOS builds for i9300
#### Latest Build: 20210310 - March Security Update

###### Additional tweaks:
* Boeffla sound engine and charging control [[@andip71](https://github.com/andip71)]
   * Configure with [SmartPack Kernel Manager](https://play.google.com/store/apps/details?id=com.smartpack.kernelmanager.release) or with an init.d script ([example](https://forum.xda-developers.com/t/rom-unofficial-8-1-0-lineageos-15-1-beta-6-03-2019.3862953/page-12#post-78269922)).
* MagiskHide support, Passes SafetyNet
* Lower minimum brightness [[@Oebbler](https://github.com/Mibo5354/android_kernel_samsung_smdk4412/commit/0d207185ac260a6816760cae405b6941b2015918)]
* Forced disable Bluetooth absolute volume 
* Added OMS support [from [LineageSubstratum](https://github.com/LineageSubstratum)]. 
* OTA update support @ [rom.mibo5354.tk](https://rom.mibo5354.tk/builds/full/)
* Optional Experimental HWComposer [[@fourkbomb](https://forum.xda-developers.com/galaxy-s3/orig-development/experimental-lineageos-14-1-i9300-t3696500)]

###### Optional magisk modules
* [AptX codec support](https://github.com/Mibo5354/i9300_builds/raw/master/Magisk%20Modules/magisk-module-op3aptx.zip)
* [Stock Samsung boot animation](https://github.com/Mibo5354/i9300_builds/raw/master/Magisk%20Modules/magisk-samsung-stock-boot-animation.zip)
* [HWComposer enabler](https://github.com/Mibo5354/i9300_builds/raw/master/Magisk%20Modules/Systemless_HWC.zip)

###### TODO

[ ] Add sdcardfs support

###### Build command used
```
docker run \
    --name=i9300_build \
    -e "BRANCH_NAME=cm-14.1" \
    -e "DEVICE_LIST=i9300" \
    -e "SIGN_BUILDS=true" \
    -e "SIGNATURE_SPOOFING=no" \
    -e "CUSTOM_PACKAGES=FDroid FDroidPrivilegedExtension" \
    -e "OTA_URL=https://rom.mibo5354.tk/api" \
    -v "/home/user/lineageBuild/lineage:/srv/src" \
    -v "/home/user/lineageBuild/zips:/srv/zips" \
    -v "/home/user/lineageBuild/logs:/srv/logs" \
    -v "/home/user/lineageBuild/cache:/srv/ccache" \
    -v "/home/user/lineageBuild/keys:/srv/keys" \
    -v "/home/user/lineageBuild/manifests:/srv/local_manifests" \
    lineageos4microg/docker-lineage-cicd
```
