# junk2

```
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Resolve-DnsName xxxx.xxx.com
Test-NetConnection xxxx.xxx.com -Port 443
Invoke-WebRequest https://xxxx.xxx.com/ -UseBasicParsing | Select-Object StatusCode, Content

```
