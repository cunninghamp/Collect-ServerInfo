# Collect-ServerInfo
This PowerShell script runs a series of WMI and other queries to collect information about Windows servers.

Each server's results are output to a HTML file.

## Parameters
- **-Verbose**, See more detailed progress as the script is running.

## Examples

Collect information about a single server named SERVER1.
```
.\Collect-ServerInfo.ps1 SERVER1
```

Collect information about multiple servers.
```
"SERVER1","SERVER2","SERVER3" | .\Collect-ServerInfo.ps1
```

Collect information about all servers in Active Directory.
```
Get-ADComputer -Filter {OperatingSystem -Like "Windows Server*"} | %{.\Collect-ServerInfo.ps1 $_.DNSHostName}
```

## Download

Download the latest release from [Github](https://github.com/cunninghamp/Collect-ServerInfo/releases/latest) or from the [TechNet Script Gallery](https://gallery.technet.microsoft.com/scriptcenter/PowerShell-Collect-Server-089f1da3).

## Credits
Written by: Paul Cunningham

Find me on:

* My Blog:	https://paulcunningham.me
* Twitter:	https://twitter.com/paulcunningham
* LinkedIn:	https://au.linkedin.com/in/cunninghamp/
* Github:	https://github.com/cunninghamp

Additional contributions by:
* [Nicolas Nowinski](https://github.com/nicknow)
