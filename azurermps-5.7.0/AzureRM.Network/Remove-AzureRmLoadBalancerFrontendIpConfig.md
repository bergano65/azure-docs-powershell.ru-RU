---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 155d2ab8a1e43264a3598a0ea44011ebb66e9e58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563451"
---
# Remove-AzureRmLoadBalancerFrontendIpConfig

## КРАТКИй обзор
Удаляет интерфейсную конфигурацию IP из подсистемы балансировки нагрузки.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmLoadBalancerFrontendIpConfig** удаляет IP-конфигурацию интерфейсов из подсистемы балансировки нагрузки Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление интерфейсной конфигурации IP из подсистемы балансировки нагрузки
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

Первая команда получает подсистему балансировки нагрузки, связанную с интерфейсной IP-конфигурацией, которую вы хотите удалить, и сохраняет ее в переменной $loadbalancer.

Вторая команда удаляет связанную конфигурацию IP-интерфейсов из подсистемы балансировки нагрузки в $loadbalancer.

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

### -Подсистема балансировки
Указывает подсистему балансировки нагрузки, которая содержит интерфейсную конфигурацию IP-интерфейса, которую нужно удалить.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя удаляемой конфигурации переднего IP-адреса.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSLoadBalancer
Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmLoadBalancerFrontendIpConfig](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[Get-AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[Get-AzureRmLoadBalancerFrontendIpConfig](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[New-AzureRmLoadBalancerFrontendIpConfig](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[Set-AzureRmLoadBalancerFrontendIpConfig](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


