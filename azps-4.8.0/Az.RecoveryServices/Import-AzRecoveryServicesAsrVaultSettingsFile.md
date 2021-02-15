---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: f71f7e37e4864de10c5387d63c101cd66ed9fd34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398875"
---
# Import-AzRecoveryServicesAsrVaultSettingsFile

## SYNOPSIS
Импортирует указанный файл параметров хранилища ASR, чтобы настроить контекст хранилища (контекст сеанса PowerShell) для последующих операций asR в сеансе PowerShell. 

## СИНТАКСИС

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для **импорта-AzRecoveryServicesAsrVaultSettingsFile** импортируется файл параметров хранилища для восстановления сайта Azure. Файл параметров хранилища используется для настройки контекста хранилища для последующих операций восстановления сайта Azure в текущем сеансе.

## ПРИМЕРЫ

### Пример 1
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

Импорт указанного файла параметров хранилища служб восстановления и возврат параметров импортируемого хранилища.

## PARAMETERS

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
Путь к папке в файле параметров хранилища ASR.
Этот файл можно скачать с портала хранилища служб восстановления и сохранить локально.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

