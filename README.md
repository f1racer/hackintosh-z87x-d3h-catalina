# hackintosh-2019-12-30-catalina

2020-09-19 Catalina 10.15.6

This is my most current Hackintosh with parts that I bought back in 2014.  Since then I have updated macOS many times.  Catalina being the most recent.  I used the vanilla method. I did initially have issues booting into the installer but once I got a correct config.plist and it was smooth sailing.  

Hardware:<br>
Gigabyte Z87X-D3H<br>
Intel Core i5 4670K (Haswell)<br>
32GB DDR3 RAM<br>
MSI AMD Radeon RX 570 GFX<br>
Sony 49XBRX700D 4K TV<br>
Fenvi T919 (WiFi/Bluetooth)<br>

Tools:<br>
 Clover EFI bootloader (https://github.com/CloverHackyColor/CloverBootloader/releases)<br>
 Clover configurator (https://mackie100projects.altervista.org/category/info-cc/)<br>

<br>

Install notes:<br>
- Download Catalina 10.15.6 from App store<br>
- Erase USB stick, name it INSTALLER, format with GUID Partition Map, Mac OS Extended (Journaled)<br>
- Run: sudo "/Applications/Install macOS Catalina.app/Contents/Resources/createinstallmedia" --volume /Volumes/INSTALLER<br>
- Clover EFI bootloader (Change install location to USB stick)<br>
  - Customize<br><br>

- UEFI Drivers<br>
ApfsDriverLoader<br>
AptioMemoryFix<br>
HPFSPlus<br>

- File System drivers<br>
Fat<br>
VBoxHFS<br>

- config.plist for Haswell (15,1) (https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-per-hardware/haswell)<br>

- Use Clover configurator (KEXT installer) to download/install to Clover/Other folder on EFI partition<br>
USBInjectAll.kext<br>
AppleALC.kext<br>
IntelMausi.kext<br>
Lilu.kext<br>
NoVPAJpeg.kext<br>
VirtualSMC.kext<br>
WhateverGreen.kext<br><br>

- Use USB stick to install OSX, F12 choose USB stick<br>
- reboot a couple times, pick USB stick, preloader<br>
- Clover EFI bootloader (install to SSD)<br>
- Copy EFI from USB to SSD (using clover configurator)<br>

Other notes:<br>
I didn't really need to tweak much.  This setup is for FCPX video editing, Adobe Lightroom/Photoshop and misc other things you do with a computer.  I installed Steam and play games every now and then like F1 2017, Grid Autosport, Hearthstone, Pokemon TCG.  
<br>
- WiFi/Bluetooth works (Fenvi T919)
- Audio through HDMI works
- 3840x2160 @ 60Hz via HDMI to my Sony TV
- not sure about sleep/hibernation since my Hackintosh is on 24/7, and I don't put it to sleep
- I don't use imessage/handoff/continuity so not sure if that works (have Android phone)
- Sidecar for sure doesn't work since it's not supported until Skylake and iMacs 17,1 and up
