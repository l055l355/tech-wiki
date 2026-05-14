---
# yaml-language-server: $schema=schemas\note.schema.json
Object type:
    - Note
Backlinks:
    - TechWiki
Creation date: "2026-05-14T03:08:24Z"
Created by:
    - ethan
id: bafyreiac4orfnxnazidleedjqxu2mm26gcqxrsip46w3vfk2qkipz4lwiu
---
Linux Commands   
> UFW   

To allow multiple ports using UFW, you can specify them in a single command by separating the ports with commas, like this: `sudo ufw allow 80,443/tcp`. Alternatively, you can allow a range of ports using a command like `sudo ufw allow 8000:8100/tcp` for TCP traffic. (/<protocol needs to be at the end of the last port).   

To change a username in Linux, you can use the usermod command. The syntax is `sudo usermod -l new\_username old\_username`, where you replace "new\_username" with the desired username and "old\_username" with the current username   
   
