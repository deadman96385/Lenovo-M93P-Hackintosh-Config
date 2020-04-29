# Lenovo-M93P Tiny 10.15 Hackintosh

You will need to replace the wifi/bt chip with some that is compatible. Personally I have done it with the Broadcom BCM4352 Azurewave AW-CE123H.

## Hardware
* CPU - I5-4570T - 4th Gen
* Ram - 16gb - 2 slots
* GPU - Intel HD4600
* Drive - 1 500gb AHCI/Sata SSD
* Audio - Realtek ALC283
* Ethernet - Realtek RTL8168/8111/8112
* wifi/bt - Azurewave AW-CE123H (Broadcom BCM4352)

## Software
Used the [Vanilla guide](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/) and the [Internet Recovery install method](https://internet-install.gitbook.io/macos-internet-install/)

## Config.plist (Removed some entries to protect my PC)
This is based on [Mingcheng's M93P guide](https://github.com/mingcheng/lenovo-thinkcentre-m93p-hackintosh) with some minor changes like a generated SMBIOS and a new theme.

* Requires Serial Number (ex. DFOWQLSGH8K)
* Requires Board-ID (ex. Mac-D859C5498DA9EE9D)
* Requires MLB (ex. DFOWQLSGH8K)

## Kext Explanation
* AppleALC - Audio driver to power the Mic/Headphone jack
* Brcm kexts - Support for Broadcom wifi/bt chip
* IntelMausi - Supports the ethernet driver used
* Lilu - Allows patching of everything in the system
* SMC kexts - Expose sensors and cpu helpers to the system
* VirtualSMC - Emulates the SMC to the OS (Always required for Hackintosh's)
* WhateverGreen - Plugin for Lilu that fixes various GPU releated things in the system for AMD, Intel, Nvidia
