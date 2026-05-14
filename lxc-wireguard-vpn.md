---
# yaml-language-server: $schema=schemas\page.schema.json
Object type:
    - Page
Tag:
    - Homelab
    - Container
    - Proxmox
Backlinks:
    - n1-node.md
    - Homelab
Creation date: "2026-05-10T05:38:03Z"
Created by:
    - ethan

---
# LXC-Wireguard-VPN   
LAN IP: 192.168.X.X   
Type: Container (LXC)   
OS Type: Debian   
Starts on boot   
Last Update: 10/05/26   
Container ID: 100   
   
WGDashboard: [http://WGDASHBOARD/](http://wgdashboard)       
   

$$
https://www.youtube.com/watch?v=Qkw5fyHayvg
$$
   
[Quick Start - WireGuard](https://www.wireguard.com/quickstart/#command-line-interface)    
   
Config Location:   
Laptop: path\to\config.conf    
   
**To manage a tunnel without a GUI (administrator)**   
Open Terminal (Powershell) as Administrator.   
   
paste this command:    
```
wireguard /installtunnelservice "C:\path\to\your\config.conf"
```
   
To unninstall tunnel run this command:   
```
wireguard /uninstalltunnelservice <TunnelName>
```
   
**To start on Windows (from unprivileged account) from GUI**   
Start Windows Services (as admin) > start WireGuardTunnel:<tunnelname>   
   
