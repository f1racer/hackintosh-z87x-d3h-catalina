# hackintosh-catalina-2019
2019-12-30 Catalina 10.15.2

This is my most current Hackintosh with parts that I bought back in 2014.  Since then I have updated macOS many times.  Catalina being the most recent.  I used the vanilla method. 

Hardware:
Gigabyte Z87X-D3H
Intel Core i5 4670K (Haswell)
32GB DDR3 RAM
MSI AMD Radeon RX 570 GFX
Sony 49XBRX700D 4K TV
Fenvi T919 (WiFi/Bluetooth)

Tools:
Clover EFI bootloader
Clover configurator

Notes:

- Download Catalina from App store
- Erase USB stick, name it INSTALLER, format with GUID scheme
- Run: sudo "/Applications/Install macOS Catalina.app/Contents/Resources/createinstallmedia" --volume /Volumes/INSTALLER

- Clover EFI bootloader (install to USB stick)
- Clover configurator (KEXT installer)

USBInjectAll.kext
AppleALC.kext
IntelMausi.kext
Lilu.kext
NoVPAJpeg.kext
VirtualSMC.kext
WhateverGreen.kext


- config.plist for Haswell (https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-per-hardware/haswell)
- Use USB stick to install OSX, F12 choose USB stick
- reboot a couple times, pick USB stick, preloader
- Clover EFI bootloader (install to SSD)
- Copy EFI from USB to SSD (using clover configurator)

