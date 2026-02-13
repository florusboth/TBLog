+++
date = '2026-02-13T15:10:08Z'
draft = true
title = 'Debian 13: Add Private IP Hetzner Cloud'
+++
# Debian 13: Add private IP Hetzner Cloud

> This could be relevant if you installed a cloud server with a ISO image.

I installed a new VM on Hetzner Cloud using the Proxmox Backup Server ISO. This is an easy way to get started on some applications but when you do this there is only public IPv4 on the server. I started this by creating a Ubuntu standard image server as I could not find a way to install directly from the custom ISO.

### To get your private cloud network on it, do the following.

In the cloud console, remove the private network if it is already attached. Then add it again. This way the OS will get the right NIC configured. In my case, on Debian 13, this was ```enp7s0```.

On the server, edit ```/etc/network/interfaces``` and add the following:

```
auto enp7s0
iface enp7s0 inet dhcp
        mtu 1450
```

Do a ```systemctl restart networking``` and check the result, with for example ```ip a```:

```
5: enp7s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1450 qdisc fq_codel state UP group default qlen 1000
    link/ether 86:00:00:7a:16:1e brd ff:ff:ff:ff:ff:ff
    altname enx8600007a161e
    inet 10.0.0.5/32 brd 10.0.0.5 scope global dynamic enp7s0
       valid_lft 83899sec preferred_lft 83899sec
    inet6 fe80::8400:ff:fe7a:161e/64 scope link proto kernel_ll
       valid_lft forever preferred_lft forever
```


