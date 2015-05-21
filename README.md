# Collect-ServerInfo
This PowerShell script runs a series of WMI and other queries to collect information about Windows servers.

Each server's results are output to a HTML file.

##Parameters
- **-Verbose**, See more detailed progress as the script is running.

##Examples

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

##Credits
Written by: Paul Cunningham

Find me on:

* My Blog:	http://paulcunningham.me
* Twitter:	https://twitter.com/paulcunningham
* LinkedIn:	http://au.linkedin.com/in/cunninghamp/
* Github:	https://github.com/cunninghamp

