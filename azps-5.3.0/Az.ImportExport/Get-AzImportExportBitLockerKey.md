---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518686"
---
# Get-AzImportExportBitLockerKey

## SYNOPSIS
Возвращает ключи BitLocker для всех дисков в указанном задание.

## СИНТАКСИС

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## ОПИСАНИЕ
Возвращает ключи BitLocker для всех дисков в указанном задание.

## ПРИМЕРЫ

### Пример 1. Список всех ключей BitLocker в указанном задание ImportExport
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

Этот cmdlet перечисляет все ключи BitLocker в указанном задание ImportExport.

## PARAMETERS

### -AcceptLanguage
Указывает предпочтительный язык для ответа.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Имя задания импорта и экспорта.

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

### -ResourceGroupName
Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.

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

### -SubscriptionId
ИД подписки для пользователя Azure.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey

## ПРИМЕЧАНИЯ

ALIASES

## СВЯЗАННЫЕ ССЫЛКИ

