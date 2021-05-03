# ASRock B460 Phantom Gaming 4
Opencore config for macOS
Compatible and tested with:
* macOS 10.15 Catalina
* macOS 11 Big Sur

## Notice
* Requires SystemUUID, SystemSerialNumber and ROM into PlatformInfo (use macserial utility from OpenCore / Utilities)
* For i7-10700K and below processor, iMac20,1 is used. For i9-10850K and above iMac20.2
* The default BIOS settings are perfectly fine to work with

## Specs:
* MB - ASRock B460 Phantom Gaming 4 на Intel B460 (BIOS ver 1.70)
* Video - Intel UHD 630 (works as primary or IQSV if Discrete graphics is used)
* Network: Intel I219V
* Audio: Realtek ALC1200 (layout-id=2)

## Kexts:
* AppleALC
* IntelMausi.kext
* Lilu.kext
* NVMeFix.kext
* VirtualSMC.kext + SMCProcessor.kext + SMCSuperIO.kext
* WhateverGreen.kext
* USBMap.kext (inject all ports)
* XHCI-unsupported.kext (inject 0xa3af8086 USB controller)

## Included SSDT for:
* SSDT-AWAC - Forces enables legacy RTC clock
* SSDT-EC-USBX-DESKTOP - Fix EC
* SSDT-PLUG - XCPM power management compatibility table

## Credits
* Acidanthera team for developing Opencore and most Kexts (github.com/acidanthera)
* Dortania team for prebuilt SSDTs
* Apple for developing MacOS