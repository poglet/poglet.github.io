---
layout: default
title: How to Set Up SWAT 4 SEF-FR Multiplayer
description: How to install SWAT 4 SEF-FR Tactical Edition and play multiplayer, joining servers via direct IP and hosting a game with the required port forwarding.
parent: Guides
grand_parent: Home
nav_enabled: true
---

# How to Set Up SWAT 4 SEF-FR Multiplayer

[SWAT 4: SEF-FR Tactical Edition](https://www.moddb.com/mods/sef-fr-tactical-edition) is a popular mod that enhances the realism and tactical gameplay experience. It adds new weapons, equipment, maps, and AI behaviors, creating a more immersive and challenging experience for players.

---

## Installation

1. Install SWAT 4 by running `setup_swat4_gold_2.0.0.4.exe`.
2. Open `FRTE1.37P1_MODDB_Version.7z` using 7-Zip and extract the folder `SEF-FR Tactical Edition` to the `SWAT 4` installation directory.
   
   ![SWAT 4 installation directory showing the SEF-FR Tactical Edition folder extracted into the game folder](https://wiki.poglet.net/uploads/images/gallery/2024-11/scaled-1680-/image.png)

3. To run the game, open the `SEF-FR Tactical Edition` folder and run `LaunchSEF.bat`.
   
   ![LaunchSEF.bat file inside the SEF-FR Tactical Edition folder used to start the modded game](https://wiki.poglet.net/uploads/images/gallery/2024-11/scaled-1680-/dyNimage.png)

---

## Joining a Server

1. Run `LaunchSEF.bat`.
2. Select **Join Game** > **LAN Game** > **Direct IP**.
3. Enter the host's IP address and connect.
   
   ![SWAT 4 SEF-FR join game screen with LAN game and direct IP connection options](https://wiki.poglet.net/uploads/images/gallery/2024-11/scaled-1680-/pqSimage.png)

---

## Hosting a Server

1. Configure port forwarding for **10480** and **10487** on TCP/UDP.
2. Ensure your local firewall is configured to allow incoming connections from those ports.
3. Run `LaunchSEF.bat`.
4. Select **Host Game** > **LAN Game**.
5. Start the game.

---

## Related Guides

* [How to Host a Dedicated Zandronum Server on Linux]({% link home/guides/how-to-host-dedicated-zandronum-server-on-linux.md %}) — another retro FPS multiplayer setup, this time for Doom on Linux.

---

## Related guides

* [How to Host a Dedicated Zandronum Server on Linux]({% link home/guides/how-to-host-dedicated-zandronum-server-on-linux.md %}) — another retro gaming multiplayer setup, this time on Ubuntu.
