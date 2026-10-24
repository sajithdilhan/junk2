# junk2

```
Get-Content C:\Windows\System32\drivers\etc\hosts | Select-String -NotMatch '^\s*#'
Resolve-DnsName <alias>
ipconfig /all | Select-String 'IPv4'
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
(Invoke-WebRequest https://<alias>/captain/ -UseBasicParsing).StatusCode


```
