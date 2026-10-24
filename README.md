# junk2

```
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Invoke-WebRequest https://<real-alias>/captain/api/health/ready -UseBasicParsing | Select-Object StatusCode, Content



```
