CM11 for Xperia M2
==============

The local manifests for building CM11 for Sony Xperia M2.

To sync:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-11.0
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/M2Dev/local_manifest/common/local_manifest.xml
    repo sync
    sh vendor/cm/get-prebuilts
    . build/envsetup.sh
    brunch cm_eagle-userdebug
