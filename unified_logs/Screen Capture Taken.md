# Screen Captue Taken:


One liner command:
```shell
log show --predicate 'process == "screencapture" AND subsystem == "com.apple.screencapture" AND eventMessage CONTAINS "Capturing image"' --last 10m

```

Formatted for readability:
```shell
log show --predicate '
    process == "screencapture" 
    AND subsystem == "com.apple.screencapture" 
    AND eventMessage CONTAINS "Capturing image"' \
    --last 10m --style json
```


Example output:
```log
2025-07-27 15:47:10.504275-0400 0x96aa6    Default     0x0                  30612  0    screencapture: [com.apple.screencapture:default] Capturing image

```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "Capturing image",
  "userID" : 501,
  "activityIdentifier" : 0,
  "subsystem" : "com.apple.screencapture",
  "category" : "default",
  "threadID" : 617126,
  "senderImageUUID" : "BB6669E7-A1B7-3807-AF97-FBF5D0D0B4D5",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 279748,
        "imageUUID" : "BB6669E7-A1B7-3807-AF97-FBF5D0D0B4D5"
      }
    ]
  },
  "bootUUID" : "E312ED28-914E-4C3C-9B9E-4926AFCCD890",
  "processImagePath" : "\/usr\/sbin\/screencapture",
  "senderImagePath" : "\/usr\/sbin\/screencapture",
  "timestamp" : "2025-07-27 15:47:10.504275-0400",
  "machTimestamp" : 2030766390595,
  "eventMessage" : "Capturing image",
  "processImageUUID" : "BB6669E7-A1B7-3807-AF97-FBF5D0D0B4D5",
  "traceID" : 2175280710025220,
  "processID" : 30612,
  "senderProgramCounter" : 279748,
  "parentActivityIdentifier" : 0
}
```