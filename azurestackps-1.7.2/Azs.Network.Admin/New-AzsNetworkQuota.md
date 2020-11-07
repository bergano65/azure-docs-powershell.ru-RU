---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc762c4b7d932f682f77e2df6586c773e0f22e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720108"
---
# New-AzsNetworkQuota

## КРАТКИй обзор
Создание или обновление квоты.

## Максимальное

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Создание или обновление квоты.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

Создание новой сетевой квоты со всеми значениями по умолчанию.

### --------------------------ПРИМЕР 2--------------------------
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

Создание новой сетевой квоты с нестандартными значениями квоты.

## ПАРАМЕТРЫ

### -Location
Расположение ресурса.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxLoadBalancersPerSubscription
Максимально допустимое количество подсистем балансировки нагрузки для каждой подписки.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxNicsPerSubscription
Максимальные сетевые адаптеры, разрешенные на подписку.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPublicIpsPerSubscription
Максимальное количество общедоступных IP-адресов, разрешенных для подписки.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSecurityGroupsPerSubscription
Максимальное количество групп безопасности, разрешенных на подписку.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxVirtualNetworkGatewayConnectionsPerSubscription
Максимальное количество подключений к шлюзу виртуальной сети, разрешенных для одной подписки.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxVirtualNetworkGatewaysPerSubscription
Максимальное количество шлюзов виртуальных сетей, разрешенных для каждой подписки.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxVnetsPerSubscription
Максимальное число виртуальных сетей, разрешенных на подписку.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationPhase
Устаревшие.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя ресурса сетевой квоты.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. Network. admin. Models. Quota

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

