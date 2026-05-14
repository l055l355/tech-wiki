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
Creation date: "2026-05-10T20:22:31Z"
Created by:
    - ethan
Links:
    - running-eve-ng-in-proxmox.md
    - files\image_1778725639077_0.png
    - files\image_1778725655174_0.png
    - files\image_1778725662370_0.png
---
# VM-EVE-ng   
## ALL VIRTUAL MACHINES AND CONTAINERS SHOULD BE **OFF** WHILE EVE-NG IS RUNNING.   
   
Type: Virtual Machine   
OS: Debian/Ubuntu   
Last Updated: N/A   
VM ID: 200   
IP: 192.168.X.X   
   
[Running EVE-NG in Proxmox](https://www.packetswitch.co.uk/running-eve-ng-in-proxmox/)    
   
**Bridged Nested-VM IPs (DHCP)**   
HQ-FW (Fortinet): 192.168.X.X    
GEELONG-FW (Fortinet): 192.168.X.X    
   
Set Fortinet Static IP -   
> conf sys int   

> edit port(x)   

> set ip <ip address>/<cidr>   

> set allowaccess ping http https ssh   

end   
   
show sys int port(x) - to see what the settings on the port is.   
   
Configure bridge VM networking (VMWare (should work with vmbrX on proxmox))   
Network Adapter X = PnetX -1
VPC needed gateway
VMNet IP address/range needs to be the SAME   
![image_1778725639077_0](files\image_1778725639077_0.png)    
![image_1778725655174_0](files\image_1778725655174_0.png)    
![image_1778725662370_0](files\image_1778725662370_0.png)    
