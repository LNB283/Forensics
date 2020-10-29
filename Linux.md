# Linux  : Basic commands to perform forensic
### Evidence collection
- [ ] Registers and cache
- [ ] Routing table, arp cache , process table , kernel statistics ,memory
- [ ] Temp system files
- [ ] Disk
- [ ] Remote logging
- [ ] Physical config
- [ ] Network Information
- [ ] Archival media

----------------------
```bash
Without logsm you're being blind
```

### Process
|Description|Command|
|-------|:-----------------|
|||
### Memory
|Description|Command|
|-------|:-----------------|
### Disk
|Description|Command|
|-------|:-----------------|
### Misc
|Description|Command|
|-------|:-----------------|
|No users and groups attached to Files and directories|sudo find / \( -nouser -o -nogroup \) -exec ls -lg {} \;|
|Executable on file system|sudo find / -type f -exec file -p '{}' \; |grep ELF|
|Files modified within x days|find / -mtime x <br />x : days|