---
title: Broadcom WiFi Driver Issues on Fedora Linux
date: 2022-05-22
description: How I Installed Broadcom WiFi Drivers on Fedora Linux
authors: ["Jonathan Buchholz"]
url: fedora-broadcom
---

Today, we received our first computer donation! While I was installing Fedora 36
on a 2014 Lenovo IdeaPad, I noticed that WiFi drivers did not come installed. I
have run into issues with Broadcom brand WiFi cards while installing Linux in
the past, where the operating system does not utilize the WiFi card in the
computer after the initial installation. Every time I need to install drivers to
make Broadcom WiFi cards work on Fedora, I have trouble finding up to date
information, which is why I writing down the steps here—both for future
is reference and in case someone else runs into the same issue.

Before I continue, here are the reasons why we are installing Fedora Linux on
donated machines:

- We anticipate donated computers to be older (this one was from 2014), so
  installing Linux will make make them feel snappier
- I am only familiar setting up development environments on Unix-like operating
  systems
- Using Linux will help students become familiar with the commands needed to run
  a server and could help them get started with sysadmin work
- Fedora seems to be the best Linux distribution for new users because it is
  stable without being so bleeding edge that packages break[^1]

[^1]: Initially, I was planning on using Linux Mint because the Cinnamon desktop
environment is very similar to Windows and it comes with a graphical driver
manager, but because I had issues installing the `BCM4352` WiFi driver with the
built-in driver manager (it said the driver was installed, but WiFi did not
work), I opted for Fedora Linux.

## Installing Broadcom WiFi Drivers on Fedora Linux

Note: I used the following steps to install the `BCM4352` WiFi driver on Fedora
36, but this should work for other Broadcom WiFi cards and versions of Fedora
Linux. Your mileage may vary.

1. Update packages: `$ sudo dnf update`
2. [Enable RPM Fusion repositories](https://docs.fedoraproject.org/en-US/quick-docs/setup_rpmfusion/)
	- Make sure to install both free and nonfree repositories
3. Install Broadcom WiFi drivers: `$ sudo dnf install broadcom-wl`
4. Restart the computer: `$ sudo reboot`
