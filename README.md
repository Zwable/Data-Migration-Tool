Known errors:

Recieving the USMT error 71 means that you have done something wrong with the folder permissions.  
Recieving the USMT error 37, don’t run this tool on a server you fool 😉  
Recieving the USMT error 26, check volume size of the backup destination.

Changes:
1.14  
-Changed variables from static to env: variable in the deployment script.  
-Changed logic in when prompts are shown.  
-Changed branding.  

1.13  
-Added the option to backup only domain users who has logged in within defined days. The variables to enable/configure this option is in the top of the Deploy-Application.ps1 script called:  
$BackupDomainUsersOnly  
$BackupDomainUsersLoginWithinDays  
-Changes where made to the Start-UserStateMigrationTool function in the AppDeployToolkitExtensions.ps1 script.

1.12  
-Removed the Convert-FromString function from the Export-WLANProfiles function in the AppDeployToolkitExtensions.ps1 as it was dependent on PowerShell version >= 5.0.  
-Added a check to only export WLAN profiles when running on a psysical machine.

1.11  
-Removed the parameter -NoAppSettings switch from the Start-UserStateMigrationTool function call in the Deploy-Application.ps1 script.  
-Removed the custom XML from the command line string in the Start-UserStateMigrationTool function located in the AppDeployToolkitExtensions.ps1

1.1  
-Changed the current user variable to be the current user session instead of running context. Was an issue if running as system.

1.0
