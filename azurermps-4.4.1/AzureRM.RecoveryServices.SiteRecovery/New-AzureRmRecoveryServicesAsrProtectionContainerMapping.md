---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562279"
---
# New-AzureRmRecoveryServicesAsrProtectionContainerMapping

## КРАТКИй обзор
Создание сопоставления контейнера защиты для Azure Site Recovery путем сопоставления указанной политики репликации с указанным контейнером защиты ASR.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### EnterpriseToAzure (по умолчанию)
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** создает сопоставление с помощью заданной политики репликации с заданным контейнером защиты Azure Site Recovery.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

Запускает создание сопоставления контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя сопоставления контейнера защиты.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy (политика)
Указывает объект политики репликации ASR для политики репликации, используемой в сопоставлении.

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PrimaryProtectionContainer
Указывает объект контейнера защиты ASR для основного контейнера защиты, который будет использоваться в сопоставлении.

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryProtectionContainer
Указывает объект контейнера защиты ASR для контейнера защиты восстановления, который будет использоваться в сопоставлении (используется при репликации в расположение для восстановления, которое не является Azure).

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRecoveryServicesAsrProtectionContainerMapping](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
