---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 90cafc66857ee2ec94806628b41960eaafaf6e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564299"
---
# Get-AzureRmLoadBalancer

## КРАТКИй обзор
Получает подсистему балансировки нагрузки.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### NOEXPAND (по умолчанию)
```
Get-AzureRmLoadBalancer [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Кройте
```
Get-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmLoadBalancer** получает один или несколько подсистем балансировки нагрузки для Azure, которые содержатся в группе ресурсов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение подсистемы балансировки нагрузки
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer.
Для выполнения этого командлета должна существовать подсистема балансировки нагрузки.

## ПАРАМЕТРЫ

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

### -ExpandResource
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmLoadBalancer](./New-AzureRmLoadBalancer.md)

[Remove-AzureRmLoadBalancer](./Remove-AzureRmLoadBalancer.md)

[Set-AzureRmLoadBalancer](./Set-AzureRmLoadBalancer.md)


