---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562112"
---
# Get-AzureRmSiteRecoveryFabric

## КРАТКИй обзор
Получение свойств структуры восстановления сайта Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### По умолчанию (по умолчанию)
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmSiteRecoveryFabric** получает свойства указанной структуры восстановления сайта Azure или всех структур восстановления сайта Azure в хранилище службы восстановления.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -FriendlyName
Указывает понятное имя структуры восстановления сайта Azure.

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя структуры восстановления сайта Azure.

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

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmSiteRecoveryFabric](./New-AzureRmSiteRecoveryFabric.md)

[Remove-AzureRmSiteRecoveryFabric](./Remove-AzureRmSiteRecoveryFabric.md)
