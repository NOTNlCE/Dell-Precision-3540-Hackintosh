# macOS Monterey - Dell Precision 3450

![Dell Precision 3450](https://i.dell.com/is/image/DellContent//content/dam/global-site-design/product_images/dell_client_products/workstations/mobile_workstations/precision/15_3540/pdp/laptop-precision-3540-pdp-gallery-504x350.jpg?fmt=jpg&wid=570&hei=400)

## OS

- macOS Monterey 12.2.1

## Hardware

- i7-8650U
- HD 620 / WX 2100
- 32GB DDR4 RAM
- 1080p Screen
- DW1560 Wireless
- 256GB SK Hynix NVMe SSD

## What Works

- CPU + IGPU Power Management
- Battery Status
- HDMI
- Sleep and Wake
- Audio ALC236
- Keyboard and Audio Fn Keys
- Trackpad with Gestures & Button Support
- Realtek microSD Card Reader
- Bluetooth
- WIFI (Changed Wifi card to BCM94360NG purchased here https://www.aliexpress.com/item/4000133686502.html?spm=a2g0o.cart.0.0.6d933c00jrbW24&mp=1)
- AMD Radeon Pro WX 2100 (WIP - Disable by swapping disable/Spoof SSDTs and commenting out device)

## What doesn't work

- Thunderbolt 3 (WIP)

## Notes

This is a fork of: https://github.com/matule95/Dell-Precision-3540-Hackintosh

With the release of the newly found spoof to enable the Lexa GPU core variant as a Polaris RX 550, we can now spoof our WX2100 device ID to utilize the Polaris drivers in macOS. It seems that software (Geekbench 5, most notably) is unable to utilize the GPU despite it being enabled. However, in this repo, it is enabled by default for testing purposes.

An update to VoodooI2C has enabled functionality of the trackbad buttons as well as I2C gesture support.

It is worth noting that the 512GB model of this machine ships with a Micron 512GB SSD that is NOT compatible with macOS and will cause panics at boot.

SSDT patching is needed to enable Thunderbolt 3, though the port works as a Type-C port.

## Usefull Guides

- OpenCore --> https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html
