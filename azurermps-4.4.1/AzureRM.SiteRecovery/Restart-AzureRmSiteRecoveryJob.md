---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 1b17284a5b0dfbdc8ee031df714c9f9f03533697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567045"
---
# Restart-AzureRmSiteRecoveryJob

## КРАТКИй обзор
Перезапускает задание восстановления сайта Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByObject (по умолчанию)
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **restart-AzureRmSiteRecoveryJob** перезапустит задание восстановления сайта Azure.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -Job
Указывает объект задания по восстановлению сайта.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Указывает уникальное имя задания.

```yaml
Type: System.String
Parameter Sets: ByName
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

### ASRJob
Параметр "задание" принимает значение типа "ASRJob" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSiteRecoveryJob](./Get-AzureRmSiteRecoveryJob.md)

[Возобновить — AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[Остановить-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
