---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247192"
---
# Unregister-AzStackHCI

## КРАТКИй обзор
Unregister-AzStackHCI удаляет облачный ресурс Microsoft. AzureStackHCI, представляющий локальный кластер, и отменяет регистрацию локального кластера с помощью Azure.
Зарегистрированные данные, доступные в кластере, используются для отмены регистрации кластера, если не переданы никакие параметры.

## Максимальное

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Unregister-AzStackHCI удаляет облачный ресурс Microsoft. AzureStackHCI, представляющий локальный кластер, и отменяет регистрацию локального кластера с помощью Azure.
Зарегистрированные данные, доступные в кластере, используются для отмены регистрации кластера, если не переданы никакие параметры.

## ИЛЛЮСТРИРУЮТ

### ПРИМЕР 1
```
Invoking on one of the cluster node
```

\>Отмена регистрации C:\PS — результат AzStackHCI: успешное удаление

### ПРИМЕР 2
```
Invoking from the management node
```

C:\PS \> Unregister-AzStackHCI-ComputerName ClusterNode1 результат: успешно

### ПРИМЕР 3
```
Invoking from WAC
```

C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. Ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false результат: успех

### ПРИМЕР 4
```
Invoking with all the parameters
```

C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG.. Ere =-GraphAccessToken ACee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-credentials Get-Credential result: Success (успешно)

## ПАРАМЕТРЫ

### -SubscriptionId
Указывает подписку Azure для создания ресурса.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Указывает имя ресурса, созданного в Azure.
Если не указано, используется локальное имя кластера.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Указывает Azure TenantId.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Если не указано, \<LocalClusterName\> RG будет использоваться в качестве имени группы ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Указывает маркер доступа ARM.
Указав этот параметр вместе с GraphAccessToken и AccountId, вы не сможете интерактивно войти в Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Указывает маркер доступа Graph.
Указав этот параметр вместе с ArmAccessToken и AccountId, вы не сможете интерактивно войти в Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
Указывает маркер доступа ARM.
Если указать этот параметр вместе с ArmAccessToken и GraphAccessToken, вы не сможете интерактивно войти в Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Указывает среду Azure.
По умолчанию используется AzureCloud.
Допустимые значения — AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Указывает один из узлов кластера в локальном кластере, который регистрируется в Azure.

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

### -Credential
Указывает учетные данные для ComputerName.
По умолчанию — текущий пользователь, выполняющий командлет.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### PSCustomObject. Возвращает следующие свойства в PSCustomObject
### Результат: "успешно" или "не пройден" или "отменено".
## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
