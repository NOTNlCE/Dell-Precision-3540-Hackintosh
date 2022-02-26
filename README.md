# macOs Monterey - Dell Precision 3450

![Dell Precision 3450](https://i.dell.com/is/image/DellContent//content/dam/global-site-design/product_images/dell_client_products/workstations/mobile_workstations/precision/15_3540/pdp/laptop-precision-3540-pdp-gallery-504x350.jpg?fmt=jpg&wid=570&hei=400)

## OS

- macOS Monterey 12.2.1

## What Works

- CPU + IGPU Power Management
- Battery Status
- HDMI
- Sleep and Wake
- Audio ALC236
- Keyboard with Brightness and Audio fn keys
- Trackpad with Gestures
- Bluetooth
- WIFI (Changed Wifi card to BCM94360NG purchased here https://www.aliexpress.com/item/4000133686502.html?spm=a2g0o.cart.0.0.6d933c00jrbW24&mp=1)

## What doesn't work

- Trackpad buttons
- AMD Radeon Pro WX 2100 (WIP - Enable by swapping disable/Spoof SSDTs and uncommenting out device)
- Thunderbolt 3 (WIP)

## Notes

This is a fork of: https://github.com/matule95/Dell-Precision-3540-Hackintosh

With the release of the newly found spoof to enable the Lexa GPU core variant as a Polaris RX 550, we can now spoof our WX2100 device ID to utilize the Polaris drivers in macOS. At present, this breaks brightness control on the internal screen. Additionally, it seems that software (Geekbench 5, most notably) is unable to utilize the GPU despite it being enabled. Therefore, in this repo, it is disabled by default pending more testing.

An update to VoodooI2C is pending to enable functionality of the trackbad buttons, but at the time of writing is not yet pushed.

SSDT patching is needed to enable Thunderbolt 3, though the port works as a Type-C port.

## Usefull Guides

- OpenCore --> https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html
