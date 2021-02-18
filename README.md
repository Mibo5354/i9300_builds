# LineageOS builds for i9300
#### Latest Build: 20210218 - February Security Update

###### Additional tweaks:
* Boeffla sound engine and charging control [pulled from ChronoMonochrome's lineage 15.1 repo]
* MagiskHide support, Passes SafetyNet
* Lower minimum brightness [Oebbler]
* Forced disable Bluetooth absolute volume 
* Added OMS support [from LineageSubstratum]. 
* OTA update support @ [rom.mibo5354.tk](https://rom.mibo5354.tk/builds/full/)
* Optional Experimental HWComposer [[@fourkbomb](https://forum.xda-developers.com/galaxy-s3/orig-development/experimental-lineageos-14-1-i9300-t3696500)]

###### Optional magisk modules
* AptX codec support
* Stock Samsung boot animation
* HWComposer enabler

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
