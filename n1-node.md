---
# yaml-language-server: $schema=schemas\page.schema.json
Object type:
    - Page
Tag:
    - Proxmox
    - Homelab
    - Baremetal
Backlinks:
    - Proxmox
Creation date: "2026-05-10T19:57:52Z"
Created by:
    - ethan
Links:
    - lxc-wireguard-vpn.md
    - lxc-pride-rock-samba.md
    - vm-jellyfin.md
    - vm-eve-ng.md
    - files\untitled_i
---
# N1-Node   
**HW/**
CPU: AMD Ryzen 5 7535HS 6c/12t, 6 x 4.6 GHz AMD Zen 3+, Rembrandt R
GPU: NVIDIA GeForce RTX 2050 Mobile - 4 GB VRAM, GDDR6
Memory: 16 GB DDR5 (upgradable)
Storage: 1x 512gb M.2 PCIe (upgradeable)
Connections: 4 USB 3.0 / 3.1 Gen1, 1 HDMI, Audio Connections: 3.5mm
Networking: 802.11 a/b/g/n/ac/ax (a/b/g/n = Wi-Fi 4/ac = Wi-Fi 5/ax = Wi-Fi 6/), Bluetooth 5, 1Gb RJA45
Display: 15.60 inch 16:9, 1920 x 1080 pixel 141 PPI, IPS, 180 Hz   
   
**IP Address:** 192.168.X.X (static)
**Version: **VE 9.1.9** **
   
Last Updated: 10/05/26   
   
**(static) IP Range: **.200-.254   
   
|                              **Name**   <br> |   **Service**   <br> |                        **IP**   <br> |          **Type / ID**   <br> |                                                                                           **Notes**   <br> |
|:---------------------------------------------|:---------------------|:-------------------------------------|:------------------------------|:-----------------------------------------------------------------------------------------------------------|
|            [wg](lxc-wireguard-vpn.md)   <br> | Wireguard VPN   <br> |                 192.168.X.X   <br> | Container (LXC)<br>100   <br> |                 **Starts on boot.** [http://WGDASHBOARD](HTTP://WGDASHBOARD)    <br> |
| [pride-rock](lxc-pride-rock-samba.md)   <br> |         Samba   <br> |                 192.168.X.X   <br> | Container (LXC)<br>101   <br> | **Starts on boot.**  <br> |
|            [jellyfin](vm-jellyfin.md)   <br> |      Jellyfin   <br> |                 192.168.X.X   <br> | Virtual Machine<br>150   <br> |                         **Starts on boot.** [http://JELLYFIN](http://JELLYFIN)    <br> |
|              [EVEng-CE](vm-eve-ng.md)   <br> |   EVE-ng (CE)   <br> | 192.168.X.X   <br> | Virtual Machine<br>200   <br> |                                                          For school.<br>Also has 192.168.X.X-X.   <br> |

| **ID Range**   <br> |             **Use**   <br> |
|:--------------------|:---------------------------|
|          100   <br> |       Home Services   <br> |
|          200   <br> | Testing/Experiments   <br> |
|          300   <br> |      Backups/Copies   <br> |
|          400   <br> |        Game Servers   <br> |

**IDs 0-10 (i.e. 100-110) should be reserved for management/core services (i.e. VPN with ID 100 or Samba with 101 since both are core features for other VMs)**   
   
Edited (& backed up) systemd file logind-conf to ignore the lid closing.   
(files\untitled_i)    
