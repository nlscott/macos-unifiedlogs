# SSH Remote Login Enabled:
> System Settings > General > Sharing > Remote Login


One liner command:
```shell
log show --debug --predicate 'process = "launchd" AND eventMessage CONTAINS "Setting service com.openssh.sshd to enabled"'  --last 10m 
```

Formatted for readability:
```shell
log show --debug --predicate '
  process = "launchd" 
  AND eventMessage CONTAINS "Setting service com.openssh.sshd to enabled"' \
  --last 10m --style json
```


Example output:
```log
2025-07-26 15:47:46.559712-0400 0x118dc8   Default     0x0                  1      0    launchd: [system:] Setting service com.openssh.sshd to enabled (initiated by smd[389])
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
  "threadID" : 1150408,
  "senderImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 203948,
        "imageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5"
      }
    ]
  },
  "bootUUID" : "E71CD419-CFCF-4475-B904-E1C404B09D12",
  "processImagePath" : "\/sbin\/launchd",
  "senderImagePath" : "\/sbin\/launchd",
  "timestamp" : "2025-07-26 15:47:46.559712-0400",
  "machTimestamp" : 3688744984970,
  "eventMessage" : "Setting service com.openssh.sshd to enabled (initiated by smd[389])",
  "processImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "traceID" : 0,
  "processID" : 1,
  "senderProgramCounter" : 203948,
  "parentActivityIdentifier" : 0
} 
```


---
# SSH Remote Login Disabled:

One liner command:
```shell
log show --debug --predicate 'process = "launchd" AND eventMessage CONTAINS "Setting service com.openssh.sshd to disabled"' --last 10m
```


Formatted for readability:
```shell
log show --debug --predicate '
    process = "launchd" 
    AND eventMessage CONTAINS "Setting service com.openssh.sshd to disabled"' \
    --last 10m --style json
```


Example Output:
```log
# 2025-07-26 15:47:01.175910-0400 0x118eb5   Default     0x0                  1      0    launchd: [system:] Setting service com.openssh.sshd to disabled (initiated by smd[389])
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
  "threadID" : 1150408,
  "senderImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 203948,
        "imageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5"
      }
    ]
  },
  "bootUUID" : "E71CD419-CFCF-4475-B904-E1C404B09D12",
  "processImagePath" : "\/sbin\/launchd",
  "senderImagePath" : "\/sbin\/launchd",
  "timestamp" : "2025-07-26 15:49:35.763604-0400",
  "machTimestamp" : 3691365878378,
  "eventMessage" : "Setting service com.openssh.sshd to disabled (initiated by smd[389])",
  "processImageUUID" : "05BA185B-9D21-3EE8-B7D8-5CE21382B5E5",
  "traceID" : 0,
  "processID" : 1,
  "senderProgramCounter" : 203948,
  "parentActivityIdentifier" : 0
}
```