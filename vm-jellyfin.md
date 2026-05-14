---
# yaml-language-server: $schema=schemas\page.schema.json
Object type:
    - Page
Tag:
    - Homelab
    - VM
    - Proxmox
Backlinks:
    - n1-node.md
    - Homelab
Creation date: "2026-05-11T03:43:12Z"
Created by:
    - ethan
---
# VM-Jellyfin   
   
LAN IP: 192.168.X.X   
Type: Virtual Machine   
OS: Debian Server   
Starts on boot   
Last Update: 11/05/26   
VM ID: 150   
Proxmox VE 9.1.9   

   
**Web UI:** [http://JELLYFIN](http://JELLYFIN/)   
   
Media drive is connected via samba (lxc) - 101 pride-rock
IP: 192.168.X.X
Read-only samba account (Sambar) (so that if the jellyfin vm is compromised it can't write data to a shared drive).    
