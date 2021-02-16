---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226988"
---
# Get-AzRecoveryServicesVaultSettingsFile

## SYNOPSIS
Получает файл параметров хранилища для восстановления сайта Azure.

## СИНТАКСИС

### ForSiteWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefaultWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultTypeWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Get-AzRecoveryServicesVaultSettingsFile** получает файл параметров для хранилища восстановления сайта Azure.

## ПРИМЕРЫ

### Пример 1. Регистрация компьютера с Windows Server или DPM для резервного копирования Azure
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

Первая команда получает хранилище TestVault, а затем сохраняет его в переменной $Vault 01.
Вторая команда задает переменную $CredsPath C:\Downloads.
Последняя команда получает файл учетных данных хранилища для $Vault 01 с учетными данными в службе $CredsPath для резервного копирования Azure.

### Пример 2
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Команда получает файл учетных данных хранилища для $Vault 01 типа хранилища siteRecovery.

### Пример 3. Регистрация компьютера с Windows Server или DPM для резервного копирования Azure
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Команда получает файл учетных данных хранилища для $Vault 01.

## PARAMETERS

### -Backup
Указывает, что файл учетных данных хранилища относится к резервной копии Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certificate
{{Fill Certificate Description}}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Путь к файлу параметров хранилища для восстановления сайта Azure.
Вы можете скачать этот файл с портала восстановления сайта Azure и сохранить его локально.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Указывает имя, которое будет удобно для сайта.
Используйте этот параметр, если вы скачиваете учетные данные хранилища для сайта Hyper-V.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
Определяет идентификатор сайта.
Используйте этот параметр, если вы скачиваете учетные данные хранилища для сайта Hyper-V.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteRecovery
Указывает, что файл учетных данных хранилища относится к восстановлению сайта Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Указывает объект хранилища для восстановления сайта Azure.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## OUTPUTS

### Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzRecoveryServicesVault](./Get-AzRecoveryServicesVault.md)

[New-AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)


