# Mounted DMG:


One liner command:
```shell
log show --predicate 'process == "kernel" AND eventMessage CONTAINS "mounted"' --last 10m
```

Formatted for readability:
```shell
log show --predicate '
  process == "kernel" 
  AND eventMessage CONTAINS "mounted"' \
  --last 10m --style json
```


Example output:
```log
2025-07-27 15:31:22.695081-0400 0x91f22    Default     0x0                  0      0    kernel: (HFS) hfs: mounted Firefox on device disk4s3
```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "hfs: mounted %s on device %s\n",
  "userID" : 0,
  "activityIdentifier" : 0,
  "subsystem" : "",
  "category" : "",
  "threadID" : 597794,
  "senderImageUUID" : "080CCAD9-1651-3258-B38F-027B76E7DCFE",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 215404,
        "imageUUID" : "080CCAD9-1651-3258-B38F-027B76E7DCFE"
      }
    ]
  },
  "bootUUID" : "E312ED28-914E-4C3C-9B9E-4926AFCCD890",
  "processImagePath" : "\/kernel",
  "senderImagePath" : "\/System\/Library\/Extensions\/HFS.kext\/Contents\/MacOS\/HFS",
  "timestamp" : "2025-07-27 15:31:22.695081-0400",
  "machTimestamp" : 2008018969949,
  "eventMessage" : "hfs: mounted Firefox on device disk4s3",
  "processImageUUID" : "CBC2F718-53E4-3C8D-BEC7-FB6DDC3318E1",
  "traceID" : 176338472796164,
  "processID" : 0,
  "senderProgramCounter" : 215404,
  "parentActivityIdentifier" : 0
} 
```


---
# Unmounting DMG:

One liner command:
```shell
log show --predicate 'process == "UnmountAssistantAgent" AND eventMessage CONTAINS "Volume" AND eventMessage CONTAINS "was unmounted"' --last 10m

```


Formatted for readability:
```shell
log show --predicate '
  process == "UnmountAssistantAgent" 
  AND eventMessage CONTAINS "Volume" 
  AND eventMessage CONTAINS "was unmounted"' \
  --last 10m --style json
```


Example Output:
```log
2025-07-27 15:34:53.935599-0400 0x92cfe    Default     0x0                  28508  0    UnmountAssistantAgent: (loginsupport) [com.apple.UnmountAssistantAgent:IPC] Volume "file:///Volumes/Firefox/" was unmounted

```

Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "%{public}@",
  "userID" : 501,
  "activityIdentifier" : 0,
  "subsystem" : "com.apple.UnmountAssistantAgent",
  "category" : "IPC",
  "threadID" : 601342,
  "senderImageUUID" : "BBC11F3B-0363-3371-A8D3-F2FAE12B6482",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 5292,
        "imageUUID" : "BBC11F3B-0363-3371-A8D3-F2FAE12B6482"
      }
    ]
  },
  "bootUUID" : "E312ED28-914E-4C3C-9B9E-4926AFCCD890",
  "processImagePath" : "\/System\/Library\/CoreServices\/UnmountAssistantAgent.app\/Contents\/MacOS\/UnmountAssistantAgent",
  "senderImagePath" : "\/System\/Library\/PrivateFrameworks\/login.framework\/Versions\/A\/Frameworks\/loginsupport.framework\/Versions\/A\/loginsupport",
  "timestamp" : "2025-07-27 15:34:53.935599-0400",
  "machTimestamp" : 2013088742381,
  "eventMessage" : "Volume \"file:\/\/\/Volumes\/Firefox\/\" was unmounted",
  "processImageUUID" : "D8DFDDA5-476C-3647-AD17-9EB0B25B736E",
  "traceID" : 713394634835099652,
  "processID" : 28508,
  "senderProgramCounter" : 5292,
  "parentActivityIdentifier" : 0
}
```