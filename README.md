# Winget-DSC-Sample
This is the repository that include some DSC configuration.

| File Name | Description |
| -- | -- |
| workload.yaml | The PowerShell DSC configuration file that help the user install the software e.g. notepad++ |
| winget-dsc-devbox.yaml | Dev Box customization configuration file used to install software by Winget DSC task |
| upgrade-software.ps1 | PowerShell script used in the Intune PowerShell script to trigger the Dev Box to install by Winget DSC |
| devbox-update.yaml | TBD |

## How to use
### Scenario 1
In the Dev Box developer portal, upload the winget-dsc-devbox.yaml to provision the dev box. The dev box will install the software that defined in workload.yaml.

### Scenario 2
In the Intune portal, create the platform script and upload upgrade-software.ps1, this will trigger the related dev box to install.
Note: Create the dynamic device group if you want to only trigger the limited dev boxes. e.g. only in one dev box pool or project.