# LineageOS

Boot animation of LineageOS 21.0, extracted from [LineageOS 21.0 for hero2lte](https://xdaforums.com/t/lineageos-21-0-android-14-signature-spoofing-ota-updates-for-s7-edge-exynos.4655852)

## Install

1. Please backup your old `bootanimation.zip` at `/system/product/media/bootanimation.zip`

2. You can use ADB to do that:

```sh
adb root
adb pull /system/product/media/bootanimation.zip # or adb pull /product/media/bootanimation.zip
adb unroot
```

3. After that, download `bootanimation.zip` and put it to `/system/product/media`, then `chmod 644` it.

4. Reboot.
