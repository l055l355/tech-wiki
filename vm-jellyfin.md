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
Links:
    - files\bafyreih6g6pz7vctbgmqluz7fa6j3i5l6kpaabmcyc5rm
    - files\bafyreiai5hokyl4acifinwsdnhigshshxqk5lgnzztdnn
    - files\bafyreidgdn33kavdgjkpjmewxgybh2pbxs5xluseyp57u
    - files\bafyreifc3e6r5i4mrnfthblgtnhipmrnr5xrnk2y6ldc4
    - files\bafyreihv2cmmtep3z46asbtahh4yprpj5zwfz2sk2ydfd
    - files\bafyreiapyo42c4bbz6ne2rtf3m3dvpuraqekx22myj4rf
    - files\bafyreievlckv3tgvanxsedladdz4xsvvvns5nc5h4rww6
    - files\bafyreiavw32yaqezlh36b6gcbpyav5tsiv2ezm7twndyt
    - files\untitled_y
    - files\untitled
    - files\untitled_5
    - files\bafyreid2ocqdmpqey7rf2sydiwk2ulgl6kb3z5synv77v
    - files\untitled_p
    - files\bafyreigkmwqynsusutghu3kgelr7bncdpmwwsmjvy3yc3
    - files\bafyreifzjoovm7s4anqpldmt5ytqryrk7hhat2u2x2bbl
    - files\bafyreigqgx2idkfgguco53ckkl7qcn5m4upm6mchblfrd
    - files\untitled_4
    - bafyreifu4x73zqdzpjun6pbzdddm3dp25jis7qujbzl4b26edrntwlwuq4
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
   
**Configuring GPU Passthrough & GPU encoding to Debian Guest VM from Proxmox Host:**   
GPU passthrough to jellyfin vm for better transcoding.   
![bafyreih6g6pz7vctbgmqluz7fa6j3i5l6kpaabmcyc5rmpb5g5igiu6f5a](files\bafyreih6g6pz7vctbgmqluz7fa6j3i5l6kpaabmcyc5rm)    
Updated grub to allow gpu passthrough.   
![bafyreiai5hokyl4acifinwsdnhigshshxqk5lgnzztdnno5ydy2fuyxeyq](files\bafyreiai5hokyl4acifinwsdnhigshshxqk5lgnzztdnn)    
![bafyreidgdn33kavdgjkpjmewxgybh2pbxs5xluseyp57uc6qd4pkgcthku](files\bafyreidgdn33kavdgjkpjmewxgybh2pbxs5xluseyp57u)    
Iommu detected and ready for passthrough   
![bafyreifc3e6r5i4mrnfthblgtnhipmrnr5xrnk2y6ldc4p6sdxribn76tm](files\bafyreifc3e6r5i4mrnfthblgtnhipmrnr5xrnk2y6ldc4)    
Gpu id   
![bafyreihv2cmmtep3z46asbtahh4yprpj5zwfz2sk2ydfdsiuebfoxi37la](files\bafyreihv2cmmtep3z46asbtahh4yprpj5zwfz2sk2ydfd)    
Add iommu modules to boot on start   
![bafyreiapyo42c4bbz6ne2rtf3m3dvpuraqekx22myj4rfya6fi7udhcmme](files\bafyreiapyo42c4bbz6ne2rtf3m3dvpuraqekx22myj4rf)    
Safe ignores   
![bafyreievlckv3tgvanxsedladdz4xsvvvns5nc5h4rww6xbhdpyv773bfu](files\bafyreievlckv3tgvanxsedladdz4xsvvvns5nc5h4rww6)    
Stops proxmox from obtaining ownership of gpu so that it can get passed through.   
![bafyreiavw32yaqezlh36b6gcbpyav5tsiv2ezm7twndyth5pktydefxluq](files\bafyreiavw32yaqezlh36b6gcbpyav5tsiv2ezm7twndyt)    
Inputting the correct device ids for passthrough.   
![bafyreiaopu4ind2zkj2dyc2snltekm2pltkt75nu3c3bp3u5xr6iot3z7e](files\untitled_y)    
Update after changes.   
Then reboot.   
![bafyreidew5yc3fbnbfk4mbnk3pecwllolj54xxu3lwmnv3wcrhphdfxngu](files\untitled)    
Create the vm   
I then configured my IP to what I wanted it to be.   
![bafyreihiksdnia2vwyanbhpz66u3s3p6thkecnrdz5v5kh7tcupghidqqq](files\untitled_5)    
I then added my gpu.   
![bafyreid2ocqdmpqey7rf2sydiwk2ulgl6kb3z5synv77vfbfw47gmjl7ze](files\bafyreid2ocqdmpqey7rf2sydiwk2ulgl6kb3z5synv77v)    
Confirmed that my gpu was detected.   
I then followed the debian guide on how to install nvidia drivers.   
![bafyreie3ho5rb7ye35ktatisxps3e2fft5l7bdn5n5bicreas66rab6a2u](files\untitled_p)    
Installing the proprietary nvidia drivers.   
![bafyreigkmwqynsusutghu3kgelr7bncdpmwwsmjvy3yc3ais4oa7kqvgca](files\bafyreigkmwqynsusutghu3kgelr7bncdpmwwsmjvy3yc3)    
Confirmed that it was installed.   
![bafyreifzjoovm7s4anqpldmt5ytqryrk7hhat2u2x2bblaine4uo3txy2y](files\bafyreifzjoovm7s4anqpldmt5ytqryrk7hhat2u2x2bbl)    
Was using ram but after i swapped to ssd it worked   
![bafyreigqgx2idkfgguco53ckkl7qcn5m4upm6mchblfrd45focxiuev66a](files\bafyreigqgx2idkfgguco53ckkl7qcn5m4upm6mchblfrd)    
![bafyreiavcme55p3meae2ynvnfw4keac4br6xvtiwu7ogrshe4og3myne7q](files\untitled_4)    
Jellyfin successfully installed.   
![bafyreifu4x73zqdzpjun6pbzdddm3dp25jis7qujbzl4b26edrntwlwuq4](files\bafyreifu4x73zqdzpjun6pbzdddm3dp25jis7qujbzl4b)    
Installing cuda for hardware transcoding.   
