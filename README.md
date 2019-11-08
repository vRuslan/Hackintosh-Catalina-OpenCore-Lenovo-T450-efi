# Thinkpad T450s Catalina

## Notice: If you need to edit config.plist, don't use OpenCore configurator, use PlistEdit pro or Xcode instead.

## Introduction

EFI for Thinkpad T450 (20BXCT01WW) Hackintosh Catalina.

CPU: i5-5200U

Integrated Graphics: HD Graphics 5500

Sound Card: ALC292

Wireless Card: **BCM94360CD 4 antennas.**

## Bios

- `Security -> Security Chip`: **Disabled**;
- `Memory Protection -> Execution Prevention`: **Enabled**;
- `Virtualization -> Intel Virtualization Technology`: **Enabled**;
- `Internal Device Access -> Bottom Cover Tamper Detection`: must be **Disabled**;
- `Anti-Theft -> Current Setting`: **Disabled**;
- `Anti-Theft -> Computrace -> Current Setting`: **Disabled**;
- `Secure Boot -> Secure Boot`: **Disabled**;
- `UEFI/Legacy Boot`: **UEFI Only**;
- `CSM Support`: **Yes**.

## What works

- Sleep / Wake
- Wifi and Bluetooth (BCM94360CD)
- Handoff, Continuity, AirDrop
- iMessage, FaceTime, App Store, iTunes Store (Change Config.plist -> PlatformInfo -> Generic -> MLB and SystemSerialNumber)
- Ethernet
- Onboard audio (Use alc_fix to fix unworking jack after replug )
- TRIM
- USB 2.0 / USB 3.0
- Battery
- Touchpad
- Redpoint
- miniDP
- SD Card Reader (Thanks to @willmav5000)
- Use [one-key-hidpi](https://github.com/daliansky/XiaoMi-Pro-Hackintosh/blob/master/one-key-hidpi) to enable HiDPI
- If you are using a usb mouse with side buttons, you can spoof apple usb mouse by change the pid and vid in AnyAppleUSBMouse.kext/Info.plist and enable it in config.plist.

## What doesn't work

- Sidecar (Broadwell doesn't support sidecar)
- VGA
