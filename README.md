# junk2

```
Get-WebGlobalModule | Where-Object Name -match 'Rewrite|ApplicationRequestRouting' | Select-Object Name

$files = @("$env:windir\System32\inetsrv\config\applicationHost.config") +
  (& "$env:windir\System32\inetsrv\appcmd.exe" list vdir /text:physicalPath |
    ForEach-Object { [Environment]::ExpandEnvironmentVariables($_) } | Sort-Object -Unique |
    ForEach-Object { Get-ChildItem $_ -Recurse -Filter web.config -ErrorAction SilentlyContinue } |
    ForEach-Object FullName)
$files | Select-String -Pattern 'url="https?://' | Format-Table Path, LineNumber, Line -AutoSize -Wrap


```
