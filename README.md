# junk2

```
Get-ChildItem C:\inetpub\logs\LogFiles\W3SVC1 | Sort-Object LastWriteTime | Select-Object -Last 1 |
  Get-Content -Tail 50 | Select-String '/captain'


```
