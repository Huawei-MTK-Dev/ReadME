## 畅享5 Device使用
#### 同步源码
    repo init -u git://github.com/AospExtended/manifest.git -b 7.x  --depth=1
    repo sync -c -j128 --force-sync --no-clone-bundle --no-tags
    git clone http://github.com/LineageOS/android_packages_resources_devicesettings.git -b cm-14.1 packages/resources/devicesettings
#### 下载设备树编译
    git clone https://github.com/Huawei-MTK-Dev/android_device_huawei_titan.git -b 7.x device/huawei/tit
    cd device/huawei/tit/patches
    ./apply-patches.sh
    cd ../../../../
    git clone https://github.com/Huawei-MTK-Dev/proprietary_vendor_huawei.git -b cm-14.1 vendor/huawei
    source build/envsetup.sh
    lunch aosp_tit-userdebug
    make -j128 bacon showcommands 2>&1 | tee build.log
## 畅享5s Device使用
#### 同步源码
    repo init -u git://github.com/lineageos/android.git -b cm-14.1
    repo sync -j128
    git clone http://github.com/LineageOS/android_packages_resources_devicesettings.git -b cm-14.1 packages/resources/devicesettings
#### 下载设备树编译
    git clone https://github.com/rote66/android_device_HUAWEI_TAG_AL00.git -b los14.1 device/HUAWEI/TAG_AL00
    cd device/HUAWEI/TAG_AL00/patches
    ./apply-patches.sh
    cd ../../../../
    git clone https://github.com/rote66/android_vendor_HUAWEI_TAG_AL00.git -b los14.1 vendor/HUAWEI/TAG_AL00
    source build/envsetup.sh
    lunch lineage_TAG_AL00-userdebug
    make -j128 bacon showcommands 2>&1 | tee build.log
## 解锁
https://github.com/Huawei-MTK-Dev/Unlock

## 感谢
LineageOS
Divis1969
Oleg.svs
Moyster
Mad Team
danielhk
Wyk
s4704
