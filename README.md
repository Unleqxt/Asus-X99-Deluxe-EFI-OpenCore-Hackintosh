# Asus-X99-Deluxe-EFI-OpenCore-Hackintosh

<img width="1080" height="675" alt="grafik" src="https://github.com/user-attachments/assets/c1ff1427-93e5-44fa-9379-03506a0abba1" />


## Specs:
- CPU: Xeon E5-2690 v4 14 core, 28 threads
- GPU: Asus dual rx580
- RAM: 2x 32gb 2133MHz DDR4 ecc (out of some old server, I had laying arround)
- Motherboard: Asus X99 Deluxe
- Audio Codec: Realteak ALC1150
- Ethernet Card: dual Intel gigabit nics, but I use a X540-T2 10Gbit card
- Wifi/BT Card: BCM4350/BCM20702A0
- BIOS revision: latest non beta bios


## OS:
- MacOS Sequoia (Tahoe should be possible)

## SMBIOS:
- iMacPro1,1 (I deleted the serials out of the efi, so you'll need to generate them with SMBIOSMaster)


## Functionallity:
### Working:
Airdrop, iservices, wlan, bluetooth, almost everything else
### Not Working:
Sleep (only works like 70% of the time, probably due to usb map), CPU is spoofed wrong (didn't want to deal with it -> registered as 14 Core Xeon-W, but doesn't have a performance impact)


## Struggels:
- If you do x99 hackintosh, you need to add npci=0x2000 in the boot-args, else your graphics are fucked up (took me way too long)
- Wireless connectivity (the wifi/bt card isn't supported anymore in macos sequoia so you'll need to patch them with opencore legacy patcher). I used this guide to patch it:[ Fenvi and Broadcom Wi-Fi](https://github.com/perez987/macOS-15-Sequoia-on-z390-with-OpenCore?tab=readme-ov-file#fenvi-and-broadcom-wi-fi)
- Freezes sometimes on boot -> just reset it and on the next boot it almost always works


#### Sorry because this ain't the best efi possible but I tried my best. If you have questions, feel free to message however I'm not sure wether I can answer them.
