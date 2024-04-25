Recovery Device Tree for Redmi 12
===========================================

The Redmi 12 is a budget range smartphone from Redmi, Released 2023, June 15

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
OS	    | Android 13, MIUI 14.x.xx.x
CPU     | Octa-core (2x2.0 GHz Cortex-A75 & 6x1.8 GHz Cortex-A55)
Chipset | MediaTek Helio G88 (12nm)
GPU     | Mali-G52 MC2
Memory  | 4GB/8GB RAM
Storage | 128GB/256GB
MicroSD | microSDXC (dedicated slot)
Battery | Non-removable Li-Ion 5000 mAh battery
Resolution | 1080 x 2400 pixels, 20:9 ratio (~405 ppi density)
Camera (Rear)  | 50 MP, f/1.8, (wide), PDAF, 8 MP, f/2.2, 120˚ (ultrawide), 2 MP, f/2.4, (macro) 
Rear Camera Features | LED flash, HDR,
Video	| 1080p@30fps	
Camera (Front)  | 8 MP, f/2.0, (wide)
Features| Fingerprint (side-mounted), accelerometer, proximity, compass


## Device picture

![Redmi 12](https://akm-img-a-in.tosshub.com/aajtak/images/story/202307/redmi_12-sixteen_nine_0.jpg?size=948:533 "Redmi 12")

## How To Build?

First You Need Make Workspace Directory
---------------
```bash
mkdir workdir
cd workdir
```

And You Need Clonned Source Pitch Black Recovery Project
---------------
```bash
repo init -u https://github.com/PitchBlackRecoveryProject/manifest_pb -b android-12.1
```

If You Wan't to shallow clone, which will save even more space, Use This Command
---------------
```bash
repo init --depth=1 -u https://github.com/PitchBlackRecoveryProject/manifest_pb -b android-12.1
```

###### And Wait Sync Until Completed

You Need Clonned This Device Tree
---------------
```bash
git clone https://github.com/YudhoPatrianto/recovery_device_xiaomi_fire -b 14-pbrp device/xiaomi/fire
```

Final! Time To Build
---------------
```bash
source build/envsetup.sh
lunch pb_fire-eng
mka bootimage -j$(nproc --all)
```

After Completed You Can Find File In : /workdir/out/target/product/fire/boot.img



