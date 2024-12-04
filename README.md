# Sequoia Branch
OpenCore for ASUS ROG STRIX Z390-I GAMING

## General
System version:

OS|Version|Number|SMBIOS
|-|-|-|-|
|Sequoia|15.1.1|(24B91)|iMac19,1

_<sub>SHOULD ALSO WORK ON SONOMA (UNTESTED)</sub>_

Hardware tested:
Part|Model|Remarks
|-|-|-|
Motherboard|Asus Z390-I Gaming
CPU|i7-9700k
RAM|Corsair Vengeance Pro SL 2x16Gb 3600MHz
SSD|Corsair MP600 CORE XT 2x1Tb
iGPU|HD Graphics UHD630
dGPU|Asus Dual RX 6600 XT|`agdpmod=pikera` multiple monitor setup works
WiFi/BT|Fenvi BCM94360NG|patching required (see instructions below)

Not working / untested:
* OTA/Delta Updates (see the note below)
* Compatibility with Sonoma (untested, but should work)

## Patching Instructions
1. Download and install OpenCore Legacy Patcher - https://github.com/dortania/OpenCore-Legacy-Patcher/tree/main
2. Press `Post-Install Root Patch`
3. Reboot
4. Enjoy

Alternatively, you can use this method (pre-installation) - https://github.com/HorizonUnix/PatchSonomaWiFiOnTheFly

_<sub>NOTE: WITH BROADCOM-BASED WIFI/BT YOU WILL LOSE SIP AND SECURE BOOT IN ORDER TO GET IT WORK DUE TO NECESSITY OF PATCHES AND THERE IS <ins>CURRENTLY</ins> NO OTHER WAY TO DO IT (THEREFORE YOU WILL LOSE THE OTA/DELTA UPDATES). EITHER ACCEPT IT OR USE AN INTEL-BASED MODULE + KEXTS WITH ALL THE DOWNSIDES SUCH AS BROKEN CONTINUITY OR STAY ON VENTURA UNTIL IT GETS FIXED (IF EVER). TRADE-OFFS!</sub>_

## Important
_<sub>PLEASE GENERATE YOUR OWN `MLB`, `ROM`, `SystemSerialNumber` and `SystemUUID` OR <ins>YOUR HACK WILL NOT BOOT</ins></sub>_\
_<sub>USB MAP IS PROVIDED IN KEXTS, BUT PLEASE MAKE YOUR OWN (YOU WILL NEED TO CHOOSE WHAT PORTS TO DISABLE AS NOT ALL OF THEM CAN FIT INTO 15 PORT LIMIT)</sub>_
