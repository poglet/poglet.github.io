---
layout: default
title: Various Methods for Running Windows 98
parent: Guides
---

# Various Methods for Running Windows 98

## Introduction

Windows 98 is a notoriously difficult system to run reliably through modern emulation or virtualization. Below is a list of methods and configurations currently available to get it running.

### DosBox-X

Windows 98 can be installed inside DosBox-X by following the official [DosBox-X Installation Guide](https://dosbox-x.com/wiki/Guide%3AInstalling-Windows-98). Running Windows 98 within DosBox-X provides the unique advantage of supporting save states, a feature often missing from other virtualization solutions.

### 86Box

86Box focuses on emulating precise machine hardware execution. By configuring the correct hardware components and mounting your Windows 98 installation media, you can install the operating system directly. A comprehensive deployment walkthrough can be found on this [GitHub Gist Guide](https://gist.github.com/milnak/42652752c040f6a92638519ebd48c0c7#file-install-windows-98-in-86box-md).

For quick deployment, a list of pre-made system environments is available on the [Internet Archive](https://archive.org/details/recommended-vm-configurations-of-windows-for-86box.). These systems are built following the technical baseline documented in the [BetaWiki Recommended VM Configurations for Windows](https://betawiki.net/wiki/Draft:Recommended_VM_configurations/Windows.).

### VMware Workstation 17.x

Windows 98 can also be virtualized using VMware Workstation. A step-by-step setup guide for configuring a Windows 98SE guest environment is hosted on [GitHub](https://github.com/PhilipYip1988/vmware-workstation-installation-guide/blob/main/windows-98SE-guest/readme.md).

---

## Downloads

* **Windows 98 SE Operating System:** Can be acquired via [WinWorld Full OEM Edition](https://winworldpc.com/product/windows-98/98-second-edition). Note that only the OEM Full version contains a bootable image.
* **Applications and Archive Files:** A repository of retro software tools is available through the [Internet Archive Windows 98 Software Collection](https://archive.org/details/wincollection5).
* **Modern Software Backports:** A curated index of the latest compatible software versions still functioning on Windows 98 can be tracked via [Retro Systems Revival](https://retrosystemsrevival.blogspot.com/p/latest-versions-of-software-working-on_20.html).
