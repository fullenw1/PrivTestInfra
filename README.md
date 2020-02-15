# PrivTestInfra

This module creates a private test infrastructure on top of Hyper-V 2019.

The test infrastructure will contain the following VMs:
- Active Directory Domain Controller with all FSMO roles
- Active Directory Domain Controller with no FSMO role
- Cluster of File Server
- Router
- Web Server containing:
  - DSC/Datum
- Web Server containing:
  - NuGet server
- Web Server containing:
  - Private PS Gallery
- MS SQL 2019
- MS Exchange 2019
- WSUS
- DHCP server
- SharePoint
- Windows Server 2016 GUI
- Windows Server 2016 Core
- Windows Server 2019 GUI
- Windows Server 2019 Core
- Windows 10

# Common configuration

All computers contain:
- .Net Core 3.1
- PowerShell 7
- Chocolatey

# Computer names and network IPs:

You can either specify names and IPs or they will be set according to the following table:

|Computer Name|IP address|Computer usage|
|---|---|---|
|Router|10.0.0.1|Router between the network outside the Hyper-V host and VMs indside|
|DHCP01|10.0.0.2|File Server|
|DC01|10.0.0.11|Domain Controller with all FSMO roles and DNS service|
|DC02|10.0.0.12|Domain Controller with no FSMO roles and DNS service|
|FS|10.0.0.20|VIP of the clustered file server|
|FS01|10.0.0.21|File Server|
|FS02|10.0.0.22|File Server|
|Web01|10.0.0.31|Web Server - DSC server|
|Web02|10.0.0.32|Web Server - Nuget server|
|Web03|10.0.0.33|Web Server - Private PSGallery server|
|SQL|10.0.0.40|VIP of the clustered SQL server|
|SQL01|10.0.0.41|MS SQL Server|
|SQL02|10.0.0.42|MS SQL Server|
|EX01|10.0.0.51|Exchange Server|
|EX02|10.0.0.52|Exchange Server|
|SP01|10.0.0.61|Sharepoint Server|
|SP02|10.0.0.61|Sharepoint Server|
|W2K19C|10.0.0.71|Windows Server 2019 Core|
|W2K19G|10.0.0.72|Windows Server 2019 GUI|
|W2K16C|10.0.0.73|Windows Server 2016 Core|
|W2K16G|10.0.0.74|Windows Server 2016 GUI|
|Win10|10.0.0.75|Windows 10|

# Licences:
None of those operating systems and softwares are licenced.  
Thus they will stop functioning at the end of the trial period.
