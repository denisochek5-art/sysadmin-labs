Get-Module ActiveDirectory -ListAvailable
Import-Module ActiveDirectory

Get-ADDomain
Get-ADUser -Filter * -SearchBase "OU=Users,DC=lab,DC=local" | Select Name,SamAccountName
Get-ADUser denis -Properties * | Select Name,Enabled,LastLogonDate
New-ADUser -Name "Test User" -SamAccountName test1 -Enabled $true -AccountPassword (Read-Host -AsSecureString)
Enable-ADAccount test1
Disable-ADAccount test1
Get-ADGroupMember "Domain Admins"
Get-Service
Get-Service -Name sshd
Start-Service sshd
Stop-Service sshd
Restart-Service sshd
Set-Service sshd -StartupType Automatic
Get-CimInstance Win32_Service | Select Name,State,StartMode
Get-WinEvent -ListLog * | Select -First 20 LogName,RecordCount
Get-WinEvent -LogName System -MaxEvents 20
Get-WinEvent -FilterHashtable @{LogName="System"; StartTime=(Get-Date).AddHours(-2)} | Select TimeCreated,Id,LevelDisplayName,Message
Get-WinEvent -FilterHashtable @{LogName="Security"; Id=4624} -MaxEvents 10  # logon success
