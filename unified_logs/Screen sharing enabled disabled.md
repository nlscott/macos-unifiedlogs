# Screen Sharing Enabled: 

> System Settings > General > Sharing > Screen Sharing

One liner command:

```shell
log show --predicate 'process = "launchd" AND eventMessage CONTAINS "Setting service com.apple.screensharing to enabled"' --last 10m
```


Formatted for readability:
```shell
log show --predicate \
  'process = "launchd" \
  AND eventMessage CONTAINS "Setting service com.apple.screensharing to enabled"' \
  --last 10m --style json
```


Example output:
```log
2025-07-26 18:10:17.745652-0400 0xfa66     Default     0x0                  1      0    launchd: [system:] Setting service com.apple.screensharing to enabled (initiated by smd[379])
```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "",
  "userID" : 2863311530,
  "activityIdentifier" : 0,
  "subsystem" : "system",
  "category" : "",
  "threadID" : 64102,
  "senderImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 203948,
        "imageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5"
      }
    ]
  },
  "bootUUID" : "E312ED28-914E-4C3C-9B9E-4926AFCCD890",
  "processImagePath" : "\/sbin\/launchd",
  "senderImagePath" : "\/sbin\/launchd",
  "timestamp" : "2025-07-26 18:10:17.745652-0400",
  "machTimestamp" : 163259674292,
  "eventMessage" : "Setting service com.apple.screensharing to enabled (initiated by smd[379])",
  "processImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "traceID" : 0,
  "processID" : 1,
  "senderProgramCounter" : 203948,
  "parentActivityIdentifier" : 0
}
``` 



---

# Screen Sharing Disabled:

One liner command:

```shell
log show --predicate 'process = "launchd" AND eventMessage CONTAINS "Setting service com.apple.screensharing to disabled"' --last 10m
```

Formatted for readability:
```shell
log show --predicate \
  'process = "launchd" \
  AND eventMessage CONTAINS "Setting service com.apple.screensharing to disabled"' \
  --last 10m --style json
```



Example Output:
```log
2025-07-26 18:11:41.852585-0400 0xfa66     Default     0x0                  1      0    launchd: [system:] Setting service com.apple.screensharing to disabled (initiated by smd[379])
```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "",
  "userID" : 2863311530,
  "activityIdentifier" : 0,
  "subsystem" : "system",
  "category" : "",
  "threadID" : 64102,
  "senderImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 203948,
        "imageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5"
      }
    ]
  },
  "bootUUID" : "E312ED28-914E-4C3C-9B9E-4926AFCCD890",
  "processImagePath" : "\/sbin\/launchd",
  "senderImagePath" : "\/sbin\/launchd",
  "timestamp" : "2025-07-26 18:11:41.852585-0400",
  "machTimestamp" : 165278240667,
  "eventMessage" : "Setting service com.apple.screensharing to disabled (initiated by smd[379])",
  "processImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "traceID" : 0,
  "processID" : 1,
  "senderProgramCounter" : 203948,
  "parentActivityIdentifier" : 0
}
```