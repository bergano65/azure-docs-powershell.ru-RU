---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/stop-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 44875207b5a4317b2ceb9a0284a3818a6be36298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557127"
---
# Stop-AzureRmSiteRecoveryJob

## КРАТКИй обзор
Остановка задания по восстановлению сайта.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByObject (по умолчанию)
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Stop-AzureRmSiteRecoveryJob** останавливает задание Azure Site Recovery.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

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

### -Job
Указывает объект задания для восстановления сайта, который нужно остановить.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Указывает уникальное имя задания для восстановления сайта, которое нужно остановить.

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

### ASRJob
Параметр "задание" принимает значение типа "ASRJob" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSiteRecoveryJob](./Get-AzureRmSiteRecoveryJob.md)

[Restarting-AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[Возобновить — AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)
