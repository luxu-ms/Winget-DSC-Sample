$repoLocation = 'C:\Workspaces\Winget-DSC-Sample'
Set-Location $repoLocation
git pull *> $null
$ConfigurationFile="$repoLocation\workload.yaml"
& "C:\Program Files\PowerShell\7\pwsh.exe" -MTA -Command "Get-WinGetConfiguration -File $($ConfigurationFile) | Invoke-WinGetConfiguration -AcceptConfigurationAgreements -WarningAction SilentlyContinue" | Out-File -FilePath .\upgrade-software.log
exit 0
