---
layout: default
title: How to host dedicated Zandronum server on Linux
parent: Guides
---

# How to host dedicated Zandronum server on Linux

This is a guide I've created to help server owners host Zandronum in Linux. In my case I'm using Ubuntu 20.04. This is hosted in Oracle Cloud using the free-tier server they provide.

### Update Ubuntu

```
sudo apt update -y
sudo apt upgrade -y
sudo apt-get install -y net-tools
sudo apt-get install -y software-properties-common
```

### Install Zandronum

```
sudo apt-add-repository 'deb http://debian.drdteam.org/ stable multiverse'
wget -O - http://debian.drdteam.org/drdteam.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get install -y zandronum
```

**Note:** At this point you can attempt starting a server with the `zandronum-server` command . If you can an error about libcrypto.so.1.0 you can try the following commands. This will need to be done on each reboot.

```
LD_LIBRARY_PATH=/usr/games/zandronum export LD_LIBRARY_PATH zandronum-server
```

This should launch the server, however without .wad files and a working configuration you will get an error.

### Configure .wad Files

Copy the .wad file to ~/.config/zandronum/  
Copy or create a config.cfg file in the same location. You can find an example config.cfg file that I use here:

```
https://text.is/NPOJ
```

### Starting the Server

```
LD_LIBRARY_PATH=/usr/games/zandronum export LD_LIBRARY_PATH zandronum-server -host -port 10666 -iwad doom2.wad -file Eviternity.wad -exec ~/.config/zandronum/config.cfg
```

This is the command I use to launch my server, **yours might be different**. Now if you want to run the server as a background process you will need to use the nohup command, for example:

```
nohup nice -2 zandronum-server -host -port 10666 -iwad doom2.wad -file Eviternity.wad -exec ~/.config/zandronum/config.cfg &
```

### Stopping the Server

```
kill -9 `pgrep zandronum`
```

### Firewall Setup (for Oracle cloud users)

You will also need to create an Ingress rule through the Oracle web console.

```
sudo iptables -I INPUT 6 -m state --state NEW -p udp --dport 10666 -j ACCEPT sudo netfilter-persistent save
```

### Finished

The above steps should be enough to host a server and have it appear in Doomseeker. Let me know how you go.

### Sources

```
https://wiki.zandronum.com/Install_Zandronum_on_Ubuntu https://zandronum.com/forum/viewtopic.php?t=10236 https://docs.oracle.com/en-us/iaas/developer-tutorials/tutorials/apache-on-ubuntu/01oci-ubuntu-apache-summary.htm
```
