This is the local manifest and instructions for building CyanogenMod 11 (or AOSP ROMS) for Sony M2 (eagle) released in 2014

Please setup your build enviroment as instructed on the link below, only follow up to the "Get Prebuilt Apps" stage, after which you can follow instructions mentioned here.

http://wiki.cyanogenmod.org/w/Build_for_yuga

1) After getting the prebuilt apps move back to root cyanogenmod dir
```
cd ~/android/system
```

2) Get the local manifest
```
mkdir -p ~/android/system/.repo/local_manifests
curl https://raw.githubusercontent.com/M2Dev/local_manifest/blob/master/default.xml > ~/android/system/.repo/local_manifests/default.xml
```

3) repo sync (again) to download the additional repositories
```
repo sync -j8 --no-clone-bundle
```
4) Start the build process for the device you own
*Note: this takes a long time*
```
. build/envsetup.sh
```

```
  breakfast cm_eagle-userdebug
  brunch cm_eagle-userdebug
```

  
To run a sequential build simply run the ```breakfast``` and ```brunch``` commands again for your device.

To remove all compiled files after running ```brunch```, simply run ```make clean```

To get the latest patches from cyanogenmod run ```repo sync```
