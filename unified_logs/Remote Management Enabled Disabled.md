# Remote Management Enabled:
> System Settings > General > Sharing > Remote Management


One liner command:
```shell
log show --debug --predicate 'process = "SSMenuAgent" AND eventMessage CONTAINS "remoteManagementEnabled"'  --last 10m 
```

Formatted for readability:
```shell
log show --debug --predicate '
    process = "SSMenuAgent" 
    AND eventMessage CONTAINS "remoteManagementEnabled"'  \
    --last 10m --style json
```


Example output:
```log
2025-07-27 15:41:33.057177-0400 0x94ab7    Default     0x0                  29005  0    SSMenuAgent: remoteManagementEnabled
```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "remoteManagementEnabled",
  "userID" : 501,
  "activityIdentifier" : 0,
  "subsystem" : "",
  "category" : "",
  "threadID" : 608951,
  "senderImageUUID" : "4C078188-0FEC-3D40-879C-662E369AE81A",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 51920,
        "imageUUID" : "4C078188-0FEC-3D40-879C-662E369AE81A"
      }
    ]
  },
  "bootUUID" : "E312ED28-914E-4C3C-9B9E-4926AFCCD890",
  "processImagePath" : "\/System\/Library\/CoreServices\/RemoteManagement\/SSMenuAgent.app\/Contents\/MacOS\/SSMenuAgent",
  "senderImagePath" : "\/System\/Library\/CoreServices\/RemoteManagement\/SSMenuAgent.app\/Contents\/MacOS\/SSMenuAgent",
  "timestamp" : "2025-07-27 15:41:33.057177-0400",
  "machTimestamp" : 2022667660237,
  "eventMessage" : "remoteManagementEnabled",
  "processImageUUID" : "4C078188-0FEC-3D40-879C-662E369AE81A",
  "traceID" : 604357733253124,
  "processID" : 29005,
  "senderProgramCounter" : 51920,
  "parentActivityIdentifier" : 0
} 
```


---
# Remote Management Disabled:

One liner command:
```shell
log show --debug --predicate 'process = "SSMenuAgent" AND eventMessage CONTAINS "setAgentInactive method called"'  --last 10m 
```


Formatted for readability:
```shell
log show --debug --predicate '
    process = "SSMenuAgent" 
    AND eventMessage CONTAINS "setAgentInactive method called"'  \
    --last 10m --style json
```


Example Output:
```log
2025-07-27 15:43:14.280885-0400 0x95366    Default     0x0                  29005  0    SSMenuAgent: setAgentInactive method called

```

Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "setAgentInactive method called",
  "userID" : 501,
  "activityIdentifier" : 0,
  "subsystem" : "",
  "category" : "",
  "threadID" : 611555,
  "senderImageUUID" : "4C078188-0FEC-3D40-879C-662E369AE81A",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 82468,
        "imageUUID" : "4C078188-0FEC-3D40-879C-662E369AE81A"
      }
    ]
  },
  "bootUUID" : "E312ED28-914E-4C3C-9B9E-4926AFCCD890",
  "processImagePath" : "\/System\/Library\/CoreServices\/RemoteManagement\/SSMenuAgent.app\/Contents\/MacOS\/SSMenuAgent",
  "senderImagePath" : "\/System\/Library\/CoreServices\/RemoteManagement\/SSMenuAgent.app\/Contents\/MacOS\/SSMenuAgent",
  "timestamp" : "2025-07-27 15:43:24.402701-0400",
  "machTimestamp" : 2025339952819,
  "eventMessage" : "setAgentInactive method called",
  "processImageUUID" : "4C078188-0FEC-3D40-879C-662E369AE81A",
  "traceID" : 620850407669764,
  "processID" : 29005,
  "senderProgramCounter" : 82468,
  "parentActivityIdentifier" : 0
}    
```