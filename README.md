# LineageOS builds for i9300
#### Latest Build: 202006010 - June Security Update

###### Additional tweaks:
* Boeffla sound engine and charging control [pulled from ChronoMonochrome's lineage 15.1 repo]
* Lower minimum brightness [Oebbler]
* Forced disable Bluetooth absolute volume 
* Added OMS support [from LineageSubstratum]. 
* OTA update support @ [mibo.computer](http://mibo.computer/builds/full/)

###### Optional magisk modules
* AptX codec support
* Stock Samsung boot animation

###### TODO

[ ] Add sdcardfs support

[ ] Add MagiskHide support

###### Build command used
```
docker run \
    --name=i9300_build \
    -e "BRANCH_NAME=cm-14.1" \
    -e "DEVICE_LIST=i9300" \
    -e "SIGN_BUILDS=true" \
    -e "SIGNATURE_SPOOFING=no" \
    -e "CUSTOM_PACKAGES=FDroid FDroidPrivilegedExtension" \
    -e "OTA_URL=http://152.67.97.3/" \
    -v "/home/user/lineageBuild/lineage:/srv/src" \
    -v "/home/user/lineageBuild/zips:/srv/zips" \
    -v "/home/user/lineageBuild/logs:/srv/logs" \
    -v "/home/user/lineageBuild/cache:/srv/ccache" \
    -v "/home/user/lineageBuild/keys:/srv/keys" \
    -v "/home/user/lineageBuild/manifests:/srv/local_manifests" \
    lineageos4microg/docker-lineage-cicd
```
