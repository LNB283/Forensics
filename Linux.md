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
|Process information|ls -al /proc/[PID]|
|Capture Process Data|p /proc/PID /Destination folder/<br />Attention: This command generates a huge file. It's recommended to have enough space disk before launch this command|
|Process information|cat /proc/PID/comm<br />cat /proc/PID/cmdline|
|environment variables informaiton|strings /proc/PID/environ|
|Process using|ls -al /proc/PID/fd <br />cat /proc/PID/maps|
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
|Sticky bit|sudo find / -type f \( -perm -04000 -o -perm -02000 \) -exec ls -lg {} \;|

