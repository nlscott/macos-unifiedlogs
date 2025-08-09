# sudo Commands:


One liner command:
```shell
log show --predicate 'process == "sudo" AND eventMessage CONTAINS "COMMAND"' --last 10m
```

Formatted for readability:
```shell
log show --predicate '
	process == "sudo" 
	AND eventMessage CONTAINS "COMMAND"' \
    --last 10m --style json
```


Example output:
```log
2025-08-09 10:11:55.521570-0400 0x115ddb   Default     0x0                  51184  0    sudo: nicscott : TTY=ttys001 ; PWD=/Users/nicscott ; USER=root ; COMMAND=/bin/ls
```


Example json output:
```json
{
  "timezoneName" : "",
  "messageType" : "Default",
  "eventType" : "logEvent",
  "source" : null,
  "formatString" : "%8s : %s",
  "userID" : 0,
  "activityIdentifier" : 0,
  "subsystem" : "",
  "category" : "",
  "threadID" : 1138139,
  "senderImageUUID" : "6A15F302-EE0B-3EC6-B466-82B675870A4E",
  "backtrace" : {
    "frames" : [
      {
        "imageOffset" : 366276,
        "imageUUID" : "6A15F302-EE0B-3EC6-B466-82B675870A4E"
      }
    ]
  },
  "bootUUID" : "ED40187B-8B76-4555-B78A-E4E689E1EF47",
  "processImagePath" : "\/usr\/bin\/sudo",
  "senderImagePath" : "\/usr\/bin\/sudo",
  "timestamp" : "2025-08-09 10:11:55.521570-0400",
  "machTimestamp" : 5335783484167,
  "eventMessage" : "nicscott : TTY=ttys001 ; PWD=\/Users\/nicscott ; USER=root ; COMMAND=\/bin\/ls",
  "processImageUUID" : "6A15F302-EE0B-3EC6-B466-82B675870A4E",
  "traceID" : 2298404520722436,
  "processID" : 51184,
  "senderProgramCounter" : 366276,
  "parentActivityIdentifier" : 0
}
```