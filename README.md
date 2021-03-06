# EasyPeasy
Find accounts using common and default passwords in Active Directory.

Contributions:

Invoke-parallel contributed by @RamblingCookieMonster

PowerView recon module contributed by the PowerSploit team.

## Execution
### Dot source the code and run
```powershell
. .\EasyPeasy.ps1
EeasyPeasy
```

### Get information about the module
```powershell
Get-Help EasyPeasy
```
Make sure `Set-ExecutionPolicy` is set to `Bypass` to avoid alerts


## Usage


### Scan for common passwords for all domain accounts 
(not just privileged accounts)
```powershell
EasyPeasy -All
```
### Execute a detailed scan
Find where accounts with common passwords have access to and where those accoutns are currently logged on to.
```powershell
EasyPeasy -Detailed
```

### Use your own common passwords dictionary 
The file must be a csv file with the clear text password in column 1 and the corresponding NTLM hash in column.
```powershell
EasyPeasy -Hash_File <full CSV file path>
```

