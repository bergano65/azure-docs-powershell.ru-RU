---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562259"
---
# Remove-AzureRmRecoveryServicesAsrPolicy

## КРАТКИй обзор
Удаляет указанную политику репликации ASR из хранилища служб восстановления.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmRecoveryServicesAsrPolicy** удалил указанную политику репликации из хранилища служб восстановления.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

Запускает удаление указанной политики репликации и возвращает задание ASR, используемое для отслеживания операции.

## ПАРАМЕТРЫ

### -InputObject
Входной объект для командлета: объект политики репликации ASR, соответствующий политике репликации, которую нужно удалить.

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy

## НАПРЯЖЕНИЕ

### System. Object

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRecoveryServicesAsrPolicy](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[New-AzureRmRecoveryServicesAsrPolicy](./New-AzureRmRecoveryServicesAsrPolicy.md)
