# battery capacity and time:

## battery capacity

One liner command:

```shell
log show --predicate 'process == "powerd" AND category == "battery" AND eventMessage CONTAINS "Capacity"' --last 10m
```

Formatted for readability:
```shell
log show --predicate '
    process == "powerd" 
    AND category == "battery" 
    AND eventMessage CONTAINS "Capacity"' \
    --style json --last 10m
```


Example output:
```log
2025-08-09 10:33:00.064883-0400 0x11b271   Default     0x0                  602    8    powerd: [com.apple.powerd:battery] Battery capacity change posted(0x80063). Capacity:99 Source:Batt
```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "Battery capacity change posted(0x%llx). Capacity:%d Source:%{public}s\n",
  "userID" : 0,
  "activityIdentifier" : 0,
  "subsystem" : "com.apple.powerd",
  "category" : "battery",
  "threadID" : 1158874,
  "senderImageUUID" : "36FAA0CA-848B-3287-B23D-323F2A4C63EE",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 74096,
        "imageUUID" : "36FAA0CA-848B-3287-B23D-323F2A4C63EE"
      }
    ]
  },
  "bootUUID" : "ED40187B-8B76-4555-B78A-E4E689E1EF47",
  "processImagePath" : "\/System\/Library\/CoreServices\/powerd.bundle\/powerd",
  "senderImagePath" : "\/System\/Library\/CoreServices\/powerd.bundle\/powerd",
  "timestamp" : "2025-08-09 10:41:00.069263-0400",
  "machTimestamp" : 5377653386596,
  "eventMessage" : "Battery capacity change posted(0x80061). Capacity:97 Source:Batt",
  "processImageUUID" : "36FAA0CA-848B-3287-B23D-323F2A4C63EE",
  "traceID" : 2045882002440196,
  "processID" : 602,
  "senderProgramCounter" : 74096,
  "parentActivityIdentifier" : 0
}
```


---
## battery time remaining

One liner command:

```shell
og show --predicate 'process == "powerd" AND category == "battery" AND eventMessage CONTAINS "Battery time remaining"' --last 10m
```

Formatted for readability:
```shell
log show --predicate '
    process == "powerd" 
    AND category == "battery" 
    AND eventMessage CONTAINS "Capacity"' \
    --style json --last 10m
```


Example output:
```log
2025-08-09 10:44:00.067615-0400 0x11c1f6   Default     0x0                  602    8    powerd: [com.apple.powerd:battery] Battery time remaining posted(0x200000000480183) Time:387 Source:Batt
```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "Battery time remaining posted(0x%llx) Time:%d Source:%{public}s\n",
  "userID" : 0,
  "activityIdentifier" : 0,
  "subsystem" : "com.apple.powerd",
  "category" : "battery",
  "threadID" : 1163766,
  "senderImageUUID" : "36FAA0CA-848B-3287-B23D-323F2A4C63EE",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 73432,
        "imageUUID" : "36FAA0CA-848B-3287-B23D-323F2A4C63EE"
      }
    ]
  },
  "bootUUID" : "ED40187B-8B76-4555-B78A-E4E689E1EF47",
  "processImagePath" : "\/System\/Library\/CoreServices\/powerd.bundle\/powerd",
  "senderImagePath" : "\/System\/Library\/CoreServices\/powerd.bundle\/powerd",
  "timestamp" : "2025-08-09 10:45:00.071744-0400",
  "machTimestamp" : 5383413446120,
  "eventMessage" : "Battery time remaining posted(0x200000000480179) Time:377 Source:Batt",
  "processImageUUID" : "36FAA0CA-848B-3287-B23D-323F2A4C63EE",
  "traceID" : 2045349426495492,
  "processID" : 602,
  "senderProgramCounter" : 73432,
  "parentActivityIdentifier" : 0
}
```