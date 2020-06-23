# GA-Z97-HD3-OpenCore

This is my opencore EFI config according to [OpenCore-Desktop-Guide](https://dortania.github.io/OpenCore-Desktop-Guide/). *Unfinished*

OpenCore Version: 0.5.9

macOS Version : 10.15.5

## Hardware

* Motherboard: GA-Z97-HD3
* CPU: i7-4790k
* RAM: Kingston DDR3 8 GB 1600 MHz * 2
* Drive: EAGET S600 SSD 1T
* Graphics Card: YESTON RX 5600 XT OC

## Note

* This motherboard supports native nvram.
* `CFG-LOCK` option is not available in BIOS, thus kernel quirks: `AppleCpuPmCfgLock` and `AppleXcpmCfgLock` were enabled.
* `Above 4G decoding` is not available as well, fixed by adding boot args: `npci=0x2000`.
* I left `VT-d` enabled so the kernel quirk `DisableIoMapper` was set to `True`.
* You may have to do USB mapping by yourself if you want to use my config (delete my kext `USBMap.kext` before doing that).
* My serial is **Invalid** :sob:.