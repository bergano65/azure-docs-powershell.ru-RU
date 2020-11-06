---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566150"
---
# New-AzureRmRecoveryServicesAsrNetworkMapping

## КРАТКИй обзор
Создание сетевого сопоставления ASR между двумя сетями.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### EnterpriseToEnterprise (по умолчанию)
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AzureToAzure
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnterpriseToAzure
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmRecoveryServicesAsrNetworkMapping** запускает операцию создания сетевого сопоставления ASR из двух сетей и возвращает объект задания ASR для задания ASR, используемого для отслеживания операции.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

Запускает операцию создания сетевого сопоставления, используя указанные имя, основную сеть и сети восстановления, и возвращает задание ASR, чтобы отслеживать операцию.

### Пример 2
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

Запускает сетевое сопоставление для создания, используя указанные имя, основную сеть и сети восстановления, и возвращает задание ASR, чтобы отследить операцию (в сценарии Azure to Azure).

## ПАРАМЕТРЫ

### -AzureToAzure
Параметр Switch, указывающий, что создаваемое Сетевое сопоставление будет использоваться для репликации виртуальных машин Azure между двумя областями Azure.

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя сопоставления сети ASR для создания.

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

### -PrimaryAzureNetworkId
Указывает идентификатор виртуальной сети Azure для основной сети для сопоставления.

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryFabric
Specifes с помощью ASR Fabric, на котором должно быть создано сопоставление.

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNetwork
Задает основной объект сети для сопоставления сети ASR.

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryAzureNetworkId
Указывает идентификатор сети Azure Recovery Network для сетевого сопоставления.

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryFabric
Объект фабрики восстановления сайта Azure, соответствующий региону восстановления Azure.

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryNetwork
Указывает сетевой объект для восстановления сетевого сопоставления ASR.

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRecoveryServicesAsrNetworkMapping](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[Remove-AzureRmRecoveryServicesAsrNetworkMapping](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
