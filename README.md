# TWRP Recovery for Infinix X663/X663c 📱

Custom TWRP Recovery builds for Infinix X663/X663c devices by VBS.

## ⚠️ Important Notes

### For X663 (v363 firmware):
- This build is **ONLY** for X663 model with v363 firmware
- Remove screen lock before flashing
- Ensure proper firmware version to avoid issues

### For X663c (v328 firmware):
- This build is **ONLY** for X663c model with v328 firmware
- Remove screen lock before flashing
- Ensure proper firmware version to avoid issues

## 📋 Prerequisites

- USB Debugging enabled on device
- Unlocked bootloader
- Magisk uninstalled (if previously installed)
- ADB and Fastboot tools installed on PC
- USB drivers installed

## 📥 Downloads

- [blank_vbmeta.img](blank_vbmeta.img)
- [twrp1_X663a12_v363.img](twrp1_X663a12_v363.img) (For X663 v363)
- [twrp3_note12_fwv328.img](twrp3_note12_fwv328.img) (For X663c v328)

## 📱 Installation Guide

### For X663 (v363 firmware):

1. Connect device to PC in USB debugging mode
2. Open terminal/command prompt and enter:
```bash
adb reboot bootloader
```
3. Flash vbmeta:
```bash
fastboot --disable-verity --disable-verification flash vbmeta blank_vbmeta.img
```
4. Flash TWRP:
```bash
fastboot flash boot twrp1_x663a12_v363.img
```
5. Reboot device:
```bash
fastboot reboot
```
6. Reconnect device and enter TWRP:
```bash
adb reboot recovery
```
7. In TWRP:
   - Flash stock boot.img in boot partition
   - Flash twrp1_x663a12_v363.img in ramdisk
8. Reboot to system
9. (Optional) Flash Magisk.zip in TWRP for root access

### For X663c (v328 firmware):

1. Connect device to PC in USB debugging mode
2. Open terminal/command prompt and enter:
```bash
adb reboot bootloader
```
3. Flash vbmeta:
```bash
fastboot --disable-verity --disable-verification flash vbmeta blank_vbmeta.img
```
4. Flash TWRP:
```bash
fastboot flash boot twrp3_note12_fwv328.img
```
5. Reboot device:
```bash
fastboot reboot
```
6. Reconnect device and enter TWRP:
```bash
adb reboot recovery
```
7. In TWRP:
   - Flash stock boot.img in boot partition
   - Flash twrp3_note12_fwv328.img in ramdisk
8. Reboot to system
9. (Optional) Flash Magisk.zip in TWRP for root access

## ✨ Changelog

- Fixed internal storage detection
- Fixed TWRP booting to decrypt page at startup
- Fixed Magisk flashing issues
- Various stability improvements

## 👨‍💻 Credits

- **Developer**: VBS
- **Repository**: [TWRP-X663](https://github.com/vbs/TWRP-X663)

## 📞 Support

For support and queries:
- Telegram: [@vbs_1](https://t.me/vbs_1)
- Support Group: [Infinix Note 11/12](https://t.me/infinix_note_11_12)

## ⚠️ Disclaimer

- This is a custom recovery. Flash at your own risk.
- Make sure to backup your data before proceeding.
- Developer is not responsible for any damage to your device.
