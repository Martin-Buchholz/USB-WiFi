2022-08-21

## USB WiFi chipset information for Linux

This document is a summary that includes information about many modern USB WiFi chipsets.

Not all USB WiFi adapters are created equally.  While the chipset and driver
dictate which WiFi features are supported (e.g. which frequency bands), the
vendor of the adapter is free to decide on the performance of the antenna(s),
the power of the amp and whether the device requires mode switching and so on.

Chipset           | Interface       | Standard   | MIMO | 2.4 | 5   | 6   | Linux<br>In-Kernel<br>Driver | AP Mode          | Monitor Mode     |
------------------|-----------------|------------|:----:|:---:|:---:|:---:|:----------------------------:|:----------------:|:----------------:|
Mediatek MT7921au | USB3 / 5 Gbps   | WiFi 6E    | 2x2  |  40 |  80 |  80 |:heavy_check_mark: [1]        |:heavy_check_mark: [2]|:heavy_check_mark:|
Realtek RTL8852au | USB3 / 5 Gbps   | WiFi 6     | 2x2  |  40 |  80 |  N  |:x: - avoid                   | bad driver       | bad driver       |
Realtek RTL8832au | USB3 / 5 Gbps   | WiFi 6     | 2x2  |  40 |  80 |  N  |:x: - avoid                   | bad driver       | bad driver       |
Realtek RTL8814au | USB3 / 5 Gbps   | WiFi 5     | 3x3  |  40 |  80 |  N  |:x: - avoid                   | old driver       | old driver       |
Mediatek MT7612u  | USB3 / 5 Gbps   | WiFi 5     | 2x2  |  40 |  80 |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8822bu | USB3 / 5 Gbps   | WiFi 5     | 2x2  |  40 |  80 |  N  |:x: [3]                       |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8812bu | USB3 / 5 Gbps   | WiFi 5     | 2x2  |  40 |  80 |  N  |:x: [3]                       |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8812au | USB3 / 5 Gbps   | WiFi 5     | 2x2  |  40 |  80 |  N  |:x:                           |:heavy_check_mark:|:heavy_check_mark:|
Mediatek MT7610u  | USB2 / 480 Mbps | WiFi 5     | 1x1  |  20 |  80 |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8821cu | USB2 / 480 Mbps | WiFi 5     | 1x1  |  40 |  80 |  N  |:x: [3]                       |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8811cu | USB2 / 480 Mbps | WiFi 5     | 1x1  |  40 |  80 |  N  |:x: [3]                       |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8821au | USB2 / 480 Mbps | WiFi 5     | 1x1  |  40 |  80 |  N  |:x:                           |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8811au | USB2 / 480 Mbps | WiFi 5     | 1x1  |  40 |  80 |  N  |:x:                           |:heavy_check_mark:|:heavy_check_mark:|
Ralink RT5572     | USB2 / 480 Mbps | WiFi 4     | 2x2  |  40 |  40 |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Ralink RT3572     | USB2 / 480 Mbps | WiFi 4     | 2x2  |  40 |  40 |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Ralink RT5372     | USB2 / 480 Mbps | WiFi 4     | 2x2  |  40 |  N  |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Realtek RTL8192cu | USB2 / 480 Mbps | WiFi 4     | 2x2  |  40 |  N  |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Mediatek MT7601u  | USB2 / 480 Mbps | WiFi 4     | 1x1  |  40 |  N  |  N  |:heavy_check_mark:            |:x:               | limited          |
Ralink RT5370     | USB2 / 480 Mbps | WiFi 4     | 1x1  |  40 |  N  |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Atheros AR9271    | USB2 / 480 Mbps | WiFi 4     | 1x1  |  40 |  N  |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|
Ralink RT3070     | USB2 / 480 Mbps | WiFi 4     | 1x1  |  40 |  N  |  N  |:heavy_check_mark:            |:heavy_check_mark:|:heavy_check_mark:|

## Mediatek MT7921U (in-kernel driver for mt7921au) (WiFi 6E)

Adapters are now becoming available for purchase.

[1] USB support added to the mt7921 driver in kernel 5.18.

[2] AP mode support added to the mt7921 driver in kernel 5.19. Firmware update is required also.

## Realtek RTW88 (in-kernel driver) (WiFi 5)

[3] Work to upstream USB support for the in-kernel RTW88 driver recently started. If successful, that means
that we will see Linux Wireless Standards compliant in-kernel support for the following chipsets:

```
rtl8822bu
rtl8812bu
rtl8821cu
rtl8811cu
```

Note: No timeline is available currently.

-----

[Return to Main Menu](https://github.com/morrownr/USB-WiFi)

-----


