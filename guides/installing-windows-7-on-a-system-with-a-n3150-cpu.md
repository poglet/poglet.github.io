---
layout: default
title: Installing Windows 7 on an N3150 CPU System
parent: guides
---

# Installing Windows 7 on a System with an N3150 CPU

1. **Add USB 3.0 Drivers to Installation Media** Follow the [NUCBlog Guide](https://nucblog.net/2015/07/installing-windows-7-on-the-nuc5cpyh-or-nuc5ppyh/) to inject USB 3.0 drivers into your Windows 7 installation media. The required driver package is `USB_3.0_Win7_64_4.0.0.36.zip`.

2. **Install Windows Update Patch (Unverified)** Download and install `Windows6.1-KB3102810-x64`.

3. **Install SHA-2 Code Signing Support (Unverified)** Download and install `windows6.1-kb4474419-v3-x64` to help with driver signing.

4. **Force Unsigned Drivers** Bypass driver signing restrictions using the methods outlined in this [Reddit Thread](https://www.reddit.com/r/windows7/comments/19bgy8m/force_unsigned_drivers_into_the_windows_7_setup/). Specifically, you can complete this by choosing one of the following:
   * Run the command: `bcdedit /set nointegritychecks On`
   * Open `gpedit.msc` and navigate to: **User Configuration** > **Administrative Templates** > **Driver Installation** > **Code Signing for Device Drivers**. Set it to **Enabled**, then select **Ignore**.

5. **Reboot the System** Perform a system reboot to apply changes.

6. **Install Graphics Drivers** Download the `win64_15.40.5171.zip` graphics drivers. Install them manually via **Device Manager** or try running the `.exe` installer.

7. **Run Windows Update** Perform standard Windows Updates to complete the setup.
