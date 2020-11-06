---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562083"
---
# Start-AzureRmSiteRecoveryApplyRecoveryPoint

## КРАТКИй обзор
Изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем фиксировать операцию перехода на другой ресурс.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
**Start-AzureRmSiteRecoveryApplyRecoveryPoint** изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем она зафиксирует операцию перемещения.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -DataEncryptionPrimaryCertFile
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

### -DataEncryptionSecondaryCertFile
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

### -RecoveryPoint
Указывает объект точки восстановления, измененный этим командлетом.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationProtectedItem
Указывает объект защищенного элемента репликации.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### ASRReplicationProtectedItem
Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Командлеты Azure Site Recovery](./AzureRM.SiteRecovery.md)
