# LENOVO-B41-80 Hackintosh
- Lenovo B41-80
- 6th Gen Intel(R) Core(TM) i5-6200U
- DDR3L 1600 16GB (8GB+8GB)
- BCM94360z4
- MacBookPro13,1
- macOS: Monterey
- BASE EFI: OpencCore 8.6
# ACPI
- SSDT-EC-USBX-LAPTOP.aml 修复USB电源
- SSDT-HPET.aml 修复IRQ冲突
- SSDT-PLUG-DRTNIA.aml 修复电源管理
- SSDT-PNLF.aml 修复背光
- SSDT-SBUS-MCHC.aml 修复SMBus
- SSDT-XOSI.aml 修复触摸板
- SSDT-GPRW.aml 修复睡眠即醒
# Drivers
- HfsPlus.efi
- OpenCanopy.efi
- OpenRuntime.efi
- ResetNvramEntry.efi
- ToggleSipEntry.efi
# Tools
- CFGLock.efi
- OpenShell.efi
- VerifyMsrE2.efi
# KextS
- Lilu
- VirtualSMC
  + SMCProcessor
  + SMCSuperIO
  + SMCBatteryManager
- WhateverGreen
- AppleALC
- RestrictEvents
- USBPorts (USBInjectAll)
- AirportBrcmFixup
- RealtekCardReader.kext
- RealtekCardReaderFriend.kext
- RealtekRTL8111.kext
- SATA-100-series-unsupported.kext
- BrightnessKeys.kext
- ApplePS2SmartTouchPad.kext
- CpuTscSync.kext （Not necessary）
- ECEnabler.kext （Not necessary）
- HibernationFixup.kext （Not necessary）

# Bluesnooze
- Bluesnooze prevents your sleeping Mac from connecting to Bluetooth accessories.If you pair Bluetooth headphones or speakers with both your phone & Mac it can be frustrating when your sleeping Mac connects intermittently and disrupts the audio.With Bluesnooze the Bluetooth connection is switched off when your Mac sleeps, and switched on when your Mac wakes.
- [Bluesnooze](https://github.com/odlp/bluesnooze/)

#### How can I hide the Bluesnooze icon?
- In your terminal run the following command:
```sh
defaults write com.oliverpeate.Bluesnooze hideIcon -bool true && killall Bluesnooze
```
When you next relaunch the application there should be no icon in the menu bar.
#### How can I restore the Bluesnooze icon?
- In your terminal run the following command:
```sh
defaults delete com.oliverpeate.Bluesnooze hideIcon && killall Bluesnooze
```
When you next relaunch the application it should appear in the menu bar.

# LENOVO B41-80 BIOS Unlocks CFG LOCK?
- 首先在关机状态下，依次按下“F1-1-Q-A-Z, F2-2-W-S-X, ... , F6-6-Y-H-N”一共6排30个按键；
- 接着按下开机电源键后，再按住开机电源键的同时按住F2键不松（有的是Fn+F2，建议先进BIOS停用功能键，后期再打开）；
- 待屏幕亮了，就能进入BIOS的高级隐藏模式了！
- Power
  + Power & Performance
  + CPU - Power Management Control
  + CPU Lock Configuration
  + CFG Lock -> Disabled
