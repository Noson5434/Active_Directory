# 01 Installing the Domain Controller

1. Use `sconfig` to:
    - Change the hostname
    - Change the IP Address to statis
    - Change the DNS Server to our own IP Address

2. Install the Active Directory Windows Feature

```shell
Install-WindowsFeature AD-Domain-Services -IncludeManagementServices
```

```
Get-NetIPAddress
```

# Joining the Workstation to the domain

```
Add-Computer -DomainName xyz.com -Credential (Get-Credential) -Force -Restart
```