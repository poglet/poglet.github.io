---
layout: default
title: How to Play Fallout 2 Co-op on Bazzite Linux
description: How to install the Fallout 2 co-op mod with the GOG version of Fallout 2 via Heroic Launcher on Bazzite Linux, covering hosting a game, joining a session, and port forwarding for play over the internet.
last_modified_date: 2026-09-30
parent: Guides
grand_parent: Home
nav_enabled: true
---

# How to Play Fallout 2 Co-op on Bazzite Linux

[Fallout 2 Co-op](https://github.com/gusmarcum/fallout2-coop) is a mod built on Fallout 2 Community Edition that lets multiple players share one persistent world, each with their own character. One machine runs the dedicated server that owns the world, and every player joins it as a client.

These steps were tested on Bazzite Linux using the GOG version of Fallout 2 installed through the Heroic Launcher. I also tested port forwarding and connecting over the internet.

**What you need:**

* A GOG copy of Fallout 2
* [Heroic Launcher](https://heroicgameslauncher.com/) (preinstalled on Bazzite)
* The [Fallout 2 Co-op release zip](https://github.com/gusmarcum/fallout2-coop/releases/latest)

---

## Host the Game on Linux

1. Install the GOG version of Fallout 2 using Heroic Launcher. Briefly confirm the game launches before continuing.
2. Extract the co-op mod `.zip` file into the game folder. For example:

   ```
   /home/user/Games/Heroic/Fallout 2/
   ```

   Your path may differ depending on where Heroic installed the game. The extracted files (including `start.cmd`) should sit next to the game's data files, such as `master.dat`.

3. In Heroic, select the game, open the menu and choose **Edit Game/App**.
4. Change the game path to point at `start.cmd`.
5. Launch the game from Heroic to host the session.

---

## Join a Game on Linux

1. In Heroic, select **Add Game** and give it a title such as `Fallout 2 Join Server`.
2. Set the executable to the `join.cmd` file from the extracted mod.
3. Run the game and join the host's session.

{: .note }
We are needing to start Fallout 2 in two different Heroic game sessions, that is why we are creating the 2nd game entry pointing to the join.cmd file despite only having a single Fallout 2 installation folder.  If you are not the one hosting the game, you do not need to run the server.

---

## Playing Over the Internet

I tested port forwarding and connecting over the internet and it worked. Forward the game port (**9300**) to the host machine's LAN IP on your router, and make sure the host's firewall allows incoming connections on that port.

**Note:** The game port has no authentication, so only forward it on a trusted network or use a VPN such as ZeroTier between players if you'd rather not expose the port at all.

---

## Related Guides

* [How to Host a Dedicated Zandronum Server on Linux]({% link home/guides/how-to-host-dedicated-zandronum-server-on-linux.md %}) — another retro multiplayer setup, this time for Doom on Linux.

---

## Sources

* [Fallout 2 Co-op on GitHub](https://github.com/gusmarcum/fallout2-coop)
* [Latest release](https://github.com/gusmarcum/fallout2-coop/releases/latest)
