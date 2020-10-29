# Mac  : Basic commands to perform forensic
### Evidences collection
- [ ] Registers and cache
- [ ] Routing table, arp cache , process table , kernel statistics ,memory
- [ ] Temp system files
- [ ] Disk
- [ ] Remote logging
- [ ] Physical config
- [ ] Network Information
- [ ] Archival media

### Information gathering
- System diagnosis
  - sysdiagnose
- System logs
  - Logs MacOS 
----------------------
### Logs MacOS

```bash
Without logsm you're being blind
```

|Description|Command|Comment|
|-------|:-----------------|:-----------------|
|Collect ALL Logs|log show > {path}/{file name}.txt|`Attention`: This command create a file with ALL logs.This file may be really **BIG**.|
|Collect log from a certain period|sudo log collect–start"YYYY-MM-DD" --output <path>|Generate a lorgarchive file.|
|Open the log file|log show <file>||

----------------------
### Location

##### Autorun/Startup
- Agent : /System/Library/LaunchAgents/*
- Daemons: /System/Library/LaunchDaemons/*
- Startup : /System/Library/StartupItems/*

##### System
- System: /var/log/*
- Apple System : /var/log/asl/*
- Audit : /var/audit/*
- Install: /var/log/install.log
- Lastlog: /var/log/lastlog

##### Preferences
- Plist files: /Library/Preferences (use ls -la to see hidden folders)

##### OS
- Version : /System/Library/CoreServices/SystemVersion.plist

##### Software installed
- History: /Library/Receipts/Install History.plist

#### Jobs/Cron
- cron: /usr/lib/cron/tabs/
- jobs: /usr/lib/cron/jobs/

#### Network
- Host: /etc/hosts
- Wireless History: /Library/Preferences/SystemConfiguration/com.apple.airport.preferences.plist
