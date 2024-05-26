# LENOVO-B41-80 Hackintosh
- Lenovo B41-80
- 6th Gen Intel(R) Core(TM) i5-6200U
- DDR3L 1600 16GB (8GB+8GB)
- BCM94360z4
- MacBookPro13,1
- macOS: Monterey
- BASE EFI: OpencCore 8.6
# ACPI
- SSDT-EC-USBX-LAPTOP.aml
- SSDT-HPET.aml
- SSDT-PLUG-DRTNIA.aml
- SSDT-PNLF.aml
- SSDT-SBUS-MCHC.aml
- SSDT-XOSI.aml
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
- ECEnabler.kext
- HibernationFixup.kext
- CpuTscSync.kext
- ApplePS2SmartTouchPad.kext
