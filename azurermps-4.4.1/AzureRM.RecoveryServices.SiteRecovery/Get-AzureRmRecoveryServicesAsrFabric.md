---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559579"
---
# Get-AzureRmRecoveryServicesAsrFabric

## КРАТКИй обзор
Получение сведений о структуре восстановления сайта Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### По умолчанию (по умолчанию)
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmRecoveryServicesAsrFabric** получает свойства указанной структуры восстановления сайта Azure или всех структур восстановления сайта Azure в хранилище службы восстановления.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

Возвращает все структуры восстановления сайта Azure в хранилище.

## ПАРАМЕТРЫ

### -FriendlyName
Найдите структуру ASR с помощью понятного имени структуры.

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Найдите структуру ASR с помощью имени структуры.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmRecoveryServicesAsrFabric](./New-AzureRmRecoveryServicesAsrFabric.md)

[Remove-AzureRmRecoveryServicesAsrFabric](./Remove-AzureRmRecoveryServicesAsrFabric.md)
