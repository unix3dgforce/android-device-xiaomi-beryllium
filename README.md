For building TWRP for Xiaomi Pocophone F1

TWRP device tree for Xiaomi Pocophone F1





Xiaomi Mi MI 8 Explorer Edition was announced and released in June 2018.

## Device specifications

| Device        | Xiaomi Pocophone F1                                 |
| -----------:  | :--------------------------------------------- |
| SoC           | Qualcomm SDM845 Snapdragon 845                 |
| CPU           | 4x2.8 GHz Kryo 385 Gold & 4x1.8 GHz Kryo 385 Silver           |
| GPU           | Adreno 630                                     |
| Memory        | 6GB / 8GM RAM (LPDDR4X)                        |
| Shipped Android version | 8.1                                  |
| Storage       | 64GB / 128GB / 256GB UFS 2.1 flash storage     |
| Battery       | Non-removable Li-Po 4000 mAh                   |
| Dimensions    | 155.5 x 75.3 x 8.8 mm                          |
| Display       | 1080 x 2246 (18.7:9) 6.18 inch                 |
| Rear camera 1 | 12 MP, f/1.9 Dual LED flash                    |
| Rear camera 2 | 5 MP, f/2.0                                    |
| Front camera  | 20 MP, f/2.0                                    |

## Device picture

![Xiaomi Mi 8 Explorer Edition ](https://vistanews.ru/uploads/posts/2018-08/1533623393_xiaomi-pocophone-f1-52-1.jpg)

## Features

Works:

- ADB
- Decryption of /data
- Screen brightness settings
- Now UI is very smooth (thanks to TWRP fix 16d831bee5a660f5ac6da0d8fff2b3ec4697d663)
- Vibration on touch (see https://gerrit.omnirom.org/#/c/android_bootable_recovery/+/31021/)
- Correct screenshot color (see https://gerrit.omnirom.org/#/c/android_bootable_recovery/+/31042/)
Finally execute these:

```
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch omni_beryllium-eng 
mka recoveryimage
```

To test it:

```
fastboot boot out/target/product/beryllium/recovery.img