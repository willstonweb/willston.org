---
title: Broadcom WiFi Driver Issues on Fedora Linux
date: 2022-05-22
description: How I installed Broadcom WiFi drivers on Fedora Linux
author: Jonathan Buchholz
url: fedora-broadcom
---

Broadcom brand WiFi drivers are notorious for not working by default on Linux.
Every time I need to install drivers to make Broadcom WiFi cards work on Fedora
Linux, I have trouble finding up to date information, which is why I writing
down the steps here—both for future is reference and in case someone else runs
into the same issue.

## Installing Broadcom WiFi Drivers on Fedora Linux

Note: I used the following steps to install the `BCM4352` WiFi driver on Fedora
36, but this should work for other Broadcom WiFi cards and versions of Fedora
Linux. Your mileage may vary.

1. Update packages: `$ sudo dnf update`
2. [Enable RPM Fusion repositories](https://docs.fedoraproject.org/en-US/quick-docs/setup_rpmfusion/)
	- Make sure to install both free and nonfree repositories
3. Install Broadcom WiFi drivers: `$ sudo dnf install broadcom-wl`
4. Restart the computer: `$ sudo reboot`
