Samsung Tab A 10.5 2018 GTA2XLWIFI SHRP Recovery sTree

# How to build
1. Set up the build environment by following intructions from [here](https://shrp.github.io/#/guide?id=build-shrp)

2. In the root folder of cloned synced shrp source clone the device tree:
```
git clone -b android_10 https://github.com/lsswizard/shrp_device_samsung_gta2xlwifi.git device/samsung/gta2xlwifi
```
3. To build:
```
. build/envsetup.sh && lunch omni_gta2xlwifi-eng && mka recoveryimage -j128
```

## Note
All the scripts are written in according to bash format so consider using bash shell while building.
You can switch to bash shell just by typing ```bash``` command and logout from it by ```exit``` after you complete the build.

Source uses ```python2``` and it may give you some syntax error for if you have ```python3```. So install python2 and use following command to activate ```python2``` for building: 
```
virtualenv -p /usr/bin/python2 xyz && source xyz/bin/activate
```
You need virtualenv package to be installed. (Tested on Ubuntu, use ```virtualenv2``` in arch based linux distros.)
