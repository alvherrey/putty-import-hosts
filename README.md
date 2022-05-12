# putty-import-hosts
Import hosts to putty from csv file

## Populate out dir with all putty sessions
powershell -executionpolicy bypass .\putty_import_hosts.ps1

## Export putty sesions CMD
regedit /e "%USERPROFILE%\Desktop\putty-sessions.reg" HKEY_CURRENT_USER\Software\SimonTatham\PuTTY\Sessions
## Export putty sesions POWERSHELL
reg export HKCU\Software\SimonTatham\PuTTY\Sessions ([Environment]::GetFolderPath("Desktop") + "\putty-sessions.reg")