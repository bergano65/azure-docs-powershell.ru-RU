---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217889"
---
# Update-AzRecoveryServicesVault

## SYNOPSIS
Обновляет MSI-версию хранилища служб восстановления.

## СИНТАКСИС

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Этот cmdlet используется для добавления или удаления MSI-данных из хранилища служб восстановления. Используйте параметр -IdentityType, чтобы назначить удостоверение SystemAssigned RSVault. Используйте IdentityType None, чтобы удалить MSI из хранилища.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

Этот cmdlet используется для добавления удостоверения SystemAssigned в хранилище служб восстановления.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Указывает имя хранилища служб восстановления, которое нужно обновить.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName

Имя группы ресурсов Azure, в которой находится хранилище служб восстановления.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Тип MSI, который назначен сейфу служб восстановления.

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: SwitchParameter
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

### Microsoft.Azure.Management.RecoveryServices.Models.Vault

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
